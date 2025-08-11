# Preparation for Class: HW0
Please try to follow the instructions to [Set Up Conda](https://github.com/Columbia-Neuropythonistas/IntroPythonForNeuroscientists2024/blob/main/Week01/README.md#set-up-conda), [Install VSCode](https://github.com/Columbia-Neuropythonistas/IntroPythonForNeuroscientists2024/blob/main/Week01/README.md#install-vscode), and [Set Up Github](https://github.com/Columbia-Neuropythonistas/IntroPythonForNeuroscientists2024/blob/main/Week01/README.md#Setting-Up-Github) by Wednesday, 9/3/2025 so that we have time to troubleshoot and everyone can start on the same page. Once you've set everything up, **prepare for submission to courseworks the following:**
- a screenshot of the conda version
- a screenshot of the printed hello world in VS code
- a screenshot of the terminal output from step #3 in Set Up Your Github SSH Keys
- a screenshot of your conda environment package list

If you run into any issues, you can try googling the error message, or you can email us. If you aren't able to figure it out on your own, please email pfncolumbia@gmail.com

Please do the rest of the preparation before the first class.

# IMPORTANT!!!
Please make sure you read ALL of the text and do ALL the tasks below.
## Video Introductions to Command Line and Git
Please take some time to go through the following videos, so that you have a general familiarity with the terminal, git, and conda by the first class. This is a lot of material, so it's alright if you don't get it all in one go! We will also take some time at the beginning of class to go over these concepts once again.
1. [Introduction to the Command Line (5m 40s)](https://www.youtube.com/watch?v=cgVbqxtx3hU)
2. [Introduction to Git (Watch the first 6m 32s)](https://www.youtube.com/embed/uR6G2v_WsRA?end=392). The remainder of the video is good to watch for an introduction to how we will be using git in class, but is not necessary if you are short on time.
3. [Introduction to Git Remotes / Github (Watch from 1:30-4:48 )](https://www.youtube.com/embed/Gg4bLk8cGNo?start=90&end=288)
4. [Introduction to Conda / Package Managers (Watch the first 6m 56s](https://www.youtube.com/embed/23aQdrS58e0?end=416) and also [the end of the video from 15:50 on)](https://www.youtube.com/embed/23aQdrS58e0?start=950) The remainder of the video is good to watch and provides a good introduction to how we will be using conda in class, but is not necessary if you are short on time.

## Set up Conda

Windows users - if your username has a space in it (for instance, if your usename is `Python for Neuro`), this will cause issues down the road. Please create a new user account with no spaces or special characters to ensure that everything will run smoothly.

### Check if Conda is already installed
- Open terminal using the following instructions for your operating system. (Instructions taken from [this source](https://docs.microsoft.com/en-us/learn/modules/python-install-vscode/)).
    - Mac:
        1. Open the Terminal app by pressing Command + Spacebar key combination to search by using Spotlight.
        2. In the search box, enter Terminal. In the results set select Terminal app, and then press Return to start the app.
    - Windows:
        1. Check that you have windows terminal installed by typing in `terminal` into the search bar. If nothing pops up, please install it [here](https://apps.microsoft.com/detail/9n0dx20hk701?hl=en-us&gl=US).
        2. Check if you have anaconda prompt installed by typing in `anaconda prompt` into the search bar. If not, it is unlikely that you have conda installed. If you do have anaconda prompt installed, skip the 'installing miniconda' step for now. If you receive errors later on, uninstall anaconda and then reinstall it using our instructions.
    - Linux: 
        1. Open a Linux terminal session. The instructions for opening this session depend on your distribution and version of Linux. Check the online documentation for your Linux distribution for instructions on how to open a terminal session.
- Check if conda is already installed by typing `conda --version` in terminal and pressing enter.
- If the output says conda and a version number, e.g. `conda 4.12.0`, submit a screenshot of this to the courseworks assignment and skip to installing VSCode.
- If you get an error message, install miniconda as follows.

#### Installing Miniconda
- Download the version of miniconda for your machine [listed here](https://docs.conda.io/en/latest/miniconda.html#latest-miniconda-installer-links)
    - [Windows instructions for figuring out your system architecture](https://pcguide101.com/cpu/what-is-my-processor-architecture/)
    - Mac instructions for figuring out your system architecture:
        1. click on Apple icon in top left corner > About This Mac
        2. Look at the Chip in the Overview.
        3. Select the appropriate miniconda download link ending in `.pkg`
    - Linux: The first option under linux should be appropriate for your computers.
- Install the downloaded miniconda. If there is an option during installation to add anaconda to PATH, please make sure that it is checked.
- Windows users: You should now have 'Anaconda Powershell Prompt (Miniconda3)' set up. Check that it installed properly by searching for `Anaconda Powershell Prompt` (note: not Anaconda Prompt) in your start menu and open it. In order to finalize set up, there are a few quick steps:
    - Open Anaconda Powershell Prompt (NOTE AGAIN: not anaconda prompt) and type in (or copy and paste)
      ```
      conda init powershell
      ```
      and hit enter. If you get an error, try retyping it, making sure that you match case and spaces. If this does not work, please email us ASAP, and proceed through these instructions using `Anaconda Prompt` wherever a terminal is mentioned.
    - Next, type in the following and hit enter:
      ```
      set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
      ```
    - Open terminal once again, by typing `terminal` in the search bar and hitting enter. You should open into a window that says `Windows Powershell` at the top, and you can proceed with the instructions.

- Check that the install worked by closing terminal if it is open, reopening it, and typing `conda --version` and hitting enter. The output should say conda and a version number, e.g. `conda 4.12.0`.
#### DELIVERABLE 1: Submit a screenshot of the output above to the courseworks assignment.


## Install VSCode
**Please follow the FULL tutorial!!!** 
- Follow the instructions for your operating system (Linux, Windows, or Mac) [here:](https://docs.microsoft.com/en-us/learn/modules/python-install-vscode/)

#### DELIVERABLE 2: Once you've gone through the instructions above, please take a screenshot of your printed hello world, and submit it to the courseworks.

- Troubleshooting:
    - If `code .` doesn't work for you, try using the Uninstall 'code' command in the PATH command before the "Install 'code' command in PATH" command following the instructions [here](https://code.visualstudio.com/docs/setup/mac#_launching-from-the-command-line) ([source](https://stackoverflow.com/questions/29955500/code-is-not-working-in-on-the-command-line-for-visual-studio-code-on-os-x-ma)).
    - For Linux, you can download either a .deb or a .rpm file. Which one you should use depends on your distribution, more specifically whether it is Debian- or Redhat-based. (Ubuntu, for example, is Debian-based and would need a .deb file.)

## Making your first Conda Environment
Open up your preferred command line interface (e.g. Terminal for Mac, Windows Terminal/Powershell for Windows, konsole for Ubuntu, etc). Make sure that conda is active. Depending on your install settings, you may have to manually activate conda using the command `conda activate`. When conda is active, there should be a parentheses indicating which environment you are using preceding your input line.

![image](image.png)

Now, let's make our first conda environment! Type the following in your command line interface (CLI).
```
conda create -n intropython python numpy seaborn pandas scikit-learn scipy jupyterlab git
```
Note that the `-n` flag is short for `--name`, where all it does is specify the name of the environment. The rest of the command tells conda what version of python to install and the other packages you would like in your virtual environment to start off. Note that you can always `conda install` more packages into that environment later.

Conda will then ask if you would like to proceed--type Y and hit enter. Sit tight--it may take a few minutes to build the environment. Once it finishes, run the following command:

```
conda env list
```

Conda should then spit out a list of your environments, including `base` and `intropython`. 

Next, activate the environment by entering the following command:
```
conda activate intropython
```

Confirm which packages your environment has by entering the following command:
```
conda list 
```
This command will print out all the packages that are currently installed in the currently active environment, as well as its version numbers. 

#### DELIVERABLE 3: **Screenshot this and submit it to the courseworks prework assignment.**



## Setting UP Github
### Make a Github account
- If you don't have a github account already, go [here](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home) to make one. I would recommend using an academic email because students get github pro for free, but you can always add other email addresses to your profile later. 
- Submit your github username to this [google form](https://forms.gle/qTWTMpfT1irJSeHt5).

### Set up your Github SSH Keys 
#### What is SSH?
SSH makes sure that your local computer is allowed to have access to your Github account. To do so, you’re essentially sharing a password with Github that can be used to authenticate your identity. Except with one complication: Github has a public version of the password (the “public key”), whereas you have the private version (“private key”) as well. This ensures that someone who sees your public key would not be able to pretend to be you. You will only be authenticated if you have both the public and the private key. Importantly, Github can make sure that this is the case without ever seeing the private key.

Thus, to set up an SSH connection, you need to do two things: generate your own public/private key pair and upload the private key to Github.

### How to set up SSH
#### Step 1. Check existing SSH keys. 
First we’ll make sure that you don’t already have an SSH key. Open your terminal and enter into the command line:
```
ls -al ~/.ssh
```
Windows users, you may receive an error. That's not an issue - please type in:
```
ls -Force ~/.ssh
```
If you see two files with the naming pattern ```id_<some numbers and letters>``` and ```id_<the same numbers and letters>.pub```, you already have an SSH key. You may not have the id prefix, but if a combination of a file with and without a `.pub` exist, you have an SSH key already. Skip to step 3. If you don’t or you get an error that the folder does not exist, continue with step 2.
#### Step 2. Generate a public/private key pair:
Enter in the terminal:
```
ssh-keygen -t ed25519 -C "your_email@example.com"
```
where you enter your own email address. 

When you are prompted to "Enter a file in which to save the key," press Enter to accept the default file location. 
```
> Enter a file in which to save the key (/Users/YOU/.ssh/id_ed25519_sk): [Press enter]
```
When you are prompted to type a passphrase, press Enter if you do not want to generate a passphrase.

```
> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]
```
Congrats! Now you've generated your SSH key. 
#### Step 3. Add the SSH key to the Github account
Go back to step 1 to figure out the name of your public/private key pair. Most likely, it will be ```id_ed25519```. The file with the ending ‘pub’ is the public key.

Print out the public key by entering the following command in terminal: 

```
cat ~/.ssh/id_ed25519.pub
```
(or with some other name if your key has a different name). You will get a long string of letters and numbers, as well as the name of the algorithm that was used to generate the key.

Next, select everything that was printed out and copy it to your clipboard. Make sure you only copy the string of text that was printed out when you ran the command above, rather than copying and pasting the text that is part of your terminal.

Open up Github in your browser. In the upper-right corner of Github, click your profile photo, then click Settings. In the "Access" section of the sidebar, click SSH and GPG keys. Then, click New SSH key or Add SSH key.

Add a title that describes the laptop you’re currently using (e.g. “My Laptop”). In the "Key" field, paste your public key. Click Add SSH key.

#### DELIVERABLE 4: take a screenshot of your terminal output showing what is expected from step 3 of the instructions and submit it to the assignment on courseworks.

 
# Resources
- [Setting up Git SSH Key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

## Cheatsheets
- [Git Cheatsheet](https://training.github.com/downloads/github-git-cheat-sheet.pdf)
- [Command Line Cheatsheet](https://upload.wikimedia.org/wikipedia/commons/7/79/Unix_command_cheatsheet.pdf)
- [Conda Cheatsheet](https://docs.conda.io/projects/conda/en/latest/_downloads/cb0ffc4c7b1e6c0e716c066d2b077faf/conda-4.12.pdf)
