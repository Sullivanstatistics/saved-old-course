---
title       : Flow Control and Initial Functions in R
description : In this chapter we will work on flow control as well as the start of some basic functions in R. 


--- type:VideoExercise lang:r xp:25 skills:1 key:29e3220aac
## Conditionals in R

*** =video_link

//player.vimeo.com/video/182536770


--- type:NormalExercise lang:r xp:25 skills:1 key:e412be26b2
##Basic Conditionals in R


Our goal now is to start solving problems with what we encounter in the real world.  Before we can do this we need to understand how to evaluate some simple logical statements. 
*** =instructions

Write R expressions that deal with the last element of vector `nums`:

- Define the last element of the vector.
- Is the last element between 3 and 7
- Is the last element less than or equal to 5 or greater than 20. 


*** =hint

Here is a hint: use `<-` for assignment


*** =pre_exercise_code
```{r}
set.seed(1234)
nums <- runif(10000, 1, 25)
```


*** =sample_code

```{r}
# nums is stored for you
# Define last to be the last element of nums



# Is last between 3 and 7



# Is last less than or equal to  5 or greater than 20.  
```

*** =solution

```{r}
# nums is stored for you
# Define last to be the last element of nums
last <- tail(nums,1)


# Is last between 3 and 7
3 < last & last < 7


# Is last less than or equal to  5 or greater than 20. 

last <= 5  | last >20
```

*** =sct
```{r}
test_object("last")
test_output_contains("FALSE", incorrect_msg="Make sure to define this using an & as well as correct < or >") 
test_student_typed("<=", not_typed_msg="Make sure to define this using an & as well as correct < or >")
test_output_contains("TRUE", incorrect_msg="Make sure to define this using an | as well as correct < or >") 
success_msg("Great!")
```




--- type:VideoExercise lang:r xp:25 skills:1 key:f1dc5c338b
## Iterations in R

*** =video_link

//player.vimeo.com/video/182545482



--- type:NormalExercise lang:r xp:25 skills:1 key:2d3ff46486
##Practicing `if` statements

We will work with some simple `if` expressions in this part of the lab. 
*** =instructions

Many times with continuous random variables we wish to place them into named categories. One of the easiest ways to do this is with a simple `if` statement.

- Consider the variable `bmi`.
- Write an if statement so that if `bmi` is greater than or equal to 35 it prints `Obese`. 


*** =hint

Recall with the `if` statement we need the correct boolean and then inside brackets what you want to do with that Boolean. 


*** =pre_exercise_code
```{r}


```


*** =sample_code

```{r}
# bmi is defined for you
bmi <- 35

# write the if statement about bmi


```

*** =solution

```{r}
# bmi is defined for you
bmi <- 35

# write the if statement about bmi

if (bmi >= 35){
    print("Obese")
}

```

*** =sct
```{r}
test_object("bmi", incorrect_msg="Make sure bmi is set to its origina value!")
test_if_else(if_cond_test=test_student_typed(c("bmi >= 35", "35 <= bmi"), not_typed_msg="Make sure to include spaces between elements in the Boolean and make sure you have the correct comparisons"), if_expr_test=test_function("print", incorrect_msg="Did you remember to print out Obese")) 
success_msg("Great!")
```


--- type:NormalExercise lang:r xp:25 skills:1 key:45e09152d8
##Practicing `if` and `else` statements

We created a way to show if a `bmi` was obese. However we have done nothing for those that are not obese. We now must complete this. 
For the purposes of this exercise you may **NOT** use the `ifelse()` function. 
*** =instructions



- Consider the variable `bmi`.
- Write an if statement so that if `bmi` is greater than or equal to 35 it prints `Obese`. 
- If the Boolean is not true, make sure it prints `Not Obese`. 


*** =hint

Recall with the `if` statement we need the correct boolean and then inside brackets what you want to do with that Boolean. 


*** =pre_exercise_code
```{r}


```


*** =sample_code

```{r}
# bmi is defined for you
bmi <- 35

# write the if statement about bmi


```

*** =solution

```{r}
# bmi is defined for you
bmi <- 35

# write the if statement about bmi

if (bmi >= 35){
    print("Obese")
} else {
    print("Not Obese")
}


```

*** =sct
```{r}
test_object("bmi", incorrect_msg="Make sure bmi is set to its origina value!")
test_if_else(if_cond_test=test_student_typed(c("bmi >= 35", "35 <= bmi"), not_typed_msg="Make sure to include spaces between elements in the Boolean and make sure you have the correct comparisons"), if_expr_test=test_function("print", incorrect_msg="Did you remember to print out Obese"), else_expr_test=test_function("print", incorrect_msg="Did you remember to print out Not Obese") ) 
success_msg("Great!")
```




--- type:NormalExercise lang:r xp:25 skills:1 key:1a76220ea7
##Putting all the `if` and `else` statements together. 

We have now made it so we can classify if a person is obese to not obese. However with BMI there are many more categories. 

| Category | BMI   |
| -------- | ----- |
| Underweight | 18.5 | 
| Normal | 25 |
|Overweight | 30|
| Obese | 35|


*** =instructions



- Consider the variable `bmi`.
- Write `if`, `elseif` and `else` statements to match the table above. 
- Make sure you know what Boolean you need. 
- Start with the underweight category and move your way down through the chart for this. 


*** =hint

Recall with the `if` statement we need the correct boolean and then inside brackets what you want to do with that Boolean. 


*** =pre_exercise_code
```{r}


```


*** =sample_code

```{r}
# bmi is defined for you
bmi <- 35

# write the if statement about bmi


```

*** =solution

```{r}
# bmi is defined for you
bmi <- 35

# write the if statement about bmi

if (bmi <= 18.5){
    print("Underweight")
} else if (bmi <= 25) {
    print("Normal")
} else if (bmi <= 30) {
    print("Overweight")
} else {
    print("Obese")
}


```

*** =sct
```{r}
test_object("bmi", incorrect_msg="Make sure bmi is set to its origina value!")
test_if_else(if_cond_test=test_student_typed(c("bmi >= 35", "35 <= bmi"), not_typed_msg="Make sure to include spaces between elements in the Boolean and make sure you have the correct comparisons"), if_expr_test=test_function("print", incorrect_msg="Did you remember to print out Obese"), else_expr_test=test_function("print", incorrect_msg="Did you remember to print out Not Obese") ) 
success_msg("Great!")
```




--- type:VideoExercise lang:r xp:25 skills:1 key:5952e54720
## Avoiding Iterations in R

*** =video_link

//player.vimeo.com/video/182551068



--- type:VideoExercise lang:r xp:25 skills:1 key:b330fb454f
## Functions in R

*** =video_link

//player.vimeo.com/video/183148895





--- type:VideoExercise lang:r xp:25 skills:1 key:9b442d9826
## Example of a Function in R

*** =video_link

//player.vimeo.com/video/183153604



--- type:VideoExercise lang:r xp:25 skills:1 key:d11132a233
## What should be a function?

*** =video_link

//player.vimeo.com/video/183155131