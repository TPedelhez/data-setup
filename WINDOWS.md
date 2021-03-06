# Setup instructions

The following instructions will help you to get ready for [Le Wagon](http://www.lewagon.com) Data Bootcamp:

- Install Python via Anaconda (a distribution for the Data Scientist)
- Install a text editor, where you'll spend your day and nights
- Setup your terminal
- Setup git and GitHub


# Anaconda

Anaconda is the world's most popular data science platform.

Go to [anaconda's website](https://www.anaconda.com/distribution/) and click on "Windows" then "Download" under Python 3.7 version.

![](images/anaconda_1.png)

A little popup will appear at the bottom of the page, click on "Run".

![](images/anaconda_2.png)

A new window will appear, it is the Anaconda3 installer. Click on "Next".

![](images/anaconda_3.png)

Accept the License Agreement by clicking on "I Agree".

![](images/anaconda_4.png)

Click on "Next".  

![](images/anaconda_5.png)

Leave the default installation location, click on "Next".

![](images/anaconda_6.png)

Check "Add Anaconda to my PATH environment variable" and click on "Install"  

![](images/anaconda_7.png)

When it says "Completed", click on "Next".  

![](images/anaconda_8.png)

Click on "Next".  

![](images/anaconda_9.png)

Finally, uncheck the two options and click on "Finish".

![](images/anaconda_10.png)

Anaconda3 is now installed!


# Sublime Text 3 - Your text editor

A text editor is one of the most important tools of a developer.

Go to [Sublime's website](https://www.sublimetext.com/) and click on "Download for Windows"  

![](images/sublime_1.png)

A little popup will appear at the bottom of the page, click on "Run".  

![](images/sublime_2.png)

A new window will appear, it is the Sublime Text 3 installer. Click on "Next".  

![](images/sublime_3.png)

Click on "Next".  

![](images/sublime_4.png)

Click on "Install".  

![](images/sublime_5.png)

Click on "Finish".  

![](images/sublime_6.png)





# Github account

Have you signed up to Github? If not [do it right away](https://github.com/join).  

:point_right: **[Upload a picture](https://github.com/settings/profile)** and put your name correctly on your Github account. This is important as we'll use an internal dashboard with your avatars. please do it **now**.

# Git Bash

Git bash will allow you to run some linux command on Windows.
Go to [Git-SCM](https://git-scm.com/download/wim) and click on "Windows".

![](images/gitbash_1.png)

Click on "Next".

![](images/gitbash_2.png)

Leave the default installation folder and click on "Next".

![](images/gitbash_3.png)

Leave the default components qnd click on "Next".

![](images/gitbash_4.png)

Leave the default name "Git" and click on "Next".

![](images/gitbash_5.png)

In the dropdown, choose your new favorite text editor "Use Sublime Text as Git's default editor" and click on "Next".

![](images/gitbash_6.png)

Click on "Next".

![](images/gitbash_7.png)

Once again, click on "Next".

![](images/gitbash_8.png)

Guess what? Click on "Next" :)

![](images/gitbash_9.png)

"Nexttttt!".

![](images/gitbash_10.png)

"Again!".

![](images/gitbash_11.png)

And again! Just kidding, click on "Install".

![](images/gitbash_12.png)

Lastly, check "Launch Git Bash", uncheck "View Releave Notes" and click on "Finish".

![](images/gitbash_13.png)

The Git Bash terminal should open.

![](images/gitbash_14.png)

Please run the following command:

```bash
curl -Ls https://raw.githubusercontent.com/lewagon/data-setup/master/.bash_profile > .bash_profile
exit
```

Reopen Git bash and run the following command:

```bash
conda init bash
```

Then run this one:

```bash
conda activate base
```

Let's install two tools will need to tests our Python code ;)

```bash
pip install pytest pylint ipdb
```

If you have an error, try the same command again replacing `pip` with `conda`. Otherwise, please ask a TA.

To make sure Python is properly installed, please run the following command:

```bash
python -i
```

You should get an answer like
```bash
Python 3.7.3 (default...
```

To exit this check please run
```bash
exit()
```


# Github

We need to generate SSH keys which are going to be used by Github
to authenticate you. Think of it as a way to log in, but different from the
well known username/password couple. If you already generated keys
that you already use with other services, you can skip this step.

Open a Git Bash terminal and type this, replacing the email with **yours** (the
same one you used to create your GitHub account). It will prompt
for information. Just press enter until it asks for a **passphrase**.

```bash
mkdir -p ~/.ssh && ssh-keygen -t ed25519 -o -a 100 -f ~/.ssh/id_ed25519 -C "TYPE_YOUR_EMAIL@HERE.com"
```

**NB:** when asked for a passphrase, put something you want (and that you'll remember),
it's a password to protect your private key stored on your hard drive. You'll type,
nothing will show up on the screen, **that's normal**. Just type the passphrase,
and when you're done, press `Enter`.

Then you need to give your **public** key to GitHub. Run:

```bash
cat ~/.ssh/id_ed25519.pub
```

It will prompt on the screen the content of the `id_ed25519.pub` file. Copy that text,
then go to [github.com/settings/ssh](https://github.com/settings/ssh). Click on
**Add SSH key**, fill in the Title with your computer name, and paste the **Key**.
Finish by clicking on the **Add key** green button.

To check that this step is completed, in the Git Bash terminal run this. You will be
prompted a warning, type `yes` then `Enter`.

```bash
ssh -T git@github.com
```

If you see something like this, you're done!

```bash
# Hi --------! You've successfully authenticated, but GitHub does not provide shell access
```

Lastly, we need to set your `git` identity. In bash, type the following (**Don't blindly copy/paste it!**)

```bash
git config --global user.email "YOUR_GITHUB_EMAIL@HERE.COM"
git config --global user.name "YOUR NAME"
```


# Sublime Text 3 - Package

Let's go back to Sublime Text and install some packages that will help us to create better code.

Press the windows key + R at the same time to open the "Run" tool. Type the command:

```bash
%USERPROFILE%\AppData\Roaming\Sublime Text 3\Packages\User
```

Click on "OK"

![](images/sublime_7.png)

A new Explorer window should open, it should be empty. Right click and chose "Git Bash here".

A new Git Bash terminal will open. Please copy the following command:

```bash
curl -Ls https://raw.githubusercontent.com/lewagon/dotfiles/master/Preferences.sublime-settings > Preferences.sublime-settings
```

### Package install

Launch `Sublime Text 3`.

Install package controll via the Command Palette (`Ctrl` + `Shift` + `P`) and type `Install Package Control`. Type `Enter` and wait a few seconds. You should get an alert telling you package control has been successfully installed.

Now we can install the package `MagicPython`.<br>
You can install a package via the Command Palette (`Ctrl` + `Shift` + `P`) then type `Install package`,<br>
![](images/sublime_8.png)

Then type the name of the package you want to install and press `Enter`.
![](images/sublime_9.png)


# Make

Make is a build automation tool that build executable.  
Go to this [url](https://sourceforge.net/projects/ezwinports/files)  
Locate "make-4.2.1-without-guile-w32-bin.zip"  

![](images/make_1.png)  

Click on it. Your download should start shortly. A popup will appear at the bottom. Click on "Save".  

![](images/make_2.png)  

When the download is done you will be prompted with another popup, click on "Open folder".  

![](images/make_3.png)  

![](images/make_4.png)  
Right click on it and chose "Extract All".  

Click on "Extract".  

![](images/make_5.png)  

A new explorer window should open showing you the extracted folders.  

![](images/make_6.png)  

Select all the folders and right click and choose "Copy".  

Press the windows key + R at the same time to open the "Run" tool. Type the command  
```bash
explorer.exe "C:\Program Files\Git\mingw64"
```

Click on "OK".  

![](images/make_7.png)  

A new windows should open with folders already in it. Right click and chose "Paste". It will paste the folders you've extracted before into this folder. If it ask you for admin rights, press "Continue". Your folder should now look like this:  

![](images/make_8.png)  

To make sure "Make" is properly installed, please Click on "Start" in the bottom left corner.  

![](images/start.png)  

Search for "Git Bash" and click on the icon of it.  

![](images/gitbash_16.png)  

In the terminal please type the command:  

```bash
make -v
```

You should get and answer like this:  

![](images/make_9.png)  

If you don't, please ask a TA.  



# Alumni

Register as a Wagon alumni by going to [kitt.lewagon.com/onboarding](http://kitt.lewagon.com/onboarding). Select your batch, sign in with GitHub and enter all your information.

Your teacher will then validate that you are indeed part of the batch. You can ask him to do it as soon as you completed the registration form.

Once the teacher has approved your profile, go to your email inbox. You should have 2 emails:

- One from Slack, inviting you to the Le Wagon Alumni slack community (where you'll chat with your buddies and all the previous alumni). Click on **Join** and fill the information.
- One from GitHub, inviting you to `lewagon` team. **Accept it** otherwise you won't be able to access the lecture slides.



# Slack

Download and install the Slack app from [slack.com](https://slack.com/downloads/windows), and install it.

Launch the app and sign in to `lewagon-alumni` organization.

Make sure you upload a picture there.

You can also sign in to Slack on your iPhone or Android device!

The idea is that you'll have Slack open all day, so that you can share useful links / ask for help / decide where to go to lunch / etc.

Enjoy your ride with Le Wagon :)


