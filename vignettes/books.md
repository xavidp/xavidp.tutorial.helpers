---
title: "Tutorials for Books"
author: David Kane
output: rmarkdown::html_vignette
vignette: >
  %\VignetteEngine{knitr::knitr}
  %\VignetteIndexEntry{Tutorials for Books}
  %\VignetteEncoding{UTF-8}
---


This vignette assumes that you have already read [our advice](instructions.html) about writing good tutorials.

A common use case for this package is to write a collection of tutorials for a book. Consider the [**r4ds.tutorials**](https://ppbds.github.io/r4ds.tutorials/) package which is a companion to [*R for Data Science (2e)*](https://r4ds.hadley.nz/) by Hadley Wickham, Mine Çetinkaya-Rundel, and Garrett Grolemund.

Instructors like to assign books with code. Ideally, we want our students to read the book, working through the included code, line-by-line. Sadly, very few students are so disciplined. In fact, in a large class, a majority of the students won't even read the book.

The **tutorial.helpers** package make it easy to create a *structured* tutorial in which students type in (almost) every command which the book demonstrates, along with other commands which, in your judgment, are helpful. 

Consider some idiosyncratic advice for book-based tutorials using the example of [*R for Data Science (2e)*](https://r4ds.hadley.nz/) and [**r4ds.tutorials**](https://ppbds.github.io/r4ds.tutorials/).

* Do one or two of the tutorials before you start working on your own. One of them should be the 4-data-transform tutorial. Another might be the 21-spreadsheets tutorial. The below examples are taken from it.

* Make your Introduction look like this:

````
This tutorial covers [Chapter 21: Spreadsheets](https://r4ds.hadley.nz/spreadsheets.html) from [*R for Data Science (2e)*](https://r4ds.hadley.nz/) by Hadley Wickham, Mine Çetinkaya-Rundel, and Garrett Grolemund. You will learn how to get data from Excel spreadsheets using  `[read_excel()](https://readxl.tidyverse.org/reference/read_excel.html)` from the [**readxl**](https://readxl.tidyverse.org/) package and Google sheets using `[read_sheet()](https://googlesheets4.tidyverse.org/reference/range_read.html)` from the [**googlesheets4**](https://googlesheets4.tidyverse.org/) package.
````

  - The first sentence provides a link to your chapter as well as to R4DS.
  - We highlight some the most important packages and functions used in the tutorial.
  - We don't go overboard. You can't mention every package or every function used in the tutorial.


* Make your Summary look like this:

````
This tutorial covered [Chapter 21: Spreadsheets](https://r4ds.hadley.nz/spreadsheets.html) from [*R for Data Science (2e)*](https://r4ds.hadley.nz/) by Hadley Wickham, Mine Çetinkaya-Rundel, and Garrett Grolemund. You have learned how to get data from Excel spreadsheets using  `[read_excel()](https://readxl.tidyverse.org/reference/read_excel.html)` from the [**readxl**](https://readxl.tidyverse.org/) package and Google sheets using `[read_sheet()](https://googlesheets4.tidyverse.org/reference/range_read.html)` from the [**googlesheets4**](https://googlesheets4.tidyverse.org/) package.

Read “[Data Organization in Spreadsheets](https://doi.org/10.1080/00031305.2017.1375989)” by Karl Broman and Kara Woo for great advice about organizing your data using spreadsheets.
````

  - The first paragraph is identical to the Introduction, expected that "covers" is replaced with "covered" and "will learn" with "have learned." We began the tutorial with a promise about what students would learn. One hopes that we kept that promise.
  - The second paragraph gives one or two pointers about the best material which a student might look into if she is interested in learning more about the broad topic of the tutorial. These pointers were also mentioned as knowledge drops earlier in the tutorial.
  - These pointers will often (always?) be items which were mentioned in the book itself. Those authors, presumably, have good taste, otherwise you would not have selected the book in the first place.

* Always have a separate Exercise for each library you load and each data set you use. An Exercise like "Load the **tidyverse** package with the `library()` command." is, obviously, not difficult for students. But it forces them to practice loading libraries, which many students forget, and it provides us with an opportunity to drop some knowledge.

* Regularly require them to look up the help page for a function, proving that they have done so by copy/pasting a portion of the help page, which means that these will be Exercises with No Answer instead of Code Exercises. Students need to get in the practice of using help.

* You want students to have to type in every line of code which is mentioned in the book. One approach is to first, set up a bunch of empty Code Exercises. Then, go through the chapter, copying each snippet of example code into the Hint of an Exercise. (If the book is sourced freely, you can also copy/paste a knowledge drop associated with each code snippet.) Then, go back and write the Exercises such that the answers are the code snippets from the book. The final step is to edit out at least a portion of the Hint.

* In most books, the authors will include more than one new thing in each code example. They will add two or three lines to a pipe or pass in two or three arguments to a function. We never want to go that fast. Spread out such code snippets into two or three separate Exercises, each of which makes the smallest possible change. Recall that we are building the shallowest possible learning curve. 

* Recall the distinction between books which have a permissive license, meaning that we can copy/paste text at our own discretion, and those which do not. For the latter, you can not copy/paste text. But you can express, in your own words, the key points made in each chapter. In either case, your knowledge drops should cover the most important things for students to know.





