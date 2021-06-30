# DescribeItems

调用DescribeItems查询商品信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cloudesl&api=DescribeItems&type=RPC&version=2020-02-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeItems|系统规定参数。取值：DescribeItems。 |
|StoreId|String|是|s-dxsxx\*\*\*\*|门店ID或商家自定义门店ID。 |
|ItemBarCode|String|否|690560583\*\*\*\*|商品条码。 |
|ItemId|String|否|123456|自定义商品条码。 |
|SkuId|String|否|1234565|SkuID。 |
|ItemTitle|String|否|纯牛奶|商品名称。 |
|BePromotion|Boolean|否|true|是否促销。 |
|PageNumber|Integer|否|1|分页参数：当前页码，默认值1。 |
|PageSize|Integer|否|10|分页参数：每页显示条数，默认值10。 |
|ExtraParams|String|否|\{\}|系统保留字段，请忽略； |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|-1001|内部错误码。 |
|DynamicCode|String|PlatformResponseError.%s|动态错误码。 |
|DynamicMessage|String|The specified store %s does not exist.|动态消息。 |
|ErrorCode|String|MandatoryParameters|错误码。 |
|ErrorMessage|String|The specified resource type is invalid.|错误消息。 |
|Items|Array of ItemInfo| |商品信息列表。 |
|ActionPrice|Integer|500|实际销售价格\(单位:分\)。 |
|BeMember|Boolean|false|是否匹配会员模板显示 |
|BePromotion|Boolean|false|是否促销。 |
|BeSourceCode|Boolean|false|是否溯源。 |
|BrandName|String|阿里巴巴|品牌名称。 |
|CategoryName|String|手机|品类。 |
|CustomizeFeatureA|String|自定义属性A|自定义属性A。 |
|CustomizeFeatureB|String|自定义属性B|自定义属性B。 |
|CustomizeFeatureC|String|自定义属性C|自定义属性C。 |
|CustomizeFeatureD|String|自定义属性D|自定义属性D。 |
|CustomizeFeatureE|String|自定义属性E|自定义属性E。 |
|CustomizeFeatureF|String|自定义属性F|自定义属性F。 |
|CustomizeFeatureG|String|自定义属性G|自定义属性G。 |
|CustomizeFeatureH|String|自定义属性H|自定义属性H。 |
|CustomizeFeatureI|String|自定义属性I|自定义属性I。 |
|CustomizeFeatureJ|String|自定义属性J|自定义属性J。 |
|CustomizeFeatureK|String|自定义属性K|自定义属性K。 |
|CustomizeFeatureL|String|自定义属性L|自定义属性L。 |
|CustomizeFeatureM|String|自定义属性M|自定义属性M。 |
|CustomizeFeatureN|String|自定义属性N|自定义属性N。 |
|CustomizeFeatureO|String|自定义属性O|自定义属性O。 |
|EnergyEfficiency|String|1kw/h|能效。 |
|ForestFirstId|String|酒类|一类商品类目ID。 |
|ForestSecondId|String|白酒|二类商品类目ID。 |
|GmtCreate|String|2020-03-09T00:00:00Z|创建时间。 |
|GmtModified|String|2020-03-09T00:00:00Z|修改时间。 |
|InventoryStatus|String|OUT\_OF\_STOCK|库存状态，返回值对应关系：

 -   `OUT_OF_STOCK`：缺货
-   `NORMAL`：正常。 |
|ItemBarCode|String|69056058\*\*\*\*|商品条码。 |
|ItemId|String|123456|自定义商品条码。 |
|ItemInfoIndex|Integer|1|商品信息坐标，此字段不用用户关注。 |
|ItemPicUrl|String|http://m.taobao.com/xxx.html|商品图片URL。 |
|ItemQrCode|String|http://m.taobao.com/xxx.html|商品二维码地址。 |
|ItemShortTitle|String|牛奶|商品短标题。 |
|ItemTitle|String|纯牛奶|商品名称。 |
|Manufacturer|String|中国制造|生产商。 |
|Material|String|金属|材质。 |
|MemberPrice|Integer|500|会员价。 |
|ModelNumber|String|256G|型号。 |
|OriginalPrice|Integer|500|原价\(单位:分\)。 |
|PriceUnit|String|台|计价单位。 |
|ProductionPlace|String|中国|产地。 |
|PromotionEnd|String|2020-02-11T00:00:00Z|促销结束时间 UTC格式 "yyyy-MM-dd'T'HH:mm:ss'Z'"。 |
|PromotionReason|String|情人节活动|促销原因。 |
|PromotionStart|String|2020-02-10T00:00:00Z|促销开始时间 UTC格式 "yyyy-MM-dd'T'HH:mm:ss'Z'"。 |
|PromotionText|String|买一送一|促销文案。 |
|Rank|String|一级|等级。 |
|SaleSpec|String|1台/盒|规格。 |
|SalesPrice|Integer|500|销售价格。 |
|SkuId|String|123456|SKuID。 |
|SourceCode|String|123456|溯源码。 |
|SuggestPrice|Integer|500|建议零售价\(单位:分\)。 |
|SupplierName|String|天猫超市|经销商。 |
|TaxFee|String|增值税|税费信息。 |
|TemplateSceneId|String|1223|匹配自定义模板ID显示 |
|Message|String|success|消息。 |
|PageNumber|Integer|1|分页参数：当前页码。 |
|PageSize|Integer|10|分页参数：每页显示条数。 |
|RequestId|String|E69C8998-1787-4999-8C75-D663FF1173CF|请求ID。 |
|Success|Boolean|true|请求成功与否标识。 |
|TemplateSceneId|String|11223|自定义模板ID |
|TotalCount|Integer|100|总条数。 |

## 示例

请求示例

```
http(s)://cloudesl.cn-hangzhou.aliyuncs.com/?Action=DescribeItems
&StoreId=s-dxsxx****
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<DescribeItems>
  <code>200</code>
  <data>
        <TotalCount>9</TotalCount>
        <PageSize>10</PageSize>
        <RequestId>EFEB5CB3-A5D7-4EE6-AA9C-586B157C3176</RequestId>
        <PageNumber>1</PageNumber>
        <Items>
              <SaleSpec>1KG</SaleSpec>
              <SourceCode>123456</SourceCode>
              <CompanyId>c-nl0noz****</CompanyId>
              <ActionPrice>888</ActionPrice>
              <Rank>优等</Rank>
              <PromotionStart>2020-03-09T00:00:00Z</PromotionStart>
              <ItemBarCode>123456</ItemBarCode>
              <ItemId>43523452</ItemId>
              <PromotionEnd>2020-03-29T00:00:00Z</PromotionEnd>
              <BrandName>天然</BrandName>
              <InventoryStatus>OUT_OF_STOCK</InventoryStatus>
              <ItemShortTitle>促销溯源缺货商品</ItemShortTitle>
              <PriceUnit>只</PriceUnit>
              <StoreId>s-ph5agd****</StoreId>
              <ItemTitle>促销溯源缺货商品</ItemTitle>
              <BeSourceCode>true</BeSourceCode>
              <ExtraAttribute>null</ExtraAttribute>
              <BePromotion>true</BePromotion>
        </Items>
        <Items>
              <SaleSpec>500mg</SaleSpec>
              <SourceCode>123456</SourceCode>
              <CompanyId>c-nl0noz****</CompanyId>
              <ActionPrice>666</ActionPrice>
              <Rank>优等</Rank>
              <ItemBarCode>123456</ItemBarCode>
              <ItemId>1231244</ItemId>
              <BrandName>编码</BrandName>
              <InventoryStatus>OUT_OF_STOCK</InventoryStatus>
              <ItemShortTitle>溯源缺货商品</ItemShortTitle>
              <PriceUnit>盒</PriceUnit>
              <StoreId>s-ph5agd****</StoreId>
              <ItemTitle>溯源缺货商品</ItemTitle>
              <BeSourceCode>true</BeSourceCode>
              <ExtraAttribute>null</ExtraAttribute>
              <BePromotion>false</BePromotion>
        </Items>
        <Success>true</Success>
  </data>
  <requestId>EFEB5CB3-A5D7-4EE6-AA9C-586B157C3176</requestId>
  <successResponse>true</successResponse>
</DescribeItems>
```

`JSON`格式

```
{
    "code": 200,
    "data": {
        "TotalCount": 9,
        "PageSize": 10,
        "RequestId": "EFEB5CB3-A5D7-4EE6-AA9C-586B157C3176",
        "PageNumber": 1,
        "Items": [
            {
                "SaleSpec": "1KG",
                "SourceCode": 123456,
                "CompanyId": "c-nl0noz****",
                "ActionPrice": 888,
                "Rank": "优等",
                "PromotionStart": "2020-03-09T00:00:00Z",
                "ItemBarCode": 123456,
                "ItemId": 43523452,
                "PromotionEnd": "2020-03-29T00:00:00Z",
                "BrandName": "天然",
                "InventoryStatus": "OUT_OF_STOCK",
                "ItemShortTitle": "促销溯源缺货商品",
                "PriceUnit": "只",
                "StoreId": "s-ph5agd****",
                "ItemTitle": "促销溯源缺货商品",
                "BeSourceCode": true,
                "ExtraAttribute": "null",
                "BePromotion": true
            },
            {
                "SaleSpec": "500mg",
                "SourceCode": 123456,
                "CompanyId": "c-nl0noz****",
                "ActionPrice": 666,
                "Rank": "优等",
                "ItemBarCode": 123456,
                "ItemId": 1231244,
                "BrandName": "编码",
                "InventoryStatus": "OUT_OF_STOCK",
                "ItemShortTitle": "溯源缺货商品",
                "PriceUnit": "盒",
                "StoreId": "s-ph5agd****",
                "ItemTitle": "溯源缺货商品",
                "BeSourceCode": true,
                "ExtraAttribute": "null",
                "BePromotion": false
            }
        ],
        "Success": true
    },
    "requestId": "EFEB5CB3-A5D7-4EE6-AA9C-586B157C3176",
    "successResponse": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/cloudesl)查看更多错误码。

