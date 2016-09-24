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
                            function_test= test_output_contains("Welcome to Functions in R!", incorrect_msg = "Did you remember to ask it to print the right message?"),
                            body_test = test_function("print", incorrect_msg="Did you call the pirnt function?"))
test_correct({
  test_object("result")
}, {
  test_function("welcome")
})
success_msg("Great!")
```

test_fu



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