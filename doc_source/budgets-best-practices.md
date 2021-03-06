# Best Practices for AWS Budgets<a name="budgets-best-practices"></a>

Note the following best practices when you're working with budgets\.

**Topics**
+ [Best Practices for Controlling Access to AWS Budgets](#budgets-best-practices-access)
+ [Best Practices for Setting Budgets](#budgets-best-practices-setting-budgets)
+ [Best Practices for Using the Advanced Options When Setting Cost Budgets](#budgets-best-practices-cost-budgets)
+ [Understanding the AWS Budgets Update Frequency](#budgets-best-practices-updates)
+ [Best Practices for Setting Budget Alerts](#budgets-best-practices-alerts)
+ [Best Practices for Setting Budgets Alerts Using Amazon SNS Topics](#budgets-best-practices-alerts-sns-topics)

## Best Practices for Controlling Access to AWS Budgets<a name="budgets-best-practices-access"></a>

To allow IAM users to create budgets in the AWS Billing and Cost Management console, you must also allow IAM users to do the following:
+ View your billing information
+ Create Amazon CloudWatch alarms
+ Create Amazon Simple Notification Service \(Amazon SNS\) notifications

To learn more about giving users the ability to create budgets on the AWS Budgets console, see [Example 7: Allow IAM users to create budgets](billing-permissions-ref.md#example-billing-allow-createbudgets)\.

You can also create budgets programmatically using the Budgets API\. When configuring access to the Budgets API, we recommend creating a unique IAM user for allowing programmatic access\. This helps you define more precise access controls between who in your organization has access to the Budgets console and the API\. To give multiple IAM users query access to the Budgets API, we recommend creating a programmatic access IAM role for each of them\.

## Best Practices for Setting Budgets<a name="budgets-best-practices-setting-budgets"></a>

Budgets enables you to set custom budgets based on your costs, usage, reservation utilization, and reservation coverage\.

With Budgets, you can set budgets on a recurring basis or for a specific time frame\. However, we recommend setting your budget on a recurring basis so that you don't unexpectedly stop receiving budget alerts\.

## Best Practices for Using the Advanced Options When Setting Cost Budgets<a name="budgets-best-practices-cost-budgets"></a>

Cost budgets can be aggregated by unblended costs, amortized costs, or blended costs\. Cost budgets can also either include or exclude refunds, credits, upfront reservation fees, recurring reservation charges, non\-reservation subscription costs, taxes, and support charges\.

## Understanding the AWS Budgets Update Frequency<a name="budgets-best-practices-updates"></a>

AWS billing data, which Budgets uses to monitor resources, is updated at least once per day\. Keep in mind that budget information and associated alerts are updated and sent according to this data refresh cadence\.

## Best Practices for Setting Budget Alerts<a name="budgets-best-practices-alerts"></a>

Budget alerts can be sent to up to 10 email addresses and one Amazon SNS topic per alert\. You can set budgets to alert against either actual values or forecasted values\.

Actual alerts are only sent out once per budget, per budget period, when a budget first reached the actual alert threshold\.

Forecast\-based budget alerts are sent out on a per\-budget, per\-budget period basis\. They might alert more than once in a budgeted period if the forecasted values exceed, dip below, and then exceed the alert threshold again during the budgeted period\.

AWS requires approximately 5 weeks of usage data to generate budget forecasts\. If you set a budget to alert based on a forecasted amount, this budget alert isn't triggered until you have enough historical usage information\.

## Best Practices for Setting Budgets Alerts Using Amazon SNS Topics<a name="budgets-best-practices-alerts-sns-topics"></a>

When you create a budget that sends notifications to an Amazon SNS topic, you must either have a preexisting Amazon SNS topic or create an Amazon SNS topic\. Amazon SNS topics enable you to send notifications over SMS in addition to email\.

For budget notifications to be sent successfully, your budget must have permissions to send a notification to your topic, and you must accept the subscription to the Amazon SNS notification topic\. For more information, see [Creating an Amazon SNS Topic for Budget Notifications](budgets-sns-policy.md)\.