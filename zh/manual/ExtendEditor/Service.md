# 后台服务扩展
在拓展编辑器功能时，有时候会需要访问目录等后台功能，可以通过拓展后台服务来实现需要的功能。

## 扩展实现
* 在项目目录Project/Editor/Service下，创建一个脚本。
* 脚本使用NodeJS的require方法载入。
* 当项目打开时，后台服务将加载Project/Editor/Service下的扩展脚本，该目录下的子目录中的脚本不会自动被加载。
* 当项目切换时，会调用脚本的module.destruct方法，进行销毁操作。如果在脚本中进行了监听等操作，需要在destruct中释放资源。

## Demo
[Extend-Service Demo](http://engine.zuoyouxi.com/demo/misc/extend_service/index.html)   