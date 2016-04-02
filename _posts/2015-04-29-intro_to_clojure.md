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
at this point in my Clojure journey, the two methods look pretty similar in
brevity. And maybe this is the point, as far as list comprehensions go. List
comprehensions are actually quite concise, which is one of the reasons I like
Python. But all that said, list comprehensions are probably not a good place to
compare the two languages.

A better comparison might be a [Project Euler](https://projecteuler.net) problem
I tried out. The problem goes like this,

    If we list all the natural numbers below 10 that are multiples of 3 or 5, we
get 3, 5, 6 and 9. The sum of these multiples is 23.

    Find the sum of all the multiples of 3 or 5 below 1000.

One clarification is needed though, this is not an exclusive or, where we only
have multiples of only 3 or only 5. Multiples can be multiples of 3, 5 or 3 and
5. If you don't belive me, solve the problem and see the solution they give.

In Python, this sort of problem might be amenable to a list comprehension
(admittedly this is not the cleverest way, but really the naive straightforward
way), which would probably look like this:

```python
sum([i for i in range(1000) if ((i % 3) == 0) or ((i % 5) == 0)])
```

Clojure:

```clojure
(reduce + (filter #(or (= 0 (mod % 3)) (= 0 (mod % 5))) (range 1000)))
```

Not very different you say. I would agree again. The surprising point comes when
you look at performance. For adding up the multiples of 3 or 5 up to 1000,
Python comes in at 466 micro-seconds, while Clojure clocks in at 623
micro-seconds. The point goes to Python this time, but what happens when you ramp up the upper limit? Not surprisingly when you go up by a factor of 10, Python starts to slow down:

| Upper limit | Clojure | Python |
|-------------|---------|--------|
| 1000        |0.623 ms |0.466 ms|  
| 10000       |2.38 ms  |3.59 ms |
| 100000      |20.0 ms  |25.2 ms |
| 1000000     |235 ms   |350 ms  |

No I know this isn't a really great benchmark but I do think it does at least hint at what is going on under the hood and how each of the systems handles numerical computations. Ultimately, neither Clojure nor Python is build first and foremost for numerical computations. Python was originally conceived as a scripting language that has become an incredibly useful language that can do just about anything you want it to, from building websites to inverting matrices. Clojure is still young but it seems to me that at least at this point, it is headed in roughly the same direction, i.e. a language that wasn't quite originally intended to do everything but might actually get there some day.

At this, the beginning of my journey, I am hopeful for what Clojure can offer.
