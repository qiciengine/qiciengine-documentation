# qc.Node#removeListener

## 原型
* void removeListener([int]id);

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| id | int | 监听编号 |

## 说明
手动移除事件关注

## 范例
````
    var id = this.addListener(this.game.input.onKeyDown, function(keycode){
            console.log('key down');
    });
	
	this.removeListener(id);
````
