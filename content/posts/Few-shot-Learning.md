---
title: "Few Shot Learning: Problem Definition"
date: 2022-07-29T14:26:21+04:30
draft: false
---
In this series we are going to talk about few-shot learning.

Few shot learning is useful when there are many different related `Tasks` but data for each one of them is lacking.

To give an example:

There is branch of science called `Math`. But there are different subject areas of Math. In order to learn Math you have to learn the different subject areas. For example one might imagine that a person who knows how to do `multiplication` will have an easier time learning derivatives than a person who does not know how to do multiplication.

We i.e Humans do this all the time. It is in fact the most common way humans learn something. Do you remember the last time you learned something new? I'm sure you made a comparison with that and something else that you already knew. Because I am a software engineer, When I wanted to learn about neural networks I thought of them as functions that take an input and will then return an output. Just like the function that I wrote in a daily basis. Wheras If I was a neurologist, I would not do so, In fact If I wanted to learn about Artificial Neural Networks, I would make an analogy between them and real brain neural networks and I'll bet that I would have a hard time learning ANNs that way. Because, even though ANN's are inspired by the brain, they are inherently mathematical and a mathematical/programming background can make it alot easier to learn them even though having a Neuroscience background is still easier than not having any background in either.

This was an inutive explaination. Let's see a few formal examples:

I might have a dataset D with N datapoints. Each of the datapoints include features $X_1$ to $X_n$ and a target variable called `y`.

This is the classic definition for a classification problem. But, there is a catch. The actual values that `y` can take is a lot. Meaning the number of classes is high, think `100`. Furthermore, the number of datapoints for each of the classes is low. Think `10`. Now do you think that you can train a neural network to do this kind of classification? It depends...

As a concrete example, you can think of the problem of taking in a movie review, and instead of doing a salience test on it. you have to predict what `movie` the movie review is refering to. This is very diffcult! Why?

For one the number of movies in the world is not a static amount. Yesterday 10 new movies got released. If you tried using a simple multi layer perceptron (MLP) in order to do this prediction, you will have to add a new neuron for every single movie that gets release!

Secondly, for these new movies that got released yesterday, you don't have a lot of examples! Currently, just a few movie reviews are out and you should be able to do this prediction on new movie reviews for that particular movie based on those few examples.

Humans are good at this though, We intutively can tell whether a movie review is about the new spider man movie even though we haven't read a lot of spider man movie reviews. But how do we do that?

If we wanted to formulate this review to movie prediction problem in terms of a few shot learning problem we would formulate it as a **100 Way-K shot problem** K here refers to the number of known movie reviews of a movie that we can use as a reference point for to predict the future movie reviews for that same movie.

In later posts I will elaborate on ways that this problem can be resolved.