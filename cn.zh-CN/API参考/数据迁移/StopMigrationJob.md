# StopMigrationJob

调用StopMigrationJob接口结束处于迁移状态的数据迁移任务。

**说明：** 调用本接口结束数据迁移任务后，该任务的状态将转变为已完成，且无法通过调用[StartMigrationJob](~49429~)接口重启该任务。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Dts&api=StopMigrationJob&type=RPC&version=2020-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|StopMigrationJob|系统规定参数，取值：**StopMigrationJob**。 |
|MigrationJobId|String|是|dtsb2c11sxpi3j\*\*\*\*|数据迁移实例ID，可以通过调用**DescribeMigrationJobs**接口查询。 |
|RegionId|String|否|cn-hangzhou|地域ID，传入本参数来指定实例所在地域，详情请参见[支持的地域列表](~141033~)。 |
|ClientToken|String|否|0c593ea1-3bea-11e9-b96b-88e9fe63\*\*\*\*|保证请求幂等性。从您的客户端生成一个参数值，确保不同请求间该参数值唯一。**ClientToken**只支持ASCII字符，且不能超过64个字符。 |
|AccountId|String|否|12323344\*\*\*\*|阿里云主账号ID，无需设置，该参数即将下线。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|ErrCode|String|InternalError|调用出错时返回的错误码。 |
|ErrMessage|String|The request processing has failed due to some unknown error.|调用错误时返回对应的错误信息。 |
|RequestId|String|C306C198-7807-409D-930A-D6CE6C32\*\*\*\*|请求ID。 |
|Success|String|true|请求是否成功。 |

## 示例

请求示例

```
http(s)://dts.aliyuncs.com/?Action=StopMigrationJob
&MigrationJobId=dtsb2c11sxpi3j****
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<StopMigrationJobResponse>
      <RequestId>C306C198-7807-409D-930A-D6CE6C32****</RequestId>
      <Success>true</Success>
</StopMigrationJobResponse>
```

`JSON` 格式

```
{
	"RequestId": "C306C198-7807-409D-930A-D6CE6C32****",
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Dts)查看更多错误码。

