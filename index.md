# Lab Report 3 - Researching Grep
grep is ainly used to find a certain keyword withing files. In this report I will describe a few other ways to use grep. 

## Method 1 - grep searching a singular file
This is the most basic method of using grep. The syntax to use htis function is 
····grep <keyword> <file name>
  
This will find the number of occurence of that particular keyword in that file. It will show every line in the file with that keyword. 
**Example 1**
  ![image](https://user-images.githubusercontent.com/122576180/218659365-dab92dee-d29e-4717-99d0-ad2c07ca9ced.png)
As you can see from the example above, grep displays all of the lines with the word garden in it. 
  
**Example 2**
  ![image](https://user-images.githubusercontent.com/122576180/218659536-a4f6439f-fcce-4dba-baf1-f5560381ec75.png)
Here I used grep on my own name, and as you can see that resulted in an empty output, signifying my name is nowhere to be found in Ch1 of Berk. 

## Method 2 - Searching for a keyword in all files in a directory. 
  This can be accomplished through 
  ····grep -w <keyword> *
  the -w tells the computer to only search for the keyword in all of the files. The astrix tell the computer to search all the files. 
  
**Example 1**
    ![image](https://user-images.githubusercontent.com/122576180/218660255-2226fef2-d4ea-4ab0-a013-c7fff5034f0f.png)
  As you can see, thw word garden was returned twice from ch1.txt and once from ch2.txt. 
  
**Example 2**
  ![image](https://user-images.githubusercontent.com/122576180/218660648-b58f58a2-253a-4f1b-93e3-521b41115188.png)
 Over here once can see that grep did not return anything despite there being instances of words having ee in the file. This is because grep only find specific instances rather that the phrase used in the middle of other words like "screen" or "tree"
  
## Method 3 - Ignoring case
  In this example, we see how to use grep ignoring whether the phrase is uppercase or lowercase. The code of this is:
  ····grep -i <keyword> *
  the -i signifies to the ignore the case while *, as mentioned previously, searches all the files. 


## Sources
https://phoenixnap.com/kb/grep-command-linux-unix-examples
