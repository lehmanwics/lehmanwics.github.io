---
layout: post
title: Upload Your Codenvy Project to Github
---

Lots of steps at first but once it's set up, all you need to do is add, commit, and push whenever you make changes. Here we go.

1. Go to Profile > Preferences
![CodenvyGHSetUp-1.PNG](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/CodenvyGHSetUp-1.PNG?token=AJ_rZJTr3GC7AfvqW3v5o0X6lPuHKgQvks5Yd5S2wA%3D%3D)

2. Click on Committer from the left-side bar and type in your Github username and e-mail address. Click Save
![CodenvyGHSetUp-9.PNG](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/CodenvyGHSetUp-9.PNG?token=AJ_rZJOC7JXxk7jZO9eJ2qtiL0ITk5_Pks5Yd5TLwA%3D%3D)

3. Click on VCS under SSH on the left-side bar and click on the Octocat Github icon on the bottom-right and click OK to generate an SSH key
![](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/CodenvyGHSetUp-2.PNG?token=AJ_rZH8XEsdH2qgEndL90qiLkdCjcOPSks5Yd5TewA%3D%3D)
![](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/CodenvyGHSetUp-3.PNG?token=AJ_rZLKIumR5H9BXv43tyfMIgDQvYgT4ks5Yd5TvwA%3D%3D)

4. Click View under Public Key to view and copy the SSH key that was generated for Github
![CodenvyGHSetUp-4.PNG](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/CodenvyGHSetUp-4.PNG?token=AJ_rZF_DotoIAfa4xuJsXHuiJ5-lWxHZks5Yd5T_wA%3D%3D)

5. Go to your [Github settings](https://github.com/settings/keys "Github settings") and click SSH and GPG Keys from the left sidebar

6. Click New SSH key on the top-right and paste the public key generated from Codenvy. Choose a relevant title like "Codenvy SSH Key" and click Add SSH Key. You will be asked to enter your password again.
_NOTE: You may receive a "Key is already in use" message if you already log into Codenvy using your Github authentication_

7. Github is now connected to your Codenvy environment and can communicate securely. If you haven't created a repo in Github already for your project, go ahead and do so now.

8. Go back to Codenvy and initialize a repository by going to Git > Intitialize Repository...
![CodenvyGHSetUp-5.PNG](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/CodenvyGHSetUp-5.PNG?token=AJ_rZE3S7tWKpJfLzCUyrkMey-pI4_mNks5Yd5UOwA%3D%3D)

9. Then, add your remote Github repo by going to Git > Remotes... > Remotes 
![CodenvyGHSetUp-6.PNG](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/CodenvyGHSetUp-6.PNG?token=AJ_rZIoFN43gSxLLwhccaIfQIaGxcovbks5Yd5UewA%3D%3D)

10. Click Add and type in the name of your Github repo and the location of your repo which should be the SSH address
![CodenvyGHSetUp-7.PNG](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/CodenvyGHSetUp-7.PNG?token=AJ_rZP2GWanGHtman2wj-iuNraMqrujaks5Yd5UswA%3D%3D)

11. If you initialized your repo with any files like a README, pull them in by going to Git > Remote > Pull.
You should see any new files in your project folder

12. Highlight all of your files in your project folder and commit your addition/changes by going to Git > Commit and click Add selected files

13. Push your changes to your repo by going to Git > Remotes... > Push. You should now see your changes in your repo!

You can also work in the terminal as I'm used to by navigating to the Terminal tab under your Processes pane

![CodenvyGHSetUp-10.PNG](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/CodenvyGHSetUp-10.PNG?token=AJ_rZEwmRFmkCM7vQ4j-2MY2TC9VA_g9ks5Yd5U6wA%3D%3D)

Let me know if I missed anything or it seems confusing. 
Still working on day 5, stay tuned!
