# Getting started:

Follow these steps to install everything on your own computer (for offline use). Alternatively, get started quicker by [Using RStudio Cloud](#alternative-use-rstudio-cloud).
## 1. R

Download and install the latest version of R from:

https://www.stats.bris.ac.uk/R/

*Windows*: `Download R for Windows` - `base` - `Download R 3.6.0 for Windows`

*Mac*: `Download R for (Mac) OS X` - `R-3.6.0.pkg`

## 2. RStudio

Then download and install RStudio:

https://www.rstudio.com/products/rstudio/download/#download

*Windows*: `RStudio 1.2.1335 - Windows 7+`

*Mac*: `RStudio 1.2.1335 - Mac OS X 10.12+ (64-bit)`

## 3. R packages

### 3.1 Open RStudio and copy-paste the lines below into the Console and press Enter:

```{r}

healthyr_notebooks = c("tidyverse", "boot", "finalfit", "flexdashboard",
"gapminder", "here", "kableExtra", "knitr", "remotes",
"rmarkdown", "shiny", "survminer", "tinytex", "patchwork")
install.packages(healthyr_notebooks)

```

### 3.2 Then Restart R

## 3.3 to then run these this line (same as before, copy-paste to the Console):

```{r}

tinytex::install_tinytex()

```

If it asks you "Do you want to restart your R session", press **Yes** the first time. If it immediately asks again, press **No**.

Code to check tinyTex and Tex working as expected:

```{r, eval = FALSE}

tinytex:::is_tinytex()

#  If installed should return `TRUE`.
# Notice the triple colon, this is because it's an internal variable name.

```

### Troubleshooting 3.3

1. ~"can't find remotes": try doing step 3.2 (restart) again.
We only just installed `remotes::` in *3.1* so RStudio needs a restart before we can start using it.

2. ~"TeX failed, you already have a TeX distribution...". 
If you already have LaTex installed on your computer, the `tinytex::install_tinytex()` one is not necessary and might not work.  This is fine, there is no harm in copy-pasting in anyway if you are not sure.

## 4. Download course materials

1. Click on `Clone or download` then `Download ZIP` (top-right of this GitHub page)
2. Unzip the folder and rename it to just healthyr (so from `healthyr_notebooks_materials-master` to `healthyr`).
3. Move this folder to where you will be keeping your R projects. Each RStudio project is in a separate folder, but you can always move them afterwards (e.g. into a new folder called R-projects).
4. Open RStudio. Click on New Project.
5. Select "Existing Directory".
6. Browse to find your `healthyr` folder, then `Create Project`.
7. Click on the `01_introduction` folder in the Files pane (bottom-right), then open `01_introduction.Rmd`.

# Alternative: Use RStudio Cloud

RStudio cloud is a free online platform for learning R. It saves you from installing R and RStudio yourself, but it does mean you need an internet connection to access it via a web browser.

1. Create an account on RStudio cloud (these replace steps 1. and 2. from *Getting Started*).
2. Go to "Your workspace"
3. Click on the selection arrow next to "New project" and select "New Project from Git Repo" (this reaplaces step 4. of *Getting started*)
4. After the project has loaded, copy-paste the lines below into the Console and press Enter:

```
healthyr_notebooks = c("tidyverse", "boot", "finalfit", "flexdashboard",
"gapminder", "here", "kableExtra", "knitr", "remotes", "rmarkdown",
"shiny", "survminer", "tinytex")
install.packages(healthyr_notebooks)
```

5. Then Restart R (top menu Session - Restart R) to then run this line (same as before, copy-paste to the Console):

```
remotes::install_github("thomasp85/patchwork")
```

6. Click on the `01_introduction` folder in the Files pane (bottom-right), then open `01_introduction.Rmd`.

# Alternative: Create a new shared space on RStudio cloud

If you want to help your friends to learn R, then you can set up a shared space on RStudio Cloud.

1. Create a new space (click on `+ New Space`)
2. Create a new project following the RStudio Cloud instructions 3., 4., 5. from above
3. Find "Access" (Settings), set "Who can view this project" to Everyone (default is You, don't worry this is still everyone in the private space)
4. Set it as the Base project of this space (https://rstudio.cloud/learn/guide)
5. Invite people to join your space - any new projects they create will automatically get the files and packages of the Base project
6. After sucefully setting the Base project and testing that a new project has all the files etc you should make your first project private again (Settings, Access, Who can view, You). Otherwise people will get confused and start working directly 


# Alternative: Join an existing space on RStudio Cloud

1.	Get in invite to a an RStudio Cloud space where these materials are already set up
2.	Create an account or Log in with Google or GitHub
3.	Click on “Join Space”
4.	Click on “Projects” at the top
5.	Click on “New Project” and wait while “Deploying project” completes
