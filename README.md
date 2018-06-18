## Go 基础

与C/C++语法差异

+ 导包

+ 导出名
    以大写字母开头，相当于定义好的常量

+ 类型后置
    参数、变量的类型以及函数的返回值放在后面

+ 函数
    函数中多个同类型参数可只保留最后一个类型， var声明变量列表也可以只保留最后一个类型；
    支持多值返回；
    支持返回值命名；

+ 变量
    支持从初始值获取类型；

+ 短变量 :=
    声明+赋值

+ 基本类型
    bool
    string
    int int8 int16 int32 int64
    uint uint8 uint16 uint32 uint64 uintptr
    byte
    rune
    float32 float64
    complex64 complex128

+ 格式化输出
    %T 输出类型
    %v 输出值

+ 零值

+ for 没有() , 兼顾while的结构
    for 无限循环 for{}

+ if 没有()

+ 迭代
    迭代函数 = 条件判断跳出 + 参数校对 + 调用自身；

+ switch语句go自动提供每条case的break，支持默认值，没有条件的switch可以替换if-then-else

+ defer将函数推迟到外层函数返回后执行
    推迟调用的函数其参数会立即求值，但直到外层函数返回前该函数都不会被调用。
    推迟的函数调用会被压入一个栈中。当外层函数返回时，被推迟的函数会按照后进先出的顺序调用。

+ 空指针零值为 nil, Go没有指针运算

+ 切片 a[low, high] 左闭区间，右开区间
    切片的长度就是它所包含的元素个数。
    切片的容量是从它的第一个元素开始数，到其底层数组元素末尾的个数。
    支持使用 make 创建切片。
    切片可以包含任何类型，包括切片。
    向切片追加元素时，切片空间容量不够用时会2的指数级扩容即容量为0 2 4 8 16 ...。

+ Go 程
    go f(x, y, z)    f, x, y 和 z 的求值发生在当前的 Go 程中，而 f 的执行发生在新的 Go 程中。
    Go程同步：

+ 信道
    - 信道创建
        ch := make(chan int)
    -