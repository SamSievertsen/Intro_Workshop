# Intro Workshop

This repository serves as an introduction to GitHub and Git.

## What is Git?

**Git** is an example of a version control system. A version control system is a tool for managing a collection of program code that provides you with **reversibility**, **concurrency**, and **annotation**. Version control systems work a lot like Dropbox or Google Docs: they allow multiple people to work on the same files at the same time, and to view or “roll back” to previous versions.

## What is GitHub?

**GitHub** is a site that will host a copy of your coding project in the cloud, enabling multiple people to collaborate (using **git**). **Git** is what you use (the language) to do version control; **GitHub** is a place where repositories of code can be stored.

## Installing git and GitHub on your computer

- [Create a GitHub account](https://github.com/join) using your ohsu.edu email address.

### For MacOS:

- Paste the following into your terminal/command line interface to download Homebrew:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

- Once homebrew has been successfully installed, paste the following into your terminal/command line interface to download and install Git:
```bash
brew install git
```

### For Windows:

- [Download Git for Windows](https://git-scm.com/download/win). Most likely, you will want to select the *"64-bit Git for Windows Setup."* version.

- Once the .exe file has been downloaded onto your machine, open it and select *"Yes"* when prompted to allow changes to be made to your device

- Select *"Next"* on all the optional changes git allows you to make (AKA retaining default options).

- Upon selecting all options/preferences, the .exe will complete its installation steps. Once prompted, select *"Finish"* to complete the install

## Configuring your GitHub account on your local machine

- Verify your email address in the link sent by GitHub.

- Go into your terminal/PowerShell/command line application and paste the following code:

```bash
git config --global user.name "Your_username_here"
```

```bash
git config --global user.email "your_email@ohsu.edu"
```

- Perform a test of your connection to GitHub from your local machine by entering the following commands in the command line to clone this repo:

```bash
cd Desktop/
```

```bash
git clone https://github.com/SamSievertsen/Intro_Workshop.git
```

If the commands are successful, our GitHub introductory repo will be downloaded to your desktop, signifying your GitHub account is successfully connected to your local machine.

## Authenticating with the Command line 

This step is to gain read/write/execute access for your local machine to asess repositories on GitHub. There are two ways, HTTPs and SSH, and both have a different way of authenticating.

### [HTTPs](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-authentication-to-github#https) - Authenticate with a personal access token.

- In the upper-right corner of your GitHub account in the browser, click your profile photo, then click *Settings*.

- In the left sidebar, click *Developer settings*.

- In the left sidebar, click *Personal access tokens*.

- Click *Tokens (Classic)*.

   - Click *Generate new token* and select *Generate new token (Classic)*.

- Give your token a descriptive name in the *Note* field.

- For expiration, select the “Expiration” menu and choose the *No Expiration* option (disregard the warning, but be sure not to share this token with anyone or anywhere non-secure).

- Select the scopes you'd like to grant this token. For purposes of working on code in the lab, it will be most beneficial to select everything except *delete:packages* and *delete_repo* as these are dangerous user capabilities.
   
   - To note, a token with no assigned scopes can only access public information. For more information, see ["Available scopes"](https://docs.github.com/en/enterprise-server@3.4/developers/apps/building-oauth-apps/scopes-for-oauth-apps#available-scopes).

- Click *Generate token*.

   - **IMPORTANT NOTE:** once this token has been generated, it will display only once on your screen and not be viewable again. As such, copy and store it in a secure location (e.g., password protected document, bit-locker, etc.) to be accessed when GitHub credentials will be first required (either in pushing/pulling this repo in the steps below, or another repo on which you plan to work).
  
### [SSH](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-authentication-to-github#ssh) - Generate an SSH public/private keypair
A more secured method. Access the github help page for more information.

## Committing a test push/pull to the Intro Workshop repo

### On Mac:

1. Open Terminal or your command line interface of choice.

2. Navigate to the directory where you want to create the file and add text. For example, if you want to create the file inside the "Intro_Workshop/Workshop_Push_Directory" directory on your Desktop, you can use the following command:
   ```bash
   cd ~/Full/Path/To/Intro_Workshop/Workshop_Push_Directory
   ```

3. Pull any changes made by others to the GitHub repository:
   ```bash
   git pull
   ```
   
4. It is likely at this point that you will be prompted to enter your credentials - though it is possible you may not encounter this prompt until step 9, regardless when you are prompted for:
   - Username for 'https://github.com' *Enter your github username here*
   - Password for 'https://github.com' *Enter the token you created here*
      - At this point, since UW provides access to GitHub Enterprise and our organization uses single sign on (SSO), you will likely encounter something to the effect of "Permission denied. Could not read from remote repository", followed by a link to an SSO authorization. Copy and paste this link into your browser of choice, and agree to the terms and conditions of the SSO.
      - Once completed, you should be able to successfully perform the *git pull* action from step 3, albeit being prompted for your credentials once more. 

### On Windows:

1. Open Command Prompt or PowerShell.

2. Navigate to the directory where you want to create the file and add text. For example, if you want to create the file inside the "Intro_Workshop/Workshop_Push_Directory" directory on your Desktop, you can use the following command in Command Prompt:
   ```bash
   cd C:\Users\YourUsername\Desktop\Intro_Workshop\Workshop_Push_Directory
   ```

3. It is likely at this point that you will be prompted to enter your credentials - though it is possible you may not encounter this prompt until step 9, regardless when you are prompted for:
   - Username for 'https://github.com': *Enter your github username here*
   - Password for 'https://github.com': *Enter the token you created here*
      - At this point, since UW provides access to GitHub Enterprise and our organization uses single sign on (SSO), you will likely encounter something to the effect of "Permission denied. Could not read from remote repository", followed by a link to an SSO authorization. Copy and paste this link into your browser of choice, and agree to the terms and conditions of the SSO.
      - Once completed, you should be able to successfully perform the *git pull* action from step 3, albeit being prompted for your credentials once more. 

### Create the file using the following command:

1. Directly in the terminal

   a. Creating a new empty file (optional)
   
     For mac:
     
     ```bash
     touch your_name_test.txt
     ```
     For windows:
   
     ```bash
     New-Item your_name_test.txt
     ```
   b. Making edits 

   ```bash
   vim your_name_test.txt
   
   ```
   or 
   ```bash
   nano your_name_test.txt
   ```
   or 
   ```bash
   vi your_name_test.txt
   ```
   


2. Use any text editor of your choice (e.g Visual Studios, Sublime, Notepad...)
   ```bash
   # Basic Vim Commands
   Enter INSERT mode = click the letter "i"
   Get out of INSERT mode = click "esc"
   Save & Quit = click esc then type ":wq" and click "Enter"
   Exit = click esc then type ":x" click "Enter"

   # Basic Nano commands
   Save = click "ctrl" and the letter "O" at the same time,
   then click "enter".
   Exit = click "ctrl" then type "x"

   ```
   
### Commit a test change:
1. Stage the changes:
   ```bash
   git add .
   ```

2. Commit the changes:
   ```bash
   git commit -m "Add a line of text to your_name_test.txt"
   ```

3. Push the changes to the GitHub repository:
   ```bash
   git push
   ```
