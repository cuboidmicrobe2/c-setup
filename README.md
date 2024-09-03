# Download WSL2

To download WSL2, open Windows Command Prompt or PowerShell in **administrator mode** and run the following command.

If you already have Linux, skip this step and start with [setting up Linux](#setup-linux).

```powershell
wsl --install
```

# Setup Linux

This Linux setup involves updating the packages, downloading the necessary packages, and changing shell.

## Update packages

After creating an account, run the following command to update all packages.

```shell
sudo apt update -y && sudo apt full-upgrade -y &&
sudo apt autoremove -y && sudo apt clean -y && sudo apt autoclean -y
```

## Downloading necessary packages

```shell
sudo apt install git curl build-essential clang-format zip unzip -y
```

## Changing shell

First, to change shell to "Oh My Zsh", download zsh with the following command.

```shell
sudo apt install zsh
```

Then "Oh My Zsh" can be installed.

## Setup git

Git must be set up with your name e.g. Sebastian Einarsson, email, and the default name of newly initialized branches (preferably "main" by the new standard).

```shell
git config --global user.name "Your name"
```

```shell
git config --global user.email "Your email"
```

```shell
git config --global init.defaultBranch main
```

## Connect to GitHub CLI

First, run the following command to download GitHub CLI.

```shell
sudo apt install gh
```

Then connect to GitHub CLI by running the following command.

```shell
gh auth login
```

If you use WSL2, you have to manually click on the link in the terminal.

# Setup VS Code

After Linux has been set up, VS Code can be installed.

## Download VS Code

Install VS Code from their [website](https://vscode.download.prss.microsoft.com/dbazure/download/stable/f1e16e1e6214d7c44d078b1f0607b2388f29d729/VSCodeUserSetup-x64-1.91.1.exe).
When prompted to **Select Additional Tasks** during installation, be sure to check the **Add to PATH** option so you can easily open a folder in WSL using the code command.


## Install extensions

When VS Code has been downloaded, install the following extensions.

![Extensions]

The VS code extensions can be installed as you wish.
