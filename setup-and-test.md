# PREPARATION FOR WORCS WORKSHOP: Setup & Test

This preparation guide consists of three sections:

1. [Setting Up Your Computer For WORCS](https://nehamoopen.github.io/workshop-worcs-pilot/setup-and-test.html#setting-up-your-computer-for-worcs)
2. [Test Your Setup](https://nehamoopen.github.io/workshop-worcs-pilot/setup-and-test.html#test-your-setup)
3. [Troubleshooting](https://nehamoopen.github.io/workshop-worcs-pilot/setup-and-test.html#troubleshooting)

The instructions guide you through the installation and testing of several software packages, and registration on GitHub. In case some of the software is already installed on your system, you can skip those related steps. Additionally, we have an exercise which tests if your installation and setup was completed successfully. This allows us to identify potential errors/issues and resolve them before the workshop, so things go more smoothly during the workshop itself.
 
If you run into any issues, please don’t hesitate to ask for help during our drop-in call for _Installation & Set-Up Support_ or by emailing Neha Moopen (n.moopen@uu.nl). Try not to leave them until the morning of the workshop!  

## Setting Up Your Computer For WORCS

Source: [vignettes/setup.Rmd](https://github.com/cjvanlissa/worcs/blob/HEAD/vignettes/setup.Rmd)

This is a tutorial from the [WORCS package website](https://cjvanlissa.github.io/worcs/articles/setup.html) on how to set up your personal computer for use with the `worcs` package. It guides you through the installation of several software packages, and registration on GitHub. This vignette does not assume a prior installation of `R`, so it is suitable for novice users.
You only have to perform these steps once for every computer you intend to use `R` and `worcs` on, and the entire process should take approximately 30 minutes if you start from scratch.
In case some of the software is already installed on your system, you can skip those related steps.

Follow these steps in order:

1. Install R from https://CRAN.R-project.org

2. Install 'RStudio' Desktop (Free) from [rstudio.com](https://rstudio.com/products/rstudio/download/#download)

3. Install Git from [git-scm.com](https://git-scm.com/downloads). Use the default, recommended settings. It is especially important to leave these settings selected:
    + Git from the command line and also from third party software  
    <!--*The `worcs` R-package calls Git from the command line*-->
    + Use the 'OpenSSL' library  
    <!--*For secure data transfer with GitHub*-->
    + Checkout Windows-style, commit Unix-style line endings  
    <!--*This is the preferred setting when collaborating with others on different platforms. Be prepared that, on windows, you will receive harmless notifications about LF to CRLF line endings.  *-->
    + Enable Git Credential Manager  
    <!--*For logging in to GitHub*-->
    + If you run into any trouble, a more comprehensive tutorial on installing Git is available at [happygitwithr.com](https://happygitwithr.com/install-git.html).

4. Register on 'GitHub' (alternatively: see [this vignette](https://cjvanlissa.github.io/worcs/articles/git_cloud.html) on how to use 'GitLab' or 'Bitbucket')
    + Go to [github.com](https://github.com/) and click *Sign up*. Choose an "Individual", "Free" plan.
    <!-- + Request a [free academic upgrade](https://help.github.com/en/articles/applying-for-an-educator-or-researcher-discount). This allows you to create *private repositories*, which are only visible to you and selected collaborators, and can be made public when your work is published. -->

5. Connect 'RStudio' to Git and GitHub (for more support, see [this 'RStudio' article](https://support.rstudio.com/hc/en-us/articles/200532077-Version-Control-with-Git-and-SVN), and [this blog post](https://www.r-bloggers.com/2015/07/rstudio-and-github/))
    + Open 'RStudio', open the Tools menu, click *Global Options*, and click *Git/SVN*
    + Verify that *Enable version control interface for RStudio projects* is selected
    + Verify that *Git executable:* shows the location of git.exe. If it is missing, manually fix the location of the file.
    + Click *Create RSA Key*. Do not enter a passphrase. Press *Create*. A window with some information will open, which you can close.
    + Click *View public key*, and copy the entire text to the clipboard.
    + Close 'RStudio' (it might offer to restart by itself; this is fine)
    + Go to [github.com](https://github.com/)
    + Click your user icon, click *Settings*, and then select the *SSH and GPG keys* tab.
    + Click *New SSH key*. Give it an arbitrary name (e.g., your computer ID), and paste the public key from your clipboard into the box labeled *Key*.
    + Open 'RStudio' again (unless it restarted by itself)

6. Install all packages required for WORCS by running the following code in the 'RStudio' console. Be prepared for three contingencies:  
    + If you receive any error saying *There is no package called [package name]*, then run the code `install.packages("package name")`  
    + If you are prompted to update packages, just press [ENTER] to avoid updating packages. Updating packages this way in an interactive session sometimes leads to errors if the packages are loaded.  
    + If you see a pop-up dialog asking *Do you want to install from sources the package which needs compilation?*, click *No*.

```
install.packages("worcs", dependencies = TRUE)
tinytex::install_tinytex()
renv::consent(provided = TRUE)
```

If you do not have a Git user set up on your computer yet (e.g., if this is the first time you will be using Git), run the following - making sure to substitute your actual username and email:

```
worcs::git_user("your_name", "your_email", overwrite = TRUE)
```

If you intend to write documents in APA style, you should additionally install the `papaja` package.
Unfortunately, this package is not yet available on the central R repository CRAN, but you can install it from 'GitHub' using the following code:

```
remotes::install_github("crsh/papaja", dependencies = TRUE, update = "never")
```

Because `papaja` has many dependencies, it is recommended to skip this step if you intend to write documents in a different style than APA.

That's it! Everything should be installed and connected now.

## Test Your Setup

With this exercise we want to verify if your set-up was successful and the connection between RStudio & Git/GitHub is working smoothly.

1. **Create a new GitHub repository**

    + Login to [github.com](https://github.com/) 
    + Go to _Repositories_ and click the green 'New' button
    + Repository Name: `test`
    + Description: `repo to test my RStudio & Git/GitHub connection`
    + Visibility: Public
    + Initialize this repository with: _README_
    + .gitignore & license: _None_
    + Click the green 'Create repository' button

2. **Copy the repository SSH URL**

    + On your new repository page, click the green 'Code' button
    + Copy the SSH URL for the repository to your clipboard. It should be something like: `git@github.com:<USERNAME>/test.git`

3. **Create a new RStudio Project with Git version control**

    + In RStudio, select _File_ -> _New Project_ -> _Version Control_ -> _Git_
    + Repository URL: paste the SSH URL you just copied, it should be something like: `git@github.com:<USERNAME>/test.git`
    + Project directory name: `test`  
    + Create project as subdirectory of: _this is where you want your project folder to be located on your computer, make sure this is an easily accessible location_
    + Check 'Open in new window' or 'Open in new session'  
    + Click 'Create Project' 

The GitHub repository will be copied (or cloned in Git terms) into the specified project folder on your computer. You should immediately find yourself in a new local RStudio Project that represents your test repo on GitHub. 

The content of the GitHub repository should now appear in the "Files" pane of RStudio and you should see the _README.md_ file. Moreover, now that you have enabled git versioning for your Project, a “Git” tab should have been added to your interface next to “Environment” and “History” tabs.

4. **Push to GitHub**

    + Open the README.md file within RStudio and add a line like: `This is an edit from RStudio`. Don't forget to save the file.
    + Click the "Git" tab in the upper right pane
    + Check the 'Staged' box for README.md
    + If you're not already in the Git pop-up window, click 'Commit'
    + Type a simple, but meaningful message in the "Commit message" box such as _edited README.md in RStudio_
    + Click the 'Push' button (with the green upwards arrow) to upload your changes to GitHub. Note that you might be prompted to enter your GitHub username and password
    + Go to the test repository on GitHub and refresh the page, the local changes should now be visible online. You should see the `This is an edit from RStudio` line in the README.md file and the commit message your provided will be noted in the history of the file.

5. **Pull from GitHub**

    + Go to the README.md file within GitHub and click the _Pencil_ icon/button to edit the file. 
    + Add a line like: `This is an edit from GitHub` and commit (save) the change. Once again, use a simple, but meaningful commit message such as _edited README.md in GitHub_  
    + Go to the "Git" tab in RStudio and click the 'Pull' button (with the blue downwards arrow) to download the changes to your computer.
    + Your online changes should be visible locally. You should see the `This is an edit from GitHub` line in the README.md file.   

If you made it this far, congratulations! You're all set up to use RStudio and Git/GitHub and you even practiced the standard workflow of making commits + pushing + pulling.

## Troubleshooting

If you run into errors or issues, please use the drop-in call for _Installation & Set-Up Support_. You should have received the MS Teams link to this in the Welcome email for the course. 
You can also email one of the course instructors: Neha Moopen (n.moopen@uu.nl).

Since this course is still in it's pilot phase, we don't an extensive have troubleshooting guide yet. We will be updating this section as we hear from partcipants about their issues. 
Just follow the steps and don't worry if you don't fully understand some of the technical language, this troubleshooting guide is also for instructors to refer to.

1. **The Push/Pull buttons in my RStudio are greyed out or not clickable**

This usually means that RStudio doesn’t know the exact location of your remote repository (e.g. on GitHub). 
More specifically, it may not yet know which branch to track within the remote repository (e.g. origin).

To fix this, try the following:
 
 + Open a terminal to the working directory of your project
   
   The "Terminal" tab is next to the "Console" tab in RStudio. Click on the "Terminal" tab and a new terminal session will be created (if there isn't one already). 
   If the tab isn't visible, show it via **Shift+Alt+T** or using the menu: _Tools_ -> _Terminal_ -> _Move Focus To Terminal_

   In the terminal, type `cd <PATH\TO\THE\WORKING\DIRECTORY\OF\YOUR\PROJECT>`. The `cd` command stands for 'change directory'.
   
 + Check if the git remote was set up alright
    
   In the terminal, type `git remote -v`
   
   You should get something like: 

   `origin git@github.com:<USERNAME>/test.git (fetch)`
   `origin git@github.com:<USERNAME>/test.git (push)`
   
   In the unlikely case that there is no remot set up, then copy the SSH URL for your repository again and type:
   
   `git remote add origin git@github.com:<USERNAME>/test.git`
   
 + Tell RStudio to track the main branch of your remote repository
   
   In the terminal, type `git push --set-upstream origin main`
   This above is equivalent to `git push -u origin main` but conveys more information about what is intended. Essentially, we're ensuring the local `main` branch is set to track the `main` branch on GitHub.
 
 + Restart RStudio and try Pushing and/or Pulling again.
   
---
