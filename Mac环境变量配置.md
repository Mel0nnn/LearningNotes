mac一般使用bash作为默认shell，如果安装了oh my sh，则默认使用zshshell。
Mac系统环境变量的加载顺序：

1. /etc/profile      建议不修改
2. /etc/paths        全局建议修改这个
3. ~/.bash_profile   添加用户级环境变量,该文件仅仅执行一次
4. ~/.bash_login 
5. ~/.profile 
6. ~/.bashrc

/etc/profile和/etc/paths是系统级别的，系统启动后就会加载。后面几个是当前用户级的环境变量。
如果~/.bash_profile存在，后面几个文件就会忽略不读，不存在时，才会以此类推读取后面的文件。
~/.bashrc没有上述规则，他始终加载，他是在bash shell打开的时候载入的。

设置Path的语法：
export PATH=$PATH:<PATH 1>:<PATH 2>:<PATH 3>:------:<PATH N>

设置想立刻生效：
source 相应的文件
