# Identity Access Management

Essentially, IAM allows you to manage users and their level of access to the AWS Console.
It is important to understand IAM and it works, both for the exam and for administrating a company's AWS account in real life.

### What does IAM give you?
* Centralised control of your AWS account
* Shared Access to your AWS account
* Granular Permissions
* Identity Federation (including Active Directory, Facebook, LinkedIn, etc)
* Multifactor Authentication
* Provide temporary access for users/devices and services where necessary
* Allows you to set up your own password rotation policy
* Integrates with many different AWS services
* Supports PCI DSS Compliance

### Critical Terms
* Users - End Users (think people)
* Groups - A collection of users under one set of permissions.
* Roles - You create roles and can then assign them to AWS resources
* Policies - A document that defines one (or more permissions)

IAM is not region specific, it is global (in the since of the world).

#### Security Status - 5 goals for IAM
* Delete your root access keys
* Activate MFA (Multi-Factor Authentication) on your root account
    * enable
* Create individual IAM users
* Use groups to assign permissions
* Apply an IAM password policy

### Recap
* IAm consists of the following:
    * Users
    * Groups (A way to group our users and apply policies to them collectively)
    * Roles
    * Policy Documents - can be applied to users groups roles, made up of JSON.
    
* IAM  is universal.
* IAM does not apply to regions at this time.
* The "root acount" is simply the account created when first setup your AWS account.
* "root acount" has complete access.
* New Users have NO permissions when first created.
    * New Users are assigned Access Key ID & Secret Access Keys when first created.
    * These are not the same as a password, and you cannot use the Access key ID & Secret Access Key to Login to the console.
    * You can use this to access AWS via the APIs and Command line however.
    * You only get tot view these once. If you lose them, you have to regenerate them.
* Always setup Multifactor Authentication on your root account.
* You can create and customise your own password rotation policies.