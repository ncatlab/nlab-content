+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea
 {#Idea}

In [[vertical categorification]] of how [[monoids]]/[[monoid objects]] $A$ may [[action|act]] on other objects $N$ ([[action objects]], [[module objects]]) inside an ambient [[monoidal category]] by [[maps]]

$$
  A \otimes N \longrightarrow N
  \,.
$$

satisfying the [action property](action#eq:ActionProperty), so a [[monoidal category]] $\mathcal{A}$ may act on other *[[categories]]* $\mathcal{N}$ by [[functors]] 

$$
  \oslash 
  \;\colon\;
  \mathcal{A} \times \mathcal{N}
  \longrightarrow
  \mathcal{N}
$$

subject to [[associators]], [[unitors]] and [[coherence conditions]] for [[action objects]] [[coherence|coherently]] [[internalization|internalized]] into the [[2-category]] [[Cat]], analogous to the laws in a [[monoidal category]].

At least if some linear structure is present and respected (such as when $\mathcal{A}$ qualifies as a [[2-ring]]) it is natural to speak of *[[module categories]]* over $\mathcal{A}$ (see also at *[[n-module|$n$-module]]*).

Similarly, compatible actions from both sides, such as for a [[bimodule]], give a notion of *[[bimodule category]].

Note that the term **actegory**, introduced by [McCrudden (2000)](#McCrudden00)[^1], is often used in the literature for this concept, and consequently **[[biactegory]]** for the two-sided case. However, since "actegory" is a single transposition away from "category", we prefer to use the explicit terminology on this page and elsewhere.

[^1]: From [Cockett & Pastro (2007)](#CockettPastro07): "The term *actegory* is used to describe the situation of a monoidal category “acting” on a category.  They first appeared (under a different name) in the work of B&eacute;nabou as a simple example of a bicategory. B. Pareigis developed the theory of actegories (again under a different name) and showed there usefulness in the representation theory of monoids and comonoids. The word “actegory” was first suggested at the Australian Category Seminar and first appeared in print in the thesis of P. McCrudden where they were used to study categories of representations of coalgebroids."



## Definition

For any [[category]] $A$, the category of [[endofunctors]] $End(A)$ is [[monoidal category|monoidal]] with respect to the (horizontal) composition (the composition of functors and the [[Godement product]] for natural transformations).

Given a [[monoidal category]] $(C,\otimes,I,l,r,a)$ a (left or right) __$C$-module category__ is a category $A$ together with a (left or right) coherent action of $C$ on $A$. Depending on author and context, the left coherent action of $C$ on $A$ is a morphism of monoidal categories $C\to End(A)$ in the lax, colax, pseudo or strict sense (most often in pseudo-sense) or, in another terminology, a monoidal, comonoidal, strong monoidal or strict [[monoidal functor]]. Right coherent actions correspond to the monoidal functors into the category $End(A)$ with the opposite tensor product. 

$C$-module categories, colax $C$-equivariant functors and natural transformations of colax $C$-equivariant functors form a [[strict 2-category]] $_C Act^c$. A [[monad]] in $_C Act^c$ amounts to a pair of a monad in $Cat$ and a [[distributive law]] between the monad and an action of $C$. 

The notion of $C$-action (hence a $C$-module category) is easily extendable to [[bicategories]] (see Bakovi&#263;'s thesis).

+-- {: .num_defn #ModuleCategory}
###### Definition
A **(left) $\mathcal{C}$-module category** is

1. a category $\mathcal{A}$;
1. a functor $\oslash : \mathcal{C} \times \mathcal{A} \to \mathcal{A}$ called the *action*;
1. a natural isomorphism $\lambda_a : a \to I \oslash a$ called the *unitor*;
1. a natural isomorphism $\alpha_{c,d,a} : c \oslash (d \oslash a) \to (c \otimes d) \oslash a$ called the *actor*;

satisfying a pentagonal and two triangular laws (see [KJ01](#KJ01), diagg. (1.1)-(1.3)) that witness the coherence of $\lambda$ and $\alpha$ with the unitors and associators of $\mathcal{C}$.
=--

## Connection with enrichment 
If a category $D$ is [[enriched category|enriched]] in $C$ with [[copowers]], then the copower structure forms a module category on the ordinary category underlying $D$. 

Conversely, if module category is such that the functor $(-)\oslash d:C\to D$ has a [[right adjoint]] for all objects $d$ of $D$, then the right adjoints $D(d,-):D\to C$ provide an enrichment of $D$ in $C$ for which the action is a copower. See [KJ01](#KJ01).

More generally, supposing $C$ is small, the following data are equivalent: (1) a $C$-module category $D$; (2) an enrichment of $D$ in the category $\hat C$ of [[presheaves]] on $C$ (i.e. a [[locally graded category]]), with copowers by [[representables]]. Here we regard $\hat C$ as a monoidal category with the [[Day convolution]]. 

Starting from a $C$-module category $D$, consider the enrichment given by $D(d,d')=hom(-\oslash d,d'):C^{op}\to Set$. If these presheaves are representable, this is what it means to be enriched in $C$ for which the action is a copower. If they are not representable, it is still an enrichment, and the copowers by representables are the action. 

For this reason, many concepts from enriched category theory make sense for module categories too. 


## Related Concepts

* [[multiactegory]], a generalisation of the concept from monoidal categories to [[multicategories]]

* [[action object]], [[module object]]

* [[2-module]], [[n-module]]

* [[monoidal actegory]]


## References

* [[Bodo Pareigis]], _Non-additive ring and module theory I. General theory of monoids_, Publ. Math. Debrecen 24 (1977), 189--204. MR 56:8656; _Non-additive ring and module theory II. C-categories, C-functors, and C-morphisms_, Publ. Math. Debrecen 24 (351--361) 1977. 

* {#KJ01} [[Max Kelly]], [[George Janelidze]], _A note on actions of a monoidal category_, Theory and Applications of Categories, Vol. 9, 2001, No. 4, pp 61--91 [link](http://www.tac.mta.ca/tac/volumes/9/n4/9-04abs.html)

* {#McCrudden00} P. McCrudden, *Categories of representations of coalgebroids*, Advances in Mathematics __154__ 2 (2000) 299--332 &lbrack;[doi:10.1006/aima.2000.1926](https://doi.org/10.1006/aima.2000.1926)&rbrack;

* [[Peter Schauenburg]], _Actions of monoidal categories and generalized Hopf smash products_, J. Algebra __270__ (2003) 521--563 (remark: actegories with action in the strong monoidal sense)

* [[Zoran Škoda]], _Distributive laws for actions of monoidal categories_, [arXiv:0406310](https://arxiv.org/abs/math/0406310), _Equivariant monads and equivariant lifts versus a 2-category of distributive laws_, [arXiv:0707.1609](https://arxiv.org/abs/0707.1609)

* [[J. R. B. Cockett]], Craig Pastro, _The logic of message-passing_ [arXiv:math/0703713](https://arxiv.org/abs/math/0703713).

A recent survey of many basic definitions and operations on actegories is

* [[Matteo Capucci]], Bruno Gavranović, _Actegories for the working amthematician_, [arXiv:2203.16351](https://arxiv.org/abs/2203.16351)

A generalisation from [[monoidal categories]] to [[bicategories]] is studied in, where actions are called **representations**:

* [[Robert Gordon]], and [[John Power]]. _Enrichment through variation_, Journal of Pure and Applied Algebra 120.2 (1997): 167-185.

[[!redirects actegory]]
[[!redirects actegories]]


