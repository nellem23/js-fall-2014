## First Homework Assignment

This is your first assignment, and its very important. In this class we're going to be writing Javascript programs. In the beginning you'll be required to submit exercises each week. Rather than email we're going to use a tool called Github to share our work. Github is a website that programmers use to share and colloborate on code. At first, its going to feel like a lot of extra work, but this is a skill as important as learning Javascript syntax and semantics. In fact, among the designers I work with, knowing Git is a pre-requisite, something to include on your resume. There are two parts of this exercise:

- We'll learn how to use the computer's terminal (command line) interface.
- Then you'll learn how to create a "fork" or our class Github repository.

Since we're not meeting the first week, and our second class falls on Labor Day, you have a long time to complete it. But you also won't have much guidance. Please go carve out plenty of time and go through this document slowly. 

If you feel overwhelmed, step away and come back to it, ask one of your classmates for help, use google to search for answers or send me an email.

### Using The Command Line

You're all familiar with manipulating files and folders (directories) on your computers using their graphical interfaces (GUI). Almost every computer system also provides a text-only interface. Just as you can copy, move, create and delete files using your computers graphical interface, you can perform these actions via the command line. Using the command line can take some time to get used to, but the work pays off. Here we're just going to go through some basics. In many ways it will feel less efficient than using your computer's GUI. But the command line provides us the most direct access to Git. The following instructions are for __Mac OS__. You can perform all these operations on a Windows computer, but they're different. If you use a Window's computer, I would try to perform this part of the exercise on a lab computer. 

- Create a folder (directory) on your Desktop, called `command-line`
- Open it in Finder and resize it so it takes up the right half of your screen.
- Open Terminal.app (type command+space and type Terminal to find it in spotlight) and resize it so it takes up the left half of your screen.

Your colors and fonts might be different, but it should look like something like this:

![screen shot](https://github.com/miniatureape/js-fall-2014/raw/master/assets/images/command-line-setup.png "Screenshot of command line setup")

- Type `cd ~/Desktop/command-line`

Commands have a few parts. Here `cd` is the command name. The second part is its 'argument.' With this command you're telling the terminal to change directory to the directory you just made.

In order to __print__ your __working directory__ is, type the command `pwd`. 

- In order to __list__ what's in the current directory, type the command `ls`. Since there are no files in this directory, the command won't print anything. Let's change that.
- To create new empty file, we can use the command `touch`. Touch creates a file with whatever name you supply it. Try entering `touch my-new-file.txt` into the terminal. You should notice a new file appear in your Finder.
- Try typing `ls` now. You should see the name of your new file.
- In Finder, open this file using a text editor such as Sublime or Text Wrangler. Enter a sentence or two of text and save it.
- Back in terminal, type `cat my-new-file.txt`. You should see the text you entered printed on the screen. The `cat` command prints out the contents of a file.
- Press the up arrow in your terminal, you should see the command you just entered. Play with the up and down arrows and you'll notice you can move backwards and forwards through the commands you've entered. Press down until you have an empty terminal again.
- Type `clear` in the terminal. It clears all of the text that's been printed so far. Use it whenever you want a fresh slate.
- Create another by typing `touch another-file.txt` and then another by typing `touch yet-another.txt`.
- You can also create a __copy__ of a file. Try entering `cp another-file.txt another-file-2.txt`. 

Notice that this command takes two arguments. The first argument is the name of the file to copy, the second argument is the name of the new file.

- Type `ls` again to see your new files. So you can create a file, now let's __remove__ one. Type `rm my-` and then hit the tab key. You'll notice that terminal completes the name of the file. Hit enter. You should notice your file disappear. It's gone forever. It's not in the trash. It's just gone.
- Now let's delete all the files you've created. All the files you've created have the ending `.txt`. It would be nice if we could use this fact to avoid typing each filename. The terminal lets us use wildcards for this. Try typing `rm *.txt`. You'll notice all the files are gone.

Lets say you want to move to the Desktop. There are a few ways to do this. Remember when you typed `pwd`. It printed out the complete path to your directory. You could grab the first part of this (everything up to and including Desktop) type `cd /home/<yourname>/Desktop`. Or you can use the special directory name `..` which means __the parent directory__. Let's use that.

- Type `cd ..`. Then type `pwd`. You've moved up a directory to the desktop.
- Type `ls` uo list all the files on your desktop. You may have a lot, but you should be able to see your `command-line` directory. 

Let's create another directory, but this time we'll use the command line.

- Type `mkdir command-line-2`. Now you have another folder on your desktop. Finally, lets delete them both:
- Type `rm -rf command-line-*`

This time, the command is a little different. There is the `-rf` part. That tells the computer to delete not just these directories, but anything inside of them. 

There are many more things you can do with the terminal and we'll see some more things throughout the class. But for now you know the basics. Feel free to play around, but be careful with commands like `rm`. 

Note that you can learn more about almost any built-in command by using the `man` (manual) command. Try `man rm` and read about the r and f options.


### Getting Started with Git and Github.

Each week, you'll be submitting work by uploading it to a website called Github.com. Github is a popular site used by programmers to colloborate on code. It's based on Git, a piece of __version control software__. 

If you don't know what that is, that's ok. You know when you're working on a Photoshop file and you want to make a new copy, but you
think you might still want to keep around your old changes, so you save as and name it something like _final-project-new-jan-11th-really-the-latest-2.psd_? Programmers don't like to that.
It gets to confusing to figure out what the actual new version is. So we use a version control tool to keep around all the old versions. They're tucked away, out of site, but available. Git is one of these tools.

Git can be pretty daunting even to seasoned professionals. But our use will be pretty basic. Before you get started, here are some terms:

#### Glossary

Below are a few terms. You can read more extensive descriptions on [Github](https://help.github.com/articles/github-glossary).

##### Repository (Repo):
A single git project. It can contain multiple folders and files, exist on many computers. There is a copy of the repo for this class at https://github.com/miniatureape/js-fall-2014. I also have a local copy on my computer. You can clone it yourself and have your own copy. when you do, you have the complete project history.

##### Adding:
In order for git to track a file, you have to 'add' it to the repo. Otherwise it will ignore it.

##### Commit:
A change or set of changes you've made to one or more files.

##### Pushing:
To move the code from your computer where you're working to a central repo to share with others, you 'push' your code.

#### Example workflow.

You have a new project you're about to start. First you create a git repo to track files. Then you create a file, _index.html_. You're ready to save this work, so you add this file to the repo and commit file. You also want to share it with the world, so you push it to your remote repo. 

You decide there are a few changes you'd like to make so you edit your file. When you have completed the edits, you commit again. Then you decide you need a new file _main.css_ so you create it and add it to the repo. Now you want to share this new file and all your changes so you push again.

Your assignment for this week:

- Create an account on github.com (They have paid accounts, but a free one is just fine).
- [Install and setup](https://help.github.com/articles/set-up-git) git on your computer. Do steps 1-4 here.
- Navigate to the [class repository](https://github.com/miniatureape/js-fall-2014).
- Click the __Fork__ button.

![screen shot](https://github.com/miniatureape/js-fall-2014/raw/master/assets/images/fork-btn.png "Screen shot of github showing fork button")

When you click the fork button, it takes my repository and creates a copy under your account. Now you have a full copy of all the class files under your account on github. To actually work on them or make changes, you need to copy them to your computer. To do this, make sure your on your copy of the repo at Github (It should be at https://github.com/<YOUR GITHUB USERNAME>/js-fall-2014), find the clone url.

![screen shot](https://github.com/miniatureape/js-fall-2014/raw/master/assets/images/clone-link.png "Screen shot of github showing clone link")

- https://help.github.com/articles/creating-a-new-repository
- https://help.github.com/articles/adding-repositories-with-github-for-windows

If you're not afraid of your computer's terminal, skipping the github GUI is fine. You can work on the command line if you wish.

I know this is a lot to take in without any instruction, but remember, you have two weeks to complete this because we don't meet the first two Mondays. If you're having trouble, reach out to your fellow students, the internet at large or me. You will have completed this assignment if:

- You have a github account
- You have a local repository (doesn't matter what's in it).
- You have pushed the local repository to github.