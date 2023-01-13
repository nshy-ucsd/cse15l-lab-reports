# CSE15L Tutorial 

Welcome to my tutorial for new CSE15L students. \
This guide will include step-by-step instructions to install VSCode, remote connect to ieng6, and try some commands.

## Installing VSCode
Feel free to skip this step if you are not planning to use your personal laptop for any of the labs in this course (which you don't have to).
1. First, go to [the Visual Studio Code website](https://code.visualstudio.com) (https://code.visualstudio.com). <img width="600" alt="image" src="https://user-images.githubusercontent.com/122579697/212215180-e252bc26-f9f2-4d35-b746-3297822ff28b.png">

2. Next, click the blue icon that says "download" in the upper right-hand corner. <img width="600" alt="image" src="https://user-images.githubusercontent.com/122579697/212215137-ac6e3a35-5aca-4d05-87cc-6463a8c3aa94.png">

3. And then choose the operating system that you are using (macOS, Windows, or Linux) and click it. 
4. Now open the file you just downloaded and start installing
5. After successfully installing VSCode, you should have something like this after opening it: <img width="600" alt="image" src="https://user-images.githubusercontent.com/122579697/212215332-9619e1e3-1c4a-4bdc-9c9d-03361aaf6f79.png">

## Remote connect to ieng6
This part is likely to be the trickiest part of this tutorial, so here comes nothing!
### Some extra steps for windows user
*I don't have any screenshots for these steps since I am not using a Windows laptop*
1. Now before we start anything, you probably need to install [git for windows](https://gitforwindows.org) first if you are a Windows user.
2. After successfully installing, follow the steps in [this guide](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994) to set your default terminal to use git bash in visual studio code.

Now up to this point, everyone should be on the same page. It is now time to log in using ssh.
1. First, open up the terminal on your visual studio code. (use ctrl + \` or pull down the menubar that says terminal and click on "new terminal") \
   <img width="600" alt="image" src="https://user-images.githubusercontent.com/122579697/212217334-78ac16ae-6a91-401c-ae20-a35799291724.png">
2. Next, enter "ssh *Your_account_name*@ieng6.ucsd.edu", where your account name should be something like cs15lwi23**. <img width="600" alt="image" src="https://user-images.githubusercontent.com/122579697/212217573-448ded81-a3c0-4896-a8a5-a426ca0a7a0b.png">
3. Now enter your password for your account and log in.
4. Since it is likely your first time logging in, enter "yes" if you see something like this:
> The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
Are you sure you want to continue connecting (yes/no/[fingerprint])? 

5. Now you should be logged in to your account on ssh, and should see something like this: \
 <img width="492" alt="image" src="https://user-images.githubusercontent.com/122579697/212218323-f1e52a94-72a4-4e1c-8bb6-70d12da737fa.png">
