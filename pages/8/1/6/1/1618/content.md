+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

* table of contents
{: toc}


## Definition ##

+-- {: .num_defn}
###### Definition

A **point $x$ of a [[topos]] $E$** is a [[geometric morphism]]

$$
  x : Set \stackrel{\overset{x^*}{\leftarrow}}{\underset{x_*}{\to}} E
$$

from the base topos [[Set]] to $E$. 

For $A \in E$ an object, its [[inverse image]] $x^* A \in Set$ under such a point is called the [[stalk]] of $A$ at $x$.

If $x$ is given by an [[essential geometric morphism]] we say that it is an **essential point** of $E$.

=--

+-- {: .num_remark}
###### Remark

Since [[Set]] is the [[terminal object]] in the category [[Topos|GrothendieckTopos]] of [[Grothendieck topos]]es, for $E$ a [[sheaf topos]] this is a [[global element]] of the topos.

Since $Set = Sh(*)$ is the [[category of sheaves]] on the one-point [[locale]], the notion of point of a topos is indeed the direct analog of a point of a [[locale]] (under [[localic reflection]]).

=--


+-- {: .num_defn #EnoughPoints}
###### Definition

A [[topos]] is said to have **enough points** if isomorphy can be tested [[stalk]]wise, i.e. if the 
[[inverse image]] functors from all of its points are jointly [[conservative functor|conservative]].

More explicity: $E$ has enough points if for any morphism $f : A \to B$, we have that if for every point $p$ of $E$, the morphism of [[stalks]] $p^* f : p^* A \to p^* B$ is an [[isomorphism]], then $f$ itself is an isomorphism.

=--

## Properties

### In presheaf toposes

+-- {: .num_prop}

###### Proposition

For $C$ a [[small category]], the points of the [[presheaf topos]] $[C^{op}, Set]$ are the [[flat functor]]s
$C \to Set$:

there is an [[equivalence of categories]]

$$
  Topos(Set, [C^{op}, Set])
  \stackrel{\overset{}{\leftarrow}}{\underset{}{\to}}
  FlatFunc(C,Set)
  \,.
$$

=--

This appears for instance as ([MacLaneMoerdijk, theorem VII.5.2](#MacLaneMoerdijk)).

### In localic sheaf toposes

For the special case that $E = Sh(X)$ is the [[category of sheaves]] on a [[category of open subsets]] $Op(X)$ of a [[sober topological space|sober]] [[topological space]] $X$ the notion of topos points comes from the ordinary notion of points of $X$.

For notice that

* $Set = Sh(*)$ is simply the [[topos]] of [[sheaf|sheaves]] on a one-[[point]] [[topological space|space]].  

* [[geometric morphisms]] $f : Sh(Y) \to Sh(X)$ between [[category of sheaves|sheaf topoi]] are in a bijection with continuous functions of topological spaces $f : Y \to X$ (denoted by the same letter, by convenient abuse of notation); for this to hold $X$ needs to be sober.

It follows that for $E = Sh(X)$ points of $E$ in the sense of points of topoi are in bijection with the ordinary points of $X$.

The action of the [[direct image]] $x_* : Set \to Sh(X)$ and the [[inverse image]] $x^* : Sh(X) \to Set$ of a point $x : Set \to Sh(X)$ of a sheaf topos have special interpretation and relevance:

* The [[direct image]] of a set $S$ under the point $x : {*} \to X$ is, by definition of [[direct image]] the sheaf
  $$
    x_*(S) : (U \subset X) \mapsto S(x^{-1}(U)) = 
    \left\{
      \array{
        S & \text{ if } x \in U
        \\
        {*} & \text{otherwise}
      }
    \right.
  $$
 This is the [[skyscraper sheaf]] $skysc_x(S)$ with value $S$ supported at $x$. (In the first line on the right in the above we identify the set $S$ with the unique sheaf on the point it defines. Notice that $S(\emptyset) = pt$).

* The [[inverse image]] of a sheaf $A$ under the point $x : {*} \to X$ is by definition of [[inverse image]] (see the [[Kan extension]] formula discussed there), the set
  $$
    \begin{aligned}
       x^*(A) & = 
       colim_{{*} \to x^{-1}(V)} A(V)
       \\
       &=
       colim_{V\subset X| x \in V} A(V)
    \end{aligned}
    \,.
  $$
  This is the [[stalk]] of $A$ at the point $x$,
  $$
    x^*(-) = stalk_x(-)
    \,.
  $$

By definition of [[geometric morphisms]], taking the stalk at $x$ is [[left adjoint]] to forming the skyscraper sheaf at $x$:

for all $S \in Set$ and $A \in Sh(X)$ we have
$$
  Hom_{Set}(stalk_x(A), S) \simeq
  Hom_{Sh(X)}(A, skysc_x(S))
  \,.
$$

Note that the observation that the points of $Sh(X)$ are in bijection with the points of $X$ actually factors over an intermediate concept, namely that of [[point of a locale|points of a locale]]. Firstly, any topological space gives rise to a locale; if the space is sober, its points are in bijection with the locale-theoretic points of the induced locale. Secondly, for any locale ([[topological locale|spatial]] or not), its locale-theoretic points correspond to the points of its induced sheaf topos.

### In sheaf toposes

The following characterization of points in [[sheaf toposes]] a special case of the general statements at [[morphism of sites]].


+-- {: .num_prop}
###### Proposition

For $C$ a [[site]], there is an [[equivalence of categories]]

$$
  Topos(Set, Sh(C))
  \simeq
  Site(C,Set)
  \,.
$$

(Morphisms of sites $C\to Set$ are precisely the [[cover-preserving functor|continuous]] [[flat functors]].)
=--

This appears for instance as ([MacLaneMoerdijk, corollary VII.5.4](#MacLaneMoerdijk)).


+-- {: .num_prop}
###### Proposition

If $E$ is a [[Grothendieck topos]] with enough points (def. \ref{EnoughPoints}), there is a  *[[small set]]* of points of $E$ which are jointly conservative, and therefore a [[geometric morphism]] $Set/X \to E$, for some set $X$, which is [[surjective geometric morphism|surjective]].  

=--

This appears as ([Johnstone, Lemma C2.2.11, C2.2.12](#Johnstone)).

(In general, of course, a topos can have a proper class of non-isomorphic points.)

+-- {: .num_prop}
###### Proposition

A Grothendieck topos has enough points (def. \ref{EnoughPoints}) precisely when it underlies a bounded [[ionad]].

=--

### In classifying toposes

From the above it follows that if $E$ is the [[classifying topos]] of a [[geometric theory]] $T$, then a point of $E$ is the same as a [[model]] of $T$ in [[Set]].


### Of toposes with enough points

+-- {: .num_prop}
###### Proposition

If a [[sheaf topos]] $E$ has _enough points_ (def. \ref{EnoughPoints}) then

* there exists a [[topological space]] $X$ whose [[cohomology]] and [[homotopy theory]] is the [[cohomology|intrinsic cohomology]] and [[homotopy groups in an (infinity,1)-topos|intrinsic homotopy theory]] of the topos;

* such that $E$ is the category of [[equivariant cohomology|equivariant]] objects in the [[sheaf topos]] $Sh(X)$ with respect to some groupoid action on $X$.

=--

This is due to ([Butz](#Butz)) and ([Moerdijk](#Moerdijk)).

## Examples 

### General

* For $X$ any [[topological space]], the  [[category of sheaves|topos of sheaves]] on (the [[category of open subsets]] of) $X$ has enough points (def. \ref{EnoughPoints}): a morphism of sheaves is a mono-/epi-/isomorphism precisely if it is so on every [[stalk]]. 

* Points of [[over-toposes]] are discussed at <a href="http://ncatlab.org/nlab/show/over-topos#Points">over topos -- points</a>.

### Rings and algebraic theories
 {#Rings}

The category of points of the presheaf topos over $Ring_{fp}^{op}$, the dual of the category of finitely presented [[rings]], is the category of all rings (without a size or presentation restriction). In fact this holds for any [[algebraic theory]], not only for the theory of commutative rings. See also at  _[[Gabriel-Ulmer duality]]_, _[[flat functors]]_.



### Of a local topos

A [[local topos]] $(\Delta \dashv \Gamma \dashv coDisc) : E \to Set$ has a canonical point, $(\Gamma \dashv coDisc) : Set \to E$. Morover, this point is an [[initial object]] in the category of all points of $E$ (see _[Equivalent characterizations](local+geometric+morphism#EquivalentCharacterizations)_ at _[[local topos]]_.)

### Over $\infty$-cohesive sites

* Let [[Diff]] be a [[small category]] version of the category of smooth manifolds (for instance take it to be the category of manifolds embedded in $\mathbb{R}^\infty$). Then the sheaf topos $Sh(Diff)$ has precisely one point $p_n$ per natural number $n \in \mathbb{N}$ , corresponding to the $n$-ball: the [[stalk]] of a sheaf on $Diff$ at that point is the colimit over the result of evaluating the sheaf on all $n$-dimensional smooth balls.

  This is discussed for instance in ([Dugger, p. 36](#Dugger)) in the context of the [[model structure on simplicial presheaves]].



### Toposes with enough points

The following classes of topos have enough points (def. \ref{EnoughPoints}).

* every [[presheaf topos]];

* every [[coherent topos]] (due to the [[Deligne completeness theorem]]);

* every [[Galois topos]] (see ([Zoghaib](#Zoghaib))).

### Toposes without points

In contrast with point-set topology where non empty spaces tautologically have points there are non trivial toposes lacking points just like in pointfree topology there are nontrivial [[locale|locales]] without points. From a logical perspective these toposes correspond to consistent [[geometric theory|geometric theories]] lacking models in Set. Classical examples are provided by toposes of sheaves on complete atomless Boolean algebras (see Barr ([1974](#Barr74)) or for an example due to [[Pierre Deligne|Deligne]] [[SGA4]], p.412).

## Related concepts

* [[topological locale]]

* [[Barr's theorem]]

* [[point of a locale]]

* [[point of an (infinity,1)-topos]]

## References ##

Textbook references are section 7.5 of 

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_
  {#MacLaneMoerdijk}

as well as section C2.2 of 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
 {#Johnstone}

In 

* Carsten Butz, _Logical and cohomological aspects of the space of points of a topos_ ([web](http://www.academia.edu/9139781/Logical_and_Cohomological_Aspects_of_the_Space_of_Points_of_a_Topos))
 {#Butz}

is a discussion of how for every topos with enough points there is a [[topological space]] whose [[cohomology]] and [[homotopy theory]] is related to the [[cohomology|intrinsic cohomology]] and [[homotopy groups in an (infinity,1)-topos|intrinsic homotopy theory]] of the topos.

More on this is in

* [[Ieke Moerdijk]], _Classifying spaces for toposes with enough points_ , Milan Journal of Mathematics Volume 66, Number 1, 377-389
 {#Moerdijk}

See also

* Sam Zoghaib, _A few points in topos theory_ ([pdf](http://www.normalesup.org/~zoghaib/math/points-tt.pdf))
 {#Zoghaib}

Points of the sheaf topos over the category of [[manifold]]s are discussed in

* [[Dan Dugger]], _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf))
 {#Dugger}


Toposes without points are discused in the homonymous paper

* {#Barr74} [[Michael Barr]], *Toposes without points*, J. Pure Appl. Algebra **5** (1974) 265-280 &lbrack;[pdf](https://www.math.mcgill.ca/barr/papers/top.no.pt.pdf), [[Barr-ToposesWithoutPoints.pdf:file]]&rbrack;

[[!redirects points of a topos]]

[[!redirects points of toposes]]
[[!redirects points of topoi]]

[[!redirects point of topos]]

[[!redirects enough points]]
[[!redirects topos with enough points]]
[[!redirects topos without points]]
[[!redirects pointless topos]]

[[!redirects topos point]]
[[!redirects topos points]]

