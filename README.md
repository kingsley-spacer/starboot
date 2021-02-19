# starboot

a simple way to write java API and document for users, teams, and enterprises.

一个简单易用的在线接口生成、调试框架。

# 第一步：启用服务
	 //starboot-api:在项目启动类中创建扫描器,可以描扫多个包
	 Starbooter.star("项目名称","com.starbooter.app",...);
# 第二步：配置访问路径
         //获取接口列表的HTML页面字符串对象
         String page = ApiHtml.getApiPage();
	 //这里使用PrintWriter渲染页面，可以根据自己的实际框架来使用框架的渲染方式
	 HttpServletResponse response = getResponse();
	 response.setContentType("text/html;charset=utf-8");
	 PrintWriter out = response.getWriter();
	 out.println(page);
	 out.close();
	 
# 第三步：使用接口，参考：usercenter.java

# 注意：使用starbooter-api需要在pom中添加fastjson依赖：

      <dependency>
         <groupId>com.alibaba</groupId>
         <artifactId>fastjson</artifactId>
         <version>1.2.4</version>
      </dependency>
