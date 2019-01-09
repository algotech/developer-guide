# Story points

 - [Intro](#intro)
 - [How to estimate](#how-to-estimate)
 - [The scale](#how-to-estimate)
 
### Intro

 - Using points is one version of what is often called "Relative sizing".
 - The goal is to group things of similar overall size rather than to pursue a highly precise estimate.
 - Most uses of story point estimation limit you to the lower end of the Fibonacci series:
 1, 2, 3, 5, 8, 13 

### How to estimate

Story points often take into account three different aspects when estimating:
Complexity, Effort, and Doubt. This allows them to more effectively capture the sources of variation
that will make an hour-based estimate wrong.

 - Complexity is the "stuff we have to figure out". We know we can solve the problem, and we probably
 have a decent feel for how we'll approach it, but we still have to figure it out.
 - Effort is the sheer amount of stuff that needs done. 
 - Doubt is about the stuff we don't actually know if it can be done. We may suspect we're on the
 wrong track, that the technology isn't up to it, or some other factor that would cause us to churn
 for a while before we figure out if we can actually do the work.
 
Most stories contain a combination of all three, and thus it's useful to have a common language so
that when I say `it's an eight`, I can follow with "because of the complexity of the foobar algorithm"
or "because I'm not sure if our cache is set up to handle that yet".
 
The final point estimate is just a way to say "taking all of these things into account, I think this is
bigger than most of the things we've called a three and smaller than most of the things that we've called
an eight, so it must be a five".

### The scale

We use a Fibonacci sequence to 8. Please use the list below as a guideline. We are looking to estimate
these tasks by the amount of effort, not by the amount of time:
 - 0 - Really Easy
 - 1 - Easy
 - 2 - Medium
 - 3 - Hard
 - 5 - Very Hard
 - 8 - Really Hard and Complex
