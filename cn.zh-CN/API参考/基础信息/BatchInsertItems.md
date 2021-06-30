# BatchInsertItems

调用BatchInsertItems批量新增或修改商品

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cloudesl&api=BatchInsertItems&type=RPC&version=2020-02-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|BatchInsertItems|系统规定参数。取值：BatchInsertItems。 |
|StoreId|String|是|s-dxsxx\*\*\*\*|门店ID或商家自定义门店ID，一次最多插入100条数据。 |
|ItemInfo.N.ItemBarCode|String|是|690560583\*\*\*\*|商品条码，字符不区分大小写，最长64； |
|ItemInfo.N.ItemId|String|是|1234567|自定义商品条码，只允许输入构成整数的阿拉伯数字。 |
|ItemInfo.N.ItemTitle|String|是|光明儿童星|商品全称，最长100字符； |
|ItemInfo.N.ActionPrice|Integer|是|500|实际销售价格\(单位:分\)。 |
|ItemInfo.N.PriceUnit|String|是|箱|计价单位，最长64个字符； |
|SyncByItemId|Boolean|否|true|默认值为false，如果配置为true则商品信息会更新门店下其它ItemId字段相同的商品信息；如果一次商品列表中包含多个ItemId相同的商品，则以排在最后那个内容做更新； |
|ExtraParams|String|否|\{\}|系统扩展字段，请忽略； |
|ItemInfo.N.SkuId|String|否|1234567|商品ID\(SKU\)，最长64个字符； |
|ItemInfo.N.ItemShortTitle|String|否|牛奶|商品简称，不输入则从商品全称中截取，最长64字符； |
|ItemInfo.N.BrandName|String|否|光明乳业|品牌名称，最长64字符； |
|ItemInfo.N.ModelNumber|String|否|330|型号，最长64个字符； |
|ItemInfo.N.Material|String|否|新鲜牛奶|材质，最长64个字符； |
|ItemInfo.N.CategoryName|String|否|饮料|品类，最长64个字符； |
|ItemInfo.N.ProductionPlace|String|否|中国|产地，最长64个字符； |
|ItemInfo.N.EnergyEfficiency|String|否|2焦/毫升|能效，最长64个字符； |
|ItemInfo.N.Rank|String|否|1级|等级，最长32个字符； |
|ItemInfo.N.SaleSpec|String|否|330毫升|规格，最长64个字符； |
|ItemInfo.N.Manufacturer|String|否|中国制造|生产商，最长128个字符； |
|ItemInfo.N.ItemQrCode|String|否|http://m.taobao.com/xxx.html|商品二维码地址，最长1024个字符； |
|ItemInfo.N.SupplierName|String|否|天猫超市|经销商，最长128个字符； |
|ItemInfo.N.ForestFirstId|String|否|食品|一类商品类目ID，最长32个字符； |
|ItemInfo.N.ForestSecondId|String|否|饮料|二类商品类目ID，最长32个字符； |
|ItemInfo.N.SalesPrice|Integer|否|1000|销售价格\(单位:分\)。 |
|ItemInfo.N.OriginalPrice|Integer|否|1000|原价\(单位:分\)。 |
|ItemInfo.N.TaxFee|String|否|增值税|税费信息，最长32个字符； |
|ItemInfo.N.BePromotion|Boolean|否|true|是否匹配促销模板显示，默认值为false； |
|ItemInfo.N.PromotionReason|String|否|儿童节活动|促销原因，最长64个字符； |
|ItemInfo.N.PromotionStart|String|否|2020-02-10T00:00:00Z|促销开始时间 UTC格式 "yyyy-MM-dd'T'HH:mm:ss'Z'"。 |
|ItemInfo.N.PromotionEnd|String|否|2020-02-01T00:00:00Z|促销结束时间 UTC格式 "yyyy-MM-dd'T'HH:mm:ss'Z'"。 |
|ItemInfo.N.PromotionText|String|否|买一送一|促销文案，最长64个字符； |
|ItemInfo.N.SuggestPrice|Integer|否|600|建议零售价\(单位:分\)。 |
|ItemInfo.N.BeSourceCode|Boolean|否|true|是否匹配溯源模板显示，默认值为false； |
|ItemInfo.N.SourceCode|String|否|1234567|溯源码，最长128个字符； |
|ItemInfo.N.InventoryStatus|String|否|OUT\_OF\_STOCK|是否匹配缺货模板显示，可选值：

 -   `OUT_OF_STOCK`：缺货
-   `NORMAL`：正常。

 默认值NORMAL，如果配置为OUT\_OF\_STOCK则会配置缺货模板进行显示 |
|ItemInfo.N.BeMember|Boolean|否|true|是否匹配会员模板显示，默认值为false； |
|ItemInfo.N.MemberPrice|Integer|否|800|会员价\(单位:分\)。 |
|ItemInfo.N.ItemPicUrl|String|否|http://m.taobao.com/xxx.html|商品图片URL，最长128个字符； |
|ItemInfo.N.TemplateSceneId|String|否|23452|客户自定义模板ID，如果有输入有效字符则匹配客户自定义模板进行商品展示，默认值为空字符“”； |
|ItemInfo.N.ItemInfoIndex|Integer|否|1|商品信息坐标，此字段不用填。 |
|ItemInfo.N.CustomizeFeatureA|String|否|自定义属性A|自定义属性A，最长64个字符； |
|ItemInfo.N.CustomizeFeatureB|String|否|自定义属性B|自定义属性B，最长64个字符； |
|ItemInfo.N.CustomizeFeatureC|String|否|自定义属性C|自定义属性C，最长64个字符； |
|ItemInfo.N.CustomizeFeatureD|String|否|自定义属性D|自定义属性D，最长64个字符； |
|ItemInfo.N.CustomizeFeatureE|String|否|自定义属性E|自定义属性E，最长64个字符； |
|ItemInfo.N.CustomizeFeatureF|String|否|自定义属性F|自定义属性F，最长64个字符； |
|ItemInfo.N.CustomizeFeatureG|String|否|自定义属性G|自定义属性G，最长64个字符； |
|ItemInfo.N.CustomizeFeatureH|String|否|自定义属性H|自定义属性H，最长64个字符； |
|ItemInfo.N.CustomizeFeatureI|String|否|自定义属性I|自定义属性I，最长64个字符； |
|ItemInfo.N.CustomizeFeatureJ|String|否|自定义属性J|自定义属性J，最长64个字符； |
|ItemInfo.N.CustomizeFeatureK|String|否|自定义属性K|自定义属性K，最长128个字符； |
|ItemInfo.N.CustomizeFeatureL|String|否|自定义属性L|自定义属性L，最长128个字符； |
|ItemInfo.N.CustomizeFeatureM|String|否|自定义属性M|自定义属性M，最长128个字符； |
|ItemInfo.N.CustomizeFeatureN|String|否|自定义属性N|自定义属性N，最长128个字符； |
|ItemInfo.N.CustomizeFeatureO|String|否|自定义属性O|自定义属性O，最长128个字符； |

商品信息的下列字段会用于匹配模板显示，优先级从高到低

1.

-   TemplateSceneId：尝试匹配客户自定义模板；

    2.

-   InventoryStatus：尝试匹配缺货模板；

    3.

-   BeMember：尝试匹配会员模板；

    4.

-   BeSourceCode：尝试匹配溯源模板；

    5.

-   BePromotion：尝试匹配促销模板；

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|BatchResults|Array of BatchResult| |批量返回结果。 |
|ErrorCode|String|MandatoryParameters|错误码。 |
|Index|Integer|1|请求序列下标。 |
|Message|String|success|消息。 |
|Success|Boolean|true|当前商品插入成功与否标识。 |
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
http(s)://cloudesl.cn-hangzhou.aliyuncs.com/?Action=BatchInsertItems
&ItemInfo.1.ActionPrice=500
&ItemInfo.1.ItemBarCode=690560583****
&ItemInfo.1.ItemId=1234567
&ItemInfo.1.ItemTitle=Apple iPhone 12 Pro
&ItemInfo.1.PriceUnit=台
&StoreId=s-dxsxx****
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<code>200</code>
<data>
    <RequestId>8D4EC562-FA78-4423-AA28-9A5AA6BDEE10</RequestId>
    <BatchResults>
        <Index>1</Index>
        <Success>true</Success>
    </BatchResults>
    <Success>true</Success>
</data>
<requestId>8D4EC562-FA78-4423-AA28-9A5AA6BDEE10</requestId>
<successResponse>true</successResponse>
```

`JSON`格式

```
{
    "code": 200,
    "data": {
        "RequestId": "8D4EC562-FA78-4423-AA28-9A5AA6BDEE10",
        "BatchResults": {
            "Index": 1,
            "Success": true
        },
        "Success": true
    },
    "requestId": "8D4EC562-FA78-4423-AA28-9A5AA6BDEE10",
    "successResponse": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/cloudesl)查看更多错误码。

