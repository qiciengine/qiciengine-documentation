# 打包图集

将多张图片打包成一张大图片称为打包图集，有助于性能提升。

## 约定
* 需要打包成一张大图集的所有图片，放在单独的一个文件夹下
* 约定的文件夹名需以'@atlas'结尾，例如：“图集名字@atlas”
* 打包后，图集文件放在：Assets/atlas/图集名字.bin
* 美术原始资源，建议放在Assets/art目录下统一管理
* 图集的名字请使用英文和下划线（否则下载时可能会下载失败）

## 打包步骤示例
1. 准备好美术资源，并根据需要对各图片重命名
2. 在Project面板下，建立图集的原始文件夹：Assets/art/dota@atlas  
	![文件夹](images/atlas_folder.jpeg)  
3. 将磁盘上的图片拖拽到本文件夹下：  	
	![添加图片](images/add.jpeg)  
4. 选择主菜单：Tool/Repack Texture Atlases，开始打包所有图集		
	![打包图集](images/repack.png)	
5. 打包完毕后，图集生成在：Assets/atlas/dota.bin  
	![图集](images/atlas.jpeg)  

*注意：如果原始图片发生变更，需要执行步骤4重新打包图集*  

视频演示：  
<video controls="controls" src="../video/add_atlas.mp4"></video>  	