---
published: false
---
## 30DaysOfCode - Day 3

Day 4 is here and it's going well...too well. I didn't need to do much to get my program to replace one word, "hello", with another word, "goodbye". 

I used the ```.replaceAll()`` method to replace the string:

```public String replaceAll(String regex, String replacement)``` 

I added a case-sensitive switch ```(?i)``` to the regex in order to make the case insensitive. This means that even if "hello" is found as "**h**ello" in the file it will still replace it with "goodbye". 

These are some great resources to learn more about regular expressions:

-[Guide to Regular Expressions in Java (Part 1)](http://www.ocpsoft.org/opensource/guide-to-regular-expressions-in-java-part-1/ "Guide to Regular Expressions in Java (Part 1)")

-[Specifying Modes Inside The Regular Expression](http://www.regular-expressions.info/modifiers.html "Specifying Modes Inside The Regular Expression")

My final program to replace a string in a text file with another string looks like this:

```
import java.io.*; // Needed for File and IOException
import java.util.*; // Needed for Scanner class

public class Fello {


    public static void main(String[] args) throws IOException {

        // Open file
        File file = new File("hello2.txt");
        Scanner txtFile = new Scanner(file);

		// Start of try/catch block
        try {

            // While loop to print each line
            while (txtFile.hasNextLine()) {

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
![Fello Final Program](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/Fello--FinalProgram.PNG)

----------------------

I spread this project out over several days so I could research what I was implementing and understand what I was doing and all told, the actual coding was probably about 2 hours or less in total with the rest of the time spent researching, reading, and troubleshooting my Codenvy environment. 

The solution is not very elegant (yet) but I am happy it works. I am plenty sure there are multiple ways to do this as well. 

I know you can also use the ```BufferedReader``` class instead of the ```Scanner``` class like so:

```
        try (BufferedReader bReader = new BufferedReader(new FileReader("hello2.txt"))) {
            String line;

            while ((line = bReader.readLine()) != null) {

                // Replace a string with another string
                String replaceLine = line.replaceAll("(?i)hello", "goodbye");
                System.out.println(replaceLine);

            } //end of while loop
        } catch (IOException e) {

            e.printStackTrace();

        } //end of catch
```
This try/catch block is saying that while there is a ```nextLine``` (not null) to be read in the file, read the line, replace the "hello" string with "goodbye" and print out each line until the end of the text file.

The following article provides some detail on the differences between ```BufferedReader``` and ```Scanner``` in reading a text file: [http://www.java67.com/2015/06/2-ways-to-read-text-file-in-java-6.html#ixzz4AsBYrO8v](http://www.java67.com/2015/06/2-ways-to-read-text-file-in-java-6.html#ixzz4AsBYrO8v "2 Ways to Read a Text File in Java 6  Read more: http://www.java67.com/2015/06/2-ways-to-read-text-file-in-java-6.html#ixzz4UGMZVBJM")

For the second iteration I will be working on turning this into a GUI to accept a file and allow the user to enter a word they would like to replace and their replacement word. The GUI will then display the resulting text file. 

In the meantime, I will also be going to the second project to create a GUI with two toggle buttons as referenced in my [Day 1](https://seerocode.github.io/Code-Challenge-Day-1/ "Day 1") post.

Let's go, day 5 next!

