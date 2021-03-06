---
title       : Flow Control and Initial Functions in R
description : In this chapter we will work on flow control as well as the start of some basic functions in R. 


--- type:VideoExercise lang:r xp:25 skills:1 key:29e3220aac
## Conditionals in R

*** =video_link

//player.vimeo.com/video/182536770


--- type:NormalExercise lang:r xp:100 skills:1 key:e412be26b2
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







--- type:NormalExercise lang:r xp:100 skills:1 key:2d3ff46486
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
test_object("bmi", incorrect_msg="Make sure bmi is set to its original value!")
test_if_else(if_cond_test=test_student_typed(c("bmi >= 35", "35 <= bmi"), not_typed_msg="Make sure to include spaces between elements in the Boolean and make sure you have the correct comparisons"), if_expr_test=test_function("print", incorrect_msg="Did you remember to print out Obese")) 
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

We have now made it so we can classify if a person is obese to not obese. However with BMI there are many more categories. In each category the number represents an inclusive number. 

| Category | BMI   |
| -------- | ----- |
| Underweight | 18.5 | 
| Normal | 25 |
|Overweight | 30|
| Obese | 35|


*** =instructions



- Consider the variable `bmi`.
- Write `if`, `else if` and `else` statements to match the table above. 
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
test_if_else(if_cond_test=test_student_typed(c("bmi <= 18.5", "18.5 >= bmi"), not_typed_msg="Make sure to include spaces between elements in the Boolean and make sure you have the correct comparisons"), if_expr_test=test_function("print", incorrect_msg="Did you remember to print out Underweight"), else_expr_test=test_function("print", incorrect_msg="Did you remember to print out Obese") ) 
success_msg("Great!")
```




--- type:VideoExercise lang:r xp:25 skills:1 key:f1dc5c338b
## Iterations in R

*** =video_link

//player.vimeo.com/video/182545482




--- type:NormalExercise lang:r xp:100 skills:1 key:fb98726742
##Basic `for()` loops
For loops can be crucial for data analysis and cleaning. It is important to take time to work through some simple ones. 


*** =instructions

- Consider vector `x` which is already loaded into your workspace. 
- Write a loop that iterates through `x` and calculates the square root of each element. 
- Note: This won't print out the square roots. 

*** =hint

Recall your basics of a loop and make sure all components are there. Please use the sqrt() function rather than an exponential argument. 

*** =pre_exercise_code
```{r}
set.seed(1234)
x <- seq(1,1000, by= 6)

```


*** =sample_code

```{r}
#Do not print out x but work through the loop without having to print it
# Write the loop below


```

*** =solution

```{r}
#Do not print out x but work through the loop without having to print it
# Write the loop below

for (i in x){
    sqrt(i)
}


```

*** =sct
```{r}
test_object("x", incorrect_msg="Make sure not to change x!")
test_for_loop(cond_test = test_student_typed("in x", not_typed_msg="For this situation you do not need to use length(x) just use for (i in x)"), expr_test = test_function("sqrt",  eval = FALSE, incorrect_msg="Make sure to use the sqrt function."))
success_msg("Great!")
```





--- type:NormalExercise lang:r xp:100 skills:1 key:44ef05ca18
##Loop Through a matrix
Before we did a basic loop through a vector. We only needed to concern ourselves with one dimension. If we have a matric we need to now work with rows and columns. Remember that if `x` is a matrix, we index it by `x[r,c]` where `r` is a row and `x` is a column. 


*** =instructions

- Consider matrix `x` which is already loaded into your workspace. 
- What are the dimensions of `x`?
- Calculate the mean of the 3rd column.
- Iterate through the columns to find the mean of each. 
 



*** =hint

Recall your basics of a loop and make sure all components are there. Please use the sqrt() function rather than an exponential argument. 

*** =pre_exercise_code
```{r}
set.seed(1234)
x <- runif(1008, 0, 10)
x <- matrix(x,  ncol=4)

```


*** =sample_code

```{r}
#Do not print out x but work through the loop without having to print it

# What are the dimensions of x



#Index the dimensions to get the number of columns


#Calculate the mean of the 3rd column


# Iterate through each column and calculate the mean



```

*** =solution

```{r}
#Do not print out x but work through the loop without having to print it

# What are the dimensions of x

dim(x)

#Index the dimensions to get the number of columns

dim(x)[2]


#Calculate the mean of the 3rd column and name this mean3

mean3 <- mean(x[,3])


# Iterate through each column and calculate the mean

for (i in 1:dim(x)[2]){
    mean(x[,i])
}

```

*** =sct
```{r}
test_object("x", incorrect_msg="Make sure not to change x!")
test_function("dim", eval=FALSE, incorrect_msg="Make sure to use the dim() function.")
test_function("dim", eval=FALSE, incorrect_msg="Make sure to use the dim() function.")
test_student_typed("(x)[2]", not_typed_msg="Make sure to index the dimensions in order to get the columns")
test_object("mean3", incorrect_msg="Make sure to find mean of the 3rd column")
test_for_loop(cond_test = test_student_typed("in 1:dim(x)[2]", not_typed_msg="For this situation use i in 1:dim(x)[2]"), expr_test = test_function("mean", "x", eval = FALSE, incorrect_msg="Make sure to use the mean function."))

success_msg("Great!")
```






--- type:NormalExercise lang:r xp:100 skills:1 key:8f8dc28fd3
##Using a `for` loop to evaluate BMI. 

We have now made it so we can classify if a person is obese to not obese. However with BMI there are many more categories. 

| Category | BMI   |
| -------- | ----- |
| Underweight | 18.5 | 
| Normal | 25 |
|Overweight | 30|
| Obese | >30|


In our last example this only worked for a single BMI value. Your next task will be to make this iterate through a vector of values. 

*** =instructions



- Consider the variable `bmi`.
- Use `if`, `else if` and `else` statements from your previous work. 
- Loop through the vector `bmi` and print out the BMI categories for each patient. 


*** =hint

Recall with the `if` statement we need the correct boolean and then inside brackets what you want to do with that Boolean. 


*** =pre_exercise_code
```{r}


```


*** =sample_code

```{r}
# bmi is defined for you
bmi <- c(17, 18.5, 23, 25, 28, 31, 35)

# Calculate the length of the vector bmi

# write the loop to print out the evaluation of bmi


```

*** =solution

```{r}
# bmi is defined for you
bmi <- c(17, 18.5, 23, 25, 28, 31, 35)

# Calculate the length of the vector bmi
length(bmi)


# Use the calculation of length to iterate through
# write the loop to print out the evaluation of bmi
# hint you will need to use individual values bmi[i]


for (i in 1:length(bmi)){
  if (bmi[i] <= 18.5){
    print("Underweight")
  } else if (bmi[i] <= 25) {
    print("Normal")
  } else if (bmi[i] <= 30) {
    print("Overweight")
  } else {
    print("Obese")
  }
}


```

*** =sct
```{r}
test_object("bmi", incorrect_msg="Make sure bmi is set to its origina value!")
test_function("length", eval=FALSE, incorrect_msg="Did you use a function to find length?")

test_for_loop(cond_test = test_student_typed("in 1:length(bmi)", not_typed_msg="For this situation use i in 1:length(bmi)"), expr_test =test_if_else(if_cond_test=test_student_typed(c("bmi[i] <= 18.5", "18.5 >= bmi[i]"), not_typed_msg="Make sure to include spaces between elements in the Boolean and make sure you have the correct comparisons"), if_expr_test=test_function("print", incorrect_msg="Did you remember to print out Underweight"), else_expr_test=test_function("print", incorrect_msg="Did you remember to print out Obese") )  )



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




--- type:NormalExercise lang:r xp:100 skills:1 key:124cb65c8e
##Basic function in R
We need to be able to write our own functions. We will begin with a simple print function and move up from there. 


*** =instructions

- Consider vector `x` which is already loaded into your workspace. 
- write a function that prints x.  
- name this `my_print`

*** =hint


*** =pre_exercise_code
```{r}
set.seed(1234)
x <- seq(1,1000, by= 6)

```


*** =sample_code

```{r}
#Do not print out x but work through the loop without having to print it
# Write the function below


```

*** =solution

```{r}
#Do not print out x but work through the loop without having to print it
# Write the function below


my_print <- function(x){
                print(x)
                }




```

*** =sct
```{r}
test_object("x", incorrect_msg="Make sure not to change x!")
test_function_definition("my_print", function_test= test_expression_result("my_print(x)"), body_test = test_function("print"))
success_msg("Great!")
```


--- type:NormalExercise lang:r xp:100 skills:1 key:2544dab41f
##Basic functions in R part 2
We need to be able to write our own functions. Now write a function which adds the absolute value of two objects. 


*** =instructions

- write a function that adds the absolute value of `a` and `b`.
- Name this `my_abs_sum`.

*** =hint


*** =pre_exercise_code
```{r}
set.seed(1234)
x <- seq(1,1000, by= 6)

```


*** =sample_code

```{r}

# Write the function below


```

*** =solution

```{r}

# Write the function below


my_abs_sum <- function(a,b){
                abs(a) + abs(b)
                }




```

*** =sct
```{r}
test_function_definition("my_abs_sum",
                         function_test = {
                           test_expression_result("my_abs_sum(1,2)")
                           test_expression_result("my_abs_sum(-1,2)")
                           test_expression_result("my_abs_sum(1,-2)")
                           test_expression_result("my_abs_sum(-1,-2)")
                         },
                         body_test = {
                            test_function("abs", index = 1)
                            test_function("abs", index = 2)
                         })
success_msg("Great!")
```






--- type:VideoExercise lang:r xp:25 skills:1 key:9b442d9826
## Example of a Function in R

*** =video_link

//player.vimeo.com/video/183153604



--- type:VideoExercise lang:r xp:25 skills:1 key:d11132a233
## What should be a function?

*** =video_link

//player.vimeo.com/video/183155131