# starboot

a simple way to write java API and document for users, teams, and enterprises.

一个简单易用的在线接口生成、调试框架。

# 第一步：启用服务
	 //starboot-api:在项目启动类中创建扫描器,可以描扫多个包
	 Starbooter.star("项目名称","com.starbooter.app"...);
  
# 第二步：启用服务，使用参考：usercenter.java

注意：使用starbooter-api需要在pom中添加fastjson依赖：

 <dependency>
    <groupId>com.alibaba</groupId>
    <artifactId>fastjson</artifactId>
    <version>1.2.4</version>
</dependency>
