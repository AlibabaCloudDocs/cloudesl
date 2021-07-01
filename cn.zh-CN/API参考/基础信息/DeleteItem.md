# DeleteItem

删除门店商品

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cloudesl&api=DeleteItem&type=RPC&version=2020-02-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteItem|系统规定参数。取值：DeleteItem。 |
|StoreId|String|是|s-dxsxx\*\*\*\*|门店ID或商家自定义门店ID; |
|ItemBarCode|String|是|6937372642255|商品条码; |
|UnbindEslDevice|Boolean|否|false|是否解绑该商品已绑定的价签设备，默认值false; |

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

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DeleteItem
&StoreId=s-dxsxx****
&ItemBarCode=6937372642255
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<RequestId>E69C8998-1787-4999-8C75-D663FF1173CF</RequestId>
<Message>success</Message>
<DynamicCode>PlatformResponseError.%s</DynamicCode>
<ErrorCode>MandatoryParameters</ErrorCode>
<DynamicMessage>The specified store %s does not exist.</DynamicMessage>
<ErrorMessage>The specified resource type is invalid.</ErrorMessage>
<Code>-1001</Code>
<Success>true</Success>
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

