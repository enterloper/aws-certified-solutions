# AWS Command Line CLI Lab

commands used:
* `aws s3 ls` - allows us to see the buckets in S3.
* `aws configure` - configure aws credentials (well need credentials.csv file or respective information)
* `aws s3 help` - provides all the commands available in the s3 portion of the CLI
* `cd ~` takes you to home/root directory, from here you can enter `ls -a` to view all the directories and you'll see the `.aws` directory.
You can enter the directory with `cd .aws` and view the contents of the .aws directory once inside with `ls`.
Inside you'll see **config** and **credentials** directories, if you entered `nano credentials` you'd be able to see your **aws_access_key_id** and **aws_secret_access_key**.
* `aws ec2 describe-instances` - describes all the instances running in EC2 as well as terminated instances.
* `aws ec2 terminate-instances --instance-ids i-000a21ed7bf552e4b`