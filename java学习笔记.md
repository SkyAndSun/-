#Tomcat配置参数优化
****

Tomcat在使用的过程中会遇到很多报错，有些是程序的报错，但还有一部分是tomcat本身的报错，我们可以通过优化tomcat的初始配置来提高tomcat的性能。Tomcat的优化主要体现在两方面：内存、并发连接数。

****
##1.内存优化：
优化内存，主要是在bin/catalina.bat/sh 配置文件中进行。linux上，在catalina.sh中添加：

<pre> JAVA_OPTS="-server -Xms1G -Xmx2G -Xss256K -Djava.awt.headless=true -Dfile.encoding=utf-8 -XX:MaxPermSize=256m -XX:PermSize=128M -XX:MaxPermSize=256M"
</pre>

其中：
		


