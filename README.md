# tomcat-redis-session-manager

------

tomcat版本
--------

支持tomcat8.5， 没有对tomcat8.0、tomcat7做测试


用法
---

添加下面的配置到tomcat的conf文件夹下的context.xml中

```bash
<Valve className="com.cxhello.tomcat.redissessions.RedisSessionHandlerValve"/> 
<Manager className="com.cxhello.tomcat.redissessions.RedisSessionManager" 
		  host="192.168.223.135"
		  port="6379"
		  database="0" 
		  maxInactiveInterval="60" /> 
```



复制下面的文件到tomcat/lib目录:

- commons-pool2-2.3.jar
- jedis-2.7.3.jar
- tomcat-redis-session-manager.jar

感谢
---

此版本修改来自两位大牛

https://github.com/jcoleman/tomcat-redis-session-manager

https://github.com/cc-chen/tomcat8.5-redis-session-manager 

