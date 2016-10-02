---
title       : Simulations
description : In this chapter we will cover statistical simulations. 


--- type:VideoExercise lang:r xp:25 skills:1 key:b330fb454f
## Random Variables

*** =video_link

//player.vimeo.com/video/




--- type:VideoExercise lang:r xp:25 skills:1 key:6faff5dbf6
## Discrete Random Variables

*** =video_link

//player.vimeo.com/video/





--- type:NormalExercise lang:r xp:100 skills:1 key:e412be26b2
## Generating Discrete Distributions


We will start by generating data from discrete distributions. 

*** =instructions

Your goal will be to use the discrete distribution functions in R. (A seed ahs been set do not set one)

- Generate 100 random Poisson random variables with $\lambda = 0.2$, name this `x1`. 
- Generate 100 random Poisson random variables with $\lambda=0.2$ name this `x2`. 
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

# Generate 100 random Poisson random variables with lambda = 0.2
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

# Generate 100 random Poisson random variables with lambda = 0.2
x2= rpois(100, 0.2)


# Find the difference in means
diff_means = mean(x1) - mean(x2)


# print diff_means

print(diff_means)
```

*** =sct
```{r}
test_object("x1", incorrect_msg="Make sure you drew 100 samples using rpois().")
test_function("rpois", incorrect_msg="Make sure you drew 100 samples using rpois().")
test_object("x2", incorrect_msg="Make sure you drew 10000 samples using rpois().")
test_function("rpois", incorrect_msg="Make sure you drew 10000 samples using rpois().")
test_object("dist_means", incorrect_msg="Make sure to take the difference in means.")
test_function("mean", incorrect_msg="Did you use the mean function?")
test_function("print", incorrect_msg="Did you print the difference in means?")
success_msg("Great!")
```




--- type:VideoExercise lang:r xp:25 skills:1 key:4da94c8c0e
## Continuous Random Variables

*** =video_link

//player.vimeo.com/video/






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

//player.vimeo.com/video/


--- type:VideoExercise lang:r xp:25 skills:1 key:cb6c69d7e0
## Basics of Simulations Continued

*** =video_link

//player.vimeo.com/video/


--- type:VideoExercise lang:r xp:25 skills:1 key:2111db78fe
## Simulation of Distributions

*** =video_link

//player.vimeo.com/video/


--- type:VideoExercise lang:r xp:25 skills:1 key:d60f6b5f7c
## Further Simulations

*** =video_link

//player.vimeo.com/video/


--- type:VideoExercise lang:r xp:25 skills:1 key:d109e47bec
##Sampling by Resampling

*** =video_link

//player.vimeo.com/video/


--- type:VideoExercise lang:r xp:25 skills:1 key:b4f7a1bf1b
## Markov Chains and Monte Carlo

*** =video_link

//player.vimeo.com/video/




--- type:VideoExercise lang:r xp:25 skills:1 key:270f838f0e
## Rejection Sampling

*** =video_link

//player.vimeo.com/video/




--- type:VideoExercise lang:r xp:25 skills:1 key:685cfa54e3
## Rejection Sampling Example

*** =video_link

//player.vimeo.com/video/




--- type:VideoExercise lang:r xp:25 skills:1 key:ebe5ead16e
## Metropolis Hastings

*** =video_link

//player.vimeo.com/video/



--- type:VideoExercise lang:r xp:25 skills:1 key:f148a1ff96
## Metropolis Hastings Example

*** =video_link

//player.vimeo.com/video/




