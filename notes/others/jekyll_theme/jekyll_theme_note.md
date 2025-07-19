# How to host and format a resume using Jekyll and GitHub Pages

## Purpose
- You can host a Markdown format resume on GitHub by using GitHub Pages and GitHub Pages built-in support Jekyll. This documentation will contains the step-by step instructions on how to host a Markdown format resume on GitHub, and also introduces the principles of Andrew Etter's book [Modern Technical Writing](https://www.oberlo.ca/blog/markdown-editors).  

## Prerequisites
- Markdown Language
  - Basic Markdown knowledge is required for this tutorial, there is a link under the [More Resources](#More-Resources) section for the Markdown tutorial.
- Markdown Editor
  - Most of the Markdown editors are easy to use and able to export the content into multiple formats files such as HTML and PDF. There is a link under the [More Resources](#More-Resources) section for a variety of Markdown editor choices.
- Resume in Markdown format
  - A Resume in Markdown format is required in order to host the resume on GitHub.

## Instructions
Below is the step-by-step tutorial for hosting a resume using GitHub Pages and Jekyll. Instructions will be subdivided into sections, in every section will have steps of instructions.

### Creating a GitHub account
  1. If you do not have a GitHub account yet, go to the [GitHub homepage](https://github.com/), in the top left corner, and select the signup button to create a GitHub account. After the account is created, log in to your account.
  - ![Image](/docs/gitSignUP.png)

### Creating a repositories
##### Etter encourages developers to store documentation in the same repository as its corresponding website or source code, so that the documentation and source code branches will always stay in sync.
  1. Alternatively, you can also use an existing repository for hosting your resume.
      - If you would like to create a new repository, continue to step 2.
      - If you would like to host your resume with an existing repository, skip to the "Configuring a publishing source for your GitHub Pages website" section.
  2. In your GitHub profile homepage, in the upper-right corner, select the "+" icon for the drop-down menu, and select "New repository". 
  3. Under the "Repository name", type a name for your repository.
  -  ![Image](/docs/gitRepoName.png)
  4. Make sure your repository is set to public.
  5. Add a README file to your repository automatically by checking the "Add a README file" checkbox.
  6. Select "Create repository" at around the bottom of the page.

### Configuring a publishing source for your GitHub Pages website 
  1. Go to your repository, at around the top right of the page select the "Settings".
  2. On the left side of the page, select the "Pages" section.
  3. Under the "Build and deployment" section:
   - Under the "Source", select "Deploy from a branch".
   - Under the "Branch", select the branch where you want to store your resume. If you would like to store your resume in a folder, make sure to set to the specific folder for your publishing source.
   - ![Image](/docs/gitConfigBranch.png)![Image](/docs/gitConfigBranch2.png)
  4. select "Save".
    
### Upload your Markdown format resume to your GitHub repository
##### Markdown is a lightweight markup language, there are several good reasons why we should use lightweight markup languages. First, it is easy to read and write Markdown code, and it also makes code looks simple and clean compared to HTML. In Etter's book, he used a lightweight markup language called AsciiDoc and another type of markup language called Docbook to write the same function of code, the result is the code that wrote using AsciiDoc is 7 times lesser than Docbook. Which shows the advantages of using lightweight markup language.
  1. In your computer, make sure your Markdown format resume is named "index.md", if not please rename your resume file.
  2. At around the top left page, select the "Code" section.
  3. Select "Add file".
  4. Select "Upload file", then upload your Markdown format resume, and optionally you can leave a message and description under the "Commit changes" section.
   - ![Image](/docs/gitUploadFile.png)
  5. Select "Commit changes" at around the bottom of the page.
  
### Creating a Jekyll template for your static website
##### Etter also highly recommends using static site generators for documentation because, unlike dynamic sites, the static site does not have dependencies issues, so it is easy to migrate the entire website.  
  1. Still in the code section, select "Add file".
  2. select "Create new file", then name your file as "_config.yml".
   - ![Image](/docs/gitCreateFile.png) 
  3. Scroll to bottom of the page, optionally you can add some message and description for this change under "Commit new file" section.
  4. Select "Commit new file".
  5. Go to GitHub Pages' [Supported themes website](https://pages.github.com/themes/), there is a variety of supported themes you can choose from, simply select any one of the themes and you will go to the GitHub repository page of the supported theme, and under the README.md section, select the "preview the theme to see what it looks like" will show you how is the theme looks like.
   - ![Image](/docs/gitThemePreview.png)  
  6. Select a theme that you would like to use.
  7. Once you have decided which supported theme you would like to use, select the themes, and got to the README.md section, and under the "Usage" section, follow the first step, add the following codes to your "_config.yml" file.
   - ![Image](/docs/gitAddConfig.png)

### Hosting your resume to GitHub server
##### In Etter's book, he encourages editors to use Websites for documentation instead of PDFs, because most of the documentation will eventually become outdated, when we have options for readers to save the PDFs to their computer locally, there are chances that some readers might have read the outdated documentations. So using websites, the reader can ensure they always have the updated version of the documentation.  
  1. At the code section, at around bottom right of the page, Under "Environments" section, select "github-pages"
   - ![Image](/docs/gitGhPages.png)
  2. At right side of the page, select "View deployment".
   - ![Image](/docs/gitViewDeploy.png)
  3. Now you are able to see your resume on the website hosted by GitHub server.
  4. Your page will look similar to [this](https://yunji0387.github.io/).
   - ![GIF](/docs/myResume.gif)

## More Resources
-  Markdown Language Tutorial
   - To learn more about markdown language, [here is the link for tutorial.](https://www.markdowntutorial.com/)
- Markdown Editor List 
  - [here is the link for list of Markdown Editor list](https://www.oberlo.ca/blog/markdown-editors)
-  Book : Modern Technical Writing
   - This [book](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS) is written by Andrew Etter.
-  Article : Review of Andrew Etter's ebook on Modern Technical Writing
   -  [link for the article](https://idratherbewriting.com/2016/07/26/modern-technical-writing-review/) 

## Authors and Acknowledgments
- Authors
  - [How Yun Ji](https://github.com/yunji0387)
- template authors
  - [Steve Smith](https://github.com/orderedlist), GitHub,Inc.
- Group members
  - [Kim Gyuri](https://github.com/gyuyuu)
  - [Anghan Dharmit Kishorbhai](https://github.com/dkanghan)
  - [Ahir Md Ahiduzzaman](https://github.com/ahirgit)

## FAQs
- Why is Jekyll better than HTML?
    - Jekyll automatically generates a website for us to use rather than creating a website from scratch, which is more efficient. And also, the code is well-structured and easy to edit.
processor?
- Why is my resume not showing up?
    - remember to check your GitHub pages publishing source is set to the branch that contains the markdown that you want to render.
    -  more information can be view in [Configuring a publishing source for your GitHub Pages website](#Configuring-a-publishing-source-for-your-GitHub-Pages-website) section under instruction section.

## Reference
- Etter, A. (2016). Modern Technical Writing. Andrew Etter. 
  - https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS
- Johnson, T. (2016) Review of Andrew Etter's ebook on modern technical writing.
  - https://idratherbewriting.com/2016/07/26/modern-technical-writing-review/
