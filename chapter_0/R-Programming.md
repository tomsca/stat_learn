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
### Arithmetic Operators
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
### Assignment Operator
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
### Logical Operators
- These operators are used to perform Boolean operations like `AND`, `OR`, `NOT`, etc. on variables.
- Different logical operators are as follows: `! (NOT)`, `& (AND element-wise)`, `&& (AND)`, `| (OR Element-wise)`, `|| (OR)`.
- ZEROS are taken as `FALSE` and NON-ZERO numbers are taken as `TRUE`.
```r
x <- c(2.5, 7, FALSE, 3 + 5i)
y <- c(5.3 , 1, TRUE, 3 + 5i)

# Element-wise Logical AND Operator
 print(x & y)
[1]  TRUE  TRUE FALSE  TRUE

# Element-wise Logical OR Operator
print(x | y)
[1] TRUE TRUE TRUE TRUE

# Logical NOT Operator
print(!x)
[1] FALSE FALSE  TRUE FALSE

# Logical AND Operator
a <- c(TRUE, TRUE, FALSE, FALSE)
b <- c(TRUE, FALSE, TRUE, FALSE)
print(a && b)

# Logical OR Operator
a <- c(TRUE, TRUE, FALSE, FALSE)
b <- c(TRUE, FALSE, TRUE, FALSE)
print(a || b)
```
### Relational Operators
- Relational operators are employed to compare two values or variables.
- To find if one is `smaller`, `greater`, `equal`, `not equal`, and other similar operations these operators are used.
- The result of a relational operator is always a logical value, that is either TRUE or FALSE.
<p align="center">
  <img width="460" height="300" src="https://i0.wp.com/makemeanalyst.com/wp-content/uploads/2017/05/Relational-Operators-in-R.png?resize=508%2C305">
</p>
 
 ### Miscellaneous Operators
- These kind of operators are used for special cases and are not for general mathematical or logical computation.
- For instance the `colon` operator is used to generate a series of numbers in sequence for a vector. The `%in%`operator is used to check if an element belongs to a vector or not.
```r
# colon Operator
a <- 0:5
print(a)
[1] 0 1 2 3 4 5

# %in% Operator
a <- 2
b <- 0:5
 print(a %in% b)
[1] TRUE
```
**Note:** This operator `%*%`, multiply's a matrix with its transpose.
```r
A <- matrix(1:9, nrow = 3,ncol = 3,byrow = TRUE)
Z <- A %*% t(A)
print(Z)
     [,1] [,2] [,3]
[1,]   14   32   50
[2,]   32   77  122
[3,]   50  122  194
```

## Data Structures in R 
- A data structure is a format for organizing and storing data in a system to facilitate effective and efficient usage of the same.
- They are known to make data accessing and operations easier.
- Statistical software and programming languages have methods (or functions) designed to operate on different kinds of data structures.
- Data Structures in R include: `Vectors`, `Lists`, `Matrices`, `Factors`, `Data Frames`, and `Arrays`.

### Vectors
- Vector is one of the basic data structures in R. It only contains elements of the same data type. Data types can be numeric, integer, character, complex, or logical.
- Vectors are created by using the `c()` function. 
- The `typeof()` function is used to check the data type of the vector.
- The `class()` function is used to check the class of the vector.

```r
# Vectors
vec_1 <- c(23, 18, 93, 45, 8)
vec_2 <- c(15, TRUE, 22.6, "female")
typeof(vec_1)
[1] "double"
typeof(vec_2)
[1] "character"
```
- To delete a vector, you simply have to do the following:
```r
vec_1 <- NULL
vec_2 <- NULL
```

Vec1 <- NULL
Vec2 <- NULL

### Lists

### Matrices

### Factors

### Data Frames

### Arrays

  

## References
1. R Tutorials [Clcike me!](https://intellipaat.com/blog/tutorial/r-programming/data-structures-r-programming/?US)
2. Learn R in 39 Minutes [Click me!](https://www.youtube.com/watch?v=yZ0bV2Afkjc)


