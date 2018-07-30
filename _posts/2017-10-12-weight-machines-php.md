---
layout: post
title: Weight Machines are the PHP of Strength Training
---
This is a post about PHP, but it is not a post about whether PHP is an Objectively Good or Bad Language. Enough has been written on that, and I don't think I have much to add. Instead, it's a post on how our experiences with a tool shape our opinions on that tool.

It's also a chance for me to combine two of my seemingly unrelated obsessions of the moment: the ways people learn and talk about technology, and weight lifting. My friends are tired of hearing me talk about these things, so I'm expounding upon them for you, dear reader.

## You'll Never get Strong with Weight Machines

Over at their excellent Gains blog, fitness coach Adam Fisher [writes about their early experiences with weight lifting](http://www.gains.af/blog/machines-vs-freeweights), and how the messages they received formed their point of view on the equipment they had used.

> When I first started lifting, I used the machines at my local YMCA. I didn’t know how to lift, what good form looked like, or how to progress a program. [...]
>
> The more I learned, the more I was told not to use machines. **Free weights are better**, I heard. They mean more strength, more muscle, and greater emphasis on “stabilizer” muscles. Avoid the machines, avoid the smith machine, and avoid isolation exercises.


This is consistent with my own experience, by the way. I first started weight lifting years ago on [machines](https://en.wikipedia.org/wiki/Weight_machine), and only recently switched to barbell and dumbbell exercises--in large part because of the [messages](https://www.reddit.com/r/Fitness/wiki/faq#wiki_should_i_use_machines_to_avoid_injury.3F) I've seen about the  [inferiority](https://www.nerdfitness.com/blog/rage-against-the-machine-how-to-switch-from-exercise-machines-to-free-weights/) of weight machines. Plus, in my extremely expert opinion, barbells are more fun.

But wait!

> Later, I got more and more confused by a lot of the stuff I see from elite level athletes, including bodybuilders, strongmen, olympic weightlifters, and more - I saw them taking videos of themselves using machines! [...]
>
> These are just a few of the examples, if you know where to look. It became clear that maybe ‘no machines’ wasn’t as simple as I thought.

Does that mean that weight machines are *good*? I thought they were bad! I thought they made you less strong, they were for lazy people who didn't know what they're doing, and you'll never succeed if you don't use free weights exclusively.

> The things that huge jacked dudes do aren’t necessarily a good argument - they’re not proof that what they’re doing is **good training**, but at the very least it seemed **not to be bad training**.
>
> Are free weights better for building strength and muscle? Well, the answer (like so many in fitness) is that **it depends**.

In other words: weight machines are just a tool. There may be reasons why they're better or worse for a given person trying to accomplish a given goal. That's not the same as all weight machines being all bad all the time, or all people who use them being inferior.

However, a lot of us have opinions on weight machines that go beyond their inherent pros and cons. And often, those opinions are reinforced by the overall state of our strength training practice when we use them. In other words, we are *biased* in our opinions on the tool because of the context in which we first encountered the tool.

> I had been using machines entirely during the worst parts of my own training. The story added up, clearly the machines were at fault.

This isn't to say the tool has no problems, is perfect for every situation, or is even the right tool for the person in any context. It's to say there's often a deeper background to a person's strong feelings on that tool--and often, that background is obscured by not seeing one's own role in the problem.

> The reason that I wasn’t building much muscle or strength when I started lifting wasn't that I was using machines - just that I wasn’t following a smart program. I never tracked how much work I did, and I didn't progress my training. If you're not progressing your training, you won't be able to see results no matter whether you're using machines or free weights.

Great. What does any of this have to do with programming?

## You'll Never Build a Secure Website with PHP

The web is full of rants about the awfulness of PHP; perhaps the most famous is [PHP: a fractal of bad design](https://eev.ee/blog/2012/04/09/php-a-fractal-of-bad-design/), which leads with this colorful analogy:

> I can’t even say what’s wrong with PHP, because— okay. Imagine you have uh, a toolbox. A set of tools. Looks okay, standard stuff in there.
>
> You pull out a screwdriver, and you see it’s one of those weird tri-headed things. Okay, well, that’s not very useful to you, but you guess it comes in handy sometimes.
>
> You pull out the hammer, but to your dismay, it has the claw part on both sides. Still serviceable though, I mean, you can hit nails with the middle of the head holding it sideways.
>
> You pull out the pliers, but they don’t have those serrated surfaces; it’s flat and smooth. That’s less useful, but it still turns bolts well enough, so whatever.
>
> And on you go. Everything in the box is kind of weird and quirky, but maybe not enough to make it completely worthless. And there’s no clear problem with the set as a whole; it still has all the tools.
>
> Now imagine you meet millions of carpenters using this toolbox who tell you “well hey what’s the problem with these tools? They’re all I’ve ever used and they work fine!” And the carpenters show you the houses they’ve built, where every room is a pentagon and the roof is upside-down. And you knock on the front door and it just collapses inwards and they all yell at you for breaking their door.
>
> That’s what’s wrong with PHP.

I once worked as a developer on a legacy PHP codebase. Whenever my colleagues would get frustrated with the difficulty of working on this codebase, they'd reference the above article, or perhaps post a picture of the [double-headed hammer](https://blog.codinghorror.com/the-php-singularity/) created as a physical tribute to the analogy. I did too. It was frustrating to work on the project, and joking about it helped lighten the mood. We were struggling to make progress in the codebase because we had bad tools.

But looking back on that job, I'm less interested in the tools we used, and more in the house we built.

"Every room is a pentagon and the roof is upside-down." We didn't use a framework, at least not consistently; there were some Laravel bits in there, but structurally, the majority of the app hadn't changed since the early 2000s. There was no style guide, no automated tests, and inconsistent usage of functions--there might be a function to perform a common task defined in one section of the app, but half the pages that did that task would ignore that function and just reinvent the wheel with inline code blocks.

"And you knock on the front door and it just collapses inwards and they all yell at you for breaking their door." No automated tests meant that whenever you made a change, you had to hope whatever messing around you did in your local instance covered all the use cases. If bugs showed up in that section of the code, they would be blamed on whoever touched it last. Asking how to do something was often met with a shrug, or more jokes, or a rant about the foolishness of someone who no longer worked there.

It was easy to blame PHP for the awful legacy codebase. It was much easier than blaming ourselves.

## Power, Cultural Currency, Frustration, and Contempt

In her insightful talk, [When do we Belong?](https://www.youtube.com/watch?time_continue=1205&v=5RWBRrHxEhs), Aurynn Shaw talks about how [contempt culture](http://blog.aurynn.com/contempt-culture-2) plays out in conversations about certain languages and frameworks, and how this relates to power structures and the accessibility of information.

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/5RWBRrHxEhs?start=1167" frameborder="0" allowfullscreen></iframe>

> So let's go back to PHP. Why is PHP so hated? The major reason I'm always told is that it's insecure. The code is bad.
>
> But that's not the real reason. Instead let's go back to when I learned to code in the late 1990s. PHP was a few years old at this point but it was already eating a lot of developer mindshare for building websites, making it easier to get more people into programming. [...]
>
> But these people weren't coming from our existing communities. They didn't obey our existing power structures. They were newcomers, so PHP became not real.
>
> People who used it were excluded and told they weren't programmers--but these people still wanted to make things. The web was huge at that point, getting bigger, so they shared their code--code that didn't have habits that our communities considered secure or good--and so PHP earned a reputation of insecure or bad. Not because it was insecure or bad, but because the users were excluded from the communities. Which fulfills its own prophecy.

Here the opinion of the tool--PHP--is based not just in the qualities of the tool itself, but on where it fits in with the larger context of how it's being used. Except instead of an individual's strength training journey, it's the *field of web development as a whole*. And so the tool, and the way it's used, has larger repercussions than the individual using or not using it.

## A Caveat

None of what I'm writing here is intended as a defense of PHP, or of weight machines. None of the observations about how the larger programmer culture sees PHP will change the various inconsistencies in how PHP is designed. I don't like working with it much, myself, because my main experience with it involves an unpleasant legacy code base.

But a lot of my friends who work with PHP don't have those same associations with it, and will gladly use it for their personal projects. The [82% of the web running on PHP](https://w3techs.com/technologies/overview/programming_language/all) means that whatever you think about PHP--whether or not you'd choose it for your own work, given the choice--it's an important part of the web and it's not going away any time soon.

## Choice

"Given the choice" is important, here, and underlies a lot of the reasons PHP is such a common target for programmers' rants. It's also where my analogy with weight machines begins to fall apart. If you're strength training for fun, there's no reason you have to use weight machines if you don't want to. If you're a professional athlete, you probably have access to facilities with whatever kind of equipment you want.

If you're a programmer who *has* to use PHP at your job, your relationship with the tool is very different. Maybe you're working on a well-organized, well-documented codebase, and all the discussion about PHP's deficiencies is interesting, but your team has found ways to overcome them, using frameworks and stye guides consistently. Or maybe you're the senior developer, or even the only developer, on a legacy codebase, but you have a lot of leeway to refactor and test it--you're still dealing with the frustrations of a legacy codebase, but you're able to gradually overcome them.

But I suspect a lot of the folks who rant about the evils of PHP have, at some point in their life, found themselves in a position where they didn't have those options. When you're tasked with keeping a legacy project going but you don't have the time, resources, or buy-in from management you need to clean up a chaotic codebase, it's inevitable you'll get frustrated, and it's natural to look for someone or something to blame.

My theory is that PHP, out of all the various technologies that make up the infrastructure of the modern Web, attracts so much visceral hatred because people often interact with it in situations where they're powerless to fix the problems they face on a daily basis. And just like Adam wrote about blaming weight machines for their lack of progress when they were just starting out with strength training, programmers often blame PHP for their bad experiences on projects that have a number of cultural and institutional factors standing in the way of effective software development.

[Conway's Law](https://en.wikipedia.org/wiki/Conway%27s_law#cite_note-Conway-3) states that "organizations which design systems ... are constrained to produce designs which are copies of the communication structures of these organizations." ([Sarah Mei](https://twitter.com/sarahmei) first introduced me to this idea in her talk [Livable Code](https://www.youtube.com/watch?v=8_UoDmJi7U8), which shaped a lot of the thoughts I'm expressing here.) It would be an oversimplification to say that all the frustrations experienced by PHP programmers are a result of cultural dysfunction--but I do wonder how often vocal contempt for PHP is a way to displace frustration with the behavior of the people around us onto the tool we happen to be using.
