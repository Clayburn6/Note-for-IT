### 用户列表接口
+ 接口版本`v1`
+ 请求方式`GET`
+ 请求地址`localhost:8080/UserManager/list`

> 请求参数

无
> 返回参数

| 参数名称 | 必须 | 参数位置 | 默认值 |
|:----:|:---:|:---:|:---:|
|username|是|responseBody|无
|email|是|responseBody|无
|phone|是|responseBody|无
> 返回示例

        [    
            {
                // 有多条记录，这里只写出一条
                "username":"小明"
                "email":"132@163.com"
                "phone":"12345678900"
            }
        // ...
        ]

### 用户详情接口
+ 接口版本`v1`
+ 请求方式`GET`
+ 请求地址`localhost:8080/UserManager/detail`

> 请求参数

| 参数名称 | 必须 | 参数位置 | 默认值 |
|:----:|:---:|:---:|:---:|
|username|是|url|无

> 返回参数

| 参数名称 | 必须 | 参数位置 | 默认值 |
|:----:|:---:|:---:|:---:|
|username|是|responseBody|无
|email|是|responseBody|无
|phone|是|responseBody|无
|password|是|responseBody|无
|headphoto|是|responseBody|无

> 请求示例

        {
            "username":"小明"
        }

> 返回示例

        {
            "username":"小明"
            "email":"123@163.com"
            "phone":"12345678900"
            "password":"123456"
            "headphoto":"一个url"
        }

### 新增用户接口
+ 接口版本`v1`
+ 请求方式`POST`
+ 请求地址`localhost:8080/UserManager/add`

> 请求参数

| 参数名称 | 必须 | 参数位置 | 默认值 |
|:----:|:---:|:---:|:---:|
|username|是|post表单|无
|email|是|post表单|无
|phone|是|post表单|无
|password|是|post表单|无
|headphoto|是|post表单|无

> 返回参数

无

> 请求示例

        {
            "username":"小明"
            "email":"123@163.com"
            "phone":"12345678900"
            "password":"123456"
            "headphoto":"一个url"
        }

### 编辑用户接口
+ 接口版本`v1`
+ 请求方式`POST`
+ 请求地址`localhost:8080/UserManager/update`

> 请求参数

| 参数名称 | 必须 | 参数位置 | 默认值 |
|:----:|:---:|:---:|:---:|
|username|是|post表单|无
|email|是|post表单|无
|phone|是|post表单|无
|password|是|post表单|无
|headphoto|是|post表单|无

> 返回参数

无

> 请求示例

        {
            "username":"小明"
            "email":"123@163.com"
            "phone":"12345678900"
            "password":"123456"
            "headphoto":"一个url"
        }

### 普通用户重置密码接口
+ 接口版本`v1`
+ 请求方式`GET`
+ 请求地址`localhost:8080/UserManager/changepsw`

> 请求参数

| 参数名称 | 必须 | 参数位置 | 默认值 |
|:----:|:---:|:---:|:---:|
|oldpw|是|url|无
|newpw|是|url|无

> 返回参数

无

> 请求示例

        {
            "oldpw":"123456"
            "newpw":"654321"
        }
