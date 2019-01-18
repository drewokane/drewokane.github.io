---
layout: post
title: "Test your code. Please."
categories: engineering testing best-practices science reproducibility
---

The scientific computing community has a problem. A fairly large one. Come to think of it, even
good old experimental science has this problem. I'm talking about the 
[reproducibility crisis](http://www.wired.co.uk/article/science-academic-papers-review). 
Essentially we cannot repeat the results seen in a significant portion, somewhere between 65%
and 95%, of experiments performed in biomedical science. And even worse, scientists aren't
incentivized to make their research reproducible or even return a non-significant result.

Truth be told, [science is hard](https://fivethirtyeight.com/features/science-isnt-broken/#part1).
It's hard working with real data to find causes and effects. Being honest in science about the
fact that your model might not say anything new is not celebrated. Which leads me to my point.

If you work at a data science type tech company, you regularly have data scientists developing
models that try to make predictions, classify things, or make recommendations to people much like
science. These models are then passed along to engineers who create backend services which utilize
them. The crisis comes to a head when the engineer says to the scientist, "Hey, we need to test 
this, got any ideas?". The researcher will scratch their head, think very hard for a few minutes 
and say one of the following:

1. "I already tested it. It is a perfectly crafted model that needs no testing."
1. "I'm not sure how to test my model. Got any ideas?"
1. "What do you mean test my model? What's a test?"
1. "Sure, here are my ideas...."

If you hear the last one, consider yourself blessed. If you hear the third one, you at least can
have a conversation about what testing is and why it's important. The second response isn't quite
so bad since the researcher is willing and this could lead to a very fruitful conversation about
the model and both parties come away with a greater appreciation for how integral we all are
in making the company work.

The first response is perhaps the least desireable. The researcher knows (or at least has some idea)
what testing is. The difficulty then is that the researcher has implicit faith in the absolute
truth of their model. I realize I am perhaps putting words in people's mouths when I say this
but it does seem odd to believe absolutly in the truth of a model when statistics says the
opposite. Models have uncertainty, even perfectly crafted ones. Perhaps in a perfect world we might be
able to believe a model without needing to validate it but we are not in Kansas Dorothy.

But why do the testing? I'll present a few reasons.

## Models aren't perfect

Sad to say this but I will quote George Box: "All models are wrong, but some are useful." Models are
approximations of reality. This means we need to know *how* wrong our model is. Enter testing.

## Your dataset isn't complete

Unless you have unlimited resources and computing power, your dataset probably hasn't sampled the
entirety of the population. Therefor you'll probably encounter someone/something that wasn't in
your dataset. Edge cases, corner cases. Testing protects us against completely new data never
seen before.

## Your user population may change over time

People are born every day. Users join and leave over time. Your model that was built in 2012 might
not be as right in 2013. Your user base may have changed, new data might have become available,
demographics might have changed. Testing can surface this over time, hopefully as it happens. See
[model drift](https://en.wikipedia.org/wiki/Concept_drift).

So please, if you have a science model, test it. Test it good.
