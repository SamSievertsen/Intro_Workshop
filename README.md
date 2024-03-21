# Intro Workshop

This repository contains serves as an introduction to GitHub and Git.

## What is Git?

**Git** is an example of a version control system. A version control system is a tool for managing a collection of program code that provides you with **reversibility**, **concurrency**, and **annotation**. Version control systems work a lot like Dropbox or Google Docs: they allow multiple people to work on the same files at the same time, and to view or “roll back” to previous versions.

## What is GitHub?

**GitHub** is a site that will host a copy of your coding project in the cloud, enabling multiple people to collaborate (using **git**). **Git** is what you use (the language) to do version control; **GitHub** is a place where repositories of code can be stored.

## Installing git and GitHub on your computer

- [Create a GitHub account](https://github.com/join) using your uw.edu email address.

- Paste the following into your terminal/PowerShell/command line interface to download Homebrew:

```bash
/bin/bash -c “$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)”
```

- [Download the git language](https://git-scm.com/downloads) for your computer's operating system.

## Configuring your GitHub account on your local machine

- Verify your email address in the link sent by GitHub.

- Go into your terminal/PowerShell/command line application and paste the following code (you may be prompted for your password):

```bash
git config --global user.name "Your_username_here"
git config --global user.email “your_email@uw.edu”
```

- Perform a test of your connection to GitHub from your local machine by entering the following commands in the command line to clone this repo:

```bash
cd Desktop/
git clone https://github.com/forsyth-lab/Intro_Workshop.git
```

If the commands are successful, our lab's GitHub introductory repo will be downloaded to your desktop, signifying your GitHub account is successfully connected to your local machine.

## Configuring permanent read/write/execute access on your local machine for pushing/pulling repositories (optional)

- In the upper-right corner of your GitHub account in the browser, click your profile photo, then click **Settings**.

- In the left sidebar, click **Developer settings**.

- In the left sidebar, click **Personal access tokens**.

- Click **Generate new token**.

- Give your token a descriptive name.

- For expiration, select the “Expiration” menu and choose the **No Expiration** option (disregard the warning, but be sure not to share this with anyone).

- Select the scopes you'd like to grant this token (it is most helpful to give it access to everything). To use your token to access repositories from the command line, select **repo**. A token with no assigned scopes can only access public information. For more information, see ["Available scopes"](https://docs.github.com/en/enterprise-server@3.4/developers/apps/building-oauth-apps/scopes-for-oauth-apps#available-scopes).

- Click **Generate token**.

- Open your terminal/PowerShell/command line interface and type the following command:

```bash
git clone https://username@github.com/username/repository.git
```

Alternatively, you may attempt to `git push` or `git pull` a repo to which you have access (and the same prompt below should be generated).

Assuming you have entered your username in previous steps, you will then be prompted to provide your GitHub credentials as seen below:
Password: YOUR_TOKEN
