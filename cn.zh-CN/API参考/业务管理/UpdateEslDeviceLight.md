# UpdateEslDeviceLight

操作带Led灯的价签

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cloudesl&api=UpdateEslDeviceLight&type=RPC&version=2020-02-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|UpdateEslDeviceLight|系统规定参数。取值：UpdateEslDeviceLight。 |
|StoreId|String|是|s-dxsxx\*\*\*\*|门店ID或商家自定义门店ID。 |
|LedColor|String|是|GREEN|亮灯颜色，可选值：

 -   `GREEN`：绿色
-   `RED`：红色
-   `BLUE`：蓝色
-   `OFF`：关闭。 |
|LightUpTime|Integer|是|30|亮灯时长，单位：s。 |
|Frequency|String|是|NORMAL|亮灯频率，可选值：

 -   `ALWAYS`：持续亮灯
-   `HEIGHT`：高频率亮灯
-   `MIDDLE`：中频率亮灯
-   `NORMAL`：正常频率亮灯。 |
|EslBarCode|String|否|18bc5a631ak9|价签条码。 |
|ItemBarCode|String|否|6905605836648|商品条码。 |

ItemBarCode和EslBarCode二选一，两个都填时EslBarCode优先级比较高。

只填EslBarCode时，点亮单个价签。

只填ItemBarCode时，点亮该价签条码绑定的所以把价签。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|-1001|内部错误码。 |
|DynamicCode|String|PlatformResponseError.%s|动态错误码。 |
|DynamicMessage|String|The specified store %s does not exist.|动态消息。 |
|ErrorCode|String|MandatoryParameters|错误码。 |
|ErrorMessage|String|The specified resource type is invalid.|错误消息。 |
|FailCount|Integer|0|失败数量。 |
|LightFailEslInfos|Array of LightFailEslInfo| |失败价签信息列表。 |
|ErrorMessage|String|The specified ESL device does not exist.|错误消息。 |
|EslBarCode|String|18bc5a63\*\*\*\*|价签条码 |
|Message|String|success|消息。 |
|RequestId|String|E69C8998-1787-4999-8C75-D663FF1173CF|POP请求ID。 |
|Success|Boolean|true|POP请求成功与否标识。 |
|SuccessCount|Integer|1|成功数量。 |

使用EslBarCode点亮时，返回成功或失败；

使用ItemBarCode点亮时，返回成功数量和失败数量，以及失败的价签信息。

## 示例

请求示例

```
http(s)://cloudesl.cn-hangzhou.aliyuncs.com/?Action=UpdateEslDeviceLight
&Frequency=NORMAL
&LedColor=GREEN
&LightUpTime=30
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

