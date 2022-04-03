# Turing's Completeness Theorem and the Insufficiency of Logic

#### Very short version:

* Martin Davis is right and David Hilbert was wrong.
* 11/30/1936: The day A.M. Turing owned David Hilbert with Hilbert's own logic. ("On Computable Numbers, with an Application to the Entscheidungsproblem"; "The Deciding Problem").
* An Astonishing Coincidence: Independent discovery of lambda calculus by Church group.
* Godel's Influence on Turing and Lambda, opposition to Hilbert.
* It's beautiful because it's obvious.
* Wittgenstein's influence on Turing, and Turing's critique of Wittgenstein.

#### Slightly less short version:

Martin Davis is right and David Hilbert was wrong.

It's 11/30/1936.

David Hilbert has just become the first person in recorded history to actually be owned by their own logic, as this is the date A.M. Turing published "On Computable Numbers, with an Application to the Entscheidungsproblem."

The paper, which runs 36 pages including an appendix, describes the model of universal computing which would come to be known as the Turing Machine and serves as the basis for computer science as we know it, both theoretical and practical. Turing specifically wrote "On Computable Numbers" to demonstrate that David Hilbert was wrong about a core problem of philosophy (literally, "The Deciding Problem"). You will observe that very few people born after 1936 call themselves logicians. Turing was 24 years old.

Roughly speaking, the "Deciding Problem" as Hilbert understood it is a close cousin of those logic puzzles about soldiers who only lie or only tell the truth. It asks: is there a set of logical axioms from which it's possible to derive complete and total knowledge of the entire universe at once?

The answer, obviously, is no. But try telling that to David Hilbert.

*\[Sidebar: an effective resource for understanding Turing's Completeness Theory aka The Church-Turing Thesis is "Turing's Vision: The Birth of Computer Science" by Chris Bernhardt. While it perpetuates US academic misconceptions about Turing as an abstract mathematician rather than an implementer, the writing and examples are clear and crisp. This is the book I'd use to teach an undergrad theory class.]*

This event is also the occasion of the most astonishing coincidence I am aware of in recorded history.

Simultaneously, on the other side of the Atlantic ocean, an independent group working at Princeton University under the stewardship of Alonzo Church developed the lambda calculus, an alternate model of univeral computation which inspired the LISP family of programming languages.

Both Turing and the Lambda group were influenced by Godel's work on the legendary Incompleteness Theorem, which demonstrates that Hilbert's project to logically derive complete world knowledge is impossible. But, like a religious devotee seeing a comet narrowly miss the earth, Hilbert was only made more stubborn by Godel's refutation.

It became clear that in order to demonstrate that someone is as colossally wrong as David Hilbert was, you need a colossally persuasive argument. Turing was able to provide one. Whereas Godel's proved that Hilbert's framework was insufficient to define all computations possible in the universe, Turing's follow-up goes one step further and actually provides a mathematical model for determining whether a mathematical problem is solveable within the constraints of our universe.

Church's group published first, so it was on Turing to prove that the two models of computation are mathematically equivalent. And they are. They're exactly the same. And they both say that certain problems are undecidable, and they both agree that Hilbert's "Deciding Problem" is in fact one of them. Which is fortunate, because that sounds obvious. That's the appendix to "On Computable Numbers" mentioned earlier. It runs two and a half pages.

Turing and the Lambda group both positioned their models in direct opposition to Hilbert's, and as direct follow-ups to Godel. So now we ask ourselves... What's more likely: one, that two independent groups on opposite sides of an ocean delivered the same theory of universal computation, and yet this universal theory was wrong; or two, that David Hilbert was an idiot?

This points us to the most beautiful thing about computer science, or the theory of completeness: it seems obvious.

And Turing proved definitively in 1936, in black and white for the whole world to see, that in this case, the thing that seems obvious is actually true. 

Because everyone who has ever taken to heart a bit of folk wisdom knows that certain things are obvious. And one of the most obvious things in the world is that you can't know everything all at once. But some people, like David Hilbert, just couldn't accept that.

Did you know that Turing was a student of Wittgenstein, and that transcipts of their conversations during lectures are preserved in the historical record? Wittgenstein argues at length against Hilbert's worldview, in part on the grounds that it's obviously wrong. However, since Wittgenstein is lacking the domain knowledge to distinguish between Hilbert's model and the model proposed by Godel/Turing/Church/Kleen/et al., he puts Turing in the rhetorical position of defending Hilbert, a role Turing is entirely unwilling to perform. Their back-and-forths are truly enlightening. You can find more details about this, and quotations at length, in David Leavitt's "The Man* \[[sic](../protomolecule/index.md)] Who Knew Too Much: Alan Turing and the Invention of the Computer".

So, with Turing, Church, Kleene, Rosser, Davis, Godel, *and* Wittgenstein are all on one side, and David Hilbert alone on the other... Are you really willing to go to bat for David Hilbert? And if so, why?
