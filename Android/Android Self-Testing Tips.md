### Android 自测检查点
+ 某些情况下某个变量是否会造成空指针问题
+ 自测功能，通用的几点检查：
	+ 按下Home再返回是否正常
	+ 熄灭屏幕再打开会怎么样
	+ 切换成其它应用再切换回来会怎么样
	+ onResume, onPause是否处理好
+ 从低版本升级上来，会不会有问题
+ 打开手机的开发者选项，看新功能是否会导致过度绘制、是否会掉帧
+ 测试看是否影响启动速度：`adb shell am start -W 包名/Activity` 
+ 对比看APK大小是否增大（图片资源文件用`Tiny-JPG`压缩）
+ 跑一小时Monkey测试其稳定性
+ 试试看看App是否能被反编译
+ 检查Log是否关闭
+ 看看是否走的是Https，能否被抓包
