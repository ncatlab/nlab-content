#Contents#

* It said "Tacit"!  So I took it. 
{:toc}

##Idea##

A _monad_ abstracts the concept of an [[algebraic theory]] (such as "group" or "ring"), giving a general notion of a [[structure]] on an object of a category.

Classically, if $\mathbf{T}$ is an algebraic theory (e.g.\ the theory of groups), a $\mathbf{T}$-structure on a set tells us how to interpret various _terms_ (e.g. $(a\cdot c)$) formed from elements of the set, subject to certain _axioms_ (e.g. $(a\cdot (b\cdot c))=((a\cdot b)\cdot c)$).  A monad collects this up into a functor $T$.  For a set $X$, $T X$ is the set of all terms of the theory formed from elements of $X$, with terms identified if axioms force them to be equal.  For groups, $T X$ is thus the (underlying set of the) [[free group]] of formal words $a\cdot b \ldots \cdot s$ from $X$; the fact that $T$ gives [[free]] structures turns out to be [[monadic adjunction|typical]].

To capture the theory fully, we need to include a little more data: a natural map $\eta_X : X \to T X$ recording how each $a \in X$ gives a trivial term $a$, and a map $\mu_X:T T X \to T X$ recording how further terms built from terms are already present as terms in $T X$.  The axioms satisfied by these maps turn out to have a striking formal relation to the axioms for a [[monoid]].

##Definition##

A _monad_ on a category $C$ consists of

* an [[endofunctor]] $T : C \to C$, and

* a pair of [[natural transformations]] $\eta: 1_C \to T$ (the _unit_ of $T$) and $\mu: T^2 \to T$ (the _multiplication_), such that

* $\eta$ is a unit for $\mu$, i.e. $\mu \cdot (\eta \circ T) = 1_C = \mu \cdot (T \circ \eta)$, and

* $\mu$ is associative, i.e. $\mu \cdot (T \circ \mu) = \mu \cdot (\mu \circ T)$.

This generalises evidently from categories to the objects of any [[bicategory]].  If $\mathcal{B}$ is a bicategory, a monad on an object $C$ of $\mathcal{B}$ consists of a 1-cell $T: C \to C$ together with 2-cells $\eta, \mu$ satisfying axioms as before.

###In string diagrams###

These data and axioms can be expressed graphically in string diagrams.  The data $C \stackrel{T}{\to} C$, $1_C \stackrel{\eta}{\Rightarrow} T$, $T \circ T \stackrel{\mu}{\Rightarrow} T$ appear as:

[[monad-data-labeled.png:pic]]

Thanks to the distinctive shapes, one can usually omit the labels:

[[monad-data-unlabeled.png:pic]]

The axioms $\mu \cdot (\eta \circ T) = 1_C = \mu \cdot (T \circ \eta)$ and $\mu \cdot (T \circ \mu) = \mu \cdot (\mu \circ T)$ then appear as:

[[monad-axioms-unlabeled.png:pic]]

### As monoids ###

The name "monad" and the terms "unit", "multiplication" and "associativity" come from a clear analogy with [[monoids]].  Indeed, one can define a monad on an object $C$ of a [[bicategory]] $\mathcal{B}$ as just a monoid in its endomorphism category $\mathcal{B}(C,C)$.

Alternatively, monads can be taken as more fundamental, and a monoid in a [[monoidal category]] $C$ can be defined as a monad _in_ $C$, viewing $C$ as a one-object bicategory.

### As lax functors ###

Yet another definition, slick and mysterious:

A monad in $\mathcal{B}$ is a [[lax functor]] from the terminal bicategory $1$ to $\mathcal{B}$.

Among higher-category theorists, it's tempting to suggest that this is the most fundamental definition, and the most basic reason for the ubiquity and importance of monads.  Regardless of this, however, the earlier more elementary definitions are both practically and pedagogically essential.

+-- {: .query}
[[Peter LeFanu Lumsdaine]]: I did the diagrams with the monad called $(T,\eta,\mu)$ and have only just noticed that that disagrees with what's used in the preceding description.  Was there a particular principled reason for calling it $(A,i,\mu)$ above?  I can change the diagrams to agree if so, but if not, might it be easier on newcomers to use $(T,\eta,\mu)$ throughout?  Pretty much all the references I know use that as the generic name for a monad. ---Peter

[[Mike Shulman]]: I like $T$ as the name for a monad.  (I also think that as a matter of exposition, this page should start out with monads in $Cat$ and introduce the more general version later, but I don't have time to implement that right now.)

[[Peter LeFanu Lumsdaine]]: I'd been thinking the same; so I've re-organised things as you suggest, and added an "idea" section.  I think that probably goes into too much detail now, especially since "generalised algebraic theory" is only one of many ideas of what a monad is, but someone else can probably cut it down more dispassionately than I can :-)

[[Mike Shulman]]: I don't think it needs any cutting down.  If anything, one could add more description of all the other things that a monad is.
=--

##Remarks##

* Monads in $Cat$ are sometimes, mostly in older literature, also called **triple**s (alluding to the triple of data $(A,\mu,i)$).  In even older literature, they are also referred to as **standard constructions**, from Beck's discovery of them as a unifying description of the constructions of various homology theories.

* We can picture a monad in $B$ as an image of the [[oriental|third oriental]] in $B$. See the remarks at [[monoidal category]].


## Examples ##

Monads on [[partial order|posets]] are particularly simple.  In fact, monads on [[power set]]s are extremely common throughout mathematics; they are known in less categorially-inclined circles as [[Moore closure]]s, and there are many examples there.

Every [[algebraic theory]] with a notion of free algebra defines a monad on [[Set]].  For example, the operation taking a set $S$ to the underlying set of the [[free monoid]] on $S$ may be extended to a monad, the [[list monad]].

An [[internalization|internal]] monad on the [[subobject classifier]] of a [[topos]] $E$ is a [[Lawvere-Tierney topology]] on $E$.


##Algebras/modules over a monad##

Given that a monad in a bicategory $\mathcal{B}$ is nothing but a [[monoid]] in a hom-category $\mathcal{B}(a,a)$, it is natural to consider a [[module]] over this monoid: a [[module for a monad]].  This notion of module is more general than a module in a monoidal category, however, since it need not live in $\mathcal{B}(a,a)$ but can be in $\mathcal{B}(b,a)$ (for left modules) or $\mathcal{B}(a,c)$ (for right modules).

In a $Cat$-like bicategory, left modules over a monad are usually called _algebras over the monad_.  This terminology is confusing from the point of view of monads as monoids, but is justified because in [[Cat]] itself, such algebras with domain [[terminal category|1]] are just algebras for a monad in the classical sense.  Such algebras are a powerful tool to encode general algebraic structures; this is the topic of [[universal algebra]].

Some monads arise from [[operad]]s, in which case algebras for the monad are the same as algebras for the operad.  A [[Lawvere theory]] is another special sort of monad in $Cat$.

# Related entries #

* [[strong monad]]

##References##

Five short videotaped lectures:

* The Catsters, [Monads](http://www.youtube.com/view_play_list?p=0E91279846EC843E).

Introductory slides:

* John Baez, [Universal Algebra and Diagrammatic Reasoning](http://math.ucr.edu/home/baez/universal/universal_hyper.pdf).

Book (recall that monads are also called 'triples'):

* Michael Barr and Charles Wells, [Toposes, Triples and Theories](http://www.cwru.edu/artsci/math/wells/pub/ttt.html).



[[!redirects algebra of a monad]]
[[!redirects algebra over a monad]]
[[!redirects monads]]