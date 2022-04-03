# The April Fools Paper: Thrift, Proto, and the Making of the Modern Cloud.

*Originally posted 2022/04/02*

Happy 15th birthday to the [Thrift whitepaper](https://thrift.apache.org/static/files/thrift-20070401.pdf). Back then, we didn't understand why you were published on April 1. We get it now.

Since its publication on April 1, 2007, the technical paper "Thrift: Scalable Cross-Language Services Implementation" by employees of Facebook has served as a touchstone for developers of distributed systems at scale, influencing architectures at Amazon, Twitter, Uber, and elsewhere. Despite this, the paper remains mysteriously opaque. It's clear *what* they're talking about, but why are they talking about it? And why don't they cite any of their sources?

Well, it's kind of a funny story.

If you're not in on the joke, here's the short version.

- In 2005, Google published a paper where it described its then-proprietary IDL, Protocol Buffers. The paper, which has become known as the [Sawzall paper](https://static.googleusercontent.com/media/research.google.com/en//archive/sawzall-sciprog.pdf), ostensibly exists to describe a query language named after a circulating saw, but in passing outlines the core organizational gimmick of Google's code base: schemas are defined in a non-TC IDL hooked up to a code generator which populates templates for N target languages. The design goal is to automate the error-prone labor of serializing and deserializing objects in code. Crucially, the same IDL and library are applied to both to messages at rest and in transit. I am not personally aware of any implementation of this gimmick earlier than 2001, but I would love to be proven wrong. For small projects looking to take advantage of this organizational srategy, I recommend [JSON Typedef](https://jsontypedef.com/), a lightweight implementation with a minimum of baggage.
- In 2006-07, some people Facebook poached from Google re-implemented the exact same gimmick and called it Thrift.
- The Thrift paper was published on 04/01/2007 as a means of providing Facebook legal cover. That's why the abstract features this bizarre sentence: "\[This paper] is not intended to be taken as research, but rather it is an exposition on what we did and why."
- Google, re-evaluating its strategic position amidst the complete meltdown of the world financial system, released Protocol Buffers as an open-source project on 07/07/08. At first, this sounds like a day when you'd be feeling lucky, until you consider that 07/07/08 is *not* a desirable combination on a slot machine.
- Facebook, in turn, open-sourced Thrift just in time for Christmas in 2009.
- And at this point in the story, I'm beginning to suspect that Mark Zuckerberg is trying to trick me. And if I really think about it, it becomes clear that a Turing-complete process like Mark Zuckerberg would find the idea of publishing this paper on April Fool's absolutely hilarious. And when I think of someone like Mark Zuckerberg laughing, I get afraid.

And that's why it's called Thrift. Cause they got it for cheap.

Upon Thrift's release, it became practical to build a Google Maps-scale website with exclusively open source software. This led directly to the proliferation of large-scale startups such as Uber and Lyft in the early 2010s.

It's stories like these that have taught me to view open-source releases with scrutiny and to read between the lines.

*Post-script: in 2013, my team at Amazon introduced Thrift into the FireOS codebase. We used the Thrift whitepaper extensively as a source of documentation, and none of us ever thought twice about why the paper was published on April 1. We really should have been suspicious, though, since the second-best source of documentation for Thrift after the whitepaper is called [Thrift: The Missing Guide](https://diwakergupta.github.io/thrift-missing-guide/). As an aside, Thrift FireOS is essentially impossible to migrate away from, and to this day, the FireTV [won't even start](https://github.com/esc0rtd3w/firestick-loader/blob/230804f2480693604146a936fbb533a918dbcdb4/scripts/debloat/bloat-remove.sh#L985) if you delete the package that contains the Thrift server.*
