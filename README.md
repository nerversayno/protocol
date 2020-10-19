
**标题：管理系统_接口文档**


**简介**：描述：用暂无

**HOST**:172.16.106.14

**联系人**:迈尔医疗

**Version**:版本号:1.0.0

**接口路径**：/v2/api-docs?group=协议文档


# 1.用户信息管理

## 用户登录


**接口说明**:



**接口地址**:`/mayer/mauser/mlogin`


**请求方式**：`GET`


**consumes**:``


**produces**:`["*/*"]`



**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|deviceCode| 设备号  | header | true |string  |    |
|passwd| 密 码  | query | true |string  |    |
|uname| 用户名  | query | true |string  |    |

**响应数据**:

```json
{
	"code": 0,
	"currTime": 0,
	"data": {
		"deptId": 0,
		"deptName": "",
		"deviceCode": "",
		"email": "",
		"id": 0,
		"loginDate": "",
		"loginIp": "",
		"loginName": "",
		"phonenumber": "",
		"token": "",
		"userName": ""
	},
	"hasNext": true,
	"msg": ""
}
```

**响应参数说明**:


| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code|   |int32  |    |
|currTime|   |int64  |    |
|data|   |用户对象  | 用户对象   |
|hasNext|   |boolean  |    |
|msg|   |string  |    |



**schema属性说明**




**用户对象**

| 参数名称         |  说明          |   类型  |  schema |
| ------------ | ------------------|--------|----------- |
|deptId | 部门ID   |int64  |    |
|deptName | 部门名称   |string  |    |
|deviceCode | 设备编号   |string  |    |
|email | 登录名称   |string  |    |
|id | 用户ID   |int64  |    |
|loginDate | 最后登陆时间   |date-time  |    |
|loginIp | 最后登陆IP   |string  |    |
|loginName | 登录名称   |string  |    |
|phonenumber | 登录名称   |string  |    |
|token | 登录token   |string  |    |
|userName | 登录名称   |string  |    |

**响应状态码说明**:


| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |ResultModel«用户对象»|
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 退出登录


**接口说明**:



**接口地址**:`/mayer/mauser/mlogout`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["*/*"]`



**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|deviceCode| 设备号  | header | true |string  |    |
|userId| 用户ID  | header | true |string  |    |

**响应数据**:

```json
{
	"code": 0,
	"currTime": 0,
	"data": {},
	"hasNext": true,
	"msg": ""
}
```

**响应参数说明**:


| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code|   |int32  |    |
|currTime|   |int64  |    |
|data|   |object  |    |
|hasNext|   |boolean  |    |
|msg|   |string  |    |





**响应状态码说明**:


| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |ResultModel|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
# 2.项目信息管理

## 删除项目


**接口说明**:



**接口地址**:`/mayer/project/delete/project`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["*/*"]`



**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|deviceCode| 设备号  | header | true |string  |    |
|projectId| projectId  | query | false |integer  |    |
|userId| 用户ID  | header | true |string  |    |

**响应数据**:

```json
{
	"code": 0,
	"currTime": 0,
	"data": {},
	"hasNext": true,
	"msg": ""
}
```

**响应参数说明**:


| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code|   |int32  |    |
|currTime|   |int64  |    |
|data|   |object  |    |
|hasNext|   |boolean  |    |
|msg|   |string  |    |





**响应状态码说明**:


| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |ResultModel|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 获取项目对象


**接口说明**:



**接口地址**:`/mayer/project/get/{id}/one`


**请求方式**：`GET`


**consumes**:``


**produces**:`["*/*"]`



**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|deviceCode| 设备号  | header | true |string  |    |
|id| 项目ID  | path | true |string  |    |
|userId| 用户ID  | header | true |string  |    |

**响应数据**:

```json
{
	"code": 0,
	"currTime": 0,
	"data": {
		"clearTime": 0,
		"createAt": "",
		"createName": "",
		"createUser": 0,
		"cureTime": 0,
		"fixed": 0,
		"id": 0,
		"name": "",
		"sequence": 0,
		"temperature": 0
	},
	"hasNext": true,
	"msg": ""
}
```

**响应参数说明**:


| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code|   |int32  |    |
|currTime|   |int64  |    |
|data|   |项目信息  | 项目信息   |
|hasNext|   |boolean  |    |
|msg|   |string  |    |



**schema属性说明**




**项目信息**

| 参数名称         |  说明          |   类型  |  schema |
| ------------ | ------------------|--------|----------- |
|clearTime | 清理时间,min   |int32  |    |
|createAt | 创建时间   |date-time  |    |
|createName | 创建人名称   |string  |    |
|createUser | 创建人ID   |int64  |    |
|cureTime | 热疗时间   |int32  |    |
|fixed | 是否固定，1-固定；2-非固定   |int32  |    |
|id | ID   |int64  |    |
|name | 项目名称   |string  |    |
|sequence | 序次   |int32  |    |
|temperature | 温度   |float  |    |

**响应状态码说明**:


| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |ResultModel«项目信息»|
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 获取项目列表


**接口说明**:



**接口地址**:`/mayer/project/get/{page}/lst`


**请求方式**：`GET`


**consumes**:``


**produces**:`["*/*"]`



**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|deviceCode| 设备号  | header | true |string  |    |
|page| 页码（从1开始）  | path | true |string  |    |
|userId| 用户ID  | header | true |string  |    |

**响应数据**:

```json
{
	"code": 0,
	"currTime": 0,
	"data": [
		{
			"clearTime": 0,
			"createAt": "",
			"createName": "",
			"createUser": 0,
			"cureTime": 0,
			"fixed": 0,
			"id": 0,
			"name": "",
			"sequence": 0,
			"temperature": 0
		}
	],
	"hasNext": true,
	"msg": ""
}
```

**响应参数说明**:


| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code|   |int32  |    |
|currTime|   |int64  |    |
|data|   |array  | 项目信息   |
|hasNext|   |boolean  |    |
|msg|   |string  |    |



**schema属性说明**




**项目信息**

| 参数名称         |  说明          |   类型  |  schema |
| ------------ | ------------------|--------|----------- |
|clearTime | 清理时间,min   |int32  |    |
|createAt | 创建时间   |date-time  |    |
|createName | 创建人名称   |string  |    |
|createUser | 创建人ID   |int64  |    |
|cureTime | 热疗时间   |int32  |    |
|fixed | 是否固定，1-固定；2-非固定   |int32  |    |
|id | ID   |int64  |    |
|name | 项目名称   |string  |    |
|sequence | 序次   |int32  |    |
|temperature | 温度   |float  |    |

**响应状态码说明**:


| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |ResultModel«List«项目信息»»|
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 新建项目


**接口说明**:



**接口地址**:`/mayer/project/put/project`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["*/*"]`



**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|clearTime| 清理时间,min  | query | true |integer  |    |
|createAt| 创建时间  | query | false |string  |    |
|createName| 创建人名称  | query | false |string  |    |
|createUser| 创建人ID  | query | false |integer  |    |
|cureTime| 热疗时间  | query | true |integer  |    |
|deviceCode| 设备号  | header | true |string  |    |
|fixed| 是否固定，1-固定；2-非固定  | query | true |integer  |    |
|id| ID  | query | false |integer  |    |
|name| 项目名称  | query | true |string  |    |
|sequence| 序次  | query | true |integer  |    |
|temperature| 温度  | query | true |number  |    |
|userId| 用户ID  | header | true |string  |    |

**响应数据**:

```json
{
	"code": 0,
	"currTime": 0,
	"data": {},
	"hasNext": true,
	"msg": ""
}
```

**响应参数说明**:


| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code|   |int32  |    |
|currTime|   |int64  |    |
|data|   |object  |    |
|hasNext|   |boolean  |    |
|msg|   |string  |    |





**响应状态码说明**:


| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |ResultModel|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 修改项目


**接口说明**:



**接口地址**:`/mayer/project/update/project`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["*/*"]`



**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|clearTime| 清理时间,min  | query | true |integer  |    |
|createAt| 创建时间  | query | false |string  |    |
|createName| 创建人名称  | query | false |string  |    |
|createUser| 创建人ID  | query | false |integer  |    |
|cureTime| 热疗时间  | query | true |integer  |    |
|deviceCode| 设备号  | header | true |string  |    |
|fixed| 是否固定，1-固定；2-非固定  | query | true |integer  |    |
|id| ID  | query | false |integer  |    |
|name| 项目名称  | query | true |string  |    |
|sequence| 序次  | query | true |integer  |    |
|temperature| 温度  | query | true |number  |    |
|userId| 用户ID  | header | true |string  |    |

**响应数据**:

```json
{
	"code": 0,
	"currTime": 0,
	"data": {},
	"hasNext": true,
	"msg": ""
}
```

**响应参数说明**:


| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code|   |int32  |    |
|currTime|   |int64  |    |
|data|   |object  |    |
|hasNext|   |boolean  |    |
|msg|   |string  |    |





**响应状态码说明**:


| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |ResultModel|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
# 3.客户信息管理

## 删除客户信息


**接口说明**:



**接口地址**:`/mayer/customer/delete/customer`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["*/*"]`



**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|customerId| customerId  | query | false |integer  |    |
|deviceCode| 设备号  | header | true |string  |    |
|userId| 用户ID  | header | true |string  |    |

**响应数据**:

```json
{
	"code": 0,
	"currTime": 0,
	"data": {},
	"hasNext": true,
	"msg": ""
}
```

**响应参数说明**:


| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code|   |int32  |    |
|currTime|   |int64  |    |
|data|   |object  |    |
|hasNext|   |boolean  |    |
|msg|   |string  |    |





**响应状态码说明**:


| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |ResultModel|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 获取客户信息


**接口说明**:



**接口地址**:`/mayer/customer/get/{id}/one`


**请求方式**：`GET`


**consumes**:``


**produces**:`["*/*"]`



**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|deviceCode| 设备号  | header | true |string  |    |
|id| 项目ID  | path | true |string  |    |
|userId| 用户ID  | header | true |string  |    |

**响应数据**:

```json
{
	"code": 0,
	"currTime": 0,
	"data": {
		"createAt": "",
		"createName": "",
		"createUser": 0,
		"cusBirthday": "",
		"cusGender": 0,
		"cusHeight": 0,
		"cusName": "",
		"cusStatus": 0,
		"cusWeight": 0,
		"deptId": 0,
		"id": 0
	},
	"hasNext": true,
	"msg": ""
}
```

**响应参数说明**:


| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code|   |int32  |    |
|currTime|   |int64  |    |
|data|   |客户信息  | 客户信息   |
|hasNext|   |boolean  |    |
|msg|   |string  |    |



**schema属性说明**




**客户信息**

| 参数名称         |  说明          |   类型  |  schema |
| ------------ | ------------------|--------|----------- |
|createAt | 创建时间   |date-time  |    |
|createName | 创建人名称   |string  |    |
|createUser | 创建人ID   |int64  |    |
|cusBirthday | 客户出生年月   |date-time  |    |
|cusGender | 客户性别（1-男；2-女)   |int32  |    |
|cusHeight | 身高   |int32  |    |
|cusName | 客户名称   |string  |    |
|cusStatus | 状态(1-正常;2-删除)   |int64  |    |
|cusWeight | 体重   |int32  |    |
|deptId | 部门   |int64  |    |
|id | ID   |int64  |    |

**响应状态码说明**:


| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |ResultModel«客户信息»|
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 获取客户信息列表


**接口说明**:



**接口地址**:`/mayer/customer/get/{page}/lst`


**请求方式**：`GET`


**consumes**:``


**produces**:`["*/*"]`



**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|deviceCode| 设备号  | header | true |string  |    |
|page| 页码（从1开始）  | path | true |string  |    |
|userId| 用户ID  | header | true |string  |    |

**响应数据**:

```json
{
	"code": 0,
	"currTime": 0,
	"data": [
		{
			"createAt": "",
			"createName": "",
			"createUser": 0,
			"cusBirthday": "",
			"cusGender": 0,
			"cusHeight": 0,
			"cusName": "",
			"cusStatus": 0,
			"cusWeight": 0,
			"deptId": 0,
			"id": 0
		}
	],
	"hasNext": true,
	"msg": ""
}
```

**响应参数说明**:


| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code|   |int32  |    |
|currTime|   |int64  |    |
|data|   |array  | 客户信息   |
|hasNext|   |boolean  |    |
|msg|   |string  |    |



**schema属性说明**




**客户信息**

| 参数名称         |  说明          |   类型  |  schema |
| ------------ | ------------------|--------|----------- |
|createAt | 创建时间   |date-time  |    |
|createName | 创建人名称   |string  |    |
|createUser | 创建人ID   |int64  |    |
|cusBirthday | 客户出生年月   |date-time  |    |
|cusGender | 客户性别（1-男；2-女)   |int32  |    |
|cusHeight | 身高   |int32  |    |
|cusName | 客户名称   |string  |    |
|cusStatus | 状态(1-正常;2-删除)   |int64  |    |
|cusWeight | 体重   |int32  |    |
|deptId | 部门   |int64  |    |
|id | ID   |int64  |    |

**响应状态码说明**:


| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |ResultModel«List«客户信息»»|
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 新建客户


**接口说明**:



**接口地址**:`/mayer/customer/put/customer`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["*/*"]`



**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|createAt| 创建时间  | query | false |string  |    |
|createName| 创建人名称  | query | false |string  |    |
|createUser| 创建人ID  | query | false |integer  |    |
|cusBirthday| 客户出生年月  | query | true |string  |    |
|cusGender| 客户性别（1-男；2-女)  | query | true |integer  |    |
|cusHeight| 身高  | query | true |integer  |    |
|cusName| 客户名称  | query | true |string  |    |
|cusStatus| 状态(1-正常;2-删除)  | query | false |integer  |    |
|cusWeight| 体重  | query | true |integer  |    |
|deptId| 部门  | query | false |integer  |    |
|deviceCode| 设备号  | header | true |string  |    |
|id| ID  | query | false |integer  |    |
|userId| 用户ID  | header | true |string  |    |

**响应数据**:

```json
{
	"code": 0,
	"currTime": 0,
	"data": {},
	"hasNext": true,
	"msg": ""
}
```

**响应参数说明**:


| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code|   |int32  |    |
|currTime|   |int64  |    |
|data|   |object  |    |
|hasNext|   |boolean  |    |
|msg|   |string  |    |





**响应状态码说明**:


| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |ResultModel|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 修改客户信息


**接口说明**:



**接口地址**:`/mayer/customer/update/customer`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["*/*"]`



**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|createAt| 创建时间  | query | false |string  |    |
|createName| 创建人名称  | query | false |string  |    |
|createUser| 创建人ID  | query | false |integer  |    |
|cusBirthday| 客户出生年月  | query | true |string  |    |
|cusGender| 客户性别（1-男；2-女)  | query | true |integer  |    |
|cusHeight| 身高  | query | true |integer  |    |
|cusName| 客户名称  | query | true |string  |    |
|cusStatus| 状态(1-正常;2-删除)  | query | false |integer  |    |
|cusWeight| 体重  | query | true |integer  |    |
|deptId| 部门  | query | false |integer  |    |
|deviceCode| 设备号  | header | true |string  |    |
|id| ID  | query | false |integer  |    |
|userId| 用户ID  | header | true |string  |    |

**响应数据**:

```json
{
	"code": 0,
	"currTime": 0,
	"data": {},
	"hasNext": true,
	"msg": ""
}
```

**响应参数说明**:


| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code|   |int32  |    |
|currTime|   |int64  |    |
|data|   |object  |    |
|hasNext|   |boolean  |    |
|msg|   |string  |    |





**响应状态码说明**:


| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |ResultModel|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
# 4.设备信息管理

## 删除设备信息


**接口说明**:



**接口地址**:`/mayer/device/delete/device`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["*/*"]`



**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|deviceCode| 设备号  | header | true |string  |    |
|deviceId| deviceId  | query | false |integer  |    |
|userId| 用户ID  | header | true |string  |    |

**响应数据**:

```json
{
	"code": 0,
	"currTime": 0,
	"data": {},
	"hasNext": true,
	"msg": ""
}
```

**响应参数说明**:


| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code|   |int32  |    |
|currTime|   |int64  |    |
|data|   |object  |    |
|hasNext|   |boolean  |    |
|msg|   |string  |    |





**响应状态码说明**:


| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |ResultModel|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 获取设备信息


**接口说明**:



**接口地址**:`/mayer/device/get/{id}/one`


**请求方式**：`GET`


**consumes**:``


**produces**:`["*/*"]`



**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|deviceCode| 设备号  | header | true |string  |    |
|id| 项目ID  | path | true |string  |    |
|userId| 用户ID  | header | true |string  |    |

**响应数据**:

```json
{
	"code": 0,
	"currTime": 0,
	"data": {
		"addr": "",
		"createAt": "",
		"createName": "",
		"createUser": 0,
		"deptId": 0,
		"deviceNum": "",
		"id": 0,
		"linkman": "",
		"maStatus": 0,
		"name": "",
		"tel": ""
	},
	"hasNext": true,
	"msg": ""
}
```

**响应参数说明**:


| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code|   |int32  |    |
|currTime|   |int64  |    |
|data|   |设备信息  | 设备信息   |
|hasNext|   |boolean  |    |
|msg|   |string  |    |



**schema属性说明**




**设备信息**

| 参数名称         |  说明          |   类型  |  schema |
| ------------ | ------------------|--------|----------- |
|addr | 地址   |string  |    |
|createAt | 创建时间   |date-time  |    |
|createName | 创建人名称   |string  |    |
|createUser | 创建人ID   |int64  |    |
|deptId | 部门   |int64  |    |
|deviceNum | 设备编号   |string  |    |
|id | ID   |int64  |    |
|linkman | 联系人   |string  |    |
|maStatus | 状态(1-正常;2-删除)   |int64  |    |
|name | 服务网点   |string  |    |
|tel | 联系电话   |string  |    |

**响应状态码说明**:


| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |ResultModel«设备信息»|
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 获取设备信息列表


**接口说明**:



**接口地址**:`/mayer/device/get/{page}/lst`


**请求方式**：`GET`


**consumes**:``


**produces**:`["*/*"]`



**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|deviceCode| 设备号  | header | true |string  |    |
|page| 页码（从1开始）  | path | true |string  |    |
|userId| 用户ID  | header | true |string  |    |

**响应数据**:

```json
{
	"code": 0,
	"currTime": 0,
	"data": [
		{
			"addr": "",
			"createAt": "",
			"createName": "",
			"createUser": 0,
			"deptId": 0,
			"deviceNum": "",
			"id": 0,
			"linkman": "",
			"maStatus": 0,
			"name": "",
			"tel": ""
		}
	],
	"hasNext": true,
	"msg": ""
}
```

**响应参数说明**:


| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code|   |int32  |    |
|currTime|   |int64  |    |
|data|   |array  | 设备信息   |
|hasNext|   |boolean  |    |
|msg|   |string  |    |



**schema属性说明**




**设备信息**

| 参数名称         |  说明          |   类型  |  schema |
| ------------ | ------------------|--------|----------- |
|addr | 地址   |string  |    |
|createAt | 创建时间   |date-time  |    |
|createName | 创建人名称   |string  |    |
|createUser | 创建人ID   |int64  |    |
|deptId | 部门   |int64  |    |
|deviceNum | 设备编号   |string  |    |
|id | ID   |int64  |    |
|linkman | 联系人   |string  |    |
|maStatus | 状态(1-正常;2-删除)   |int64  |    |
|name | 服务网点   |string  |    |
|tel | 联系电话   |string  |    |

**响应状态码说明**:


| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |ResultModel«List«设备信息»»|
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 新建设备


**接口说明**:



**接口地址**:`/mayer/device/put/device`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["*/*"]`



**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|addr| 地址  | query | true |string  |    |
|createAt| 创建时间  | query | false |string  |    |
|createName| 创建人名称  | query | false |string  |    |
|createUser| 创建人ID  | query | false |integer  |    |
|deptId| 部门  | query | false |integer  |    |
|deviceCode| 设备号  | header | true |string  |    |
|deviceNum| 设备编号  | query | true |string  |    |
|id| ID  | query | false |integer  |    |
|linkman| 联系人  | query | true |string  |    |
|maStatus| 状态(1-正常;2-删除)  | query | false |integer  |    |
|name| 服务网点  | query | true |string  |    |
|tel| 联系电话  | query | true |string  |    |
|userId| 用户ID  | header | true |string  |    |

**响应数据**:

```json
{
	"code": 0,
	"currTime": 0,
	"data": {},
	"hasNext": true,
	"msg": ""
}
```

**响应参数说明**:


| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code|   |int32  |    |
|currTime|   |int64  |    |
|data|   |object  |    |
|hasNext|   |boolean  |    |
|msg|   |string  |    |





**响应状态码说明**:


| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |ResultModel|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 修改设备信息


**接口说明**:



**接口地址**:`/mayer/device/update/device`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["*/*"]`



**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|addr| 地址  | query | true |string  |    |
|createAt| 创建时间  | query | false |string  |    |
|createName| 创建人名称  | query | false |string  |    |
|createUser| 创建人ID  | query | false |integer  |    |
|deptId| 部门  | query | false |integer  |    |
|deviceCode| 设备号  | header | true |string  |    |
|deviceNum| 设备编号  | query | true |string  |    |
|id| ID  | query | false |integer  |    |
|linkman| 联系人  | query | true |string  |    |
|maStatus| 状态(1-正常;2-删除)  | query | false |integer  |    |
|name| 服务网点  | query | true |string  |    |
|tel| 联系电话  | query | true |string  |    |
|userId| 用户ID  | header | true |string  |    |

**响应数据**:

```json
{
	"code": 0,
	"currTime": 0,
	"data": {},
	"hasNext": true,
	"msg": ""
}
```

**响应参数说明**:


| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code|   |int32  |    |
|currTime|   |int64  |    |
|data|   |object  |    |
|hasNext|   |boolean  |    |
|msg|   |string  |    |





**响应状态码说明**:


| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |ResultModel|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
