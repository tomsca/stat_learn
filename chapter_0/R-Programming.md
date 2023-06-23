# Unit 0: R Programming
## Introduction to R

R is a language and environment for statistical computing and graphics. It is widely used among statisticians and data miners for data analysis. R is ideal for machine and statistical learning operations such as regression and classification. 

As of June 2023, R ranks 11th in the TIOBE index, a measure of programming language popularity, in which the language peaked in 8th place in August 2020. In this R tutorial, we will start by learning what exactly is R. 

R is an open-source programming language,  it can be downloaded and installed for free. It is cross-platform compatible language, one can run the same R code in multiple operating systems. With the help of R language, one is able to implement various machine learning algorithms such as Linear Regression, Decision Tree, etc. This is the link to R [Click me!](https://cran.r-project.org/)

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
> quantity = 5
> unit_price = 20
> total_cost = 5 * 20
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
quantity = 5
unit_price = 20
total_cost = 5 * 20
print(total_cost)
```
```r
print("Is this the final result?")
```

### Variables in R

- A variable is a name given to a memory location, which is used to store values in a computer program.
- Variables in R programming can be used to store numbers (real and complex), words, matrices, and even tables.
- For a variable to be valid, it should follow these rules
    - It should contain letters, numbers, and only dot or underscore characters.
    - It should not start with a number (eg:- 7mauch)
    - It should not start with a dot followed by a number (eg:- .7mauch)
    - It should not start with an underscore (eg:- _mauch)
    - It should not be a reserved word (see this [link](https://www.datamentor.io/r-programming/reserved-words#:~:text=Reserved%20words%20in%20R%20programming,%2C%20function%20name%20etc.))for detail!

- **Constants in R:** The characteristic whose values are fixed are called constants. In R, there are two types of constants:
    - Numeric Constants: All numeric values such as integer, double, or complex fall under this category. Numeric constants followed by ‘L’ and ‘i’ are considered as integer and complex respectively. And, numeric constants preceded by 0x/0X are treated as hexadecimal numbers.
    - Character Constants: These constants are represented by single (‘) or double (“) quotes called delimiters.

### Data Types in R 
- Numeric:
```r
# In R, if we assign any decimal value to a variable it becomes a variable of a numeric data type.
# For example, the statement below assigns a numeric data type to the variable “x”.
x = 20.7
# The following statement is used to print the data type of the variable “x”:
class(x)
[1] "numeric"
```
- Integer
```r
e = as.integer(3)
class(e)
Output: [1] "integer"
```

```r
# Another way of creating an integer variable is by using the L keyword as follows:
x = 5L
class(x)
Output: [1] "integer"
```
- Complex
```r
# The values containing the imaginary number ‘i’ (iota) are called complex values.
# The following code gives an error when run:
sqrt(-1)
[1] NaN
Warning message:
In sqrt(-1) : NaNs produced
```
```r
# To overcome this error, we coerce the value (−1) into a complex value and denote it as ‘i’.
sqrt(as.complex(-1))
[1] 0+1i
```
- Character
```r
# This data type is used to represent strings.
# For example:
str1 = "Sam"
class(str1)
Output: [1] "character"
```

```r
# We can also use the as.character() function to convert objects into character values.
# For example:
x <- as.character(100.5)
print(x)
Output:[1] "100.5"
class(x)
Output:[1] "character"
```
- Logical
```r
# A logical data type stores either of the two values: TRUE -/FALSE. A logical value is often generated when two values are compared.
# For example:
x = 5
y = 7
z = x > y
z
Output:
FALSE
```

```r
# Three standard logical operations,i.e., AND (&), OR (|), and NOT (!) yield a variable of the logical data type.
# For example:
x = TRUE; y = FALSE
x & y
Output:
[1] FALSE
x | y
Output:
[1] TRUE
!x
Output:
[1] FALSE
```

## Operators in R
### R Operators
- Arithmetic Operators
    - Basic arithmetic operations include `addition`, `subtraction`, `multiplication`, `division`, `exponent`, `modulus`, etc.
```r
x = 5; y = 2.5

# Addition
print(x + y)
[1] 7.5

# Subtraction
print(x - y)
[1] 2.5

# Multiply
print(x * y)
[1] 12.5

# Divide
print(x / y)
[1] 2

# Exponent
print(x^y)
[1] 55.9017

# Modulus
print(x %% y)
[1] 0
```
**Note:** The arithmetic operators can also be used to perform mathematical operations on vectors. For creating vectors, we use the `c()` function}.

```r
# Vectors
x = c( 3.0, 2.5, 6, 9.2)
y = c(12.3, 3.3, 4.10, 5.9)

# Addition
print(x + y)
[1] 15.3  5.8 10.1 15.1

# Subtraction
print(x - y)
[1] -9.3 -0.8  1.9  3.3

# Multiplication
print(x * y)
[1] 36.90  8.25 24.60 54.28

# Division
 print(x / y)
[1] 0.2439024 0.7575758 1.4634146 1.5593220

# Exponent
print(x ^ y)
[1] 738909.81106     20.56847   1550.31563 485677.72028

# Modulus
print(x %% y)
[1] 3.0 2.5 1.9 3.3
```
- Assignment Operator
    - The assignment operator is used to assign values to variables in R. There are two types of assignments: leftwards and rightwards.
    - Operators `<-` and  `=` are used to assign values to any variable.
```r
# Leftwards Assignment
x <- 25.5
x = 25.5

# Rightwards Assignment
25.5 -> x
x = 25.5
```
- Logical Operators
- Relational Operators
- Miscellaneous Operators

See this [link](https://www.tutorialspoint.com/r/r_operators.htm) for more...

## Resources
- Learn R in 39 Minutes [Click me!](https://www.youtube.com/watch?v=yZ0bV2Afkjc)


