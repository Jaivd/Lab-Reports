# Lab Report 4

In this lab report I will be challenging to quickly run tests on a server, fix the code, run them again and then push it code back to the repository. This is how I did it in the least amount of time possible. 
*Note before I started, I had set up logging into my account without a password for quicker login as well as generating an ssh key for github to allow for quick pushing*

The steps I will be following for this challenge task are as follows:
> 1. **Setup** Delete any existing forks of the repository you have on your account
> 2. **Setup** Fork the repository
> 3. **The real deal Start the timer!**
> 4. Log into ieng6
> 5. Clone your fork of the repository from your Github account
> 6. Run the tests, demonstrating that they fail
> 7. Edit the code file to fix the failing test
> 8. Run the tests, demonstrating that they now succeed
> 9. Commit and push the resulting change to your Github account

## Step 1 through 3
Since this I will be attempting this challenge again, I will delete the repository and then refork it. 
To delete the repository, I will go to the forked respository, then go to settings and in general scroll to the bottom and click delete repository. The following message will pop up prompting me to confirm the deletion of the repository. ![image](https://user-images.githubusercontent.com/122576180/221385623-4266d9f3-3ca9-4944-96fa-344e24e51829.png)
I will then enter the name and delete the repository to start fresh. 

To fork the repository I will go to [this](https://github.com/ucsd-cse15l-w23/lab7) repository and then click 'Fork' in the top left corner. This page will pop up and I will use then click create fork to then finally succesfully fork my repository. 
![image](https://user-images.githubusercontent.com/122576180/221385546-7fd8374e-b209-42b8-a7e2-efa2e32aa470.png)
Once this is done, I am ready to start fresh. 

## Step 4 logging into my account 
I opened bash terminal on my laptop and then typed in my ieng account (cs15lwi23aia@ieng6.ucsd.edu)

```
$ssh cs15lwi23aia@ieng6.ucsd.edu
```

This will then be the following output:
![image](https://user-images.githubusercontent.com/122576180/221385821-cd5d4fa1-b6aa-4939-9960-51c527f604f9.png)

## Step 5 cloning the repository 
In the account I will run the following code, copy pasting the repository link (https://github.com/ucsd-cse15l-w23/lab7) from this document.

```
$git clone https://github.com/ucsd-cse15l-w23/lab7
```
*Keys Pressed : <Cntrl-v> (for the url of the repository)* 

# Step 6
