# CreateConsumerGroup

调用CreateConsumerGroup接口为数据订阅实例新增消费组。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Dts&api=CreateConsumerGroup&type=RPC&version=2020-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateConsumerGroup|系统规定参数，取值：**CreateConsumerGroup**。 |
|ConsumerGroupName|String|是|测试订阅组|消费组名称，不超过128个字符。建议配置具有业务意义的名称，便于后续识别。 |
|ConsumerGroupPassword|String|是|Test123456|消费组账号的密码。

 -   由大写字母、小写字母、数字、特殊字符中的任意两种或两种以上组成。
-   密码长度为8~32个字符。 |
|ConsumerGroupUserName|String|是|dtstest|消费组的账号。

 -   由大写字母、小写字母、数字、下划线中的任意一种或多种组成。
-   最长16个字符。 |
|SubscriptionInstanceId|String|是|dtsg2m10r1x15a\*\*\*\*|数据订阅实例ID，可以通过调用**DescribeSubscriptionInstances**接口查询。 |
|RegionId|String|否|cn-hangzhou|地域ID，传入本参数来指定实例所在地域，详情请参见[支持的地域列表](~141033~)。 |
|AccountId|String|否|12323344\*\*\*\*|阿里云主账号ID，无需设置，该参数即将下线。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|ConsumerGroupID|String|dtswc411cg617p\*\*\*\*|消费组ID。 |
|ErrCode|String|InternalError|调用出错时返回的错误码。 |
|ErrMessage|String|The request processing has failed due to some unknown error.|调用出错时返回的错误信息。 |
|RequestId|String|6063641E-BAD1-4BA7-B70B-26FFFD18\*\*\*\*|请求ID。 |
|Success|String|true|请求是否成功。 |

## 示例

请求示例

```
http(s)://dts.aliyuncs.com/?Action=CreateConsumerGroup
&ConsumerGroupName=测试订阅组
&ConsumerGroupPassword=Test123456
&ConsumerGroupUserName=dtstest
&SubscriptionInstanceId=dtsg2m10r1x15a****
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<CreateConsumerGroupResponse>
      <ConsumerGroupID>dtswc411cg617p****</ConsumerGroupID>
      <RequestId>6063641E-BAD1-4BA7-B70B-26FFFD18****</RequestId>
      <Success>true</Success>
</CreateConsumerGroupResponse>
```

`JSON` 格式

```
{
	"ConsumerGroupID": "dtswc411cg617p****",
	"RequestId": "6063641E-BAD1-4BA7-B70B-26FFFD18****",
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Dts)查看更多错误码。

