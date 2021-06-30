# DescribeStoreConfig

查询门店配置信息

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cloudesl&api=DescribeStoreConfig&type=RPC&version=2020-02-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeStoreConfig|系统规定参数。取值：DescribeStoreConfig。 |
|StoreId|String|是|s-dxsxx\*\*\*\*|门店ID或商家自定义门店ID。 |

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
|StoreConfigInfo|Struct| |门店配置信息列表。 |
|EnableNotification|Boolean|true|是否启用钉钉异常消息通知。 |
|NotificationSilentTimes|String|\[\{"from":960,"to":1320\},\{"from":1170,"to":1230\}\]|用户配置的静默期，不发通知消息，JSON列表，单位为分钟，每个JSON字段表示一个静默期时间段，里面的值为UTC时间下一天里面的分钟数，from为静默期的起始分钟数，to为结束分钟数。 |
|NotificationWebHook|String|https://oapi.dingtalk.com/robot/send?.|钉钉消息的webHook地址。 |
|StoreId|String|s-dxsxx\*\*\*\*|门店ID。 |
|Success|Boolean|true|请求状态标识。 |

## 示例

请求示例

```
http(s)://cloudesl.cn-hangzhou.aliyuncs.com/?Action=DescribeStoreConfig
&StoreId=s-dxsxx****
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<code>200</code>
<data>
    <RequestId>CE715689-3EBA-422C-B3E7-76D98B7D0AE8</RequestId>
    <StoreConfigInfo>
        <StoreId>s-cc3nq****</StoreId>
        <EnableNotification>true</EnableNotification>
    </StoreConfigInfo>
    <Success>true</Success>
</data>
<requestId>CE715689-3EBA-422C-B3E7-76D98B7D0AE8</requestId>
<successResponse>true</successResponse>
```

`JSON`格式

```
{
    "code": 200,
    "data": {
        "RequestId": "CE715689-3EBA-422C-B3E7-76D98B7D0AE8",
        "StoreConfigInfo": {
            "StoreId": "s-cc3nq****",
            "EnableNotification": true
        },
        "Success": true
    },
    "requestId": "CE715689-3EBA-422C-B3E7-76D98B7D0AE8",
    "successResponse": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/cloudesl)查看更多错误码。

