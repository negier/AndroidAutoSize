## 修改AndroidAutoSize中的AutoSizeConfig的源码，将application.registerComponentCallbacks中onConfigurationChanged中对三大基本运算单元的修改给删掉。这样可以破除锁屏对应用的影响。

## 为什么？
如果是横屏这时手机锁屏，锁屏是竖屏，这时就会触发onConfigurationChanged回调，设置一些和我们应用完全无关的三大基本运算单元的值，而且我发现的问题手机上，锁屏时RecyclerView的所有itemView还会刷新一遍，用的是错误的值，导致我们解锁时看到的界面异常。

更多详见自己的笔记《Debug AndroidAutoSize 已完美解决》，这是备份修改这个库的部分。

*所实话我难以想象上万star的项目是有问题的*
