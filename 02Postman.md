

### 安装

> 下载应用安装
>
> - [Postman](https://www.postman.com/)
>
> chrome 浏览器插件安装：2018年之后不再支持



### 使用

> 新建、导入（import 可以导入脚本）
>
> ![image-20200330155924398](E:\测试\测试工具\images\postman\01.png)
>
> 

> Postman 接口测试
>
> - 进行接口测试的必要条件
>   1. 请求地址
>   2. 请求协议
>   3. 请求方式
>   4. 请求头
>   5. 参数
> - 请求方式
>   1. get
>   2. post
>   3. push
>   4. delete
> - 传参格式
>   1. 表单提交
>   2. 请求体提交

> 调用变量的方式：`{{变量名}}`

> Postman 接口关联
>
> - 方式：
>   1. 设置环境变量
>   2. 设置全局变量
>   3. Tests 设置变量

> Postman 相应断言
>
> - 常用：
>   1. `Response body:JSON value check`：检验返回结果中某个字段值是否等于指定值
>   2. `Status code:Code is 200`：检验响应头是否包含某个值
> - 其他：
>   1. `Response body:Contains string`：检验返回结果是否包含某个字符串
>   2. `Response body:Is equal to a string`：校验返回结果是否等于该字符串
>   3. `Response header:Content-type header check`：校验响应头是否包含某个值
>   4. `Response time is less than 200ms`：校验响应时间是否少于 200 ms

> Postman 参数化
>
> - 参数化方式：`csv, txt, json`文档参数化

> Postman 随机数
>
> - 大批量测试以及自动化测试过程中，对同一个不允许重复的参数进行传参时，可以保证其不被重复
> - 方式：
>   1. `{{$guid}}`：添加一个 `V4` 风格的 `guid`
>   2. `{{$timestamp}}`：将当前的时间戳，精确到秒，精准到毫秒，后面增加 000 即可
>   3. `{{$randomInt}}`：添加 0 -- 1000 之间的随机整数

> Monitor 监控器
>
> - 是 Postman 自带的监控模块
>   - 能依据设置按分钟，小时，周进行监控
>   - 当借口出现错误的情况下，可以设置邮件通知
>   - 缺点：免费每个月只有1000配额