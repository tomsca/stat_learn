# Unit 0: R Programming
## Introduction to R

R is a language and environment for statistical computing and graphics. It is widely used among statisticians and data miners for data analysis. R is ideal for machine and statistical learning operations such as regression and classification. 

As of June 2023, R ranks 11th in the TIOBE index, a measure of programming language popularity, in which the language peaked in 8th place in August 2020. In this R tutorial, we will start by learning what exactly is R. 

R is an open-source programming language,  it can be downloaded and installed for free. It is cross-platform compatible language, one can run the same R code in multiple operating systems. With the help of R language, one is able to implement various machine learning algorithms such as Linear Regression, Decision Tree, etc. This is the link to R [Click me!](https://cran.r-project.org/).

## History of R
R is a programming language developed by *Ross Ihaka* and *Robert Gentleman* at the University of Auckland, New Zealand. In April 2003, the R Foundation was founded as a non-profit organization to provide further support for the R project. In 1995, R was made a free and open-source software under the GNU General Public Licence. The first official release came in 1995 followed by the first 'stable beta' version (v1.0) released on 29th February 2000.

## R Studio
R Studio is a free integrated developed environment (IDE) designed for R. It comes in two versions, i.e., R Studio Desktop and R Studio Server. It inclues a console, syntax-highlighting editor, and tools for plotting, history, debugging and workspace management. This is the link to RStudio [Click me!](https://posit.co/).

## Download and Install R and RStudio

- For Windows, follow the instructions on this video [Click me!](https://www.youtube.com/watch?v=YrEe2TLr3MI)
- For Mac, follow the instructions on this video [Click me!](https://www.youtube.com/watch?v=n8kP7c_QbLA)

## Variables and Data Types in R
### Basic Syntax in R
- There are two ways to write code in RStudio:
    1) in the command prompt
    2) in the R script file. We will go through both one by one.
 1.a) Command Prompt
    - Launch RStudio
    - In the command prompt window, type the following:
        - quantity = 5
        - unit_price = 20
        - total_cost = quantity * price
        - print(total_cost)

```r
> quantity <- 5
> unit_price <- 20
> total_cost <- 5 * 20
> print(total_cost)
[1] 100
```

1.b) Command Prompt
   - Launch RStudio
   - In the command prompt window, type the following:
     - print("Is this the final result?")
```r
> print("Is this the final result?")
[1] "Is this the final result?"
```

 2) R Script File
   - R Programs are usually written in R scripts and then executed in the console window
   - Create a new R script file
   - Write the code shown in 1.a and 1.b, select the block of code you want to run, and then press Ctrl+Enter or click on ‘Run’:

```r
quantity <- 5
unit_price <- 20
total_cost <- 5 * 20
print(total_cost)
```
```r
print("Is this the final result?")
```
     

## Resources
- Learn R in 39 Minutes [Click me!](https://www.youtube.com/watch?v=yZ0bV2Afkjc)


