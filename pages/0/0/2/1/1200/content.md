
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--



# Ordinal numbers
* table of contents
{: toc}

## Idea

The _ordinal numbers_ (or just _ordinals_) constitute a generalisation of a [[natural numbers]] to [[numbers]] of possibly infinite magnitudes.  Specifically, ordinal numbers generalise the concept of 'the next number after ...' or 'the index of the next item after ...'.  In particular, the next number after the natural numbers is the first infinite ordinal number.


## Definition

Na&#239;vely, an **ordinal number** should be an [[isomorphism]] class of [[well-ordered sets]], and the **ordinal rank** of a well-ordered set $S$ would be its isomorphism class.  That is:

1. every well-ordered set has a unique ordinal number as its ordinal rank;
1. every ordinal number is the ordinal rank of some well-ordered set;
1. two well-ordered sets have the same ordinal rank if and only if they are isomorphic as well-ordered sets.

Then a **finite ordinal** is the ordinal rank of a [[finite set]], while an **infinite ordinal** or **transfinite ordinal** is the ordinal rank of an [[infinite set]].  (If you interpret both terms in the strictest sense, then there may be ordinals that are neither finite nor infinite, without some form of the [[axiom of choice]]).

Taking this definition literally in material [[set theory]], each ordinal is then a [[proper class]] (so one could not make further sets using them as elements).  For this reason, in axiomatic set theory one usually defines an ordinal number as a particular representative of this equivalence class.  One particularly slick definition is due to von Neumann:

* An __ordinal__ is a [[transitive set|transitive]] [[pure set]] $X$ which is [[well-ordered]] by the membership relation $\in$.  Then the __ordinal rank__ of a well-ordered set $S$ is the unique ordinal number that is isomorphic (as a well-ordered set) to $S$; it is a theorem that this exists, satisfying (1--3).

These pure sets are the __von Neumann ordinals__.  In the presence of the [[axiom of foundation]], $\in$ is automatically a [[well-founded relation]], so it suffices to require that $\in$ be a [[transitive relation]] on $X^+ = X \cup \{X\}$.

In the appendix of [[John Kelley]]'s topology textbook, ordinals are defined as:

* An __ordinal__ is a class $X$ such that every element of $X$ is a subset of $X$ and for all $A,B \in X$, either $A \in B$, $B \in A$ or $A=B$.  

It is later proven that in the axiomatic setting of the appendix ([[Morse-Kelley set theory]]), ordinals are sets.

From the perspective of structural [[set theory]], it breaks the [[principle of equivalence]] to care about distinctions between [[isomorphism|isomorphic]] [[objects]], and unnecessary to insist on a canonical choice of representatives for isomorphism classes.  Therefore, from this point of view it is natural to simply say:

* An __ordinal__ is a [[well-ordered set]].

However, one still may need sets of ordinals, that is sets that serve as the target of an ordinal rank function satisfying (1--3) on any (small) collection of well-ordered sets.  One can construct this as a [[quotient set]] of that collection.

## Properties

The class of ordinals is itself [[well-ordered]].  There are many equivalent ways to define this ordering.  One is that $\alpha\lt\beta$ iff $\alpha$ is isomorphic to a proper _initial segment_ of $\beta$ (that is, a subset $S\subsetneq \beta$ such that $b\in S$ and $a\lt b$ imply $a\in S$).  With the von Neumann definition, this is equivalent to simply saying that $\alpha\in\beta$.

Every ordinal $\alpha$ has a **[[successor]]** $\alpha^+$, which in the von Neumann definition is simply $\alpha^+ = \alpha \cup \{\alpha\}$.  A **limit ordinal** is any ordinal which is not a successor of any other ordinal.

In the presence of the [[axiom of choice]], a [[cardinal number]] can be defined as a special ordinal number, specifically an ordinal which is not equipollent (isomorphic as a [[set]]) to any smaller ordinal.

## Related pages

* [[countable ordinal]], [[uncountable ordinal]]

* [[ordinal arithmetic]]

* [[cardinal]]

* [[plump ordinal]]

* [[∞-number]]

* [[ordinal analysis]]

One important use of ordinals is to index transfinite constructions, such as:

* [[transfinite composition]]
* [[transfinite construction of free algebras]]

## References

For ordinal numbers in [[homotopy type theory]], see section 10.3 of:

* *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

On the equivalence of set-theoretic and type-theoretic ordinals, see:

* [[Tom de Jong]], [[Nicolai Kraus]], [[Fredrik Nordvall Forsberg]], and [[Chuangjie Xu]], *Ordinals.CumulativeHierarchy.html* ([web](https://www.cs.bham.ac.uk/~mhe/TypeTopology/Ordinals.CumulativeHierarchy.html))

On [[ordinals]] in [[dependent type theory]] and [[marked extensional well-founded orders]]:

* {#deJongEtAl23} [[Tom de Jong]], [[Nicolai Kraus]], [[Fredrik Nordvall Forsberg]], [[Chuangjie Xu]], *Set-Theoretic and Type-Theoretic Ordinals Coincide* &lbrack;[arXiv:2301.10696](https://arxiv.org/abs/2301.10696)&rbrack;

On ordinal exponentiation in [[dependent type theory]], see:

* {#deJongEtAl25} [[Tom de Jong]], [[Nicolai Kraus]], [[Fredrik Nordvall Forsberg]], [[Chuangjie Xu]], *Ordinal Exponentiation in Homotopy Type Theory* ([arXiv:2501.14542](https://arxiv.org/abs/2501.14542))

Basic set-theory including ordinals is developped in the appendix of:

* [[John Kelley]], _General topology_, D. van Nostrand, New York (1955), reprinted as: Graduate Texts in Mathematics, Springer (1975) &lbrack;[ISBN:978-0-387-90125-1](https://www.springer.com/gp/book/9780387901251)&rbrack;

[[!redirects ordinal]]
[[!redirects ordinals]]
[[!redirects ordinal number]]
[[!redirects ordinal numbers]]

[[!redirects von Neumann ordinal]]
[[!redirects von Neumann ordinals]]
[[!redirects Von Neumann ordinal]]
[[!redirects Von Neumann ordinals]]
[[!redirects von Neumann ordinal number]]
[[!redirects von Neumann ordinal numbers]]
[[!redirects Von Neumann ordinal number]]
[[!redirects Von Neumann ordinal numbers]]

[[!redirects limit ordinal]]
[[!redirects limit ordinals]]

[[!redirects limiting ordinal]]
[[!redirects limiting ordinals]]

