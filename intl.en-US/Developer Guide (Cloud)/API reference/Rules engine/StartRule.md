# StartRule {#reference_m1j_yjd_xdb .reference}

You can call this operation to start the specified rule.

## Request parameters {#section_cyy_v51_ydb .section}

**Note:** You need to verify that the rule has SQL expressions configured before you start the rule. To configure SQL expressions, see the [CreateRule](reseller.en-US/Developer Guide (Cloud)/API reference/Rules engine/CreateRule.md#) API.

|Name|Type|Required|Description|
|:---|:---|:-------|:----------|
|Action|String|Yes|The operation that you want to perform. Set the value to: StartRule.|
|RuleId|Long|Yes|The ID for the rule to be triggered.|

## Response parameters {#section_m43_gv1_ydb .section}

|Name|Type|Description|
|:---|:---|:----------|
|RequestId|String|The GUID generated by Alibaba Cloud for the request.|
|Success|Boolean|Indicates whether the call is successful. A value of true indicates that the call is successful. A value of false indicates that the call has failed.|
|ErrorMessage|String|The error message returned when the call fails.|

## Examples {#section_w1j_jw1_ydb .section}

**Request parameters**

```
https://iot.cn-shanghai.aliyuncs.com/?Action=StartRule
&RuleId=1000
&<common request parameters>
```

**Response parameters**

```
{
    "RequestId":"9A2F243E-17FE-4846-BAB5-D02A25155AC4",
    "Success":true
}
```

