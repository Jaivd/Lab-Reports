# Lab Report 1 - Remote Access 

Welcome CSE 15L Stduents. Today I will be explain all of you how to set up remote access to the CSE servers on your computer. 

## Installing VScode
The first thing you will need to do is install VScode on your computer. If you already have VScode downloaded you can skip this section. 
*(If you are not planning on using your own personal computers and are planning on using the computers in the lab you can skip this section)*

**Step 1 - Download Visual Studio Code**
    You can download the editor from this link [here](https://code.visualstudio.com/)
    Download the version for your computer (Mac/Windows/Linux)
    Click the blue download button to start downloading
    ![Image](https://jaivd.github.io/Lab-Reports/Screenshot%202023-01-12%20153541.png)
    
**Step 2 - Follow the instructions to install the software**
    Once downloaded, open (or double click) on the downloaded file and then follow the instructions in front of you in order to install the software.
    
**Step 3 - Open VScode**
    Once opened, your VScode should look something like this. If it does, that means you have succesfully installed VScode!
    ![Image](https://jaivd.github.io/Lab-Reports/Screenshot%202023-01-13%20145439.png)

## Remote connecting
  Here we are going to use the terminal on our VScode to connect to the UCSD server. 
  This is a useful skill to have as many of the CSE courses at UCSD have unique accounts and some work requires us to use the servers. 
  This skill could also be carried over to any future occupations. 
    
**Step 1 - Download git**
    *This step is only for windows computers*
    You can download git from [here](https://gitforwindows.org/)
    Similair to how we downloaded VScode, follow the steps after opening the downloaded file and git should be installed. 
    After that, to open git in your VScode terminal, follow the instructions below. 
    [Link to the guide shown below](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994)
    ![Image](https://jaivd.github.io/Lab-Reports/Stackoverflow.png)
    
**Step 2 - Using Terminal** 
    Now, in VScode open terminal (open using the tab on the top left corner of your screen). In terminal (The box on the bottom of your screen), type in `ssh` followed by your CSE 15L account ID with the phrase '@ieng6.ucsd.edu' appended to the end of it. It should look something like the example below, however in place of the 'aia' it would be whatever code is unique to your account. (Note: Anything written in a box, like below, signifies what is in the terminal)
  ```
  $ ssh cs15lwi23aia@ieng6.ucsd.edu
  ```
    
  As this is the first time you will be connecting to the server, this will be the output
  ```
  The authenticity of host 'ieng6.ucsd.edu (128.54.70.238)' can't be established RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec. 
  This key is not known by any other names. 
  Are you sure you want to continue connecting (yes/no/[fingerprint])? 
  ```
  Type in yes and click enter.for an explanation as to why this message is popping up can be found [here](https://superuser.com/questions/421074/ssh-the-authenticity-of-host-host-cant-be-established/421084#421084)
  The computer should then prompt you for a password. Go ahead and give them your password. (Don't worry if you cannot see the password while typing, that is a precaution for security measures. Once you click enter, the password will be submitted)
  
  Once that is done, it will give you some details about the sever and some other information as shown below. 
  ![image](https://user-images.githubusercontent.com/122576180/212446336-e370d3e4-a2b9-4d7f-8cee-5cb5f49a7e12.png)
  
  Congratualtions! you are now remotely connected to the CSE servers. Anything you type in terminal now will be running on the servers, rather than what you previously typed (which was running on your laptop). 
  
## Practice Commands
Now that you are connected, its time to have some fun! you should try out some of the commands below and figure out what each of them do. 
* `cd`
* `ls`
* `pwd`
* `mkdir`
* `cp`
* `ls -lat`
* `ls -a`
* `cp /home/linux/ieng6/cs15lwi23/public/hello.txt ~/`
* `cat /home/linux/ieng6/cs15lwi23/public/hello.txt`

An example of one of the commands above is `ls-lat`, which as can be seen below, shows a list of all the files on the server sorter by date
![image](https://user-images.githubusercontent.com/122576180/212446647-02e7e6d1-ebda-4ecf-9314-54d1f072f62a.png)

When you are done with using the server, use (Ctrl/Command D) to quit the connection and with that you've ended your remote connection. 




