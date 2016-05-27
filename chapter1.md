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




--- type:NormalExercise lang:r  xp:75 skills:1 key:770d89a78d
## Vectors in R Exercise 1

This exercise will allow you to look further into vectors. 

*** =instructions
Use R to answer the following questions. 

1. What is the length of x?
2. How many values in your vector x are below 2?
3. How many values in your vector x are above 7?
4. How many values in your vector x are below 3 or above 8?


*** =hint
Use your knowledge of indexing and functions that return Booleans.

*** =pre_exercise_code
```{r}
#You will find out more about the runif command in a few weeks.
set.seed(1234)
x = runif(5000, 1, 8)
```

*** =sample_code
```{r}
# Do Not Print X as it is a long vector
# 1. What is the length of x?

# 2. How many values in your vector x are below 2?


# 3. How many values in your vector x are above 7?


# 4. How many values in your vector x are below 3 or above 8?


```

*** =solution
```{r}
# Do Not Print X as it is a long vector
# 1. What is the length of x?
length(x)

# 2. How many values in your vector x are below 2?
length(which(x<2))

# 3. How many values in your vector x are above 7?
length(which(x>7))

# 4. How many values in your vector x are below 3 or above 8?
length(which(x<3 | x>8))

```

*** =sct
```{r}
test_error()
test_output_contains("5000")
test_function("which", args="x")
test_output_contains("696")
test_function("which", args="x")
test_output_contains("729")
test_function("which", args="x")
test_output_contains("1411")
success_msg("Great Job")
```


--- type:NormalExercise lang:r  xp:75 skills:1  key:0cd0b2c4e3
## Vectors in R Exercise 2

This exercise will allow you to look further into vectors. 

*** =instructions
Use R to answer the following questions. Given `x` from before:

1. How many times does the value 2 occur?
2. What are the 3400th - 3402th elements in your vector?
3. What is the smallest value in x?
4. What is the largest value in x?



*** =hint
Use your knowledge of indexing and functions that return Booleans.

*** =pre_exercise_code
```{r}
#You will find out more about the runif command in a few weeks.
set.seed(1234)
x = runif(5000, 1, 8)
```

*** =sample_code
```{r}
# Do Not Print X as it is a long vector
# 1. How many times does the value 2 occur?



# 2. What are the 3400th - 3402th elements in your vector?


# 3. What is the smallest value in x?


# 4. What is the largest value in x?


```

*** =solution
```{r}
# Do Not Print X as it is a long vector
# 1. How many times does the value 2 occur?
length(which(x==2))


# 2. What are the 3400th - 3402th elements in your vector?
x[3400:3402]

# 3. What is the smallest value in x?
min(x)

# 4. What is the largest value in x?
max(x)

```

*** =sct
```{r}
test_error()
test_function("length", args="x")
test_function("which", args="x")
test_output_contains("0")
test_output_contains("696")
test_output_contains("3400")
test_output_contains("3402")
test_output_contains("7.47")
test_output_contains("3.28")
test_output_contains("2.07")
test_function("min", args="x")
test_output_contains("1.0")
test_function("max", args="x")
test_output_contains("7.99")
success_msg("Great Job")
```


//player.vimeo.com/video/168261729

--- type:VideoExercise lang:r xp:25 skills:1      key:fb0dfd78e7
## Arrays in R

*** =video_link



//player.vimeo.com/video/168265628


--- type:VideoExercise lang:r xp:25 skills:1      key:bb2242f8de
## Matrices in R

*** =video_link

//player.vimeo.com/video/168271916


--- type:NormalExercise lang:r  xp:75 skills:1   key:2c0f7cc31b
## Matrices in R Practice

This exercise will allow you to look Explore Matrices. 

*** =instructions
Use R to complete the tasks on the right and answer the following questions. 

1. Find the row sums of c. 
2. Find the column sums of c. 
3. What is the value of the 3rd column and 98th row?


*** =hint
Use your knowledge of Matrices to answer these questions. 

*** =pre_exercise_code
```{r}
#You will find out more about the runif command in a few weeks.
set.seed(1234)
x = runif(5000, 1, 8)
```

*** =sample_code
```{r}
# Do Not Print X as it is a long vector
# Create a matrix of x with 100 columns and fill it by row
# Label this matrix c


# 1. Find the row means of c. 


# 2. Find the column means of c. 


# 3. What is the value of the 3rd column and 98th row?


```

*** =solution
```{r}
# Do Not Print X as it is a long vector
# Create a matrix of x with 100 columns and fill it by row
# Label this matrix c
b <- matrix(x, ncol=100, byrow=TRUE)

# 1. Find the row means of c. 
apply(b, 1, mean)


# 2. Find the column means of c. 
apply(b, 2, mean)

# 3. What is the value of the 3rd column and 98th row?
b[3,98]
```

*** =sct
```{r}
test_error()
test_object("b")
}, {
  test_function("matrix", args = "byrow") 
})
test_object("b")
}, {
  test_function("matrix", args = "ncol") 
})
test_function("apply")
test_output_contains("4.614700")
test_function("apply")
test_output_contains("4.483649")
text_object("b")
test_output_contains("1.80")
success_msg("Great Job")
```



--- type:VideoExercise lang:r xp:25 skills:1      key:7317839f79
## Lists in R

*** =video_link



//player.vimeo.com/video/168275483

--- type:VideoExercise lang:r xp:25 skills:1      key:55e8de92d3
## Dataframes in R

*** =video_link



//player.vimeo.com/video/


