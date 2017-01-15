---
layout: post
title: 30DaysOfCode - Day 3
excerpt_separator: <!--more-->
---

The last two days I didn't get any coding done besides looking through my Java textboook. Back to schedule today, day 3!

I figured out what was wrong with my setup in Codenvy last time. I had created a file object and passed my hello.txt file to it but when I checked it with the ```File.exists()``` method, I kept getting ```false``` which meant the file did not exist or could not be found. 

I had moved the file from my src folder to the root of the project folder and it didn't work so I ended up re-creating the file in the root of my project folder as hello2.txt and success, it worked! 

Here's my code again from before: 

```
import java.io.*; // Needed for File and IOException
import java.util.*; // Needed for Scanner class

public class Fello {
    
    
    public static void main (String[] args) throws IOException {
        
        File file = new File("hello2.txt");
        System.out.println(file.exists());
        
    } //end of main

} //end of class
```
<!--more-->
Now, I can start using the ```Scanner``` class to read lines from the file. See below for the setup:

```
import java.io.*; // Needed for File and IOException
import java.util.*; // Needed for Scanner class

public class Fello {
    
    
    public static void main (String[] args) throws IOException {
        
        File file = new File("hello2.txt");
        Scanner txtFile = new Scanner(file);
        
    } //end of main

} //end of class
```

Again, the first statement creates a ```file``` object that represents the file hello2.txt, also opening the file. The second statement passes a reference to the ```file``` object instead of ```System.in``` to the ```Scannner``` class constructor.

Next, I want to read just the first line of the file. I can do so by creating a String to store the ```.nextline()``` in the file and print it to the console like so:

```
import java.io.*; // Needed for File and IOException
import java.util.*; // Needed for Scanner class

public class Fello {
    

    public static void main (String[] args) throws IOException {
        
        // Open file
        File file = new File("hello2.txt");
        Scanner txtFile = new Scanner(file);
        
        // Read a line
        String readLine = txtFile.nextLine();
        
        // Print the first line
        System.out.println("The first line in the file is:");
        System.out.println(readLine);
        
    } //end of main

} //end of class
```

The result is:
```
The first line in the file is:
Hello, it's me
```

If we check against the hello2.txt file in the project we see that is correct!

![Read Line Result](/_posts/Fello--ReadLineResult.PNG)

The last part is to read the text file in it's entirety. I found there are a few ways to do this and the way that makes most sense for me is a while loop.

With a while loop I can have the program check if the file has another line and print each line while that's true so it eventually print the entire text file. This is the code I have for that:

```
import java.io.*; // Needed for File and IOException
import java.util.*; // Needed for Scanner class

public class Fello {
    

    public static void main (String[] args) throws IOException {
        
        // Open file
        File file = new File("hello2.txt");
        Scanner txtFile = new Scanner(file);
        
        // Read a line
        String readLine = txtFile.nextLine();
        
        // while loop to print each line
        while(txtFile.hasNextLine()) {
        	System.out.println(readLine);
        }
        
    } //end of main

} //end of class
```

When I did this my codenvy environment froze. I realized I needed to put my String inside the while loop and when I did it worked! If I wanted to, I could remove it altogether and just print the value of the String variable in the while loop as ```System.out.println(txtFile.nextLine());``` instead. I am going to leave as-is in the meantime and will refactor when I create my methods.

I also surrounded the while loop with a try/catch block so it could catch any exception and throw it out without stopping the program. This is my main method program so far (without my own methods) to read and print a file.

```
import java.io.*; // Needed for File and IOException
import java.util.*; // Needed for Scanner class

public class Fello {
    

    public static void main (String[] args) throws IOException {
        
        // Open file
        File file = new File("hello2.txt");
        Scanner txtFile = new Scanner(file);
        
        try {
           // While loop to print each line
           while(txtFile.hasNextLine()) {
               
               // Read a line
               String readLine = txtFile.nextLine();
               // Print a line
               System.out.println(readLine);
               
           } // end of while loop
            
        } catch (Exception e) {
           
           // Print stacktrace if exception found
           e.printStackTrace(); 
           
        } // End of catch
        
    } // End of main

} // End of class
```

It prints out the entire file as expected:

![Print File](/_posts/Fello--PrintFile.PNG)

Next, I will be working on my methods:

1. Open a file
2. Read a file
3. Replace a specific String in file with another
4. Print the resulting file

On to day 4 tomorrow!

