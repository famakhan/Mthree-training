Mthree Training Repository
This repository is dedicated to the ungraded activities and exercises for the Mthree training course. It serves as a practical guide to understanding and using Git and GitHub in a software development environment.

Setting Up a GitHub Repository
Git is a distributed source control system that is widely used in the software development industry. It allows developers to store copies of their source code on multiple computer systems throughout their network and across the world. GitHub is a platform that hosts Git repositories, enabling collaboration and version control for projects.

# Create a New Repository on GitHub

Sign in to GitHub: 
- Navigate to GitHub and sign in with your credentials.

Create a New Repository:
- Click on the + icon in the top right corner and select New repository.
- Name your repository (e.g., Mthree-training).
- Optionally, add a description for your repository.
- Choose the repository visibility: Public or Private.
- Initialize the repository with a README file, if desired.
- Click Create repository.

## Clone the Repository to Your Local Machine
Once the repository is created, you can clone it to your local machine to begin working with it.

    # Use the following command to clone the repository
    git clone https://github.com/famakhan/Mthree-training.git

## Synchronize Your Local Files with the GitHub Repository
To keep your local files in sync with the remote repository on GitHub, use the following Git commands:

    # Add all changes to the staging area
    git add .

    # Commit the changes with a descriptive message
    git commit -m "Initial commit"

    # Push the changes to the remote repository
    git push origin main
    
## Learning Objectives
By the end of this course, you will be able to:

Explain the role of repositories in software development processes.
- Create a personal repository on GitHub.
- Clone the repository to your computer.
- Synchronize your local files with your GitHub repository.


# GitHub Repositories Access Guide
Welcome to the SRE Training course! The GitHub repositories used in this course are private, meaning that only users who have been invited can access them. To access these repositories, you will need to generate a personal access token from GitHub.

## Generating a Personal Access Token
To access the repositories, follow the steps below to generate a personal access token:

### Navigate to the Tokens Page: 
- Go to https://github.com/settings/tokens.
### Generate a New Token:
- Click the Generate new token button.
### Add a Note:
- In the Note text box, type in a use for the token. For example: SRETraining.
### Set an Expiration Date:
- Specify when you want the token to expire. For this training, select 45 days to ensure the token is available for the duration of the course.
### Assign Scopes:
- Check the box next to repo to grant access to repository features.
- Check the box next to user to grant access to user-related information.
### Generate the Token:
- Click the Generate token button.
### Save the Token:
- Copy the access token value shown on the screen.
- Important: Store the token securely. Once you leave this page, you will not be able to retrieve the token again. If you lose it, you will need to regenerate or create a new one.


# AWS EC2 Setup for Course
This guide will help you set up and use an AWS EC2 instance for the course.

### 1. Create a Free AWS Account
- Visit AWS Free Tier and sign up.
- Provide a credit card (no charges if within free tier limits).
- Use a different email if you’ve used the free tier before.
### 2. Create a Linux EC2 Instance
- Log into AWS.
- Create a Linux EC2 instance.
- Save the .pem key file securely for future access.
### 3. Connect to the EC2 Instance (macOS)
- Open the Terminal application.
- Use this guide to connect using SSH: Connect to your Linux instance using SSH.
### 4. Install Git
- Check installed packages:
  
      sudo yum list installed
- Install Git:

      sudo yum install git
- Configure Git:

      git config --global user.name "your_username"
      git config --global user.email "your_email@domain.com"

### Tips
- Username: Use ec2-user by default.
- Terminate/Stop: Terminate instances to avoid charges. Stopping an instance changes its IP and may take 10–15 minutes to restart.
- Secure Key: Save your .pem file securely as it cannot be retrieved if lost.


# Acitivity 1 - Linux Navigation Activity
In this activity, you'll practice using basic navigation commands in a Linux system. Follow these instructions to complete the activity.

### Navigate Using Basic Commands:

- Check Linux Version:
  
      uname -a

- Check Current Location:

      pwd

- Move Up One Directory:

      cd ..

- Check Location Again:

       pwd


- List Files with Details:

      ls -l

  
- List Files Sorted by Modification Time (Oldest First):

      ls -ltr

- Change to Root Directory:

      cd /

- Check Location in Root Directory:

      pwd

- List Files in Root Directory Sorted by Modification Time:

      ls -ltr

- Change Back to Home Directory:

      cd ~

- List All Files, Including Hidden Files:

      ls -ltra

- View Command History:

      history



#### Tips
- Using ls -l provides detailed information about files and directories.
- ls -ltr sorts files by modification time, with the oldest files listed first.
- ls -ltra shows all files, including hidden ones, and sorts by modification time.


# Activity 2 - File Management and Git Operations
## Part A: Managing Files and Folders
In this part of the activity, you'll practice creating, moving, and managing files and folders on a remote Linux system.

### Steps
- Create a Folder with Your Name:

      mkdir <yourname>

- Move into the New Folder:

      cd <yourname>

- Create an Empty File:

      touch file

- Create a New Folder Called myfolder:

      mkdir myfolder

- Move the File to myfolder:

      mv file myfolder

- Create a Backup of the File:

      cp -p myfolder/file file.bkp

- Remove the myfolder Directory:

      rm -rf myfolder

- Return to Your Home Directory:

      cd ~

## Part B: Working with Git
In this part, you'll clone a Git repository and perform various file operations.

### Steps
- Clone the Repository:

      git clone https://github.com/The-Software-Guild/pss-orderbook-deploy/

- Navigate to the Cloned Repository Directory:

      cd pss-orderbook-deploy
- Navigate to the src/linux_activities/Activity2 Directory:

      cd src/linux_activities/Activity2
- Searching and Managing Files
Display the Contents of stock_investments.txt:

      cat stock_investments.txt

Display the First Five Lines of the File:

      head -5 stock_investments.txt

Display the Last Five Lines of the File:

     tail -5 stock_investments.txt

Count Lines Containing the Word GOOG:

     grep GOOG stock_investments.txt | wc -l

Count Lines Containing the Word T:

     grep -wc T stock_investments.txt

List Files Containing the Word SPY:

     grep -lir spy .

List Files Not Containing the Word spy:

     grep -lvri spy .

Find Files Containing data in Their Name:

    find . -type f -name "*data*"

Find Folders Named error:
 
     find . -type d -name error

Change Permissions on Files Containing data to Read-Only for Group and Others:

     sudo find . -type f -name "*data*" -exec chmod 744 {} \;

Remove Write Permission from the File WFC/data.txt:

     chmod -w WFC/data.txt

#### Tips
- Use ls -l to get detailed information about files and directories.
- Use grep for searching text within files and use flags to refine your search.
- Use find to locate files and directories based on various criteria.



