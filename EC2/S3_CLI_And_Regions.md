aws s3 cp --recursive s3://example-bucket /home/ec2-user --region us-west-2

It's a good practice to use the region flag to ensure that you're focusing on the proper bucket.