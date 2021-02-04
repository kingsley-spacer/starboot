# starboot
a simple way to write java API and document for users, teams, and enterprises.

#第一步：启用服务

//在项目启动类中创建扫描器

Starbooter.star("您的项目名称","扫描使用了api注解的包1","扫描使用了api注解的包2",...);

#第二步：使用注解

/**
 * @ApiCatalog 一级分类名称，方便接口管理
 */
@ApiCatalog(name = "用户中心")
/**
 * @ApiAuthor 接口作者
 */
@ApiAuthor(author = "kingsley")
public class usercenter {

	/**
	 * @ApiAuthor 
	 *  author - 接口作者，如果不指定到方法，则继承类的作者
	 */
	@ApiAuthor(author = "kingsleysb")
	/**
	 * @Api 
	 *  name - 接口名称
	 *  desc - 接口描述
	 *  url - 接口请求地址，如：/starbooter/signIn/
	 */
	@Api(name = "用户注册", desc = "用户注册帐号", url = "/starbooter/signIn/")
	
	/**
	 * @ApiParam 
	 *  name - 接口参数名称
	 *  desc - 接口参数描述
	 *  type - 接口参数的类型：目前支持string、file类型
	 */
	@ApiParam(name = "username", desc = "用户名", type = ApiParamDataType.String)
	@ApiParam(name = "password", desc = "用户密码", type = ApiParamDataType.String)
	@ApiParam(name = "avator",   desc = "用户头像", type = ApiParamDataType.File)
	
	/**
	 * @ApiField 
	 *  name - 返回字段名称
	 *  desc - 返回字段说明
	 */
	@ApiField(name = "status",  desc = "注册成功：status=1，status=2：注册失败")
	@ApiField(name = "request.info",  desc = "注册反馈消息")
	@ApiField(name = "request.code",  desc = "操作码，操作成功：code=200，操作失败：code=500")
	public void signUp() {
	}
}
