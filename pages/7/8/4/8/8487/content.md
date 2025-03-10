
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _parenthesized braid operad_ is an [[operad]] in [[Grpd]] modelled on the [[braid group]].

## Definition

Let $PaB_n$ denote the category defined as follows:

* its set of [[objects]] is the [[free construction|free]] [[magma]] on one generator, or equivalently the set of [[rooted binary tree]]s.

* the set of morphisms between two objects $s,t$ is given by the [[braid group]] $B_n$ whenever $s$ and $t$ are words of the same length $n$, and is [[empty set|empty]] otherwise.

Then the collection $PaB$ of the $PaB_n$'s is a [[braided operad]]. 

The [[composition]]

$$\circ_i:PaB_n \times PaB_m \rightarrow PaB_{m+n-1}$$

is given by replacing the $i$th strand of the first braid, by the second braid made very thin.

$PaB$ also carries an obvious structure of a [[braided monoidal category]]. In fact:

+-- {: .num_theorem}
###### Theorem

$PaB$ is the [[free object|free]] [[braided monoidal category]] on one object. As a consequence, it is an [[initial object]] in the [[category]] of 
[[braided monoidal categories]].

=--


## Colored/ordered version

let $CPaB_n$ be the [[groupoid]] defined as follows:

* it set  [[objects]] are parenthesized [[permutations]] of $\{1,\dots,n\}$, that is non-associative, non-commutative monomials on this set in which every letter appears exactly once.

* [[morphisms]] between two objects $s,t$ are braids connecting each letter in $s$ to the same letter in $t$. In other words, let $p:B_n\rightarrow S_n$ be the canonical projection from the braid group to the symmetric group whose kernel is the pure braid group. Then, forgetting the parenthesization and viewing $s,t$ as permutations:

$$Hom(s,t)=p^{-1}(\{s^{-1}t\})$$

Then $CPaB$ is an (ordinary) [[operad]], the operadic structure being the same as for the non-colored version.

A topological interpretation of $CPaB$ is as follows:

+-- {: .num_theorem}
###### Theorem

$CPaB$ may be identified with a full sub-operad of the [[fundamental groupoid]] of the [[little 2-disk operad]].

=--

## References

$PaB$ was originally defined in

* [[Dror Bar-Natan]], _On Associators and the Grothendieck-Teichmuller Group I_ &lbrack;[arXiv:q-alg/9606021](http://arxiv.org/abs/q-alg/9606021)&rbrack;

The operad structure was pointed out in

* [[Dmitry Tamarkin]], _Formality of Chain Operad of Little Discs_, [Letters in Mathematical Physics 66:65–72, 2003.](https://sites.math.northwestern.edu/~tamarkin/Papers1/Formality.pdf)

