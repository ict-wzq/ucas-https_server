用c语言实现了一个简单的https服务器，实现了以下功能：

1.	支持GET和POST方法；
2.	可以下载文件和上传==小文件==；
3. <del>支持分块传输，支持管道</del>
4. 使用openssl库，支持HTTPS；
5.	使用libevent支持多路并发；
