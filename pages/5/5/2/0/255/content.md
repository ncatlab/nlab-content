<div class="rightHandSide toc">
[[!include 2-category theory - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _monad_ is an [[endomorphism]] in a [[2-category]] equipped with the structure of a [[monoid]]: a 2-morphism from the composite of the morphism to itself, and one from the identity endomorphism to it, satisfying associativity and uniticity.

In the same spirit there is a notion of [[module over a monad]].

Monads are often considered in the 2-category [[Cat]] where they are given by [[endofunctor]]s with a monoid structure on them.  Modules over monads _in_ [[Cat]] _and on_ [[Set]] encode algebraic structures on sets. Therefore modules over a monad are also called _algebras_ overa monad.

In this way, a _monad_ abstracts the concept of an [[algebraic theory]] (such as "group" or "ring"), giving a general notion of [[extra structure]] on an object of a category.

Classically, if $\mathbf{T}$ is an algebraic theory (e.g. the theory of groups), a $\mathbf{T}$-structure on a set tells us how to interpret various _terms_ (e.g. $(a\cdot c)$) formed from elements of the set, subject to certain _axioms_ (e.g. $(a\cdot (b\cdot c))=((a\cdot b)\cdot c)$).  A monad collects this up into a functor $T$.  For a set $X$, $T X$ is the set of all terms of the theory formed from elements of $X$, with terms identified if axioms force them to be equal.  For groups, $T X$ is thus the (underlying set of the) [[free group]] of formal words $a \cdot b \cdot \cdots \cdot s$ from $X$; the fact that $T$ gives [[free object|free]] structures turns out to be [[monadic adjunction|typical]].

To capture the theory fully, we need to include a little more data: a natural map $\eta_X : X \to T X$ recording how each $a \in X$ gives a trivial term $a$, and a map $\mu_X:T T X \to T X$ recording how further terms built from terms are already present as terms in $T X$.  The axioms satisfied by these maps turn out to have a striking formal relation to the axioms for a [[monoid]].


##Definition

### In Cat

A _monad_ in [[Cat]] on a [[category]] $C$ is a [[monoid]] in the strict [[monoidal category] $End(C)$ of [[endofunctor]]s in $C$ (where the [[tensor product]] of [[natural transformation]]s is the [[horizontal composition]]).  

More explicitly a monad on $C$ consists of

* an [[endofunctor]] $T : C \to C$, and

* a pair of [[natural transformations]] $\eta: 1_C \to T$ (the _unit_ of $T$) and $\mu: T^2 \to T$ (the _multiplication_), such that

* there exists $\eta$ which is a unit for $\mu$, i.e. $\mu \cdot (\eta \circ T) = 1_C = \mu \cdot (T \circ \eta)$, and

* $\mu$ is associative, i.e. $\mu \cdot (T \circ \mu) = \mu \cdot (\mu \circ T)$.

If we consider $C$ as an object in the 2-category $Cat$ of categories, functors and natural transformations, then we see that $(C,T,\mu,\eta)$ is a 4-tuple of a 0-cell, 1-cell and two 2-cells satisfying some diagrams.  
Thus this makes sense in arbitrary 2-category and even a [[bicategory]].  If $\mathcal{B}$ is a bicategory, a monad on an object $C$ of $\mathcal{B}$ consists of a 1-cell $T: C \to C$ together with 2-cells $\eta, \mu$ satisfying axioms as before, but with associativity coherences taken into account (monad with underlying object $C$ in $\mathcal{B}$ is the same as a monoid in the monoidal category $Hom_{\mathcal{B}}(C,C)=\mathcal{B}(C,C)$).

### In a general 2-category

More generally, for an [[object]] $C$ in any [[2-category]] $\mathcal{B}$ a _monad on $C$_ is a [[monoid]] in the [[monoidal category]] $End_{\mathcal{B}}(C)$.

###In string diagrams

These data and axioms can be expressed graphically in string diagrams.  The data $C \stackrel{T}{\to} C$, $1_C \stackrel{\eta}{\Rightarrow} T$, $T \circ T \stackrel{\mu}{\Rightarrow} T$ appear as:

[[monad-data-labeled.png:pic]]

Thanks to the distinctive shapes, one can usually omit the labels:

[[monad-data-unlabeled.png:pic]]

The axioms $\mu \cdot (\eta \circ T) = 1_C = \mu \cdot (T \circ \eta)$ and $\mu \cdot (T \circ \mu) = \mu \cdot (\mu \circ T)$ then appear as:

[[monad-axioms-unlabeled.png:pic]]


### As monoids

The name "monad" and the terms "unit", "multiplication" and "associativity" come from a clear analogy with [[monoids]].  Indeed, one can define a monad on an object $C$ of a [[bicategory]] $\mathcal{B}$ as just a monoid in its endomorphism category $\mathcal{B}(C,C)$.

Alternatively, monads can be taken as more fundamental, and a monoid in a [[monoidal category]] $C$ can be defined as a monad _in_ $C$, viewing $C$ as a one-object bicategory.


### As lax functors 

Yet another definition, slick and mysterious:

A monad in $\mathcal{B}$ is a [[lax functor]] from the terminal bicategory $1$ to $\mathcal{B}$.

Among higher-category theorists, it's tempting to suggest that this is the most fundamental definition, and the most basic reason for the ubiquity and importance of monads.  Regardless of this, however, the earlier more elementary definitions are both practically and pedagogically essential.

+-- {: .query}
[[Peter LeFanu Lumsdaine]]: I did the diagrams with the monad called $(T,\eta,\mu)$ and have only just noticed that that disagrees with what's used in the preceding description.  Was there a particular principled reason for calling it $(A,i,\mu)$ above?  I can change the diagrams to agree if so, but if not, might it be easier on newcomers to use $(T,\eta,\mu)$ throughout?  Pretty much all the references I know use that as the generic name for a monad. ---Peter

[[Mike Shulman]]: I like $T$ as the name for a monad.  (I also think that as a matter of exposition, this page should start out with monads in $Cat$ and introduce the more general version later, but I don't have time to implement that right now.)

[[Peter LeFanu Lumsdaine]]: I'd been thinking the same; so I've re-organised things as you suggest, and added an "idea" section.  I think that probably goes into too much detail now, especially since "generalised algebraic theory" is only one of many ideas of what a monad is, but someone else can probably cut it down more dispassionately than I can :-)

[[Mike Shulman]]: I don't think it needs any cutting down.  If anything, one could add more description of all the other things that a monad is.

[[Zoran ?koda]]: I do not like the idea section. It describes a very special case of monad theory as the principal motivation, namely of monads in the category of sets. I know lots of heavy monad users, including mine, who almost never use monads to describe algebraic theories. For Jon Beck the principal motivation is cohomology theory, for some is the descent theory, for some generalized module theory, for some equivariance, for some relativizing affiness in algebraic geometry...
=--


## Remarks

* Monads in $Cat$ are sometimes, mostly in older literature, also called **triple**s (alluding to the triple of data $(A,\mu,i)$).  In even older literature, they are also referred to as **standard constructions**, from Beck's discovery of them as a unifying description of the constructions of various homology theories.

* We can picture a monad in $B$ as an image of the [[oriental|third oriental]] in $B$. See the remarks at [[monoidal category]].


## Examples 

Monads on [[partial order|posets]] are particularly simple.  In fact, monads on [[power set]]s are extremely common throughout mathematics; they are known in less categorially-inclined circles as [[Moore closure]]s, and there are many examples there.

Every [[algebraic theory]] with a notion of free algebra defines a monad on [[Set]].  For example, the operation taking a set $S$ to the underlying set of the [[free monoid]] on $S$ may be extended to a monad, the [[list monad]]; the operation taking $S$ to the underlying set of the free [[pointed set]] on $S$ may be extended to the [[successor]] monad (see below).

An [[internalization|internal]] monad on the [[subobject classifier]] of a [[topos]] $E$ is a [[Lawvere-Tierney topology]] on $E$.


### The Successor Monad

The successor monad is an example of monad on $Set$. We define $S X$ as a [[disjoint union]] of $S$ and a [[singleton set]].  In [[material set theory]] (with the [[axiom of foundation]]), it is handy to define this as $S X \coloneq X \cup\{X\}$; then for $f\colon X \to Y$,
$$ S f(x) \coloneqq \left\{ \begin{matrix} f(x) & x \in X \\ Y & x = X \end{matrix} \right .$$
The structure map $\eta_X$ is the [[inclusion function|inclusion]] of $X$ in $S X$; the map $\mu_X\colon S S X \to S X$ [[restriction|restricts]] to $S X$ as the [[identity function|identity]], and futhermore has as [[image]] $\mu_X(S X) = X$.

The [[hom-set]] of morphisms in the [[Kleisli category]] of $(S,\eta,\mu)$ from $X$ to $Y$ is canonically equivalent (using [[excluded middle]]) to the set of [[partial functions]] from $X$ to $Y$; its [[Eilenberg?Moore category]] is equivalent to the category of [[pointed sets]] and pointed maps, i.e. functions of the form $1 \to X$ and commuting squares between such morphisms.

The successor monad as defined here is also interesting in that it stabilizes the finite [[von Neumann ordinals]] and *monotone* maps between them, and that $\eta$ and $\mu$ are also monotone.  Thus the successor monad restricts as a monad to the augmented [[simplex category]].  Furthermore, every monotone map of finite ordinals can be written as a composite of arrows of the form $S^k \mu_l$ and $S^m \eta_n$.  Indeed, the [[monoidal category]] $\Delta_a$ is generated by the [[monoid object]] $0 \overset{\iota_0}\rightarrow 1 \overset{\mu_0}\leftarrow 2$.

+-- {: .query}
[[JCMcKeown]]: I want to say something like $(S,\eta,\mu)$ _generates_ the (skeletal augmented) simplex category; there is surely a right way to say that, but what is it?

_Toby_:  I don\'t think that it\'s quite true that $S$ generates the simplex category, because you need an object to start applying it to.  But I\'d agree that $(S,\eta,\mu)$ generates it starting from $0$.  I don\'t know any slick way to say that.

I\'ve put in a suggestion by Finn above.  How\'s that?
=--


## Algebras/modules over a monad {#Algebras}

Given that a monad in a bicategory $\mathcal{B}$ is nothing but a [[monoid]] in a hom-category $\mathcal{B}(a,a)$, it is natural to consider a [[module]] over this monoid: a [[module for a monad]].  This notion of module is more general than a module in a monoidal category, however, since it need not live in $\mathcal{B}(a,a)$ but can be in $\mathcal{B}(b,a)$ (for left modules) or $\mathcal{B}(a,c)$ (for right modules).

In a $Cat$-like bicategory, left modules over a monad are usually called _algebras over the monad_.  This terminology is confusing from the point of view of monads as monoids, but is justified because in [[Cat]] itself, such algebras with domain [[terminal category|1]] are just algebras for a monad in the classical sense.  Such algebras are a powerful tool to encode general algebraic structures; this is the topic of [[universal algebra]].  The algebras over a monad form its [[Eilenberg-Moore category]], which is characterized by a universal property.

Some monads arise from [[operad]]s, in which case algebras for the monad are the same as algebras for the operad.  A [[Lawvere theory]] is another special sort of monad in $Cat$.


## Monads in higher category theory


There is a [[vertical categorification]] of monads  to [[(∞,1)-category|(∞,1)-categories]]. See [[(infinity,1)-monad|(∞,1)-monad]].

in [section 3](http://arxiv.org/PS_cache/math/pdf/0702/0702299v5.pdf#page=93) of

* [[Jacob Lurie]], _Noncommutative algebra_ ([arXiv](http://arxiv.org/abs/math/0702299))


## Related entries 

* [[strong monad]]

* [[bar construction]]

* [[monadic descent]]


## References

* R. Street, _The formal theory of monads_, J. of Pure and Applied Algebra __2__ (1972), 149--168; R. Street, S. Lack, _The formal theory of monads II_, J. Pure Appl. Algebra __175__ (2002), No. 1-3,
243--265.

* [[Francis Borceux|F. Borceux]], _Handbook of categorical algebra_,  vol. 2, Ch. 4 "Monads" 

An early collection of articles is

* H. Appelgate, M. Barr, J. Beck, F. W. Lawvere, F. E. J. Linton,
E. Manes, M. Tierney, F. Ulmer, _Seminar on triples and categorical
homology theory_, ETH 1966/67, edited by B.~Eckmann, LNM 80, Springer 1969. 

* [[The Catsters]], [Monads](http://www.youtube.com/view_play_list?p=0E91279846EC843E) (five short video lectures)

* [[John Baez]], _[Universal Algebra and Diagrammatic Reasoning](http://math.ucr.edu/home/baez/universal/universal_hyper.pdf)_ (Introductory slides).

Book (recall that monads are also called 'triples'):

* [[Michael Barr]] and [[Charles Wells]], _[Toposes, Triples and Theories](http://www.cwru.edu/artsci/math/wells/pub/ttt.html)_.

* T. M. Fiore, N. Gambino, J. Kock,  _Monads in double categories_, [arxiv/1006.0797](http://arxiv.org/abs/1006.0797)

* Gabriella B&#246;hm, Stephen Lack, [[Ross Street]], _Weak bimonads_, [arxiv/1002.4493](http://arxiv.org/abs/1002.4493)


[[!redirects monad]]
[[!redirects monads]]

[[!redirects successor monad]]
