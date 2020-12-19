1. 服务器关闭ctrl+c后, 如果不设置set....重新执行绑定失败:Address already in use
有一个time_wait, 需要等待time_wait结束
2. 客户端ctrl+c执行过程
客户端操作系统协议栈会自动向服务端发送FIN报文, 然后服务端ret=0, close(fd)服务端发送FIN报文
