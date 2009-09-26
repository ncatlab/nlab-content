__Note.__  I was going to go with "The Fruit of Our Purloins", but I rechnen this is more succinct.  The way I usually start an inquiry like this is just to collect a sample of source materials that seem like they belong together.  Still traveling, so this will be sporadic at first.  ---[[JA]]

* Aristotle, _[Categories](http://ebooks.adelaide.edu.au/a/aristotle/categories/)_

* Kant

* C.S. Peirce, "[On a New List of Categories](http://www.cspeirce.com/menu/library/bycsp/newlist/nl-frame.htm)"

* Carnap, _[The Logical Syntax of Language](http://books.google.com/books?id=Yf9R6WFFLhYC&printsec=frontcover)_, _cf._ "[Functor](http://books.google.com/books?id=Yf9R6WFFLhYC&printsec=frontcover#v=onepage&q=Functor&f=false)"

# Discussion #

[[Todd Trimble]]: Can I ask what you mean when you call these "precursors"?

[[JA]]:  Anticipations, 4-runners, 4-shadowings, philosophical underpinnings &#8230;

_Toby_:  If I may presume to translate Todd\'s question for him:  Why do you think that Aristotle, Kant, Peirce, and Carnap are precursors, anticipations, forerunners, foreshadowings, or philosophical underpinnings of category theory?  The only thing that I can think of myself is that Eilenberg & Mac Lane borrowed the term 'category' from Aristotle & Kant and borrowed the term 'functor' from Carnap.  Otherwise, I do not see any connection.

However, I don\'t object to this list; it might or might not work better on a separate page (although it\'s short enough that it fits here well enough).  I just changed its heading to something that seems more appropriate to me. 

_Todd_: Yes, I thought what Jon wrote might have been what he had in mind (but I didn't want to put words in his mouth, so I left the question open-ended), and then what Toby wrote would have been my follow-up question. Mind you, I am open to the suggestion that there may be philosophical antecedents or anticipations of the notion of category in these earlier developments (and I'd find that very interesting), but it's not clear to me how that would be the case in any precise sense. I think Toby's recasting this as 'Etymology' is far safer, until more evidence is brought to the table.

[[JA]]: I don't think that E & MacL were simply punning, but I doubt if it's necessary to take up more space here, as this page already bogs down my connection.  Just for one thing to think about, though, you might reflect on the question of "natural kinds", and the part that it played in the thought of Aristotle, Kant, and Peirce. 

_Todd_: It's clear enough (especially in view of examples of 'large categories' which consist of various species of structured sets) that "categories" was not an altogether inappropriate choice of word, but that's speaking at a pretty broad philosophical level. The more specific sense of category as involving morphisms and their compositional algebra is a different matter. It's not clear (to me, yet) that the germ of any such sense can be traced to any of the aforementioned authors; IMO a more convincing precursor in this wise might be Klein's Erlangen Program. 

As for "functor": it's even less clear to me that there was any tight connection in Mac Lane's mind between Carnap's use and his (Mac Lane's) own appropriation. I suspect that it was meant more to conjure an association with "function" than with Carnap particularly.

[[JA]]: Brother, can you paradigm ...

> __Paradigm.__  The basic idea of category theory is to shift attention from the study of [[object]]s to the study of _maps_ or _relations_ between objects: of (homo)[[morphism]]s between objects.

See also:

1. Aristotle's "[Paradeigma](http://mywikibiz.com/Inquiry#Analogy)", or reasoning by analogy.  Analogies and metaphors are kissing cousins to morphisms.
1. Peirce's "[Pragmatic Maxim](http://knol.google.com/k/jon-awbrey/pragmatic-maxim/3fkwvf69kridz/6)", which has to do with clarifying concepts by translating them into their operational meanings.

_Todd_: Ah, thanks for drawing attention to this! Now the argument becomes rather more interesting for me. 

In particular, the diagram you drew in your wiki under 'analogy' (speaking to an example from Aristotle) is a perfect concrete illustration of the mathematical notion of [[span]]; even better, you've drawn a _morphism_ of spans (from A to B). Now it happens that a category can be defined as a monoid in the bicategory of spans; if $C_0$ denotes the collection of objects and $C_1$ the collection of morphisms of a category $C$, then the span has the shape 

$$\array{
& C_1 & \\
 dom \swarrow & & \searrow cod\\
C_0 & & C_0
}$$ 

I'll also mention that the connection between analogies and spans has come up in discussion on the blog; our good friend Jim Dolan has drawn attention to this. See Toby's comment [here](http://golem.ph.utexas.edu/category/2006/11/a_categorical_manifesto.html#c006085) and the ensuing discussion. 


