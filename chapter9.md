---
title       : Simulations
description : In this chapter we will cover statistical simulations. 


--- type:VideoExercise lang:r xp:25 skills:1 key:b330fb454f
## Random Variables

*** =video_link

//player.vimeo.com/video/185149327




--- type:VideoExercise lang:r xp:25 skills:1 key:6faff5dbf6
## Discrete Random Variables

*** =video_link

//player.vimeo.com/video/185151455





--- type:NormalExercise lang:r xp:100 skills:1 key:e412be26b2
## Generating Discrete Distributions


We will start by generating data from discrete distributions. 

*** =instructions

Your goal will be to use the discrete distribution functions in R. (A seed ahs been set do not set one)

- Generate 100 random Poisson random variables with $\lambda = 0.2$, name this `x1`. 
- Generate 1000 random Poisson random variables with $\lambda=0.2$ name this `x2`. 
- What is the difference in means of `x1` and `x2` name this `diff_means`.
- Print `diff_means`.


*** =hint

Remember the parts of the function. This is very similar to one created during the video.


*** =pre_exercise_code
```{r}



```


*** =sample_code

```{r}
set.seed(1234)
# Generate 100 random Poisson random variables with lambda = 0.2
x1 = 

# Generate 1000 random Poisson random variables with lambda = 0.2
x2= 


# Find the difference in means
diff_means


# print diff_means


```

*** =solution

```{r}
set.seed(1234)
# Generate 100 random Poisson random variables with lambda = 0.2
x1 = rpois(100, 0.2)

# Generate 100 random Poisson random variables with lambda = 0.5
x2 = rpois(1000, 0.2)


# Find the difference in means
diff_means = mean(x1) - mean(x2)


# print diff_means

print(diff_means)
```

*** =sct
```{r}
test_object("x1", incorrect_msg="Make sure you drew 100 samples using rpois().")
test_function("rpois", incorrect_msg="Make sure you drew 100 samples using rpois().")
test_object("x2", incorrect_msg="Make sure you drew 1000 samples using rpois().")
test_function("rpois", incorrect_msg="Make sure you drew 1000 samples using rpois().")
test_object("diff_means", incorrect_msg="Make sure to take the difference in means.")
test_function("mean", incorrect_msg="Did you use the mean function?")
test_function("print", incorrect_msg="Did you print the difference in means?")
success_msg("Great!")
```




--- type:VideoExercise lang:r xp:25 skills:1 key:4da94c8c0e
## Continuous Random Variables

*** =video_link

//player.vimeo.com/video/185152755






--- type:NormalExercise lang:r xp:100 skills:1 key:ef4e3ece30
## Generating Continuous Distributions


We will start by generating data from continuous distributions. 

*** =instructions

Your goal will be to use the continuous distribution functions in R. (A seed ahs been set do not set one)

- Generate 100 random Normal(0,1) values name this `x1`. 
- Generate 10000 Gamma(2,2) name this `x2`. 
- Generate 1000 Beta(0.2, 0.2) name this `x3`.
- Generate histograms of `x1`, `x2`, and `x3`


*** =hint

Remember the parts of the function. This is very similar to one created during the video.


*** =pre_exercise_code
```{r}

set.seed(1234)
par(mfrow=c(1,3))

```


*** =sample_code

```{r}
# Generate 100 N(0,1) values.
x1 = 

# Generate 10000 Gamma(2,2) values.
x2= 


# Generate 1000 Beta(0.2,0.2) values.

x3=

# generate histograms of the 3 variables

```

*** =solution

```{r}
# Generate 100 N(0,1) values.
x1 = rnorm(100,0,1)

# Generate 10000 Gamma(2,2) values.
x2= rgamma(10000, 2,2)


# Generate 1000 Beta(0.2,0.2) values.

x3= rbeta(1000,0.2,0.2)

# generate histograms of the 3 variables
hist(x1)
hist(x2)
hist(x3)
```

*** =sct
```{r}
test_object("x1", incorrect_msg="Make sure you drew 100 samples using rnorm().")
test_function("rnorm", incorrect_msg="Make sure you drew 100 samples using rnorm().")
test_object("x2", incorrect_msg="Make sure you drew 10000 samples using rgamma().")
test_function("rgamma", incorrect_msg="Make sure you drew 10000 samples using rgamma().")
test_object("x3", incorrect_msg="Make sure you drew 1000 samples using rbeta().")
test_function("rbeta", incorrect_msg="Make sure you drew 1000 samples using rbeta().")
test_function("hist", incorrect_msg="Did you make the histograms?")
success_msg("Great!")
```




--- type:VideoExercise lang:r xp:25 skills:1 key:a24a8c8a04
## Basics of Simulations

*** =video_link

//player.vimeo.com/video/185153204


--- type:VideoExercise lang:r xp:25 skills:1 key:cb6c69d7e0
## Basics of Simulations Continued

*** =video_link

//player.vimeo.com/video/185153636




--- type:NormalExercise lang:r xp:100 skills:1 key:b5ee583fab
## Using the function replicates


We will begin working with the function `replicates()` in R. This function allows us to replicate an action over a specified abount of times. 

*** =instructions

The code below replicates the calculation of mean on a random sample of normals:

```
replicate(3 , rnorm(100,0,2))
```

- Change this so it replicates it 10 times and name this `x`.
- Print `x`.

*** =hint

Remember the parts of the function. This is very similar to one created during the video.


*** =pre_exercise_code
```{r}

set.seed(1234)


```


*** =sample_code

```{r}
# Replicate the mean calculation 10 times.





#Print x
```

*** =solution

```{r}
# Replicate the mean calculation 10 times.
 x= replicate(10 , rnorm(100,0,2))
 
 
 #Print x
 print(x)

```

*** =sct
```{r}
test_object("x", incorrect_msg="Make sure you replicated 10 times. Do not set a seed for this. ")
test_function("replicate", incorrect_msg="Did you use the replicate function?")
test_function("print", incorrect_msg="Did you remember to print?")
success_msg("Great!")
```












--- type:NormalExercise lang:r xp:100 skills:1 key:757c64a18c
## Further Functions for Analysis I


We need to build functions that allow us to start to simulate these things on an easier scale. 


*** =instructions

The next exercises will modify this code. Start with a basic function and follow all the steps. 

- Create a function with argument `n`.
- This function will create a histogram of `n` replicates of:
```
mean(rnorm(100,0,2))
```
- Evaluate `rep_hist` with `n=25`.
- call it with just the number and not with `n=`


*** =hint

Remember the parts of the function. This is very similar to one created during the video.


*** =pre_exercise_code
```{r}

set.seed(1234)


```


*** =sample_code

```{r}
# Create the function and name it rep_hist


#Evaluate when n=25


```

*** =solution

```{r}
# Replicate the mean calculation 10 times.
rep_hist <- function(n){
        hist(replicate(n, mean(rnorm(100,0,2))))
        }

#Evaluate when n=25
rep_hist(25)

```

*** =sct
```{r}
test_function_definition("rep_hist",
                              body_test = test_function("hist", incorrect_msg="Did you call the hist function?"))
test_student_typed("rep_hist(25)", not_typed_msg="Did you remember to call this with n=25? Make sure to call it with (25).")
success_msg("Great!")
```




--- type:NormalExercise lang:r xp:100 skills:1 key:6d5031d908
## Further Functions for Analysis II


We will continue working with our function from the previous problem. 


*** =instructions

Start with the function you had before and modify it in the following way:

- Modify the function so that you can create the histogram of repliccates of 
```
mean(rnorm(N, 0,2))
```
- Set the default value of `N` to be 100.

- call this function with N=90, n=25. 
- call this function with n=25 only. 
- Do not use `N=` or `n=` in the calls. Also put no spaces in the calls. 
*** =hint

Remember the parts of the function. This is very similar to one created during the video.


*** =pre_exercise_code
```{r}

set.seed(1234)


```


*** =sample_code

```{r}
# Create the function and name it rep_hist


#Evaluate when N=90 and n=25


#Evaluate when n=25


```

*** =solution

```{r}
# Replicate the mean calculation 10 times.
rep_hist <- function(n, N=100){
        hist(replicate(n, mean(rnorm(N,0,2))))
        }

#Evaluate when N=90 and n=25
rep_hist(25,90)


#Evaluate when n=25
rep_hist(25)

```

*** =sct
```{r}
test_function_definition("rep_hist",
                              body_test = test_function("hist", incorrect_msg="Did you call the hist function?"))
test_student_typed("rep_hist(25,90)", not_typed_msg="Did you remember to call this with n=25? Make sure to call it with (25,90).")
test_student_typed("rep_hist(25)", not_typed_msg="Did you remember to call this with n=25? Make sure to call it with (25).")

success_msg("Great!")
```





--- type:VideoExercise lang:r xp:25 skills:1 key:2111db78fe
## Simulation of Distributions

*** =video_link

//player.vimeo.com/video/185155969




--- type:NormalExercise lang:r xp:100 skills:1 key:82b0d7ea8e
## Simulation with t-test

We will start to create a function that allows us to work with t-tests. 

*** =instructions

In your environment are `x` and `y`. These are random normal values that we wish to t-test. 

- use the `t.test` function on x and y. name this `test`.
- find the names of `test`.
- extract the p-value of `test` and call this `pval`.


*** =hint

Remember the parts of the function. This is very similar to one created during the video.


*** =pre_exercise_code
```{r}

set.seed(1234)
x <- rnorm(100, 0, 2)
y <- rnorm(100,0,2)


```


*** =sample_code

```{r}
# use the `t.test` function on x and y. name this `test`.




# find the names of `test`.





# extract the p-value of `test` and call this `pval`.


#print pval


```

*** =solution

```{r}
# use the `t.test` function on x and y. name this `test`.

test = t.test(x,y)


# find the names of `test`.
names(test)




# extract the p-value of `test` and call this `pval`.
pval = test$p.value


#Print pval
print(pval)

```

*** =sct
```{r}
test_object("test", incorrect_msg="Did you perform a t test of x and y?")
test_function("t.test", incorrect_msg="Did you use the t.test() function?")
test_function("names", incorrect_msg="Make sure you find the names of test.")
test_object("pval", incorrect_msg="Remember that test is just a list and there are a few ways to index from this list. ")
test_function("print", incorrect_msg="Make sure to print pval.")
success_msg("Great!")
```




--- type:NormalExercise lang:r xp:100 skills:1 key:d9322d8ce4
## Simulation with t-test function I

Now that you know how to extract the p-value we will create a function that does this for us. 

*** =instructions

- Write a function that takes input `x` and `y` call this `my_test`.
- This function should take the t-test of `x` and `y`.
- Then it should return the p-value. 
- Run this on `x` and `y`. (Already loaded on your system). Name this `pvals`.


*** =hint

Remember the parts of the function. This is very similar to one created during the video.


*** =pre_exercise_code
```{r}

set.seed(1234)
x <- rnorm(100, 0, 2)
y <- rnorm(100,0,2)


```


*** =sample_code

```{r}
# Write a function that takes input `x` and `y` call this my_test
# This function should take the t-test of `x` and `y`.
# Then it should return the p-value. 

# Run this on `x` and `y`. (Already loaded on your system). name this pvals.

```

*** =solution

```{r}
# Write a function that takes input `x` and `y` call this my_test
# This function should take the t-test of `x` and `y`.
# Then it should return the p-value. 


my_test = function(x,y){
    test = t.test(x,y)
    pval = test$p.value
    return(pval)
}
    




# Run this on `x` and `y`. (Already loaded on your system).

pvals = my_test(x,y)
```

*** =sct
```{r}
test_function_definition("my_test",
                              function_test= {
                              test_expression_result("my_test(x,y)")
                               }, 
                              body_test = test_function("t.test", incorrect_msg="Did you use t.test?"))
test_object("pvals", incorrect_msg="Did you remember to call your function for x and y and name it pvals?")
success_msg("Great!")
```




--- type:NormalExercise lang:r xp:100 skills:1 key:43c7f94b95
## Simulation with t-test function II

We will now modify the function to allow us to try more values. 
What we had been testing before was:
```
x <- rnorm(100, 0, 2)
y <- rnorm(100,0,2)
```

*** =instructions
Modify your previous function to now allow for:

- `mu1` mean of first normal.
- `var1` variance of first normal.
- `mu2` mean of second normal.
- `var2` variance of second normal.
- `n` number of samples of each normal.


- Generate `x` as the first normal with `n` samples of mean `mu1` and var `var1`.
- Generate `y` as the second normal with `n` samples of mean `mu2` and var `var2`.
- Compare with a t-test and return the p-value.
- Run this function with `mu1=mu2=var1=var2=1` and `n=100` name this p-vals.
*** =hint

Remember the parts of the function. This is very similar to one created during the video.


*** =pre_exercise_code
```{r}

set.seed(1234)


```


*** =sample_code

```{r}

# Modify the function as directed.





# Run the function with the parameters as listed and name pvals

```

*** =solution

```{r}
# Write a function that takes input `x` and `y` call this my_test
# This function should take the t-test of `x` and `y`.
# Then it should return the p-value. 

my_test = function(mu1, mu2, var1, var2, n ){
    x = rnorm(n,mu1,var1)
    y = rnorm(n,mu2, var2)
    test = t.test(x,y)
    pval = test$p.value
    return(pval)
}
    





# Run the function with the parameters as listed and name pvals

pvals = my_test(1,1,1,1,100)
```

*** =sct
```{r}
test_function_definition("my_test",
                            body_test = test_function("t.test", incorrect_msg="Did you use t.test?"))
test_object("pvals", incorrect_msg="Did you remember to call your function for x and y and name it pvals?")
success_msg("Great!")
```






--- type:VideoExercise lang:r xp:25 skills:1 key:d60f6b5f7c
## Further Simulations

*** =video_link

//player.vimeo.com/video/185158276


--- type:VideoExercise lang:r xp:25 skills:1 key:d109e47bec
##Sampling by Resampling

*** =video_link

//player.vimeo.com/video/185163362





--- type:MultipleChoiceExercise lang:r xp:75 skills: key:7a9a50bad5
## Resampling I


The Boostrap and Jackknife are the same method. 

*** =instructions

- True
- False



*** =hint


Try to remember the scope of functions.

*** =pre_exercise_code
```{r}


```

*** =sct
```{r}

test_mc(correct=2, feedback_msgs = c("Incorrect: They are not the same method. Jackknife leaves out a value and bootstrap actually samples the same length as the original object. ",
                                    "Correct: They are not the same but are 2 methods of resampling. "))

```





--- type:MultipleChoiceExercise lang:r xp:75 skills: key:2c64a67e71
## Resampling II


The Bootstrap only allows for each object to be chosen once. 

*** =instructions

- True
- False



*** =hint


Try to remember the scope of functions.

*** =pre_exercise_code
```{r}


```

*** =sct
```{r}

test_mc(correct=2, feedback_msgs = c("Incorrect:The bootstrap allows drawing with replacement. Remember the first bootstrap samples in the video.",
                                    "Correct: Bootstrap is sampling with replacement. We could actually sample the same value 1000 times even though this is unlikely.  "
                                    ))

```




--- type:MultipleChoiceExercise lang:r xp:75 skills: key:86b4c8800f
## Resampling III


The `sample()` function will work as long as the object has a value for `length()`. 

*** =instructions

- True
- False



*** =hint


Try to remember the scope of functions.

*** =pre_exercise_code
```{r}


```

*** =sct
```{r}

test_mc(correct=1, feedback_msgs = c("Coorrect:The bootstrap allows drawing with replacement. Remember the first bootstrap samples in the video.",
                                    "Incorrect: Bootstrap is sampling with replacement. We could actually sample the same value 1000 times even though this is unlikely.  "
                                    ))

```


--- type:VideoExercise lang:r xp:25 skills:1 key:b4f7a1bf1b
## Markov Chains 

*** =video_link

//player.vimeo.com/video/185166932




--- type:VideoExercise lang:r xp:25 skills:1 key:270f838f0e
## Rejection Sampling

*** =video_link

//player.vimeo.com/video/185171914




--- type:VideoExercise lang:r xp:25 skills:1 key:685cfa54e3
## Rejection Sampling Example

*** =video_link

//player.vimeo.com/video/185174478




--- type:VideoExercise lang:r xp:25 skills:1 key:ebe5ead16e
## Metropolis Hastings

*** =video_link

//player.vimeo.com/video/185175777



--- type:VideoExercise lang:r xp:25 skills:1 key:f148a1ff96
## Metropolis Hastings Example

*** =video_link

//player.vimeo.com/video/185177040




