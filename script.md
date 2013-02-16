// This is the work-in-progress page that will be the bones of the DIY tutorial on how to be an Open Sourcerer on Github

## What is Open Source
Open Source is a phrase used to describe sharing how you made something. When you show someone on DIY how you made your project, you're open sourcing that project! 

The phrase is most commonly used to refer to code and programing. The code that makes up a project is its **source code** and when you open that source code up to everyone, showing them how the project was made, the code becomes **open source**. 

Open Source projects are great because everyone can learn from each other and everyone can help each other make something really great. 

## Git and Github
Git is a software that helps manage your code. It helps you see the changes that you've made, called *diffs*, and undo changes when you've saved mistakes! Github makes git even easier and social. With Github you can put your code online and share it with others. Users can create new projects and work together on projects. You can help someone thousands of miles away with their project! 

Lot of places use Github for their code and a lot of places open source their code. Here is [DIY's account](https://github.com/diy) - all of our code that runs the website and app is stored on Github and we've made xxx projects open source. The [New York Times](https://github.com/NYTimes), [Facebook](https://github.com/facebook), an [Mojang](https://github.com/Mojang) who make Minecraft are on Github, too. 


### Make a Github Account
1. Visit www.github.com and sign up for a free account. 
2. You can use your DIY avatar as your avatar on Github, here's how:
	1. In another tap, go to your DIY profile page. 
	2. Right-click on your avatar and select "save as" and put the file somewhere you'll remember on your computer.
	3. Now you have a copy of your avatar and can upload it to Github when it asks for an avatar. 

### Exploring Github
> screencast - repository, users, organizations, fork (but we'll talk more about what you can do with files later), explore page, octocat.

> screenshots

REPOSITORY - Typically called "repo" these are projects on Github. 
USERS - everyone on github is a user
ORGANIZATION - Companies have accounts on Github, the users who contribute to their code are typically their employees or others close to the organization.
FORK - A fork is when someone duplicates the repository so that they can use or work on the code on their computer. We'll talk more about this later.

> diagram of repo

OCTOCAT - He's the official mascot of Github and in someways, programing and open source. [Look at all his personalities!](http://octodex.github.com/)

### Explore the Repo
Go to [github.com/diy](http://github.com/diy) and click the repo called Open-Sourcerer. Now you're on the page for this repo. You can see the files inside the repo, the readme.md and see when changes have been made to them, these are called "commits".

> diagram of repo page

### Using Git an Bash
We're going to be copying files from Github, putting them our computer then making changes and then sending them back to Github to store and make available to everyone else. To do this, we'll use **Git** and **Bash**. With these tools we can talk to our computer and Github and tell them both what to do with files. 

### Install Git
1. Visit [git-scm.com](http://git-scm.com) and download the latest version for your operating system.
* In mac, you won't notice anything or see the application installed, but it will install on your computer.
* In windows, hit ok or next for all options, then finish and you don't have to review notes.

### Bash 
In Mac you've already got Bash. If you go to `Launchpad` and search for `Terminal`, this is the application you'll use.

In Windows you got Bash when you installed Git. Go to `Programs > Git` and select `Git Bash`.

We'll refer to both Mac's *Terminal* and Window's *Git Bash* as just *Bash*.

Let's check bash and check our git. In Bash window type:

    git --version

You should have been returned a line that reads version 1.8.1… this means that git was correctly installed and is up and running!

### Configure Git
We need to tell Git who we are, so that when we move files around it knows who is moving them. Type the following lines one at a time into Bash and inside of the quotations add the email you signed up to Github with and your Github username.

    git config --global user.email "yourgithub@email.com"
    git config --global user.name "yourgithubusername"

## Let's Get to Work!
We want to make changes to a file in DIY's Open-Sourcerer repo and sumbit those changes back to DIY so that they can be incorporated into the original. Then everyone will be able to see each others additions and work together to build something.

### Fork
This is how we create a remote copy (that means it's stored on Github.com) of a project on our account that stays linked to the original (because we want our changes to affect this original).

> diagram of what fork is in the git universe

1. Go to [github.com/diy](http://github.com/diy) and click on the repo [Open-Sourcerer](https://github.com/diy/open-sourcerer).
2. Near the top right, click `Fork`. See the animation? This means we're creating a copy of the code onto our account and it will be linked to the original on DIY's account. 

### Clone 
Now that we've forked the files to our Github account, we need to clone (aka copy) them so that we have a local (on our computer) version of the files. Our clone will be linked to our fork which is linked to the DIY original.

At the same time we'll be learning how to use Bash. By typing comands we can tell the computer to the same things that we do by clicking our mouse. 

> diagram of what clone is in the git universe

Open Bash
1. Open a new window in bash, or if all you've done is set up git from earlier, you're fine to use the same window.

Navigate to Folder
2. Let's create a folder that will hold all of our code files. Bash is starting us at the root of our computer, but let's move into our Documents folder.

> Little diagram of dude walking through folder branches?

To move to another folder, we need to *change directories* or **cd**. 

In Macs type:

    cd Documents
    
In Windows type:

    cd My\ Documents/
    
*The slashes let the application know that there is a space between 'My' and 'Documents'*

Now that we're inside the Documents folder, let's create a new folder with **mkdir** - *make directory*, get it?

Type:

    mkdir myCode
    
Great! But we're still inside of the Documents folder, so let's go into myCode:

    cd myCode
    
Now we've made a folder called myCode inside our our Documents folder. Let's put the DIY files in it!

Clone the Repo
3. We want to tell our Git to go to the place on the internet where Github is storing our forked files and clone them to where we are right now inside of the myCode folder. Each repo on github has an address for its location. You'll see it following the HTTP and SSH buttons near the top middle of the page. Click on HTTP, this is the address you'll use. 

**Pro tip** the http address will look like this: https://github.com/YOURUSERNAME/open-sourcerer. If you add your user name and the @ symbol before the word 'github', you won't have to enter it in so much later on. That will make the address look like this: https://YOURUSERNAME@github.com/jllord/open-sourcerer. By default this will be our fork's *origin* and *master branch*. 

[screenshot of SSH addie]()

Type:

    git clone https://github.com/YOURUSERNAME/open-sourcerer

Watch as it copies the files! It will also create a folder for you with the name of the repo. When it's done cloning, move into the repo's folder:

    cd open-sourcerer

Now we're inside our very own copy of the files. Let's use **ls** to *list* the contents of this folder to see what we've got!

    ls

You should see a set of filenames that look exactly like the files you see on the website for both DIY and your account page.

[screenshot of side by side filenames]()

Connect to Original
4. We have one last thing to do. Because this is an open project, we can expect that may others will be doing the same forking and cloning and making changes to the files. We want to make sure we're always working with the most up to date files. To ensure this, we'll connect our local copy to the DIY original so that we can **pull** in the most recent changes before we work on ours. If you go back to the DIY page for Open-Sourcerer, you'll see the HTTP address in the near the top middle: https://github.com/diy/open-sourcerer. We're going to name this connection *upstream*.

> should they type in their username@ here too?

Type

    git remote add upstream https://github.com/diy/open-sourcerer
    
Pull
5. Before we make any additions, we want to make sure we have the latest files by pulling in any changes from the *master* branch *upstream*.

Type

    git pull upstream master

If it says 'Already up to date' then no changes have been made since you started setting up! If there were changes, it updated your files. In both cases, your files matcht the files on DIY's Github.

### Edit the File
Now let's add our part to the story! We can open up a file from Bash.

Type

    open collaborative-story.txt
    
It should open up the file in your computer's text editor. Add your own portion of the story after the last sentence.

I'll wait... 

When you're done, save the file. Make sure you keep it saved as a .txt file. 

### Push Changes
Now let's add our changes to our fork and then submit them to be added to the DIY original file. 

Return to Bash and let's check what changes we've made. Type

    git status
 
> screenshot

This shows you what files you've made changes to - it should say collaborative-story.txt. Let's see the *difference* before and after our changes with **diff**. 

    git diff
    
> screenshot

You'll see a plus and minus sign showing the before and after.

Add Changes
Tell Git what file you want to add.

    git add collaborative-story
    
**Pro tip** if you have multiple files and want to add them all, you'll type `git add .` The period means 'all'.

Commit Changes
Now we'll add a *message* describing our changes and attach that to our push.

    git commit -m "your description"
    
Push Changes to our Fork
Now, finally, we'll actually push our file and message to our fork on Github. 

    git push origin master
    
Pull Request
Now our local (computer) version and our fork on Github match. Let's submit our changes to DIY to be added to the original. We're **requesting** they **pull** our changes into their files.

You do this part online. If you go to your forked version on Gituhub's website, you'll see a button near the top right `Pull Request`, click this.

> screenshot

You'll be taken to a page that shows DIY's original on the left and your Fork on the right. Fill out the form to describe to DIY what it is you're suggesting they add and then click `Send pull request`.

Now DIY staff will get an alert of your request, be able to see your changes and merge them into the original. Now when the next user forks or pulls and update of this repo, they'll get your updates too!

> screenshot

WOW! You've just forked, pulled, pushed and pull requested like an open source programming pro!

This walk through was long, but we did a lot of setting up. Now, if you wake up one day with some story inspiration, all you need to do is use Bash navigate back to your folder and pull any updates that have been made since you last checked the files:

    git pull upstream master

Then open up the text file and make changes. Save your changes and then:

    git push origin master
    
Next, go to your Github page for the repo and select Pull Request. You've done it again!





# Dictionary

* Git
* Github
* Open Source
* Repository
* Fork
* Push
* Pull
* Clone
* cd
* mkdir
* open
* 

 

	

