---
layout: post
title: Upload Your Codenvy Project to Github
---

Lots of steps at first but once it's set up, all you need to do is commit and push whenever you make changes. Here we go.

1. Go to Profile > Preferences
![CodenvyGHSetUp-1.PNG](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/CodenvyGHSetUp-1.PNG)

2. Click on Committer from the left-side bar and type in your Github username and e-mail address. Click Save
![CodenvyGHSetUp-9.PNG](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/CodenvyGHSetUp-9.PNG)

3. Click on VCS under SSH on the left-side bar and click on the Octocat Github icon on the bottom-right and click OK to generate an SSH key
![](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/CodenvyGHSetUp-2.PNG)
![](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/CodenvyGHSetUp-3.PNG)

4. Click View under Public Key to view and copy the SSH key that was generated for Github
![CodenvyGHSetUp-4.PNG](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/CodenvyGHSetUp-4.PNG)

5. Go to your [Github settings](https://github.com/settings/keys "Github settings") and click SSH and GPG Keys from the left sidebar

6. Click New SSH key on the top-right and paste the public key generated from Codenvy. Choose a relevant title like "Codenvy SSH Key" and click Add SSH Key. You will be asked to enter your password again.
_NOTE: You may receive a "Key is already in use" message if you already log into Codenvy using your Github authentication_

7. Github is now connected to your Codenvy environment and can communicate securely. If you haven't created a repo in Github already for your project, go ahead and do so now.

8. Go back to Codenvy and initialize a repository by going to Git > Intitialize Repository...
![CodenvyGHSetUp-5.PNG](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/CodenvyGHSetUp-5.PNG)

9. Then, add your remote Github repo by going to Git > Remotes... > Remote 
![CodenvyGHSetUp-6.PNG](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/CodenvyGHSetUp-6.PNG)

10. Click Add and type in the name of your Github repo and the location of your repo which should be the SSH address
![CodenvyGHSetUp-7.PNG](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/CodenvyGHSetUp-7.PNG)

11. If you initialized your repo with any files like a README, pull them in by going to Git > Remote > Pull.
You should see any new files in your project folder

12. Highlight all of your files in your project folder and commit your addition/changes by going to Git > Commit and click Add selected files

13. Push your changes to your repo by going to Git > Remotes... > Push. You should now see your changes in your repo!

You can also work in the terminal as I'm used to by navigating to the Terminal tab under your Processes pane

![CodenvyGHSetUp-10.PNG](https://raw.githubusercontent.com/seerocode/seerocode.github.io/master/_posts/CodenvyGHSetUp-10.PNG)

Let me know if I missed anything or it seems confusing. 
Still working on day 5, stay tuned!
