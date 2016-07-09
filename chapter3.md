
title       : Characters and Strings in R
description : In this Section we will focus on working with character and string data in R.  
attachments :


--- type:VideoExercise lang:r xp:25 skills:1    key:16d952138c
## Character and String Data in R

*** =video_link

//player.vimeo.com/video/173632704





--- type:VideoExercise lang:r xp:25 skills:1    key:7a592a6f8f
## String Basics in R

*** =video_link

//player.vimeo.com/video/173693951





--- type:NormalExercise lang:r xp:25 skills:1  key:f863fcb9ce
##Strings Basics in R

*** =instructions
There is a vector of strings stored in R. Answer questions about this vector. 


*** =hint

Remember the R commands for learning more about strings. They are stored in a vector called `string_vec`. 




*** =pre_exercise_code
```{r, warning=FALSE, message=FALSE}
string_vec <- readLines("https://drive.google.com/uc?export=download&id=0B8CsRLdwqzbzbWp6X2trZzRfYTA", encoding="UTF-8")
```

*** =sample_code

```{r}
# How many strings are in string_vec?


# How many characters are in each string?


# What are the last 3 characters in each string?


# What are the 56 and 57 characters in each string?

```

*** =solution

```{r}
# How many strings are in string_vec?

length(string_vec)

# How many characters are in each string?
nchar(string_vec)


```

*** =sct
```{r}
test_object("length(string_vec)", incorrect_msg="Go back to the video to see what command tells you string count.")
test_object("nchar(string_vec)", incorrect_msg="Go back to the video to see what command counts characters.")
success_msg("Great!")
```



--- type:VideoExercise lang:r xp:25 skills:1    key:00141dac01
## Substrings in R

*** =video_link

//player.vimeo.com/video/173801171



--- type:NormalExercise lang:r xp:25 skills:1    key:fdee851eec
##Substrings in R Exercise

*** =instructions
There is a vector of strings stored in R. Answer questions about this vector. 


*** =hint

Remember the R commands for learning more about strings. They are stored in a vector called `string_vec`. 




*** =pre_exercise_code
```{r, warning=FALSE, message=FALSE}
string_vec <- readLines("http://drive.google.com/uc?export=download&id=0B8CsRLdwqzbzbWp6X2trZzRfYTA", encoding="UTF-8")
```

*** =sample_code

```{r}
# What is the first character in each string?



# What are the last 3 characters in each string of string_ vec?


# What are the 56 and 57 characters in each string of string_vec?

```

*** =solution

```{r}
# What is the first character in each string  of string_ vec?
substr(string_vec, 1,1)

# What are the last 3 characters in each string of string_ vec?
substr(string_vec, nchar(string_vec)-2, nchar(string_vec))

# What are the 56 and 57 characters in each string of string_ vec?
substr(string_vec, 56,57)

```

*** =sct
```{r}
test_object("substr(string_vec, 1,1)", incorrect_msg="Go back to the video to see how to use the substr() command.")
test_object("substr(string_vec, nchar(string_vec)-2, nchar(string_vec))", incorrect_msg="Make sure to use the substr() command.")
test_object("substr(string_vec, 56,57)", incorrect_msg="Make sure to use the substr() command.")
success_msg("Great!")
```



--- type:VideoExercise lang:r xp:25 skills:1    key:adb0c94697
## Analyzing Larger Amounts of Text in R

*** =video_link

//player.vimeo.com/video/173807748




--- type:NormalExercise lang:r xp:25 skills:1     key:33ce09fc0e
##Analyzing Text from a Blog

*** =instructions
This problem containts a vector of strings called `julia`. Answer these questions with this string and using the tools in the previous video. 


*** =hint

*** =pre_exercise_code
```{r, warning=FALSE, message=FALSE}
julia <- readLines("http://drive.google.com/uc?export=download&id=0B8CsRLdwqzbzNXVqd0pxYmZQcTg")
```

*** =sample_code

```{r}
# How many strings are in julia?



# What are the last 3 characters in each string of string_ vec?


# What are the 56 and 57 characters in each string of string_vec?

```

*** =solution

```{r}
# What is the first character in each string  of string_ vec?
substr(string_vec, 1,1)

# What are the last 3 characters in each string of string_ vec?
substr(string_vec, nchar(string_vec)-2, nchar(string_vec))

# What are the 56 and 57 characters in each string of string_ vec?
substr(string_vec, 56,57)

```

*** =sct
```{r}
test_object("substr(string_vec, 1,1)", incorrect_msg="Go back to the video to see how to use the substr() command.")
test_object("substr(string_vec, nchar(string_vec)-2, nchar(string_vec))", incorrect_msg="Make sure to use the substr() command.")
test_object("substr(string_vec, 56,57)", incorrect_msg="Make sure to use the substr() command.")
success_msg("Great!")
```









--- type:VideoExercise lang:r xp:25 skills:1    key:a92891b2e1
## Regular Expressions in R

*** =video_link

//player.vimeo.com/video/173823132




--- type:VideoExercise lang:r xp:25 skills:1    key:9ea6818506
## Quantifiers and Positions in Strings

*** =video_link

//player.vimeo.com/video/



--- type:VideoExercise lang:r xp:25 skills:1    key:264bf79f24
## Character Classes in R

*** =video_link

//player.vimeo.com/video/


--- type:VideoExercise lang:r xp:25 skills:1    key:16ff5be601
## Extended String Example in R

*** =video_link

//player.vimeo.com/video/
