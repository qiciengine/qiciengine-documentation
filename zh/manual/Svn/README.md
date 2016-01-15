# 工程目录结构与版本控制

## 工程目录结构
一个完整的工程，包含如下几个目录：  
* Assets - 存放资源
* Build - 存放发布后的文件
* Editor - 编辑器扩展脚本
* Plugins - 插件信息
* ProjectSetting - 工程配置
  * editor.setting - 编辑器设定信息
  * project.setting - 工程设置
  * scene.setting - 游戏场景配置
  * script.setting - 脚本依赖配置
* Scripts - 游戏逻辑脚本
* Temp - 临时目录

## 版本管理
可以使用svn或git等进行版本管理，以下目录和文件需要加入到版本库中：  
* Assets
* Editor
* Plugins
* ProjectSetting
  * project.setting
  * scene.setting
  * script.setting
* Scripts