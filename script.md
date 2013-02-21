// This is the work-in-progress page that will be the bones of the DIY tutorial on how to be an Open Sourcerer on Github

## What is Open Source
Open Source is a phrase used to describe sharing how you made something. When you show someone on DIY how you made your project, you're open sourcing that project! 

The phrase is most commonly used to refer to code and programing. The code that makes up a project is its **source code** and when you open that source code up to everyone, showing them how the project was made, the code becomes **open source**. 

Open Source projects are great because everyone can learn from each other and everyone can help each other make something really fantastic. 

## Git and Github

![simply git](http://diy-visualpedia.s3.amazonaws.com/git-graphic-01.png)

Git is software that helps manage your code. It allows you see the changes that you've made, called *diffs*, and undo changes when you've saved mistakes! Github makes Git even easier and social. With Github you can put your code online and share it with others. Users can create new projects and work together on projects -- making something better, together. 

Lots of places use Github for their code and a lot of places open source their code. Here is [DIY's account](https://github.com/diy) - all of our code that runs the website and app is stored on Github and we've made xxx projects open source. The [New York Times](https://github.com/NYTimes), [Facebook](https://github.com/facebook), an [Mojang](https://github.com/Mojang) who make Minecraft are on Github, too. 

Oh, and Github has a cool mascot, Octocat, check out all the [personalities](http://octodex.github.com/)!


### Make a Github Account
1. Visit www.github.com and sign up for a free account. 
* You'll need an email address to create an account. 

### Exploring Github
Since you've just joined Github, there won't be much on your account page. Let's have a look at DIY's page. Go to [www.github.com/diy](www.github.com/diy). 

> screencast - repository, users, organizations, fork (but we'll talk more about what you can do with files later), explore page, octocat.

![github organization page](http://diy-visualpedia.s3.amazonaws.com/github-org-page-01.png)

1. **Users** Everyone on Github is a user. Some users belong to organizations.
2. **Organization** Organizations have accounts on Github, the users who contribute to their code are called **members** and typically are employees or others close to the organization.
3. **Repository** These are projects on Github, they contain all the project's instructions and files. Often people say "repo," short for repository. Public repos are open source! 

On pages that list repos such as an organization's page, you can quickly see the language used in the repo, the number of favorites the repo has and how many people have forked a copy of the repo (we'll talk more about forking later). 

![github repo](http://diy-visualpedia.s3.amazonaws.com/github-repo-01.png)
> Elements of a repository when shown in a list

### Explore the Repo
Go to [github.com/diy](http://github.com/diy) and click the repo called Open-Sourcerer. Now you're on the page for this repo. You can see the files inside the repo, the readme.md and see when changes have been made to them, these are called *commits*.

![diy repo](http://diy-visualpedia.s3.amazonaws.com/repo-page-dia-01.png)
> Parts of a repository's page


### Using Git and Bash
We're going to be copying files from Github, putting them our computer, making changes to them and then sending them back to Github to store and make available to everyone else. To do this, we'll use **Git** and **Bash**. With these tools we can talk to our computer and Github and tell them both what to do with files. 

### Install Git
*A few of the steps may require your computer's password if one is set*

1. Visit [git-scm.com](http://git-scm.com) and download the latest version for your operating system.
* In Mac, you won't notice anything or see the application installed, but it will install on your computer.
* In Windows, hit *Ok* or *Next* for all options, then finish (you don't have to review notes).

### Bash 
![mac terminal icon](http://diy-visualpedia.s3.amazonaws.com/mac-terminal.png)

In Mac you've already got Bash. If you go to your `Launchpad` and search for `Terminal`, this is the application you'll use.

![windows git bash icon](http://diy-visualpedia.s3.amazonaws.com/git-bash-icon.png)

In Windows you got Bash when you installed Git. Go to `Programs` > `Git` and select `Git Bash`.

We'll refer to both Mac's *Terminal* and Window's *Git Bash* as just *Bash*.

> screenshot of both a terminal and git bash window

Let's check our git in Bash. In the Bash window type:

    git --version

You should have been returned a line that reads version 1.8.1… this means that git was correctly installed and is up and running!

![git --version](http://diy-visualpedia.s3.amazonaws.com/git-version.png)

### Configure Git
We need to tell Git who we are so that when we move files around it knows who is moving them. Type the following lines one at a time into Bash and inside of the quotations add the email you signed up to Github with and your Github username.

    git config --global user.email "yourgithub@email.com"
    git config --global user.name "yourgithubusername"
    
![git config](http://diy-visualpedia.s3.amazonaws.com/git-config.png)

## Let's Get to Work!
DIY has a repo with a story in it, we need everyone to help complete the story by adding parts to it.

### Fork
First we create a **remote** copy (that means it's stored on Github.com) of a project on our account that stays linked to the original (because we want our changes to affect this original). This is called a **fork**

1. If you're not already there, go to [github.com/diy](http://github.com/diy) and click on the repo [Open-Sourcerer](https://github.com/diy/open-sourcerer).
2. Near the top right, click `Fork`. See the animation? This means we're creating a copy of the code onto our account that will be linked to the original on DIY's account. 

![forking](http://diy-visualpedia.s3.amazonaws.com/repo-fork.png)

### Clone 
Now that we've forked the files to our Github account, we need to **clone** (aka copy) them so that we have a local (on our computer) version of the files (this means we can work on them while offline). Our clone will be linked to our fork which is linked to the DIY original.

As we do this, we'll also be learning how to use Bash. By typing comands, we can tell the computer to do the same things that we do by clicking our mouse. 

### Open Bash
1. Open a new window in bash, or if all you've done is set up git from earlier, you're fine to use the same window.

### Navigate to Folder
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
    
Now we've made a folder called myCode inside our Documents folder. Let's put the DIY files in it!

### Clone the Repo
3. We want to tell Git to go to the place on the internet where Github is storing our forked files and clone them to where we are right now inside of the myCode folder. Each repo on github has an address for its location. You'll see it following the HTTP and SSH buttons near the top middle of the page. Click on HTTP, this is the address you'll use. 

**Pro tip** the http address will look like this: https://github.com/YOURUSERNAME/open-sourcerer. If you add your user name and the @ symbol before the word 'github', you won't have to enter it in so much later on. That will make the address look like this: https://YOURUSERNAME@github.com/YOURUSERNAME/open-sourcerer. By default our fork's name is *origin* and it is on the *master branch*. 

> screenshot of SSH addie

Type:

    git clone https://github.com/YOURUSERNAME/open-sourcerer

Watch as it copies the files! It will also create a folder for you with the name of the repo. When it's done cloning, move into the repo's folder:

    cd open-sourcerer

Now we're inside our very own copy of the files. Let's use **ls** to *list* the contents of this folder to see what we've got!

    ls

You should see a set of filenames that look exactly like the files you see on the website for both DIY and your account page.

> screenshot of side by side filenames

### Connect to Original
4. We have one last thing to do. Because this is an open project, we can expect that may others will be doing the same as us: forking and cloning and making changes to the files. We want to make sure we're always working with the most up to date files. To ensure this, we'll connect our local copy to the DIY original so that we can **pull** in the most recent changes before we work on ours. If you go back to the DIY page for Open-Sourcerer, you'll see the HTTP address in the near the top middle: https://github.com/diy/open-sourcerer. We're going to name this connection *upstream*.

> should they type in their username@ here too?

Type

    git remote add upstream https://github.com/diy/open-sourcerer
    
### Pull Changes
5. Before we make any additions, we want to make sure we have the latest files by pulling in any changes from the *master* branch *upstream*.

Type

    git pull upstream master

If it says 'Already up to date' then no changes have been made since you started setting up! If there were changes, it updated your files. In both cases, your files will match the files on DIY's Github.

### Edit the File
Now let's add our part to the story! We can also open up a file from Bash.

Type

    open collaborative-story.txt
    
It should open up the file in your computer's text editor. Add your own portion of the story after the last sentence.

> screenshot of how to add a portion

I'll wait... 

When you're done, save the file. Make sure you keep it saved as a .txt file. 

### Push Changes
Now let's add our changes to our forked copy and then submit them to be added to the DIY original file. 

Return to Bash and let's check what changes we've made. Type

    git status
 
> screenshot

This shows you what files you've made changes to - it should say `collaborative-story.txt`. Let's see the *difference* before and after our changes with **diff**. 

    git diff
    
> screenshot

You'll see a plus and minus sign showing the before and after.

Add Changes
Tell Git what file you want to add.

    git add collaborative-story
    
**Pro tip** if you have multiple files and want to add them all, you'll type `git add .` The period means *all*.

### Commit Changes
Now we'll add a *message* describing our changes and attach that to our push.

    git commit -m "your description of changes"
    
### Push Changes to our Fork
Now, finally, we'll actually push our file and message to our fork on Github. Remember our fork's name is origin (it's our *original* file) and the branch is *master*.

    git push origin master
    
### Pull Request
Now our local (computer) version and our fork on Github match. Let's submit our changes to DIY to be added to the original. We're **requesting** they **pull** our changes into their files.

You do this part online. If you go to your forked version on Gituhub's website, you'll see a button near the top right `Pull Request`, click this.

> screenshot

You'll be taken to a page that shows DIY's original on the left and your fork on the right. Fill out the form to describe to DIY what it is you're suggesting they add and then click `Send pull request`.

Now DIY staff will get an alert of your request, be able to see your changes and merge them into the original. Now when the next user forks or pulls and update of this repo, they'll get your updates too!

> screenshot

WOW! You've just forked, pulled, pushed and pull requested like an open source programming pro!

This walk through was long, but we did a lot of setting up. Now, if you wake up one day with some story inspiration, all you need to do is use Bash to navigate back to your folder and pull any updates that have been made since you last checked the files:

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
* Commit

 

    

