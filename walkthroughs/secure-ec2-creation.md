# Walk-through: Secure EC2 Creation

1. Launch instance
   1. Amazon Linux 2
   2. t2.micro
   3. **In order to use SSM we need to create an IAM role.**
   4. Add IAM role `AmazonSSMRoleForInstancesQuickSetup`.
   5. Example user data:
   
       ```bash
       #!/bin/bash
       sudo su
       yum install httpd -y
       echo "<html><body><h1><span style="color:#FFB570">Hello from EC2 web instance with SSM agent #1</span></h1><p>This server acts as an Apache nginx server</p></body></html>" > /var/www/html/index.html
       echo "<html><body><h1><span style="color:#FFB570">Serving web interactions from EC2 web instance with SSM agent #1</span></h1><p>This server acts as an Apache nginx server</p></body></html>" > /var/www/html/application.html
       service httpd start
       ```
   6. Add storage `gp2`
   7. Disable SSH access (this will give a warning saying that you won't be able to connect over SSH).
   8. Open port `80` as well be opening a web server here.
2. _Any need for a Key Pair?_
3. Use the _Connect_ button and 
   