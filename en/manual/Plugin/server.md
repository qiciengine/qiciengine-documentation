# Simple Server  
It supports login、logout、save function, also can customize command to implement custom function.  
  
## Github  
https://github.com/qiciengine/qiciengine-server    
 
## Install Requirement   
* [nodejs](https://nodejs.org/en/)  
* [redis](http://redis.io/)  
* [mysql](http://www.mysql.com/downloads/)  
* [pm2](https://www.npmjs.com/package/pm2)  

## Boot Step
### windows  
* Execute `npm install` in package.json's folder, download dependent js lib.   
* Default config file is `config/Config.js`. We can create custom config file, then boot different process, such as: `node gs/StartGs.js config/Config2.js` --repl 	 
* Execute `start_server.bat` or `node gs/StartGs.js --repl` manually, to start single process server.   

### linux  
* Execute `npm install` in package.json's folder, download dependent js lib.   
* Default config file is `config/Config.js`. We can create custom config file, then boot different process, such as: `node gs/StartGs.js config/Config2.js` --repl 		
* Execute `./start_server.sh` or `node gs/StartGs.js --repl` manually, to start single process server.  
* Recommend execute `./start_cluster.sh`, to start multi process server in cluster mode. It will impletment overload balance.   

## Directory Structure
````
config : config file
global : global common code
    base : global function
	include : global definition
	clone : global object
	daemons : global module
	cmds : global command handler
gs : game server code
    base : gs function
	include : gs definition
	clone : gs object
	daemons : gs module
	cmds : gs command handler
logs : log file
````

## Server Function  
* [http communicate and dispatch mechanism](#http-communicate-and-dispatch-mechanism)  
* [websocket communicate and dispatch mechanism](#websocket-communicate-and-dispatch-mechanism)  
* [redis support](#redis-support)  
* [mysql support](#mysql-support)  
* [log system](#log-system)  
* [catch script exception](#catch-script-exception)  
* [win32 console](#win32-console)  
* [telnet console](#telnet-console)  
* [account support](#account-support)  

### http communicate and dispatch mechanism  
File name: *global/daemons/Communicate.js*    
Module name: *COMMUNICATE_D*   
Main API:   
* `COMMUNICATE_D.listen(port)`  
listen port. It will automatically listen port configured in `Config/Config.js` when server boot.    
* `COMMUNICATE_D.sendMessage(res, jsonData)`   
Send response data to client.  
res: response object of http connection; jsonData: response data in json format.    
 
* `COMMUNICATE_D.registerCmd(cmd, func)`   
Register command handler. In global/cmds and gs/cmds folder, there are many files that impletment command handler. These handler will be loaded when boot, then
this interface will be invoked.  
cmd: command name; 
func: callback function, prototype is main(res, para), para is json format.

### websocket communicate and dispatch mechanism    
File name: *global/daemons/Communicate.js*    
Module name: *COMMUNICATE_D*   
Main API:   
* `COMMUNICATE_D.listen(port)`   
listen port. It will automatically listen port configured in `Config/Config.js` when server boot.     	 
* `COMMUNICATE_D.sendSocketMessage(socket, ...)`    
Send socket message to client.     
socket: socket io instance.    
...: Optional parameters.   
   
* `COMMUNICATE_D.registerSocketCmd(cmd, func)`   
Register hander for socket command. In global/cmds/socket and gs/cmds/socket folder, there are many files that impletment command handler. These handler will be loaded when boot, then
this interface will be invoked.    
cmd: command name;  
func: command handler, prototype is main(socket, ...)  

### redis support  
Sever will connect automatically to redis according to redis config information of `Config/Config.js`. Support to multi redis server simultaneously.  

File name: *global/daemons/Redis.js*    
Module name: *REDIS_D*   
Main API:   
* `REDIS_D.redisOper(dbName, cmd, cmdArg)`    
````
/**
 * execute redis command, return Promise object
 * @method REDIS_D.redisOper
 * @param {string} dbName - redisDb in Config.js
 * @param {string} cmd - redis command
 * @param {array} cmdArg - redis command argument
 *    For example: hset id key value
 *    cmd is hset, cmdArg is [id, key, value]
 */ 
````  

* `REDIS_D.redisMulti(dbName, cmdList)`   
````
/**
 * execute redis multi transcation command, return Promise object
 * @method REDIS_D.redisMulti
 * @param {string} dbName - redisDb in Config.js
 * @param {array} cmdList - multi redis command
 *    For example: hset id key value; hset id2 key value
 *    cmdList is [ ['hset', 'id', key, value], ['hset', 'id', key, value] ]
 */  
````  

### mysql support  
Sever will connect automatically to mysql according to mysql config information of `Config/Config.js`. Support to multi mysql server simultaneously.  

File name: *global/daemons/Mysql.js*    
Module name: *MYSQL_D*   
Main API:   
* `MYSQL_D.query(dbName, sql)`    
````
/**
 * execute mysql command, return Promise object
 * @method MYSQL_D.query
 * @param {string} dbName - mysql database in Config.js
 * @param {string} cmd - mysql sqlite command
 *    For example: select * from test;    
 */ 
````  

* `MYSQL_D.transaction(dbName, sqlList)`   
````
/**
 * execute mysql multi transcation command
 * @method MYSQL_D.transaction
 * @param {string} dbName - mysql database in Config.js
 * @param {array} sqlList - multi mysql command
 *    For example: ['update test set value = 1 where id =1;', 'update test set value = 2 where id = 2']
 */  
````  

* `MYSQL_D.batchQuery(dbName, sqlList)`   
````
/**
 * Diffirent from transaction, batchQuery alway execute commit, even some sql fail.
 * @method MYSQL_D.batchQuery
 * @param {string} dbName - mysql database in Config.js
 * @param {array} sqlList - multi mysql command
 *    For example: ['update test set value = 1 where id =1;', 'update test set value = 2 where id = 2']
 */  
````  

### log system      
Using log4js lib to support multi level trace and dateFile.  
Module name: *global/daemons/Log.js*    
Module name: *LOG_D*   
Main API:     
* `enableTrace(bool flag)`    
Open or close trace。   
* `trace(string format, [...])`    
Normal trace, control by enableTrace.  
* `debug(string format, [...])`    
Debug log.  
* `info(string format, [...])`    
Information log.   
* `log(string format, [...])`    
Important log.  
* `warn(string format, [...])`    
Warning log, write to log file in logs folder.   
* `error(string format, [...])`    
Error log, write to log file in logs folder.   
* `fatal(string format, [...])`    
Fatal log, write to log file in logs folder.   

format is following:   
````
%s : string
%d : number
%j : json
````

### catch script exception
Catch script exception, print error stack, write log file, avoid to exit.     
File name: *global/base/Util.js*    

### win32 console   
Execute server with --repl, console is enabled. Then we can interactive with script environment, such as:   
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

### telnet console  
When server run in linux, we can telnet to process, then interactive with script environment like win32 console.   
File name: *global/base/Repl.js*   

### account support  
It support account auth、login、logout、save function.  
By default, it use redis to store account information, developer can use [mysql database](#mysql-support) by self.  
File name: *gs/daemons/Login.js*    
Module name: *LOGIN_D*   
Main API:   
* `LOGIN_D.login(res, data)`  
Account login. If account exists, it will check account, then return account information, else it will create a new account, then return account information.  
res: response object of http connection; data: login data in json format, must contain username and password.    
* `LOGIN_D.logout(res, data)`  
Account logout. If account exists, it will check account, then save account information.  
res: response object of http connection; data: login data in json format, must contain username、password and saveData.    

## Server Communicate Plugin  
[ServerCommunicate](ServerCommunicate.html)
