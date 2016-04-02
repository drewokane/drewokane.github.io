---
layout: post
title: First Steps in Clojure
---

Usually for me there has to be some major motivating force for me to learn
something new, like an optimization technique, statistical model, etc.
Programming languages are like that too. It is only because I am transitioning
into doing half engineering, half research work that I am even motivated to
learn Clojure. Not to say that Clojure is bad. Or good for that matter.

Another wrinkle to the situation is that I am diving into a Lisp-like language
for the first time. I find myself chuckling and recalling a [cartoon about
programming
languages](http://bjorn.tipling.com/if-programming-languages-were-weapons). The
punchline, to ruin it for you dear reader, is that Lisp is a shiv and the
wielder
of said shiv is probably crazy and dangerous. Philosophically speaking, I sort
of get the joke but like all humor, there's a grain of truth in the backhanded
compliment. Take a simple task, like filtering out certain things from a list.
In good old Python, which is described as a double barreled shotgun that you
always use the wrong barrel of, such a task would look like this:

```python
[i for i in range(10) if i > 3]
```

while in Clojure we get:

```clojure
(filter #(> % 3) (range 10))
```

You could probably say that the Clojure syntax is a little more elegant, but 
at this point in my Clojure journey, the two methods look pretty similar in brevity. And maybe this is the point, as far as list comprehensions go. List comprehensions are actually quite concise, which is one of the reasons I like Python. 
