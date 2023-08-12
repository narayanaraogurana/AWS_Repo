
IAM:  to authentic and autorize the service which is called as identity access management.

* We have 2 ways to access AWS.
   1. programatic access   -> Cli and SDk (Eclipse and vscode like)
   2. console access       -> Browser
Authentication in IAM : to login to system we need authentication needed.
======================

* Manage users and their access
   * You can create  and manage users and their security such as access key , passwords and multifactor authentication.
* Manage fedarated users and their access. (Fedaration is nothing but checking trusted third party identity)
   * Using fedaration  you can use single sign-on to access the aws resources using the corporate directory.
* Aws supports security Assertion markup language(SAML) as non-SAML options such as AWS directory  service for Microsfot Active Directory to exchange identity and security information between and identiry provider and an application.

Authorization:
===============

* In AWS authorization is mainly done by IAM policies, these policies are written in json, where we define permissions.
* AWS has built in IAM policies which we can use for standard usecases, for any custom scenario we can create our own IAM Policies.
* IAM Policies can be attached to any IAM entity (user, group or role)
 
IAM Entities:
=============
* In AWS have 3 IAM entities    
    * user  : This is a user, trying to access from console or programatically
    * Group : Group is collection of users so that you can manage permissions at group level rather then individual user level
    * Role  : A Role represent an AWS Resource for example Ec2 resource trying to access S3 bucket. one reources to another resources need to connect we need IAM Role for this. 

Understanding how IAM works:
==========================   
  * IAM resources: user, group, role, policy, identify provider
  * IAM Identities:  user or group or role
  * IAM entity: IAM user or roles
  * Principal:A principal is authenticated aws account root user or IAM entity to make request to aws

IAM Policy structure:
=====================
* in AWS any resources if we want to create resource we need ARN(amazon resource name)

{
  "Version" : "2012-10-17",
  "Statement" : [
    {
      "Effect" : "Deny",
      "Action" : [
        "s3:Get*",
        "s3:List*"
      ],
      "Resources": "*"
    }
  ]
}

* How to get access on AWS resources: 
======================================
* In aws when we create any resource will have ARN(Amazon resource name)
Refere notes [https://directdevops.blog/2021/09/16/aws-classroom-series-16-sept-2021/]


  