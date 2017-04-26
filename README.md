# FtpServer-FtpClient
FTP服务器和客户端
版本1： 使用linux系统原生API实现简单的FTP服务器和客户端，在本地和远程都通过测试。

版本2： 将版本1的FTP服务器发送文件的read和write部分，改为了使用mmap和write系统调用发送文件。

版本3： 将版本2的使用mmap和write发送文件部分，改为了使用sendfile系统调用发送文件。

版本4： 将版本3的服务器使用sendfile发送文件部分，改为了使用splice系统调用发送文件。 将版本3的客户端使用的read和write接收文件部分，改为了使用splice系统调用接收文件。

版本5： 将socket系统调用的函数封装成一个类Socket，见文件mysocket.h。 版本5的服务器和客户端使用的是类Socket来创建socket。
