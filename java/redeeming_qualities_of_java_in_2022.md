# Redeeming Qualities of Java in 2022

*Cross-posted from Stack Overflow.* *https://stackoverflow.com/a/71611139/18573935 . The question from DevelJoe, paraphrased, is: would Java be an appropriate language for cross-platform mobile app development? Originally posted 03/25/22.*

----

Post is a few months old now, but I figure someone with a similar question will probably find this with web search, so this reply is for them. *(Disclaimer: I wrote Java professionally for about five years, and I grew up when Java was supposed to be the future.)*

If the question is, "Can you write Java code and run it on iOS?" then the answer is, "Technically yes, but you almost certainly don't want to."

It requires jumping through all kinds of hoops and sleight-of-hand to make it work. The project linked in previous answer, Codename One, is a pretty heavyweight framework and the kind of thing you'd only want to use if you were heavily committed to a Java codebase already.

There are advantages to knowing Java in 2022, but cross-platform mobile development isn't one of them.

Some reasons why you might want to learn Java:
- Developing on Android. Android now supports/recommends Kotlin for new projects, but Java was the sole first-class language on the platform for 10+ years, so it's advantageous to be able to read/write/reuse Java code and libraries.
- Using long-standing big-data tools (spark, hadoop, neo4j, etc.). While this domain has increasingly moved to Python over the past 5-7 years, there's still a lot of production Java code that someone needs to maintain. *\[Edit 3/31/22: See also the Apache http server, whose name never sat right with me because as far as I know, the people who wrote it aren't Apache.]*
- Stylistic similarity to C-family languages. Java can be a more intuitive introduction to C-style languages than jumping right into, say C++. These days, though, I would recommend C# over Java since it's used in more domains.
- Continuity with some JS dialects. React code in particular is full of Object Oriented(tm) design conventions that are very strongly influenced by Java practices, and those design choices in turn have influenced changes in the JS spec. So being familiar with Java conventions can help make sense of that stuff. It can also help you identify which of those practices are bad ideas so you can avoid them in JS.


As far as reasons why you won't see widespread Java usage outside of those legacy domains, I'd say there are a lot of good reasons people have moved away from Java since 2006 or so:
- It's incredibly verbose, and requires a lot of esoteric knowledge about implementation details to write code that runs efficiently. This is the kind of problem that languages like Scala and Kotlin have tried to solve, while retaining compatibility with the JVM platform for ease of migration.
- The JVM platform itself introduces substantial overhead, both in resource usage and integration complexity.
- Changes in approach and policy since Sun's acquisition by Oracle. This is related to licensing issues (see Oracle v Google), as well as complexity/feature creep, which has given rise to compatibility issues across codebases.
- Emergence of viable alternative languages in the 2000's and 2010's.
- Widespread adoption of virtualization technology has yielded alternate ways to solve the compatibility issues that Java was designed to address.

It's ironic, since the motto of Java used to be "write once, run everywhere", but that's the way things go.

