#知识点

1. 内存的几大区域：
    - 栈区  
        * 编译器自动分配并且释放,存放函数的参数值,局部变量等
    - 堆区  
        * 由程序员分配和释放,主要存放new构造的对象和数组.只要是new出来的对象,就需要delete来销毁
    - 全局区（静态区）
        * 用来存放全局变量和静态变量,程序结束后由系统释放
    - 文字常量区
        * 存放常量字段,程序结束后由系统释放
    - 代码区
        * 存放函数的二进制代码

2. const char* | char const* | char *const | const char[] 的区别：
    - const char* = char const*: 指针指向可以改变,而字符串内容不可以改变
    - char *const: 字符串内容可以改变,而指针指向不可以改变
    - const char []: 字符串的内容和指向都不可以改变(只有这种方式可以在头文件中书写)

3. TCP是全双工的协议，就是客户端在给服务端发信息的同时，服务端也可以给客户端发送信息。三次握手  
    保证双方都能够收到对方的信息，并且避免因为超时重传或者丢包的情况而建立多个TCP连接。四次挥手
    保证服务端数据已经传输完成才结束。
   
4. CMake Error: Cannot determine link language for target  
    SET(CTP_TD_SRCS td) set变量的时候指定目录而没有到具体文件，导致编译器不知道要采用什么语言编译
    
5. 只登录一次，一个启动，作为服务。再启动另外一个层次
    共享内存，tcp socket，
    
6. 进程间通信的方式
    - 管道（半双工）
    
7. 需求确认邮件