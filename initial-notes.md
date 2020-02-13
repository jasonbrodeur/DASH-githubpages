# Introduction

# Pre-event prepartion

## Step 0.1: Install git version control software
- Navigate to the [official git website](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) and follow the instructions to download and install for your operating system.
  - For Windows, use [this download link](https://git-scm.com/download/win) and install using all of the default (recommended) options.

## Step 0.2: Create a GitHub account (if you don't have one)
- Navigate to [Github](https://github.com) and sign up for an account if you don't already have one. 
- After registering, sign in to your account.
- Watch the short introductory video[What is GitHub?](https://www.youtube.com/watch?v=w3jLJU7DT5E).

## Step 0.3: Install and configure GitHub Desktop
- If using a Windows or Mac, download and install [GitHub Desktop](https://desktop.github.com/)
  - More guidance can be found in guides from [GitHub](https://help.github.com/en/desktop/getting-started-with-github-desktop) and [TechRepublic](https://www.techrepublic.com/article/how-to-install-github-desktop/).
  - Sign into GitHub Desktop using your GitHub credentials
  - In the *Configure Git* page, enter the name and email address that you want associated with your changes
  - In File > Options > Advanced, set the Shell to Git Bash
- (optional) Once configured, the main GitHub Desktop page will show any repositories that exist in your GitHub account. For those who use git already, you can add any local repositories that already exist on your machine.

# In-Class Activity
- Navigate to [Github](https://github.com) and sign up for an account if you don't already have one. 
- After registering, sign in to your account.

## 3. 
- From your GitHub main page, click on the green **New Repository** button. This is the repository (storage location) where the content of your website will be hosted. 
  - Provide a name for your repository. This will determine the URL of your repository. i.e. https://github.com/<your-github-username>/<your-repo-name>
- Check the box to **Initialize this repository with a README**
- Click the **Create repository** button
- Your browser will now open to the top-level page of the repository. Your repository will contain one file: **README.md**. 
  - Click on the **README.md** file to open it in the file viewer page
  - On the file viewer page, click the edit button (pencil icon) to switch to editing mode
  - Add a bit of information to the README file that explains what this repository is for, and who created it. 
  - When finished editing, scroll to the bottom of the page to the **Commit changes** box. 
	- The **Commit changes** box is used to record information about changes before you commit them. 
	  - (optional) If interested, modify the comment from **Update README.md** to something more descriptive
	  - (optional) Add a description, if desired
	- Click the **Commit changes** box to finalize your commit. Your changes will be represented in the README file. 
Viewing changes
- In the README file viewing page, explore the Blame and History buttons to better understand how GitHub keeps track of file changes. 
Creating a folder
- Next, we want to create a folder named **docs** in the top level of the repository. This is where the webpage content will be created. 
  - In the top-level repository page, click **Create new file**
    - NOTE1: To create a file, simply enter the name (with extension). 
	- NOTE2: To create a folder, you need to add a trailing slash (/) to the name, and you need to [create a file within the folder](https://github.com/KirstieJane/STEMMRoleModels/wiki/Creating-new-folders-in-GitHub-repository-via-the-browser) (empty folders aren't saved). You can always delete this file later.
	- In the **Name your file...** box, enter **docs/foo.txt** (you can use any filename in place of foo.txt). Click **Commit change**. You will now have a folder named *docs* in your repository.
	


### Exploring Features and Settings | Creating webpages
In this step, we'll explore some of the functionality available in a GitHub repository and show you how to get started with [GitHub Pages](https://help.github.com/en/github/working-with-github-pages/about-github-pages)
- Ensure that you created the **docs** folder, as outlined in the previous step.
- Explore with Jay the various Features (tabs) that are available within a repository
- Open the Settings Tab. Follow along with Jay as he explains the various pages
- On the (topmost) **Options** page, scroll down to the **GitHub Pages** section
  - For **Source**, select `master branch /docs folder` (note you could also pick the *master branch* option)
  - Click **Choose a theme** to select a theme for your webpage
- Congratulations, your website is now live. The link will be provided in the GitHub Pages section.
- ... however, if you click it, you'll receive a 404 error. Now we need to create some content!

### Creating content | Customizing pages
- Navigate to the **docs** folder of your repository
  - Note that there is now a file named **_config.yml**. This is your configuration file, and it's written in a language called [YAML](https://en.wikipedia.org/wiki/YAML). 


- Create index.md file 
- Include front matter
```
plugins:
  - jekyll-relative-links
relative_links:
  enabled: true
  collections: true
include:
  - pagetwo.md

title: Welcome to my webpage
```

### Jekyll
From jekyllrb.com
>“Jekyll is a static site generator. You give it text written in your favorite markup language and it uses layouts to create a static website. You can tweak how you want the site URLs to look, what data gets displayed on the site, and more.”

GitHub pages uses jekyll to turn your markdown files (hosted in your GitHub repo) into html files and presents them on your desired website. 

Jekyll [webpage](https://jekyllrb.com/) and Jekyll project [on GitHub](https://github.com/jekyll/jekyll)



## Introduction

Follow along with the [introductory slides](https://docs.google.com/presentation/d/e/2PACX-1vSjyUEk9jOYf-5aYJUT898qN1qxw7Wohn-kOoniaOgfy6GhPRpMB6abZJhIzAUnB0eh0NBa9N4Dh82f/pub?start=false&loop=false&delayms=60000). 

Presentations slides
<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSjyUEk9jOYf-5aYJUT898qN1qxw7Wohn-kOoniaOgfy6GhPRpMB6abZJhIzAUnB0eh0NBa9N4Dh82f/embed?start=false&loop=false&delayms=3000" frameborder="0" width="1280" height="749" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>


During today's workshop, you will accomplish the following tasks:  
- Use GitHub to fork someone else’s project into your own GitHub repository
- Use GitHub Desktop (GHD) and git to clone your repository to your local computer
- Use Openrefine to clean some messy data, and edit the contents of your local repository (by exporting a processing script and refined data products to your working folder)
- Add and commit your changes to your local git repository
- Push your changes from your local computer to your GitHub repository using GHD
- Edit content (i.e. Markdown files) using the GitHub web interface
- Pull new changes back to your local repository
- Initiate a ‘pull request’ to the original project repository

![flowchart of workshop activities](https://github.com/data-curation/cdcf-workshop2A/blob/master/docs/Overview.png?raw=true)

## For Windows and Mac users

### Step 1.1: Fork a GitHub repository
In this step, you will 'fork' an existing (original) GitHub repository (belonging to someone else) to create a branch repository in your GitHub account. This allows you to create a copy of the original repository that you can modify as desired...and perhaps, allow your changes to be merged back 'upstream' to the original repository. 

- Ensure that you are logged into your GitHub account.
- Navigate to the workshop GitHub repository [https://github.com/data-curation/cdcf-workshop2A](https://github.com/data-curation/cdcf-workshop2A). 
- Click the **Fork** button at the top of the repository--this will "fork" the repository and create a branch in your GitHub account. By default, it will use a similar URL naming convention to the original (i.e. https://github.com/<yourUsername>/cdcf-workshop2A).

### Step 1.2: Clone to your local computer
In this next step, you will 'clone' your GitHub repository to your local computer so that you can work on files locally. 
- **In GitHub Desktop**, your newly forked repository should appear in the **Your repositories** list (You may need to refresh the list for it to show). 
  - **NOTE:** If it doesn't appear, double-check that the repository exists in your GitHub profile. If it does exist, you can copy the repository URL from GitHub and paste it into the appropriate place using the "Clone a repository from the Internet" button on GitHub Desktop.
- Highlight your repository in the list and click "Clone <*repository name*>". Select the local path where you would like to download the repository--a new folder will be created with the name of the repository. 

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


## D. An introduction to Markdown
### D1. What is Markdown? 
Borrowed shamelessly from Github's [Mastering Markdown](https://guides.github.com/features/mastering-markdown/) page: 
> Markdown is a way to style text on the web. You control the display of the document; formatting words as bold or italic, adding images, and creating lists are just a few of the things we can do with Markdown. Mostly, Markdown is just regular text with a few non-alphabetic characters thrown in, like # or *.

Markdown uses simple notation to apply simple formatting rules. Since it's pretty much just plain text, it's transferrable and much simpler than marked-up text like HTML or even Word or Google documents. For much of the writing that you do for the web, Markdown is good enough. Github uses Markdown for its documents (this document was created in markdown), as does a variety of other web platforms (Trello, for example). 

Using Markdown in Github lets you create readme files that can use better formatting than a plain text file, but is still readable as plain text -- it's the best of both worlds. 

### D2. Get familiar with Markdown
1. Using the Github web interface, add some content to your newly-created **readme.md** document. Use the [Mastering Markdown guide](https://guides.github.com/features/mastering-markdown/) as a reference (or other guides on the web) to create a fictional document that contains the following elements: 
- Headings of a number of different levels
- bolded, italicized text 
- insert an image from the web
- insert an image that is hosted in your GitHub repository
- An ordered list
- A bulleted list
- A link to another website 
- A table
- And finally, an emoji! 
2. Commit your changes and enjoy the products of your hard work!

### More information and references for Markdown:
- [Mastering Markdown](https://guides.github.com/features/mastering-markdown/) 
- [Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
- [Daring Fireball's Markdown Introduction](https://daringfireball.net/projects/markdown/)



  
## For Linux users
### Step 1.0: Configuring your git account 
Open up Git Bash and navigate to the desired directory for your repository
- Set your name: ```git config --global user.name "John Doe"```
- Set your email address: ```git config --global user.email johndoe@example.com```
- Check your settings ```git config --list```
See [git documentation](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup) for more information.

### Step 1.1: Fork a GitHub repository
In this step, you will 'fork' an existing (original) GitHub repository (belonging to someone else) to create a branch repository in your GitHub account. This allows you to create a copy of the original repository that you can modify as desired...and perhaps, allow your changes to be merged back 'upstream' to the original repository. 
- Ensure that you are logged into your GitHub account.
- Navigate to the workshop GitHub repository [https://github.com/data-curation/cdcf-workshop2A](https://github.com/data-curation/cdcf-workshop2A). 
- Click the **Fork** button at the top of the repository--this will "fork" the repository and create a branch in your GitHub account. By default, it will use a similar URL naming convention to the original (i.e. https://github.com/<yourUsername>/cdcf-workshop2A).

### Step 1.2: Clone to your local computer
In this next step, you will 'clone' your GitHub repository to your local computer so that you can work on files locally. 
- In the top-level page of your newly-forked GitHub repository (i.e. /cdcf-workshop2A), click on the **Clone or Download** button. Copy the URL that is provided. 
- Open Git Bash in the desired directory for your repository. Enter the command: ```git clone <copied url>```
- Git should now download the contents of your GitHub repository to a new folder in your current directory

### Step 1.3: Do things in Openrefine!
- Once you've cloned the repository, use the button on GitHub Desktop to view the repository/files in Explorer. 
- Proceed with the [Data Carpentries Openrefine lesson](https://datacarpentry.org/openrefine-socialsci/01-introduction/index.html), using the downloaded data.

### Step 1.4: Export/Save modified data and processing script from Openrefine 
- Be sure to save all exported products (processing script, tar.gz project file, csv file) in the folder you cloned in Step 2.

### Step 1.5: Add and commit new files and changes to your local repository
- Check the status of your repository (i.e. what's been modified): ```git status```
  - This will provide a list of items that are not yet being tracked (i.e. have not been added to the index), and those that are being tracked and have been modified.
- Add new items to the list of tracked files (individually): ```git add <filename>```
  - **OR** Add all items to this list of tracked files: ```git add --all```
- Commit changes to git (i.e. record changes): ```git commit -m '<enter a note on what has changed>'```
  - **OR** add and commit all at once: ```git commit -a -m '<enter a note on what has changed>'```

### Step 1.6: Push changes to your GitHub repository
- To check if there are connected remote repositories use the command: ```git remote -v```
- Push changes to the target Github repository using the command: ```git push origin master```
  - In this example -- which is the default case -- **origin** specifies the remote (i.e. Github) repository that is the target of your 'push'. **master** specifies the branch of the git repository that you're working on as the source data.

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
- You can check changes (before merging them) with: ```git fetch``` ```git diff origin master```
- Pull (fetch and merge) changes: ```git pull origin master```
  - **Note:** ```git pull``` actually runs two processes: ```fetch``` (get changes) and ```merge``` (place in your directory) 
- Inspect the changes to your local repository.

### Step 1.9: Make a Pull Request to the original repository
On occasion, you may want to ask the maintainer of an 'upstream' branch to incorporate your changes. This can be done by making a **Pull request**
- From the top-level page of your GitHub repository (i.e. /cdcf-workshop2A), click on **New pull request**. You'll be taken to a page that compares the differences between the two repositories. Review the suggested changes and click **Create pull request**. 
- Add a title and leave a comment. and click **Create pull request**. 
- Your pull request will now appear in the upstream repository's [list of requests](https://github.com/data-curation/cdcf-workshop2A/pulls). The owner of the upstream repository can now manage the merger of files (either automatically or manually). 

# More information

## git
- [Official git documentation page](https://git-scm.com/book/en/v2/)
- [The Smart Ways to Correct Mistakes in Git](https://css-tricks.com/the-smart-ways-to-correct-mistakes-in-git/) 
