# Turing's Completeness Theorem and the Insufficiency of Logic

#### Very short version:

* Martin Davis is right and David Hilbert was wrong.
* 11/30/1936: The day A.M. Turing owned David Hilbert with Hilbert's own logic. ("On Computable Numbers, with an Application to the Entscheidungsproblem"; "The Deciding Problem").
* An Astonishing Coincidence: Independent discovery of lambda calculus by Church group.
* Turing's model is discrete, and so is our universe.
* Godel's Influence on Turing and Lambda, opposition to Hilbert.
* It's beautiful because it's obvious.
* Wittgenstein's influence on Turing, and Turing's critique of Wittgenstein.

#### Slightly less short version:

It's 11/30/1936.

David Hilbert has just become the first person in recorded history to actually be owned by their own logic, as this is the date A.M. Turing published "On Computable Numbers, with an Application to the Entscheidungsproblem."

The paper, which runs 36 pages including an appendix, describes the model of universal computing which would come to be known as the Turing Machine and serves as the basis for computer science as we know it, both theoretical and practical. Turing specifically wrote "On Computable Numbers" to demonstrate that David Hilbert was wrong about a core problem of philosophy (literally, "The Deciding Problem"). You will observe that very few people born after 1936 call themselves logicians. Turing was 24 years old.

Roughly speaking, the "Deciding Problem" as Hilbert understood it is a close cousin of those logic puzzles about soldiers who only lie or only tell the truth. It asks: is there a set of logical axioms from which it's possible to derive complete and total knowledge of the entire universe at once?

The answer seems like it should be: "obviously, no." But then, not everything that seems obvious is true and not everything that's true is obvious. But Turing's paper, despite all expectations, actually proves in this case that the obvious is correct, and the enterprise which became known as "Hilbert's Project" cannot be fulfilled in our universe.

*\[Sidebar: an effective resource for understanding Turing's Completeness Theorem aka The Church-Turing Thesis aka the Fundamental Theorem of Computer Science, is "Turing's Vision: The Birth of Computer Science" by Chris Bernhardt. While it perpetuates US academic misconceptions about Turing as an abstract mathematician rather than an implementer, the writing and examples are clear and crisp. This is the book I'd use to teach an undergrad theory class.]*

This event is also the occasion of the most astonishing coincidence I am aware of in recorded history.

Simultaneously, on the other side of the Atlantic ocean, an independent group working at Princeton University under the stewardship of Alonzo Church developed the lambda calculus, an alternate model of univeral computation which inspired the LISP family of programming languages.

Both Turing and the Lambda group were influenced by Godel's work on the legendary Incompleteness Theorem, which demonstrates that Hilbert's project to logically derive complete world knowledge is impossible. But, like a religious devotee seeing a comet narrowly miss the earth, Hilbert was only made more stubborn by Godel's refutation.

It became clear that in order to demonstrate that someone is as colossally wrong as David Hilbert was, you need a colossally persuasive argument. Turing was able to provide one. Whereas Godel's proved that Hilbert's framework was insufficient to define all computations possible in the universe, Turing's follow-up goes one step further and actually provides a mathematical model for determining whether a mathematical problem is solveable within the constraints of our universe.

That's a bold claim, so it's worthwhile to elaborate on what I mean by "the constraints of our universe." Specifically, Turing's model of computation, following from Cantor, presents a **discrete time-step** model of computation, where information can be represented by a **countably infinite set of discrete symbols**. *\[TODO: Find OCN quote where Turing shuts down 'but what if we write a smaller symbol on the paper' argument]*.

These two constraints happen to align with every experimental result we have from the field of quantum mechanics, which is just too big a coincidence to overlook. I have no opinion on whether our universe is "a simulation", but it's a mathematical fact that **our universe is simulatable**, and it can be simulated with the Turing model of universal computation. Which is good, because that seems like it should be obvious.

*\[TODO: Find someplace to note Hilbert's diverging interpretation of Cantor, which seems like the root cause of the schism. In OCN, Turing highlights a specious argument based on a misapplication of the diagonal proof, and demonstrates that the proper application of the diagonal argument supports the paper's central claim. Seems like a good start.]*


*\[Sidebar 2022/04/05: Thinking more about the divergence of interpretation in the context of a discrete vs continuous universe. It occured to me that Turing never knew a world before Einstein published his results on the photoelectric effect. Hilber was already an adult when these observations were recorded. That means Turing's brain and Hilbert's brain were trained to build intuition based on a different set of heuristics from one another. In this light, it's easy to understand how the two would form opposing interpretations. There's a comparison to be made to the way early 21st century commentators describe "digital natives." Turing's native scientific language centered quantum mechanics; Hilbert's didn't.]*

Church's group published first, so it was on Turing to prove that the two models of computation are mathematically equivalent. And they are. They're exactly the same. And they both say that certain problems are undecidable, and they both agree that Hilbert's "Deciding Problem" is in fact one of them. Which is fortunate, because that sounds obvious. That's the appendix to "On Computable Numbers" mentioned earlier. It runs two and a half pages.

Turing and the Lambda group both positioned their models in direct opposition to Hilbert's, and as direct follow-ups to Godel. So now we ask ourselves... What's more likely: one, that two independent groups on opposite sides of an ocean delivered the same theory of universal computation, and yet this universal theory was wrong; or two, that David Hilbert was sorely mistaken?

This points us to the most beautiful thing about computer science, or the theory of completeness: it seems obvious.

And Turing proved definitively in 1936, in black and white for the whole world to see, that it doesn't just *seem* obvious, it actually *is*.

Because everyone who has ever taken to heart a bit of folk wisdom knows that certain things are simply undeniable. And one of the most undeniable propositions in the world is that you can't know everything all at once. But some people, like David Hilbert, just couldn't accept that.

Did you know that Turing was a student of Wittgenstein, and that transcipts of their conversations during lectures are preserved in the historical record? Wittgenstein argues at length against Hilbert's worldview, in part on the grounds that it's obviously wrong. However, since Wittgenstein is lacking the domain knowledge to distinguish between Hilbert's model and the model proposed by Godel/Turing/Church/Kleen/et al., he puts Turing in the rhetorical position of defending Hilbert, a role Turing is entirely unwilling to perform. Their back-and-forths are truly enlightening. You can find more details about this, and quotations at length, in David Leavitt's "The Man* \[[sic](../protomolecule/index.md)] Who Knew Too Much: Alan Turing and the Invention of the Computer".

So, with Turing, Church, Kleene, Rosser, Davis, Godel, *and* Wittgenstein all on one side, and David Hilbert alone on the other... Are you really willing to go to bat for David Hilbert? And if so, why?
