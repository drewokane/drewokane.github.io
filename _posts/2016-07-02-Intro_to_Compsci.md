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
help determine what models and data get used in production, doing proof of concept
in Python, which is then handed off to software engineers for implementation. This is 
somewhat standard practice at a medium to large size company from what I can tell. The difficulty,
and I could probably write a whole other essay on this, is that Engineering implements
models in Clojure (or Scala to a lesser extent), so there is no continuity of language from
Science to engineering.

To mitigate this mismatch, I recently decided to learn Clojure, which brings me to the actual
point of this post.

## Not quite learning

Numerous self-paced coding resources exist these days, which is a blessing. Learning to code not
so long ago usually involved tracking down a book, motivating yourself to invent a project,
or take a class (if you were lucky) at a local junior college. Now you can go to any of several
websites that make games out of learning coding. Which has its pros and cons.

For the most part I have been happy with what I have found. The assignments are usually bite
sized and teach a single concept at a time. Most websites also organize the content so that
assignments get progressively more complex. Feedback is usually very quick since tests are run
right at submit time.

While I applaud efforts like this, I have found some of these websites frustrating. The quality
of the assignments is very spotty. The issues range from poorly worded explanations of the problem
to unrealistic and obscure test cases. I probably sound bitter.

As a former math teacher I can see the merit of stretching students minds with corner cases, but
I also know that with self motivating study programs there is usually short window of time where
the student needs to be rewarded for their efforts. Taunting a student with pathalogical test 
cases becomes mean. You are no longer teaching, you are rubbing dirt in someones face.

## A compromise?

While I wish I had a good compromise for this kind of situation, I don't see a clear one. As I
becomes a more and more competant programmer, I have begun to realize that edge cases pop up all
the time, contrary to popular opinion. The needs of a production environment, however, demand
results yesterday. It is the agile philosophy of "move fast and break things". In fact most tech
companies would probably subscribe to this philosophy.

This is a difficult tension to live in. Wanting to produce a product that satisfies a customer
while covering that edge cases where a thousand customers request information from your server at
5:30 am and the service crashes.

Learning is much the same way. There is a tension between wanting the student to succeed and see
the connections between concepts, and the growing and stretching to understand the subtleties
of a problem. So for now, I leave you with this tension and hope that we all will continue to
persevere in learning and building better learning tools.
