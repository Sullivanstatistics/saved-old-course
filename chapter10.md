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




--- type:MultipleChoiceExercise lang:r xp:75 skills: key:813400786a

## Split, Apply and Combine Exercise 3

Please answer the following question about split, apply and combine:

With the `plyr` class of functions what is not a type of data that has a specific input. 

*** =instructions

- Vectors
- Lists
- Arrays
- Data Frames




*** =pre_exercise_code
```{r}


```

*** =sct
```{r}

test_mc(correct=1, feedback_msgs = c("Correct: plyr works with arrays, lists and data frames. " , "Incorrect:  plyr works lists. ",  "Incorrect: plyr works with arrays",  "Inccorrect: plyr works with data frames. " ))

```




--- type:MultipleChoiceExercise lang:r xp:75 skills: key:a6c4ed1373

## Split, Apply and Combine Exercise 4

Please answer the following question about split, apply and combine:

With the `plyr` class of functions what is not a type of data that has a specific output

*** =instructions

- Vectors
- Lists
- Arrays
- Data Frames




*** =pre_exercise_code
```{r}


```

*** =sct
```{r}

test_mc(correct=1, feedback_msgs = c("Correct: plyr works with arrays, lists and data frames. " , "Incorrect:  plyr works lists. ",  "Incorrect: plyr works with arrays",  "Inccorrect: plyr works with data frames. " ))

```

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



--- type:NormalExercise lang:r xp:100 skills:1 key:1f5a22e759
## dplyr Exercise 1

We will work with dplyr to analyze date. 

*** =instructions


Work with dplyr functions to explore the flights data. This is a dataset of all flights departing from Houston in 2011.  

*** =hint




*** =pre_exercise_code
```{r}
library(tibble)
library(dplyr)
library(hflights)
flights <- as_tibble(hflights)

```


*** =sample_code

```{r}
# call saved data flights


#Using base R filter flights by the 7th month and 3rd day.  save this as df1



# Using dplyr filter flights by the 7th month and 3rd day.  save this as df2



```

*** =solution

```{r}
# call saved data flights

flights


#Using base R filter flights by the 7th month and 3rd day.  save this as df1

df1 = flights[flights$Month==7 & flights$DayofMonth==3, ]

# Using dplyr filter flights by the 7th month and 3rd day.  save this as df2


df2 = filter(flights, Month==7, DayofMonth==3)
```

*** =sct
```{r}

test_student_typed("flights",not_typed_msg= "Make sure to call flights.")
test_object("df1", incorrect_msg = "Make sure to use the right call for month and day.")
test_student_typed("flights$Month",not_typed_msg = "Make sure to index Month")
test_student_typed("flights$DayofMonth",not_typed_msg = "Make sure to index DayofMonth")
test_object("df2", incorrect_msg = "Make sure to use the right call for month and day.")
test_function("filter", incorrect_msg = "Make sure you use the filter function with dplyr.")
success_msg("Great!")



```





--- type:NormalExercise lang:r xp:100 skills:1 key:b1ef41b537
## dplyr Exercise 2

We will work with dplyr to analyze date. 

*** =instructions

Work with dplyr functions to explore the flights data. This is a dataset of all flights departing from Houston in 2011.  

*** =hint




*** =pre_exercise_code
```{r}
library(tibble)
library(dplyr)
library(hflights)
flights <- as_tibble(hflights)

```


*** =sample_code

```{r}
# call saved data flights

#select departure time, arrival time and the flight number using base R techniques


#select departure time, arrival time and the flight number using dplyr 

```

*** =solution

```{r}
# call saved data flights

flights


#Using base R filter flights by the 7th month and 3rd day.  save this as df1

df1 = flights[, c("DepTime", "ArrTime", "FlightNum") ]

# Using dplyr filter flights by the 7th month and 3rd day.  save this as df2

df2 = select(flights, DepTime, ArrTime, FlightNum)
```

*** =sct
```{r}

test_student_typed("flights",not_typed_msg= "Make sure to call flights.")
test_object("df1", incorrect_msg = "Make sure to use the right call for Arrival Time, Departure Time and Flight number?")
test_student_typed("ArrTime",not_typed_msg = "Make sure to select Arrival Time")
test_student_typed("DepTime",not_typed_msg = "Make sure to select Departure Time")
test_student_typed("FlightNum",not_typed_msg = "Make sure to select flight number")
test_object("df2", incorrect_msg = "Make sure to use the right call for Arrival Time, Departure Time and Flight number?")
test_function("select", incorrect_msg = "Make sure you use the filter function with dplyr.")
success_msg("Great!")

```


--- type:VideoExercise lang:r xp:25 skills:1 key:066788f46e
## Chaining and Pipelining with dplyr in R

*** =video_link

//player.vimeo.com/video/187468763






--- type:NormalExercise lang:r xp:100 skills:1 key:e4736b7f66
## Chaining and Pipelining Exercise 1

We will complete the previous tasks using chaining and pipelining. 

*** =instructions


Work with dplyr functions to explore the flights data. This is a dataset of all flights departing from Houston in 2011.  

*** =hint




*** =pre_exercise_code
```{r}
library(tibble)
library(dplyr)
library(hflights)
flights <- as_tibble(hflights)

```


*** =sample_code

```{r}
# call saved data flights


# Using dplyr filter flights by the 7th month and 3rd day.  Use %>% commands to do this. 



```

*** =solution

```{r}
# call saved data flights


# Using dplyr filter flights by the 7th month and 3rd day.  Use %>% commands to do this. call this df1


df1 = flights %>% 
      filter(Month==7, DayofMonth==3)
```

*** =sct
```{r}

test_student_typed("flights",not_typed_msg= "Make sure to call flights.")
test_object("df1", incorrect_msg = "Did you use the corret month and day?")
test_student_typed("%>%",not_typed_msg= "Make sure to use piping")
test_function("filter", incorrect_msg = "Make sure you use the filter function with dplyr.")
success_msg("Great!")



```





--- type:NormalExercise lang:r xp:100 skills:1 key:6baaefb441
## Chaining and Pipelining Exercise 2

We will work with dplyr to analyze date. 

*** =instructions

Work with dplyr functions to explore the flights data. This is a dataset of all flights departing from Houston in 2011.  

*** =hint




*** =pre_exercise_code
```{r}
library(tibble)
library(dplyr)
library(hflights)
flights <- as_tibble(hflights)

```


*** =sample_code

```{r}
# call saved data flights


#select departure time, arrival time and the flight number using dplyr and %>% name this df1.


```

*** =solution

```{r}
# call saved data flights

flights


#select departure time, arrival time and the flight number using dplyr and %>% name this df1.

df1 = flights %>%
          select(ArrTime, DepTime, FlightNum)

```

*** =sct
```{r}


test_student_typed("flights",not_typed_msg= "Make sure to call flights.")
test_object("df1", incorrect_msg = "Did you select the correct columns?")
test_student_typed("%>%",not_typed_msg= "Make sure to use piping")
test_function("select", incorrect_msg = "Make sure you use the select function with dplyr.")
success_msg("Great!")


```





--- type:NormalExercise lang:r xp:100 skills:1 key:085f0bc093
## Chaining and Pipelining Exercise 3

We will work with dplyr to analyze date. 

*** =instructions

Work with dplyr functions to explore the flights data. This is a dataset of all flights departing from Houston in 2011.  

*** =hint




*** =pre_exercise_code
```{r}
library(tibble)
library(dplyr)
library(hflights)
flights <- as_tibble(hflights)

```


*** =sample_code

```{r}
# call saved data flights


#select departure time, arrival time and the flight number using dplyr where departure time is greater than 700 and %>% name this df1. 



```

*** =solution

```{r}
# call saved data flights

flights

#select departure time, arrival time and the flight number using dplyr where departure time is greater than 700 and %>% name this df1. 



df1 = flights %>%
            select(ArrTime, DepTime, FlightNum) %>%
            filter(DepTime > 700)

```

*** =sct
```{r}


test_student_typed("flights",not_typed_msg= "Make sure to call flights.")
test_object("df1", incorrect_msg = "Did you select the correct columns?")
test_student_typed("%>%",not_typed_msg= "Make sure to use piping")
test_function("select", incorrect_msg = "Make sure you use the select function with dplyr.")
test_function("filter", incorrect_msg = "Make sure you use the select function with dplyr.")
test_student_typed("700", not_typed_msg = "Make sure you filter with departures greater than 700.")
success_msg("Great!")


```



--- type:VideoExercise lang:r xp:25 skills:1 key:cf746ce32e
## Arranging and Mutating Data

*** =video_link

//player.vimeo.com/video/187469410


--- type:NormalExercise lang:r xp:100 skills:1 key:23dd6c039a
## Arranging and Mutating Exercise 1

We will work with dplyr to analyze date. 

*** =instructions

Work with dplyr functions to explore the flights data. This is a dataset of all flights departing from Houston in 2011.  

*** =hint




*** =pre_exercise_code
```{r}
library(tibble)
library(dplyr)
library(hflights)
flights <- as_tibble(hflights)

```


*** =sample_code

```{r}
# call saved data flights


#select distance and air time
# Then calculate speec as distance divided by air time multiplied by 60
# Then arrange by speed
# name this df1



```

*** =solution

```{r}
# call saved data flights

flights

# call saved data flights


#select distance and air time
# Then calculate speec as distance divided by air time multiplied by 60
# Then arrange by speed
#name this df1

df1 = flights %>%
    select(Distance, AirTime) %>%
    mutate(Speed = Distance/AirTime*60) %>%
    arrange(Speed)


```

*** =sct
```{r}


test_student_typed("flights",not_typed_msg= "Make sure to call flights.")
test_object("df1", incorrect_msg = "Did you select the correct columns?")
test_student_typed("%>%",not_typed_msg= "Make sure to use piping")
test_function("select", incorrect_msg = "Make sure you use the select function with dplyr.")
test_student_typed("%>%",not_typed_msg= "Make sure to use piping")
test_function("mutate", incorrect_msg = "Make sure you use the mutate function with dplyr.")
test_student_typed("%>%",not_typed_msg= "Make sure to use piping")
test_function("arrange", incorrect_msg = "Make sure you use the arrange function with dplyr.")
success_msg("Great!")


```



--- type:NormalExercise lang:r xp:100 skills:1 key:d1ef4e76e6
## Arranging and Mutating Exercise 2

We will work with dplyr to analyze date. 

*** =instructions

Work with dplyr functions to explore the flights data. This is a dataset of all flights departing from Houston in 2011.  

*** =hint




*** =pre_exercise_code
```{r}
library(tibble)
library(dplyr)
library(hflights)
flights <- as_tibble(hflights)

```


*** =sample_code

```{r}
# call saved data flights


#select distance and air time
# Then calculate speec as distance divided by air time multiplied by 60
# Then arrange by descending speed
# name this df1



```

*** =solution

```{r}
# call saved data flights

flights

# call saved data flights


#select distance and air time
# Then calculate speec as distance divided by air time multiplied by 60
# Then arrange by descending speed
# name this df1

df1= flights %>%
    select(Distance, AirTime) %>%
    mutate(Speed = Distance/AirTime*60) %>%
    arrange(desc(Speed))


```

*** =sct
```{r}


test_student_typed("flights",not_typed_msg= "Make sure to call flights.")
test_object("df1", incorrect_msg = "Did you select the correct columns?")
test_student_typed("%>%",not_typed_msg= "Make sure to use piping")
test_function("select", incorrect_msg = "Make sure you use the select function with dplyr.")
test_student_typed("%>%",not_typed_msg= "Make sure to use piping")
test_function("mutate", incorrect_msg = "Make sure you use the mutate function with dplyr.")
test_student_typed("%>%",not_typed_msg= "Make sure to use piping")
test_function("arrange", incorrect_msg = "Make sure you use the arrange function with dplyr.")
test_function("desc", incorrect_msg = "Make sure you use the desc function with dplyr.")
success_msg("Great!")


```


--- type:VideoExercise lang:r xp:25 skills:1 key:0b83d01480
## Using the summarise verb to summarize Data in R

*** =video_link

//player.vimeo.com/video/187472223





--- type:NormalExercise lang:r xp:100 skills:1 key:882ce33b21
##  Summrise verb Exercise 1

We will work with dplyr to analyze date. 

*** =instructions

Work with dplyr functions to explore the flights data. This is a dataset of all flights departing from Houston in 2011.  

*** =hint




*** =pre_exercise_code
```{r}
library(tibble)
library(dplyr)
library(hflights)
flights <- as_tibble(hflights)

```


*** =sample_code

```{r}
# call saved data flights


# Count the flights by month
# weight this by distance
# Name the dataframe    df1
# Name the flight count to be flight_count


```

*** =solution

```{r}
# call saved data flights

flights


# Count the flights by month
# weight this by distance
# Name the dataframe    df1
# Name the flight count to be flight_count

df1 = flights %>%
  group_by(Month) %>%
  summarise(flight_count = n())


```

*** =sct
```{r}


test_student_typed("flights",not_typed_msg= "Make sure to call flights.")
test_object("df1", incorrect_msg = "Did you select the correct columns or did you name the count to be flight_count?")
test_student_typed("%>%",not_typed_msg= "Make sure to use piping")
test_function("group_by", incorrect_msg="Did you use the group by function?")
test_student_typed("%>%",not_typed_msg= "Make sure to use piping")
test_function("summarise", incorrect_msg="Did you use the summarise function?")
success_msg("Great!")


```



--- type:NormalExercise lang:r xp:100 skills:1 key:3d4d68fe4f
##  Summrise verb Exercise 2

We will work with dplyr to analyze date. 

*** =instructions

Work with dplyr functions to explore the flights data. This is a dataset of all flights departing from Houston in 2011.  

*** =hint




*** =pre_exercise_code
```{r}
library(tibble)
library(dplyr)
library(hflights)
flights <- as_tibble(hflights)

```


*** =sample_code

```{r}
# call saved data flights


# Group flights by month
# tally this
# weight this by average distance (Using wt option in tally() ) 
# Name this df1


```

*** =solution

```{r}
# call saved data flights

flights


# Group flights by month
# tally this
# weight this by distance
# Name this df1

df1 = flights %>%
        group_by(Month) %>%
        tally( wt = mean(Distance))


```

*** =sct
```{r}


test_student_typed("flights",not_typed_msg= "Make sure to call flights.")
test_object("df1", incorrect_msg = "Did you select the correct columns?")
test_student_typed("%>%",not_typed_msg= "Make sure to use piping")
test_function("group_by", incorrect_msg="Did you use the group_by() function?")
test_student_typed("%>%",not_typed_msg= "Make sure to use piping")
test_function("tally", incorrect_msg="Did you use the tally() function?")
test_student_typed("wt", not_typed_msg="Did you remember to weight this?")
success_msg("Great!")


```


--- type:VideoExercise lang:r xp:25 skills:1 key:0d2dcd61ea
## Choosing Columns and Rows with dplyr

*** =video_link

//player.vimeo.com/video/187473418








--- type:VideoExercise lang:r xp:25 skills:1 key:44e9d99f39
## Adding new variables with dplyr

*** =video_link

//player.vimeo.com/video/187486162




--- type:VideoExercise lang:r xp:25 skills:1 key:9d26f88f31
## Jenny Bryan's Cheatsheet for dplyr joins

*** =video_link

//player.vimeo.com/video/187487417


--- type:NormalExercise lang:r xp:100 skills:1 key:16f9bc9aa4
##  Joins 1

We will practice the difficult concept of joins.  

*** =instructions

Two data frames `a` and `b` have been stored. We will practice joins on them. 

*** =hint




*** =pre_exercise_code
```{r}
library(dplyr)
(a <- data_frame(color = c("green","yellow","red"), num = 1:3))
(b <- data_frame(color = c("green","yellow","pink"), size = c("S","M","L")))

```


*** =sample_code

```{r}
# Print out a


# Print out b


```

*** =solution

```{r}
# Print out a

print(a)


# Print out b

print(b)
```

*** =sct
```{r}


test_function("print", incorrect_msg="Did you use the print function to print a?")
test_function("print", incorrect_msg="Did you use the print function to print b?")
success_msg("Great")


```





--- type:NormalExercise lang:r xp:100 skills:1 key:de483734fd
##  Joins 2

We will practice the difficult concept of joins.  

*** =instructions

Two data frames `a` and `b` have been stored. We will practice joins on them. 

*** =hint




*** =pre_exercise_code
```{r}
library(dplyr)
(a <- data_frame(color = c("green","yellow","red"), num = 1:3))
(b <- data_frame(color = c("green","yellow","pink"), size = c("S","M","L")))

```


*** =sample_code

```{r}

# inner join a and b


# full join a and b


```

*** =solution

```{r}
# inner join a and b

inner_join(a,b)

# full join a and b
full_join(a,b)

```

*** =sct
```{r}


test_function("inner_join", incorrect_msg="Did you use the inner_join function?")
test_function("full_join", incorrect_msg="Did you use the full_join function?")
success_msg("Great")


```


--- type:NormalExercise lang:r xp:100 skills:1 key:027cb37cd9
##  Joins 3

We will practice the difficult concept of joins.  

*** =instructions

Two data frames `a` and `b` have been stored. We will practice joins on them. 

*** =hint




*** =pre_exercise_code
```{r}
library(dplyr)
(a <- data_frame(color = c("green","yellow","red"), num = 1:3))
(b <- data_frame(color = c("green","yellow","pink"), size = c("S","M","L")))

```


*** =sample_code

```{r}

# left join a and b


# right join a and b


```

*** =solution

```{r}
# left join a and b

left_join(a,b)

# right join a and b
right_join(a,b)

```

*** =sct
```{r}


test_function("left_join", incorrect_msg="Did you use the left_join function?")
test_function("right_join", incorrect_msg="Did you use the right_join function?")
success_msg("Great")


```



