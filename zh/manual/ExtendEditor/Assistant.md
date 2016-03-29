# 开放的辅助功能

## 服务后端模块
* __M.EXTERNAL_MODULES__：拓展模块，该模块提供一些常用的接口：
    - M.EXTERNAL_MODULES.load(filePath)：通过完整路径加载脚本。
    - M.EXTERNAL_MODULES.loadDir(dirPath)：通过完整路劲加载目录下的所有脚本。
    - M.EXTERNAL_MODULES.loadExistModule(moduleName)：加载后台服务已经存在的模块。
* __M.PROJECT__：项目管理模块，该模块提供一些项目操作接口：
    - M.PROJECT.saveProjectSetting()：保存项目配置。
    - M.PROJECT.publisTo(buildDir)：发布游戏到指定目录。
* __G.config.project__：当前项目的配置信息。
* __G.emitter__：后台服务的事件派发对象，可用的事件有：
    - 'BeforePublish'：项目发布前的事件类型。
    - 'AfterPublish'：项目发布成功后的事件类型。
* __M.SERVICE_PIPE__：前端和后台服务的通讯通道，提供与前端通讯的接口：
    - M.SERVICE_PIPE.on(command, listener)：监听从前端接收到的指定消息。
    - M.SERVICE_PIPE.off(command, listener)：不再监听从前端接收到指定消息。
    - M.SERVICE_PIPE.emit(command, data)：派发消息事件。
    - M.SERVICE_PIPE.sendData(command, data)：向前端发送数据。

## 编辑器前端功能
* __G.e__：编辑器前端的事件派发对象，可用事件有：
    - G.e.BEFORE_PUBLISH：项目发布前的事件类型，在后台服务的BeforePublish之前。
    - G.e.AFTER_PUBLISH：项目发布后的事件类型，在后台服务器的AfterPublish之后。
* __qc.servicePipe__：编辑器前端与后台服务的通讯通道，提供与后台服务通讯的接口：
    - qc.servicePipe.on(command, listener, scope)：监听从后台接收到的指定消息。
    - qc.servicePipe.off(command, listener, scope)：不再监听从后台接收到指定消息。
    - qc.servicePipe.emit(command, data)：派发消息事件。
    - qc.servicePipe.sendData(command, data)：向后台服务发送数据。