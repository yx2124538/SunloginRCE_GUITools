# SunloginRCE GUI

向日葵命令执行图形化利用工具

纯学习开发使用，大佬勿喷

# 工具界面

漏洞检测 



命令执行（主要是利用cmd去执行，powershell查杀比较严，故没有用powershell去执行命令）

IMG/1.png

增加Bypass模式 （主要利用 /check?cmd=ping/../进行部分杀软的绕过）

目标环境开启某数字安全卫士和杀毒软件 采用命令执行会被直接拦截

https://github.com/ddwGeGe/SunloginRCE_GUITools/blob/master/IMG/3.png

采用bypass模式可进行绕过 执行部分命令

https://github.com/ddwGeGe/SunloginRCE_GUITools/blob/master/IMG/4.png

# 参考链接

GUI框架部分代码及相关代码执行语句有参考如下师傅文章，感谢前辈的总结

https://github.com/yhy0/ExpDemo-JavaFX

https://mp.weixin.qq.com/s/417I9fuDHN53VGZcnZYS3g

https://mp.weixin.qq.com/s/7xgiLVx6Nq0F9eKxcCV8nw

# 存在BUG问题

1、再搭建环境测试的时候，发现执行 tasklist /svc、dir、netstat -ano等命令时，使用burpsuite会回显成功，但时间比较久，故将http请求的读取超时时间进行了延长，所以在执行该相关命令会有稍微的卡顿，可稍微等一会儿 ~~。

2、实战中测试，发现目标存在漏洞，但一执行命令就会卡死（采用Bypass模式也不行），推测是其他杀软或者防护进行拦截，导致卡死

3、可能使用中还有很多的bug问题，有时间在研究 研究，大佬勿喷

# 免责声明

1、本工具仅用于学习交流，请勿在未授权的情况下，进行非法攻击等一切违法行为，如您在使用本工具的过程中存在任何非法行为，您将自行承担所有后果，与本作者无关。
