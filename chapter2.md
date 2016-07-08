---
title       : Basics of Julia Programming
description : In this Section we will begin to explore Julia and learn how it handles data. We will focus on major data types that we use frequently in statistics and the basics of how we use them. As we move forward these data types will be key to analyzing statistics.  
attachments :


--- type:VideoExercise lang:r xp:25 skills:1    key:8164d3d037
## Getting Start in Julia

*** =video_link

//player.vimeo.com/video/173632704



--- type:NormalExercise lang:r xp:25 skills:1   key:d4bdee1c7f
##Practicing Basic Julia

*** =instructions

This course site is only equipped to handle either R or Python, because of this you will need to run the code for all Julia exercises on your own computer and copy the answers into R as a comment. 

Copy the following Julia output as a comment:

```
julia> 5+5
10
```



*** =hint

Here is a hint: Remember to use # for comments

*** =sample_code

```{r}
# Copy the code in as a comment




```

*** =solution

```{r}
# Copy the code in as a comment
#julia> 5+5
#10
```

*** =sct
```{r}
test_student_typed("#julia> 5+5", not_typed_msg =  "Make sure there is no space between the # and julia")
test_student_typed("#10", not_typed_msg = "Make sure there is no space between the # and 10")
success_msg("Great!")
```






--- type:VideoExercise lang:r xp:25 skills:1    key:b29f203e7b
## Simple Procedures in Julia

*** =video_link

//player.vimeo.com/video/173640734



--- type:VideoExercise lang:r xp:25 skills:1    key:3ff42236f6
## Getting Help in Julia

*** =video_link

//player.vimeo.com/video/173643609



--- type:VideoExercise lang:r xp:25 skills:1    key:c4dd2f996d
## Data Objects in Julia

*** =video_link

//player.vimeo.com/video/173648225



--- type:NormalExercise lang:r xp:25 skills:1    key:a87eb5e29d
##Practicing Basic Data Objects in Julia

*** =instructions

This course site is only equipped to handle either R or Python, because of this you will need to run the code for all Julia exercises on your own computer and copy the answers into R as a comment. 

In this question we will explore what $2^4350$ is. 

*** =hint

Here is a hint: Remember to use # for comments

*** =sample_code

```{r}
# Define x to be 2^50



# Calculate what exponent is needed to evaluate 2^4350 using x. 



# What is 2^4350?





```

*** =solution

```{r}
# Define x to be x^50

# julia> x = BigInt(2^50)
# 1125899906842624


# Calculate what exponent is needed to evaluate 2^4350 using x. 
# julia> 4350/50
# 87.0


# What is 2^4350?

# julia> x^87
# 302329926387631491762682321300950422637040652746489596080755218462507481840988720148672142490037623037741533619021676516308782906696 655830582538599405641767288978710205407921377254395022051040495722935620061709127927885606820904892503159455591998229488470428744083# 03327521364009519737780511534049894828514038745879437379948448477988494391419677651837818291171715385319537740779666738612841452661134821303142175708166764481916771360808797324939228382260001991301986925700641989008112484618117429798080761782454099379339958495096692184448194386710912004906632389015085770941757025428748001903510847583005213914666176028083874131610171770928601382134291916955028972636476858606716617996917352031775236035228360454064923052326530508657239807932786563202110398126417870975808323894167539772588013737909019299717188295414304986943373576117880755582779004309786352302659303539325027976520603040877743789984819708783508980072110275715412965062026196249436095338212811327281296197152773834385278584232523687569154448212669055810949023811092899969095773472560540128934564535709337945237630304009451673265635237564018442126096709714255254307792872725257227564442205862449923419468540524399522192103979391055776122897276898904263625823416760353061725269376220497335573832641105473416095428750598499632653965813050322714624


```

*** =sct
```{r}
test_student_typed("julia> x = BigInt(2^50)", not_typed_msg =  "Make sure you use BigInt()")
test_student_typed("4350/50", not_typed_msg = "You need to divide 4350 by 50")
test_student_typed("julia> x^87", not_typed_msg = "You need to raise x to a different exponent.")
success_msg("Great!")
```




--- type:VideoExercise lang:r xp:25 skills:1    key:b62fd8174d
## Arrays in Julia

*** =video_link

//player.vimeo.com/video/173651431





--- type:NormalExercise lang:r xp:25 skills:1     key:5f3b5ac010
##Practicing Arrays in Julia 1

*** =instructions

This course site is only equipped to handle either R or Python, because of this you will need to run the code for all Julia exercises on your own computer and copy the answers into R as a comment. 

In this exercise we will focus on arrays in Julia. 

*** =hint

Here is a hint: Remember to use # for comments

*** =sample_code

```{r}
# Define a = [ 1, 2, 3, 4]



# redefine a without using commas



# Add a semi-colon in your above definition of a to make it a 2x2 matrix.





```

*** =solution

```{r}
# Define a = [ 1, 2, 3, 4]

#julia> a = [1,2,3,4]
#4-element Array{Int64,1}:
# 1
# 2
# 3
# 4

# redefine a without using commas

# julia> a = [1 2 3 4 ]
# 1x4 Array{Int64,2}:
# 1  2  3  4


# Add a semi-colon in your above definition of a to make it a 2x2 matrix.

# julia> a = [1 2; 3 4]
# 2x2 Array{Int64,2}:
# 1  2
# 3  4

```

*** =sct
```{r}
test_student_typed("#1", not_typed_msg =  "Make sure to copy the julia output.")
test_student_typed("#2", not_typed_msg =  "Make sure to copy the julia output.")
test_student_typed("#3", not_typed_msg =  "Make sure to copy the julia output.")
test_student_typed("#4", not_typed_msg =  "Make sure to copy the julia output.")
test_student_typed("# 1 2 3 4", not_typed_msg = "Make sure to define without commas")
test_student_typed(" julia> a = [1 2; 3 4]", not_typed_msg = "Make sure the semi-colon is in the correct spot.")
success_msg("Great!")
```




--- type:VideoExercise lang:r xp:25 skills:1    key:22254b93ba
## Working with Arrays in Julia

*** =video_link

//player.vimeo.com/video/173668768


