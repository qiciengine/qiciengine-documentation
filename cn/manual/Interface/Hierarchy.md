# 层级（Hierarchy）面板
![](images/hierarchy.jpeg)  

Project（项目）视图显示游戏场景中所有可用的对象、文件等资源；而Hierarchy视图则列出当前场景中真正的游戏对象，并展示游戏对象的层次父子关系。  

通过拖放节点即可将节点随意插入到任何新位置以改变父子关系（如下详述），随着游戏场景中的对象添加或删除，层次树会实时反映游戏对象的出现和消失。

* 插入作为孩子节点		
![](images/child.png)  
拖拽操作后node节点将作为B节点的最后一个孩子

* 插入到节点下方	
![](images/under.png)  
拖拽操作后node节点与B节点挂载在相同父亲下，排在B节点后面：A, B, node, C

* 插入到节点上方	
![](images/above.png)  
拖拽操作后node节点与B节点挂载在相同父亲下，排在B节点前面：A, node, B, C

视频演示：  
<video controls="controls" src="../video/drag_node_in_hierachy.mp4"></video>  