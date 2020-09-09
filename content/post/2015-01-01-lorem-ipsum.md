---
title: "How to Create a Website"
author: "Rohit Satyam"
date: "9/8/2020"
categories: ["R"]
output: html_document
tags: ["R Markdown", "Hugo", "blogdown"]
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

## R Markdown

This is a short step by step tutorial used to make IIT Delhi workflow website. We will use `blogdown` package for that and also download static site generator Hugo (https://gohugo.io) to use  ready-to-use themes. For more on installation and issues, read [here](https://bookdown.org/yihui/blogdown/installation.html).

```{r}
#installing required packages
install.packages('blogdown') 
blogdown::install_hugo()
library(blogdown)
```

## Creating Website
For the workflow management purpose, I chose a theme named `chipzoller/hugo-clarity` more about which can be found [here](https://themes.gohugo.io/hugo-clarity/). Some Basic Commands to know

-   **build_site()**  : Compiles all .Rmd files into Hugo-readable HTML & builds the site
-   **html_page()**  : Renders .Rmd file into Hugo-readable HTML
-   **hugo_cmd()**  : Allows you to run Hugo commands
-   **install_hugo()**  : Downloads the appropriate Hugo files to your computer to allow site generation
-   **install_theme()**  : Downloads the specified theme from GitHub
-   **new_content()**  : Generates a new file in your working directory
-   **new_site()**  : Creates the environment necessary for a new site
-   **serve_site()**  : Allows you to preview a working version of your site

First, create a new project directory in windows where you wish to keep your website files (say website folder). Now lets create basic architecture of the website

```{r }
new_site()

#It will create a .toml and few more directories
##Now install a theme. Here we will use chipzoller/hugo-clarit theme

install_theme("chipzoller/hugo-clarity", theme_example = TRUE, update_config = TRUE)

```

Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.

## Bugs
1.https://www.edureka.co/community/63787/rejected-master-master-fetch-first-error-failed-github-abc70


## **References**


