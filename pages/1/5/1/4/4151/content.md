
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Basic localizers
* table of contents
{: toc}

## Idea

By a _basic localizer_ one means a [[localizer]] on the category [[Cat]] of [[categories]], hence a choice of a [[class]] of [[functors]] to be called the _[[weak equivalences]]_, subject to some conditions. 

These conditions ensure in particular that a basic localizer always contains the weak equivalences of the [[Thomason model structure]] on [[Cat]] (see [Maltsiniotis 11, 1.2.1](#Maltsiniotis11)), the [[localization]] at which is equivalent to the standard [[homotopy category]]. On the other hand, the standard [[equivalences of categories]], which are the weak equivalences in the [[canonical model structure]] on [[Cat]], do not form a basic localizer. 

Hence basic localizers are a tool for [[homotopy theory]] modeled on [[category theory]]. In fact, their introduction by [[Grothendieck]] was motivated from the study of [[test categories]] (see remark \ref{CitationOnTestCategories} below).



## Definition

The definition is due to [[Grothendieck]]: 

+-- {: .num_defn #BasicLocalizer}
###### Definition

A **basic localizer** is a [[class]] $W$ of [[morphisms]] in [[Cat]] such that

1. $W$ contains all [[identities]], satisfies the [[2-out-of-3 property]] and is closed under [[retracts]] (in the literature this is sometimes called being *weakly saturated*),

1. If $A$ has a [[terminal object]], then the functor $A\to 1$ is in $W$, and

1. Given a commutative triangle in $Cat$:
   $$\array{ A & & \overset{u}{\to} & & B\\ & _v \searrow & & \swarrow_w \\ & & C } $$
   if each induced functor $v/c \to w/c$ between [[comma categories]] is in $W$, then $u$ is also in $W$.

=--

+-- {: .num_remark}
###### Remark

The term in French is **localisateur fondamental**, which is sometimes translated as **fundamental localizer**.

=--

+-- {: .num_remark #CitationOnTestCategories}
###### Remark

In [[Pursuing Stacks]] [[Grothendieck]] wrote about def. \ref{BasicLocalizer} the following:

> These conditions are enough, I quickly checked this night, in order to validify all results developed so far on [[test categories]], [[weak test categories]], [[strict test categories]], weak test functors and test functors (with values in $(Cat)$) (of notably the review in par. 44, page 79&#8211;88), provided in the case of test functors we restrict to the case of loc. cit. when each of the categories $i(a)$ has a final object. All this I believe is justification enough for the definition above.

=--

## Examples

* The class of *all* functors between small categories is, of course, the maximal basic localizer.

* The class of functors inducing an [[isomorphism]] on [[connected components]] is a basic localizer.

* The class of functors whose [[nerve]] is a [[weak homotopy equivalence]] is a basic localizer. (These are the [[weak equivalences]] in the [[Thomason model structure]].)

* For any [[derivator]] $D$, the class of $D$-equivalences is a basic localizer.  This includes all the previous examples.

* The class of [[equivalences of categories]] is *not* a basic localizer (it fails the second condition). (These are the weak equivalences of the [[canonical model structure]].)


## Properties

### Asphericity and local equivalences

If $W$ is a basic localizer, we define the following related classes.  We sometimes refer to functors in $W$ as *weak equivalences*.

* A category $A$ is **($W$-)aspherical** if $A\to 1$ is in $W$.  Thus the second axiom says exactly that any category  with a terminal object is aspherical.
* A functor $u\colon A\to B$ is **($W$-)aspherical** if for all $b\in B$, the comma category $u/b$ is aspherical.
* When the hypotheses of the third axiom are satisfied, we say that $u$ is a **local weak equivalence over $C$**.  Thus the third axiom says exactly that every local weak equivalence is a weak equivalence.

+-- {: .num_example}
###### Example
If $W = \pi_0$-equivalences, then a category is aspherical iff it is connected, and a functor is aspherical iff it is [[initial functor|initial]].
=--

+-- {: .num_example}
###### Example
If $W = $ nerve equivalences, then a category is aspherical iff its nerve is contractible, and a functor is aspherical iff it is [[homotopy initial functor|homotopy initial]].
=--

We observe the following.

* A category $A$ is aspherical iff the functor $A\to 1$ is aspherical, since the only comma category involved in the latter assertion is $A$ itself.

* An aspherical functor is a weak equivalence.  For if $u\colon A\to B$ is aspherical, then consider the triangle
  $$\array{ A & & \overset{u}{\to} & & B\\ & _u \searrow & & \swarrow \\ & & B } $$
  The third axiom tells us to consider, for a given $b\in B$, the functor $u/b \to B/b$.  But $u/b$ is aspherical by assumption, while $B/b$ is aspherical by the second axiom since it has a terminal object.  Thus, by 2-out-of-3, the functor $u/b \to B/b$ is in $W$, and thus by the third axiom $u$ is in $W$.

* If $u$ has a right adjoint, then it is aspherical.  For in this case, each category $u/b$ has a terminal object, and thus is aspherical.

* If $I$ denotes the [[interval category]], then for any category $A$ the projection $A\times I\to A$ has a right adjoint, hence is aspherical and thus a weak equivalence.  By 2-out-of-3, the two injections $A \rightrightarrows A\times I$ are also weak equivalences, so $A\times I$ is a [[cylinder object]] for $W$.  It follows that if we have a natural transformation $f\to g$, then $f$ is in $W$ if and only if $g$ is.  Moreover, if $f$ is a "homotopy equivalence" in the sense that it has an "inverse" $g$ such that $f g$ and $g f$ are connected to identities by arbitrary natural zigzags, then $f$ is a weak equivalence.

* In particular, any left or right adjoint is a weak equivalence.

### Self-duality

It is a non-obvious fact that the notion of basic localizer is self-dual.

+-- {: .num_theorem}
###### Theorem
A functor $u : A \to B$ is in a basic localizer $W$ if and only if $u^{op} : A^{op} \to B^{op}$ is in $W$.
=--

+-- {: .proof}
###### Proof
See Proposition 1.2.6 in ([Cisinski 04](#Cisinski04)).
=--


### Cisinski's theorem

Since the definition consists merely of closure conditions, the intersection of any family of basic localizers is again a basic localizer.  It follows that there is a unique *smallest* basic localizer.  The following was conjectured by [[Grothendieck]] and proven by [[Denis-Charles Cisinski]].

+-- {: .num_theorem}
###### Theorem (Cisinski)
The class of functors whose [[nerve]] is a [[weak homotopy equivalence]] is the smallest basic localizer.
=--

+-- {: .proof}
###### Proof
See Th&#233;or&#232;me 2.2.11 in ([Cisinski 04](#Cisinski04)).
=--


Note that this is a larger class than the class of "[[homotopy equivalences]]" considered above.  For instance, the category generated by the graph
$$\bullet \leftarrow \bullet \rightarrow \bullet \leftarrow \bullet \rightarrow \bullet \leftarrow \bullet \rightarrow \cdots$$
has a contractible nerve, but its identity functor is not connected to a constant one by any natural zigzag.

## Related concepts

* [[canonical model structure]], [[Thomason model structure]] on [[Cat]]

* [[Cisinski model structure]]

## References

* [[Denis-Charles Cisinski]], _[[joyalscatlab:Les préfaisceaux comme type d'homotopie]]_, Ast&#233;risque, Volume 308, Soc. Math. France (2006), 392 pages ([pdf](http://www.math.univ-toulouse.fr/~dcisinsk/ast.pdf))
 {#Cisinski06}

* [[Denis-Charles Cisinski]], _Le localisateur fondamental minimal_, Cahiers de Topologie et Géométrie Différentielle Catégoriques, Tome 45 (2004) no. 2, pp. 109-140, [numdam](http://www.numdam.org/item/CTGDC_2004__45_2_109_0/)
 {#Cisinski04}

See also at _[[Cisinski model structure]]_.


* [[Georges Maltsiniotis]], _Homotopical exact squares and derivators_ ([arXiv:1101.4144](http://arxiv.org/abs/1101.4144))
 {#Maltsiniotis11}


[[!redirects basic localizor]]
[[!redirects basic localizors]]
[[!redirects basic localizers]]
[[!redirects basic localiser]]
[[!redirects basic localisers]]
[[!redirects fundamental localizer]]
[[!redirects fundamental localizers]]
[[!redirects fundamental localiser]]
[[!redirects fundamental localisers]]
[[!redirects localisateur fondamental]]
