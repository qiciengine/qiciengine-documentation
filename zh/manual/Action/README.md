# 动作系统

本章将介绍 QICI Engine 的动作系统，该动作系统主要有两个工具：[动作编辑器](ActionEditor.md) 和 [动作管理器](ActionManager.md)。其中 [动作编辑器](ActionEditor.md) 负责编辑单个 _动作剪辑_ 文件；
[动作管理器](ActionManager.md) 负责对 _动作剪辑_ 和 _动作管理器剪辑_ 文件进行串行、并行组合，导出 _动作管理器剪辑_ 文件。游戏对象播放 _动作剪辑_ 或 _动作管理器剪辑_ 文件，需要挂载 [Animator 组件](Animator.md)，
[Animator 组件](Animator.md) 负责控制 _动作剪辑_ 或 _动作管理器剪辑_ 文件的加载、播放等操作。 

* [Animator 组件](Animator.md)  
* [动作编辑器](ActionEditor.md)  
* [动作管理器](ActionManager.md)  