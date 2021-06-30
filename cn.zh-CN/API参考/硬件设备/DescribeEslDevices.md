# DescribeEslDevices

查询价签设备信息

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cloudesl&api=DescribeEslDevices&type=RPC&version=2020-02-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeEslDevices|系统规定参数。取值：DescribeEslDevices。 |
|StoreId|String|是|s-dxsxx\*\*\*\*|门店ID或商家自定义门店ID。 |
|EslBarCode|String|否|18bc5a63\*\*\*\*|价签条码。 |
|Type|String|否|ESL\_TYPE\_E\_INK|价签类型，可选值：

 -   `ESL_TYPE_E_INK`：电子墨水屏幕
-   `ESL_TYPE_DM_LCD`：段码屏幕
-   `ESL_TYPE_FULL_COLOR`：彩色屏幕。 |
|EslStatus|String|否|ESL\_STATUS\_ONLINE|价签状态，可选值：

 -   `ESL_STATUS_ONLINE`：在线，已绑定
-   `ESL_STATUS_OFFLINE`：离线，已绑定
-   `ESL_STATUS_UNBIND`：未绑定。 |
|FromBatteryLevel|Integer|否|20|电量区间左偏移。 |
|ToBatteryLevel|Integer|否|80|电量区间右偏移。 |
|PageNumber|Integer|否|1|分页参数：当前页码，默认值1。 |
|PageSize|Integer|否|10|分页参数：每页显示条数，默认值10。 |
|ExtraParams|String|否|\{\}|扩展参数 |

根据电量区间查询暂时不支持

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|-1001|内部错误码。 |
|DynamicCode|String|PlatformResponseError.%s|动态错误码。 |
|DynamicMessage|String|The specified store %s does not exist.|动态消息。 |
|ErrorCode|String|MandatoryParameters|错误码。 |
|ErrorMessage|String|The specified resource type is invalid.|错误消息。 |
|EslDevices|Array of EslDeviceInfo| |价签信息列表。 |
|BatteryLevel|Integer|100|电量。 |
|EslBarCode|String|18bc5a63\*\*\*\*|价签条码。 |
|EslSignal|Integer|54|价签信号 |
|EslStatus|String|ESL\_STATUS\_ONLINE|价签状态，返回值对应关系：

 -   `ESL_STATUS_ONLINE`：在线，已绑定
-   `ESL_STATUS_OFFLINE`：离线，已绑定
-   `ESL_STATUS_UNBIND`：未绑定。 |
|LastCommunicateTime|String|2020-03-16T07:04:16Z|最后通讯时间。 |
|Mac|String|18:bc:5a:63:\*\*:\*\*|价签Mac地址。 |
|Model|String|AESL0213|价签型号。 |
|ScreenHeight|Integer|200|屏幕高度。 |
|ScreenWidth|Integer|200|屏幕宽度。 |
|StoreId|String|s-dxsxx\*\*\*\*|门店ID。 |
|Type|String|ESL\_TYPE\_E\_INK|价签类型，返回值对应关系：

 -   `ESL_TYPE_E_INK`：电子墨水屏幕
-   `ESL_TYPE_DM_LCD`：段码屏幕
-   `ESL_TYPE_FULL_COLOR`：彩色屏幕。 |
|Message|String|success|消息。 |
|PageNumber|Integer|1|分页参数：当前页码。 |
|PageSize|Integer|10|分页参数：每页显示条数。 |
|RequestId|String|E69C8998-1787-4999-8C75-D663FF1173CF|请求ID。 |
|Success|Boolean|true|请求成功与否标识。 |
|TotalCount|Integer|100|总条数。 |

## 示例

请求示例

```
http(s)://cloudesl.cn-hangzhou.aliyuncs.com/?Action=DescribeEslDevices
&StoreId=s-dxsxx****
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<code>200</code>
<data>
    <TotalCount>4</TotalCount>
    <PageSize>10</PageSize>
    <RequestId>80B45212-5669-4B27-9B8E-80BDCB18E99C</RequestId>
    <PageNumber>1</PageNumber>
    <EslDevices>
        <EslBarCode>18bc5a63****</EslBarCode>
        <Type>ESL_TYPE_E_INK</Type>
        <BatteryLevel>100</BatteryLevel>
        <StoreId>s-ph5agd****</StoreId>
        <ScreenWidth>320</ScreenWidth>
        <EslStatus>ESL_STATUS_ONLINE</EslStatus>
        <ScreenHeight>240</ScreenHeight>
        <LastCommunicateTime>2020-03-16T07:04:16Z</LastCommunicateTime>
        <Mac>18:bc:5a:63:**:**</Mac>
        <EslSignal>47</EslSignal>
    </EslDevices>
    <EslDevices>
        <EslBarCode>18bc5a7a****</EslBarCode>
        <Type>ESL_TYPE_E_INK</Type>
        <BatteryLevel>100</BatteryLevel>
        <StoreId>s-ph5agd****</StoreId>
        <ScreenWidth>400</ScreenWidth>
        <EslStatus>ESL_STATUS_OFFLINE</EslStatus>
        <ScreenHeight>300</ScreenHeight>
        <LastCommunicateTime>2020-03-14T17:19:57Z</LastCommunicateTime>
        <Mac>18:bc:5a:7a:**:**</Mac>
        <EslSignal>47</EslSignal>
    </EslDevices>
    <Success>true</Success>
</data>
<requestId>80B45212-5669-4B27-9B8E-80BDCB18E99C</requestId>
<successResponse>true</successResponse>
```

`JSON`格式

```
{
    "code": 200,
    "data": {
        "TotalCount": 4,
        "PageSize": 10,
        "RequestId": "80B45212-5669-4B27-9B8E-80BDCB18E99C",
        "PageNumber": 1,
        "EslDevices": [
            {
                "EslBarCode": "18bc5a63****",
                "Type": "ESL_TYPE_E_INK",
                "BatteryLevel": 100,
                "StoreId": "s-ph5agd****",
                "ScreenWidth": 320,
                "EslStatus": "ESL_STATUS_ONLINE",
                "ScreenHeight": 240,
                "LastCommunicateTime": "2020-03-16T07:04:16Z",
                "Mac": "18:bc:5a:63:**:**",
                "EslSignal":47
            },
            {
                "EslBarCode": "18bc5a7a****",
                "Type": "ESL_TYPE_E_INK",
                "BatteryLevel": 100,
                "StoreId": "s-ph5agd****",
                "ScreenWidth": 400,
                "EslStatus": "ESL_STATUS_OFFLINE",
                "ScreenHeight": 300,
                "LastCommunicateTime": "2020-03-14T17:19:57Z",
                "Mac": "18:bc:5a:7a:**:**",
                "EslSignal":47
            }
        ],
        "Success": true
    },
    "requestId": "80B45212-5669-4B27-9B8E-80BDCB18E99C",
    "successResponse": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/cloudesl)查看更多错误码。

