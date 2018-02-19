
After SSHing into your instance, you can use the following command:

`curl http://169.254.169.254/latest/meta-data/`

to view exposed variables you can use.

For Example `curl http://169.254.169.254/latest/meta-data/public-ipv4` will give us the ip address.
If we enter `curl http://169.254.169.254/latest/meta-data/public-ipv4 > mypublicip.html`,
a file will be created called mypublicip.html. We can then use `ls` to ensure the file is in the directory. 
If we open the file with `nano mypublicip.html` we will see the same ip address! 
With the knowledge gained with the bash lab, we can create more advanced behavior. 
