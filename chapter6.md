---
title       : Flow Control in Julia
description : We will discuss flow control in Julia for this chapter. 





--- type:VideoExercise lang:r xp:25 skills:1 key:b330fb454f
## Controlling the Flow in Julia

*** =video_link

//player.vimeo.com/video/183156471







--- type:MultipleChoiceExercise lang:r xp: skills: key:2526ff8b47
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



--- type:VideoExercise lang:r xp:25 skills:1 key:64225b942f
## Loops and Iterations in Julia

*** =video_link

//player.vimeo.com/video/183157227


--- type:VideoExercise lang:r xp:25 skills:1 key:06fa978938
## Further Iteration in Julia

*** =video_link

//player.vimeo.com/video/