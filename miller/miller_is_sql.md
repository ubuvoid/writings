# Miller is SQL: Networking, Turing-Completeness, and 'The Expanse'.

### Corrolary: The Ring is XHR.

___

*Spoilers ahead for The Expanse, Season 3, Episode 10, "Dandelion Sky".*

Earlier this evening I got high and watched this TV show about superintelligent alien computers, and it gave me an idea for an analogy about Turing-Completeness and networking that seems like a very promising entry point to explore a computational theory book for a broad audience.

The show is called "The Expanse", based on a book series by Daniel Abraham and Ty Franck writing as James S. A. Corey. It concerns a technology that's discovered in an alien artifact orbiting Saturn. The technology is found by an Earth corporation, which dubs it "the protomolecule" and seeks to understand its potential as a weapon. They find it can't be contained, and unimaginable death occurs as a result. Eventually, the technology begins to develop its own intelligence, and builds a structure at the edge of the solar system. A ring.

What's on the other side of the ring, no one knows. Except...

James Holden, our protagonist and leader of our scrappy band of heroes, is approaching The Ring with his crew when he begins to see visions of his dead friend, Miller. Back in Season 2, Miller passed away averting a crisis related to the protomolecule, and it appears some essence of his consciousness has been absorbed by it.

At first, Miller only appears in brief flashes, speaking in fragments what appears to be gibberish. Then he disappears. And he only appears when Holden is completely alone. If anyone else approaches, walks into the room, even has a shot of seeing him, Miller vanishes.

So that's his source for clues about the alien artifact that is terrifying the entire solar system. Hallucinations of a dead friend.

There's something fascinating about their communications. Every time Miller appears, his memory is wiped. When prompted, he has access to memories from Miller's biological life, but no recollection of earlier appearances as a manifestation of the technology.

Which got me thinking.... it's almost like a timeout for an HTTP request.

Consider. A commonly accepted design pattern for HTTP servers is to treat requests in a stateless way, meaning the program that's running answering the request has no knowledge of any prior requests. That is, unless another program gives it that knowledge. This is how security vulnerabilities are limited -- stripping this program of its "memory" limits the possibilities for cumulative effects to linger and cause unwanted behavior.

When we want to get a full picture of a conversation between an HTTP server and a browser, we look at the logs, where a data artifact of each request is preserved. You can have a log on both ends of the connection, much like Holden can remember his previous conversations with Miller, and.... well, whatever's on the other end of Miller can remember what happened, too.

In the show, this becomes the basis for bootstrapping a process of building trust by testing information, asking questions only the real Miller or Holder would know the answer to. At the end of the episode, Miller and Holden make contact inside The Ring.

The Ring is shown to be some sort of limbo, or bubble. A pocket dimension, between realities. A place where humans and.... manifestations?.... can coexist and communicate, without consequences for their respsective subjective realities. A neutral meeting place. Kind of like a sandboxed execution environment on a web server. The client and the server can have a civilized conversation, both invoking Turing-complete processes.

Because at the end of the day, it's all about Turing-completeness.

\[end of intro]

----

Next steps: Types of languages, "degrees" of completeness. Disclaimer: I made up this entire framework out of thin air, but it seems plausible to me.

----

simplest category of languages: description.

"description languages" : includes idl's (proto, thrift, diana idl, corba, jsontypedef), markup languages, json, xml, html. abstract syntax trees. any language that specifically has no performing of verbs. no decisions, no actions. only descriptions of what is. (or what might be). see also, serialized representation of diana. grammars/language specifications. antlr.

----

category two: description, performance without choice.

ex: simple four-function calculator. '=' is 'perform'.

performance. that's the word. description and performance, with no choice or branching pathways.

----

third (boundary) category: description, performance, choice, with restrictions on repetition.

typically, small set of atomic actions. ex: traditional atomic SQL implementations (trivially extended to TC by adding 'while true', easy to accidentally make TC by adding convenience language features.)

---

turing completeness:

final category: description, performance, choice, unrestricted repetition. turing completeness. branching.

while true subtract and jump if less than zero -> sufficient for turing completeness ([i think.](https://en.wikipedia.org/wiki/One-instruction_set_computer#Subtract_and_branch_if_less_than_or_equal_to_zero))

sidebar: interesting relationship between dna and representation of single instruction set computer programs ex: subleq.

----

category 3 and category 4 are so similar as to be meaningfully indistinguishable.

category 3 is best described as a special case restricted execution of a turing complete language. justification: writing the words "while true:" before running the programming language's interpreter in shell will result in TC execution.

really, this leads us to conclude that there really is no meaningful 'without repetition' category at all, since repetition is the most basic element of a language. next time someone tries to tell you that SQL is "not" Turing-complete, send them to [this post](https://stackoverflow.com/a/71723783).

----

Bringing it back around:

At first, the protomolecule allows the Turing-complete process known as Miller's consciousness to operate in the same physical space as Holden within very strict and very specific operational and timing constraints. The reason is obvious -- Turing completeness is powerful, and if you place unwarranted trust in another Turing-complete process you're talking to, that process can hurt you in any number of ways. So in the show, as in reality, we execute our code in a sandbox.

As we gain confidence about our code and its provenance, we start running the code in bigger and bigger sandboxes. In the show, the biggest sandbox we see is the interior of The Ring itself, a neutral zone, a bubble separate from other realities, but one with a rich bandwidth of information into and out of it through controlled channels.

A little bit like running code as a trusted user rather than inside a Sawzall interpreter.

Of course, whatever side of the Ring you're on, it's all just one big interpreter at the end of the day.
