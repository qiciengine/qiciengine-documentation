# 简易服务器
提供简单的登录、登出、数据保存功能，可自定义通信消息实现自定义的通信功能。

## 下载
[server zip](http://docs.zuoyouxi.com/manual/Plugin/server.zip)

## 安装需求
* [nodejs](https://nodejs.org/en/)
* [redis](http://redis.io/)

## 启动步骤：
* 在 package.json 所在目录执行 npm install，下载安装 server 所依赖的 js 库
* 默认的启动配置文件为 config/Config.js，可自定义启动配置文件，运行不同的游戏进程，比如：node gs/StartGs.js config/Config2.js --repl 	
* window 下执行 start_server.bat；linux 下执行 ./start_server.sh；或手动执行 node gs/StartGs.js --repl，启动单进程服务
* 在 linux 下执行 start_cluster.sh，可启动 cluster 多进程集群服务，实现负载分担(linux 下使用 pm2 进行进程管理，需要先 npm install pm2 -g)  


## 目录结构
````
config : 存放配置文件
global : 存放全局通用的功能代码
    base : 存放全局函数
	include : 存放全局定义
	clone : 存放全局对象
	daemons : 存放全局模块
	cmds : 存放全局的消息处理代码
gs : 存放 game server 相关的功能代码  
    base : 存放 gs 相关的全局函数
	include : 存放 gs 相关的定义
	clone : 存放 gs 相关的对象
	daemons : 存放 gs 相关的模块
	cmds : 存放 gs 相关的消息处理代码
logs : 存放服务器日志文件
````

## 服务器框架功能  
* [http 消息通信及派发机制](#http-消息通信及派发机制)  
* [websocket 消息通信及派发机制](#websocket-消息通信及派发机制)  
* [redis 数据库支持](#redis-数据库支持)  
* [mysql 数据库支持](#mysql-数据库支持)  
* [日志系统](#日志系统)  
* [脚本异常报错捕获机制](#脚本异常报错捕获机制)  
* [win32 脚本交互控制台](#win32-脚本交互控制台)  
* [支持 telnet 后台机制](#支持-telnet-后台机制)  
* [简易的帐号登录、登出、保存数据功能](#简易的帐号登录、登出、保存数据功能)  
* [微信SDK支持](#微信SDK支持)

### http 消息通信及派发机制  
文件名：*global/daemons/Communicate.js*    
模块名：*COMMUNICATE_D*   
主要接口：  
* `COMMUNICATE_D.listen(port)`    
监听端口，服务进程启动时会根据 Config/Config.js 中配置的 port 调用 listen 开始监听端口。	 
* `COMMUNICATE_D.sendMessage(res, jsonData)`   
发送回复数据给前端。  
参数 res 为 http 连接中的 response 对象；参数 jsonData 为回复的数据，json格式。   
* `COMMUNICATE_D.registerCmd(cmd, func)`   
注册消息处理函数。在 global 和 gs 目录下的 cmds 目录中放置各个消息处理文件，启动时会加载这些消息处理文件，会自动调用该接口注册消息处理函数。   
参数 cmd 为消息名; func 为收到消息的回调函数，格式为：main(res, para)。其中 para 为 json 格式数据。  

### websocket 消息通信及派发机制  
文件名：*global/daemons/Communicate.js*    
模块名：*COMMUNICATE_D*   
主要接口：  
* `COMMUNICATE_D.listen(port)`    
监听端口，服务进程启动时会根据 Config/Config.js 中配置的 port 调用 listen 开始监听端口。  	 
* `COMMUNICATE_D.sendSocketMessage(socket, ...)`   
发送 socket 消息给前端。  
参数 socket 为 socket io 对象；后面为可选的消息参数   
* `COMMUNICATE_D.registerSocketCmd(cmd, func)`   
注册 socket 消息处理函数。在 global/cmds 和 gs/cmds 目录下的 socket 目录中放置各个 socket 消息处理文件，启动时会加载这些消息处理文件，会自动调用该接口注册消息处理函数。   
参数 cmd 为消息名; func 为收到消息的回调函数，格式为：main(socket, ...)  

### redis 数据库支持  
进程启动时，根据 Config/Config.js 中的 redis 配置信息，自动连接 redis 服务器。支持同时配置多个 redis 服务器。  

文件名：*global/daemons/Redis.js*    
模块名：*REDIS_D*   
主要接口：  
* `REDIS_D.redisOper(dbName, cmd, cmdArg)`    
````
/**
 * 执行 redis 命令，返回 Promise 对象
 * @method REDIS_D.redisOper
 * @param {string} dbName - Config 配置文件中配置的 redisDb
 * @param {string} cmd - redis cmd
 * @param {array} cmdArg - redis 命令参数
 *    比如 hset id key value 这条 redis 语句，cmd 为 hset，cmdArg 为 [id, key, value]
 */ 
````  

* `REDIS_D.redisMulti(dbName, cmdList)`   
````
/**
 * 执行 redis multi 多事务命令，返回 Promise 对象
 * @method REDIS_D.redisMulti
 * @param {string} dbName - Config 配置文件中配置的 redisDb
 * @param {array} cmdList - 多条 redis 命令
 *    比如 hset id key value; hset id2 key value 这2条 redis 语句，
 *    cmdList 为 [ ['hset', 'id', key, value], ['hset', 'id', key, value] ]
 */    
````  

### mysql 数据库支持  
进程启动时，根据 Config/Config.js 中的 mysql 配置信息，自动连接 mysql 服务器。支持同时配置多个 mysql 服务器。  

文件名：*global/daemons/Mysql.js*    
模块名：*MYSQL_D*   
主要接口：  
* `MYSQL_D.query(dbName, sql)`    
````
/**
 * 执行 mysql 命令，返回 Promise 对象
 * @method MYSQL_D.query
 * @param {string} dbName - Config 配置文件中配置的 mysql database
 * @param {string} cmd - mysql sql 语句
 *    比如 select * from test;    
 */ 
````  

* `MYSQL_D.transaction(dbName, sqlList)`   
````
/**
 * 执行 mysql transaction 多事务命令，返回 Promise 对象
 * @method MYSQL_D.transaction
 * @param {string} dbName - Config 配置文件中配置的 mysql database
 * @param {array} sqlList - 多条 mysql sqlite
 *    比如 ['update test set value = 1 where id =1;', 'update test set value = 2 where id = 2']
 */    
````  

* `MYSQL_D.batchQuery(dbName, sqlList)`   
````
/**
 * 与 transation 不同的是，总是执行 commit 操作，即使某条语句执行失败
 * @method MYSQL_D.batchQuery
 * @param {string} dbName - Config 配置文件中配置的 mysql database
 * @param {array} sqlList - 多条 mysql sqlite
 *    比如 ['update test set value = 1 where id =1;', 'update test set value = 2 where id = 2']
 */    
````  

### 日志系统    
使用 log4js 库，提供多级日志接口、按日期写日志文件功能。  
文件名：*global/daemons/Log.js*    
模块名：*LOG_D*   
主要接口：  
* `enableTrace(bool flag)`    
开启或关闭 trace。   
* `trace(string format, [...])`    
普通打印日志，受 enableTrace 开关控制。  
* `debug(string format, [...])`    
调试日志。 
* `info(string format, [...])`    
信息日志。  
* `log(string format, [...])`    
重要的打印日志。  
* `warn(string format, [...])`    
警告日志，会写文件，目录在 logs 下。  
* `error(string format, [...])`    
错误日志，打印报错栈，会写文件，目录在 logs 下。  
* `fatal(string format, [...])`    
异常日志，打印报错栈，会写文件，目录在 logs 下。  

format 格式如下：   
````
%s : 字符串
%d : 数值
%j : json格式数据
````

### 脚本异常报错捕获机制    
捕获脚本异常报错，打印报错栈，写日志文件，避免进程崩溃退出。  
文件名：*global/base/Util.js*    

### win32 脚本交互控制台   
启动时带上 --repl 参数，可在控制台上与进程脚本环境进行交互。比如：  
````
GS1>
GS1> COMMUNICATE_D
{ listen: [Function: listen],
  registerCmd: [Function: registerCmd],
  sendMessage: [Function: sendMessage],
  create: [Function: create] }
GS1>
GS1> 1+2
3
GS1>
````

### 支持 telnet 后台机制
在 linux 环境下，后台运行游戏进程，可通过 telnet 端口(config/Config.js 中的 telnetPort 配置)连接到游戏进程后台，游戏进程后台，与游戏脚本环境进行交互，类似 win32 的脚本交互控制台。  
文件名：*global/base/Repl.js*   

### 简易的帐号登录、登出、保存数据功能  
帐号登录时进行帐号验证、创建新帐号、返回已有帐号信息的操作；登出时进行帐号验证及保存数据的操作。  
本模块目前默认使用 redis 数据库进行数据存储，开发者可自行使用 [mysql 数据库](#mysql-数据库支持)。    
文件名：*gs/daemons/Login.js*    
模块名：*LOGIN_D*   
主要接口：
主要接口：  
* `LOGIN_D.login(res, data)`    
用户登录，若用户存在，会进行帐号密码验证，验证成功后返回用户信息；若用户不存在，会以 username 和 password 创建新用户，并返回新用户数据。  
参数 res 为 http 连接中的 response 对象；参数 data 为 json 格式的登录信息，必须有 username 和 password。  	 
* `LOGIN_D.logout(res, data)`    
用户登出，若用户存在，会进行帐号密码验证，验证成功后保存用户信息。  
参数 res 为 http 连接中的 response 对象；参数 data 为 json 格式的登录信息，必须有 username、password、saveData。  

### 微信SDK支持  
提供微信公众平台的 token、ticket、signature 的获取接口；提供开放平台微信登录返回用户信息的接口 

文件名：*gs/daemons/Wechat.js*    
模块名：*WECHAT_D*   
主要接口：  
* `WECHAT_D.wechatLogin(res, appid, codeOrSessionId, isCode)`     
````  
/**  
 * 执行微信登录，成功返回用户信息  
 * @method WECHAT_D.wechatLogin  
 * @param {object} res - http 连接中的 response 对象  
 * @param {string} appid - 应用程序id  
 * @param {string} codeOrSessionId - 登录 code 或 session_id  
 * @param {bool} isCode - codeOrSessionId 是否为 code，还是 session_id  
 */ 
````  

* `WECHAT_D.getSign(appid, url)`     
````  
/**  
 * 取得微信公众平台 js 接口初始化所须的签名信息  
 * @method WECHAT_D.getSign  
 * @param {string} appid - 应用程序id  
 * @param {string} url - 应用程序的 url  
 */ 
````  

## 前端的通信插件
[ServerCommunicate](ServerCommunicate.html)
