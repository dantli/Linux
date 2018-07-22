# 网络管理
 + ifconfig
  +  查看网卡信息：`ifconfig`
  +  关闭网卡eth0：`sudo ifconfig eth0 down`
  +  开启网卡eth0：`sudo ifconfig eth0 up`
  +  给eth0配置临时IP：`sudo ifconfig eth0 IP`

 + netstat
  +  netstat [选项] 显示网络连接、路由表和网络接口信息
  +  -a 显示所有socket,包括正在监听的。
  +  -c 每隔1秒就重新显示一遍,直到用户中断它。
  +  -i 显示所有网络接口的信息,格式同“ifconfig -e”。
  +  -n 以网络IP地址代替名称,显示出网络连接情形。
  +  -r 显示核心路由表,格式同“route -e”。
  +  -t 显示TCP协议的连接情况。
  +  -u 显示UDP协议的连接情况。
  +  -v 显示正在进行的工作
 +



+ grep
  +  grep [options] PATTERN [FILE...],PATTERN支持正则表达式，options如下：
  +  -c:只输出匹配行的计数。
  +  -I:不区分大小写(只适用于单字符)。
  +  -h:查询多文件时不显示文件名。20
  +  -l:查询多文件时只输出包含匹配字符的文件名。
  +  -n:显示匹配行及行号。
  +  -s:不显示不存在或无匹配文本的错误信息。
  +  -v:显示不包含匹配文本的所有行。
  +  -R: 连同子目录中所有文件一起查找
