# Hosting Your Resume on GitHub Pages: A Step-by-Step Guide for Beginners

## Purpose

This guide shows the steps on how to host and format a Markdown resume on GitHub Pages, a static site hosting service that can utilize the static site generator Jekyll, while relating the process to the technical writing principles from Andrew Etter's book "Modern Technical Writing".

## Prerequisites

- A resume formatted in Markdown.
- A [GitHub](https://github.com) Account.
- Git installed and setup. [Installation Guide](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git). [Setup Guide](https://docs.github.com/en/get-started/getting-started-with-git/set-up-git).
- Visual Studio Code or a similar source-code editor installed. [Installation Guide](https://code.visualstudio.com/docs/setup/setup-overview).

## Instructions

#### Creating a New Repository on GitHub

1. Log into your GitHub account.
2. Click the `New` button to create a new repository. A repository is essentially a directory in GitHub.
   ![New repo button](graphics/newrepo.png)
3. Name the repository `yourusername.github.io`, replacing `yourusername` with your actual GitHub username.
4. Create the repository with a README file by clicking on the checkbox labeled `Add a README file` and then clicking `Create repository`.
   ![Creating a new repo](graphics/createnewrepo.png)

**Note**: Utilizing GitHub exemplifies Etter's recommendation to share and host documents on a distributed version control system.

#### Cloning Your Repository

1. Copy the repository's link to your clipboard by clicking the `Code` button within your repository and then clicking on the two boxes layered over one another.
   ![Copying the repository URL link](graphics/gitclonebutton.png)
2. Open your terminal.
   - As an example for macOS:
     - Press the `command⌘` and `space bar` keys at the same time. This will open Spotlight Search.
     - Type "terminal".
     - Press enter or click the application.
3. Clone your repository to your computer by typing the `git clone` command followed by your repository's URL. This will create a new folder in your computer that mimics the GitHub repository.
   ![Git clone in command line](graphics/gitclonecmd.png)

**Note**: Cloning is a concept within Git that facilitates distributed version control. The concept allows a new edited version of the document to be created and later shared as the main source of truth containing the current state of the document. This exemplifies the use of a distributed version control system as advocated by Etter.

#### Adding Your Resume to the Repository

8. Open Visual Studio Code.
   - As an example for macOS:
     - Press "command+space". This will open the spotlight search.
     - Type "Visual Studio Code".
     - Press enter or click the application.
9. Open the newly created folder that is now titled `yourusername.github.io`.
   - As an example for macOS:
     - Press the `File` button located on the top right hand of the application. This will open your file system.
     - ![Open Folder VSCode](graphics/openfolder.png)
     - Navigate to and click the folder `yourusername.github.io`.
10. Ensure your Markdown-formatted resume is named `index.md`.
11. Place the resume in the cloned repository folder on your computer.
12. Navigate to the `yourusername.github.io` folder in the terminal.
    - As an example for Visual Studio Code in macOS:
      - Press the `Terminal` button located on the top right hand of the application. This will open the terminal conveniently situated within your current folder.
      - ![VSCode Terminal](graphics/terminal.png)
13. Use Git to upload your resume on GitHub. This can be done by typing and entering the following commands sequentially in the terminal:

    - `git add index.md`
    - `git commit -m "Add my resume"`
    - `git push`

**Note**: Markdown exemplifies Etter's recommendation in using a lightweight markup language.

#### Viewing Your Resume Online

13. Navigate to your github repository.
    - A simple way to do this is to open your preferred web browser and go to the link `https://github.com/yourusername/yourusername.github.io/`
14. Click on the `Actions` tab to see if the resume has been generated and is online.
    - If the workflow similar shown to the one below shows a green checkmark, the resume is now online.
    - ![GitHub Pages Resume Deployed](graphics/deployed.png)
    - Your resume is now live at `https://yourusername.github.io`.

**Note**: Implicitly deploying through GitHub Pages' built in site hosting by following all the previous steps exemplifies Etter's recommendation of using static site generator to present a document.

### Formatting Your Resume

15. Create a file inside the `yourusername.github.io` folder called `_config.yml`.
16. Copy and paste the following Jekyll formatting instructions inside the file:

```
remote_theme: pages-themes/minimal@v0.2.0
plugins:
  - jekyll-remote-theme
```

17. Use Git to apply a minimal formatting to your resume, which can be seen at the same previous site `https://yourusername.github.io`. This can be done by typing and entering the following commands sequentially:
    - `git add _config.yml`
    - `git commit -m "Add formatting to my resume"`
    - `git push`

**Note**: Formatting the deployed resume through GitHub Pages' built in synergy with Jekyll by following the previous step exemplifies Etter's recommendation of formatting a document with a static site generator.

#### Example Resume Deployed Online

![Resume Deployed on GitHubPages](graphics/BriczCruzMarkdownResume.gif)

## More Resources

- [Markdown tutorial](https://www.markdowntutorial.com/)
- [Learn more about Jekyll and static site generators](https://jekyllrb.com/docs/)
- [Learn more about GitHub Pages and static site hosting services](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages)
- [Learn more about GitHub and distributed version control systems](https://docs.github.com/en/get-started/using-git/about-git)

## Authors and Acknowledgements

Credits to the [template contributors](https://github.com/pages-themes/minimal/graphs/contributors) and my team members Izan Cuetara Diez & NhatAnh Nguyen.

## FAQs

1. **Why is Markdown better than a word processor for resumes?**

   - Markdown is better than a word processor for resumes because of its simplicity and usability across various platforms. It allows users to focus on content through its strict and uniform formatting framework and usage. Since the format is enforced through symbols and syntax, it can be done through any text editor, making it lightweight unlike word processors.

2. **Why is my resume not showing up on GitHub Pages?**
   - Please see [this troubleshooting document](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-404-errors-for-github-pages-sites) to figure out why your resume is not showing up on GitHub Pages.
