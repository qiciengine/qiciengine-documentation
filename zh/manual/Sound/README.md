# 声音

## 支持的格式
青瓷引擎目前支持__mp3__和__ogg__这两个声音文件格式

## 导入音效资源
直接将声音文件拖入Project工程面板中（建议放在Assets/audio目录方便管理），即可自动生成。为了确保大部分浏览器能够支持，请确保mp3和ogg格式全部导入到工程中（如果浏览器不支持ogg播放会自动加载mp3格式）

## 使用代码播放音效

````javascript
// 下载音乐资源，下载完毕后立刻播放
game.assets.load('audio_test', 'Assets/audio/CM_ATK.mp3.bin', function(audio) {
	// 构造音效节点
	var sound = game.add.sound();

	// 赋予音效资源，类型为qc.SoundAsset
	sound.audio = audio;

	// 播放完毕后自动销毁
	sound.destroyWhenStop = true;

	// 开始播放
	sound.play();
});
````

## 在场景中挂载播放
1. 新建Sound节点：点击主菜单（游戏对象/声音），或者选择工具栏的声音按钮，或者在Hierarchy右键菜单进行创建
2. 拖拽音效资源文件绑定到Audio属性
3. 设置Inspector面板声音属性
	* __Loop__ - 是否循环播放，node.loop = true;
	* __Mute__ - 是否静音，node.mute = true;
	* __Volume__ - 声音播放时的音量，node.volume = 1.0;
	* __Play On Awake__ - 但声音对象awake时是否自动播放，node.playOnAwake = true;
	* __Destroy When Stop__ - 声音播放结束后是否自动销毁对象，node.destroyWhenStop = true;
	* __Play__ - 开始播放声音，node.play();
	* __Stop__ - 停止声音播放，node.stop();  
![](images/sound.png)

## 声音兼容性说明
声音播放的时候，引擎会优先使用 [Web Audio](http://www.w3.org/TR/webaudio) 的方式播放音乐。如果浏览器不支持 [Web Audio](http://www.w3.org/TR/webaudio)，引擎会自动改用 [Audio Tag](http://www.w3.org/wiki/HTML/Elements/audio) 方式来完成播放。

另外，不同的浏览器支持的音乐格式不同（绝大部分都能支持 mp3 格式），放置音乐资源的时候，建议将声音的 mp3、ogg 格式（二者之间的转换可以用格式工厂之类的转换软件）都存一份，__使用同一个名字并放在同级目录下__（例如 bgSound.mp3、bgSound.ogg）。这样，实际播放的时候如果浏览器不支持 mp3 的情况，引擎会判断并会自动下载对应的 ogg 格式来进行播放。

注意，挂载的时候用 .mp3.bin 或者 .ogg.bin 均可。

## API
[Sound API](http://docs.zuoyouxi.com/api/gameobject/CSound.html)

## Demo
[Sound Demo](http://engine.zuoyouxi.com/demo/Audio/audioSupportInfo/index.html)
