## 1. git 代理造成的Failed to connect to 127.0.0.1 port 7891: Connection refused

- 先执行git config --global -l命令 查看git代理设置
- 继续在终端执行git config --global -e进入编辑状态，然后删掉7891端口有关的那条设置

然后保存重新执行就好了~

作者：Tobesky
链接：https://www.jianshu.com/p/9ed0337806b2
来源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。