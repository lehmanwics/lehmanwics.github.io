---
published: false
---
## 30DaysOfCode - Day 3

The last two days I didn't get any coding done besides looking through my Java textboook because I was sick. Back to schedule today, day 3!

I figured out what was wrong with my setup in Codenvy last time. I had created a file object and passed my hello.txt file to it but when I checked it with the ```File.exists()``` method, I kept getting ```false``` which means it did not exist or could not be found. 

I had moved the file from my src folder to the root of the project folder and it didn't work so I ended up re-creating the file in the root of my project folder as hello2.txt and success, it worked! 

Here's my code again from before:

```
import java.io.*;
import java.util.*;

public class Fello {
    
    
    public static void main (String[] args) throws IOException {
        
        File file = new File("hello2.txt");
        System.out.println(file.exists());

    } //end of main

} //end of class
```
gfdfg