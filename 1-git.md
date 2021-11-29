## 1. git 代理造成的Failed to connect to 127.0.0.1 port 7891: Connection refused

- 先执行git config --global -l命令 查看git代理设置
- 继续在终端执行git config --global -e进入编辑状态，然后删掉7891端口有关的那条设置

然后保存重新执行就好了~

作者：Tobesky
链接：https://www.jianshu.com/p/9ed0337806b2
来源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

## 2. git clone / push 时遇到time out的错误：
第1种方法：查看windows 电脑的网络代理设置：《控制面板》 -- 《网络和Internet》-- 《Internet选项》-- 《连接》 -- 《局域网设置》-- 《只勾选自动检测设置》

第2种方法：git config --global http.sslVerify "false"

第3种方法：\
git config --global --unset http.proxy
git config --global --unset https.proxy


## 3. github 相关的常用命令
删除已经push到远端的 .idea 文件夹及文件夹中的文件
- git rm -r --cache .idea/ 

git push remote_name local_name 
- git push origin master  // origin 时远端分支， master是本地分支

对项目中的子分支的操作
git submodule init && git submodule update
git submodule foreach git switch master
git submodule foreach git pull
git submodule foreach git status