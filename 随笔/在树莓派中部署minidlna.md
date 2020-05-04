# 在树莓派中部署 minidlna
&emsp;&emsp;minidlna 是一个使用 dlna 协议的软件，可以向外提供流媒体服务，实现在线的视频或者音乐的播放。
## 步骤一
&emsp;&emsp;使用 apt-get 命令安装 minidlna
```
$ sudo apt-get update
$ sudo apt-get install minidlna
```

## 步骤二
&emsp;&emsp;修改 minidlna 配置文件，这里将 minidlna 的目录配置为 /minidlna
```
$ mkdir /minidlna
$ vi /etc/minidlna.conf
```
&emsp;&emsp;修改配置文件中的 media_dir 配置项
```
media_dir=/minidlna
```
## 步骤三
&emsp;&emsp;修改完配配置文件后可以将媒体文件放入 /minidlna 目录，或者使用 mount 命令将其他磁盘挂载到该目录。  
&emsp;&emsp;这里使用外置的U盘挂载到 /minidlna 目录，首先查看U盘设备。
```
$ sudo fdisk -l
```
&emsp;&emsp;可以通过磁盘大小来判断U盘的盘符，并挂载该U盘，例如这里U盘设备为 /dev/sda1
```
$ sudo mount /dev/sda1 /minidlna
```
&emsp;&emsp;可以使用 ls 命令查看 /minidlna 是否挂载成功，成功显示U盘内容即可。
```
$ ls /minidlna
```
## 步骤四
&emsp;&emsp;启动 minidlna 服务，并查看服务状态。
```
$ /etc/init.d/minidlna restart
$ /etc/init.d/minidlna status
```
&emsp;&emsp;也可以使用 systemctl 命令启动服务
```
$ systemctl restart minidlna
$ systemctl status minidlna
```
&emsp;&emsp;启动成功之后可以在浏览器中查看到当前 minidlna 的服务状态，地址为 http://IP地址:8200  
&emsp;&emsp;或者在其他带有 dlna 功能的播放器中查看 minidlna 的媒体服务。