
# Contents
* automatic table of contents goes here
{:toc}

## Definition

A [[monad]] $(T,\mu,i)$ on the category [[Set]] of sets, is __finitary__ (also called __algebraic__, although some people consider any monad to be an algebraic notion) if the underlying [[endofunctor]] $T:\mathrm{Set}\to\mathrm{Set}$ commutes with [[filtered colimits]]. 

In other words, an algebraic monad is a [[monoid]] in the category of algebraic endofunctors on $\mathrm{Set}$.


## Properties

A finitary monad $(T,\mu,i)$ is completely determined by its value on all finite [[ordinal]]s $n\in\mathbb{N}_0$ considered as standard [[finite set]]s.  $T(n)$ is then the set of $n$-ary operations.  The notion of algebraic monad is hence similar to the notion of a nonsymmetric [[operad]] in $\mathrm{Set}$, but it is not equivalent, because of the possibility of duplicating or discarding inputs.

More precisely, each finitary monad $T$ defines a [[Lawvere theory]] $Th_T$, namely $Th_T = Free_{fin}^{op}$ where $Free_{fin}$ is the category of [[free construction|free]] algebras $T(n)$ on finite sets (as a full subcategory of $Alg_T$). In fact, the two notions are equivalent: the assignment 

$$T \mapsto Th_T$$

defines an equivalence between the category of finitary monads on $Set$ and the category of Lawvere theories. Moreover, the category of $T$-algebras is equivalent to the [[category of models]] of $Th_T$. However, a technical advantage of Lawvere theories is that they can be interpreted in categories other than [[Set]]: a model of a Lawvere theory $\mathcal{T}$ in a category with cartesian products $C$ is just a product-preserving functor $\mathcal{T} \to C$. 


## Applications

There is an interesting commutativity condition singling out the subclass of commutative algebraic/finitary monads, cf. [[commutative algebraic theory]]; they are useful to establish a theory of [[generalized scheme after Durov|generalized commutative schemes]]. 


## References 

For a proof of the equivalence between finitary monads and Lawvere theories, see 

* J. Adamek and J. Rosicky, _Locally presentable and accessible categories_ (chapter 3), LMS Lecture Notes 189, Cambridge U. Press, 1994. 

Durov's application of finitary monads to the "field with one element" may be found in...


## Discussion

This discussion appeared when the page was at [[algebraic monad]].

+--{: .query}
[[Mike Shulman|Mike]]: Does anyone besides Durov use this terminology?  In category theory these already have two standard names: "finitary monads" and "(Lawvere) theories."

[[Zoran Škoda]] Lawvere theories are equivalent to algebraic monads, but not in standard exposition literally a type of monad, but one says algebraic monad when one really talks about a condition on monads. Algebraic monad is just a monoid in the category of algebraic endofunctors. Lawvere and others studied few variants of notion of algebraic functor, but in all of them algebraic functor commutes with filtered colimits, isn't it ? I heard the term certainly in a number of algebra talks before [[Nikolai Durov]]'s thesis (I can say some names but I may misremeber sources). Definitely the term is getting much more influential after the Durov's work, and reused by algebraic geometers now. He is quite familiar with Lawvere's work so I hope the related expression "algebraic endofunctor" is not chosen incompatibly. Also there is some parallel with terminology [[cartesian monad]]. But what do you think ?
In any case, one should also list term finitary monad, both synonyms should be listed.

_Toby_:  Whether these are 'algebraic' or 'finitary' (I\'d be more inclined to the latter, but not through any familiarity with the literature), they\'re not obviously the same as Lawvere theories.  I\'ve tried to indicate the connection, although (vague as my statement is) I\'m not even sure that it\'s correct!

[[Zoran Škoda]] added below redirect [[finitary monad]].

_Toby_:  I moved this to [[finitary monad]] now, after Zoran made a link to it using that name from [[generalized scheme after Durov|an article on Durov's work]].
=--


[[!redirects finitary monad]]
[[!redirects finitary monads]]
[[!redirects algebraic monad]]
[[!redirects algebraic monads]]
