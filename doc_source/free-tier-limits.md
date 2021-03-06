# Free Tier Limits<a name="free-tier-limits"></a>

All services that offer a Free Tier have limits on what you can use without being charged\. Many services have multiple types of limits\. For example, Amazon EC2 has limits on both the type of instance you can use and how many hours you can use in one month\. Amazon S3 has a limit on how much storage you can use and on how often you can call certain operations each month\. For example, the Free Tier covers the first 20,000 times you retrieve a file from Amazon S3, but you're charged for additional file retrievals\. Each service has limits that are unique to that service\.

Some of the most common limits are by time, such as hourly or by the minute, or by requests, which are the requests you send to the service, also known as API operations\. For more information about Free Tier limits, see [AWS Free Tier](http://aws.amazon.com/free/)\.

**Topics**
+ [Hourly Usage in the Free Tier](#hourly-limits)
+ [Amazon Machine Images](#ami-limits)

## Hourly Usage in the Free Tier<a name="hourly-limits"></a>

Some services, such as Amazon EC2, Amazon RDS, and Elastic Load Balancing, charge for usage on an hourly basis\. The Free Tier for these services provides you with a monthly allotment of hours for the first 12 months\. For example, the Free Tier for Amazon EC2 provides you with 750 hours usage of Linux \(any combination of `t2.micro` and `t1.micro` instances\), plus 750 hours usage of Windows \(any combination of `t2.micro` and `t1.micro` instances\)\. How you divide this allotment is up to you\. For example, you can use one Linux instance continuously for a month, or 10 Linux instances for 75 hours a month\.

In some cases, leaving your resources running maximizes your Free Tier benefits\. For example, if you run an Amazon EC2 instance for only a portion of an hour, AWS counts that as an entire hour\. Therefore, if you stop and start an Amazon EC2 instance three times in a single hour, you use up three hours of your monthly allotment\. The following diagram illustrates how this works\. Both the red and green usage scenarios use up three hours of your monthly allotment\.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/)![\[Image NOT FOUND\]](http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/)![\[Image NOT FOUND\]](http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/)

**Note**  
Several services measure usage in seconds\. See each service page's details to see how your service is measured and billed\.

For more information, see [Amazon EC2 Pricing](https://aws.amazon.com/ec2/pricing/)\.

## Amazon Machine Images<a name="ami-limits"></a>

When you start an Amazon EC2 instance, you must select an Amazon Machine Image \(AMI\) that is eligible for the Free Tier\. Because of licensing restrictions, some AMIs aren't eligible for the Free Tier\.

**Important**  
Third\-party applications or services from AWS Marketplace aren't eligible for the Free Tier\.

AMIs that are eligible for the Free Tier are marked in the Amazon EC2 Launch Wizard as **Free tier eligible**\. The Free Tier allotment for Linux and Microsoft Windows instances is counted separately\. You can run 750 hours of a Linux `t2.micro` or `t1.micro` instance plus 750 hours of a Windows `t2.micro` or `t1.micro` instance each month for the first 12 months\.

For more information, see [Amazon EC2 Pricing](https://aws.amazon.com/ec2/pricing/)\.