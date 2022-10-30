A [[monad]] $(T,\mu,i)$ on the category of sets, is an __algebraic monad__, or __finitary monad__, if the underlying endofunctor $T:\mathrm{Set}\to\mathrm{Set}$ commutes with [[filtered category|filtered]] [[colimit]]s. In other words, an algebraic monad is a monoid in the category of algebraic endofunctors on $\mathrm{Set}$.

Algebraic monad $(T,\mu,i)$ is completely determined by its value on all finite ordinals $n\in\mathbb{N}_0$ considered as standard [[finite set]]s.  $T(n)$ is then the set of $n$-ary operations.  The notion of algebraic monad is hence similar to the notion of a nonsymmetric [[operad]] in $\mathrm{Set}$, but it is not equivalent, because of the possibility of duplicating or discarding inputs.

An algebraic monad defines a [[Lawvere theory]], which can then be interpreted in categories other than [[Set]].

+--{: .query}
[[Mike Shulman|Mike]]: Does anyone besides Durov use this terminology?  In category theory these already have two standard names: "finitary monads" and "(Lawvere) theories."

[[Zoran Škoda]] Lawvere theories are equivalent to algebraic monads, but not in standard exposition literally a type of monad, but one says algebraic monad when one really talks about a condition on monads. Algebraic monad is just a monoid in the category of algebraic endofunctors. Lawvere and others studied few variants of notion of algebraic functor, but in all of them algebraic functor commutes with filtered colimits, isn't it ? I heard the term certainly in a number of algebra talks before Durov's thesis (I can say some names but I may misremeber sources). Definitely the term is getting much more influential after the Durov's work, and reused by algebraic geometers now. He is quite familiar with Lawvere's work so I hope the related expression "algebraic endofunctor" is not chosen incompatibly. Also there is some parallel with terminology [[cartesian monad]]. But what do you think ?
In any case, one should also list term finitary monad, both synonyms should be listed.

_Toby_:  Whether these are 'algebraic' or 'finitary' (I\'d be more inclined to the latter, but not through any familiarity with the literature), they\'re not obviously the same as Lawvere theories.  I\'ve tried to indicate the connection, although (vague as my statement is) I\'m not even sure that it\'s correct!

[[Zoran Škoda]] added below redirect [[finitary monad]].

=--

[[!redirects finitary monad]]