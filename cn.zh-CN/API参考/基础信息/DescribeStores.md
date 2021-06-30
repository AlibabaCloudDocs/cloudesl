# DescribeStores

查询门店信息

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cloudesl&api=DescribeStores&type=RPC&version=2020-02-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeStores|系统规定参数。取值：DescribeStores。 |
|StoreId|String|否|s-dxsxx\*\*\*\*|门店ID。 |
|StoreName|String|否|天猫超市|门店名称。 |
|UserStoreCode|String|否|123456|商家自定义门店ID。 |
|FromDate|String|否|2020-03-06T02:58:16Z|门店创建时间：开始时间。 |
|ToDate|String|否|2020-03-08T02:58:16Z|门店创建时间：结束时间。 |
|TemplateVersion|String|否|1.1.0|门店配置的模板版本号； |
|PageNumber|Integer|否|1|分页参数：当前页码，默认值1。 |
|PageSize|Integer|否|10|分页参数：每页显示条数，默认值10。 |
|ExtraParams|String|否|\{\}|系统保留字段，请忽略； |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|-1001|后端错误码。 |
|DynamicCode|String|PlatformResponseError.%s|动态错误码。 |
|DynamicMessage|String|The specified store %s does not exist.|动态消息。 |
|ErrorCode|String|MandatoryParameters|错误码。 |
|ErrorMessage|String|The specified resource type is invalid.|错误消息。 |
|Message|String|success|消息。 |
|PageNumber|Integer|1|分页参数：当前页码。 |
|PageSize|Integer|10|分页参数：每页显示条数。 |
|RequestId|String|E69C8998-1787-4999-8C75-D663FF1173CF|请求ID。 |
|Stores|Array of StoreInfo| |门店信息列表。 |
|GmtCreate|String|2020-03-06T02:58:16Z|创建时间。 |
|GmtModified|String|2020-03-06T02:58:16Z|修改时间。 |
|Level|String|1级|级别。 |
|ParentId|String|s-aasx\*\*\*\*|父门店ID。 |
|Phone|String|0571-5666888|门店所在监督工商局的监督电话。 |
|StoreId|String|s-dxsxx\*\*\*\*|门店ID。 |
|StoreName|String|天猫旗舰店|门店名称。 |
|TemplateVersion|String|1.1.0|门店模板版本号； |
|UserStoreCode|String|20200201|商家自定义门店ID。 |
|Success|Boolean|true|请求成功与否标识。 |
|TotalCount|Integer|100|总条数。 |

## 示例

请求示例

```
http(s)://cloudesl.cn-hangzhou.aliyuncs.com/?Action=DescribeStores
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<code>200</code>
<data>
    <TotalCount>2</TotalCount>
    <PageSize>10</PageSize>
    <RequestId>517B75BE-323F-4963-A4B3-BCF898E54AD6</RequestId>
    <PageNumber>1</PageNumber>
    <Stores>
        <GmtCreate>2020-03-06T02:58:16Z</GmtCreate>
        <StoreName>312</StoreName>
        <StoreId>s-cc3nqi****</StoreId>
        <CompanyId>c-nl0no****</CompanyId>
        <Phone>123456</Phone>
        <GmtModified>2020-03-06T02:58:16Z</GmtModified>
    </Stores>
    <Stores>
        <GmtCreate>2020-03-05T06:02:10Z</GmtCreate>
        <StoreName>11</StoreName>
        <StoreId>s-4sory****</StoreId>
        <CompanyId>c-nl0noz****</CompanyId>
        <Phone>123456</Phone>
        <GmtModified>2020-03-05T06:02:10Z</GmtModified>
    </Stores>
    <Success>true</Success>
</data>
<requestId>517B75BE-323F-4963-A4B3-BCF898E54AD6</requestId>
<successResponse>true</successResponse>
```

`JSON`格式

```
{
    "code": 200,
    "data": {
        "TotalCount": 2,
        "PageSize": 10,
        "RequestId": "517B75BE-323F-4963-A4B3-BCF898E54AD6",
        "PageNumber": 1,
        "Stores": [
            {
                "GmtCreate": "2020-03-06T02:58:16Z",
                "StoreName": 312,
                "StoreId": "s-cc3nqi****",
                "CompanyId": "c-nl0no****",
                "Phone": 123456,
                "GmtModified": "2020-03-06T02:58:16Z"
            },
            {
                "GmtCreate": "2020-03-05T06:02:10Z",
                "StoreName": 11,
                "StoreId": "s-4sory****",
                "CompanyId": "c-nl0noz****",
                "Phone": 123456,
                "GmtModified": "2020-03-05T06:02:10Z"
            }
        ],
        "Success": true
    },
    "requestId": "517B75BE-323F-4963-A4B3-BCF898E54AD6",
    "successResponse": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/cloudesl)查看更多错误码。

