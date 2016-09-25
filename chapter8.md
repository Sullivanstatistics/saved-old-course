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
## Returning Values in Julia
#### Remember to comment out your answers as DataCamp does not accept Julia code.

Consider the function `courses` in the video

*** =instructions

- Return a the string "The cost of ____ mandatory courses and ____ extra course is $____"
- Fill in the blanks with the appropriate values from the function.
- Use the printline function.
- Remember when you need to use an escape character. 
- Paste the output of `courses(2,1)`.


*** =hint

Remember the parts of the function. This is very similar to one created during the video.


*** =pre_exercise_code
```{r}

```


*** =sample_code

```{r}
#function courses( mandatory, extra)
#                  cost_of_course = mandatory * 6126
#                  cost_of_extra = (extra == true ? 5049 : 0)
#                  total_cost = cost_of_course + cost_of_extra
#              end


#courses(2,1) paste output below.
#
```

*** =solution

```{r}
#function courses( mandatory, extra)
#                  cost_of_course = mandatory * 6126
#                  cost_of_extra = (extra == true ? 5049 : 0)
#                  total_cost = cost_of_course + cost_of_extra
#                  return(println("The cost of $mandatory mandatory courses and $extra extra course is \$$total_cost"))
#              end


#courses(2,1) paste output below.
# The cost of 2 mandatory courses and 1 extra course is $17301
```

*** =sct
```{r}
test_student_typed("return", not_typed_msg="Did you remember to use return()?")
test_student_typed("println", not_typed_msg="Remember to use the println function?")
test_student_typed("mandatory", not_typed_msg="Did you remember to call up the number of mandatory courses?")
test_student_typed("extra", not_typed_msg="Did you remember to call up the number of extra courses?")
test_student_typed("total_cost", not_typed_msg="Did you remember to call up the total cost")
test_student_typed("The cost of 2 mandatory courses and 1 extra course is", not_typed_msg="The correct outcome of this is: The cost of 2 mandatory courses and 1 extra course is $17301")

success_msg("Great!")
```




--- type:VideoExercise lang:r xp:25 skills:1 key:59ea3c577a
## Further Function Details in Julia

*** =video_link

//player.vimeo.com/video/184139354



--- type:NormalExercise lang:r xp:100 skills:1 key:7537021881
## map function in Julia
#### Remember to comment out your answers as DataCamp does not accept Julia code.

Consider the function below:

```
map([2, 3, 5, 7]) do x
        if mod(x, 3) == 0
            x^2 + 2x - 4
        elseif mod(x, 3) == 1
            2x^3 + x^2 - 2x + 4
        else
            2x-4
        end
    end
```

*** =instructions

- Copy this into Julia.
- Paste the output of this in a commented form below


*** =hint

Run this function in Julia and then paste the answer.


*** =pre_exercise_code
```{r}

```


*** =sample_code

```{r}
# Paste the outcome below
```

*** =solution

```{r}
# Paste the outcome below
#4-element Array{Int64,1}:
#   0
#  11
#   6
# 725
```

*** =sct
```{r}
test_student_typed("4-element", not_typed_msg="Did you remember to copy this exactly?")
test_student_typed("0", not_typed_msg="You should have had a value of 0.")
test_student_typed("11", not_typed_msg="You should have had a value of 11.")
test_student_typed("6", not_typed_msg="You should have had a value of 6.")
test_student_typed("725", not_typed_msg="You should have had a value of 725.")

success_msg("Great!")
```


--- type:MultipleChoiceExercise lang:r xp:75 skills: key:2526ff8b47
## Functions in Julia MC

Do not run this code in Julia but imagine what would happen if you did:

```
function foo()
        println(x)
    end

    function bar()
        x = 2
        foo()
    end
```

What would the outcome of this be?

*** =instructions

- The outcome would be 2. 
- There would be no outcome it would run and return nothing. 
- This would return an error. 



*** =hint


Try to remember the scope of functions.

*** =pre_exercise_code
```{r}


```

*** =sct
```{r}

test_mc(correct=3, feedback_msgs = c("Incorrect: foo() cannot see what x is.", 
                                        "Incorrect: This function will return something.  ",
                                        "Correct: Since foo() cannot see x = 2 it does not work right. It will return an error. This is because x is outside of the scope of foo(). "))

```





--- type:VideoExercise lang:r xp:25 skills:1 key:1acf8f7cc5
## Functions as Objects in Julia

*** =video_link

//player.vimeo.com/video/184139806



--- type:MultipleChoiceExercise lang:r xp:75 skills: key:7a9a50bad5
## Functions as Objects in Julia MC


which of the following is not true of lambda syntax.

*** =instructions

- It makes the function code more concise.
- It is designed to create rates in our functions. 
- It uses `->` to name a function.



*** =hint


Try to remember the scope of functions.

*** =pre_exercise_code
```{r}


```

*** =sct
```{r}

test_mc(correct=2, feedback_msgs = c("Incorrect: With the removal of the function and end, the code is much more concise. ",
                                    "Correct: It has nothing to do with rates.",
                                    "Incorrect: We do use the -> in order to name the function."))

```



--- type:VideoExercise lang:r xp:25 skills:1 key:f96656952f
## Further Complexities of Functions in Julia

*** =video_link

//player.vimeo.com/video/184141060


--- type:MultipleChoiceExercise lang:r xp:75 skills: key:85c6561b64
## Multiple Dispatch in Julia


Which of the following is true about Multiple Dispatch?


*** =instructions

- It allows a function to use multiple arguments. 
- It allows a function to use multiple methods for different types of data. 
- It dispatches more than one function each time you run it.



*** =hint


Remember what is unique about the * operator. 

*** =pre_exercise_code
```{r}


```

*** =sct
```{r}

test_mc(correct=2, feedback_msgs = c("Incorrect: With the removal of the function and end, the code is much more concise. ",
                                    "Correct: It has nothing to do with rates.",
                                    "Incorrect: We do use the -> in order to name the function."))

```





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


