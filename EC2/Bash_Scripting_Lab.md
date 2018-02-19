# Bash Scripting Lab
Using the bash_scripting_lab.html in this same directory,
    
    #!/bin/bash
    yum update -y
    yum install httpd -y
    service httpd start
    chkconfig httpd on
    aws s3 cp s3://my-bash-scripting-lab-bucket/bash_scripting_lab.html /var/www/html --region us-east-1
   
