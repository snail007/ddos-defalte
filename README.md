# DDos-defalte
DDOS defalte是一款免费的用来防御和减轻DDoS攻击。它通过netstat监测跟踪创建大量网络连接的IP地址，在检测到某个结点超过预设的限制时，该程序会通过APF或iptables禁止或阻挡这些IP.  

#该版对原版进行了错误修复，而且进行了本地化不需要安装的时候下载文件。  

#安装步骤 
1. 下载 ddos-defalte.tar.gz
2. tar zxfv ddos-defalte.tar.gz
3. cd ddos-defalte
4. ./install.sh
5. 安装完毕
6. 配置文件位于 /usr/local/ddos/ddos.conf
7. ip白名单文件位于 /usr/local/ddos/ignore.ip.list ，格式：一行一个ip
8. 配置完毕之后执行命令 ddos 可以看到一行行的输出，每行：第一个是连接数 第二个是对ip  
/usr/local/sbin/ddos命令是脚本/usr/local/ddos/ddos.sh的一个软链接  
9. 我们只需要计划任务周执 ddos 命令即可。ddos每执行一次都会按着配置里面的设置封ip。
10. 比如可以这样执行计划任务 */1 * * * * /usr/local/ddos/ddos.sh >/dev/null 2>&1
11. 命令ddos有一些带参数的用法，可以通过ddos -h 了解用法。
