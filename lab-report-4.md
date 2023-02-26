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
To delete the repository, I will go to the forked respository, then go to settings and in general scroll to the bottom and click delete repository. The following message will pop up prompting me to confirm the deletion of the repository. 

![image](https://user-images.githubusercontent.com/122576180/221385623-4266d9f3-3ca9-4944-96fa-344e24e51829.png)

I will then enter the name and delete the repository to start fresh. 

To fork the repository I will go to [this](https://github.com/ucsd-cse15l-w23/lab7) repository and then click 'Fork' in the top left corner. This page will pop up and I will use then click create fork to then finally succesfully fork my repository. 
![image](https://user-images.githubusercontent.com/122576180/221385546-7fd8374e-b209-42b8-a7e2-efa2e32aa470.png)
Once this is done, I am ready to start fresh. 

## Step 4 logging into my account 
I opened bash terminal on my laptop and then typed in my ieng account (cs15lwi23aia@ieng6.ucsd.edu)

```
$ssh cs15lwi23aia@ieng6.ucsd.edu
```
Keys pressed: `<enter>`

This will then be the following output:
![image](https://user-images.githubusercontent.com/122576180/221385821-cd5d4fa1-b6aa-4939-9960-51c527f604f9.png)

## Step 5 cloning the repository 
In the account I will run the following code, copy pasting the repository link (https://github.com/ucsd-cse15l-w23/lab7) from this document.

```
$git clone https://github.com/ucsd-cse15l-w23/lab7
```
Keys Pressed : `<Cntrl-v>` (for the url of the repository) `<enter>`
  ![image](https://user-images.githubusercontent.com/122576180/221385995-94090e9e-3c03-4fd0-b831-fd12a4902518.png)


# Step 6 Running the tests
For this, I will copy paste the commands mentioned below to run the tests. First I will cd into the folder and then run the tests. 
  
```
$cd lab7
$javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
$java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
```
Keys pressed : `<enter>`, `<Cntrl-v>` `<enter>`, `<Cntrl-v>` `<enter>`
![image](https://user-images.githubusercontent.com/122576180/221386112-51676dd9-6a2d-4f8d-a697-69eb70153479.png)

# Step 7 Editting the code
To fix the mistake, we must edit the code. We could do so using either vim or nano but for my challenge I used nano. I first ran 
```
$nano ListExamples.java
```
Keys Pressed : `<tab>` (when typing List examples to type it quicker) `<enter>`
![image](https://user-images.githubusercontent.com/122576180/221386282-37873a1f-900e-4785-99c9-049354f74c0b.png)

This then opened a nano editor and then repeatedly pressed `<down>` untill I reached the last while loop in which I changed the value of the increment function from `index1 += 1;` to `index2 +=1;`. 
 I then pressed `<Cntrl-O>` `<enter>` `<Cntrl-X>`. This saves the file and exits. 

# Step 8 Rerunning the tests
For this I will use the same commands we previously used to run the tests. To do this, I will use Control R (This searches your command history and returns the closest match)
Keys Pressed: `<Cntrl-r>` `javac` `<enter>`, `<Cntrl-r>` `java` `<enter>`
This allowed me to re run the texts extremely quickly. 
![image](https://user-images.githubusercontent.com/122576180/221386495-b58452c3-e613-445e-88af-9f87a2190f62.png)

# Step 9 Commiting and pushing the files to github
For this, To quickly type the commands, I used tab. 

```
$ git add ListExamples.java ListExamplesTests.class
```
Keys Pressed: `<tab>` (After typing L to quickly get the name of the file) `<tab>` `<enter>`
```
$ git commit -m "Fixed"
```
![image](https://user-images.githubusercontent.com/122576180/221386727-67b475cd-14c9-4958-a855-a76bde6c22af.png)

And then finally pushing the commit, doing so using my unique ssh (git@github.com:Jaivd/lab7.git) *SSH key must be established beforehand for this to work*
``` 
$ git push git@github.com:Jaivd/lab7.git
```
Keys Pressed: `<Cntrl-v>` (this was for the ssh key)
![image](https://user-images.githubusercontent.com/122576180/221386782-0247dd1e-de96-4937-9282-5a63766f6bd0.png)

  


  
