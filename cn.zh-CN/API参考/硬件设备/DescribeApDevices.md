# DescribeApDevices

查询基站设备信息

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cloudesl&api=DescribeApDevices&type=RPC&version=2020-02-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeApDevices|系统规定参数。取值：DescribeApDevices。 |
|StoreId|String|是|s-dxsxx\*\*\*\*|门店ID或商家自定义门店ID。 |
|ApMac|String|否|112233445566|基站设备的Mac地址。 |
|Status|Boolean|否|true|设备在线或离线状态。 |
|BeActivate|Boolean|否|false|设备的激活状态。 |
|Model|String|否|aliyun|设备型号。 |
|PageNumber|Integer|否|1|分页参数：当前页码，默认值1。 |
|PageSize|Integer|否|10|分页参数：每页显示条数，默认值10。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|ApDevices|Array of ApInfo| |基站设备列表。 |
|BeActivate|Boolean|true|是否激活。 |
|Mac|String|112233445566|设备的mac地址。 |
|Model|String|aliyun|设备型号。 |
|Remark|String|测试数据|备注。 |
|Status|Boolean|false|在线状态：离线。 |
|StoreId|String|s-cxsds\*\*\*\*|门店ID。 |
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

## 示例

请求示例

```
http(s)://cloudesl.cn-hangzhou.aliyuncs.com/?Action=DescribeApDevices
&StoreId=s-dxsxx****
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<code>200</code>
<data>
    <TotalCount>2</TotalCount>
    <PageSize>10</PageSize>
    <RequestId>E210B842-6AD3-4420-833A-4ED8756DBFD0</RequestId>
    <PageNumber>1</PageNumber>
    <ApDevices>
        <Status>true</Status>
        <BeActivate>true</BeActivate>
        <StoreId>s-xsaa****</StoreId>
        <Mac>112233445566</Mac>
    </ApDevices>
    <ApDevices>
        <Status>true</Status>
        <BeActivate>true</BeActivate>
        <StoreId>s-xsaa****</StoreId>
        <Mac>141FBA86****</Mac>
    </ApDevices>
    <Success>true</Success>
</data>
<requestId>E210B842-6AD3-4420-833A-4ED8756DBFD0</requestId>
<successResponse>true</successResponse>
```

`JSON`格式

```
{
    "code": 200,
    "data": {
        "TotalCount": 2,
        "PageSize": 10,
        "RequestId": "E210B842-6AD3-4420-833A-4ED8756DBFD0",
        "PageNumber": 1,
        "ApDevices": [
            {
                "Status": true,
                "BeActivate": true,
                "StoreId": "s-xsaa****",
                "Mac": 112233445566
            },
            {
                "Status": true,
                "BeActivate": true,
                "StoreId": "s-xsaa****",
                "Mac": "141FBA86****"
            }
        ],
        "Success": true
    },
    "requestId": "E210B842-6AD3-4420-833A-4ED8756DBFD0",
    "successResponse": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/cloudesl)查看更多错误码。

