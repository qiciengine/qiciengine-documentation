# qc.Transition
组件的交互变换模式，定义如下：
````
	qc.Transition = {
	    /**
	     * @property {number} NONE - 不需要有任何变换
	     * @static
	     */
	    NONE : 0,

	    /**
	     * @property {number} COLOR_TINT - 变换颜色
	     * @static
	     */
	    COLOR_TINT : 1,

	    /**
	     * @property {number} TEXTURE_SWAP - 使用图片变换
	     * @static
	     */
	    TEXTURE_SWAP : 2,

	    /**
	     * @property {number} ANIMATION - 使用自定义动画
	     * @static
	     */
	    ANIMATION : 3
	};
````

## 参考手册
[TransitionBehaviour](http://docs.zuoyouxi.com/manual/BuildinComponents/TransitionBehaviour.html)