---
title       : Basics of R Programming
description : In this Section we will begin to explore R and learn how it handles data. We will focus on major data types that we use frequently in statistics and the basics of how we use them. As we move forward these data types will be key to analyzing statistics.  
attachments :


--- type:VideoExercise lang:r xp:25 skills:1   key:1ee3f6290a
## Getting Start in R

*** =video_link

//player.vimeo.com/video/168224745





--- type:NormalExercise lang:r xp:25 skills:1 key:e412be26b2
##Practicing Basic R

*** =instructions
You can run R code with this. Place the solution under the commented section and hit run.

*** =hint

Here is a hint: use `<-` for assignment

*** =sample_code

```{r}
# Create a variable a, equal to 5


# Square a

```

*** =solution

```{r}
# Create a variable a, equal to 5
a <- 5

# Square a
a^2
```

*** =sct
```{r}
test_object("a")
test_output_contains("25", incorrect_msg = "Make sure to print `a`")
success_msg("Great!")
```
