# Lab 0

Data analysis workflow example using R notebooks.


## Setup

- Install software: [*R*](https://cran.r-project.org), [*RStudio*](https://www.rstudio.com/products/rstudio/download/#download), and Git

  * Git on Windows: [Git for Windows](https://gitforwindows.org)
  
  > **Important**: when installing, choose "*Use Git from the Windows Command Prompt*"!
  
  * Git on Mac:
  ```sh
  $ xcode-select --install
  ```
  or install [Homebrew](https://brew.sh) and then
  ```sh
  $ brew install git
  ```

---

## GitHub

- Go to [GitHub](https://github.com) and hit *Sign Up*

- **Important**: use your `bu.edu` email when registering!

- Tips on picking a username<sup>1</sup>:
.footnote[<sup>1</sup>Thanks to [Happy Git with R](http://happygitwithr.com)!]

  * Incorporate your actual name! People like to know who they’re dealing with. Also makes your username easier for people to guess or remember.
  
  * Reuse your username from other contexts, e.g., Twitter or Slack.
  
  * Pick a username you will be comfortable revealing to your future boss.
  
  * Be as unique as possible in as few characters as possible. 
Make it timeless. Don’t highlight your current university, employer, or place of residence.

  * Avoid words laden with special meaning in programming, such as `NULL` and `NA`.

- Now head to BB and complete the survey!

---

## Git setup

- In RStudio, open a shell (`Tools > Shell`) and enter

```sh
git config --global user.name "Your name"
git config --global user.email "your@e.mail"
```

- Check with

```sh
git config --global user.name
git config --global user.email
```

---

## Quick exercise

- Go to the public repository [`sussmanbu/ma415-lab0`](https://github.com/sussmanbu/ma415-lab0/)and "clone" it:

  * Click on "Clone or download" and copy the link under "Clone with HTTPS"

  .center[![](figures/github-lab0.png)]

  * In RStudio: create a new project (`File > New Project`), then select "Version Control", "Git", and provide the copied link from GitHub as the "Repository URL". Specify the path for the project (and **do not forget** it!)

  * Done! For now, just notice the Git tab and the project menu in the top right corner