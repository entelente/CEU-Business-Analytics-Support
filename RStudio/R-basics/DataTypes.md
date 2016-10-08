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
