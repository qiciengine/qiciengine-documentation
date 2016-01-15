# 输入框
文本输入框qc.InputField用于显示并可输入文本。

## 输入框构成
从主菜单(游戏对象/输入框)或工具条上创建输入框对象，得到如下的输入框对象结构：  
![](images/inputfield1.png)
* __InputField__: 输入框InputField对象，其继承于[UIImage](UIImage.html)，作为背景图
* __Text__: 文本[UIText](UIText.html)对象，用于显示输入的文本内容。输入框的textComponent属性
* __Placeholder__: 文本[UIText](UIText.html)对象，用于在Text对象内容为空时，显示提示信息。输入框的placeholder属性

通过如下代码可实现和编辑器上创建输入框同样的效果：
````javascript
var node = new qc.InputField(game, parent);
node.texture = game.assets.find('__builtin_resource__');
node.frame = 'button.png';
node.imageType = qc.UIImage.IMAGE_TYPE_SLICED;
node.textComponent.fontSize = 18;
node.placeholder.fontSize = 18;
````

## 输入框属性
* __Text__: 本文内容，node.textComponent.text = 'QICI Engine';
* __Placeholder Text__: 提示文本内容，node.placeholder.text = 'Enter Text...'; 
* __State__ 输入框的state属性具有以下几种状态：
	* qc.UIState.NORMAL - 正常状态
	* qc.UIState.PRESSED - 按下状态
	* qc.UIState.DISABLED - 不可编辑状态
* __Character Limit__: 输入框可输入字符限制，node.characterLimit = 6;	
* __LineType__: 输入框行类型，node.lineType = qc.InputField.SINGLE_LINE;
	* qc.InputField.SINGLE_LINE: 单行输入框
	* qc.InputField.MULTI_LINE: 多行输入框
* __Content Type__: 内容类型，node.contentType = qc.InputField.PASSWORD;
	* qc.InputField.STANDARD: 标准类型
	* qc.InputField.INT: 整数类型
	* qc.InputField.NUMBER: 浮点数类型
	* qc.InputField.TEL: 电话号码类型
	* qc.InputField.EMAIL: 邮箱地址类型
	* qc.InputField.PASSWORD: 密码类型
* __Text Component__: 文本组件引用	
* __Placeholder__: 提示组件引用
  
## API
[InputField API](http://docs.zuoyouxi.com/api/gameobject/CInputField.html)

## Demo
[InputField Demo](http://engine.zuoyouxi.com/demo/index.html#anchor_InputField)