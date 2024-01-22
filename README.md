# Lab 0

Data analysis workflow example using R notebooks.

## Setup

Please ask questions if you have them.

Install software:

---

* [*R*](https://cran.r-project.org)
  * Click the download link for your OS.
  * If you have a previous installation, I would still recommend downloading and installing the latest version.
* [*RStudio*](https://www.rstudio.com/products/rstudio/download/#download)
  * Select the link for your OS (usually in the blue box under _2._ the top) and follow the instructions.

---

* Git
  * Git on Windows: [Git for Windows](https://gitforwindows.org)
  
  > **Important**: when installing, choose "*Use Git from the Windows Command Prompt*"!
  > Otherwise, defaults should be OK.
  
  * Git on Mac. In a terminal, run
  ```sh
  xcode-select --install
  ```
  or install [Homebrew](https://brew.sh) and then
  ```sh
  brew install git
  ```

---
layout:false

## R Packages

- If you had RStudio open when you installed Git, close RStudio.
- Start RStudio
- Click the `Console` panel and run the following command.

```r
install.packages(
  c(
    "tidyverse", "devtools", "knitr",
    "arrow", "babynames", "curl", "duckdb", "gapminder", 
    "ggrepel", "ggridges", "ggthemes", "hexbin", "janitor", "Lahman", 
    "leaflet", "maps", "nycflights13", "openxlsx", "palmerpenguins", 
    "repurrrsive", "tidymodels", "writexl"
  )
)
```

This will probably take while.


---

## GitHub

- Go to [GitHub](https://github.com) and hit *Sign Up*

- If you can, use your `bu.edu` email when registering!

- Tips on picking a username<sup>1</sup>:
.footnote[<sup>1</sup>Thanks to [Happy Git with R](http://happygitwithr.com)!]

  * Incorporate your actual name! People like to know who they’re dealing with. Also makes your username easier for people to guess or remember.
  
  * Reuse your username from other contexts, e.g., Twitter or Slack.
  
  * Pick a username you will be comfortable revealing to your future boss.
  
  * Make it timeless. Don’t highlight your current university, employer, or place of residence.

  * Avoid words laden with special meaning in programming, such as `NULL` and `NA`.

---
layout:true

## Git/Github setup in RStudio

---

- In the Console in RStudio, copy and paste the code below, replace `#YOUR NAME#` and `#EMAIL@bu.edu#` with your full name and BU email address, and run

```r
usethis::use_git_config(
  user.name = "#YOUR NAME#",
  user.email = "#EMAIL@bu.edu#"
)
```

so for example, I would write

```R
usethis::use_git_config(
  user.name = "Daniel Sussman",
  user.email = "sussman@bu.edu"
)
```

---

- Next, we're going to set up your authentication for Github. Run 

```r
usethis::create_github_token(description = "MA 415 SP2022")
```

This will open a tab in your browser to create a new Github personal access token. (You might need to sign in first.)

__Make sure not to close the tab.__

On this page, click on "30 days" underneath "Expiration" and click "Custom..." and choose "12/22/2022" as the expiration date.

Scroll to the bottom and click "Generate token". 

__Make sure not to close the tab.__

---

- Go back to RStudio and run 

```{r}
gitcreds::gitcreds_set()
```

If it asks select 2 by typing 2 and pressing enter.

When you get to `? Enter new password or token: `, go back to your browser and copy the token and paste it in the console and press enter.
The token will look something like `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`.

- Next, run

```r
usethis::git_vaccinate()
```

This adds some items to your global `.gitignore` that will help avoid common problems and increase security. 

---

- Finally, run 

```r
usethis::git_sitrep()
```

This will give a summary of the situation with Git and Github and should indicate your Name, Email, and the fact that you set up a Github PAT.