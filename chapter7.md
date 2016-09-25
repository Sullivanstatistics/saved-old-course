---
title       : Functions in R
description : In this chapter we will explore creating and debugging functions in R.



--- type:VideoExercise lang:r xp:25 skills:1 key:b330fb454f
## Basic Function Design in R

*** =video_link

//player.vimeo.com/video/184065557




--- type:NormalExercise lang:r xp:100 skills:1 key:e412be26b2
## Basic Functions in R Exercise


We want to start creating functions in R but we need to start out slowly. 

*** =instructions

Write an R function called `welcome`. 

- This function will take no arguments
- When called this function will print out "Welcome to Functions in R!"
- Write this function and then call it. 


*** =hint

Remember the parts of the function. This is very similar to one created during the video.


*** =pre_exercise_code
```{r}

```


*** =sample_code

```{r}
# Write the function welcome


# call the function welcome
```

*** =solution

```{r}
# Write the function welcome

welcome <- function(){
        print("Welcome to Functions in R!")
        }

# call the function welcome

welcome()

```

*** =sct
```{r}
test_function_definition("welcome",
                              body_test = test_function("print", incorrect_msg="Did you call the print function?"))
test_output_contains("Welcome to Functions in R!")
success_msg("Great!")
```





--- type:NormalExercise lang:r xp:100 skills:1 key:0e2f719dab
## Slightly More advanced Functions in R Exercise


We will now make a function that takes some arguments in R. 

*** =instructions

Write a function called `my_abs`.

- This function will take an argument `x`. 
- This function will use `ifelse` function to define output absolute value of `x`.
- Call this function for `c(-2,2)`.


*** =hint

Remember the parts of the function. This is very similar to one created during the video.


*** =pre_exercise_code
```{r}

```


*** =sample_code

```{r}
# Write the function my_abs


# call the function with c(-2,2)
```

*** =solution

```{r}
# Write the function my_abs

my_abs <- function(x){
            ifelse(x>=0, x, -x)
            }
            


# call the function with c(-2,2) name this out

out <- my_abs(c(-2,2))

```

*** =sct
```{r}
test_function_definition("my_abs",
                              function_test= {
                              test_expression_result("my_abs(-1)")
                              test_expression_result("my_abs(1)")
                              }, 
                              body_test = test_function("ifelse", incorrect_msg="Did you use ifelse?"))
test_object("out")
success_msg("Great!")
```




--- type:NormalExercise lang:r xp:100 skills:1 key:abb14a9293
## Functions as Objects in R Exercise


We will now make a function that calls other functions. 

*** =instructions

Write a function called `my_row`.

- This function will take arguments, `mat` and `func`. 
- This function will use the `apply()` function with `mat` as the object and `func` as the function. 
- Make sure this operates on the row.
- Call this functon for `mat=A` and `func=mean`. Name this out.


*** =hint

Remember the parts of the function. This is very similar to one created during the video.


*** =pre_exercise_code
```{r}
A = matrix( 
     c(2, 4, 3, 1, 5, 7), # the data elements 
    nrow=2,              # number of rows 
    ncol=3,              # number of columns 
    byrow = TRUE)        # fill matrix by rows
```


*** =sample_code

```{r}
# Write the function my_row


# call the function as directed and name out
```

*** =solution

```{r}
# Write the function my_row

my_row = function(mat,func){
                apply(mat, 1, func)
                }

# call the function as directed and name out
out <- my_row(A, mean)
```

*** =sct
```{r}
test_function_definition("my_row",
                              function_test= {
                              test_expression_result("my_row(A,sum)")
                              test_expression_result("my_row(2*A,mean)")
                              }, 
                              body_test = test_function("apply", incorrect_msg="Did you use apply?"))
test_object("out")
success_msg("Great!")
```

--- type:VideoExercise lang:r xp:25 skills:1 key:e84601da06
## Debugging Functions in R

*** =video_link

//player.vimeo.com/video/184067063



--- type:MultipleChoiceExercise lang:r xp:75 skills: key:2526ff8b47
## Debugging Functions Multiple Choice 


With Debugging we want to make sure we follow some procedures in order to correctly diagnose and repair our functions. 

Answer the following Question. 

*** =instructions

Which of the following is **NOT** a stage of debugging.


- Modify the Code.
- Characterize the Error
- Localize the error
- Delete code leading to error.



*** =hint

Remember the stages of debugging

*** =pre_exercise_code
```{r}


```

*** =sct
```{r}

test_mc(correct=4, feedback_msgs = c("Incorrect: We need to modify the code in order to remove the error", 
                                        "Incorrect: This is the first stage, where we try and figure out what is going wrong. ",
                                        "Incorrect: We need to figure out where in the function the error is coming from before modifying.",
                                        "Correct: We should not delete the code but correct it! "))

```









--- type:VideoExercise lang:r xp:25 skills:1 key:3c0bd31c27
## Some Debugging Methods in R

*** =video_link

//player.vimeo.com/video/184080457





--- type:NormalExercise lang:r xp:100 skills:1 key:0f6e468d43
## Debugging Methods in R Exercise 1 

We will begin with some simple debugging methods. 
*** =instructions

Consider the function `my_mean`

- This function does not work on strings. 
- Use the `stopifnot()` function to stop if the value put into this function is a not numeric.  


*** =hint

Figure out how to insert the `stopifnot` in here. How can we test if our value is a string?


*** =pre_exercise_code
```{r}
allow_solution_error()
```


*** =sample_code

```{r}

#Add stopifnot message in so that you do not get an error
# when you use a string

#This function calculates the mean of an object.size
# The object should not be a string
# It outputs the mean
my_mean <- function(x){
            mu <- sum(x)/length(x)
            return(mu)
            }

# If you do this right, you will not get an error here.

out <- my_mean("Statistical Computing")
                
```

*** =solution

```{r}
#Add stopifnot message in so that you do not get an error
# when you use a string

#This function calculates the mean of an object.size
# The object should not be a string
# It outputs the mean
my_mean <- function(x){
            stopifnot(is.numeric(x))
            mu <- sum(x)/length(x)
            return(mu)
            }

# If you do this right, you will not get an error here.

out <- my_mean(as.character(2))
       
```

*** =sct
```{r}
success_msg("Great!")
```

test_e







--- type:VideoExercise lang:r xp:25 skills:1 key:35d2362554
## Designing Programs for Debugging in R

*** =video_link

//player.vimeo.com/video/184133246



--- type:VideoExercise lang:r xp:25 skills:1 key:b0337a0e75
## Designing Functions in R

*** =video_link

//player.vimeo.com/video/184134719


--- type:VideoExercise lang:r xp:25 skills:1 key:2f6772ef47
## Top Down Function Design in R

*** =video_link

//player.vimeo.com/video/184136056


--- type:VideoExercise lang:r xp:25 skills:1 key:5fc6a5dbb8
## Refactoring Functions in R

*** =video_link

//player.vimeo.com/video/184136884