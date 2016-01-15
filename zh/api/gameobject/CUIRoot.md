# UIRoot

## 描述
挂载UI界面的根节点，本身是一个空节点（[qc.Node](CNode.md)），UI元素都应该在此节点下面，UIRoot保持和世界一样的大小并始终和相机位置保持一致。

一般我们会给该节点设置一个 [qc.ScaleAdapter](../components/ScaleAdapter.md)，让其随着设备分辨率缩放，而其他 UI 元素则跟随 UIRoot 进行定位缩放

## 参考手册
[UIRoot](http://docs.zuoyouxi.com/manual/Sample/UIRoot.html)