---
title: Digging into versioning with GitHub Desktop
---

# Install git and GitHub Desktop software

## Install git version control software
- Navigate to the [official git website](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) and follow the instructions to download and install for your operating system.
  - For Windows, use [this download link](https://git-scm.com/download/win) and install using all of the default (recommended) options.

## Create a GitHub account (if you don't have one)
- Navigate to [Github](https://github.com) and sign up for an account if you don't already have one. 
- After registering, sign in to your account.
- (optional) Watch the short introductory video[What is GitHub?](https://www.youtube.com/watch?v=w3jLJU7DT5E).

## Install and configure GitHub Desktop
**NOTE:** If you are a Linux user, GitHub Desktop will not work for you. Instead, you'll need to learn how to use git and git Bash. Separate instructions are provided below.

If using a Windows or Mac, download and install [GitHub Desktop](https://desktop.github.com/)
- More guidance can be found in guides from [GitHub](https://help.github.com/en/desktop/getting-started-with-github-desktop) and [TechRepublic](https://www.techrepublic.com/article/how-to-install-github-desktop/).
- Sign into GitHub Desktop using your GitHub credentials
- In the *Configure Git* page, enter the name and email address that you want associated with your changes
- In File > Options > Advanced, set the Shell to Git Bash
- (optional) Once configured, the main GitHub Desktop page will show any repositories that exist in your GitHub account. For those who use git already, you can add any local repositories that already exist on your machine.

# Introduction to git and GitHub Desktop
Follow along with the slides describing git and GitHub Desktop
<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSjyUEk9jOYf-5aYJUT898qN1qxw7Wohn-kOoniaOgfy6GhPRpMB6abZJhIzAUnB0eh0NBa9N4Dh82f/embed?start=false&loop=false&delayms=30000" frameborder="0" width="640" height="389" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

# Cloning, editing, pushing changes

## For Windows and Mac users

### Clone your existing GitHub repository to your local computer
In this next step, you will 'clone' your existing GitHub repository to your local computer so that you can work on files locally. 
- **In GitHub Desktop**, your newly forked repository should appear in the **Your repositories** list (You may need to refresh the list for it to show). 
  - **NOTE:** If it doesn't appear, double-check that the repository exists in your GitHub profile. If it does exist, you can copy the repository URL from GitHub and paste it into the appropriate place using the "Clone a repository from the Internet" button on GitHub Desktop.
- Highlight your repository in the list and click "Clone <*repository name*>". Select the local path where you would like to download the repository--a new folder will be created with the name of the repository. 

### Make some local edits | add some files!
- In GitHub Desktop, click the **Show in Explorer** button to open up your file explorer to your repository's contents. 
- Open one of your Markdown (.md) files in a text editor. Make some changes and save them.
- Add a few files (images, maybe?) to the ```docs``` folder. 

### Commit new changes
- In GitHub Desktop, you should be shown the files that have been changed, and be able to view the specific changes. 
- If you are comfortable with the changes, you are ready to commit them.
  - Provide a summary of the changes (or used the suggested text), and lengthier description, if desired.
  - Click **Commit to master**. This commits your changes to your local repository. 
  - If you continue to work on your local files, you will need to again commit changes.  

### Push changes to GitHub (remote) repository
In this step, you'll 'push' your local changes back up to your GitHub repository, so that both are synced. 
- In GitHub Desktop, click the **Push origin** button

### Make changes in the GitHub (remote) repository
- Make a change to a file in the GitHub (remote) repository using the web editor. 

### Pull changes to the local directory
- In GitHub Desktop, click the **Fetch origin** button. This will check the GitHub repository to see if any changes have been made remotely.
- 



### Step 1.3: Do things in Openrefine!
- Once you've cloned the repository, use the button on GitHub Desktop to view the repository/files in Explorer. 
- Proceed with the [Data Carpentries Openrefine lesson](https://datacarpentry.org/openrefine-socialsci/01-introduction/index.html), using the downloaded data.

### Step 1.4: Export/Save modified data and processing script from Openrefine 
- Be sure to save all exported products (processing script, tar.gz project file, csv file) in the folder you cloned in Step 2.

### Step 1.5: Add and commit new files and changes to your local repository
- Maximize (or reopen) GitHub Desktop and open the local repository for this workshop (\cdcf-workshop2A). 
- The modified files will appear in the left-hand pane. Clicking on any of these files will display changes in the main pane.
- To commit changes, add a short summary (e.g. "outputs from OpenRefine workshop") and a further description of contents and activities (if desired). Click **Commit to master**.  

### Step 1.6: Push changes to your GitHub repository
- The repository overview page in GitHub Desktop will now display a new message: **Push 1 commit to the origin remote**. Click to push changes to the origin remote in GitHub. 

### Step 1.7: View and edit your readme file in the GitHub Editor
- Once your changes have been pushed to your remote (GitHub) repository, use your web browser to navigate to your GitHub repository. Confirm that the new files have been added to the repository along with the timestamp and summary from the commit.
- Explore the files in your GitHub repository. View the exported csv file, which will be presented in a formatted table. 
- View the README.md file and open it up for editing by clicking the pencil icon (*"Edit this file"*)
  - The README file is written in [Markdown](), a lightweight markup language that allows you to use plain text and a few special characters to create formatted text. 
  - More information and references for Markdown:
    - [Mastering Markdown](https://guides.github.com/features/mastering-markdown/) 
    - [Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
    - [Daring Fireball's Markdown Introduction](https://daringfireball.net/projects/markdown/)
- Edit the readme file to include pertinent information about the repository's creation, its contents, and sharing information. An empty template has been created for you from Cornell University's [Guide to writing "readme" style metadata](https://data.research.cornell.edu/content/readme). Click the **Preview changes** tab to see how the Markdown will render on the web.
- When finished editing, scroll to the bottom of the page, add a Summary and Description and commit changes to the master branch.

### Step 1.8: Pull GitHub changes to your local repository
- Maximize GitHub Desktop and click "Fetch origin" near the top of the window. A new prompt should appear to *"Pull 1 commit from the origin remote"*. Click **Pull origin** to incorporate the changes into your local repository. 
- Inspect the changes to your local repository.

### Step 1.9: Make a Pull Request to the original repository
On occasion, you may want to ask the maintainer of an 'upstream' branch to incorporate your changes. This can be done by making a **Pull request**
- From the top-level page of your GitHub repository (i.e. /cdcf-workshop2A), click on **New pull request**. You'll be taken to a page that compares the differences between the two repositories. Review the suggested changes and click **Create pull request**. 
- Add a title and leave a comment. and click **Create pull request**. 
- Your pull request will now appear in the upstream repository's [list of requests](https://github.com/data-curation/cdcf-workshop2A/pulls). The owner of the upstream repository can now manage the merger of files (either automatically or manually).









