# DescribeUsers

查询用户信息

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cloudesl&api=DescribeUsers&type=RPC&version=2020-02-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeUsers|系统规定参数。取值：DescribeUsers。 |
|UserId|String|否|1344\*\*\*|阿里云子账号UID。 |
|UserType|String|否|USER\_TYPE\_COMPANY\_OWNER|用户类型，可选值：

 -   `USER_TYPE_COMPANY_OWNER`：商家主账号
-   `USER_TYPE_COMPANY_ROOT`：高级商家管理员
-   `USER_TYPE_COMPANY_ADMIN`：商家管理员
-   `USER_TYPE_STORE_ADMIN`：门店管理员
-   `USER_TYPE_STORE_OPERATOR`：门店操作员
-   `USER_TYPE_GUEST`：没有任何权限的访客。 |
|UserName|String|否|张三|用户姓名。 |
|PageNumber|Integer|否|1|分页参数：当前页码，默认值1。 |
|PageSize|Integer|否|10|分页参数：每页显示条数，默认值10。 |
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
|PageNumber|Integer|1|分页参数：当前页码。 |
|PageSize|Integer|10|分页参数：每页显示条数。 |
|RequestId|String|E69C8998-1787-4999-8C75-D663FF1173CF|请求ID。 |
|Success|Boolean|true|请求成功与否标识。 |
|TotalCount|Integer|100|总条数。 |
|Users|Array of UserInfo| |用户信息列表。 |
|Bid|String|26842|账号类型；

 26842：阿里云 |
|DingTalkInfos|Array of DingTalkInfo| |钉钉账号信息 |
|DingTalkCompanyId|String|13124|钉钉商家ID |
|DingTalkUserId|String|3455566|钉钉用户ID |
|OwnerId|String|1212124434535|阿里云主账号； |
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
http(s)://cloudesl.cn-hangzhou.aliyuncs.com/?Action=DescribeUsers
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<requestId>D2B9B967-7879-46BA-AA29-9ED91D37C1AD</requestId>
<code>200</code>
<message/>
<action/>
<apiName/>
<extendedCode/>
<data>
    <TotalCount>2</TotalCount>
    <RequestId>D2B9B967-7879-46BA-AA29-9ED91D37C1AD</RequestId>
    <PageSize>10</PageSize>
    <PageNumber>1</PageNumber>
    <Users>
        <UserName>android</UserName>
        <UserId>123456</UserId>
        <UserType>USER_TYPE_STORE_OPERATOR</UserType>
    </Users>
    <Users>
        <UserId>654321</UserId>
        <UserType>USER_TYPE_COMPANY_OWNER</UserType>
    </Users>
    <Success>true</Success>
</data>
<successResponse>true</successResponse>
```

`JSON`格式

```
{
    "requestId": "D2B9B967-7879-46BA-AA29-9ED91D37C1AD",
    "code": 200,
    "message": "",
    "action": "",
    "apiName": "",
    "extendedCode": "",
    "data": {
        "TotalCount": 2,
        "RequestId": "D2B9B967-7879-46BA-AA29-9ED91D37C1AD",
        "PageSize": 10,
        "PageNumber": 1,
        "Users": [
            {
                "UserName": "android",
                "UserId": 123456,
                "UserType": "USER_TYPE_STORE_OPERATOR"
            },
            {
                "UserId": 654321,
                "UserType": "USER_TYPE_COMPANY_OWNER"
            }
        ],
        "Success": true
    },
    "successResponse": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/cloudesl)查看更多错误码。

