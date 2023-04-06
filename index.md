# Lab Report
## Step 1 VSCode 
Firstly, I need an application for all of my later cse 15l lab work, so I download the VSCode from  https://code.visualstudio.com/ and follow the instruction on this website to run the installing package on my MAC OS system. 
After I changes the background color and download numbers of plug-in, it look something like this:
![Image](Assets/VSCode.png)

## Step2 Remotely Connecting
After getting the account name and reset the password for CSE15L account. I can have access to the cse basement computers.
To connect remotely, I followed the following steps:
1. Open VSCode
2. Open terminal
3. To use **ssh** and enter the account name
  
  ssh cs15lsp23bt@ieng6.ucsd.edu 
  
4. Enter the password of my account 

  2bmjaNmcu@Nw2e*

Then I see the terminal message:
![Image](Assets/Remotely_Connecting.png)
This indicates I am successfully connected remotely to the ucsd cs basement computer

## Step3 Trying Some Commands
Now it is time to play around. 
![Image](Assets/Step3.png)
As the picture show above, I firstly check the file in current path by use `ls`, and it shows that there is only a file called `perl5` in this path. 
Then I try the command `ls -a` which will show all of the file including the hidden file. 
Then I try the command `cd` which takes me to the home directory.
I can check the home directory by using command `pwd`, it returns /home/linux/ieng6/cs15lsp23/cs15lsp23bt
I am also able to check other path remotely such as /home/linux/ieng6/cs15lsp23/public/hello.txt I can print the file by using `cat` and it print "Hello!"
Pretty cool!

