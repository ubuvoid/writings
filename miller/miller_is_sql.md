Miller is SQL.

Corrolary: The Ring is XHR.

Earlier this evening I got high and watched this TV show about superintelligent alien computers, and it gave me an idea for an analogy about Turing-Completeness and networking that seems like a very promising entry point to explore a computational theory book for a broad audience.

The show is called "The Expanse", and it concerns a technology that's discovered in an alien artifact orbiting Saturn. The technology is discovered by an Earth corporation, which dubs it "the protomolecule" and seeks to understand its potential as a weapon. They find it can't be contained, and unimaginable death occurs as a result. Eventually, the technology begins to develop its own intelligence, and builds a structure at the edge of the solar system. A ring.

What's on the other side of the ring, no one knows. Except...

Our protagonist James Holden, scrappy ragtag captain with a heart of gold, is approaching The Ring in a spaceship, and begins to see visions of his dead friend, Miller. Miller passed away averting a crisis related to the protomolecule, and it appears some essence of his consciousness has been absorbed by it.

At first, Miller only appears in brief flashes, speaking in fragments what appears to be gibberish. Then he disappears. And he only appears when Holden is completely alone. If anyone else approaches, walks into the room, even has a shot of seeing him, Miller vanishes.

So that's his source for clues about the alien artifact that is terrifying the entire solar system. Hallucinations of a dead friend.

There's something fascinating about their communications. Every time Miller appears, his memory is wiped. When prompted, he has access to memories from Miller's biological life, but no recollection of earlier appearances as a manifestation of the technology.

Which got me thinking.... it's almost like a request timeout for an HTTP request.

Consider. A commonly accepted design pattern for HTTP servers is to treat requests in a stateless way, meaning the program that's running answering the request has no knowledge of any other requests. That is, unless another program gives it that knowledge. This is how security vulnerabilities are limited -- stripping this program of its "memory" limits the possibilities for cumulative effects to linger and cause unwanted behavior.

When we want to get a full picture of a conversation between an HTTP server and a browser, we look at the logs, where a data artifact of each request is preserved. You can have a log on both ends of the connection, much like Holden can remember his previous conversations with Miller, and.... well, whatever's on the other end of Miller can remember what happened, too.

In the show, this becomes the basis for bootstrapping a process of building trust by testing information, asking questions only the real Miller or Holder would know the answer to. At the end of the episode, Miller and Holden make contact inside The Ring.

The Ring is shown to be some sort of limbo, or bubble. A pocket dimension, between realities. A place where humans and.... manifestations?.... can coexist and communicate, without consequences for their respsective subjective realities. A neutral meeting place. Kind of like a sandboxed execution environment on a web server. The client and the server can have a civilized conversation, both invoking Turing-complete processes.

Because at the end of the day, it's all about Turing-completeness.

\[end of intro]
