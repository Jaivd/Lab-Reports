# Lab Report 5 - Researching less
In lab report 3, I used grep and showcased how grep was used with different functions. In this lab report I will do the same thing, but with the less command

## Method 1 - less standard
This is the most basic method of using less. The syntax to use this function is 
```
less <file name>
```
  This will showcase the contents of the file line by line. 
  
**Example 1**
![image](https://user-images.githubusercontent.com/122576180/224581949-5e023e22-ce86-4200-87ce-f60e4b4c75dc.png)

In the above screenshot, I used the command `less ch1.txt`. When doing this, as one can see, it showcased the beggining of the file and not the entire file, this allows the user to peep into the file. Since the bar to type a new command hasnt been seen, we can see that the user can press enter and more of the file will load, making it easier to access to parse through a file on a terminal, compared to the cat function which displays everything as a massive string making large files difficult to digest. 
  
**Example 2**

![image](https://user-images.githubusercontent.com/122576180/224582574-21b8deab-6666-4d72-99fe-98a26012d2e6.png)

Here we can see when I tried to use `less` on a  folder, it gives me this error. So less can only be used to show the contents of a specific file, not the contents of a directory. 

## Method 2 - Line numbers 
  You can also show specific line numbers in a file. 
  ```
  less -N <file_name>
  ```
  the -N tells the computer to show all the line numbers
  
**Example 1**
    ![image](https://user-images.githubusercontent.com/122576180/224582395-8d4c983a-f28a-4c7b-9662-7294b9ec38b5.png)

The command I ran here was `less -N ch1.txt`. As you can see, it shows the line numbers of all the lines in the file. A unique feature to notice about this is how the smae line number is repeated several times. This showcases to us how it shows line numbers associated with the actual txt file rather than lines on the terminal. 
  
**Example 2**

![image](https://user-images.githubusercontent.com/122576180/224582647-b3f58098-4b35-4e14-b498-a123e42e4ae8.png)

Here I ran the command `less -N ch10.txt`. ch10.txt is an empty file that I created. As you can see since it is completely empty it does not show any line numbers, not even line number 1. 
  
## Method 3 - Searching a file
  In this example, we see how after opening a file you can search the contents of the file. 
  ```
  / <keyword>
  ```
  the / tell the computer to search and the keyword is the keyword to search for. This should only be run after using the original less function. 
  
**Example 1**
![image](https://user-images.githubusercontent.com/122576180/224582900-1752ddaf-4e91-440b-9c7b-82daf49f194c.png)

The command I used here was `/ parents` after using `less ch1.txt`. As you can see the computer now highlights all the instances of parents it finds. It however does not give  a count for the number of instances of parents. Moreover, if I proceed to press enter it will continue to highlight all instances of the word parent. 

**Example 2**
![image](https://user-images.githubusercontent.com/122576180/224583017-98ec9813-f204-47bf-8d8b-f6896b68c40c.png)

In this example, I used the command `/ child`. THe reason for this, as shown in the screenshot, is to show how this command is not case sensitive. It is showing every instance of the word child, including when the word child is using in other words like children. 

## Method 4 - Blank Lines
While less is extremely useful, sometime the blank line can take up valuable space on your terminal. This is how one can get rid of it. 
```
less -s <file_name>
```
Here, -s tell the computer to not display blank lines. 

**Example 1**
![image](https://user-images.githubusercontent.com/122576180/224583506-3062a2db-de00-469e-8b66-3c3ece2ce52a.png)

The command I used here was `less -s ch1.txt`. Now we can see a lot more the file. If we compare this to Example 1 in Method 1, we cna see more information has been displayed in the same amount of space. However something important to note is that it does not overwrite intentional formatiing ad there is still a line ga between the parahgraph and the bullet points. 

**Example 2**

![image](https://user-images.githubusercontent.com/122576180/224583758-7de152b1-8d31-4d79-bae4-e3ac08d844b4.png)

The command I used here was `less -N -s ch10.txt`. I modified ch10.txt, the file created by me, to have '(Hello world)' on line number 10 and nothing before. As you can see, by combining `-N` and `-s`, we can see that while the program removes all blank lines, it preserves the line numbers and position of text, but compressed it down to make it easier to read. This example also shows how one can combine several methods together to get the output they would like. 
## Sources
https://phoenixnap.com/kb/less-command-in-linux
