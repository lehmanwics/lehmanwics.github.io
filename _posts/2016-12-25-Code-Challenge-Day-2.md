---
layout: post
title: 30DaysOfCode - Day 2
excerpt_separator: <!--more-->
---

Merry Christmas everyone! 

Today marks day 2 of the 30DaysOfCode challenge. Yesterday I spent the better part of the morning setting up this Jekyll blog and working my way through markdown. I've got the basics down right now which should get me through these posts.

I watched TheNewBoston video I posted about yesterday along with some other videos that seemed a lot more helpful. Specifically, [Nathan Schutz](https://www.youtube.com/channel/UCbJnFSkT67nSK2oxQjoKvRg "Nathan Schutz Youtube Channel") 5-part Reading Java Files series here: [https://www.youtube.com/watch?v=YXpgcRa7_sg](https://www.youtube.com/watch?v=YXpgcRa7_sg "5-part Reading Java Files series")

I appreciated that he carefully explained what he was coding and how it worked. After watching a few more videos, I started testing this out. First, I wanted to make sure the file worked so I didn't start coding and wondering why the heck my methods were failing.

To do so, I first imported the ```java.io.*``` package to use classes like ```File``` later. I also imported the Java utility package as a precaution because I will need to use ```Scanner``` class and others later. 

This is the start of my class so far:
<!--more-->
![Start of Class](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/Fello--StartOfClass.PNG)

Plain and simple! I will need to add an IOException to the main class and I will show that later.

**Note:** I am using [Codenvy.io](Codenvy.io "Codenvy") here since I forgot my laptop at home and am not allowed to download software onto my work computer. =/ 

Next, I created a new object from the ```File``` class. I am calling the object ```file``` and passing my hello.txt file that hold's lyrics to Adele's _Hello_. The file lives in the project folder.

I call the ```File.exists()``` method on my ```file``` object to check if my program is able to locate the file. This method returns a boolean value and this is what I get:

![Testing File Object](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/Fello--TestingFileObject.PNG)

Womp Womp.

So very few lines of code and it looks right but I know I am doing something wrong. I am going to check in Eclipse to make sure it's not just Codenvy's file structure not reading the file correctly although I did try to create the fil in the root of the project folder and that did not work either. Still returned a ```false``` value.

I will be spending time with my family for Christmas after I am out of work and will hopefully have some time in the evening to figure this out.

Until tomorrow! 









