---
title       : Functions in Julia
description : We will explore functions in Julia in this chapter.




--- type:VideoExercise lang:r xp:25 skills:1 key:b330fb454f
## Basic Functions in Julia

*** =video_link

//player.vimeo.com/video/184138658





--- type:NormalExercise lang:r xp:100 skills:1 key:e412be26b2
## Basic Functions in Julia Exercise
#### Remember to comment out your answers as DataCamp does not accept Julia code. 

We will start out with a single expression function in Julia. 

*** =instructions

Write a julia function called `geom_average`. 

- This function will take the arguemnts `a` and `b`. 
- When this function is called it will take the `sqrt` of the sum of `a` squared and `b` squared.
- Write this function on one line. 


*** =hint

Remember the parts of the function. This is very similar to one created during the video.


*** =pre_exercise_code
```{r}

```


*** =sample_code

```{r}
# Write the function geom_average


# call the function with arguments 3 and 4

```

*** =solution

```{r}
# Write the function geom_average

# geom_avg(a,b) = sqrt(a^2 + b^2)

# call the function with arguments 3 and 4

#geom_avg(3,4)
#5.0

```

*** =sct
```{r}
test_student_typed("geom_average", not_typed_msg="Did you name this geom_average?")
test_student_typed("sqrt", not_typed_msg="Did you call the sqrt function?")
test_student_typed("a^2 + b^2", not_typed_msg="Did you remember to use a^2 + b^2?")
test_student_typed("geom_average", not_typed_msg="Did you call the function into use?")
test_student_typed("5.0", not_typed_msg="Did you paste the answer of the function call in here?")
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



--- type:VideoExercise lang:r xp:25 skills:1 key:59ea3c577a
## Further Function Details in Julia

*** =video_link

//player.vimeo.com/video/184139354


--- type:VideoExercise lang:r xp:25 skills:1 key:1acf8f7cc5
## Functions as Objects in Julia

*** =video_link

//player.vimeo.com/video/184139806


--- type:VideoExercise lang:r xp:25 skills:1 key:f96656952f
## Further Complexities of Functions in Julia

*** =video_link

//player.vimeo.com/video/184141060



--- type:VideoExercise lang:r xp:25 skills:1 key:f708daa41e
## Exceptions in Julia

*** =video_link

//player.vimeo.com/video/184141478


--- type:VideoExercise lang:r xp:25 skills:1 key:f52e5b57c6
## Handling Exceptions in Julia

*** =video_link

//player.vimeo.com/video/184142074



--- type:VideoExercise lang:r xp:25 skills:1 key:03fdb184eb
## Advanced Exception Hnadling in Julia

*** =video_link

//player.vimeo.com/video/184142654


