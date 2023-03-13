# Lab Report 3 - Researching Grep
grep is mainly used to find a certain keyword withing files. In this report I will describe a few other ways to use grep. 

## Method 1 - grep searching a singular file
This is the most basic method of using grep. The syntax to use htis function is 
```
grep <keyword> <file name>
```
  This will find the number of occurence of that particular keyword in that file. It will show every line in the file with that keyword. 
  
**Example 1**
  ![image](https://user-images.githubusercontent.com/122576180/218659365-dab92dee-d29e-4717-99d0-ad2c07ca9ced.png)
As you can see from the example above, grep displays all of the lines with the word garden in it. 
  
**Example 2**
  ![image](https://user-images.githubusercontent.com/122576180/218659536-a4f6439f-fcce-4dba-baf1-f5560381ec75.png)
Here I used grep on my own name, and as you can see that resulted in an empty output, signifying my name is nowhere to be found in Ch1 of Berk. 

## Method 2 - Searching for a keyword in all files in a directory. 
  This can be accomplished through 
  ```
  grep -w <keyword> *
  ```
  the -w tells the computer to only search for the keyword in all of the files. The astrix tell the computer to search all the files. 
  
**Example 1**
    ![image](https://user-images.githubusercontent.com/122576180/218660255-2226fef2-d4ea-4ab0-a013-c7fff5034f0f.png)
  As you can see, thw word garden was returned twice from ch1.txt and once from ch2.txt. 
  
**Example 2**
  ![image](https://user-images.githubusercontent.com/122576180/218660648-b58f58a2-253a-4f1b-93e3-521b41115188.png)
 Over here once can see that grep did not return anything despite there being instances of words having ee in the file. This is because grep only find specific instances rather that the phrase used in the middle of other words like "screen" or "tree"
  
## Method 3 - Ignoring case
  In this example, we see how to use grep ignoring whether the phrase is uppercase or lowercase. The code of this is:
  ```
  grep -i <keyword> *
  ```
  the -i signifies to the ignore the case while the astrix, as mentioned previously, searches all the files. 
  
**Example 1**
![image](https://user-images.githubusercontent.com/122576180/218662063-87ef4aae-3267-4e0d-a9c9-85ca44a2d46a.png)
As you can see, in both of the instances returned, Hello is in uppercase but me putting the function in lowercase did not make a difference. 

**Example 2**
![image](https://user-images.githubusercontent.com/122576180/218662336-61a6f620-7911-4e0d-a5b3-904446a2adfe.png)
In this example, I deliberately used a number as a keyword as that is neither lower or uppercase and the grep command was still able to find it in the files without any issue. 

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
https://phoenixnap.com/kb/grep-command-linux-unix-examples
