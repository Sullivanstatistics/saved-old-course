---
title       : Data Wrangling in R with plyr and dplyr
description : In this chapter we will begin to explore large data in R. We will learn data wrangling techniques such as split, apply and combine with plyr and using tibbles and dplyr on large data. 


--- type:VideoExercise lang:r xp:25 skills:1 key:b330fb454f
## Tibbles in R

*** =video_link

//player.vimeo.com/video/187459312


--- type:NormalExercise lang:r xp:100 skills:1 key:e412be26b2
## Working with tibbles in R


Lets look at some features of tibbles in R. 

*** =instructions


Explore the tibble in the exercise below. 

*** =hint




*** =pre_exercise_code
```{r}

library(tibble)
tib <- tibble( x = letters, y = rank(letters))

```


*** =sample_code

```{r}
# Print the tibble `tib`




# Call up x from tib using a dollar sign name this x1





# Call up x from tib using double brackets and name this x2



# Are x1 and x2 equal?


```

*** =solution

```{r}
# Print the tibble `tib`

tib


# Call up x from tib using a dollar sign name this x1


x1 = tib$x


# Call up x from tib using double brackets and name this x2

x2 = tib[[1]]

# Are x1 and x2 equal?

x1 == x2
```

*** =sct
```{r}

test_student_typed("tib",not_typed_msg= "Make sure to call tib.")
test_object("x1", incorrect_msg = "Make sure you index x from tib.")
test_student_typed("tib$x",not_typed_msg = "Use the dollar sign to index x from tib.")
test_object("x2", incorrect_msg = "Make sure you index x from tib.")
test_output_contains("TRUE", incorrect_msg = "Make sure you compare x1 to x2.")



```



--- type:VideoExercise lang:r xp:25 skills:1 key:cf760ad48e
## Beginning to work with Large Data in R

*** =video_link

//player.vimeo.com/video/187460874







--- type:VideoExercise lang:r xp:25 skills:1 key:3081c7aabe
## Split, Apply and Combine

*** =video_link

//player.vimeo.com/video/187462579




--- type:MultipleChoiceExercise lang:r xp:75 skills: key:2526ff8b47

## Split, Apply and Combine Exercise 1

Please answer the following question about split, apply and combine:

With split, apply and combine a good way to complete this is to copy and paste code over and over until we complete for all splits. 

*** =instructions

- True
- False




*** =pre_exercise_code
```{r}


```

*** =sct
```{r}

test_mc(correct=2, feedback_msgs = c("Incorrect: Anytime we copy and paste we run the risk of introducing error into oru analysis. ","Correct: Anytime we copy and paste we run the risk of introducing error into oru analysis. " ))

```



--- type:MultipleChoiceExercise lang:r xp:75 skills: key:d8ad3533ca

## Split, Apply and Combine Exercise 2

Please answer the following question about split, apply and combine:

What is not a good reason to do split, apply and combine?

*** =instructions

- The data is naturally grouped and we wish to anaylze the data across groups. 
- The data is large and able to be split in a way that makes sense for our analysis. 
- This method works in all cases. 




*** =pre_exercise_code
```{r}


```

*** =sct
```{r}

test_mc(correct=3, feedback_msgs = c("Incorrect: This is an excellent situation to use the split, apply, and combine method", "Incorrect: If we can split large data and then bring it back together this is a reasonable way to analyze the data.", "Correct: This is not necessarily always a viable option. Many times there is no logical reason to split the data." ))

```






--- type:VideoExercise lang:r xp:25 skills:1 key:eca6dc8dfc
## Split, Apply and Combine with plyr

*** =video_link

//player.vimeo.com/video/187463389






--- type:VideoExercise lang:r xp:25 skills:1 key:3ea9bc221e
## BRFSS with plyr

*** =video_link

//player.vimeo.com/video/187464635





--- type:VideoExercise lang:r xp:25 skills:1 key:15c484f6da
## Further work with Split, Apply and Combine

*** =video_link

//player.vimeo.com/video/187466682





--- type:VideoExercise lang:r xp:25 skills:1 key:f71264a59f
## Beginning with dplyr

*** =video_link

//player.vimeo.com/video/187468101




--- type:VideoExercise lang:r xp:25 skills:1 key:066788f46e
## Chaining and Pipelining with dplyr in R

*** =video_link

//player.vimeo.com/video/187468763




--- type:VideoExercise lang:r xp:25 skills:1 key:cf746ce32e
## Arranging and Mutating Data

*** =video_link

//player.vimeo.com/video/187469410




--- type:VideoExercise lang:r xp:25 skills:1 key:0b83d01480
## Using the summarise verb to summarize Data in R

*** =video_link

//player.vimeo.com/video/187472223




--- type:VideoExercise lang:r xp:25 skills:1 key:0d2dcd61ea
## Choosing Columns and Rows with dplyr

*** =video_link

//player.vimeo.com/video/187473418




--- type:VideoExercise lang:r xp:25 skills:1 key:44e9d99f39
## Adding new variables with dplyr

*** =video_link

//player.vimeo.com/video/187486162




--- type:VideoExercise lang:r xp:25 skills:1 key:9d26f88f31
## Jenny Bryan's Cheatsheet for dpylr joins

*** =video_link

//player.vimeo.com/video/187487417






