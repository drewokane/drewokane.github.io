---
layout: post
title: First Steps with Theano
---

As I have progressed deeper and deeper into the scientific Python stack over the years, it struck me as surprising that I hadn't encountered or tried Theano before now. But first a little background on Theano.

# Theano

[Theano](http://www.deeplearning.net/software/theano/index.html) is a fairly nice Python library that mainly concerns itself with efficient mathematical operations. Think of it as an extension of [Numpy](http://www.numpy.org/), but with some added features. Specifically, when you write out mathematical operations in Theano, that operation gets turned into an operations graph, which dynamically generates C code, which is always nice for faster mathematics. Additionally there is the bonus of [automatic differentiation](https://en.wikipedia.org/wiki/Automatic_differentiation) for easy gradient calcuations. Now at this point I should probably let you know that I only have a basic understanding of automatic differentiation, but I *do* understand the practical upshot, easily computed gradients.

Being a statistician and applied mathematician, this brings me much joy, mostly because it means I can write likelihood functions directly, take gradients, and optimize them quickly. There is a little extra work but it's worth it.

# Theano in Practice

$$ \nabla \mathcal{L} $$
