smartformsAPI

1、智能表单平台API接口； 2、流程业务平台API接口；
扩展使用说明

1、目录说明 com.gzsolartech.smartforms. --api --controller 控制层 --mode DTO层 --service 业务逻辑数据处理层

--entity 实体类

2、扩展使用 (1) 在控制层创建controller类，继承BaseApiController (2) 在controller层类头部添加

    @Controller    // 注入控制层标识
    @RequestMapping("/api/datAppAcl")   //映射访问路径
    @Api(tags="Application library permissionsl")  //添加对改api 控制层的说明

(3) 在controller方法头部添加

	@ApiOperation(notes = "获取应用库的acl权限",  httpMethod = "POST", value = "获取应用库的acl权限")  //添加方法注释说明
@RequestMapping(value="/getAllAppAcl",method=RequestMethod.POST)   //映射访问路径    标明请求方式GET、POST、DELETE、PUT
@ResponseBody    

(4) 添加controller方法参数说明，如下参数

// 	required是否必须参数，name值对应参数属性，value 为参数说明   @RequestParam 标明为参数类型
	@ApiParam(required = true, name = "token", value = "用户标识令牌")  @RequestParam String token    
