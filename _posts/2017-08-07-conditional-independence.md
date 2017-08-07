---
layout: post
title: What is conditional independence?
description: An intuitive explanation.
comments: true
published: false
feature: assets/img/conditional_independence/batman_robin_divorce.png
---

## Analogy

Conditional independence is like a marriage that ends in divorce. Two people are bound together till death do they part, but for one reason or another the relationship seems wrong. So they file for divorce and, conditional on confirmation from a lawyer, they are henceforth independent in the eyes of the law.

The "independent" part is a description of two parties' relationship to each other, and the "conditional" part is a description of their relationship's mediation by a third party, the lawyer. In probability, conditional independence is just this: *a relationship between two variables that is mediated by a third variable*.

## Diagram

![](../assets/img/conditional_independence/batman_robin_divorce.png)

## Example

For example, is there a relationship between a person's height and the size of their vocabulary? To answer this question, you might begin by comparing the heights and vocabularies of your friends. You would probably conclude that there is no relationship. If I were to tell you that I know one person who is 5'8" and another who is 5'11", you probably wouldn't bet any money on their relative vocabulary sizes. It may seem, therefore, that the height and vocabular size are independent of each other: knowing the value of one doesn't tell you anything about the value of the other. If height and vocabulary size were people, then they were never even married in the first place.

But then I tell you that I know somebody who is just 1'4". Are you willing to bet that this person's vocabulary size is smaller than those of the other two people? You should, because this person is probably a toddler. As it turns out, people's heights and their vocabulary sizes are *not* independent. If you know the value of either variable, you can make a decent guess at the person's age, which will help you guess the approximate value of the other variable.

When the value of one variable can help you guess the value of another variable, the two variables are said to be *dependent.* So, in the absence of any other information, age and vocabulary size are in fact dependent on each other. For better or for worse, the two variables are married.

However, if I tell you that I know two people who are 4 and 26 years old, you will be just as good at guessing their relative heights regardless of whether I tell you their vocabulary sizes. Given that you already know a person's age, you shouldn't pay a dime to learn their height if you're just trying to guess their vocabulary size, or vice versa. *Conditional on your knowledge of one variable, two other variables are independent of each other.*

I think the most confusing thing about the phrase "conditional independence" is that in statistics, saying "these two variables are independent" usually means "these two variables are useless for predicting each other." It has a *negative* connotation. And yet a state of conditional independence between two variables arises only when you *learn the value of a third variable.* How can it be that adding 



## Plain English

Independence is a relationship between two variables. "Conditional" means that that relationship depends on knowledge of the value of a third variable. It's almost like a divorce. It depends on a lawyer. Without the lawyer, the two people are not technically independent of each other. So we might know that the two people don't really want to associate with each other anymore. But we don't know whether the lawyer has pronounced their legal relationship to be annulled. It's not a perfect analogy, of course, because it kind of implies that the relationship used to exist but now it doesn't anymore. But maybe that's not so bad

## Technical definition


## Who cares?