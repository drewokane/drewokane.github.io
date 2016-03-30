---
layout: post
title: First Steps with Theano
---

As I have progressed deeper and deeper into the scientific Python stack over the
years, it struck me as surprising that I hadn't encountered or tried Theano
before now. But first a little background on Theano.

# Theano

[Theano](http://www.deeplearning.net/software/theano/index.html) is a fairly
nice Python library that mainly concerns itself with efficient mathematical
operations. Think of it as an extension of [Numpy](http://www.numpy.org/), but
with some added features. Specifically, when you write out mathematical
operations in Theano, that operation gets turned into an operations graph, which
dynamically generates C code, which is always nice for faster mathematics.
Additionally there is the bonus of [automatic differentiation](https://en.wikipedia.org/wiki/Automatic_differentiation)
for easy gradient calcuations. Now at this point I should probably let you know
that I only have a basic understanding of automatic differentiation, but I *do*
understand the practical upshot, easily computed gradients.

Being a statistician and applied mathematician, this brings me much joy, mostly
because it means I can write likelihood functions directly, take gradients, and
optimize them quickly. There is a little extra work but it's worth it.

# Theano in Practice

For me, while a tool may be amazing in its capabilities, if the initial learning curve is too steep I will probably give up and find something else. While this might be a suboptimal strategy when it comes to expanding my skills, I still would argue that this is what really separates widely used tools from tools that languish in obscurity. For example, this is why [scikit-learn](http://www.scikit-learn.org)
is such a widely used, strongly supported, and actively developed Python machine learning package. All you really have to do is the following if you want to do a random forest regression:

```python
> from sklearn.ensemble import RandomForestRegressor

> regressor = RandomForestRegressor()
> regressor.fit(Xtrain, ytrain)

> predictions = regressor.predict(Xtest)

> regressor.score(Xvalidation, yvalidation)
```

That is a total of five lines of code to:

1. Fit a model
2. Predict at new x values
3. Evaluate the model at some validation locations

It really doesn't get much easier than this.

This is also why R is also popular with _most_ statisticians. The formula syntax for generalized linear models is incredibly easy to use. My point with these examples is that lower hurdles to entry for non-computer scientists generally allows for a wider adoption of a tool. Which is why I have found myself coming to Theano so late and not much earlier.

Not that Theano is difficult to use. The package's main page looks very cluttered and full of information I wish I knew what it meant. *Note to Theano maintainers: the main home page is _very_ cluttered.* The home page that greets you does have links to introductions which, once you find them, are actually quite informative. For the most part, you can pretty much write mathematical operations as you would have in numpy. This is a tremendous advantage. Hurdle number one is not so bad.
There is some thinking ahead that needs to be done regarding whether the objects you are working with are matrices or vectors, but this is pretty light. Definitely not on the order of having to declare the type and size of arrays like in a compiled language.

$$ \nabla \mathcal{L} $$
