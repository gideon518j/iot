# UpdateRule {#reference_szx_zjd_xdb .reference}

You can call this operation to modify the specified rule.

## Request parameters {#section_yrn_rx1_ydb .section}

|Name|Type|Required|Description|
|:---|:---|:-------|:----------|
|Action|String|Yes|The operation that you want to perform. Set the value to: UpdateRule.|
|RuleId|Long|Yes|The rule ID that you want to modify.|
|Name|String|Yes|The rule name. The rule name must meet the following requirements: consists of 4-30 characters, including Chinese characters \(Each Chinese character counts as two characters\), English letters, numbers, and underscores \(\_\).|
|ProductKey|String|No|The identifier of the product that uses this rule.|
|ShortTopic|String|No| The specific topic to which the rule is applied, and the format is: `${deviceName}/ topicShortName` Where `${deviceName}` specifies the name of the specific device, and `topicShortName` specifies the topic level customized for the specified device.

 You can call the QueryDevice operation to view all the devices under the product. The result contains all the devices with the name matching the value of DeviceName. 

 You can call the QueryProductTopic operation to view all the topic categories under the product. The result contains all the topics with the name matching the value of TopicShortName.

 |
|Select|String|No| The SQL SELECT statement that you want to execute. For more information, see the SQL expressions.

 **Note:** Set the parameters following the Select keyword. For example, if the Select statement is `Select a,b,c`, set the parameters to the strings `a,b,c`.

 |
|RuleDesc|String|No|The descriptions of the rule.|
|Where|String|No| The trigger of the rule. For more information, see the SQL expressions.

 **Note:** Set it to the strings after Where. For example, if the Where clause is `Where a>10`, set it to `a>10`.

 |

## Response parameters {#section_qrf_gy1_ydb .section}

|Name|Type|Description |
|:---|:---|:-----------|
|RequestId|String|The GUID generated by Alibaba Cloud for the request.|
|Success|Boolean|Indicates whether the call is successful. A value of true indicates that the call is successful. A value of false indicates that the call has failed.|
|ErrorMessage|String|The error message returned when the operation call fails.|

## Examples {#section_p4w_ky1_ydb .section}

**Request example**

**Note:** For your easy understanding of the format of the parameter values, in the following example, the special characters in parameter values are not encoded. However, when you call the API in practice, the special characters must be encoded.

```
https://iot.cn-shanghai.aliyuncs.com/?Action=UpdateRule
&RuleId=1000
&Name=test_2
&ProductKey=al*********
&ShortTopic=+/get
&Select=a,b,c
&RuleDesc=test
&Where=a>10
&<common request parameters>
```

**Response example**

```
{
    "RequestId":"9A2F243E-17FE-4846-BAB5-D02A25155AC4",
    "Success":true
}
```

