# GetUser

查询单个用户信息

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cloudesl&api=GetUser&type=RPC&version=2020-02-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|GetUser|系统规定参数。取值：GetUser。 |
|UserId|String|否|1344\*\*\*|阿里云子账号UID。 |
|ExtraParams|String|否|\{\}|系统保留字段，请忽略； |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|-1001|内部错误码。 |
|DynamicCode|String|PlatformResponseError.%s|动态错误码。 |
|DynamicMessage|String|The specified store %s does not exist.|动态消息。 |
|ErrorCode|String|MandatoryParameters|错误码。 |
|ErrorMessage|String|The specified resource type is invalid.|错误消息。 |
|Message|String|success|消息。 |
|RequestId|String|E69C8998-1787-4999-8C75-D663FF1173CF|请求ID。 |
|Success|Boolean|true|请求成功与否标识。 |
|User|Struct| |用户信息。 |
|Bid|String|26842|账号类型；

 26842：阿里云 |
|DingTalkInfos|Array of DingTalkInfo| |钉钉账号信息 |
|DingTalkCompanyId|String|131242|钉钉商家ID |
|DingTalkUserId|String|34352525|钉钉用户ID； |
|OwnerId|String|12143124132|阿里云主账号 |
|Stores|String|\[s-dxsxxxxxx,s-dxsyyyyyyy\]|门店ID列表。 |
|UserId|String|1344\*\*\*|阿里云子账号UID。 |
|UserName|String|张三|用户姓名。 |
|UserType|String|USER\_TYPE\_COMPANY\_OWNER|用户类型，可选值：

 -   `USER_TYPE_COMPANY_OWNER`：商家主账号
-   `USER_TYPE_COMPANY_ROOT`：高级商家管理员
-   `USER_TYPE_COMPANY_ADMIN`：商家管理员
-   `USER_TYPE_STORE_ADMIN`：门店管理员
-   `USER_TYPE_STORE_OPERATOR`：门店操作员
-   `USER_TYPE_GUEST`：没有任何权限的访客。 |

## 示例

请求示例

```
http(s)://cloudesl.cn-hangzhou.aliyuncs.com/?Action=GetUser
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<code>200</code>
<data>
    <User>
        <UserId>10634757</UserId>
        <UserType>USER_TYPE_COMPANY_OWNER</UserType>
    </User>
    <RequestId>D8E9737F-7EFC-4E65-A2BB-3B10E8C89964</RequestId>
    <Success>true</Success>
</data>
<requestId>D8E9737F-7EFC-4E65-A2BB-3B10E8C89964</requestId>
<successResponse>true</successResponse>
```

`JSON`格式

```
{
    "code": 200,
    "data": {
        "User": {
            "UserId": 123456,
            "UserType": "USER_TYPE_COMPANY_OWNER"
        },
        "RequestId": "D8E9737F-7EFC-4E65-A2BB-3B10E8C89964",
        "Success": true
    },
    "requestId": "D8E9737F-7EFC-4E65-A2BB-3B10E8C89964",
    "successResponse": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/cloudesl)查看更多错误码。

