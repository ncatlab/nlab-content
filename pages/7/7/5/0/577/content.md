# Cartesian monads
* tic
{: toc}


##Idea##

A cartesian monad is a [[monad]] on a [[locally cartesian category]] that gets along well with [[pullbacks]].


##Motivation through generalised multicategories

Ordinary [[categories]] can be defined as [[monad|monads]] in the [[bicategory]] of [[spans]] of [[sets]]. Multicategories can be defined in a similar way. (A [[multicategory]] is like an ordinary category where each morphism has a list of objects as its domain, and a single object as its codomain; think [[Vect|vector spaces and multilinear maps]]).

To see how a multicategory $C$ can be defined as a monad in some appropriate bicategory, let $C_0$ be the set of objects of $C$, and notice that the domain of a morphism of $C$--a finite list of objects--is an element of $T C_0$, where $T$ is the [[free monoid]] monad. In this way the data for $C$ can be conveniently organized in the diagram
\[\begin{matrix}
&&C_1&&\\
&\overset{d}\swarrow&
&\overset{c}\searrow&\\
T C_0 &&&& C_0.
\end{matrix}\]

[[Tom Leinster]] built on the idea of [[generalized multicategory|generalized multicategories]], where the domain of a morphism can have a more general, higher dimensional shape than just a list. This is accomplished by considering a category $\mathcal{E}$ other than $\mathrm{Set}$, and a monad $T$ on $\mathcal{E}$, and mimicking the above construction. So the data for a $T$-multicategory is a digram in $\mathcal{E}$ like the one above.

To state the structure required on the data for a $T$-multicategory, we want to define a bicategory in which the above span is an [[endomorphism]]. Then a $T$-multicategory will be such a span together with structure making it a monad in that bicategory. The bicategory is $\mathcal{E}_{(T)}$, the bicategory of $T$-spans in $\mathcal{E}$. Its objects are the objects of $\mathcal{E}$, and its morphisms are spans
\[\begin{matrix}
&&M&&\\
&\overset{d}\swarrow&
&\overset{c}\searrow&\\
T E &&&& E'.
\end{matrix}\]

This won't in general be a bicategory without a few extra assumptions. Identity spans are defined using the unit $\eta: \mathrm{Id}\to T$. Composition of spans is defined using [[pullbacks]] and the multiplication $\mu: T^2\to T$, so the category $\mathcal{E}$ must at least have pullbacks--usually it will be [[finitely complete category|finitely complete]]. The associativity and unit $2$-cells are defined using the universal property of the pullbacks. However, these $2$-cells won't in general be invertible. In fact, it turns out that requiring the monad $T$ to be _cartesian_ is exactly what is needed to ensure that the coherence $2$-cells are isomorphisms, and hence that $T$-spans do in fact form a bicategory. Maybe this should be the "fundamental theorem of cartesian monads".

Extending Bounabou's observation that a [[small category]] is a monad in $Cat$, Burroni defined  $T$-multicategories as _monads in the bicategory_ $\mathcal{E}_{(T)}$ from above. When $T$ is the [[identity monad]] on $\mathrm{Set}$, $T$-multicategories reduce to small categories, and when $T$ is the free monoid monad on $\mathrm{Set}$, $T$-multicatories are exactly ordinary small multicategories.

As an indication of how this theory is useful as a language for higher categories, take $T$ to be the free [[strict ∞-category]] monad on the category of [[globular set]]s. Then $T$-multicategories with exactly one object are called [[globular operad]]s, and Leinster defines one such globular operad (the initial "globular operad with contraction") for which the algebras are [[weak ∞-categories]].


##Definition#

Let $(T, \mu, \nu)$ be a
[[monad]] on a category $C$.
Specifically, $T: C \to C$ is a functor,
and $\mu: T^2 \to T$ and 
$\nu: \mathrm{Id}_C \to T$ are natural
transformations, satisfying unital and associative
axioms making $T$ a monoid in the (strict)
monoidal category $\mathrm{End}(C)$.
This monad is cartesian if

* the category $C$ has all [[pullback]]s,
* the functor $T$ preserves pullbacks,
* the natural transformations $\mu$ and $\nu$
  are cartesian.
  A natural transformation $\alpha: S \to T$
  between functors $C \to D$
  is cartesian if for each map $f: A \to B$
  in $C$, the naturality square
  \[\array{
    S A & \overset{S f}{\to} & S B \\
    \alpha_A \downarrow & & \downarrow \alpha_B \\
    T A & \underset{T f}{\to} & T B
  }\]
  is a pullback.


## Examples

* The free [[monoid]] monad $(-)^*: Set \to Set$ is cartesian. 

* The free [[category]] monad acting on [[directed graph]]s is cartesian.

* The free strict $\omega$-[[strict omega-category|category]] monad acting on [[globular set]]s, $T: Set^{G^{op}} \to Set^{G^{op}}$, is cartesian. 


##Remarks

There is some slight inconsistency in the use of
the word _cartesian_ in category theory.
Sometimes, a category is called cartesian if it [[finitely complete category|has all finite limits]];
similarly, a functor is called cartesian if it [[exact functor|preserves all finite limit]]s.
In most examples of cartesian monads, the category
$C$ has a [[terminal object]], and hence finite limits.
However, the functor $T$ almost never preserves
terminal objects.
For example, the free monoid monad on
$\mathrm{Set}$ is cartesian, as can be checked
directly, but $T 1 \simeq \mathbb{N}$ is not
a terminal object.
In this sense, a cartesian monad is really *locally* cartesian.


##References

* [[Tom Leinster]], _Higher Operads, Higher Categories_ 
  ([arXiv](http://arxiv.org/abs/math.CT/0305049)),
  section 4.1

* A. Burroni, _$T$-cat&#233;gories (cat&#233;gories dans un triple)_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 12 no. 3 (1971), p. 215-321 ([numdam](http://www.numdam.org/item?id=CTGDC_1971__12_3_215_0))

* [blog comment](http://golem.ph.utexas.edu/category/2009/07/the_monads_hurt_my_head_but_no.html#c025402) giving the Motivation above


## Discussion ##

Some past discussion about the term 'cartesian' has been moved to [[locally cartesian category]].


[[!redirects cartesian monads]]
[[!redirects Cartesian monad]]
[[!redirects Cartesian monads]]