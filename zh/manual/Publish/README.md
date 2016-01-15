# 发布  
1. 再三确认[工程设置](../Settings/index.html)的内容：	
  * 正确设置标识符  
  * 正确设置版本号  
  * 所有需要发布的场景都已勾选，并且正确设置入口场景   
2. 点击主菜单：工程/发布...  
3. 稍候片刻，在游戏工程Build目录下出现如下内容：    
  * Assets目录：所有的游戏资源
  * js/：打包后的逻辑脚本  
  * qici.appcache：[Application Cache](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Using_the_application_cache) 的 manifest 文件，若[工程设置](../Settings/index.html)中的 [Application Cache](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Using_the_application_cache) 打勾，此时发布会生成该文件  
  * StartGame.html：游戏启动页面，您可以对此文件进行修改、美化等  
![Publish](images/publish.png)    
4. 将Build目录内容上传到您的网站，就可以直接访问了  

