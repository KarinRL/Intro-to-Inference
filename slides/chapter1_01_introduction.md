---
type: slides
---

# Introduction

Notes: Many time we are interested in the characteristics of a population. For example, we may want to know what proportion of college students are registered to vote, what is the fatality rate of the corona virus? are minorities discriminated in the way the SAT test is performed?

To investigate any of these questions, we take an appropriate sample or compare samples that will help us make an educted guess. In the earlier part of the course, you learned about techniques to collect data in a way that are useful to study the question. That is, we talked about sampling techniques to make sure the sample is representative of the population we want to study and that it makes the best attempt are reducing sources of biases. 

The data was collected with a particular measurement in mind. For the voting question, we simply needed the number of registered voters, for the SAT, we would collect the SAT scores aong with minority classification of students taking the test. We also learned how to produce statistical summaries, and pictures that helps display the data and start to get a basic feeling for the story the data is telling. 

Next, we want to make inferences about the larger population, using the statistics we can compute from our data. 

So in this section, we will develop a basic understanding of how can we use our simple sample or samples to make inferences to answer our questions.

---

# This is a slide
UAlbany campus has a fish pond.   Suppose there are 100 fish in the pond.  The lengths of the fish (in inches) are given below: 

```r
x<-rnorm(100,8.25,.75)
print(x)
```

```out
print(x)
```

If we are interested in finding out how large the fish are, we would take a sample of size 5 and measure each fish. 

```r
sampl<-smaple(5,x,replace=FALSE)
```

And we can estimate the mean length using our sample:
```{r}
mean(sampl)
```

Now this is just one sample and with our time and budge, we can not take more samples we need to use what we got to make an educated guess about the true mean average of the fish in the pod.

The word "educated" means that we need to know a little about the distribution of the sample mean. Our one sample had mean: and standard deviation: but if I take another sample, we would get different answers. So let's take a few samples and see what happens.

```{r}
m=100, n=5
sample.means<-numeric(m)
sample.sdevs<-numeric(m)
for(i in 1:m){
   temp<-sample(n,x)
   sample.means[i]<-mean(temp)
   sample.sdevs[i]<-sd(temp)
   }
plot(sample.means)
```

- Slides can have code, bullet points, tables and pretty much all other Markdown
  elements.
- This is another bullet point.

<img src="profile.jpg" alt="This image is in /static" width="25%">

Notes: Some more notes go here

---

# Let's practice!

Notes: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam tristique
libero at est congue, sed vestibulum tortor laoreet. Aenean egestas massa non
commodo consequat. Curabitur faucibus, sapien vitae euismod imperdiet, arcu erat
semper urna, in accumsan sapien dui ac mi. Pellentesque felis lorem, semper nec
velit nec, consectetur placerat enim.
