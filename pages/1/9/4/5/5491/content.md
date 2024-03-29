+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In full generality, an **$\infty$-representation** is an [[∞-action]] of some [[higher algebra|higher algebraic]] structure on some object in a [[higher category theory|higher category]] up to [[coherent]] [[homotopy]]. One also speaks of _representation up to homotopy_ or maybe _sh-representations_ .

We motivate the general notion of $\infty$-representation by recalling first some [[category theory|category theoretic]] aspects of the ordinary notion of representation, and then leading over to the analogous [[(∞,1)-category theory|(∞,1)-category theoretic]] notions.

### Representations as functors


Recall that for $G$ a [[discrete group]] with [[delooping]] [[groupoid]] $\mathbf{B}G = (G \stackrel{\to}{\to})$, and $k$[[Vect]] the category of [[vector space]]s (over some base [[field]] $k$), ordinary linear [[representation]]s of $G$ are equivalently [[functor]]s

$$
  \rho : \mathbf{B}G \to k Vect
  \,.
$$

Such a functor takes the single object of $\mathbf{B}G$ to some vector space $V$ and takes every morphism $(* \stackrel{g}{\to} * )$ in $\mathbf{B}G$ labeled by an element $g \in G$ to a linear [[automorphism]] $\rho(g) : V \to V$ such that composition and the identity is respected. We have an [[equivalence of categories]]

$$
  Func(\mathbf{B}G, k Vect) \simeq Rep_k(G)
  \,.
$$

Here the category $Vect$ could be replaced by other categories and they need not be [[abelian categories]] or otherwise linear for the above to make sense. For instance if we take instead the category [[Set]] itself, then a functor

$$
  \rho : \mathbf{B}G \to Set
$$

is what is called a [[permutation representation]]. In [[topology]] one is interested in representations in [[Top]]

$$
  \rho : \mathbf{B}G \to Top
  \,.
$$

(However, rarely is it sufficient to regard these just as functors to the 1-category $Top$. Instead, in order to speak about topological [[fiber bundle]]s and fibrations, one needs to regard [[Top]] here as an [[(∞,1)-category]] and regard $\rho : \mathbf{B}G \to Top$ as an [[(∞,1)-functor]]. This we come to below in [∞-Representations](#IdeaInfRepresentations))


Moreover, we may replace $\mathbf{B}G$ by a more general [[groupoid]]. For $K$ any groupoid, a functor

$$
  \rho : K \to k Vect
$$

is called a linear representation of $K$. This now picks not just a single vector space $V \in Vect$, but one vector space $V_x$ for each [[object]] $x \in K$. And to each morphism $(x \stackrel{g}{\to} y)$ in $K$ is assigns a [[linear map]] $\rho(g) : V_x \to V_y$.

For instance if $K = \Pi_1(X)$ is the [[fundamental groupoid]] of a [[manifold]] $X$, then a representation

$$
  \rho : \Pi(X) \to vect
$$

is a [[vector bundle]] over $X$ with [[curvature|flat]] [[connection on a bundle]].

And we do not even need to assume that $K$ here is a groupoid. For instance if $D$ is a [[directed graph]] (or [[quiver]]) and $F(D)$ its [[path category]], then a functor

$$
  F(D) \to Vect
$$

is called a [[quiver]]-representation of $D$. 

One could in principle therefore speak of a functor

$$
  F(D) \to Set
$$

as a "quiver permutation representation", but there does not seem to be much use of this terminology in practice. The examples do show, however, that there is considerable overlap between the notion of _[[representation]]_ and of _[[functor]]_ .


### Structured representations as morphisms in 2-toposes

Still a bit more generally, we can speak of representations that preserve extra structure, such as [[smooth structure]]. For instance for $G$ a [[Lie group]] we have that $\mathbf{B}G$ is a [[Lie groupoid]]: an object in the [[(2,1)-topos]] of [[(2,1)-sheaves]] over the [[site]] $C = $ [[CartSp]] or $C =$ [[Diff]].

We may also promote the category [[Vect]] to this $(2,1)$-topos, by replacing it by the [[stack]] $VectBund$, which assigns to each test manifold $U \in C$ the groupoid of smooth [[vector bundle]]s over $U$. Then a morphism

$$
  \rho : \mathbf{B}G \to VectBund
$$

in the [[(2,1)-topos]] $Sh_{(2,1)}(C)$ is a _smooth representation_ of $G$, in that the linear automorphisms $\rho(g) : V \to V$ depend smoothly on the point $g \in G$. 


We can recover the underlying ordinary representation by applying the [[global section]] functor $\Gamma : Sh_{(2,1)}(C) \to Grpd$. This is given by evaluating every thing on the [[terminal object]] ${*} \in C$, which here is just the ordinary [[point]], regarded as a smmoth manifold.

This yields the underlying bare representation

$$
  \Gamma(\rho) : \mathbf{B}G \to Vect
  \,.
$$

Conversely, one finds that extending such a bare representation from the point to all test spaces in $C$ amounts to equipping it with smooth structure.

As before, this is not restricted to [[connected]] objects: we may replace $\mathbf{B}G$ here with any [[Lie groupoid]]. For instance for $X$ a [[smooth manifold]] and $\mathbf{P}_1(X)$ is smooth [[path groupoid]] a representation

$$
  \rho : \mathbf{P}_1(X) \to VectBund
$$

as a morphism in the 2-topos is a [[vector bundle]] on $X$ with [[connection on a bundle]]. Or if we consider non-linear representations, a representation

$$
  \rho : \mathbf{P}_1(X) \to \mathbf{B}G
$$

is a $G$-[[principal bundle]] with [[connection on a bundle]] on $X$. See [[parallel transport]] for more details and references.


By just changing the [[site]] here, we can implement other geometric structures. For instance for $G$ an [[algebraic group]] we may think of $\mathbf{B}G$ as an [[algebraic stack]] over something like the [[fppf-site]]  structure $C = CAlg_k^{op}$ on formal duals of commutative $k$-algebras or similar.

In this case there is a well-known good generalization of $VectBund$: instead of just vector bundles we can consider their completion to [[quasicoherent sheaves]]. The stack of these is the object in the [[(2,1)-topos]] given by

$$  
  QC : Spec A \mapsto A Mod
  \,,
$$

where on the right we have the groupoid of [[module]]s over $A$. Over the point this is again just a $k$-module hence a [[vector space]] and hence a representation

$$
  \rho : \mathbf{B}G \to QC
$$

of an algebraic group is a representation of $G$ on a vector space. 

But also here we may allow the represented structure to have more than one object. For instance for $X$ any [[scheme]] regarded as an object in $Sh_{(2,1)}(C)$ a representation of $X$ in the context of $QC$ is a morphism

$$
  \rho : X \to QC
  \,,
$$

which is equivalently a [[quasicoherent sheaf]] of modules on $X$. As before, we may think of this as assigning to each point of $X$ one representation space, only that in a scheme $X$ there are no morphisms that would act on these.

But more generally for $K$ an [[algebraic stack]], a representation

$$
  \rho : K \to QC
$$

assigns to each point of $K_0$ a representation space, such that these glue together to a quasicoherent sheaf of modules, and to each [[morphism]] in $K$ a morphism between the corresponding representation spaces, as before.


Analogous constructions are available for more general sites, effectively we can take $C$ to be the [[opposite category]] of $T$-[[algebras over a Lawvere theory]] for $T$ any [[algebraic theory]] that contains the theory of [[abelian group]]s. If for instance we take $T =$ [[CartSp]] we are back to the smooth case discussed before.

Also notice that if we take the site to be the point, $C = *$, then sheaves over it are just sets and stacks over it are just bare groupoids, so that we recover the discussion at the very beginning.

### $\infty$-Representations  {#IdeaInfRepresentations}

We have found above the term "representation" is, to a large extent, congruent with the term "morphism in a (2,1)-topos with codomain a stack of modules".

This way of thinking of representations has an immediate generalization to [[higher category theory]] and in particular to [[(∞,1)-category theory]]/[[homotopy theory]].

To start with the simple discussion over the point again, a model for a notion of a category of $\infty$-modules that is useful is an [[(∞,1)-category]] $Ch_\bullet(k)$ that is [[presentable (∞,1)-category|presented]] by a [[model structure on chain complexes]].

If again $G$ is a [[discrete group]], then an  [[(∞,1)-functor]] (equivalently: a "strong homotopy-functor" or "homotopy coherent functor", see there for details)

$$
  \rho : \mathbf{B}G \to Ch_\bullet(k)
$$

assigns 

* to the single obect of $\mathbf{B}G$ a chain complex $V_\bullet$;

* to a group element $g \in G$ a chain map $\rho(g) : V_\bullet \to V_\bullet$;

* to a pair of group elements $g, g'$ a chain homotopy

  $\rho(g,g') : \rho(g')\circ\rho(g) \Rightarrow \rho(g' g)$;

* to a triple of group elements a homotopy of homotopies between composites of $\rho(g,g'), \rho(g,g'')$ and $\rho(g',g'')$ and so on

  (see the diagrams at [[group cohomology]] for more details in low degree).

In other words, this is much like representation of $G$ as before on an ordinary vector space, only that now the action property of $\rho$ holds only _up to [[coherent]] [[homotopy]]_ . Therefore people also speak of _representations up to homotopy_ ([AbadCrainic](#AbadCrainic)) as well as 
_strong homotopy representations_ and many other variants.  

As before, there is in principle no reason to restrict oneself to representations of groupoids here. For $K$ any [[∞-groupoid]] or even [[(∞,1)-category]] (recall the [[quiver]] representations) and for $Mod$ any [[(∞,1)-category]] of $\infty$-modules (for instance as [[presentable (∞,1)-category|presented]] by a [[model structure on modules over an algebra over an operad]]) we may call an [[(∞,1)-functor]]

$$
  \rho : K \to Mod
$$

an $\infty$-representation of $K$.

If we wish to consider $\infty$-generalizations of [[permutation representation]]s we can also consider more general codomain $(\infty,1)$-categories here. For instance if we take [[∞Grpd]] itself, then an  $\infty$-permutation representation

$$
  K \to \infty Grpd
$$

is known as an [[(∞,1)-presheaf]]. For $K$ the [[delooping]] of an ordinary group or the [[orbit category]] of a [[topological group]], such appear genuinely from the point of view of representations for instance in [[equivariant cohomology]] and [[orbit category|equivariant homotopy]]  theory. Notice that by the [[homotopy hypothesis]]-theorem we have an [[equivalence of (∞,1)-categories]]

$$
  \infty Grpd \simeq Top
$$ 

so that the above is equivalently an [[(∞,1)-functor]]

$$
  K \to Top
$$

hence literally a _representation up to homotopy_ in the classical sense of [[homotopy theory]].

As before, all this may be lifted from the point into large classes of [[(∞,1)-topos]]es  to equip the notion of $\infty$-representation with geometric structure (algebraic structure, smooth structure, etc.)

There are then analogs of the above relation between representations of path groupoids and connections on bundles. For more on this see [[higher parallel transport]]. Quite generally, in every [[locally ∞-connected (∞,1)-topos]] $\mathbf{H}$ there is a notion of [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos|fundamental ∞-groupoid]] $\mathbf{P}(X)$ of any object $X$. Representation of $\mathbf{\Pi}(X)$ define general abstract <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity,1)-topos#FlatDifferentialCohomology">flat differential cohomology</a> and [[local system]]s on $X$, generally also in [[nonabelian cohomology]] (see there for some more properties and examples).



For instance [[dg-geometry]] is the study of the [[(∞,1)-topos]] over an [[(∞,1)-site]] of formal duals of [[dg-algebra]]s. Again there is the canonical [[∞-stack]] 

$$
  QC : Spec A \mapsto A Mod
$$

on this site, where now however $A Mod$ denotes the [[∞-groupoid]] (or [[(∞,1)-category]] if we do a more comprehensive discussion) of [[chain complex]]es equipped with the structure of a [[module]] ove the dg-algebra $A$.

For $X$ any [[∞-stack]] then a morphism

$$
  \rho : X \to QC
$$

is a equivalently a [[quasicoherent ∞-stack]] of modules on $X$, or an $\infty$-representation with "dg-algebraic structure".

If one replaces $X$ here by its [[de Rham space|de Rham stack]] $X_{dR}$ then dg-algebraic $\infty$-representations

$$
  \rho : X_{dR} \to QC
$$

are [[D-module]]s on $X$.

A discussion of these higher categorical structure in [[representation theory]] is in ([Ben-ZviNadler](#Ben-ZviNadler)).


### $n$-Representations

If the codomain $Mod$ is  an [[(∞,1)-category]] that is just a [[(n,1)-category]] (all [[k-morphisms]]s for $k \gt n$ are effectively identities) then an $\infty$-representation is called an **$n$-representation**. These are _representations up to homotopy_ where from degree $n$ on all homotopies are actually identities: $n$-[[truncated]] representations up to homotopy.

As always in [[higher category theory]], the cases for low $n$ are more restrictive but typically admit a more tractable detailed analysis and construction.

2-representations of [[2-groups]] and [[Lie 2-group]]s on various variants of [[2-vector space]]s have been considered for instance in ([Schreiber](#Schreiber),  [BaezBaratinFreidelWise](#BaezBaratinFreidelWise), and other places).

In analogy to the case for $n=1$, 2-Representations $\mathbf{P}_2(X) \to 2 Vect$ of the smooth [[path 2-groupoid]] of a [[smooth manifold]] describe [[connections on a 2-bundle]]. See there for more details.

## Definition
 {#Definition}

### In homotopy type theory
 {#InHomotopyTypeTheory}

In a general abstract context of [[homotopy type theory]] we may define $\infty$-representations as follows.

For $\mathbf{H}$ an [[(∞,1)-topos]], let $G \in Grp(\mathbf{H})$ be a [[group object in an (∞,1)-category|group object]] in $\mathbf{H}$, hence an [[∞-group]]. Then the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}G}$ over its [[delooping]] is the [[(∞,1)-category]] of [[∞-actions]] of $G$

$$
  Act(G) \simeq \mathbf{H}_{/\mathbf{B}G}
  \,,
$$

hence of possibly "non-linear" $\infty$-representations. (See at _[[∞-action]]_ for details). A genuine (linear) $\infty$-representation is then an  [[abelian ∞-group]] object in $Act(G)$.

## Related concepts

* [[(∞,1)-module bundle]]

* [[action]], [[∞-action]]

* [[module]], [[∞-module]]

* [[representation]], **$\infty$-representation**

  * [[2-representation]],

* [[associated bundle]], [[associated ∞-bundle]]

[[!include homotopy type representation theory -- table]]

## References

2-representations of [[2-groups]] and [[Lie 2-group]]s such as the [[string 2-group]] on [[2-vector space]]s are disscussed in

* {#Schreiber}[[Urs Schreiber]], _AQFT from $n$-functorial QFT_ 
  ([arXiv:0806.1079](http://arxiv.org/abs/0806.1079)) (appendix)


* {#BaezBaratinFreidelWise} [[John Baez]], Aristide Baratin, Laurent Freidel, Derek Wise, _Infinite-Dimensional Representations of 2-Groups_ ([arXiv:0812.4969](http://arxiv.org/abs/0812.4969))


References for 2- and 3-representations of [[path n-groupoid]]s are at [[higher parallel transport]].

$\infty$-Representations of [[groupoids]] and [[Lie algebroid]]s on $(\infty,1)$-categories of chain complexes are discussed under the term  _representations up to homotopy_ in

* {#AbadCrainic} [[Camilo Arias Abad]], [[Marius Crainic]] , _Representations up to homotopy and Bott's spectral sequence for Lie groupoids_ ([arXiv](http://arxiv.org/abs/0911.2859))


A discussion of quasicoherent $\infty$-stacks and D-modules in the context of [[representation theory]] is for instance in

* {#Ben-ZviNadler} [[David Ben-Zvi]], [[David Nadler]], 

  _The character theory of a complex group_ ([arXiv:0904.1247](http://arxiv.org/abs/0904.1247))

  _Loop Spaces and Representations_ ([arXiv:1004.5120](http://arxiv.org/abs/1004.5120))


[[!redirects infinity-representations]]
[[!redirects ∞-representation]]
[[!redirects ∞-representations]]
[[!redirects representation up to homotopy]]
[[!redirects representations up to homotopy]]