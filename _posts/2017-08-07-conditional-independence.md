---
layout: post
title: What is conditional independence?
description: An intuitive explanation.
comments: true
published: true
feature: assets/img/conditional_independence/batman_robin_divorce.png
---

Conditional independence is like a marriage that ends in divorce. Two people are bound together till death do they part, but for one reason or another the relationship seems wrong. So they file for divorce and, conditional on assistance from a lawyer, they are henceforth independent in the eyes of the law.

The "independent" part is a description of two parties' relationship to each other, and the "conditional" part is a description of their relationship's mediation by a third party, the lawyer. In probability, conditional independence is just this: *a relationship between two variables that is mediated by a third variable*.

![](../assets/img/conditional_independence/batman_robin_divorce.png)

For example: Is there a relationship between a person's height and the size of their vocabulary? To answer this question, you might begin by comparing the heights and vocabularies of your friends. You would probably conclude that there is no relationship. If I were to tell you that I know one person who is 5'8" and another who is 5'11", you wouldn't bet any money on their relative vocabulary sizes. It may seem, therefore, that height and vocabulary size are independent of each other: knowing the value of one doesn't tell you anything about the value of the other. If height and vocabulary size were people, then they were never even married in the first place.

But then I tell you that I know somebody who is just 1'4". Are you willing to bet that this person's vocabulary size is smaller than those of the other two people? You should, because based on the information you've been given, this person is probably a toddler. As it turns out, people's heights and their vocabulary sizes are *not* independent. If you know the value of either variable, you can make a decent guess at the person's age, which will help you guess the approximate value of the other variable.

When the value of one variable can help you guess the value of another variable, the two variables are said to be *dependent.* So, in the absence of any other information, height and vocabulary size are in fact dependent on each other. For better or for worse, the two variables are married.

Now, if I tell you that I know two people who are 4 and 26 years old, you will be just as good at guessing their relative heights regardless of whether I tell you their vocabulary sizes. Given that you already know a person's age, you shouldn't pay a dime to learn their height if you're just trying to guess their vocabulary size, or vice versa. *Conditional on your knowledge of one variable, two other variables are independent of each other.* When you learn the value of that third variable, the lawyer steps in and the other two variables are officially divorced.

Let's get a bit more formal. When we talk about probability, we usually denote the probability of an event *A* as *Pr(A)*. Let's say the following:

* The event *A* is that a person is in the 99th percentile for vocabulary size.
* The event *B* is that the person is 1'4".
* The event *C* is that the person is two years old.

Now let's compare a few probabilities. Consider the following statement:

$$Pr(A|B)=Pr(A)$$

This means, *The probability that {this person is in the 99th percentile for vocabulary size given that they are 1'4"} is the same as the probability that {they are in the 99th percentile for vocabulary size}.* Is this statement true? Take a moment to think about it.

...

...

...

...

...

...

...

No, it's not true. If we know that a person is 1'4", it's reasonable to guess that they're a toddler, and that they are therefore much closer to the 1st percentile than to the 99th. The right-hand probability is, by definition, 1%. But the left-hand probability is infinitesimally small. There are simply no two-year-olds whose vocabularies are larger than 99% of all people.

Now consider the following statement:

$$Pr(A|C)=Pr(A|B \cap C)$$

This means, *The probability that {a person is in the 99th percentile for vocabulary size given that they are two years old} is the same as the probability that {they are in the 99th percentile for vocabulary size given that they are 1'4" and two years old}.* Is this true?

...

...

...

...

...

...

...

Yes! Once we know that the person is two years old, we won't learn anything new about their vocabulary size by learning about their height. We can therefore say that events *A* and *B* are independent conditional on *C*. The above formula expresses the necessary and sufficient conditions for conditional independence. We can also write it like this:

$$A\perp \!\!\!\perp B\mid C$$

This reads, "*A* is independent of *B*, given *C*."

I think the most confusing thing about conditional independence is that in statistics, "these two variables are independent" is often said as a shorthand for "these two variables are useless for predicting each other." The word "independent" has a *negative* connotation. And yet a state of conditional independence between two variables arises only when you *learn the value of a third variable.* How can it be that to begin with, two variables are *useful* for predicting each other, but then you learn something new, and now those two variables are *useless* for predicting each other? Couldn't you just, you know, pretend you hadn't learned about that third variable?

Well, you could. But that would be a bit like sitting in a trailer and pretending that you're moving forward because of the trailer rather than because of the truck that is pulling it. If you want to predict a person's height or their vocabulary size based on another variable, you should be happier if that other variable is *causing* the one you're interested in, rather than simply being *correlated* with it. Why is it better to find causality than to find correlation? Because it means that if you want to intervene, you won't waste resources trying to manipulate a variable that exerts no causal force. You can't make a child taller by forcing them to read the dictionary. But you can wait till they're older, and they will grow taller and more erudite.