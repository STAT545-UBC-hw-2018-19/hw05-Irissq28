hw001\_Data frame exploration
================
Irissq28
16th September, 2018

Data frame exploration
----------------------

### Setting up

First, check the existing packages in your computer. `data(package = .packages(all.available = TRUE))`

If you don't have the package you need, visit [Contributed Packages](https://cran.r-project.org), run `install.packages(yourpackage_name)` in the console before next move.

### Choose package and data set

Data set 'animals' in package ‘cluster’

``` r
library(cluster)
```

``` r
print(animals)
```

    ##     war fly ver end gro hai
    ## ant   1   1   1   1   2   1
    ## bee   1   2   1   1   2   2
    ## cat   2   1   2   1   1   2
    ## cpl   1   1   1   1   1   2
    ## chi   2   1   2   2   2   2
    ## cow   2   1   2   1   2   2
    ## duc   2   2   2   1   2   1
    ## eag   2   2   2   2   1   1
    ## ele   2   1   2   2   2   1
    ## fly   1   2   1   1   1   1
    ## fro   1   1   2   2  NA   1
    ## her   1   1   2   1   2   1
    ## lio   2   1   2  NA   2   2
    ## liz   1   1   2   1   1   1
    ## lob   1   1   1   1  NA   1
    ## man   2   1   2   2   2   2
    ## rab   2   1   2   1   2   2
    ## sal   1   1   2   1  NA   1
    ## spi   1   1   1  NA   1   2
    ## wha   2   1   2   2   2   1

### Exploration of data frames

Explore `animals` with functions like `name`, `head`, `tail`, `str`, `summary`.

``` r
#list the variables in animals
names(animals)
```

    ## [1] "war" "fly" "ver" "end" "gro" "hai"

``` r
#print first 5 rows in animals
head(animals,n=5L)
```

    ##     war fly ver end gro hai
    ## ant   1   1   1   1   2   1
    ## bee   1   2   1   1   2   2
    ## cat   2   1   2   1   1   2
    ## cpl   1   1   1   1   1   2
    ## chi   2   1   2   2   2   2

``` r
#print last 2 rows in animals
tail(animals,n=2L)
```

    ##     war fly ver end gro hai
    ## spi   1   1   1  NA   1   2
    ## wha   2   1   2   2   2   1

``` r
#list the structure of animals
str(animals)
```

    ## 'data.frame':    20 obs. of  6 variables:
    ##  $ war: int  1 1 2 1 2 2 2 2 2 1 ...
    ##  $ fly: int  1 2 1 1 1 1 2 2 1 2 ...
    ##  $ ver: int  1 1 2 1 2 2 2 2 2 1 ...
    ##  $ end: int  1 1 1 1 2 1 1 2 2 1 ...
    ##  $ gro: int  2 2 1 1 2 2 2 1 2 1 ...
    ##  $ hai: int  1 2 2 2 2 2 1 1 1 1 ...

``` r
#result summaries
summary(animals)
```

    ##       war           fly           ver           end             gro       
    ##  Min.   :1.0   Min.   :1.0   Min.   :1.0   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.0   1st Qu.:1.0   1st Qu.:1.0   1st Qu.:1.000   1st Qu.:1.000  
    ##  Median :1.5   Median :1.0   Median :2.0   Median :1.000   Median :2.000  
    ##  Mean   :1.5   Mean   :1.2   Mean   :1.7   Mean   :1.333   Mean   :1.647  
    ##  3rd Qu.:2.0   3rd Qu.:1.0   3rd Qu.:2.0   3rd Qu.:2.000   3rd Qu.:2.000  
    ##  Max.   :2.0   Max.   :2.0   Max.   :2.0   Max.   :2.000   Max.   :2.000  
    ##                                            NA's   :2       NA's   :3      
    ##       hai      
    ##  Min.   :1.00  
    ##  1st Qu.:1.00  
    ##  Median :1.00  
    ##  Mean   :1.45  
    ##  3rd Qu.:2.00  
    ##  Max.   :2.00  
    ##
