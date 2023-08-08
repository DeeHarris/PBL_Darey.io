## Documentation for Project 3
# "MERN Stack Implementation (MongoDB, ExpresJS, ReactJS, Node.js)"

## In this project, I will be implementing a 'To-Do List' application using MERN web stack solution on AWS Cloud 

### First, I connected to my EC2 instance, upgraded my Ubuntu package manager, and installed NodeJS and its package manager (NPM)

(All successful)

![image](https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/79bbe9ad-61e3-46af-a15b-db65c7c953f1)

### Next I created a new directory called 'Todo'

After that, I changed into the new directory

    cd Todo
    
### Next, I created a 'JavaScript Object Notation' (.json) file using the _initialize_ command

    npm init

![image](https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/835fe318-e3b1-4373-91c9-593fe39361a1)

### Next, I installed the Web App framework for Nodejs (ExpressJS) and created an index.js file afterward

![image](https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/4db50069-cfd1-4dcb-81af-698da53fc89b)

### Next, I installed the environment module 'Dotenv', and using my text editor I wrote a script in the index.js file I earlier created

![image](https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/39d1d006-9dae-4627-912b-eff5e8a15b55)

### And after opening a custom port (5000) on my EC2 instance, I was able to connect using the public IP

![image](https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/942b8898-245f-43b0-86e9-cc137e39f31c)

### Next, after identifying the set actions for the 'Todo list' application, I create _'Routes'_ to define endpoints

I started by creating a directory named "Routes" and after that an _'api.js'_ file.

After that, I edited the file with my editor and wrote the script to define the routes and actions

![image](https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/07d98823-f16a-4a85-8290-9598e2d77222)

### Next, I install _'Mongoose'_ which is the NodeJS module that helps us work with MongoDB. 

I then create models _(this is to make my Todo list application interactive)_

Started by creating a directory called _Model_ and inside it I created a _todo.js_ file

After which I edited the _todo.js_ file and wrote the script to define the schema

![image](https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/2fef35e9-a555-43ad-8446-063d2a82b853)

### Next I went to my routes directory to change the script written earlier _(this is so it can now make use of the model I just created)_

### Next, as we will be using MongoDB as our database, I registered on mLab, created a free service, and set it to be assessed from anywhere.

![image](https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/62cf3573-fa97-4b31-8890-9853b38a10ba)

### I then created a _'.env'_ file and added the connection string to my database using vi

![image](https://github.com/DeeHarris/PBL_Darey.io/assets/20859155/18ac3897-9836-4101-90da-207e4e3862d8)
