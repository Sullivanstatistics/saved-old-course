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

Remember how Julia does an if statement, no brackets, braces but needs and end

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
test_student_typed("print(", not_typed_msg="make sure to use print function and not println")
test_student_typed("end", not_typed_msg="make sure to end.")
success_msg("Great!")
```


--- type:NormalExercise lang:r xp:100 skills:1 key:45e09152d8
##Practicing `if` and `else` statements

#### Remember to comment out your answers as DataCamp does not accept Julia code. 


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

# write the if statement about bmi


```

*** =solution

```{r}
# write the if statement about bmi

# if bmi >= 35
#     print("Obese")
# else 
#     print("Not Obese")
# end


```

*** =sct
```{r}
test_student_typed("if bmi >= 35", not_typed_msg="make sure to use if bmi >=35")
test_student_typed("print(", not_typed_msg="make sure to use print function and not println")
test_student_typed("else", not_typed_msg="Make sure that you use else.")
test_student_typed("print(", not_typed_msg="make sure to use print function and not println")
test_student_typed("end", not_typed_msg="make sure to end.")
success_msg("Great!")
```




--- type:NormalExercise lang:r xp:100 skills:1 key:1a76220ea7
##Putting all the `if` and `else` statements together. 


#### Remember to comment out your answers as DataCamp does not accept Julia code. 

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

# write the if statement about bmi


```

*** =solution

```{r}

# write the if statement about bmi

# if bmi <= 18.5
#    print("Underweight")
# else if (bmi <= 25) 
#    print("Normal")
# else if (bmi <= 30) 
#    print("Overweight")
# else 
#    print("Obese")
# end


```

*** =sct
```{r}
test_student_typed("if bmi <= 18.5", not_typed_msg="make sure to use if bmi <= 18.5")
test_student_typed("print(", not_typed_msg="make sure to use print function and not println")
test_student_typed("else if", not_typed_msg="Make sure that you use else if.")
test_student_typed("print(", not_typed_msg="make sure to use print function and not println")
test_student_typed("else if", not_typed_msg="Make sure that you use else if.")
test_student_typed("print(", not_typed_msg="make sure to use print function and not println")
test_student_typed("else", not_typed_msg="Make sure that you use else if.")
test_student_typed("print(", not_typed_msg="make sure to use print function and not println")
test_student_typed("end", not_typed_msg="make sure to end.")
success_msg("Great!")
```




--- type:VideoExercise lang:r xp:25 skills:1 key:64225b942f
## Loops and Iterations in Julia


*** =video_link

//player.vimeo.com/video/183157227


--- type:NormalExercise lang:r xp:100 skills:1 key:fb98726742
##Basic `for()` loops in Julia
#### Remember to comment out your answers as DataCamp does not accept Julia code. 


For loops can be crucial for data analysis and cleaning. It is important to take time to work through some simple ones. 


*** =instructions

- Iterate through a sequence of numbers from 1 to 200 by 25
- Print on a separate line whether or not it is prime. 

*** =hint

Recall your basics of a loop and make sure all components are there. 
*** =pre_exercise_code
```{r}


```


*** =sample_code

```{r}
#Write the loop out and remember how Julia creates a sequence


```

*** =solution

```{r}
#Do not print out x but work through the loop without having to print it
# Write the loop below

# for i in 1:25:200
#        println(isprime(i))
#   end

```

*** =sct
```{r}
test_student_typed("for", not_typed_msg= "Did you use a for loops?")
test_student_typed("1:25:200", not_typed_msg="Remember how Julia creates a sequence by every 25 numbers.")
test_student_typed("println", not_typed_msg="Did you remember to use println instead of print. ")
test_student_typed("isprime", not_typed_msg= "Did you use the isprime function?")
test_student_typed("end", not_typed_msg="Did you remember to end it?")
success_msg("Great!")
```




--- type:NormalExercise lang:r xp:100 skills:1 key:108594c0c1
##Iterating through a string in Julia
#### Remember to comment out your answers as DataCamp does not accept Julia code. 


Julia allows us to easily loop through a string. 


*** =instructions

- Create a sentence
- Iterate through this sentance using the iterator `letter`.
- print each letter with a space after it. 

*** =hint

Recall your basics of a loop and make sure all components are there. 


*** =sample_code

```{r}
#Write the loop out 

#My sentance:


```

*** =solution

```{r}
#Write the loop out 

#My sentance: "This is the best class ever!"

# julia> for letter in "This is the best class ever!"
#                  print(letter, " ")
#               end


```

*** =sct
```{r}
test_student_typed("for", not_typed_msg= "Did you use a for loops?")
test_student_typed("letter", not_typed_msg="Use letter as the iterator here.")
test_student_typed("print(",  not_typed_msg="Did you remember to use print? ")
test_student_typed("letter",  not_typed_msg="Use your iterator of letter.")
test_student_typed("end", not_typed_msg="Did you remember to end it?")
success_msg("Great!")
```






--- type:NormalExercise lang:r xp:100 skills:1 key:bff406a879
## While loop in Julia
#### Remember to comment out your answers as DataCamp does not accept Julia code. 


While loops are important when we are trying to convege on values. We use these a lot in optimization. 


*** =instructions

- Create a `while` loop.
- Make sure to run this loop while `x < 10`
- Have this loop print `x` on its own line until the end, increasing by 0.5 each time. 

*** =hint

Recall your basics of a loop and make sure all components are there. 


*** =sample_code

```{r}
#Write the loop out 



```

*** =solution

```{r}
#Write the loop out 

#julia> while x < 10
#          println(x)
#           x += 0.5
#       end
```

*** =sct
```{r}
test_student_typed("while", not_typed_msg= "Did you use a while loop?")
test_student_typed("x < 10", not_typed_msg="Remember to do this while x < 10")
test_student_typed("println",  not_typed_msg="Did you remember to use println function? ")
test_student_typed("x += 0.5",  not_typed_msg="Did you increase it by 0.5?")
test_student_typed("end", not_typed_msg="Did you remember to end it?")
success_msg("Great!")
```






--- type:NormalExercise lang:r xp:100 skills:1 key:47a7431bf2
## While loop in Julia with `break`
#### Remember to comment out your answers as DataCamp does not accept Julia code. 


While loops are important when we are trying to convege on values. We use these a lot in optimization. 


*** =instructions

- Create a `while` loop.
- Make sure to run this loop while `x < 10`
- Have this loop print `x` on its own line until the end, increasing by 0.5 each time. 
- This time use a break command to stop it rather than `while x < 10`, this would be `while true`.

*** =hint

Recall your basics of a loop and make sure all components are there. 


*** =sample_code

```{r}
#Write the loop out 



```

*** =solution

```{r}
#Write the loop out 

#julia> while true
#          println(x)
#           x += 0.5
#           x >= 10 && break
#       end
```

*** =sct
```{r}
test_student_typed("while", not_typed_msg= "Did you use a while loop?")
test_student_typed("true", not_typed_msg="Remember to do this for all true values?")
test_student_typed("println",  not_typed_msg="Did you remember to use println function? ")
test_student_typed("x += 0.5",  not_typed_msg="Did you increase it by 0.5?")
test_student_typed("x >= 10", not_typed_msg="Remember it does not stop for x < 10.")
test_student_typed("&& break", not_typed_msg="Did you remeber to break?")
test_student_typed("end", not_typed_msg="Did you remember to end it?")
success_msg("Great!")
```

--- type:VideoExercise lang:r xp:25 skills:1 key:06fa978938
## Further Iteration in Julia

*** =video_link

//player.vimeo.com/video/183471255