# TagResources

调用TagResources接口为一个或多个迁移、同步和订阅实例绑定标签。

在实例数量较多的情况下，您可以创建多个标签，为实例绑定不同的标签对其进行分类，之后通过标签进行实例筛选。

-   标签由一对键（key）值（value）组成，键在同账号同地域下唯一，值无此限制。
-   若设置的标签不存在，则自动创建该标签并绑定到目标实例。
-   若实例已经绑定了有相同键的标签，则进行覆盖绑定。
-   每个实例最多可以绑定20个标签。
-   每次调用最多设置50个实例进行批量标签绑定。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Dts&api=TagResources&type=RPC&version=2020-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|TagResources|系统规定参数，取值：**TagResources**。 |
|RegionId|String|是|cn-hangzhou|地域ID，传入本参数来指定实例所在地域，详情请参见[支持的地域列表](~141033~)。 |
|ResourceId.N|RepeatList|是|dtsntk10k6r12v\*\*\*\*|数据迁移、同步和订阅的实例ID，可以通过调用**DescribeMigrationJobs**、**DescribeSynchronizationJobs**、**DescribeSubscriptionInstances**接口查询。

 **说明：** N表示传入第几个实例ID。例如ResourceId.1表示传入第一个实例ID；ResourceId.2表示传入第二个实例ID。 |
|ResourceType|String|是|ALIYUN::DTS::INSTANCE|资源类型定义，固定取值为：**ALIYUN::DTS::INSTANCE**。 |
|Tag.N.Key|String|是|testkey1|标签的键。

 **说明：**

-   N表示传入第几个标签的键。例如Tag.1.Key表示传入第一个标签的键；Tag.2.Key表示传入第二个标签的键。
-   不允许传入空字符串。 |
|Tag.N.Value|String|是|testvalue1|标签的值。

 **说明：**

-   N表示传入第几个标签的值。例如Tag.1.Value表示传入第一个标签的值；Tag.2.Value表示传入第二个标签的值。
-   允许传入空字符串。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|ErrCode|String|InternalError|调用出错时返回的错误码。 |
|ErrMessage|String|The request processing has failed due to some unknown error.|调用错误时返回对应的错误信息。 |
|RequestId|String|755D7B84-6813-42B0-BC9D-2699CFEA\*\*\*\*|请求ID。 |
|Success|Boolean|true|请求是否成功。 |

## 示例

请求示例

```
http(s)://dts.aliyuncs.com/?Action=TagResources
&RegionId=cn-hangzhou	
&ResourceId.1=dtsntk10k6r12v****
&ResourceType=ALIYUN::DTS::INSTANCE
&Tag.1.Key=testkey1
&Tag.1.Value=testvalue1
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<TagResourcesResponse>
      <RequestId>755D7B84-6813-42B0-BC9D-2699CFEA****</RequestId>
      <Success>true</Success>
</TagResourcesResponse>
```

`JSON` 格式

```
{
    "RequestId": "755D7B84-6813-42B0-BC9D-2699CFEA****",
    "Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Dts)查看更多错误码。

