---
layout: post
title: If you want to learn to program...
---

When people ask me what I do, I usually reply that I do statistics at a tech company.
This usually placates people. For the more tenacious questioner, I usually go on to say
something about developing statistical models and programming. At this point most
people are content but for the very few who press me further, I will admit that I
am not a computer scientist and my programming training has been largely spotty,
pragmatic, and not particularly formal.

## Beginnings

The first clue to this is that my first language was Matlab. I took an introductory course
which was mostly filled with mechanical engineers and hence my major takeaway from the
class was how to do math with a computer. From here, I then learned IDL, which only 
astronomers seem to use any more. Again, this wound up being fancy calculator stuff. It
really wasn't until I did a research internship with a planetary science professor that
I encountered Python.

## Python

Python was something of a revelation. It was much less a set of calculator instructions
so much as an actual general purpose programming language. You could do so much more
than math. You could process text, write a command line program, etc. This was the
first time I had encountered object oriented programming, list comprehensions, and
lambdas. My mind was expanded greatly to say the least.

I didn't really get any formal training in computer science which is not a huge regret to
me. I'm an astrophysicist who likes to use programming to solve things. Python made sense
for this kind of work. It is a general purpose language with lots of capabilities. And
from the first time I encountered it, circa 2008, it has mushroomed to include all sorts
of capabilities. It makes a pretty great first programming language.

## And then there was Clojure

Fastforward a few years, I have my masters, I've learned R, and I have a job at a tech company.
I'm using Python to do data science. It's all very straighforward. But not quite.

I was hired to work in the Science group at my company, which essentially means that I
help determine what models and data get used in production, essentially doing proof of concept
in Python, which is then handed off to software engineers for implementation. This is 
somewhat standard practice at a medium to large size company from what I can tell. The difficulty,
and I could probably write a whole other essay on this, is that Engineering implements
models in Clojure (or Scala to a lesser extent), so there is no continuity of language from
Science to engineering.

There's several ways you could solve this problem:

1. Have your Engineers write tools in the production language that scientists can use
   for research and prototyping.
2. Let your Scientists write in their language of choice and then have Engineers translate
   to the preferred production language.
3. Have your Engineers and Scientists use the same language for research and production.


