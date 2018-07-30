# 发布微信小游戏   
1. 在发布界面中，配置相关的内容，点击 Build 一键生成小游戏工程目录  
![](images/publish.png)  
其中远程资源地址为 Assets 资源目录在资源服务器上的 Url 地址。默认指向发布后的 Assets 目录所在地址。  

2. 默认会在 build/wechat 目录下生成 DevProject 和 PublishProject 两个目录  
PublishProject 为发布正式版本的工程目录；DevProject 目录为开发版本的工程目录。以下以 DevProject 目录作重点说明：  
	* Assets 目录：游戏所有资源目录，需要完整上传到资源服务器上。目录下有个 assets.md5 文件记录所有资源对应的 md5，用于资源版本控制。  
	* Code 目录：小游戏工程目录，包含小游戏环境的配置文件 game.json 和 project.config.json  
	* dislist.dis 文件：小游戏版本及其它配置文件。游戏启动时会先取该文件，对比版本号及其它配置，若版本号不一致，需要下载 Assets 目录下的 assets.md5 文件取得最新资源的 md5 信息。  
 
3. 在[微信公众平台](https://developers.weixin.qq.com/minigame/dev/devtools/download.html)上下载微信开发者工具
创建小游戏工程，工程目录为上面的 Code 目录，自行修改 project.config.json 中的 appid 等配置
