#Cloud Compass Inc. Digital Literacy Course - DevOps for Business Managers - Lab 1

##Introduction

In this exercise, you will be going through a set of steps similar to those that a developer would follow in implementing a new feature, or a bug fix, including deploying an updated build into a live environment.  The purpose of this exercise is for you to gain an understanding of the workflow, as well as the supporting tools that work together to provide the automation.
  
This exercise makes use of a basic "ToDo List" web application.  In the course of this exercise, you will learn:
 
* how to access and navigate in Github
* how code is stored and organized on GitHub
* how edits to source code can trigger builds and deployments in a DevOps environment such as OpenShift.

Each student will have the use of their own repository for this exercise, but please ensure that you access your *assigned repo only* to avoid causing confusion for another student.

Before proceeding, make sure you have the label provided with your workbook, as it has links and login details that you'll need in the steps below.

##Setup

For this exercise to work best, open your browser, and open separate tabs for each of:
 
 * <a href="https://github.com" target="github">GitHub</a>
 * <a href="https://https://master.labs.cloudcompass.ca:8443" target="openshift">OpenShift Console</a>
 
##Access your deployed ToDo List web application
 
The starting point of the exercise is that a version of the ToDo application has been deployed for each student with a unique url, which will have been provided to you along with your workbook.

To view your version of the ToDo application:

* In a new tab, open your web browser to the URL provided.
* Enter some items in the ToDo list.
* Congratulations, your life is now 17% more organized!

##Access your repository on GitHub

Each student's label will have a GitHub username+password, along with the name of a repository that they will use for this part of the exercise.

Each instance of the deployed ToDo application has a distinct repository in GitHub to allow students to work independently.

The steps to find your way to your assigned GitHub repository are as follows:

* In your GitHub browser tab, login to GitHub. (If you're a keener and have already logged into GitHub with your own personal account, log out prior to doing this step) 
* Enter the username and password provided on your label
* Switch to the "C3IDigitalLiteracyLab" organization in GitHub by using the drop-down list in the middle of the page towards the left.  Select "C3IDigitalLiteracyLab".  Then click the button labeled "View C3IDigitalLiteracyLab" at the top right of the page.  
* You should see a list of repositories.  Select the repository in this list that corresponds to the one on your label.
* You should see a list of files. These are the contents of the repository.
* Congratulations! You have now completed GitHub Competency Level 1! 

##Edit a source code file

Each of the files listed in the repository you navigate to above are a part of the ToDo application, or some form of supporting material.  You will be making a change to the contents of one of these files, and then watching how it propagates through the build and deployment tooling.
 
To perform your edits:

* Locate the file "index.html" in the repository's file list and click it. The screen will update and display the contents (code) of the file.
* Switch to to the tab showing your ToDo app. Notice the title of the app is "todos" and the prompt is "What needs to be done?".  We want to change these to something awesome.
* Switch back to your GitHub tab.
* Find the Edit (pencil) button at the top-right of the area showing the source code and click it. You're now in Edit mode.
* Go to line 16 in the source code and change the text `<h1>todos</h1>` to `<h1>awesome list</h1>`
* Go to line 18 in the srouce code and change the text `placeholder="What needs to be done?"` to `placeholder="How to be awesome..."`
* Scroll to the very bottom of the page and in the "Update" field of the Commit changes" section, type something like "make app more awesome" and then click the green "Commit changes" button underneath.
* Congratulations, you're now a junior front-end dev!
  
##Follow build and deploy process

The GitHub repository containing the file you edited above is connected to an OpenShift build and will build and deploy a new version of your ToDo app for every change you make to your GitHub repository.

In this exercise, we're going to explore OpenShift a little bit to see some of the pieces that work together to build and run your app.

* Switch to your browser OpensShift tab.
* Log in to OpenShift using the username+password on your label.
* You should see a project list (containing a single project).  It will be named something like "Digital Literacy Course Lab..."
* Click the project name.  You should now see an overview of all of the components that make up your project's home in OpenShift.
* Depending on how quickly your code edits from the prior part exercise took to process, you may see a build happening (progress indicator near the top of the page), or a brand-new deployment (text like "Deployment Config lab - a few seconds ago"), meaning the build has already completed.
* If the new deployment is complete, switch to your ToDo app browser tab and refresh the page.  Your (awesome) edits should appear.
* If the build is still running, wait for it to complete, and watch the blue glowing ring (ooh! glowing things!) as it deploys afterwards, then check for your changes in your ToDo app browser tab.
* Congratulations you're now a DevOps Apprentice Level 1!



