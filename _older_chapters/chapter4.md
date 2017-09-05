---
title       : Strings in Julia
description : In this chapter we will explore how Julia handles string data. 


--- type:VideoExercise lang:r xp:25 skills:1 key:5192ce09ed
## Strings in Julia


*** =video_link
//player.vimeo.com/video/182220427



--- type:NormalExercise lang:r xp:100 skills:1    key:a87eb5e29d
## Practicing Basic Strings in Julia

*** =instructions

This course site is only equipped to handle either R or Python, because of this you will need to run the code for all Julia exercises on your own computer and copy the answers into R as a comment. 



*** =hint

Here is a hint: Remember to use # for comments

*** =sample_code

```{r}
# What is the 253 Char?




```

*** =solution

```{r}
# What is the 253 Char?
#julia> Char(253)
#'ý'
```

*** =sct
```{r}
test_student_typed("Char(253)", not_typed_msg =  "Make sure you use Char()")
success_msg("Great!")
```


--- type:VideoExercise lang:r xp:25 skills:1 key:6801370b95
## Substrings in Julia



*** =video_link
//player.vimeo.com/video/182221297









--- type:VideoExercise lang:r xp:25 skills:1 key:2de5e65711
## Working with Strings in Julia


*** =video_link
//player.vimeo.com/video/182223119





--- type:NormalExercise lang:r xp:100 skills:1    key:00594f3380
## Practicing Substrings in Julia

*** =instructions

This course site is only equipped to handle either R or Python, because of this you will need to run the code for all Julia exercises on your own computer and copy the answers into R as a comment. 


Copy this string into Julia to begin:

string = "This is the best Statistical Computing Class I have taken!"


*** =hint

Here is a hint: Remember to use # for comments

*** =sample_code

```{r}
# Paste what happens when you try to concatenate 'a' and 'b' using and *



# What are the words with the indexing of 8:16?



# Compare string[1] to string[1:1] are these exactly equal? Do this in one line and paste the answer.







```

*** =solution

```{r}
# Paste what happens when you try to concatenate 'a' and 'b' using and *

#julia> 'a' * 'b'
#ERROR: MethodError: `*` has no method matching *(::Char, ::Char)
#Closest candidates are:
#  *(::Any, ::Any, ::Any, ::Any...)

# What are the words with the indexing of 8:16?
#julia> string[8:16]
#" the best"



# Compare string[1] to string[1:1] are these exactly equal? Do this in one line and paste the answer.
#julia> string[1] == string[1:1]
#false

```

*** =sct
```{r}
test_student_typed("'a'")
test_student_typed("'b'")
test_student_typed("ERROR: MethodError: `*` has no method matching *(::Char, ::Char)")
test_student_typed("string[8:16]", not_typed_msg= " Did you index properly")
test_student_typed("the best", not_typed_msg = "Did you copy the string properly?")
test_student_typed("string[1] == string[1:1]", not_typed_msg = "Did you logically compare them using ==")
test_student_typed("false")
success_msg("Great!")
```





--- type:VideoExercise lang:r xp:25 skills:1 key:4212816bed
## Regular Expressions in Julia


*** =video_link
//player.vimeo.com/video/182227544






--- type:NormalExercise lang:r xp:100 skills:1    key:ce67f9b4e3
## Practicing Regular Expressions in Julia

*** =instructions

This course site is only equipped to handle either R or Python, because of this you will need to run the code for all Julia exercises on your own computer and copy the answers into R as a comment. 


Copy this string into Julia to begin:

string = "This is the best Statistical Computing Class I have taken!"


*** =hint

Here is a hint: Remember to use # for comments

*** =sample_code

```{r}
# Search for all vowels. 


# Index the above search to show the vowel.


# Match all vowels in string. 


# Replace the word best with first.









```

*** =solution

```{r}
# Search for all vowels. 
#julia> search(string, r"a|e|i|o|u")
#3:3


# Index the above search to show the vowel.
#julia> string[search(string, r"a|e|i|o|u")]
#"i"

# Match all vowels in string. 
#julia> matchall(r"a|e|i|o|u", string)
#16-element Array{SubString{UTF8String},1}:
# "i"
# "i"
# "e"
# "e"
# "a"
# "i"
# "i"
# "a"
# "o"
# "u"
# "i"
# "a"
# "a"
# "e"
# "a"
# "e"

# Replace the word best with first.
#julia> replace(string, "best", "first")
#"This is the first Statistical Computing Class I have taken!"

```

*** =sct
```{r}
test_student_typed("search(string, r", not_typed_msg = "Make sure you use the search function with a real expression")
test_student_typed("3:3")
test_student_typed("i", not_typed_msg="Did you search for the first one and then index?")
test_student_typed("matchall(r", not_typed_msg= " Make sure to use the matchall() function.")
test_student_typed("replace(string, ", not_typed_msg = "Did you use the replace() function?")
test_student_typed("This is the first Statistical Computing Class I have taken!")
success_msg("Great!")
```





--- type:VideoExercise lang:r xp:25 skills:1 key:f038199a67
## Text Files in Julia


*** =video_link
//player.vimeo.com/video/182234071
