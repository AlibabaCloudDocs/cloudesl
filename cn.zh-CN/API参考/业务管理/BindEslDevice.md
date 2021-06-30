# BindEslDevice

绑定价签设备

该接口分为陈列模式和普通模式两种。陈列模式是用陈列货位和价签条码进行绑定，普通模式是用商品条码和价签条码进行绑定。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cloudesl&api=BindEslDevice&type=RPC&version=2020-02-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|BindEslDevice|系统规定参数。取值：BindEslDevice。 |
|StoreId|String|是|s-dxsxx\*\*\*\*|门店ID或商家自定义门店ID。 |
|EslBarCode|String|是|18bc5a63\*\*\*\*|价签条码。 |
|ItemBarCode|String|否|690560583\*\*\*\*|商品条码。 |
|Shelf|String|否|20200201|陈列系统中的货架号。 |
|Layer|Integer|否|1|陈列系统中的层号。 |
|Column|String|否|1|陈列系统中的逻辑列。 |

普通绑定模式下，StoreId+EslBarCode+ItemBarCode必填；

陈列绑定模式下，StoreId+EslBarCode+Shelf+Layer+Column必填，ItemBarCode如果填写要和陈列货位上的信息保存一致。

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
http(s)://cloudesl.cn-hangzhou.aliyuncs.com/?Action=BindEslDevice
&EslBarCode=18bc5a63****
&StoreId=s-dxsxx****
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

