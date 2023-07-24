## Documentation for Project 2
# LEMP Stack Implementation (Linux, NGINX, MySQL, PHP)

### It was very exciting!!! finally completing my LAMP installation and understanding the process and principles.
### It's now time to move to LEMP Stack. For this, I will be using NGINX as my web server instead of APACHE2.

### I started by creating a new EC2 instance.
### Note to self:
(Initially, was wondering why I needed to create a new instance; if I could use my previous instance and just install NGINX. During my self-study, I learned that 'yes' it is possible to run both web servers; however, separate ports have to be created for them as both cannot listen on the same port and IP)

### After creating a new EC2 instance, I connected to it using 'GIT Bash'

<img width="558" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/ba17e760-cd63-42fd-a6da-de875bf528aa">

### Then I updated the installation package manager and went ahead to install my web server (NGINX)
After installation, I used the 'systemctl' command I checked the run status

<img width="716" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/7ea3bca9-b3a9-4836-a0ed-c2ff3fbe553a">

### Next, I went into the security inbound rule on my instance to add a port 80 rule (like we did in the previous project). This is to allow public web access to my server
<img width="533" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/379db9b0-9343-4832-945c-23a3246f3920">

### Next, I installed my database management server (MSQL)
After installing MYSQL, tried to see if the 'systemctl status' command will work on it and it did ☺

<img width="613" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/43ef63cc-6ca8-4a1f-a280-236a954bca51">

Then logged in to MYSQL server

<img width="464" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/7bf18395-df6d-42dc-934a-cfcae7c51606">

Changed root user password before secure installation

<img width="520" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/c3f6d6d2-df3a-4898-a039-1d3a4c094529">

### After running the secure installation script and defining my security policies, I tried logging into the mysql server without the '-p' flag . . . . JUST TO SEE WHAT WILL HAPPEN
And I got an access denied error 

<img width="466" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/695a40b4-3015-4ce8-a5b9-d036d4838831">

### Anyways, lesson learned; now moving on!!!

Logged in using the root user password I created

<img width="444" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/0ea707ff-92f0-4d01-8b15-8468058f03e8">

### Now time to install my scripting layer (PHP)

Like the previous project, we also need to make a couple other installations

1). A PHP process manager - to enable NGINX process PHP scripts

2). A PHP-MSQL package - the php module that allows it to communicate with the mysql-based database

As a note to notice, we didn't add the PHP package itself and that's because the above installations will install core PHP packages automatically.

### Ran installation command for both installations 
    sudo apt php-fpm php-mysql
    
<img width="675" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/b869ada8-b218-4325-a3ec-8c9d0b10a45e">

### Next, time to configure the webserver to use the PHP processor installed

### Did this in three steps . . . 
First, created a new web directory so as not to modify the default /html directory 

Second, change the directory permission by assigning ownership to my system user

Third and final, Create a new configuration file in the server's 'available sites' directory

<img width="400" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/715b79cb-7207-477e-af4e-0ac2657009e4">

Then I created an index.html file to be displayed

<img width="467" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/e6407d91-9b8f-4d72-987b-2c0d905b1164">

### Next, time to test my server with a PHP script

<img width="552" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/6b25e8e2-ba64-4cbb-9ddc-60bc3077401f">

### Next, I test my server with a MYSQL database file

First, I created a new database called "lemp_database"

Second, I created a new user called "lemp_user" and then granted them full privileges (asides creating or modifying other databases)

<img width="184" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/e261f63e-4ec4-435c-9bf7-f85dcfbc88a0">

### Now, I created a test table called 'lemp_list' and added content to it

<img width="304" alt="image" src="https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/c73a8d90-ab3b-4721-b7c8-2f89f76edf7c">

