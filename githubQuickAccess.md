# GitHub Quick Access Desktop Utility (githubQuickAccess)

## [Video]

## About

- Rapid prototyping excites me and I am always looking for ways to improve my workflow. This video demonstrates two desktop features that help automate the process of setting up GitHub repositories and GitHub gists directly from your local machine.
- I created these features because I wanted to:
  - Spend more time creating an idea and less time fiddling around with the set up.
  - Make it easier and quicker to share ideas with fellow programmers.

## Issue

- Using the browser to set up GitHub repositories and gists is slow and tedious.
- When you are trying to code an idea quickly, needing to navigate to GitHub to set up infrastructure before you can share your code causes a break in your natural workflow and train of thought.

## Task

- The aim of this project is to automate the browser tasks of creating GitHub repositories and gists.
- Create GitHub repositories and gists directly from the local machine through GitHub's API.
- Add custom GitHub commands to the Windows context menu:
  - Command #1: Creates a new GitHub repository from a directory,
  - Command #2: Creates a new GitHub gist from a file.

## Action

- Front End:
  - Create new context menu items for the commands by adding the appropriate registry keys to the Windows Registry.
- Back End:
  - Connect the context menu commands to a Python program through a Windows Batch Script file (.cmd).
  - Use the Python program to connect with the GitHub API to create repositories and gists.

## Result

- By streamlining the process of creating GitHub repositories and gists directly from your local environment, you can achieve higher productivity and quicker collaboration.
- You can move from an abstract idea to written code immediately without having to navigate through the tedious setup procedures.
- Once you are ready to share an idea, you are only a single click away from doing so.

## Features Built Using

### [Python 3.7.3](https://www.python.org/ )

- Modules
  - [os](https://docs.python.org/3.7/library/os.html?highlight=os#module-os "Miscellaneous operating system interfaces")
  - [json](https://docs.python.org/3.7/library/json.html "JSON encoder and decoder")
  - [requests](https://pypi.org/project/requests/, "pip install requests")
  - [pyperclip](https://pypi.org/project/pyperclip/ "pip install pyperclip")

### [GitHub API v3](https://developer.github.com/v3/)

- [Create a gist](https://developer.github.com/v3/gists/#create-a-gist)
  - Endpoint: POST /gists
- [Create a repository](https://developer.github.com/v3/repos/#create)
  - Endpoint: POST /user/repos

### Windows (.cmd) Batch Script

- Windows Batch Scripting
  - <https://steve-jansen.github.io/guides/windows-batch-scripting/index.html>
  - <https://www.tutorialspoint.com/batch_script/>
- Parameter Extensions
  - <https://ss64.com/nt/syntax-args.html>
- Windows Environmental Variables
  - <https://docs.microsoft.com/en-us/windows/deployment/usmt/usmt-recognized-environment-variables>
  - <https://www.itprotoday.com/cloud-computing/what-environment-variables-are-available-windows>

### Windows Registry (Context Menu Items)

- <https://www.howtogeek.com/107965/how-to-add-any-application-shortcut-to-windows-explorers-context-menu/>
- <https://www.howtogeek.com/370022/windows-registry-demystified-what-you-can-do-with-it/>
- <https://www.howtogeek.com/school/using-windows-admin-tools-like-a-pro/lesson5/>

<!-- ===================================================== -->

## Outline

- Video demo of desktop GitHub features:
  - (1) Create a GitHub repository locally.
    - Right-click on directory
  - (2) Create a GitHub Gist directly from any file on your computer.
    - Right-click on a file
  - (3) Quick save from a repository that is already on your Desktop.
    - Right-click on directory
    - Right-click on a file

## Commentary

- Other Methods (Contrast):
  - Manually
    - Workflow:
      - Idea --> Log into GitHub --> Create new repo on GitHub  --> Clone GitHub repo to local machine --> Start coding idea --> Push code to GitHub repo --> Share code
        - Lots of navigation, need to sign in.
      - Idea --> Start coding idea locally --> Log into GitHub --> Create new repo on GitHub --> Set up git remote for local project --> Push code to GitHub  --> Share code
        - Lots of navigation, need to sign in.
      - Idea --> Start coding idea locally --> Create GitHub repo, push to GitHub repo, share code
    - You want to start building usually directly on your local machine.
  - GitHub Desktop
    - Need to open another application. Form-like approach, need to sign in.
  - Selenium Approach
    - <https://youtu.be/7Y8Ppin12r4>
