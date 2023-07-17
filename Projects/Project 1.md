## Documentation for Project 1
# LAMP Stack Implementation (Linux, Apache, MySQL, PHP)

### First, I started by connecting to my EC2 instance using my Ubuntu desktop (LINUX)

I did this by running the code to SSH into my instance using the PEM key I downloaded (for my Windows, what I did was to move the pem key file to the ubuntu user folder)

<img width="677" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/fdbf7e50-f577-4f02-a0fa-8d42fc1a273e">

### Next, I updated my ubuntu package manager and went ahead to install my web server (APACHE2)

To confirm run status and/or accuracy, I ran the code 'sudo systemctl status apache2' and came up with an 'Active (running)' feedback 

<img width="520" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/ecf5db55-d9f2-4ba8-afde-b9d732f8bf2f">

### Next, I edited the inbound rule on my EC2 instance to enable web browser access

<img width="880" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/e94218b2-5d38-490e-9ba4-8d09e913dbc9">

## (Point of note:)

Before editing the inbound rule, I tried accessing the web server from my web browser using it's public IP and got the error screen below;

<img width="479" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/505ca2a1-9b81-41cb-ad61-d76e5be2d8d4">

However, after editing the inbound rule I got a success screen;

![image](https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/1949ce97-fd2d-4a85-ae6c-ed5cb717969c)

### Next, I moved on to install my database server (MYSQL)

Afterwards, I sudo'd into it using the 'sudo mysql' command

<img width="443" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/8079c928-f8e0-4607-9d66-a8fff17777f5">

Then, I set root user passsword using the default authentication method

<img width="504" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/69ebdf5a-d6d6-41a3-986a-824041b62695">

### Next, I run the mysql security script and defined root access and test database rules 

<img width="431" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/1b94ef63-8586-447b-8f56-0779d98c1757">

Then, I tried logging into my msql server using the root user password
### It worked!!!

<img width="437" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/1435e9d4-f721-4e6f-af33-10ea46ffb4f8">

### Next, for the final step of this project, i'll need to install my Scripting Layer (PHP)

### As I have come to learn, in this step, there are 3 installations to make
1). The PHP package itself

2). A PHP-MYSQL package - the php module that allows it to communicate with the mysql-based database

3). LIBAPACHE2-MOD-PHP - to enable my web sever (Apache) to handle PHP files

### Now, to get into it proper; I run the command to install all 3 packages at same time ('sudo apt install php libapache2-mod-php php-mysql')

To check my PHP version, I ran the 'php -v' command

<img width="445" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/0dd2f428-da43-4819-be0c-d9ab398b685c">

### Next, I set up a virtual host to test my setup

After following all the configuration steps and creating an index.html file; I got a feedback screen from my public IP address

<img width="415" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/f09ba74d-5536-4603-8d36-6cc37684ed72">

### Now time to enable PHP on my website to avoid index.html files taking precedence.

After following the configuration steps and creating a PHP file using '<?php
phpinfo();

# ...and BOOM!!!!!! It worked

<img width="504" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/a3134881-2df7-4613-9ab6-a9ced39586ae">

