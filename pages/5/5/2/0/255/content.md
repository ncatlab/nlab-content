#Contents#

* It said "Tacit"!  So I took it. 
{:toc}

##Definition##

A _monad_ in any [[bicategory]] $B$ is a [[monoid]] in the endomorphism category on an object of $B$.

###Explicit description###

This means that a monad is

* an object $a$ of $B$;

* an [[endomorphism]] $a \stackrel{A}{\to} a$ on $a$;

* a 2-morphism 
$$
  \array{
    &&
    a
    \\
    & 
    {}^A\nearrow &\Downarrow^\mu& \searrow^A
    \\
    a
    &&\stackrel{A}{\to}&&
    a
  }
$$

* and a 2-morphism
$
  i : Id_a \Rightarrow A
$

* such that

  * $\mu$ is associative in the obvious sense;

  * $\mu$ is unital with respect to $i$ in the obvious sense.

This can be encoded as saying that

* A monad is a [[lax functor]] ${*} \to B$ from the [[point]] to $B$.

###In string diagrams###

These data and axioms can be expressed graphically in string diagrams.  The data $C \stackrel{T}{\to} C$, $1_C \stackrel{\eta}{\Rightarrow} T$, $T \circ T \stackrel{\mu}{\Rightarrow} T$ appear as:

[[monad-data-labeled.png:pic]]

Thanks to the distinctive shapes, one can usually omit the labels:

[[monad-data-unlabeled.png:pic]]

The axioms $\mu \cdot (\eta \circ T) = 1_C = \mu \cdot (T \circ \eta)$ and $\mu \cdot (T \circ mu) = \mu \cdot (\mu \circ T)$ then appear as:

[[monad-axioms-unlabeled.png:pic]]

+-- {: .query}
[[Peter LeFanu Lumsdaine]]: I did the diagrams with the monad called $(T,\eta,\mu)$ and have only just noticed that that disagrees with what's used in the preceding description.  Was there a particular principled reason for calling it $(A,i,\mu)$ above?  I can change the diagrams to agree if so, but if not, might it be easier on newcomers to use $(T,\eta,\mu)$ throughout?  Pretty much all the references I know use that as the generic name for a monad. ---Peter
=--

##Remarks##

* Originally monads were conceived and defined for $B =$ [[Cat]]. In parts of the literature "monad" still exclusively means monad in $Cat$. Similarly for algebras over monads.
Monads in $Cat$ are sometimes, mostly in older literature, also called **triple**s (alluding to the triple of data $(A,\mu,i)$). 


* We can picture a monad in $B$ as an image of the [[oriental|third oriental]] in $B$. See the remarks at [[monoidal category]].


## Examples ##

Monads on [[partial order|posets]] are particularly simple.  In fact, monads on [[power set]]s are extremely common throughout mathematics; they are known in less categorially-inclined circles as [[Moore closure]]s, and there are many examples there.

Every [[algebraic theory]] with a notion of free algebra defines a monad on [[Set]].  For example, the operation taking a set $S$ to the underlying set of the [[free monoid]] on $S$ may be extended to a monad, the [[list monad]].

An [[internalization|internal]] monad on the [[subobject classifier]] of a [[topos]] $E$ is a [[Lawvere-Tierney topology]] on $E$.


##Algebras/modules over a monad##

Given that a monad in $B$ is nothing but a [[monoid]] in a hom-category $B(a,a)$, it is natural to consider a [[module]] over this monoid: a [[module for a monad]].  This notion of module is more general than a module in a monoidal category, however, since it need not live in $B(a,a)$ but can be in $B(b,a)$ (for left modules) or $B(a,c)$ (for right modules).

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