## What is Open Source
Open Source is a phrase used to describe sharing how you made something. When you show someone on DIY how you made your project, you're open sourcing that project! 

The phrase is most commonly used to refer to code and programing. The code that makes up a project is its *source code* and when you open that source code up to everyone, showing them how the project was made, the code becomes *open source*. 

Open Source projects are great because everyone can learn from each other and everyone can help each other make something really great. 

## Git and Github
Git is a software that helps manage your code. It helps you see the changes that you've made, called *diffs*, and undo changes when you've saved mistakes! Github makes git even easier and social. With Github you can put your code online and share it with others. Users can create new projects and work together on projects. You can help someone thousands of miles away with their project! 

Lot of places use Github for their code and a lot of places open source their code. Here is [DIY's account](https://github.com/diy) - all of our code that runs the website and app is stored on Github and we've made xxx projects open source. The [New York Times](https://github.com/NYTimes), [Facebook](https://github.com/facebook), an [Mojang](https://github.com/Mojang) who make Minecraft are on Github, too. 


## Make a Github Account
1. Visit www.github.com and sign up for a free account. 
2. You can use your DIY avatar as your avatar on Github, here's how:
		1. In another tap, go to your DIY profile page. 
		2. Right-click on your avatar and select "save as" and put the file somewhere you'll remember on your computer.
		3. Now you have a copy of your avatar and can upload it to Github when it asks for an avatar. 

## Exploring Github
[screencast] - repository, users, organizations, fork (but we'll talk more about what you can do with files later), explore page, octocat.

[screenshots]
REPOSITORY - Typically called "repo," these are projects on Github. 
USERS - everyone on github is a user
ORGANIZATION - Companies have accounts on Github, the users who contribute to their code are typically their employees or others close to the organization.

[diagram of repo] 
OCTOCAT - He's the official mascot of Github and in someways, programing and open source. [Look at all his personalities!](http://octodex.github.com/)

### Explore the Repo
Go to github.com/diy and click the repo called Open-Sourcerer. Now you're on the page for the page for this repo. You can see the files inside the repo, the readme.md and see when changes have been made to them, these are called "commits".

## Now Let's Make Stuff
We're going to be copying files from Github, putting them our computer and making changes and then sending them back to Github to store and make available to everyone else. To do this, we'll use Git and Bash. With these tools we can talk to our computer and Github and tell them both what to do with files. 

## Install Git
1. Visit (git-scm.com)[http://git-scm.com] and download the latest version for your operating system.
- (in mac, you won't notice anything or see the application installed, but it will install on your computer)
- (in windows, hit ok or next for all options, then finish and you don't have to review notes)

## Bash 
In Mac, you've already got Bash. If you go to Launchpad and search for Terminal, this is the application you'll use.

In Windows, you'll got Bash when you installed Git. Go to Programs > Git and select Git Bash.

I'll refer to both Mac's Terminal and Window's Git Bash as just Bash.

Let's check bash and check our git. In Bash type:

git --version

You should have been returned a line that reads version 1.8.1… this means that git was correctly installed and is up and running!

### Fork
This is how we create a remote copy of a project that stays linked to the original.

FORK - A fork is when someone duplicates the repository so that they can use or work on the code on their computer.

1. Go to github.com/diy and click on Open-Sourcerer
2. Near the top right, click Fork. These means we're creating a copy of the code on our account that is linked to the original on DIY's account. 
[illustration of a fork] Fork it to your account.

### Clone 
This is how we get a local (on our computer) copy of the project that's linked to our remote fork.

1. Near the top left, click 'Clone in Mac' (or Windows). 
2. Select a place on your computer to keep your code files! 

You now have a copy of the files on your computer. The Github App also now shows you that you have this repo. Since we just cloned it, we know it's pretty up to date. But what if someone just added a change - just right now? Before we work on it, we should make sure we *pull* the most up-to-date version from Github. Do this by Selecting 'Repository' from the m

### Edit the File
1. On your computer, navigate to where you cloned the folder, it should be called Open-Sourcerer.
2. Open the folder, inside you'll see the same files we saw on the github website. 
3. Open collaborative-story.txt in a text editor, like Text Edit (on Mac) or Notepad or Word (in Windows). 
4. Now add something to the story! 
5. When you're done, save the file. Make sure it stays saved as a .txt file. 

 

	

