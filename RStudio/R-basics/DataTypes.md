Most important data types and corresponding operations in R
===========================================================

Basic types
-----------

``` r
# By default the type of number is double. It is called numeric sometimes.
typeof(12)
```

    ## [1] "double"

``` r
# For complex number the imaginary part is denoted by "i"
typeof(12+3i)
```

    ## [1] "complex"

``` r
# A single character or any text : character
typeof("Some text")
```

    ## [1] "character"

``` r
# Logical variables can only two values: TRUE, FALSE or T, F as a short form
typeof(TRUE)
```

    ## [1] "logical"

``` r
# Integers are mainly used as indexes
typeof(as.integer(12))
```

    ## [1] "integer"

Basic operations
----------------

### Numbers

``` r
# For numeric and integer all the mathematical operatons can be used
(1+2-3*4)/2
```

    ## [1] -4.5

``` r
# Exp
5^2
```

    ## [1] 25

``` r
# Square and n-th root
sqrt(25)
```

    ## [1] 5

``` r
125^(1/3)
```

    ## [1] 5

### Logical variables

``` r
# AND : TRUE only if both of the values are TRUE
TRUE & TRUE
```

    ## [1] TRUE

``` r
FALSE & TRUE
```

    ## [1] FALSE

``` r
FALSE & FALSE
```

    ## [1] FALSE

``` r
# OR : TRUE if at least one of the values are TRUE
TRUE | TRUE
```

    ## [1] TRUE

``` r
FALSE | TRUE
```

    ## [1] TRUE

``` r
FALSE | FALSE
```

    ## [1] FALSE

### Text (Character)

``` r
# concatanation of text (or numbers), the default separator is a space
paste("I have", 3, "apples.")
```

    ## [1] "I have 3 apples."

``` r
# Using empty separator
paste("I have", 3, "apples.", sep = "")
```

    ## [1] "I have3apples."

``` r
# Using custom separator
paste("I have", 3, "apples.", sep = " giggity ")
```

    ## [1] "I have giggity 3 giggity apples."

``` r
# Replacing parts of text with something
sub("3", "5", "I have 3 apples and 3 bananas.")
```

    ## [1] "I have 5 apples and 3 bananas."

``` r
# Sub replaces only the first occurance. To have a "global" substitution use gsub
gsub("3", "5", "I have 3 apples and 3 bananas.")
```

    ## [1] "I have 5 apples and 5 bananas."

Vectors
-------

``` r
# Vectors can be created with c(...)
x <- c(1, 2, 3, 4, 5) # Numeric vector
y <- c("a", "b", "c", "d", "e") # Character vector
z <- c(T, F, F, T, F) # Logical vector
# : can be used to create a range of integers
2:18 # Vector of integers from 2 to 18
```

    ##  [1]  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18

``` r
2 * 1:9 # Vector of every second integer from 2 to 18
```

    ## [1]  2  4  6  8 10 12 14 16 18

``` r
# COncatenate vectors
x321 <- c(x, c(3, 2, 1) )
print(x321)
```

    ## [1] 1 2 3 4 5 3 2 1

Creating DataFrames
-------------------

``` r
# Dataframes can be created with either loading a CSV file or by combining vectors
d <- data.frame(x, y, z, stringsAsFactors = FALSE) # We don't want the default option to create factors yet.
# R used the variable names as colum names
print(d, row.names=FALSE) # row.names=FALSE won't list row names/indexed
```

    ##  x y     z
    ##  1 a  TRUE
    ##  2 b FALSE
    ##  3 c FALSE
    ##  4 d  TRUE
    ##  5 e FALSE

``` r
# Getting column names vector
colnames(d)
```

    ## [1] "x" "y" "z"

``` r
# Setting column names
colnames(d) <- c("First", "Second", "Third")
```

Subsetting DataFrames
---------------------

``` r
# TODO
```
