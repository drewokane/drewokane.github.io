---
layout: post
title: There be Jabberwockies, A Tale of Mismatched Needs
---

## The Manager's Tale

Let's say one day you're sitting in your manager's chair and one of your data scientists
comes up to you and says, "Hey, I have this fantastic idea that will give us a 10X boost in
customer satisfaction!". The moment you hear this your eyes bug out and you leap from your
chair and holler:

> And, has thou slain the Jabberwock?
> Come to my arms, my beamish boy!
> O frabjous day! Callooh! Callay!

Your delight is short lived though as you begin to think about how you will get this 10X
idea implemented. Images of irrate middle managers, thundering vice president's of product, and
a fuming CSO make you recall some very wise words passed along to you years ago:

> Beware the Jabberwock, my son!
> The jaws that bite, the claws that catch!
> Beware the Jubjub bird, and shun
> The frumious Bandersnatch!

You take a deep breath and think some more about what your available options are. It occurs to 
you that there are several ways you could solve this problem:

1. Have your Engineers write tools in the production language that scientists can use
   for research and prototyping.
2. Let your Scientists write in their language of choice and then have Engineers translate
   to the preferred production language.
3. Have your Engineers and Scientists use the same language for research and production.

Option 2 seems to be the status quo for most tech companies. Option 1 seems like a 
really cool idea which you have heard some companies claim to do 
([Stitch Fix for example](https://multithreaded.stitchfix.com/blog/2016/03/16/engineers-shouldnt-write-etl/)).
Option 3 frankly sounds like a place that only unicorns work at. Let's think about each of 
these options one at a time.

## A Common Tongue (Option 3)

In a perfect world, there would be only one programming language that did it all. It would
be the swiss army knife that could do CSV parsing, plotting, data science, and parallel
big data processing. Unfortunately we don't live in that kind of world. What we have is more
along the lines of as-seen-on-tv types of programming languages that can do some things
fantastically but not everything.

I know at this point someone will be saying, "Hey, what about ___ ? It does it 
all and is quite good at everything!". I would counter that if this were the case then there
would actually be a company that only uses one langauge for their full stack, which I have
yet to hear about. Some of this can probably be traced back to having too many cooks wanting to use
their favorite framework/JVM/newly fashionable language to do the job.

In reality, certain languages are more suited to certain tasks than others along with the fact
that developers will develop what they are passionate about. Developers don't seem to want to
build some programming tower of babel. That just doesn't seem to be a thing. Individuals have tried
to advocate for certain languages being the final word but again, where is this "one
langauge to rule them all"?

Another issue that comes with this option is that you need data scientists and engineers to agree
on a language. And it will have to do both tasks well enough. Which will probably disappoint everybody
at some point. So scratch that.

## SSWEeeet Times (Option 2)

Like I mentioned, this option seems to be the standard method for putting models and improvements
into production. It then requires some sort of assignment of engineering resources towards
translating of researcher code.

One could argue that this arrangement separates the concerns of ideation and implementation. Let the
data scientists come up with the ideas and let the engineers make it work in the real world. While this
sounds great, I do think it leads to conflict, disappointment, and frustration. The Stitch Fix article
puts it pretty well I think:

> In case you did not realize it, *Nobody enjoys writing and maintaining data pipelines or ETL*. It’s
> the industry’s ultimate hot potato. It really shouldn’t come as a surprise then that ETL engineering
> roles are the archetypal breeding ground of mediocrity.
> 
> Engineers should not write ETL. For the love of everything sacred and holy in the profession, this
> should not be a dedicated or specialized role. There is nothing more soul sucking than writing, 
> maintaining, modifying, and supporting ETL to produce data that you yourself never get to use or consume.

I would take some issue with the label of mediocre that the author places on all who wind up in this weird 
middle ground. But his point is still valid. Nobody likes implementing someone elses idea, particularly if
it's poorly written in the first place. As a SSWE you then have two options:

1. Rewrite the d@mn thing using proper software engineering design principles
2. Give in to apathy and just pass the code along (mostly) unchanged

This arrangement also allows data scientists to abdicate responsibility for writing good code in the first
place. Why bother writing something that will scale, has good documentation, and is fast when you have an 
engineer to do that for you?

## The Nailsmith and The Knight (Option 3)

A small digression, please indulge me. I play [Hollow Knight](http://hollowknight.com/) in my spare time, 
when I'm not cooking, hiking with my wife and daughter, or building tiny lego towers with my daughter. The
knight in the game starts out with a basic nail to fight with. Part was through the game he meets the
nailsmith who offers to make the knight's nail stronger and sharper. The knight gives his nail to the smith
who proceeds to make it sharper and more powerful. The knight can now defeat enemies quicker, deal more damage,
and explore more dangerous places on his quest. Why am I mentioning this?

I already elaborated the previous two approaches and what the disadvatages are. The main failing usually is
that people wind up doing things then don't really want to. For example, if everyone writes the in same 
language, then either data scientists will feel underpowered and weak or engineers will feel hamstrung. In
option 2 we have engineers specifically hired to deal with other people's messy inefficient code who dream
of doing better things.

In either of those cases we have woefully ill equipped knights fighting monsters far bigger then they
originally thought they would.

So why not let people do what they are good at and passionate about?

Engineers are good at crafting well thought out tools. Data scientists are good at analysis, discovery, and
exploration. Let the engineers craft the tools for the data nerds. You wouldn't tell a novice cook, "Hey, 
if you want to make bread, you'll need to go buy some wheat seed, plant it, tend it, harvest it, grind it,
make the bread, build your own brick oven, chop some wood, and then bake the bread!". A cook *cooks*. A
farmer *farms*. The knight can't fight monsters all that effectively without a good nail and he can't have
good tools unless there's a nailsmith to help him.

## Epilogue

So where does that leave us? You've been twirling in your managers chair for some time now talking to yourself.
Your coworkers are giving you odd looks. The facilities manager has even wandered by and asked if you're okay.

Unfortunately you can't do much. You're stuck with the organization structure that you have. *You*, as the
manager, need to make sure everyone is happy in what they're doing. So my advice to you is this. Tell
your data scientist to get cozy with the engineer(s) they will be working with to implement the enhancement.
As we all know, ultimately the engineer is going to be implementing it, but we can ease the transition. The
data scientist can shepherd the new code from ideation through crafting by the engineer. Keep everyone in the 
loop for the whole process. Once you allow someone to back out, it will create resentment. New ideas need 
passionate people. The new idea is a baby that needs nuturing. And just like you need both parents involved to
have a happy healthy child, you need your scientists and engineers talking, collaborating, and working
together if we want a scalable, performant, fault-tolerant system.

I don't really have a silver bullet for you, but I do know a nailsmith who might come in handy. Good luck people.
