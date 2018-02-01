Getting Your Feet Wet in `R`
================


-   [Getting Acquainted](#getting-acquainted)
    -   [What is `R`?](#what-is-r)
    -   [What is `RStudio`?](#what-is-rstudio)
    -   [What can you do with `R` and `RStudio`?](#what-can-you-do-with-r-and-rstudio)
        -   ["Traditional" Statistics](#traditional-statistics)
        -   [GIS and Geospatial Analysis](#gis-and-geospatial-analysis)
        -   [Advanced Network Analysis](#advanced-network-analysis)
        -   [Text Mining and Natural Language Processing](#text-mining-and-natural-language-processing)
        -   [Dashboard Applications](#dashboard-applications)
-   [Setting up `R`](#setting-up-r)
    -   [Starting a Project](#starting-a-project)
    -   [`R Markdown`](#r-markdown)
        -   [Why `R Markdown`?](#why-r-markdown)
    -   [Creating a new `.Rmd` file](#creating-a-new-.rmd-file)
    -   [Adding a Code `chunk`](#adding-a-code-chunk)
-   [Programming in `R`](#programming-in-r)
    -   [Basic Arithmetic](#basic-arithmetic)
    -   [Variable Assignment](#variable-assignment)
    -   [Data Types](#data-types)
        -   [`character`](#character)
        -   [Combining Data](#combining-data)
            -   [`vector`s and `list`s](#vectors-and-lists)
            -   [`logical`](#logical)
            -   [Tabluar Data](#tabluar-data)
                -   [`matrix`](#matrix)
                -   [`data.frame`](#data.frame)
-   [Dealing with packages](#dealing-with-packages)
    -   [Reading Data Files](#reading-data-files)
-   [Packages](#packages)
    -   [Installing](#installing)
    -   [Loading](#loading)
-   [Functions](#functions)

![Alt text](https://github.com/MIIS-META-Lab/NetworkAnalysisMIIS/blob/master/newLogo.jpg)

Thanks for attending the META Lab's Introduction to `R` Geek Out!

We're going to try and cover as much ground as possible in our limited time, but not to the detriment of learning what the code is doing or what its potential applications are.

Do not feel overwhelmed or that you are expected to immediately grasp everything that we cover. Today is a VERY cursory overview of `R`

Today's intent is not to immediately transform you into a functional programmer. That is not a remotely realistic goal.

Instead, the goal is to provide you with a basic grasp of how R works and some resources and support to puruse further learning.

If you have questions on anything, now or in the future, please feel free to ask. Thanks again for coming!

Getting Acquainted
==================

What is `R`?
------------

![Alt text](https://media.licdn.com/mpr/mpr/AAEAAQAAAAAAAAh1AAAAJDM1ZGE4MjFiLWU4ZDYtNGE3NC1iNTY3LWE2YWVlZjhjOWUzNw.png)

-   `R` is a language and environment for statistical computing and graphics.
-   `R` is an integrated suite of software facilities for:
    -   data manipulation,
    -   calculation,
    -   and graphical display.
-   The term “environment” is intended to characterize it as a fully planned and coherent system
    -   as opposed to being an incremental accretion of very specific and inflexible tools.
        -   Inflexibility frequently characterizes other data analysis software.
-   One of `R`’s strengths is the ease with which well-designed publication-quality plots can be produced.
-   Many users think of `R` as simply a statistics system.
    -   It's more accurate to think of it as an environment within which statistical techniques are implemented.
-   `R` is available as Free Software under the terms of the Free Software Foundation’s GNU General Public License.

Takeaway: `R` is a powerful, free, extensible platform with which you can perform analysis that may not be possible in other platforms.

![Alt text](https://paulvanderlaken.files.wordpress.com/2017/08/i2-wp-combigdatasciencetraining-comwp-contentuploads201607importance-of-learning-r-30e49bf00fcc57f39db94df59c306537448f0110.jpg?w=601)

What is `RStudio`?
------------------

![Alt text](https://upload.wikimedia.org/wikipedia/en/f/f0/RStudio_logo.png)

-   `RStudio` is a free and open-source integrated development environment (`IDE`) for `R`.
    -   An `IDE` is a software application that provides comprehensive facilities to computer programmers for software development.
        -   Think of an `IDE` as a really fancy text editor that allows you to write, run, debug, share, and deploy code.
            -   `RStudio` is undoubtedly one of the perks of using `R` as likely all of your work can be completed within `RStudio`.

Takeaway: `RStudio` is a powerful, free `IDE` that offers the ability to perform practically every task of a data science project in one environment.

![Alt text](http://edild.github.io/qetxrbook/figures/rstudio.png)

What can you do with `R` and `RStudio`?
---------------------------------------

### "Traditional" Statistics

![Alt text](http://www.gekkoquant.com/wp-content/uploads/2012/05/rstudio-windows.png)

### GIS and Geospatial Analysis

![Alt text](http://spatialanalysis.co.uk/wp-content/uploads/2012/02/bike_ggplot.png)

### Advanced Network Analysis

![Alt text](http://wallpup.com/wp-content/uploads/2013/04/Facebook-World-Network-Wallpaper.jpg)

### Text Mining and Natural Language Processing

![Alt text](http://cfss.uchicago.edu/fall2016/text01_files/figure-html/unnamed-chunk-4-1.png)

### Dashboard Applications

-   [Bus Routes: Tracking locations over time using streaming data](https://shiny.rstudio.com/gallery/bus-dashboard.html)
    -   ![Alt text](https://shiny.rstudio.com/gallery/images/thumbnails/bus-dashboard.png)
-   [Diagnostics for Lake Erie fisheries](https://gallery.shinyapps.io/lake_erie_fisheries_stock_assessment_app/)
    -   ![Alt text](https://www.rstudio.com/wp-content/uploads/2015/05/lake-erie.png)
-   [San Francisco Crime Map, Live Simulation](https://snak.shinyapps.io/apptrois/) ![Alt text](https://www.showmeshiny.com/wp-content/uploads/2017/01/Crime-Map-768x383.png)

... and those are just the pretty pictures I found in a few minutes of 5am Google-Fu!

Setting up `R`
==============

Starting a Project
------------------

By using `RStudio`'s project manager, we can eliminate many of the common headaches associated with file management.

Keeping our work in a project: 

* automatically sets our `working directory` to the project's folder
* creates a `.Rproj` file that allows us to easily return to our project 
* facilitates simple sharing our code, data, and reports

![Alt text](https://image.slidesharecdn.com/20150422reproresr8-160404131652/95/reproducible-research-in-r-and-r-studio-20-638.jpg?cb=1459775831)

`R Markdown`
------------

### Why `R Markdown`?

We're going to use `R Markdown` for our code as it lets us:

-   Perform our analysis
-   Share our code, workflow, exploration, and findings
-   Reproduce our results
    -   Reproducibility is the ability of an entire analysis of an experiment or study to be duplicated, either by the same researcher or by someone else working independently.

When we're doing any sort of analysis, we want to keep in mind that our data tells a story. `R Markdown` lets us turn our analyses into professional quality documents, reports, presentations, and dashboards.

Creating a new `.Rmd` file
--------------------------

![Alt text](http://rmarkdown.rstudio.com/articles/images/new-file-screenshot.png)

![Alt text](http://jules32.github.io/2016-07-12-Oxford/workflow/img/rstudio_new-rmd-doc-html.png)

`RStudio` provides some sample code when you open a new `.Rmd` file, but you can go ahead ad delete everything below the `chunk` with the following code:

``` r
knitr::opts_chunk$set(echo = TRUE)
```

`R` code `chunk`s can be used as a means render `R` output into documents or to simply display code for illustration. Another perk is that it allows us to organize our code and thus our analytical workflow.

We're not going to dive into everything that you can do with `R Markdown`, but here's a [cheatsheet](https://www.rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf) that explains much of the syntax that you can use to customize your reports.

For now, just know that you can type explanatory notes between code `chunk`s.

As you can see, code chunks in RStudio are highlighed with a gray background. Everything you put in this chunk will be evaluated by R Markdown as R code when you `knit` the document.

Adding a Code `chunk`
---------------------

![Alt text](https://ourcodingclub.github.io/img/Code_Chunk_Screenshot.jpg)

You can insert a new code chunk in a few ways:

* Click the “insert new code chunk” button on the top right hand of this panel. It looks like a green square with an arrow.
        + Your version may look a bit different ![Alt text](https://ourcodingclub.github.io/img/Code_Chunk_Screenshot.jpg)
* Copy and paste an existing chunk and change its content and properties.

You may notice that there are setting you can customize for each `chunk`. Don't worry about that for now, but realize it's there for the future.

Programming in `R`
==================

Go ahead and insert a new `R` code `chunk`.

In order to run your code, you can: 

* click the green arrow on the right side of the code `chunk` 
* click `Run` at the top of your screen 
* use _Ctrl_ + _Enter_/_Return_ to run your current line 
* use _Ctrl_ + _Shift_ + _Enter_ to run your current chunk

Basic Arithmetic
----------------

You're going to see `#` in this code, which is used to comment within code. `R` sees `#` and knows not to try and run execute whatever follows it on the same line.

``` r
1 + 2   # addition
```

    ## [1] 3

``` r
2 - 1   # subtraction
```

    ## [1] 1

``` r
3 * 3   # multiplication
```

    ## [1] 9

``` r
9 / 3   # division
```

    ## [1] 3

``` r
3 ** 2  # exponents
```

    ## [1] 9

``` r
9 %% 2  # modulo, which returns the remainder of division
```

    ## [1] 1

Variable Assignment
-------------------

As opposed to many other programming languages, proper `R` syntax uses `<-` for variable assignment, rather than the more commonly seen use of `=` you may have seen in C-based languages like Python. 

While using `=` will variable accomplish the task of assignment without any side-effects in the vast majority of cases, you should stick to the `R` convention of `<-` as `=` there are different uses for each, your code will be more readable to other useRs, the habit will set you up to read the code of other useRs better, and you won't be forced to break the habit in collaborative projects that enforce proper syntax (read: 99% of them).

Think of using proper syntax as being analogous to writing a paper in the proper format. Ensuring that your code is readable should be a priority, even if you will never share it. You will likely encounter challenges that you overcame months earlier. You want to be able to return to your old code and actually understand the solution you used.

On that note, just what the heck is assignment anyways?

When programming, you will want to be able to assign data to variables that you can use in other parts of your code.

``` r
x <- 1

x
```

    ## [1] 1

``` r
y <- 1

z <- x + y

z
```

    ## [1] 2

Data Types
----------

We already saw `numerical` data above, but we can do a lot more than just numbers.

### `character`

For `character`s (commonly referred to as strings), we encapsulate our data with `""`

``` r
first_name <- "John"
last_name <- "Smith"
```

We can use numbers as strings too.

``` r
one <- "1"

one
```

    ## [1] "1"

In that case, what if we aren't sure what type of data is store in a variable?

``` r
mode(one)
```

    ## [1] "character"

### Combining Data

#### `vector`s and `list`s

``` r
a_vector <- c(1, 2, 3)

a_vector
```

    ## [1] 1 2 3

We'll use the `first_name` and `last_name` variables that we created above.

``` r
a_list <- c(first_name, last_name)

a_list
```

    ## [1] "John"  "Smith"

#### `logical`

To compare objects, we often want to evaluate whether an `object` is equal to another `object`.

-   `==` checks to see if 2 objects are equal to eachother.
-   `!=` checks to see if 2 objects are not equal to eachother.

``` r
1 == 2
```

    ## [1] FALSE

``` r
1 != 2
```

    ## [1] TRUE

We can also combine our `logical` evaluations. 

* `&` simply means `and`, which we can use to evaluate whether 2 (or more!) conditions are both `TRUE`. 
        + If either one is `FALSE`, then the whole expression is `FALSE`.

``` r
1 == 1 & 2 == 2
```

    ## [1] TRUE

``` r
1 == 2 & 2 == 2
```

    ## [1] FALSE

* `|` means `or`, which we can use to evaluate whether or not any conditions are `TRUE`.

``` r
1 == 1 | 2 == 3
```

    ## [1] TRUE

``` r
1 != 1
```

    ## [1] FALSE

#### Tabluar Data

##### `matrix`

First, let's create a few `vector`s of data...

``` r
a <- c(1, 2, 3)
b <- c(4, 5, 6)
c <- c(7, 8, 3)

a
```

    ## [1] 1 2 3

``` r
b
```

    ## [1] 4 5 6

``` r
c
```

    ## [1] 7 8 3

... and we want to combine our `vector`s into a `matrix` using `rbind()` 

* `rbind()` simply stands for `row bind`, and treats our `vector`s as rows in a `matrix`. For now, think of a `matrix` as a collection of `vector`s.

``` r
my_matrix <- rbind(a, b, c)
                       
my_matrix
```

    ##   [,1] [,2] [,3]
    ## a    1    2    3
    ## b    4    5    6
    ## c    7    8    3

If we look at the `mode` of `my_matrix` we see that it is `numeric` data...

``` r
mode(my_matrix)
```

    ## [1] "numeric"

But there are MANY types of `numeric` data in `R`, so we can get more specific by checking its `class`...

``` r
class(my_matrix)
```

    ## [1] "matrix"

![](http://i.imgur.com/7j15tXU.jpg)

Don't worry about what `class` is referring to now, but just realize there are ways to figure out which type of data you're dealing with.

Returning to the `matrix` we already created...

``` r
my_matrix
```

    ##   [,1] [,2] [,3]
    ## a    1    2    3
    ## b    4    5    6
    ## c    7    8    3

We can access the third row by using subscripts, i.e. `variable[row, ]`...

``` r
third_row <- my_matrix[3,]

third_row
```

    ## [1] 7 8 3

We can do the same to the third column with `variable[, column]`, which also gives us our `row` names...

``` r
third_column <- my_matrix[, 3]

third_column
```

    ## a b c 
    ## 3 6 3

Finally, we can access individual values from our matrix by using both `row` and `column` subscripting...

``` r
bottom_right <- my_matrix[3, 3]

bottom_right
```

    ## c 
    ## 3

Make sure you understand that the convention for subscripting then is `my_matrix[`row`,`column`]`

##### `data.frame`

A `data.frame` is very similar to a `matrix` in that they are both forms of tabular data containing `column`s and `row`s, but there are some differences in their use: \* `column`s in a `matrix` should contain data that are of the same type, while a `data.frame` contain mixed types of data \* all `column`s in a matrix should be of the same length, i.e. you don't have missing data \* the data in a `matrix` is accessible by calling it by its `[row, ]` and `[ , column]`, which we can't do with a `data.frame` \* `data.frame`s are more general in that different columns can have different types of data + this is what you'll typically see when dealing with data "in the wild"

We're going to stick with `data.frame`s (and its variations) from here on... but let's cover some other stuff first

Dealing with packages
=====================

Reading Data Files
------------------

We're going to read in some data contained in a `.csv` file

In your `Files` pane (probably bottom, right corner in `RStudio`), click `raw_data.csv` and then click `Import Dataset`.

You'll get a window that looks something like this... ![](https://support.rstudio.com/hc/en-us/article_attachments/206277598/Screen_Shot_2016-04-08_at_2.47.27_PM.png)

`RStudio` assigned the file's data to a variable with the same name as the file by executing the following...

``` r
library(readr)
raw_data <- read_csv("~/IntroToR/data/raw_data.csv")
```

What happens here is that `R` loads the `readr` package using the function `library()`. What's important is that there are thousands of packages available for `R` that extend its capabilities beyond the "basics" and *often* make it vastly easier to use.

Then, we can take a peak at our data...

``` r
raw_data
```

    ## # A tibble: 6 x 5
    ##          City `Pollution index` `Cost of living` Language `Misc Amenities`
    ##         <chr>             <int>            <int>    <int>            <int>
    ## 1    Shanghai                80               30        9               44
    ## 2   Mexico DF                73               17       22               29
    ## 3 Panama City                16               20       22               32
    ## 4       Hanoi                28               14       18               25
    ## 5   Singapore                44               70       70               71
    ## 6  Chittagong                46               11       27               14

Since `R` used code that's unfamiliar, we should also check what type of data that `raw_data` is...

``` r
class(raw_data)
```

    ## [1] "tbl_df"     "tbl"        "data.frame"

A tad different than what we've seen, but this is just a special form of a `data.frame` which we can manipulate with a suite of tools collectively known as the `tidyverse`... let's do that!

Packages
========

Installing
----------

First, we need to install it, which is the same as installing most packages in `R`...

``` r
install.packages("tidyverse")
```

Loading
-------

To use the `tidyverse` package, we use the `library()` function...

``` r
library(tidyverse)
```

    ## Loading tidyverse: ggplot2
    ## Loading tidyverse: tibble
    ## Loading tidyverse: tidyr
    ## Loading tidyverse: purrr
    ## Loading tidyverse: dplyr

    ## Conflicts with tidy packages ----------------------------------------------

    ## filter(): dplyr, stats
    ## lag():    dplyr, stats

Tidy data let us easily manipulate data. If you've ever used `SQL` with databases, it's very similar.

We can select data by column names with `select`...

``` r
select(raw_data, City)
```

    ## # A tibble: 6 x 1
    ##          City
    ##         <chr>
    ## 1    Shanghai
    ## 2   Mexico DF
    ## 3 Panama City
    ## 4       Hanoi
    ## 5   Singapore
    ## 6  Chittagong

Omit data in a similar way...

``` r
select(raw_data, -City)
```

    ## # A tibble: 6 x 4
    ##   `Pollution index` `Cost of living` Language `Misc Amenities`
    ##               <int>            <int>    <int>            <int>
    ## 1                80               30        9               44
    ## 2                73               17       22               29
    ## 3                16               20       22               32
    ## 4                28               14       18               25
    ## 5                44               70       70               71
    ## 6                46               11       27               14

Manipulate our data with `%>%`, called `pipe`s

``` r
raw_data %>%
  select(City, Language)
```

    ## # A tibble: 6 x 2
    ##          City Language
    ##         <chr>    <int>
    ## 1    Shanghai        9
    ## 2   Mexico DF       22
    ## 3 Panama City       22
    ## 4       Hanoi       18
    ## 5   Singapore       70
    ## 6  Chittagong       27
