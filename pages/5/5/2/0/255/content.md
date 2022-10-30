
> This entry is about the notion of _monad_ in [[category theory]]. For other notions see _[[monad (disambiguation)]]_.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

The entry is about monads in the sense of category theory, for another concept see also [[monad in nonstandard analysis]]. 

## Idea

A [[monad]] is a structure that is a lot like a [[monoid]], but that lives in a [[bicategory]] rather than a [[monoidal category]].  In other words, the concept of a monad is the [[horizontal categorification]] of that of a monoid.

Monads are among the most pervasive structures in [[category theory]] and its applications: for example, they are central to the category-theoretic account of [[universal algebra]], as well as underlying the theory of [[simplicial objects]] and thus, via the [[Dold?Kan correspondence]], much of [[homological algebra]].

##Definition

A **monad** in a [[bicategory]] $K$ is given by

* an [[object]] $a$, together with

* an [[endomorphism]] $t \colon a \to a$, and

* [[2-cells]] $\eta \colon 1_a \to t$ (the _unit_ of $t$) and $\mu \colon t \circ t \to t$ (the _multiplication_)

such that the diagrams
$$
\array{
  t & \stackrel{\eta t}{\to} & t t & \stackrel{t \eta}{\leftarrow}
  & t \\
  & \searrow & \downarrow \mathrlap{\mu} & \swarrow & \\
  & & t & &
}
\qquad \qquad
\array{
  t t t & \stackrel{\mu t}{\to} & t t \\
  \mathllap{t \mu} \downarrow & & \downarrow \mathrlap{\mu} \\
  t t & \stackrel{\mu}{\to} & t
}
$$
commute (where certain [[coherence]] [[isomorphism]]s have been omitted).

The name "monad" and the terms "unit", "multiplication" and "associativity" bear a clear analogy with [[monoids]].  Indeed, one can define a monad on an object $a$ of a [[bicategory]] $K$ as just a **monoid** in the endomorphism category $K(a,a)$.  Alternatively, monads can be taken as more fundamental, and a monoid in a [[monoidal category]] $C$ can be defined as a monad in $\mathbf{B} C$, the one-object bicategory corresponding to $C$.

A third and somewhat less obvious definition says that a monad in $K$ is a **[[lax 2-functor]]** from the terminal bicategory $1$ to $K$: the unique object $\ast$ of $1$ is sent to the object $a$, the morphism $1_a$ becomes $t$, and $\eta$ and $\mu$ arise from the coherent 2-cells expressing lax functoriality.  Among higher-category theorists, it's tempting to suggest that this is the most fundamental definition, and the most basic reason for the ubiquity and importance of monads.  Regardless of this, however, the earlier more elementary definitions are both practically and pedagogically essential.

We can picture a monad in $K$ as an image of the [[oriental|third oriental]] in $K$. See the remarks at [[monoidal category]].

The data of and axioms for a monad can be expressed graphically as [[string diagrams]].  Writing $T \colon C \to C, \eta, \mu$ for the monad in question (this notation being the standard one when $K = Cat$), these data can be represented as

[[monad-data-labeled.png:pic]]

Thanks to the distinctive shapes, one can usually omit the labels:

[[monad-data-unlabeled.png:pic]]

The axioms then appear as:

[[monad-axioms-unlabeled.png:pic]]

Monads in $Cat$ are sometimes, mostly in older literature, also called **triple**s (alluding to the triple of data $(A,\mu,i)$), following Eilenberg and Moore.  In even older literature, they are also referred to as **standard constructions**, the original term used by Godement when he introduced the idea. For terminological remarks by Ross Street see category-list [here](http://article.gmane.org/gmane.science.mathematics.categories/225/match=).


## The bicategory $Mnd(K)$

Given the equivalence between monads in $K$ and lax functors $1 \to K$ it is straightforward to define the bicategory $Mnd(K)$ of monads in $K$ to be the lax functor category $[1,K]_\ell$, which consists of lax functors, [[lax transformations]] and [[modifications]].

Spelling this out, we see that an object of $Mnd(K)$ is a monad $(a,t,\eta,\mu)$ in $K$.  A **morphism** of monads $(a,t) \to (b,s)$ is given by 1-cell $x \colon a \to b$ together with a 2-cell $\lambda \colon s x \to x t$ satisfying
$$
\array{
  x & \stackrel{\eta^s x}{\to} & s x \\
  \mathllap{x \eta^t} \downarrow & & \downarrow \mathrlap{\lambda} \\
  x t & \stackrel{1}{\to} & x t
}\qquad \qquad
\array{
 s s x & \stackrel{s \lambda}{\to} & s x t & \stackrel{\lambda t}{\to}
 & x t t \\
 \mathllap{\mu^s x} \downarrow & & & & \downarrow \mathrlap{x \mu^t}
 \\
 s x & & \stackrel{\lambda}{\to} & & x t
}
$$
Finally, a 2-cell $(x,\lambda) \Rightarrow (y, \kappa)$ is given by a 2-cell $m \colon x \Rightarrow y$ satisfying
$$
\array{
 s x & \stackrel{s m}{\to} & s y \\
 \mathllap{\lambda} \downarrow & & \downarrow \mathrlap{\kappa} \\
 x t & \stackrel{m t}{\to} & y t
}
$$

## Examples 

### Monads in Cat

Monads are often considered in the 2-category [[Cat]] where they are given by [[endofunctors]] with a monoid structure on them.  In particular, monads _in_ [[Cat]] _on_ [[Set]] are equivalent to the equational theories studied in universal algebra.  In this context, a monad abstracts the concept of an [[algebraic theory]] (such as "group" or "ring"), giving a general notion of [[extra structure]] on an object of a category.

Classically, if $\mathbf{T}$ is an algebraic theory (e.g. the theory of groups), a $\mathbf{T}$-structure on a set tells us how to interpret various _terms_ (e.g. $(a\cdot c)$) formed from elements of the set, subject to certain _axioms_ (e.g. $(a\cdot (b\cdot c))=((a\cdot b)\cdot c)$).  A monad collects this up into a functor $T$.  For a set $X$, $T X$ is the set of all terms of the theory formed from elements of $X$, with terms identified if axioms force them to be equal.  For groups, $T X$ is thus the (underlying set of the) [[free group]] of formal words $a \cdot b \cdot \cdots \cdot s$ from $X$; the fact that $T$ gives [[free object|free]] structures turns out to be [[monadic adjunction|typical]].

To capture the theory fully, we need to include a little more data: a natural map $\eta_X : X \to T X$ recording how each $a \in X$ gives a trivial term $a$, and a map $\mu_X:T T X \to T X$ recording how further terms built from terms are already present as terms in $T X$.  

### Other examples

* Monads on [[partial order|posets]] are particularly simple (in particular, they are always [[idempotent monad|idempotent]]).  In fact, monads on [[power set]]s are extremely common throughout mathematics; they are known in less categorially-inclined circles as [[Moore closure]]s, and there are many examples there.

* An [[internalization|internal]] monad on the [[subobject classifier]] of a [[topos]] $E$ is a [[Lawvere-Tierney topology]] on $E$.

* If $C$ is a category with [[finite limits]], then a monad in the bicategory of [[spans]] in $C$ is the same thing as an [[internal category]] in $C$.

* A monad in the bicategory [[Prof]] of [[profunctors]] on a category $A$ can be identified with an identity-on-objects functor $A\to B$.


## Algebras/modules over a monad {#Algebras}

Given that a monad in a bicategory $\mathcal{B}$ is nothing but a [[monoid]] in a hom-category $\mathcal{B}(a,a)$, it is natural to consider a [[module]] over this monoid: a [[module for a monad]].  This notion of module is more general than a module in a [[monoidal category]], however, since it need not live in $\mathcal{B}(a,a)$ but can be in $\mathcal{B}(b,a)$ (for left modules) or $\mathcal{B}(a,c)$ (for right modules).

In a [[Cat]]-like [[bicategory]], left modules over a monad are usually called _algebras over the monad_.  This terminology is confusing from the point of view of monads as monoids, but is justified because in [[Cat]] itself, such algebras with domain [[terminal category|1]] are just algebras for a monad in the classical sense.  Such algebras are a powerful tool to encode general algebraic structures; this is the topic of [[universal algebra]].  The algebras over a monad form its [[Eilenberg-Moore category]], which is characterized by a [[universal property]].

Some monads arise from [[operad]]s, in which case algebras for the monad are the same as algebras for the operad.  A [[Lawvere theory]] is another special sort of monad in $Cat$.


## Monads in higher category theory


There is a [[vertical categorification]] of monads  to [[(∞,1)-category|(∞,1)-categories]]. See [[(infinity,1)-monad|(∞,1)-monad]].

in [section 3](http://arxiv.org/PS_cache/math/pdf/0702/0702299v5.pdf#page=93) of

* [[Jacob Lurie]], _Noncommutative algebra_ ([arXiv](http://arxiv.org/abs/math/0702299))


## Related concepts


* [[adjunction]], [[comonad]], [[adjoint monad]], [[algebra over a monad]], [[monad with arities]], [[distributive law]], [[monoidal monad]], [[cartesian monad]]

* [[algebraic theory]] / [[Lawvere theory]] /  [[(∞,1)-algebraic theory]]

* **monad** [[2-monad]]/[[doctrine]] / [[(∞,1)-monad]]

  * [[idempotent monad]], [[strong monad]]

  * [[monad (in computer science)]], [[Lawvere-Tierney topology]]

* [[operad]] / [[(∞,1)-operad]]

* [[strong monad]]

* [[bar construction]]

* [[monadic descent]]

## References

Introductions:

* [[The Catsters]], _[Monads](http://www.youtube.com/view_play_list?p=0E91279846EC843E) (five short video lectures)_

* [[John Baez]], _[Universal Algebra and Diagrammatic Reasoning](http://math.ucr.edu/home/baez/universal/universal_hyper.pdf)_ (Introductory slides).

Detailed accounts:

* [[Michael Barr]], [[Charles Wells]], _[Toposes, Triples and Theories](http://www.cwru.edu/artsci/math/wells/pub/ttt.html)_.

* [[Francis Borceux|F. Borceux]], _Handbook of categorical algebra_,  vol. 2, Ch. 4 "Monads" 

* [[R. Street]], _The formal theory of monads_, J. of Pure and Applied Algebra __2__ (1972), 149--168 (<a href="http://dx.doi.org/10.1016/0022-4049(72)90019-9">doi</a>)

* [[Ross Street]], [[Steve Lack]], _The formal theory of monads II_, J. Pure Appl. Algebra __175__ (2002), No. 1-3, 243--265, (<a href="http://dx.doi.org/10.1016/S0022-4049(02)00137-8">doi</a>)

* H. Appelgate, [[M. Barr]], [[J. Beck]], [[F. W. Lawvere]], [[F. E. J. Linton]], [[E. Manes]], [[M. Tierney]], [[F. Ulmer]], _Seminar on triples and categorical homology theory_, ETH 1966/67, edited by B.~Eckmann, LNM 80, Springer 1969. 

Relation to [[universal algebra]]:

* [[Martin Hyland]] and [[John Power]], _The category theoretic understanding of universal algebra: Lawvere theories and monads_ ([pdf](http://www.dpmms.cam.ac.uk/~martin/Research/Publications/2007/hp07.pdf)).

* Anthony Voutas, _The basic theory of monads and their connection to
universal algebra_ ([pdf](http://cs.anu.edu.au/student/projects/12S1/Reports/Anthony_Voutas_Report.pdf))

In [[higher category theory]]:

* [[T. M. Fiore]], [[N. Gambino]], [[J. Kock]],  _Monads in double categories_, [arxiv/1006.0797](http://arxiv.org/abs/1006.0797)

* Gabriella B&#246;hm, [[Stephen Lack]], [[Ross Street]], _Weak bimonads_, [arxiv/1002.4493](http://arxiv.org/abs/1002.4493)


[[!redirects monad]]
[[!redirects monads]]

