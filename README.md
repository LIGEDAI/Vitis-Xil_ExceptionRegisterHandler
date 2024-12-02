# Xil_ExceptionRegisterHandler函数的用法
## 1.1定义
`Xil_ExceptionRegisterHandler`是Xilinx提供的一个用于注册异常处理程序的函数，其原函数为`void Xil_ExceptionRegisterHandler(u32 Exception_id, Xil_ExceptionHandler Handler, void *Data){......}`
- `u32 Exception_id`为指定异常的类型，通常是一个与异常相关的标识符。例如，`XIL_EXCEPTION_ID_IRQ_INT` 表示中断异常，`XIL_EXCEPTION_ID_SWI` 表示软件中断，等等。
- `Xil_ExceptionHandler Handler`是指向一个异常处理函数的指针。这个函数将在对应异常发生时被调用。它的原型通常如下：
`typedef  void  (*Xil_ExceptionHandler)(void *Data);`
- 
