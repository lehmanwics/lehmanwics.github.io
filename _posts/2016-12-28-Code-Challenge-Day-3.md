---
published: false
---
## 30DaysOfCode - Day 3

The last two days I didn't get any coding done besides looking through my Java textboook because I was sick. Back to schedule today, day 3!

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

Next, I want to read line