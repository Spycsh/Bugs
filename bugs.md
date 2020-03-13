# Bugs

## 2020/03/13 ImportError

安装tensorflow 出现 ImportError: DLL load failed: A dynamic link library (DLL) initialization routine failed

### 原因：

电脑不支持AVX操作

### 解决方法：
把TensorFlow降版本，卸载pip uninstall tensorflow ，然后按照1.5pip install tensorflow==1.5.0.可能pip会找不到1.5.0，这个时候就需要自己去找1.5.0的wheel了

如果是死活不想降版本的人话（比如我），就进tensorflow-windows-wheel,选择sse2版本的wheel下载，然后pip install <filename.whl>就可以按照完成。

————————————————
版权声明：本文为CSDN博主「佐斯特勒」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/weixin_42313701/article/details/104756483

