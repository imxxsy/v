
安装V
```
bash <(curl -sSL "https://raw.githubusercontent.com/imxxsy/v2mtp/main/v.sh")
```
安装MTP

创建程序目录并进入
```
mkdir /home/mtproxy && cd /home/mtproxy
```
安装
```
curl -s -o mtproxy.sh https://raw.githubusercontent.com/imxxsy/v2mtp/main/mtproxy.sh && chmod +x mtproxy.sh && bash mtproxy.sh
```
使用
```
# 进入程序目录
cd /home/mtproxy

# 运行
bash mtproxy.sh start

# 调试
bash mtproxy.sh debug

# 停止
bash mtproxy.sh stop

# 重启
bash mtproxy.sh restart
```

####卸载

因为是绿色版卸载极其简单，直接删除程序目录即可
```
rm -rf /home/mtproxy
```
开机启动
编辑 /etc/rc.local 开机自启服务文件，将如下代码添加到开机自启脚本中；
# 编辑自启文件
```
vi /etc/rc.local
```
# 添加代码
```
bash /home/mtproxy/mtproxy.sh start > /dev/null 2>&1 &
```
