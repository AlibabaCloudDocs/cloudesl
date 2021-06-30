# DescribeBinders

查询商品和价签的绑定信息

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cloudesl&api=DescribeBinders&type=RPC&version=2020-02-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeBinders|系统规定参数。取值：DescribeBinders。 |
|StoreId|String|是|s-dxsxx\*\*\*\*|门店ID或商家自定义门店ID。 |
|EslBarCode|String|否|18bc5a63\*\*\*\*|价签条码。 |
|ItemBarCode|String|否|690560583\*\*\*|商品条码。 |
|ItemTitle|String|否|iPhone|商品名称。 |
|PageNumber|Integer|否|1|分页参数：当前页码，默认值1。 |
|PageSize|Integer|否|10|分页参数：每页显示条数，默认值10。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|-1001|内部错误码。 |
|DynamicCode|String|PlatformResponseError.%s|动态错误码。 |
|DynamicMessage|String|The specified store %s does not exist.|动态消息。 |
|ErrorCode|String|MandatoryParameters|错误码。 |
|ErrorMessage|String|The specified resource type is invalid.|错误消息。 |
|EslItemBindInfos|Array of EslItemBindInfo| |绑定信息列表。 |
|ActionPrice|String|500|实际销售价格\(单位:分\)。 |
|BePromotion|Boolean|true|是否促销。 |
|BindId|String|1234|绑定ID。 |
|EslBarCode|String|18bc5a63\*\*\*\*|价签条码。 |
|EslConnectAp|String|11:22:33:44:55:66|价签链接基站Mac。 |
|EslModel|String|AESL0213|价签型号。 |
|EslPic|String|kUzlfuzgayDo5uTXW3D66Q|价签显示图片，请使用Base64解码工具解码成图片。 |
|EslStatus|String|ESL\_STATUS\_ONLINE|价签状态，返回值对应关系：

 -   `ESL_STATUS_ONLINE`：在线，已绑定
-   `ESL_STATUS_OFFLINE`：离线，已绑定
-   `ESL_STATUS_UNBIND`：未绑定。 |
|GmtModified|String|2020-03-16T03:43:05Z|更新时间。 |
|ItemBarCode|String|690560583\*\*\*\*|商品条码。 |
|ItemId|String|1234567|自定义商品条码。 |
|ItemShortTitle|String|牛奶|商品短标题。 |
|ItemTitle|String|纯牛奶|商品标题。 |
|OriginalPrice|String|500|原价\(单位:分\)。 |
|PriceUnit|String|台|计价单位。 |
|PromotionEnd|String|2020-03-17T07:05:34Z|促销开始时间。 |
|PromotionStart|String|2020-03-16T07:05:34Z|促销结束时间。 |
|PromotionText|String|买一送一|促销文案。 |
|SkuId|String|124|SkuID。 |
|StoreId|String|s-dxsxx\*\*\*\*|门店ID。 |
|TemplateId|String|123456|模板编号。 |
|TemplateSceneId|String|123456|模板情景code码。 |
|Message|String|success|消息。 |
|PageNumber|Integer|1|分页参数：当前页码。 |
|PageSize|Integer|10|分页参数：每页显示条数。 |
|RequestId|String|E69C8998-1787-4999-8C75-D663FF1173CF|请求ID。 |
|Success|Boolean|true|请求成功与否标识。 |
|TotalCount|Integer|100|总条数。 |

## 示例

请求示例

```
http(s)://cloudesl.cn-hangzhou.aliyuncs.com/?Action=DescribeBinders
&StoreId=s-dxsxx****
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<code>200</code>
<data>
    <TotalCount>3</TotalCount>
    <PageSize>10</PageSize>
    <RequestId>ED5FF37F-7BDE-4D77-B4FE-FA46D3A78F33</RequestId>
    <PageNumber>1</PageNumber>
    <Success>true</Success>
    <EslItemBindInfos>
        <BindId>123456</BindId>
        <OriginalPrice>2600</OriginalPrice>
        <GmtModified>2020-03-16T07:05:34Z</GmtModified>
        <ActionPrice>1688</ActionPrice>
        <EslPic>iVBORw0KAAAElFTkSuQmCC</EslPic>
        <ItemBarCode>123456</ItemBarCode>
        <BindStatus>0</BindStatus>
        <ItemId>123456</ItemId>
        <PromotionText/>
        <EslModel>null</EslModel>
        <EslBarCode>18bc5a63****</EslBarCode>
        <PriceUnit>盒</PriceUnit>
        <ItemShortTitle>常规商品</ItemShortTitle>
        <StoreId>s-ph5agd****</StoreId>
        <ItemTitle>常规商品</ItemTitle>
        <EslStatus>0</EslStatus>
        <TemplateId>null</TemplateId>
        <EslConnectAp>14:1F:BA:86:**:**</EslConnectAp>
    </EslItemBindInfos>
    <EslItemBindInfos>
        <BindId>123456</BindId>
        <OriginalPrice>100</OriginalPrice>
        <GmtModified>2020-03-16T03:43:05Z</GmtModified>
        <ActionPrice>999</ActionPrice>
        <EslPic>iVBOR6/gM4PnpubddQljAwYUVV89WwoofM2EBR24PBj/KJPUBnRGhVAsr9XlOlZ/I6V0HDtwkPK+n4uXP9N4oTUIAucZUZm6C/GdoBj95s1ugx6rgEzm968CRhFXUTCt63Ho5YamwAE3CEUFk5rZzlxDAIs6aPg4rVXMZhwUAEwTtTwCAsACAsAAQFgAQFgAQFgDCAgDCAgDCAkBYAEBYAFDD/wFX2SqYKGouSwAAAABJRU5ErkJggg==</EslPic>
        <ItemBarCode>123456</ItemBarCode>
        <BindStatus>0</BindStatus>
        <ItemId>13453</ItemId>
        <PromotionText>促销价</PromotionText>
        <EslModel>null</EslModel>
        <EslBarCode>18bc5a7a****</EslBarCode>
        <PriceUnit>瓶</PriceUnit>
        <ItemShortTitle>44</ItemShortTitle>
        <StoreId>s-ph5agd****</StoreId>
        <ItemTitle>促销缺货商品</ItemTitle>
        <EslStatus>1</EslStatus>
        <TemplateId>123456</TemplateId>
        <EslConnectAp>14:1F:BA:86:**:**</EslConnectAp>
    </EslItemBindInfos>
    <EslItemBindInfos>
        <BindId>123456</BindId>
        <OriginalPrice>200</OriginalPrice>
        <GmtModified>2020-03-05T14:44:59Z</GmtModified>
        <ActionPrice>150</ActionPrice>
        <EslPic>iVBORw0KD2A7f1WwIdufYq4Begu/QM2RGnVDoqKMQAAAABJRU5ErkJggg==</EslPic>
        <ItemBarCode>123456</ItemBarCode>
        <BindStatus>0</BindStatus>
        <ItemId>123456</ItemId>
        <PromotionText/>
        <EslModel>null</EslModel>
        <EslBarCode>18bc5a7e****</EslBarCode>
        <PriceUnit>瓶</PriceUnit>
        <ItemShortTitle>缺货商品</ItemShortTitle>
        <StoreId>s-ph5agd****</StoreId>
        <ItemTitle>缺货商品</ItemTitle>
        <EslStatus>1</EslStatus>
        <TemplateId>123456</TemplateId>
        <EslConnectAp>null</EslConnectAp>
    </EslItemBindInfos>
</data>
<requestId>ED5FF37F-7BDE-4D77-B4FE-FA46D3A78F33</requestId>
<successResponse>true</successResponse>
```

`JSON`格式

```
{
    "code": 200,
    "data": {
        "TotalCount": 3,
        "PageSize": 10,
        "RequestId": "ED5FF37F-7BDE-4D77-B4FE-FA46D3A78F33",
        "PageNumber": 1,
        "Success": true,
        "EslItemBindInfos": [
            {
                "BindId": 123456,
                "OriginalPrice": 2600,
                "GmtModified": "2020-03-16T07:05:34Z",
                "ActionPrice": 1688,
                "EslPic": "iVBORw0KAAAElFTkSuQmCC",
                "ItemBarCode": 123456,
                "BindStatus": 0,
                "ItemId": 123456,
                "PromotionText": "",
                "EslModel": "null",
                "EslBarCode": "18bc5a63****",
                "PriceUnit": "盒",
                "ItemShortTitle": "常规商品",
                "StoreId": "s-ph5agd****",
                "ItemTitle": "常规商品",
                "EslStatus": 0,
                "TemplateId": "null",
                "EslConnectAp": "14:1F:BA:86:**:**"
            },
            {
                "BindId": 123456,
                "OriginalPrice": 100,
                "GmtModified": "2020-03-16T03:43:05Z",
                "ActionPrice": 999,
                "EslPic": "iVBOR6/gM4PnpubddQljAwYUVV89WwoofM2EBR24PBj/KJPUBnRGhVAsr9XlOlZ/I6V0HDtwkPK+n4uXP9N4oTUIAucZUZm6C/GdoBj95s1ugx6rgEzm968CRhFXUTCt63Ho5YamwAE3CEUFk5rZzlxDAIs6aPg4rVXMZhwUAEwTtTwCAsACAsAAQFgAQFgAQFgDCAgDCAgDCAkBYAEBYAFDD/wFX2SqYKGouSwAAAABJRU5ErkJggg==",
                "ItemBarCode": 123456,
                "BindStatus": 0,
                "ItemId": 13453,
                "PromotionText": "促销价",
                "EslModel": "null",
                "EslBarCode": "18bc5a7a****",
                "PriceUnit": "瓶",
                "ItemShortTitle": 44,
                "StoreId": "s-ph5agd****",
                "ItemTitle": "促销缺货商品",
                "EslStatus": 1,
                "TemplateId": 123456,
                "EslConnectAp": "14:1F:BA:86:**:**"
            },
            {
                "BindId": 123456,
                "OriginalPrice": 200,
                "GmtModified": "2020-03-05T14:44:59Z",
                "ActionPrice": 150,
                "EslPic": "iVBORw0KD2A7f1WwIdufYq4Begu/QM2RGnVDoqKMQAAAABJRU5ErkJggg==",
                "ItemBarCode": 123456,
                "BindStatus": 0,
                "ItemId": 123456,
                "PromotionText": "",
                "EslModel": "null",
                "EslBarCode": "18bc5a7e****",
                "PriceUnit": "瓶",
                "ItemShortTitle": "缺货商品",
                "StoreId": "s-ph5agd****",
                "ItemTitle": "缺货商品",
                "EslStatus": 1,
                "TemplateId": 123456,
                "EslConnectAp": "null"
            }
        ]
    },
    "requestId": "ED5FF37F-7BDE-4D77-B4FE-FA46D3A78F33",
    "successResponse": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/cloudesl)查看更多错误码。

