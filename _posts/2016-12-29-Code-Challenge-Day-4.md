---
published: false
---
## A New Post

Day 4 is here and it's going well...too well.

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
               // Replace a string with another string
               String replaceLine = readLine.replaceAll("(?i)hello", "goodbye");
               // Print each line
               System.out.println(replaceLine);
               
           } // end of while loop
            
        } catch (Exception e) {
           
           // Print stacktrace if exception found
           e.printStackTrace(); 
           
        } // End of catch
        
    } // End of main

} // End of class
```
