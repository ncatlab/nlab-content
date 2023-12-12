> This page is about an alternative presentation of [[monads]] as popular for [[monads in computer science]].  For a different notion of "extension system" (that is to a [[bicategory]] what a [[closed category]] is to a [[monoidal category]]) see instead at *[[closed category]]*.


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--


# Extension systems
* table of contents
{: toc}


## Idea
 {#Idea}

The notion of "*extension system*" ([Marmolejo & Wood (2010)](#MarmolejoWood10)), originally called "*[[algebraic theory]] in extension form*" ([Manes (1976), p. 32](#Manes76)) and previously also referred to as "*[[Kleisli triple]]*" ([Moggi (1991), Def. 1.2](#Moggi91)) is an equivalent way of presenting the [[mathematical structure|structure]] of a *[[monad]]* (on a [[category]]) that does not explicitly refer to [[composition]] ("iteration") of its [[underlying]] [[endofunctor]]. This is simpler for certain purposes, and in any case more natural for others, notably in the use of [[monads in computer science]]. Abstractly, the notion may be understood as specialising the definition of $J$-[[relative monads]] to the case where $J$ is the [[identity functor]]

Specifically, noticing that the [[endofunctor]] [[underlying]] a [[monad]] may be understood as constructing its [free algebras](algebra+over+a+monad#FreeAlgebras), which (lacking [[relations]]) tend to be "large" (say as concerns the [[cardinality]] of their [[underlying sets]]), the iterated application of this endofunctor produces ever larger objects, and some authors have pointed to avoiding this phenomenon as motivation for considering extension systems:

> {#MarmolejoWoodQuote} &lbrack;[Marmolejo-Wood 10](#MarmolejoWood10)&rbrack;: there is an important overarching reason to consider monads in this way. Extension systems allow us to completely dispense with the iterates $[$...$]$ of the underlying arrow. No iteration is necessary. A moment's reflection on the various terms of terms and terms of terms of terms that occur in practical applications suggest that this alone justifies the alternate approach. $[$...$]$ we note that extension systems in [[higher category theory|higher dimensional category theory]] provide an even more important simplication of monads. For even in dimension 2, some of the tamest examples are built on [[pseudofunctors]] that are difficult to iterate.

Major alternative motivation for extension systems comes from their understanding as [[monads in computer science]] ([[Kleisli triples]]); see there for more.

## Definition

An **extension system** ([Marmolejo-Wood 2010](#MarmolejoWood10)) on a [[category]] $C$ consists of

* For every [[object]] $A\in C$, an object $T A\in C$ and a [[morphism]] $\eta_A \colon A\to T A$, and

* For every [[morphism]] $f\colon B\to T A$ in $C$, a morphism $f^T \colon T B \to T A$ (the *Kleisli extension* of $f$), satisfying the following [[axioms]]:

  * For every $A$ we have $(\eta_A)^T = 1_{T A}$,

  * For every $f \colon B\to T A$, we have $f^T \circ \eta_B = f$, and

  * For every $f \colon B\to T A$ and $g:C \to T B$, we have $f^T \circ g^T = (f^T \circ g)^T$.

Given these data, we make $T$ a [[functor]] by $T f = (\eta_A \circ f)^T$, we define multiplication maps $\mu_A:T T A \to T A$ as $(1_{T A})^T$, and we verify that the result is a [[monad]].  Conversely, given a monad $(T,\eta,\mu)$, we define $f^T = \mu_A \circ T f$ and check the above axioms.  Thus, extension systems are [[equivalence|equivalent]] to monads.

### The Kleisli category

This presentation of a monad is especially convenient for defining the [[Kleisli category]] $C_T$ (whence the aternative terminology "[[Kleisli triple]]"): 

its objects are those of $C$, its morphisms $B\to A$ are the morphisms $B\to T A$ in $C$, and the composite of $f:B\to T A$ with $g:C \to T B$ is $f^T \circ g$.

### The category of algebras

It is also possible to define [[algebras over a monad]] using this presentation.  A $T$-algebra consists of

* An object $B$, and

* For every morphism $h:X\to B$, a morphism $h^B : T X \to B$, such that

* For every $h:X\to B$ we have $h^B \circ \eta_X = h$, and

* For every $h:X\to B$ and $y:Y\to T X$ we have $h^B \circ y^T = (h^B \circ y)^B$.

### Strong monads

When $C$ is a [[cartesian closed category]], to make $T$ a [[strong monad]] we simply have to enhance the extension operation $(-)^T$ to an internal morphism $(T A)^B \to (T A)^{T B}$, or equivalently $T B \times (T A)^B \to T A$.  This morphism is known as "bind" in use of [[monads in computer science]].

## Related concepts

* [[monad in computer science]]

* [[relative monad]]

* [[polymonad]]

## References

The notion appears explicitly in:

* {#Manes76} [[Ernest G. Manes]], Sec 3, Ex. 12 (p. 32) of: *Algebraic Theories*, Springer (1976) &lbrack;[doi:10.1007/978-1-4612-9860-1](https://doi.org/10.1007/978-1-4612-9860-1)&rbrack;

and is expanded on considerably in

* {#MarmolejoWood10} [[Francisco Marmolejo]], [[Richard J. Wood]], *Monads as extension systems -- no iteration is necessary* [[TAC]] **24** 4 (2010) 84-113 &lbrack;[tac:24-04](http://www.tac.mta.ca/tac/volumes/24/4/24-04abs.html)&rbrack;

An earlier appearance in a different guise ("devices"):

* [[R. F. C. Walters]], Chapter I of: *A categorical approach to universal algebra*, Ph.D. Thesis (1970) &lbrack;[anu:1885/133321](https://openresearch-repository.anu.edu.au/handle/1885/133321)&rbrack;



The use of extension systems (there called [[Kleisli triples]]) as [[monads in computer science]] capturing [[computation]] with side effects is due to:

* {#Moggi91} [[Eugenio Moggi]], *Notions of computation and monads*, Information and Computation, **93** 1 (1991) &lbrack;<a href="https://doi.org/10.1016/0890-5401(91)90052-4">doi:10.1016/0890-5401(91)90052-4</a>, [pdf](http://www.disi.unige.it/person/MoggiE/ftp/ic91.pdf)&rbrack;

This way of presenting a monad is also closely related to [[continuation-passing style]], as described in

* [[Andrzej Filinski]], _Representing Monads_, POPL 1994. ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.43.8213&rep=rep1&type=pdf))


Generalization to [[pseudomonads]]:

* [[Francisco Marmolejo]], [[Richard J. Wood]], *Kan extensions and lax idempotent pseudomonads*, [[TAC]] **26** 1 (2012) 1-29 &lbrack;[26-01](http://www.tac.mta.ca/tac/volumes/26/1/26-01abs.html)&rbrack;

* [[Francisco Marmolejo]], [[Richard J. Wood]], *No-iteration pseudomonads*, [[TAC]] **28** 14 (2013) 371-402 &lbrack;[tac:28-14](http://www.tac.mta.ca/tac/volumes/28/14/28-14abs.html)&rbrack;


[[!redirects extension systems]]

[[!redirects Kleisli extension]]
[[!redirects Kleisli extensions]]


