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
            


# call the function with c(-2,2)

my_abs(c(-2,2))

```

*** =sct
```{r}
test_function_definition("my_abs",
                              function_test= {
                              test_expression_result("my_abs(-1)")
                              test_expression_result("my_abs(1)")
                              }, 
                              body_test = test_function("ifelse", incorrect_msg="Did you use ifelse?"))
test_correct({
  test_object("result")
}, {
  test_function("my_abs")
})
success_msg("Great!")
```


--- type:VideoExercise lang:r xp:25 skills:1 key:e84601da06
## Debugging Functions in R

*** =video_link

//player.vimeo.com/video/184067063



--- type:VideoExercise lang:r xp:25 skills:1 key:3c0bd31c27
## Some Debugging Methods in R

*** =video_link

//player.vimeo.com/video/184080457



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