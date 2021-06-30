# DescribeUserLog

查询操作日志

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cloudesl&api=DescribeUserLog&type=RPC&version=2020-02-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeUserLog|系统规定参数。取值：DescribeUserLog。 |
|StoreId|String|是|s-dxsxx\*\*\*\*|门店ID或商家自定义门店ID。 |
|LogId|String|否|123456|日志ID。 |
|OperationType|String|否|OPERATION\_TYPE\_BIND|日志类型，可选值：

 -   `OPERATION_TYPE_BIND`：价签绑定
-   `OPERATION_TYPE_UNBIND`：价签解绑
-   `OPERATION_TYPE_FORCE_UPDATE`：价签刷新
    -   主动刷新
-   `OPERATION_TYPE_ITEM_CHANGE_UPDATE`：价签刷新
    -   商品更新
-   `OPERATION_TYPE_ALL_UPDATE`：价签刷新
    -   门店级刷新
-   `OPERATION_TYPE_SEND_FAILED_RETRY`：操作重试
    -   发送失败
-   `OPERATION_TYPE_DISPLAY_FAILED_RETRY`：操作重试
    -   显示失败
-   `OPERATION_TYPE_LIGHT_UP_ESL_LED`：价签亮灯。 |
|UserId|String|否|134\*\*\*\*|阿里云子账号UID。 |
|EslBarCode|String|否|18bc5a63\*\*\*\*|价签条码。 |
|ItemBarCode|String|否|690560583\*\*\*\*|商品条码。 |
|ItemShortTitle|String|否|牛奶|商品短标题。 |
|FromDate|String|否|2020-03-18T02:26:28Z|查询操作日志：开始时间。 |
|ToDate|String|否|2020-03-17T02:26:28Z|查询操作日志：结束时间。 |
|OperationStatus|String|否|OPERATION\_STATUS\_NEW|日志状态，可选值：

 -   `OPERATION_STATUS_NEW`：新建
-   `OPERATION_STATUS_SENT`：已发送
-   `OPERATION_STATUS_DISPLAY`：已显示
-   `OPERATION_STATUS_DELETE`：已删除
-   `OPERATION_STATUS_BREAK`：中断
-   `OPERATION_STATUS_DEVICE_RETRY_DISPLAY`：重试中
-   `OPERATION_STATUS_SEND_FAILED`：发送失败
-   `OPERATION_STATUS_DISPLAY_FAILED`：显示失败。 |
|PageNumber|Integer|否|1|分页参数：当前页码，默认值1。 |
|PageSize|Integer|否|10|分页参数：每页显示条数，默认值10。 |
|ExtraParams|String|否|\{\}|系统保留字段，请忽略； |

UserId字段暂时不支持

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
|Success|Boolean|true|POP请求成功与否标识。 |
|TotalCount|Integer|100|总条数。 |
|UserLogs|Array of UserLogInfo| |日志信息列表。 |
|ActionPrice|String|500|实际销售价格\(单位:分\)。 |
|BePromotion|Boolean|false|是否促销。 |
|EslBarCode|String|18bc5a63\*\*\*\*|价签条码。 |
|EslSignal|Integer|50|价签信号强度； |
|GmtCreate|String|2020-03-17T02:26:17Z|创建时间。 |
|GmtModified|String|2020-03-17T02:26:17Z|修改时间。 |
|ItemBarCode|String|690560583\*\*\*\*|商品条码。 |
|ItemId|String|123456|自定义商品条码。 |
|ItemShortTitle|String|牛奶|商品短标题。 |
|LogId|String|123456|日志ID。 |
|OperationResponseTime|String|2020-03-17T02:26:17Z|操作响应时间。 |
|OperationSendTime|String|2020-03-17T02:25:17Z|操作发送时间。 |
|OperationStatus|String|OPERATION\_STATUS\_NEW|日志状态，返回值对应关系：

 -   `OPERATION_STATUS_NEW`：新建操作
-   `OPERATION_STATUS_SENT`：发送操作
-   `OPERATION_STATUS_DISPLAY`：完成操作
-   `OPERATION_STATUS_DELETE`：删除操作
-   `OPERATION_STATUS_DEVICE_RETRY_DISPLAY`：重试操作
-   `OPERATION_STATUS_SEND_FAILED`：发送失败
-   `OPERATION_STATUS_DISPLAY_FAILED`：刷新失败。 |
|OperationType|String|OPERATION\_TYPE\_BIND|日志类型，可选值：

 -   `OPERATION_TYPE_BIND`：价签绑定
-   `OPERATION_TYPE_UNBIND`：价签解绑
-   `OPERATION_TYPE_FORCE_UPDATE`：价签刷新
    -   主动刷新
-   `OPERATION_TYPE_ITEM_CHANGE_UPDATE`：价签刷新
    -   商品更新
-   `OPERATION_TYPE_ALL_UPDATE`：价签刷新
    -   门店级刷新
-   `OPERATION_TYPE_SEND_FAILED_RETRY`：操作重试
    -   发送失败
-   `OPERATION_TYPE_DISPLAY_FAILED_RETRY`：操作重试
    -   显示失败
-   `OPERATION_TYPE_TIMEOUT_RETRY`：操作重试
    -   操作超时
-   `OPERATION_TYPE_ESL_NOT_FOUND_RETRY`：操作重试
    -   未知设备
-   `OPERATION_TYPE_TEMPLATE_NOT_FOUND_RETRY`：操作重试
    -   未知模板
-   `OPERATION_TYPE_DRAW_PICTURE_FAILED_RETRY`：操作重试
-   异常模板
-   `OPERATION_TYPE_BATCH_TIMES_DIRECTIONAL_REFRESH`：价签刷新
    -   商品导入
-   `OPERATION_TYPE_ON_LINE_RETRY`：价签刷新
    -   上线重试
-   `OPERATION_TYPE_LIGHT_UP_ESL_LED`：亮灯。 |
|PriceUnit|String|台|计价单位。 |
|ResultCode|String|2002|执行结果编码。 |
|SpendTime|String|10|耗时\(单位：ms\)。 |
|StoreId|String|s-dxsxxx\*\*\*\*|门店ID。 |
|UserId|String|134\*\*\*\*|阿里云子账号UID。 |

## 示例

请求示例

```
http(s)://cloudesl.cn-hangzhou.aliyuncs.com/?Action=DescribeUserLog
&StoreId=s-dxsxx****
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<code>200</code>
<data>
    <TotalCount>68</TotalCount>
    <PageSize>10</PageSize>
    <RequestId>78DDE5D5-7E14-4BED-92AF-C465C74BCDBF</RequestId>
    <PageNumber>1</PageNumber>
    <Success>true</Success>
    <UserLogs>
        <GmtModified>2020-03-16T06:38:56Z</GmtModified>
        <ActionPrice>999</ActionPrice>
        <OperationSendTime>2020-03-16T06:38:57Z</OperationSendTime>
        <ItemBarCode>123456</ItemBarCode>
        <SpendTime>0</SpendTime>
        <ItemId>123456</ItemId>
        <GmtCreate>2020-03-16T06:38:56Z</GmtCreate>
        <EslBarCode>18bc5a63****</EslBarCode>
        <PriceUnit>个</PriceUnit>
        <ItemShortTitle>促销商品</ItemShortTitle>
        <StoreId>s-ph5agd****</StoreId>
        <OperationStatus>OPERATION_STATUS_SEND_FAILED</OperationStatus>
        <OperationType>OPERATION_TYPE_BIND</OperationType>
        <LogId>123456</LogId>
        <ResultCode>Error00000011|Assemble sending package fail!</ResultCode>
        <BePromotion>true</BePromotion>
    </UserLogs>
    <UserLogs>
        <GmtModified>2020-03-16T06:36:46Z</GmtModified>
        <ActionPrice>1688</ActionPrice>
        <OperationSendTime>2020-03-16T06:36:47Z</OperationSendTime>
        <ItemBarCode>123456</ItemBarCode>
        <SpendTime>0</SpendTime>
        <ItemId>123456</ItemId>
        <GmtCreate>2020-03-16T06:36:46Z</GmtCreate>
        <EslBarCode>18bc5a63****</EslBarCode>
        <PriceUnit>盒</PriceUnit>
        <ItemShortTitle>常规商品</ItemShortTitle>
        <StoreId>s-ph5agd****</StoreId>
        <OperationStatus>OPERATION_STATUS_SEND_FAILED</OperationStatus>
        <OperationType>OPERATION_TYPE_BIND</OperationType>
        <LogId>123456</LogId>
        <ResultCode>Error00000011|Assemble sending package fail!</ResultCode>
        <BePromotion>false</BePromotion>
    </UserLogs>
</data>
<requestId>78DDE5D5-7E14-4BED-92AF-C465C74BCDBF</requestId>
<successResponse>true</successResponse>
```

`JSON`格式

```
{
    "code": 200,
    "data": {
        "TotalCount": 68,
        "PageSize": 10,
        "RequestId": "78DDE5D5-7E14-4BED-92AF-C465C74BCDBF",
        "PageNumber": 1,
        "Success": true,
        "UserLogs": [
            {
                "GmtModified": "2020-03-16T06:38:56Z",
                "ActionPrice": 999,
                "OperationSendTime": "2020-03-16T06:38:57Z",
                "ItemBarCode": 123456,
                "SpendTime": 0,
                "ItemId": 123456,
                "GmtCreate": "2020-03-16T06:38:56Z",
                "EslBarCode": "18bc5a63****",
                "PriceUnit": "个",
                "ItemShortTitle": "促销商品",
                "StoreId": "s-ph5agd****",
                "OperationStatus": "OPERATION_STATUS_SEND_FAILED",
                "OperationType": "OPERATION_TYPE_BIND",
                "LogId": 123456,
                "ResultCode": "Error00000011|Assemble sending package fail!",
                "BePromotion": true
            },
            {
                "GmtModified": "2020-03-16T06:36:46Z",
                "ActionPrice": 1688,
                "OperationSendTime": "2020-03-16T06:36:47Z",
                "ItemBarCode": 123456,
                "SpendTime": 0,
                "ItemId": 123456,
                "GmtCreate": "2020-03-16T06:36:46Z",
                "EslBarCode": "18bc5a63****",
                "PriceUnit": "盒",
                "ItemShortTitle": "常规商品",
                "StoreId": "s-ph5agd****",
                "OperationStatus": "OPERATION_STATUS_SEND_FAILED",
                "OperationType": "OPERATION_TYPE_BIND",
                "LogId": 123456,
                "ResultCode": "Error00000011|Assemble sending package fail!",
                "BePromotion": false
            }
        ]
    },
    "requestId": "78DDE5D5-7E14-4BED-92AF-C465C74BCDBF",
    "successResponse": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/cloudesl)查看更多错误码。

