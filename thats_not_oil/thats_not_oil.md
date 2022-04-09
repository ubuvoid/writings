# That's Not Oil, That's Blood

### An organizing metaphor for circulation in distributed systems.

---

*And there's nothin' left but some blood where the body fell  
That is, nothin' left that you could sell  
Just junk all across the horizon, a real highwayman's farewell  
And I said, "Hey kid, you think that's oil? Man, that ain't oil, that's blood"  
I wonder what he was thinking when he hit that storm  
Or was he just lost in the flood?*

 \- Song by Bruce Springsteen
 
---

// Changelog:

// 2022/04/03: Establish title and gimmick.

// TLDR, traditional object-oriented models tend to develop blood clots. Data needs to circulate just like blood, or the system collapses under its own weight.

// 2022/04/08:

New direction for this piece. I have the perfect poster child. It's called Fling SDK, aka Whisperplay, aka Thrift FireOS, and I helped write it between 2013 and 2016. It was an ingeneous design for the time, and a truly clever feat of product engineering. The whole idea can be summed up as, "five features for the price of one." You build one communication library to get FireOS Stuff and Companion Apps talking other FireOS Stuff, in a year when they planned to release A Lot of it. Then, every single app that uses it looks like a new killer feature instead of simply an application calling an API.

So Whisperplay was well equipped to fulfill the immediate project goals of selling FireTVs and getting the engineers promoted. Where it fell short, in hindsight, was longevity. The design, in practice, ended up being too complicated for the engineering team to reason about succinctly, so the code became hard to maintain, and so on. We've all been there, and it's a natural property of software systems.

I was reflecting on the various distributed systems I've had a hand in implementing over the years, and it occured to me that I should do a web search for ["site:stackoverflow.com whisperplay"](https://www.google.com/search?q=site:stackoverflow.com%20whisperplay) to see if anyone was still using this thing in 2022. Findings: the top three results were all stack traces that no one on the internet seems to know how to debug, and users report a severe lack of functioning on Android 11. This experience has led me to create the very first [Unofficial Whisperplay/Fling Helpline](https://github.com/Unofficial-Whisperplay-Fling-Helpline/wp/issues/1), a crisis center for those in need, as a way of giving back to my community. Think of it like the twenty-five cent psychiatry booth from the Peanuts cartoons.

I think the decisions we made on that project were reasonable and defensible, for the most part, along the way. Where we faltered was in the execution. The short version is that when we implemented this system, we believed the lies we were taught in school about Object oriented Programming being the future. And we wrote it in Java.

If you were working in corporate software development in the 2000's through 2010's, you've probably been here before. If you weren't, let's just say it was a long road and at the end of it was a great big brick wall waiting to be slammed into. 

What happened was, in JavaSchool, they told us it was Good Practice to copy your objects for no reason, other than that you got bored while you were writing the program. This is a property of Java that made it fun and approachable for demos in the mid-90's, but it results in exceptionally poor-performing software.

The reason has to do with memory locality. In the mid 90's, home computers were largely CPU-bound. This as the era of the early Pentium models and the bizarre [proto-Daft Punk marketing campaign](https://www.youtube.com/watch?v=es_YbDQnTqo) that would take the world by storm. Contemporary processor architectures have different properties. Since most CPU's are multi-core, operations are now IO bound, meaning the processor spends most of its time waiting for information to be read from or written out to main memory. 

If you've never done real-time systems programming, it can be hard to appreciate just how much slower main memory is than L1 or L2 cache. The difference is orders of magnitude, and the single biggest bottleneck for performance on contemporary CPUs is unnecessary cache misses in memory due to data being scattered randomly around the memory bank rather than in a nice compact unit.

Guess what happens when you allocate objects willy-nilly just because you're bored. You make a lot of random garbage in random corners of your computer. Somebody has to keep track of all that garbage, and by using Java you've implicitly agreed it's not gonna be you so the computer had better get to work.

So take that problem, and multiply it by itself, because in this same system, we were also integrating with Thrift, a library from Facebook developed for a similar purpose but with totally different operational requirements, that none of us had used before, and which was barely documented outside of a paper that was [published on April Fool's Day](../april/thrift.md) and a website called [Thrift: The Missing Guide](https://diwakergupta.github.io/thrift-missing-guide/).

Here's the astonishing thing: it actually worked well enough to ship five features at once, and we did actually get our engineers promoted, so the project was a success by the metrics that really matter in Silicon Valley. That's because the organizing effect of using an IDL like Thrift as the backbone of a code base is a fundamentally solid structure that is very, very, very difficult to fuck up, even if you're using an IDL that is as hastily engineered as Thrift. Now you can appreciate how Facebook got so big.

But none of us had ever used anything remotely like Thrift before, and we certainly hadn't used it to pass messages back and forth between servers in a datacenter, which was what Facebook built it for. So when Thrift was sending messages back and forth, we didn't see them as messages that needed to circulate. We saw them as Objects. And in Java, Objects are something we Own and Hold On To.

So the system held on to copies of all these messages that it was sending and receiving, because it was worried about corrupting the original message, which it also wanted to hold onto in memory for some reason (it was inside an Object, after all).

Instead of seeing the messages as blood cells circulating through a system, we saw them as material wealth to hoard. And the system collected more and more of these messages, using more and more threads to allocate more and more memory, until the Core Service capped out at around half the memory on the entire FireTV.

Because we didn't respect that blood must be circulated, our system was prone to blood clots.

In short, we forgot the memorable Springsteen lyric quoted above. This is my advice to aspiring distributed systems developers:

*That's Not Oil, That's Blood.*

Blood and Oil, two things that even people who run corporations understand. Capitalism is, and always has been, predicated upon obscuring the difference between the two. The blood on the gears, the oil that's burned to turn them, the blood that's spilled to claim the oil. And so on, an unending chain of references, like a stray Java object that just keeps hanging on when the heap scanner comes knocking.

No Blood For Oil?

NO! Blood for Oil!

If any of this makes sense to you, it's because you grew up at a time in history that made absolutely no sense. I'm the same way, I was there. Fortunately for us, given the way things are going, we're gonna fit right in.

It's starting to get warm in here. Don't get lost in the flood.

\- Dana E. Anderson

---

*Dana E. Anderson is a liberated ex-borg and erstwhile correspondent reporting from the heart of the twenty-first century bullshit machine on unceded, occupied Ohlone land.*
