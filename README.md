# IntegrateApplication

整合应用，前后端彻底分离，此后端提供所有应用所需的接口。

# 注意事项

解密部分若报错非法的密钥长度,是因为标准的Java密码学支持里,不支持16位长的密钥,解决方法:请搜索JCE8。

# 功能说明

## 公共部分

公共部分包括易班授权认证,公共管理员,错误信息报告类,易班信息解析类。

### 授权认证

由前端把数据发送到接口,接口调用公共包里Auth模块里的方法进行解密,存session。

### 公共管理员

管理员信息由yibanid确定,存进数据库里。公共包里提供了方法判断是否是管理员。

### 错误信息报告类

若有出错信息需要返回,用公共包dto里的ErrorReporter生成对象。若属性不足,自己继承写新的。