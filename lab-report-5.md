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

In the above screenshot, I used the command `less ch1.txt`. When doing this, as one can see, it showcased the beggining of the file and not the entire file, this allows the user to peep into the file. Since the bar to type a new command hasnt been seen, we can see that the user can press enter and more of the file will load, making it easier to access to parse through a file on a termina, compared to the cat function which displays everything as a massive string making large files difficult to digest. 
  
**Example 2**
![image](https://user-images.githubusercontent.com/122576180/224582574-21b8deab-6666-4d72-99fe-98a26012d2e6.png)

Here we can see when I tried to use `less` ona  folder, it gives me this error. So less can only be used to show the contents of a specific file, not the contents of a directory. 

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

The command I used here was `/ parents' after using `less ch1.txt`. As you can see the computer now highlights all the instances of parents it finds. It however does not give  a count for the number of instances of parents. Moreover, if I proceed to press enter it will continue to highlight all instances of the word parent. 

**Example 2**
![image](https://user-images.githubusercontent.com/122576180/224583017-98ec9813-f204-47bf-8d8b-f6896b68c40c.png)

In this example, I used the command `/ child`. THe reason for this, as shown in the screenshot, is to show how this command is not case sensitive. It is showing every instance of the word child, including when the word child is using in other words like children. 

## Method 4 - Excludinging keywords
In this example, I will show you the syntax to write grep in order to exclude lines with certain instances of keywords. 
```
grep -v <keyword> <filename>
```
Here, -v tell the computer to exclude results with this specific keyword. 

**Example 1**
![image](https://user-images.githubusercontent.com/122576180/218663168-dca76ba3-929b-41ff-9b7b-aaca719b54f9.png)
Here, te computer printed out all the lines without the keyword I in chpater 1. I was not able to include the entire output due to its size. THis function is useful if there is a repition of an output that you do no require. 

**Example 2**
![image](https://user-images.githubusercontent.com/122576180/218663610-ee55d654-7caa-4153-9ac6-deba0dfbb742.png)
Here, again I used my own name and as a result the entire file was outputed. THis signifies that it does not check if the keyword is in the file rather searches for files without the keyword.

## Sources
https://www.hostinger.com/tutorials/how-to-use-find-and-locate-commands-in-linux/
