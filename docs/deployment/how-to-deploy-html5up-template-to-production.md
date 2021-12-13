---
title: Deploy an HTML5 template to production
description: A guide on how to deploy an HTML5 template from GitHub.
---

# How to Deploy an HTML5 Template to Production on Code Capsules

Deploy an HTML5 template and learn how to host frontend code on Code Capsules. 

## Set up

Code Capsules connects to GitHub repositories to deploy applications. To follow this guide, you’ll need a [Code Capsules](https://codecapsules.io/) account and a [GitHub](https://github.com/) account.

To demonstrate how to deploy an HTML5 template to Code Capsules, we'll be using a template from [HTML5up](https://html5up.net/). Head over to the HTML5up site and download the zip file for any template you find there. Unzip this template file in your preferred working directory on your local machine.

## Create a Repository

Sign in to GitHub and create a repository for the template site you downloaded.

We'll need to push the unzipped template files to your newly created repository for Code Capsules to deploy the template site from your GitHub account. To do this, initialize a git repository in the project's root folder on your machine by running the command `git init` from a terminal window while in the root folder. 

## Push to GitHub

Before you can push to GitHub, you need to add the untracked files to your local repository. Run `git add -A` in a terminal window from the project's root folder to do so. After adding the files, commit your changes by running `git commit -m "Initial app commit"`.

Run the command below to set the remote repository for your local repo. Be sure to replace `<YOUR-REMOTE-GITHUB-URL>` with the actual URL for your remote repository. 

```
git remote add origin <YOUR-REMOTE-GITHUB-URL>
```

Push the unzipped files to your remote repository by running `git push origin main`.

## Link to GitHub

To link Code Capsules to your remote GitHub repository, log in to your Code Capsules account and click your profile image at the top right of the screen and find the “GitHub” button under “GitHub Details”.

![git-button](../assets/deployment/html/git-button.png)

Click the “GitHub” button, select your GitHub username, and do the following in the dialog box that appears:

1. Select “Only Select Repositories”.
2. Choose the GitHub repository you recently pushed to.
3. Press “Install & Authorize”.

![Install & authorize github](../assets/deployment/html/github-integration.png)

## Add Repository to Team

Select “Team Settings” in the top navigation bar to switch to the Team Settings tab.

Click on the “Modify” button under the “Team Repos” section. An “Edit Team Repos” screen will slide in from the right. Click “Add” next to the demo repo, and then “Confirm”. All the Spaces in your Team will now have access to this repo.

![Edit Team Repos](../assets/deployment/html/team-repos.gif)

## Create a Space for your Site

[Spaces](https://codecapsules.io/docs/FAQ/what-is-a-space/) are an organisational tool for your applications. You can select the Personal Space that you find in your default Personal Team to host this site, or you can create a new Space. In the “Spaces” tab, click the “Create A New Space For Your Apps” button. 

Follow the prompts, choosing your region and giving your Space a name, then click “Create Space”.

![space name](../assets/deployment/html/space-name.png)

## Create the Capsule

A [Capsule](https://codecapsules.io/docs/FAQ/what-is-a-capsule/) provides the server for hosting an application on Code Capsules.

Navigate to the “Spaces” tab and open the Space you’ll be using.

Click the “Create a New Capsule for Your Space” button, and follow the instructions below:

1. Choose “Frontend Capsule”.
2. Under “Product”, select “Trial - Static Site Hosting”.
3. Choose the GitHub repository with the HTML5up site.
4. Press “Next”.
5. Leave the “Build command” and “Static content folder path” blank. 
6. Click “Create Capsule”.

Code Capsules will automatically build your application when you’ve finished creating the Capsule. While the build is in progress, you can view the log by clicking “View Build Progress” next to the “Building Capsule” message.

Once your application is live, you can view the build log by selecting the “Deploy” tab and clicking the “View build log” link in the “Builds” section. 

![Build logs](../assets/deployment/html/frontend-capsule-build-logs.png)

Once the build is complete, a “Live Website” link will appear at the top of the tab. Click the link and you should see your deployed site.

![Deployed App](../assets/deployment/html/html5up-site.png)

If you’d like to deploy another application in a different language or framework, take a look at our other [deployment guides](/docs/deployment/).
