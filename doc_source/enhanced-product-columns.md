# Product Details<a name="enhanced-product-columns"></a>

You can use the product columns to find information about the service and type of line item\. Different services include different product columns in their reports\. Examples include the following:

** product/instanceType**  
If you used Amazon EC2, the type of Amazon EC2 instance is included in the **product/InstanceType** column\.

** product/instanceTypeFamily**  
The instance family that is associated with the given usage: for example, `t2` or `m4`\.

** product/operatingSystem**  
If you used Amazon EC2, the type of operating system of an Amazon EC2 instance is included in the **product/OperatingSystem** column\.

** product/ProductFamily**  
The category for the type of product: for example, `compute` for Amazon EC2 or `storage` for Amazon S3\.

** product/ProductName**  
The full name of the AWS service\.

** product/region**  
 The geographical area that hosts your AWS services: for example, `us-east-1`\. Use this field to analyze spend across a particular region\. 

**product/sku**  
A unique code for a product\. The SKU is created by combining the `ProductCode`, `UsageType`, and `Operation`\. For size\-flexible RIs, the SKU uses the instance that was used\. For example, if you used a `t2.micro` and AWS applied a `t2.small` RI discount to the usage, the line item SKU is created with the `t2.micro`\.

** product/tenancy**  
If you used Amazon EC2, the type of tenancy allowed on the Amazon EC2 instance, such as single tenant or multiple tenant, is included in the **product/Tenancy** column\.