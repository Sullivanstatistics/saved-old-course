---
title       : Characters and Strings in R
description : In this Section we will focus on working with character and string data in R.  
attachments :


--- type:VideoExercise lang:r xp:25 skills:1    key:16d952138c
## Character and String Data in R

*** =video_link

//player.vimeo.com/video/173671485





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
string_vec <- readLines("http://s3.amazonaws.com/assets.datacamp.com/production/course_1118/datasets/gettysburg.txt")
```

*** =sample_code

```{r}
# How many strings are in string_vec?


# How many characters are in each string?



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
test_function("length")
test_function("nchar")
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
string_vec <- readLines("http://s3.amazonaws.com/assets.datacamp.com/production/course_1118/datasets/julia.txt")
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
test_output_contains("substr(string_vec, 1,1)", incorrect_msg="Go back to the video to see how to use the substr() command.")
test_output_contains("substr(string_vec, nchar(string_vec)-2, nchar(string_vec))", incorrect_msg="Go back to the video to see how to use the substr() command.")
test_output_contains("substr(string_vec, 56,57)", incorrect_msg="Go back to the video to see how to use the substr() command.")
success_msg("Great!")
```



--- type:VideoExercise lang:r xp:25 skills:1    key:adb0c94697
## Analyzing Larger Amounts of Text in R

*** =video_link

//player.vimeo.com/video/173807748




--- type:NormalExercise lang:r xp:25 skills:1 key:bd6a38c579
##Analyzing Text from a Blog

*** =instructions
This problem containts a vector of strings called `julia`. Answer these questions with this string and using the tools in the previous video. 


*** =hint

*** =pre_exercise_code
```{r, warning=FALSE, message=FALSE}
julia <- readLines("http://s3.amazonaws.com/assets.datacamp.com/production/course_1118/datasets/julia.txt")
```

*** =sample_code

```{r}
# How many strings are in julia?



# Make julia one long string. 



# Split julia into individual words. 

```

*** =solution

```{r}
# How many strings are in julia?
length(julia)


# Make julia one long string. 
julia <- paste(julia, collapse=" ")

# Split julia into individual words. 
julia <- strsplit(julia, split=" ")[[1]]
```

*** =sct
```{r}
test_function("length")
test_function("paste")
test_object("julia")
success_msg("Great!")
```









--- type:VideoExercise lang:r xp:25 skills:1    key:a92891b2e1
## Regular Expressions in R

*** =video_link

//player.vimeo.com/video/173823132



--- type:NormalExercise lang:r xp:25 skills:1 key:33fe23b9de
##Regular Expressions in the blog Data

*** =instructions
This problem containts a vector of strings called `julia`. Answer these questions with this string and using the tools in the previous video. 


*** =hint

*** =pre_exercise_code
```{r, warning=FALSE, message=FALSE}
julia <- readLines("http://s3.amazonaws.com/assets.datacamp.com/production/course_1118/datasets/julia.txt")
julia <- paste(julia, collapse=" ")
```

*** =sample_code

```{r}
# How many strings are in julia?



# Make julia one long string. 



# Split julia into individual words. 

```

*** =solution

```{r}
# How many strings are in julia?
length(julia)


# Make julia one long string. 
julia <- paste(julia, collapse=" ")

# Split julia into individual words. 
julia <- strsplit(julia, split=" ")[[1]]
```

*** =sct
```{r}
test_function("length")
test_function("paste")
test_object("julia")
success_msg("Great!")
```



--- type:VideoExercise lang:r xp:25 skills:1    key:9ea6818506
## Quantifiers and Positions in Strings

*** =video_link

//player.vimeo.com/video/181938733



--- type:VideoExercise lang:r xp:25 skills:1    key:264bf79f24
## Character Classes in R

*** =video_link

//player.vimeo.com/video/181959434


--- type:VideoExercise lang:r xp:25 skills:1    key:16ff5be601
## Extended String Example in R

*** =video_link

//player.vimeo.com/video/
