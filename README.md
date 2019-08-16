# HealthyR Notebooks course on RStudio Cloud:

1.	Go to https://rstudio.cloud/spaces/20603/join?access_code=loFjFYH4SU4q9uQX5Ymqkd6reLjK9vlbkXAMyeFX

2.	Create an account or Log in with Google or GitHub
3.	Click on “Join Space”
4.	Click on “Projects” at the top
5.	Click on “New Project” and wait while “Deploying project” completes

# Alternatively, install on your computer (to work offline):

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

```{r, eval=FALSE}

healthyr_notebooks = c("tidyverse", "boot", "finalfit", "flexdashboard", "gapminder", "here", "kableExtra", "knitr", "remotes", "rmarkdown", "shiny", "survminer", "tinytex")
install.packages(healthyr_notebooks)

```

### 3.2 Then Restart R

## 3.3 to then run these two lines (same as before, copy-paste to the Console):

```{r, eval = FALSE}

remotes::install_github("thomasp85/patchwork")
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
