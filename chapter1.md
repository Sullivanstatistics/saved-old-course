---
title       : Data in R
description : In this Section we will begin to explore R and learn how it handles data. We will focus on major data types that we use frequently in statistics and the basics of how we use them. As we move forward these data types will be key to analyzing statistics.  
attachments :


--- type:VideoExercise lang:r xp:25 skills:1   key:1ee3f6290a
## Getting Start in R

*** =video_link

//player.vimeo.com/video/168224745





--- type:NormalExercise lang:r xp:25 skills:1 key:e412be26b2
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



--- type:NormalExercise lang:r xp:25 skills:1 key:5a54b078aa

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
## Data Objects in R

*** =video_link



//player.vimeo.com/video/168247352






--- type:MultipleChoiceExercise lang:r xp:25 skills:1  key:be0cd6ce2a

## Practicing with Data Objects in R


Consider the functions Below. What are the boolean values for them. 

```
#The First

0 == 4/3*3 - 1

The Second

all.equal(0, 4/3*3 - 1)
```


*** =instructions
- Both False
- Both True
- First False and Second True
- First True and Second True

*** =pre_exercise_code

```{r}
# no pec
```

*** =hint
If you cannot figure this out try and run them. 

*** =sct
```{r}
msg1 = "That is not correct!"
msg2 = "Exactly! "
msg3 = "Ask yourself if we perform an operation on anything of the numbers"
test_mc(correct=3, feedback_msg=c(msg1, msg3, msg2, msg3))
```





--- type:VideoExercise lang:r xp:25 skills:1     key:78f70d2224
## Vectors in R

*** =video_link


*** =instructions




//player.vimeo.com/video/168261729

--- type:VideoExercise lang:r xp:25 skills:1      key:fb0dfd78e7
## Arrays in R

*** =video_link



//player.vimeo.com/video/168265628


--- type:VideoExercise lang:r xp:25 skills:1      key:bb2242f8de
## Matrices in R

*** =video_link



//player.vimeo.com/video/168271916


--- type:VideoExercise lang:r xp:25 skills:1      key:7317839f79
## Lists in R

*** =video_link



//player.vimeo.com/video/168275483

--- type:VideoExercise lang:r xp:25 skills:1      key:55e8de92d3
## Dataframes in R

*** =video_link



//player.vimeo.com/video/


