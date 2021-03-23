# ssm客户关系管理系统
ssm客户关系管理系统

#### 介绍
```
客户关系管理系统主要功能包括：
  系统管理：
     用户管理
     日志管理
     权限管理
     角色管理
     系统信息
  客户管理
     我的客户
     联系跟进
  客户流失
  销售机会
  客户服务
     我的服务
     服务统计
  客户关怀
  统计
  个人中心  
```
源码获取地址：[点此获取](http://www.shuyue.fun/?type=productinfo&id=177)

#### 环境需要
```
1.运行环境：最好是java jdk 1.8，我们在这个平台上运行的。其他版本理论上也可以。
2.IDE环境：IDEA，Eclipse,Myeclipse都可以。推荐IDEA;
3.tomcat环境：Tomcat 7.x,8.x,9.x版本均可
4.硬件环境：windows 7/8/10 1G内存以上；或者 Mac OS；
5.是否Maven项目: 是；查看源码目录中是否包含pom.xml；若包含，则为maven项目，否则为非maven项目 
6.数据库：MySql 5.7版本；
```

#### 系统框架
```
spring框架
springmvc框架
mybatis框架
Logback日志框架
安全验证框架
maven框架
layui前端框架
shiro安全框架
```
#### 系统关键性技术

```
基于角色的权限访问控制RBCA（Role-Based Access Control）
Spring+Springmvc+Mybatis三大框架
Ajax技术
springmvc文件上传
shiro安全框架
Redis缓存
JavaMail邮件
基于aop切面的日志管理
Layui前端框架
登录验证码
富文本输入框
md5加密加盐
```

#### 使用说明
```
1. 使用Navicat或者其它工具，在mysql中创建对应名称的数据库，并导入项目的sql文件,sql文件命名为CRM.sql，其中‘user’表为账户表；
2. 部署项目前，需要配置好MqSQL数据库，Redis数据库、mail邮箱，这三个配置文件都在crm/src/main/resources/properties
3. 使用IDEA/Eclipse/MyEclipse导入项目，Eclipse/MyEclipse导入时，若为maven项目请选择maven;若为maven项目，导入成功后请执行maven clean;maven install命令，配置tomcat，然后运行；
4.项目登录帐号：malizhi(管理员级别)，密码123456，部署项目后，可以到测试类中（test包下的TestUserService）进行添加账户，密码经过md5加密加盐
5.登录页：如果是本地部署 http://localhost:8080/crm2/pages/login.jsp ,端口号以及项目名要与部署的环境一致
6.订单可以在客户流失（客户是否流失由Spring定时器定时检测）模块中，点击客户详情，可以查看到此客户的历史订单，关于订单的数据问题，因为在企业模式中，订单数据是从销售系统中获取的，但由于没有外接销售系统，所以订单数据以及产品定价的数据是自个插入数据库的。
```
#### 部署过程异常错误解决方法
```
1.权限，菜单都会缓存到redis中，如果redis无法连接，将会报空指针错误或登陆后首页会显示404，请确保能连接上redis数据库
2.如果有报此异常org/hyperic/sigar/SigarException，可以将WEB-INF/lib下的文件（根据你的系统以及位数选择）放在你的JDK/bin目录下
3.在发布出来前，由于隐私关系删除了部分登录帐号（客户经理），如果出现此客户找不到对应的客户经理，删掉此客户即可
```

![输入图片说明](https://images.gitee.com/uploads/images/2021/0305/171035_c9b1b83d_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0305/171102_d64f3f07_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0305/171129_898f5213_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0305/171144_a578bfe8_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0305/171158_b5b46ef7_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0305/171209_c20c0dcf_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0305/171220_91534f93_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0305/171235_e4b4ddcc_863230.png "屏幕截图.png")

源码获取地址：[点此获取](http://www.shuyue.fun/?type=productinfo&id=177)
