---
title       : Flow Control in Julia
description : We will discuss flow control in Julia for this chapter. 





--- type:VideoExercise lang:r xp:25 skills:1 key:b330fb454f
## Controlling the Flow in Julia

*** =video_link

//player.vimeo.com/video/183156471







--- type:MultipleChoiceExercise lang:r xp:75 skills: key:2526ff8b47
## Ternary Expressions in Julia


We now are moving into flow control in Julia. What would the outcome of the following ternary expression be:

```
julia> x=1
1
julia> x>3 ? "False" : "True"
```

*** =instructions

- Error
- True
- False
- 1



*** =hint

Remember what Julia does here not the answer in your mind. 

*** =pre_exercise_code
```{r}


```

*** =sct
```{r}

test_mc(correct=2, feedback_msgs = c("Incorrect: This will run in Julia without error.", 
                                        "Correct: Julia defaults to the second position when the statement is False. ",
                                        "Incorrect: The outcome is mathematically False but that is not what Julia does here.",
                                        "Incorrect: This is the value of x but not a solution here."))

```






--- type:VideoExercise lang:r xp:25 skills:1 key:3beefa24b7
## Further Flow Control in Julia

*** =video_link

//player.vimeo.com/video/183155844



--- type:VideoExercise lang:r xp:25 skills:1 key:533c100147
## Conditional Evaluation in Julia

*** =video_link

//player.vimeo.com/video/183156845





--- type:NormalExercise lang:r xp:100 skills:1 key:2d3ff46486
##Practicing `if` statements in Julia

#### Remember to comment out your answers as DataCamp does not accept Julia code. 

We will work with some simple `if` expressions in this part of the lab. 
*** =instructions

Many times with continuous random variables we wish to place them into named categories. One of the easiest ways to do this is with a simple `if` statement.

- Consider the variable `bmi`.
- Write an if statement so that if `bmi` is greater than or equal to 35 it prints `Obese`. 
- - Use the `print` function.


*** =hint

Recall with the `if` statement we need the correct boolean and then inside brackets what you want to do with that Boolean. 


*** =pre_exercise_code
```{r}


```


*** =sample_code

```{r}

# write the if statement about bmi


```

*** =solution

```{r}

# write the if statement about bmi

# if bmi >= 35
#    print("Obese")
# end

```

*** =sct
```{r}
test_student_typed("if bmi >= 35", not_typed_msg="make sure to use if bmi >=35")

success_msg("Great!")
```


--- type:NormalExercise lang:r xp:100 skills:1 key:45e09152d8
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




--- type:NormalExercise lang:r xp:100 skills:1 key:1a76220ea7
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
bmi <- 25

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
test_if_else(if_cond_test=test_student_typed(c("bmi <= 18.5", "18.5 >= bmi"), not_typed_msg="Make sure to include spaces between elements in the Boolean and make sure you have the correct comparisons"), if_expr_test=test_function("print", incorrect_msg="Did you remember to print out Underweight"), else_expr_test=test_function("print", incorrect_msg="Did you remember to print out Obese") ) 
success_msg("Great!")
```




--- type:VideoExercise lang:r xp:25 skills:1 key:64225b942f
## Loops and Iterations in Julia

*** =video_link

//player.vimeo.com/video/183157227


--- type:VideoExercise lang:r xp:25 skills:1 key:06fa978938
## Further Iteration in Julia

*** =video_link

//player.vimeo.com/video/