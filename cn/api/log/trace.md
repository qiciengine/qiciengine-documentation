# [qc.Log](README.md).trace

## 原型
````
	void trace(content:string, params...);
````

## 说明
输出普通日志信息，受到enableTrace开关的影响。为了方便调试等，我们建议在主流程中增加日志的打印，发布时禁止掉即可。

## 范例
````
	game.log.trace('{0} download ok.', 'assets/npc/slime.bin');
````
