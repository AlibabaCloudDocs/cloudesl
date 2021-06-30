# CreateStore

创建门店

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cloudesl&api=CreateStore&type=RPC&version=2020-02-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateStore|系统规定参数。取值：CreateStore。 |
|StoreName|String|是|天猫旗舰店|门店名称 |
|Phone|String|是|0571-5666888|门店所在监督工商局的监督电话 |
|UserStoreCode|String|否|20200201|商家自定义门店ID |
|ParentId|String|否|s-dxsxx\*\*\*\*|父门店ID |

ParentId字段，暂时不支持。

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
|StoreId|String|s-dxsxx\*\*\*\*|门店ID。 |
|Success|Boolean|true|请求成功与否标识。 |

## 示例

请求示例

```
http(s)://cloudesl.cn-hangzhou.aliyuncs.com/?Action=CreateStore
&Phone=0571-5666888
&StoreName=天猫旗舰店
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<code>200</code>
<data>
    <RequestId>8F124625-DF0A-4B08-B205-2CF538FAF713</RequestId>
    <Success>true</Success>
</data>
<requestId>8F124625-DF0A-4B08-B205-2CF538FAF713</requestId>
<successResponse>true</successResponse>
```

`JSON`格式

```
{
    "code": 200,
    "data": {
        "RequestId": "8F124625-DF0A-4B08-B205-2CF538FAF713",
        "Success": true
    },
    "requestId": "8F124625-DF0A-4B08-B205-2CF538FAF713",
    "successResponse": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/cloudesl)查看更多错误码。

