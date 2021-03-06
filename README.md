# CryopolyMerization
文档冷聚合 -- 6.1

# ☆ 强制认证手机号

<br/>

> JSONRPC接口


*1.密码验证*

```
    方法名:mobile.bind.authPassword
```

请求:

| 名称	 | 类型 | 必传 |描述
|:---|---|---|:---|
|**account**|String|Y|用户账号
|**password**|String|Y|用户密码

```
{
	"jsonrpc": "2.0",
	"method": "mobile.bind.authPassword",
	"id": "xxx",
	"params": {
		"account": "13813840001",
		"password": "*********"
	}
}
```

响应:

|名称	 | 类型 | 必回 |描述
|:---|---|---|:---|
|**phone**|String|N|用户手机存在返回
|**userId**|String|Y|用户ID

```
{
    "id": "xxx",
    "result": {
        "phone":"138741092552",
        "userId":"u40001"
    },
    "jsonrpc": "2.0"
}
```


<br/>

*2.手机绑定*

```
    方法名:mobile.bind.bindMobile
```

请求:

| 名称	 | 类型 | 必传 |描述
|:---|---|---|:---|
|**phone**|String|Y|手机号


```
{
	"jsonrpc": "2.0",
	"method": "mobile.bind.bindMobile",
	"id": "xxx",
	"params": {
		"phone": "13813840001"
	}
}
```

响应:

|名称	 | 类型 | 必回 |描述
|:---|---|---|:---|

```
{
    "id": "xxx",
    "result": {},
    "jsonrpc": "2.0"
}
```

<br/>

*3.验证码验证*

```
    方法名:mobile.bind.authCode
```

请求:

| 名称	 | 类型 | 必传 |描述
|:---|---|---|:---|
|**phone**|String|Y|手机号
|**authCode**|String|Y|验证码


```
{
	"jsonrpc": "2.0",
	"method": "mobile.bind.authCode",
	"id": "xxx",
	"params": {
		"phone": "13813840001",
		"authCode":"5428"
	}
}
```

响应:

|名称	 | 类型 | 必回 |描述
|:---|---|---|:---|

```
{
    "id": "xxx",
    "result": {},
    "jsonrpc": "2.0"
}
```

