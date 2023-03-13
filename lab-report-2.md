# Lab Report 2

## Part 1
In this part of the report I will write a program called `StringServer.java` that tracks strings that get added by incoming requests. My code for this is as shown below:

```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    String s = "";
    String next_line = "\n";

    public String handleRequest(URI url) {
        System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    s += next_line;
                    s += parameters[1];
                    return s;
                }
                return "404";
            }
            return "404";
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```

**Example 1**
![image](https://user-images.githubusercontent.com/122576180/215357136-1cb8333d-7a53-42a0-be88-75f51f877361.png)
* This calls the Handler method as well as the default constructor.
* The relevant arguments are 'String[] parameters = url.getQuery().split("=");' which turns the URL into a string after the = sign, allowing us to hen extract the text from the URL, which as can be seen from the image is 'This will now be shown on the screen'.
* The only value that changed from this request is the string value s, which has now become 'This will now be shown on the screen'. THe URI matches the URI shown above. 

**Example 2**
![image](https://user-images.githubusercontent.com/122576180/215362258-5ad07bb9-6ac9-4977-affe-c8ca50319e8f.png)
* This example also calls the Handler method as well as the default constructor. 
* Here, Before i put the URL as seen in the screenshot, I used the URL http://localhost:4000/add-message?s= so that it will leave a line before displaying the new output, which as can be seen is 'THis will now be printed after leaving a line'. This also uses the same arguments as the example before. 
* The string value s has now change to become 'This will now be shown on the screen \n\nTHis will now be printed after leaving a line'. THe URI also now matches the URI shown in the image. 


## Part 2
The function with a bug that I will be talking about in this report is the `static void reverseInPlace(int[] arr)` from the file 'ArrayExamples.java' which can be found [here](https://github.com/ucsd-cse15l-w23/lab3). 

The JUnit test I used to test the methods is as follows:

* Test 1 *(This test should exposes the bug and fail)*
```
  @Test
  public void testReverseinplacenew() {
    int[] input2 = new int[]{1,2,3,4,5};
    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[]{5,4,3,2,1}, input2);
  }
```

* Test 2 *(This test should not expose the bug and should pass)*
```
	@Test 
	public void testReverseInPlacenew2() {
    int[] input1 = { 18 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 18 }, input1);
	}
```

I then compiled and executed the files, using
> For Mac
> local $ javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
> local $ java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ArrayTests
JUnit version 4.13.2

>For Windows
>local $ javac -cp ".;lib/hamcrest-core-1.3.jar;lib/junit-4.13.2.jar" *.java
>local $ java -cp ".;lib/junit-4.13.2.jar;lib/hamcrest-core-1.3.jar" org.junit.runner.JUnitCore ArrayTests

**This was the output**
![image](https://user-images.githubusercontent.com/122576180/214992289-c940bcda-2d72-46e5-8c73-e315f847728b.png)
As we can see, the first test failed while the second test passed, as we expected. 

The reason the first test failed is because the array is swapping the values but not saving the swapped value. So if we use the array given in Test 1, instead of [5,4,3,2,1], we are getting [5,4,3,4,5]. Hence to fix this we just need to save the swapped value and then use that to change the original position, as you can see in the changes made below. Additionally, the loop should not run through the entire loop, rather only run through half of the loop, as we are swapping boht the values in one iteration, so the limit in the for loop should be `i<arr.length/2`. 
**Uncorrected code**
```
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
 ```
 
 **Corrected code**
 ```
   static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/2; i += 1) { //Limit of the list here is changed
      int saved_value = arr[i]; //Saves this value so that it an be used to reverse the list
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = saved_value; //This line is added to swap the other value
    }
  }
  ```

## Part 3

I learnt from Lab 2 how to decode a URL in Java. I also learned in Lab 2 how to host a website on a remote server so that it can be accesed in multiple locations. 
