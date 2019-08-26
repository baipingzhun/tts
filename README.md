TTS-语音合成
------------------------------------------------------------------------------
（demo可以直接放到工程下打开，资源路径视情况调整)

SpeechSynthesisUtterance和SpeechSynthesis简单介绍：
------------------------------------------------------------------------------

SpeechSynthesisUtterance是HTML5中新增的API,用于将指定文字合成为对应的语音.也包含一些配置项,指定如何去阅读(语言,音量,音调)等
SpeechSynthesisUtterance基本属性
------------------------------------------------------------------------------

SpeechSynthesisUtterance.lang 获取并设置话语的语言
SpeechSynthesisUtterance.pitch 获取并设置话语的音调(值越大越尖锐,越低越低沉)
SpeechSynthesisUtterance.rate 获取并设置说话的速度(值越大语速越快,越小语速越慢)
SpeechSynthesisUtterance.text 获取并设置说话时的文本
SpeechSynthesisUtterance.voice 获取并设置说话的声音
SpeechSynthesisUtterance.volume 获取并设置说话的音量

SpeechSynthesisUtterance.text基本方法：
speak() 	将对应的实例添加到语音队列中
cancel() 删除队列中所有的语音.如果正在播放,则直接停止
pause() 暂停语音
resume() 恢复暂停的语音
getVoices 获取支持的语言数组. 注意:必须添加在voiceschanged事件中才能生效


网页语音 API 的SpeechSynthesis接口是语音服务的控制接口；它可以用于获取设备上关于可用的合成声音的信息，开始、暂停语音，或除此之外的其他命令。
------------------------------------------------------------------------------
方法:
SpeechSynthesis 也从它的父接口继承方法， EventTarget.
SpeechSynthesis.cancel()
移除所有语音谈话队列中的谈话。
SpeechSynthesis.getVoices()
返回当前设备所有可用声音的 SpeechSynthesisVoice列表。
SpeechSynthesis.pause()
把 SpeechSynthesis 对象置为暂停状态。
SpeechSynthesis.resume()
把 SpeechSynthesis 对象置为一个非暂停状态：如果已经暂停了则继续。
SpeechSynthesis.speak()
添加一个 utterance 到语音谈话队列；它将会在其他语音谈话播放完之后播放
