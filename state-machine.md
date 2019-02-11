### 状态机
- OpenGL自身是一个巨大的状态机(State Machine)：一系列的变量描述OpenGL此刻应当如何运行
- OpenGL的状态通常被称为OpenGL上下文(Context)
- 通常使用如下途径去更改OpenGL状态：设置选项，操作缓冲
- 最后，使用当前OpenGL上下文来渲染。

### 通常的过程
- 假设当画线段而不是三角形的时候，通过改变一些上下文变量来改变OpenGL状态
- 一旦改变了OpenGL的状态为绘制线段，下一个绘制命令就会画出线段而不是三角形

### 大状态机
- 当使用OpenGL的时候，我们会遇到一些状态设置函数(State-changing Function)，这类函数将会改变上下文
- 以及状态使用函数(State-using Function)，这类函数会根据当前OpenGL的状态执行一些操作
- 只要你记住OpenGL本质上是个大状态机，就能更容易理解它的大部分特性