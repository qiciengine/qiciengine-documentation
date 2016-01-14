# 滚动支持

## 描述
滚动窗口支持。

## 构造函数
```
com.qici.extraUI.ScrollSupport(game, node, fnGetViewRect, fnGetContentRect, fnSetContentPosition);
```

| 参数 | 类型 | 描述 |
|------|----|----|
| game | qc.Game | 游戏对象 |
| node | qc.Node | 用来提供事件监听的节点对象，一般为可视区域对应的节点。|
| fnGetViewRect | function | 获取可视区域大小的函数，返回qc.Rectangle。|
| fnGetContentRect | function | 获取整个内容区域大小的函数，返回qc.Rectangle，宽或者高可以为Infiity。|
| fnSetContentPosition | function | 设置内容区域相对于可视区域偏移的函数，function(offX, offY)。|

## 变量
| 变量名        |  类型     |   作用           |
| ------------- |-------------| -------------|
| canHorizontal | bool | 是否响应水平滑动 |
| canVertical | bool | 是否响应垂直滑动 |
| movementType | number | 边界限制类型，ScrollView.MOVEMENT_UNRESTRICTED（滚动区域无限制）、ScrollView.MOVEMENT_ELASTIC（滚动区域有限制，但可以超越边界，之后被拖回）、ScrollView.MOVEMENT_CLAMPED（滚动区域有限制，无法超过边界） |
| elasticity | number | 当 moveMentType 为 MOVEMENT_ELASTIC 时生效，用于表示复位速度 |
| inertia | bool | 是否惯性滑动 |
| decelerationRate | number | 惯性滑动的减速参数 |
| scrollSensitivity | number | 响应滚动时的倍率 |
| propagationScroll | bool | 是否向上传递滚动事件 |
| horizontalScrollBar | qc.ScrollBar or null | 水平滚动条，该 ScrollBar 的滑动会影响 ScrollView 的水平值，反之亦然 |
| horizontalNormalizedPosition | number | 水平方向滚动的比例（0 - 1） |
| verticalScrollBar | qc.ScrollBar or null | 垂直滚动条，该 ScrollBar 的滑动会影响 ScrollView 的纵向值，反之亦然 |
| verticalNormalizedPosition | number | 垂直方向滚动的比例（0 - 1） |

## 事件
| 事件名  | 作用 |
| ------------- |-------------|
| onValueChange | 偏移值发生变化时调用 |

## 使用方式
在任意脚本中实例化一个本对象。并设置事件对象等信息后，即可获得滚动支持。
```
this.scrollSupport = new com.qici.extraUI.ScrollSupport(
    this.game, // 游戏对象
    this.gameObject, // 用来监控事件的节点对象
    this.getViewRect.bind(this), // 获取可显示视窗大小的函数
    this.getContentRect.bind(this), // 获取滚动的内容区域大小的函数
    this.setContentPosition.bind(this) // 设置滚动内容偏移的函数
);
```
这样就可以让gameObject获得滚动视图的支持了。

## 编辑器支持
如果需要编辑器支持，需要在使用该对象的脚本中添加下列属性:
```
    canHorizontal: {
        get : function() {
            return this.scrollSupport ? this.scrollSupport.canHorizontal : null;
        },
        set : function(value) {
            this.scrollSupport && (this.scrollSupport.canHorizontal = value);
        }
    },

    canVertical: {
        get : function() {
            return this.scrollSupport ? this.scrollSupport.canVertical : null;
        },
        set : function(value) {
            this.scrollSupport && (this.scrollSupport.canVertical = value);
        }
    },

    movementType: {
        get : function() {
            return this.scrollSupport ? this.scrollSupport.movementType : null;
        },
        set : function(value) {
            this.scrollSupport && (this.scrollSupport.movementType = value);
        }
    },

    elasticity: {
        get : function() {
            return this.scrollSupport ? this.scrollSupport.elasticity : null;
        },
        set : function(value) {
            this.scrollSupport && (this.scrollSupport.elasticity = value);
        }
    },

    inertia: {
        get : function() {
            return this.scrollSupport ? this.scrollSupport.inertia : null;
        },
        set : function(value) {
            this.scrollSupport && (this.scrollSupport.inertia = value);
        }
    },

    decelerationRate: {
        get : function() {
            return this.scrollSupport ? this.scrollSupport.decelerationRate : null;
        },
        set : function(value) {
            this.scrollSupport && (this.scrollSupport.decelerationRate = value);
        }
    },

    scrollSensitivity: {
        get : function() {
            return this.scrollSupport ? this.scrollSupport.scrollSensitivity : null;
        },
        set : function(value) {
            this.scrollSupport && (this.scrollSupport.scrollSensitivity = value);
        }
    },

    propagationScroll: {
        get : function() {
            return this.scrollSupport ? this.scrollSupport.propagationScroll : null;
        },
        set : function(value) {
            this.scrollSupport && (this.scrollSupport.propagationScroll = value);
        }
    },

    /**
     * @property {qc.Node | null} horizontalScrollBar - 水平滚动条
     */
    horizontalScrollBar : {
        get : function() {
            return this.scrollSupport ? this.scrollSupport.horizontalScrollBar : null;
        },
        set : function(value) {
            this.scrollSupport && (this.scrollSupport.horizontalScrollBar = value);
        }
    },

    /**
     * @property {qc.Node | null} verticalScrollBar - 竖直滚动条
     */
    verticalScrollBar : {
        get : function() {
            return this.scrollSupport ? this.scrollSupport.verticalScrollBar : null;
        },
        set : function(value) {
            this.scrollSupport && (this.scrollSupport.verticalScrollBar = value);
        }
    },

    /**
     * @property {number} horizontalNormalizedPosition - 水平方向上滚动的比例
     */
    horizontalNormalizedPosition : {
        get : function() {
            return this.scrollSupport ? this.scrollSupport.horizontalNormalizedPosition : null;
        },
        set : function(value) {
            this.scrollSupport  && this.scrollSupport.setNormalizedPosition(value, 0);
        }
    },

    /**
     * @property {number} verticalNormalizedPosition - 竖直方向上滚动的比例
     */
    verticalNormalizedPosition : {
        get : function() {
            return this.scrollSupport ? this.scrollSupport.verticalNormalizedPosition : null;
        },
        set : function(value) {
            this.scrollSupport  && this.scrollSupport.setNormalizedPosition(value, 1);
        }
    }
```
并在对应的editor脚本中添加：
```
    var self = this;
    gui.columnWidths = [self.indent, "70+0.1", "60+0.5"];
    // 是否水平滚动
    var title = gui.titleLine('Horizontal Scroll', G.preference.query('collapse.scrollView') === true);
    title.add(gui.line([
        gui.empty(),
        gui.text('Horizontal', { toolTip: 'canHorizontal' }),
        gui.checkBox({ bind: 'canHorizontal' })
    ]));
    title.add(InspectorUtil.drawNodeRef(target, 'horizontalScrollBar', undefined, true, 'ScrollBarH'));
    title.add(gui.line([
        gui.empty(),
        gui.text('Value', { toolTip: 'horizontalNormalizedPosition' }),
        gui.numberInput({ bind: 'horizontalNormalizedPosition' })
    ]));

    // 是否垂直滚动
    title = gui.titleLine('Vertical Scroll', G.preference.query('collapse.scrollView') === true);
    title.add(gui.line([
        gui.empty(),
        gui.text('Vertical', { toolTip: 'canVertical' }),
        gui.checkBox({ bind: 'canVertical' })
    ]));
    title.add(InspectorUtil.drawNodeRef(target, 'verticalScrollBar', undefined, true, 'ScrollBarV'));
    title.add(gui.line([
        gui.empty(),
        gui.text('Value', { toolTip: 'verticalNormalizedPosition' }),
        gui.numberInput({ bind: 'verticalNormalizedPosition' })
    ]));
    gui.columnWidths = defaultConfig;

    // 边界限制类型
    gui.line([
        gui.text('Movement Type', { toolTip: 'movementType' }),
        self._moveType = gui.dropDownList({ bind: 'movementType', items: [
            { label: 'Unrestricted', value: qc.ScrollView.MOVEMENT_UNRESTRICTED },
            { label: 'Elastic', value: qc.ScrollView.MOVEMENT_ELASTIC },
            { label: 'Clamped', value: qc.ScrollView.MOVEMENT_CLAMPED }
        ]})
    ]);

    // 复位速度
    var old = target.movementType;
    self._moveType.onValueChanged = function(v) {
        if (v !== old)
            self.repaint();
    };

    if (target.movementType === qc.ScrollView.MOVEMENT_ELASTIC) {
        gui.line([
            gui.text('Elasticity', { align: 'left' }),
            gui.numberInput({ bind: 'elasticity' })
        ]);
    }

    // 惯性滑动
    gui.line([
        gui.text('Inertia', { align: 'left' }),
        gui.checkBox({ bind: 'inertia' })
    ]);
    gui.line([
        gui.text('Deceleration Rate', { toolTip: 'decelerationRate' }),
        gui.numberInput({ bind: 'decelerationRate' })
    ]);

    // 滚动的敏感度
    gui.line([
        gui.text('Scroll Sensitivity', { toolTip: 'scrollSensitivity' }),
        gui.numberInput({ bind: 'scrollSensitivity' })
    ]);

    // 滚动的敏感度
    gui.line([
        gui.text('Propagation Scroll', { toolTip: 'propagationScroll' }),
        gui.checkBox({ bind: 'propagationScroll' })
    ]);

```
