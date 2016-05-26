---
title       : Data in R
description : This section will be cover how to get started in R. 
attachments :


--- type:VideoExercise lang:r xp:25 skills:1   key:1ee3f6290a
## Getting Start in R

*** =video_link

//player.vimeo.com/video/168224745





--- type:NormalExercise lang:r xp:100 skills:1 key:e412be26b2
##Practicing Basic R

*** =instructions
You can run R code with this. Place the solution under the commented section and hit run.

*** =hint

Here is a hint: use `<-` for assignment

*** =sample_code

```{r}
# Create a variable a, equal to 5


# Square a

```

*** =solution

```{r}
# Create a variable a, equal to 5
a <- 5

# Square a
a^2
```

*** =sct
```{r}
test_object("a")
test_output_contains("25", incorrect_msg = "Make sure to print `a`")
success_msg("Great!")
```


--- type:VideoExercise lang:r xp:25 skills:1   key:7fb790f570
## Simple Procedures in R

*** =video_link

//player.vimeo.com/video/168226884



--- type:NormalExercise lang:r xp:100 skills:1 key:5a54b078aa

## Basic Procedures in R

*** =pre_exercise_code
```{r}
b <- NA
```

*** =sample_code

```{r}
# Create a variable b, equal to 4



# What is the log of b?


# what is the exponential of the log of b?

```

*** =solution

```{r}
# Create a variable b, equal to 4
b = 4


# What is the log of b?
 log(b)

# what is the exponential of the log of b?

exp(log(b))
```
*** =sct

```{r}
test_object("b")
test_function("log", args = "x") 
test_function("exp", args="x")
test_output_contains("1.386", incorrect_msg = "Did you take the logarithm of b?")
test_output_contains("4", incorrect_msg = "Did you take theexponential of the logarithm of b?")
test_error()
success_msg("Great job!")


```

--- type:VideoExercise lang:r xp:25 skills:1    key:d1e309b772
## Getting Help in R

*** =video_link

//player.vimeo.com/video/168234652



--- type:VideoExercise lang:r xp:25 skills:1    key:c1c4a17c89
## R for Simple Procedures

*** =video_link



//player.vimeo.com/video/168226884
