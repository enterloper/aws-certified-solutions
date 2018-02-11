# Security Group Lab
### What is a Security Group?
A Security Group is a virtual firewall for an instance. It is the first defence against hackers.
One instance can have multiple security groups.

### Lab portion

#### steps for SSH-ing into the AWS instance

* In the terminal, navigate to where you hold your SSH keys for AWS (the file with an extension of .pem)
  Once you are in the directory of the SSH file, enter in the following command to gain access to AWS after changing the ip address and the name of the file:
  
  `ssh ec2-user@55.55.55.550 -i ExamplePemFileName.pem`
  
* You'll be prompted to continue connecting to the EC2 instance, **unless** you tried to to enter the following command above without providing a proper path to the `.pem` file.
* If you don't have super user/root access, you'll need it to install Apache. Do this by entering the following command:

    `sudo su`

* Update the server with `yum update -y` to insure everything is up to date with the most recent patches.
* Install apache with `yum install httpd -y` which will install apache.
* Start the apache server with `service httpd start` 
* To insure the apache server automatically starts everytime we boot our EC2 instance, enter `chkconfig httpd on` 
* Navigate to the `html` directory inside the `www` directory inside `var` directory by entering `cd /var/www/html`
* You can check the contents of the `html` directory using the `ls` command, and if this the first time you've accessed this directory, it should be empty.
* use the following command to open the **nano** text editor and create a file title **index.html** `nano index.html`

## **IMPORTANT** Any rule you make in a security group applies **Immediately**
Security Groups are stateful, that simply means that when you add a rule down here whether it's HTTP, SSH, HTTPS, IDP etc, that rule will be allowed back out.
As soon as you add an inbound rule, outbound rules will be allowed automatically. This is why they are stateful.

### SUMMARY
* All Inbound Traffic is **Blocked By Default** when a security is first created
* All Outbound Traffic is **Allowed**
* Changes to Security Groups take effect immediately
* You can have any number of EC2 instances within a security group.
* You can have multiple security groups attached to EC2 instances.
* Security Groups are **STATEFUL**.
    * If you create an inbound rule allowing traffic in, that traffic is automatically allowed back out again.
* You cannot block specific IP addresses using Security Groups, instead use Network Access Control Lists.
* You can specify allow rules, but not deny rules.
