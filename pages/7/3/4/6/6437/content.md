
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Phyiscs
+--{: .hide}
[[!include physicscontents]]
=--
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
=--
=--




> This is a sub-entry of [[sigma-model]]. See there for background and context.

***


#Contents#
* table of contents
{:toc}

## Exposition of higher gauge theories as $\sigma$-models


We discuss how [[gauge theories]] and their higher analogs are 
naturally regarded as $\sigma$-models.



### Higher geometric target spaces
 {#HigherGeometricTargetSpaces}

The [[sigma-model -- exposition of classical sigma-models|classical sigma-models]] all have [[target space]]s that are [[smooth manifold]]s. However, we saw that from [[dimension]] $d \geq 2$ on, the [[background gauge field]]s on these target spaces are naturally no longer just [[principal bundle]]s [[connection on a bundle|with connection]]: instead they are smooth [[principal 2-bundle]]s, then smooth principal 3-bundles, etc. and eventually generally [[principal ∞-bundle]]s with [[connection on an ∞-bundle|∞-connections]]. But the total [[space]] of such higher smooth bundles is no longer in general a [[smooth manifold]]: instead, the total space is a _[[Lie groupoid]]_ for $d = 2$, then a _[[Lie 2-groupoid]]_ for $d = 3$ and eventually generally a [[smooth ∞-groupoid]].

This means that -- unless we would artifically treat the total space of a [[background gauge field]] bundle on different grounds than its base space -- the general theory of $\sigma$-models should naturally include target spaces that are not just smooth manifolds. 

At least from $d = 2$ on, for instance, target spaces should be allowed to be [[Lie groupoid]]s. This has a fairly long tradition: the _[[proper groupoid|proper]] [[étale groupoid|étale]]_ [[Lie groupoid]]s are precisely _[[orbifold]]s_, spaces that are locally isomorphic to sufficiently nice quotients of a [[Cartesian space]] by a [[group]] [[action]]. Orbifolds have received a lot of attention in the study of [[string]] [[sigma-model]]s. The [[orientifold]] background gauge fields mentioned [before](http://ncatlab.org/nlab/show/sigma-model+--+exposition+of+classical+sigma-models#RelativisticString) involve in general a $\mathbb{Z}_2$-orbifold target space, for instance.

But once we pass to the higher geometry of [[Lie groupoid]]s at all, there is no good reason to restrict ourselves to those that are orbifolds. For instance, for any [[Lie group]] $G$ there is its _[[delooping]]_ Lie groupoid, the [[action groupoid]] of the trivial action of $G$ on the point, which we shall write 

$$
  \mathbf{B}G := *//G
  \,;
$$

and this can perfectly serve as a [[target space]] object for $\sigma$-models too. Here the boldface notation is to indicate that this Lie groupoid is a smooth refinement of the [[classifying space]] $B G \in Top$ of the Lie group. In fact, where $B G$ gives [[isomorphism class]] of smooth $G$-principal bundles, $\mathbf{B}G$ also remembers the [[isomorphism]]s themselves -- and hence in particular the [[automorphism]]s -- of these bundles. It is the _[[moduli stack]]_ of smooth $G$-principal bundles: for $\Sigma$ a [[smooth manifold]] we have that the _groupoid_ of morphisms of [[smooth infinity-groupoid|smooth groupoid]]s $\Sigma \to \mathbf{B}G$ (the _correct_ morphisms, sometimes called _[[Morita morphism]]_ to distinguish them from any incorrect notion) is that of smooth $G$-principal bundles and smooth homomorphisms between these

$$
  SmoothGrpd(\Sigma, \mathbf{B}G) \simeq G Bund(\Sigma) \in Grpd
  \,,
$$

whereas the [[geometric realization]] $B G \simeq \vert \mathbf{B}G\vert$ only sees the equivalence classes:
$$
  [\Sigma, B G] \simeq \pi_0 G Bund(\Sigma) \in Set
  \,.
$$ 

This indicates that ([[nonabelian cohomology|nonabelian]]) [[gauge theory]] on $\Sigma$ should have a formulation as a $\sigma$-model with target "[[space]]" $X$ the Lie groupoid $X = \mathbf{B}G$: a $\sigma$-model field $\Sigma \to X = \mathbf{B}G$ is a $G$-bundle, and an isomorphism of field configurations is a [[gauge transformation]] of $G$-bundles.

But a field configuration in $G$-gauge theory on $\Sigma$ is not just a $G$-principal bundle, but is a $G$-bundle _with [[connection on a bundle|connection]]_. There is no Lie groupoid that that would similarly represent such connections as a target space object. But there is a _[[smooth infinity-groupoid|smooth groupoid]]_ that does: $\mathbf{B}G_{conn}$, the [[groupoid of Lie algebra valued 1-forms]].

Here by a _smooth groupoid_ we mean a [[groupoid]] that comes with a rule for which of its collections of objects or morphisms are _smoothly parameterized families_. Technically this is a _[[(2,1)-sheaf]]_ or _[[stack]]_ on the [[site]] [[CartSp]] of [[Cartesian space]]s and [[smooth function]]s between them. Among all smooth groupoids, Lie groupoids -- and generally [[diffeological space|diffeological groupoid]]s -- are singled out as being the _[[concrete sheaf|concrete]]_ objects. While it is useful to know if a given smooth groupoid is [[concrete sheaf|concrete]] or even [[Lie groupoid|Lie]], it is in any case a fact that all of [[higher geometry|higher]] [[differential geometry]] exists for general smooth $\infty$-groupoids just as well. Therefore, if we can allow Lie groupoids as targets for $\sigma$-models, we can allow general smooth groupoids as well.

The non-concrete smooth groupoid $\mathbf{B}G_{conn}$ that we just mentioned is defined by the following rule: for $U \in $ [[CartSp]], a smoothly $U$-parameterized family of objects is by definition a $\mathfrak{g}$-[[Lie algebra valued 1-form|valued differential 1-form]] $A \in \Omega^1(U, \mathfrak{g})$ on $U$, where $\mathfrak{g}$ is the [[Lie algebra]] of $G$. A smoothly $U$-parameterized family of morphisms $g : A_1 \to A_2$ is a smooth [[gauge transformation]] $g \in C^\infty(U, G) : A_2 = g A g^{-1} + g d g^{-1}$ between two such form data. (This is "non-concrete" because the smooth $U$-parameterized families $U \to \mathbf{B}G_{conn}$ are not $U$-families of points $* \to \mathbf{B}G_{conn}$.)

One then finds that the [[mapping space]] groupoid for this target $X = \mathbf{B}G_{conn}$ is the groupoid 

$$
  SmoothGrpd(\Sigma , \mathbf{B}G_{conn})
   \simeq
  G Bund_{conn}(\Sigma)
  \,,
$$

whose objects are smooth $G$-principal bundles with connection on $\Sigma$, and whose morphisms are smooth morphisms of principal bundles with connection. 
This groupoid is the [[configuration space]] of $G$-[[gauge theory]] on $\Sigma$, for instance of $G$-[[Yang-Mills theory]] or of $G$-[[Chern-Simons theory]]:

$$
  SmoothGrpd(\Sigma, \mathbf{B}G_{conn})
  \simeq 
   Conf_{Yang-Mills}(\Sigma)
  \simeq
   Conf_{Chern-Simons}(\Sigma)
  \,.
$$

Notice that this configuration space is now itself a groupoid: morphisms are [[gauge transformation]]s. In fact, it is naturally itself a smooth groupoid (when we read the [[hom-object]] here as an [[internal hom]] in [[Smooth∞Grpd|SmoothGrpd]]). In the traditional physics literature these Lie groupoidal [[configuration space]]s of fields are best known in terms of their [[infinitesimal object|infinitesimal]] approximation $Lie(Conf(\Sigma)) \in LieAld$, which are _[[Lie algebroid]]s_, and these in turn are best known in terms of their [[function algebras on ∞-stacks|function algebras]], called the _[[Chevalley-Eilenberg algebra]]s_ $CE(Lie(Conf(\Sigma)))$: this [[dg-algebra]] is in physics called the [[BRST complex]]. Its degree-1 generators, the [[cotangent vector|cotangents]] to the [[morphism]]s of $Conf(\Sigma)$, are called the _ghost fields_ of gauge theory.

Of course we already saw secretly groupoidal configuration spaces in the [above](ExpositionClassical) list of examples of $\sigma$-models of relativistic [[branes]]. We said that their configuration spaces $C^\infty(\Sigma,X)//Diff(\Sigma)$ were [[quotient]]s; but really they are to be taken as higher categorical quotients, known as _[[homotopy colimit|homotopy quotients]]_ or _[[2-colimit|weak quotients]]_ : they are the [[action groupoid]]s of $Diff(\Sigma)$ acting on $C^\infty(\Sigma,X)$.

We will see in the examples below that there is, of course, no reason to stop after passing from target manifolds to smooth target groupoids. At least as the $\sigma$-model increases in dimension, it is natural to consider smooth target [[2-groupoid]]s, target [[3-groupoid]]s, ... target [[n-groupoid]]s  and eventually [[smooth ∞-groupoids]]. The full context of smooth $\infty$-groupoids is the natural completion of traditional [[differential geometry]] to _[[higher geometry]]_ .


Given that it does thus make sense to regard general [[smooth ∞-groupoid]]s as target spaces for $\sigma$-models, the questions is if there are useful [[background gauge field]]s on such. This is indeed the case:

for instance we have a <a href="http://ncatlab.org/nlab/show/smooth%20infinity-groupoid#CohomologyOfLieGroups">theorem</a> that says that for $G$ a compact Lie group, there is, for every integral cohomology class $c \in H^{n+1}(B G, \mathbb{Z})$ of the classifying space of $G$ -- a [[characteristic class]] for $G$-principal bundles -- up to equivalence a unique smooth lift $\mathbf{c} : \mathbf{B}G \to \mathbf{B}^n U(1)$ to a smooth [[circle n-bundle]] on the smooth $\mathbf{B}G$. Moreover, we have a [[infinity-Chern-Weil theory|theorem]] that for sufficiently highly connected Lie groups or smooth $\infty$-groups $G$, this refines canonically to a [[circle n-bundle with connection]] on the differentially refined smooth moduli space $\mathbf{B}G_{conn}$, given by a morphism:

$$
  \hat \mathbf{c} : \mathbf{B}G_{conn} \to \mathbf{B}^n U(1)_{conn}
  \,.
$$

This assignment generalizes the classical [[Chern-Weil homomorphism]]: we may speak of the _[[∞-Chern-Weil homomorphism]]_ . The first example [below](#SigmaCS) shows that ordinary [[Chern-Simons theory]] is a $\sigma$-model that arises this way. Generally we may this speak of $\sigma$-models with target space a [[smooth ∞-groupoid]] and [[background gauge field]]s given by the [[∞-Chern-Weil homomorphism]] this way as [[schreiber:∞-Chern-Simons theories]]. 

The second example [below](#SigmaDW) shows that ordinatry [[Dijkgraaf-Witten theory]] is a $\sigma$-model that arises this way when $G$ is a [[discrete group]]. Generally we may thus speak of $\sigma$-models with target space a [[discrete ∞-groupoid]] and  [[background gauge field]]s given by the [[∞-Chern-Weil homomorphism]] this way as [[schreiber:∞-Dijkgraaf-Witten theories]]. 


### Chern-Simons theory as a $\sigma$-model
 {#SigmaCS}

One of the earliest [[topological quantum field theories]] ever considered in detail is _[[Chern-Simons theory]]_ . We introduce this from the point of view of $\sigma$-models with higher geometric target spaces as discussed [above](#HigherGeometricTargetSpaces). 

An ordinary (as opposed to higher) _[[gauge theory]]_ is a [[quantum field theory]] whose field configurations on a manifold $\Sigma$ are [[connection on a bundle|connections]] on $G$-[[principal bundle]]s over $\Sigma$, for $G$ some [[Lie group]]. The word _[[gauge transformation]]_ is essentially the physics equivalent of the word _[[isomorphism]]_ , referring to isomorphisms in a [[configuration space]] of a field theory and specifically to isomorphisms between such bundles with connection. The [[action functional]] of a gauge theory is to be _[[gauge invariance|gauge invariant]]_ meaning that it assigns the same value to configurations that are related by a gauge transformaiton. This means precisely that the exponentiated action is a [[functor]]

$$
  \exp(i S(-)) :  G Bund_{conn}(\Sigma) \to U(1)
$$

from the [[groupoid]] of gauge field configurations and gauge transformaitons, to the [[circle group]] (regarded as a [[0-truncated]] groupoid).

The first nonabelian gauge theory to receive attention was _[[Yang-Mills theory]]_ : in that model $\Sigma$ is a 4-dimensional [[pseudo-Riemannian manifold]] modelling [[spacetime]]. The exponentiated [[action functional]] is given by the integral of differential 4-forms naturally associated with a connection and a Riemannian structure:

$$
  \exp(i S_{YM}(-)) : (P, \nabla) \mapsto \exp(i \int_\Sigma 
     \frac{1}{e^2} \langle F_\nabla \wedge \star F_\nabla\rangle 
     +
     i \theta \langle F_\nabla \wedge  F_\nabla 
   \rangle)
  \,.
$$

Here

* $P$ is any $G$-[[principal bundle]] and $\nabla$ a [[connection on a bundle|connection]] on it;

* $F_\nabla \in \Omega^2(P, \mathfrak{g})$ is the [[Lie algebra]]-valued [[curvature]] 2-form of this connection;

* $\langle -,-\rangle : \mathfrak{g} \otimes \mathfrak{g} \to \mathbb{R}$ is an _[[invariant polynomial]]_ on the Lie algebra: a bilinear form that is gauge invariant when evaluated on curvature 2-forms --  for $\mathfrak{g}$ a [[semisimple Lie algebra]] this would be the _[[Killing form]]_ and for a [[matrix Lie algebra]] this is simply the [[trace]] operation on products of matrices;

* $\star$ is the [[Hodge star]] operator given by the pseudo-Riemannian metric structure on $\Sigma$. 

* $e \in \mathbb{R}$ is some constant, called the [[coupling constant]] of the model;

* $\theta$ is another parameter called the [[theta-angle]]. 

The first summand in the exponent, that depending on the pseudo-Riemannian structure, is the crucial term for the direct application of this as a model of phenomenologically observed physics: it controls the dynamics of three of the four [[force]] fields in the [[standard model of particle physics]]. 

Instead of investigating this further, we shall here look at the case where $\frac{1}{e^2}$ is set to 0. While not _directly_ of phenomenological relevance, this is of quite some interest for the general theoretical understanding of the space of all possible field theories. Since the resulting action functional

$$
  \exp(i S_{tYM}) : (P, \nabla) \mapsto \exp(i \int_\Sigma \langle F_\nabla \wedge F_\nabla \rangle) 
$$

no longer depends on any extra (pseudo-Riemannian) structure on $\Sigma$ this may be interpreted as defining a [[topological quantum field theory]] : one speaks of _[[topological Yang-Mills theory]]_ .

This is not quite a $\sigma$-model in the sense that we have been discussing: while the [[configuration space]] of [[topological Yang-Mills theory]] does consist of maps into the [[target space]] $X = \mathbf{B}G_{conn}$ (the smooth [[moduli stack]] of $G$-principal bundles with connection, as discussed [above](HigherGeometricTargetSpaces)),  there is no way that the above action functional is induced directly from the transgression of the [[higher parallel transport|higher holonomy]] of a [[circle n-bundle with connection]] on this target space.  This is because, at least for [[semisimple Lie group]]s $G$, these are nontrivial only for odd $n$, whereas here we have $n = dim \Sigma = 4$.

But something closely related is true: $\exp(i S_{tYM})$ is the integrated _[[curvature]]_ functional of a circle $3$-bundle with connection on $\mathbf{B}G_{conn}$: what we call the _[[Chern-Simons circle 3-bundle]]_ .

This means the following: in generalization of how an ordinary [[circle bundle]] with connection $\nabla$ has a [[curvature]] 2-form, a [[circle n-bundle with connection]] $\nabla$ on a manifold $X$ has a curvature $(n+1)$-form $F_\nabla \in \Omega^{n+1}_{cl}(X)$. These curvature forms are closed, but not necessarily exact. Nevertheless, a generalization of the [[Stokes theorem]] holds true for them: for $\Sigma$ of dimension $n+1$ and denoting by $\partial \Sigma$ the [[boundary]] of $\Sigma$ and by $\gamma : \Sigma \to X$ a $\Sigma$-shaped trajectory in $X$, we have that the integral of the curvature over $\Sigma$ equals the [[higher parallel transport|higher holonomy]] of $\nabla$ over $\partial_\Sigma$:

$$
  \exp(i \int_\Sigma \phi^* F_\nabla)
  = 
  hol(\nabla, \gamma|_{\partial \Sigma})  
  \,.
$$

This property in fact characterizes equivalence classes of circle $n$-bundles with connection. When conceiving of circle $n$-bundles with connection as rules for assigning higher holonomy that satisfy this property, one speaks of _[[Cheeger-Simons differential characters]]_ . 

Therefore, if we can find a circle 3-bundle with connection on the [[moduli stack]] $\mathbf{B}G_{conn}$ of $G$-principal bundles with connection whose [[curvature]] 4-form at $(P,\nabla)$ is $\langle F_\nabla \wedge F_\nabla \rangle$, then we can interpret [[topological Yang-Mills theory]] on a 4-dimensional $\Sigma$ with boundary as being given by a $\sigma$-model on $\partial \Sigma$ with [[background gauge field]] that circle 3-bundle. 

For $G$ a connected and [[simply connected]] Lie group, such a circle 3-bundle indeed exists. Its characteristic morphism 

$$
  \frac{1}{2}\hat \mathbf{p}_1 : 
  \mathbf{B}G_{conn}
   \to 
  \mathbf{B}^3 U(1)_{conn}
$$

from the smooth moduli stack of $G$-bundles with connection to the smooth moduli 3-groupoid of [[circle n-bundle with connection|circle 3-bundles with connection]] is constructed and discussed in (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(?%2C1)-topos+--+references#FSS">Fiorenza-Schreiber-Stasheff</a>), see _[[Chern-Simons circle 3-bundle]]_ . This is the differential refinement of the [[differential string structure|smooth first fractional Pontryagin class]]

$$
  \frac{1}{2}\mathbf{p}_1 : \mathbf{B}G \to \mathbf{B}^3 U(1)
$$

which in turn is a smooth refinement of the fractional [[Pontryagin class]]

$$
  \frac{1}{2} p_1 : B G \to B^3 U(1) \simeq K(\mathbb{Z}, 4)
$$

of the [[classifying space]] $B G$.

To get a feeling for what this circle 3-bundle is like, we look at what its pull-back $\frac{1}{2}\hat \mathbf{p}_1(\phi) : \Sigma \stackrel{\phi}{\to} \mathbf{B}G_{conn} \stackrel{\frac{1}{2} \hat \mathbf{p}_1}{\to} \mathbf{B}^3 U(1)_{conn}$ to $\Sigma$ along any field configuration $\phi : \Sigma \to X = \mathbf{B}G_{conn}$ is like.

Notice that for simply conneced $G$ the [[classifying space]] $B G$ has vanishing [[homotopy group]]s in degree $k \leq 3$. Therefore every $G$-principal bundle $P$ on the 3-dimensional $\partial \Sigma$ is necessarily trivializable. In this case the [[configuration space]] of the $\sigma$-model is equivalent to the [[groupoid of Lie algebra valued forms]] 

$$
  SmoothGrpd(\partial \Sigma, \mathbf{B}G_{conn})
  \simeq
  \Omega^1(\partial \Sigma, \mathfrak{g})//C^{\infty}(\partial \Sigma,G)
$$ 

on $\partial \Sigma$. For $A \in \Omega^1(\Sigma, \mathrak{g})$ a field configuration and $F_A = d A + \frac{1}{2}[A \wedge A]$ the corresponding curvature 2-form, the curvature 4-form of $\frac{1}{2}\hat \mathbf{p}_1(\phi)$ is $\langle F_A \wedge F_A \rangle$. Its connection 3-form $C$ satisfying $d C = \langle F_A \wedge F_A \rangle$ is -- up to a closed 3-form -- the _[[Chern-Simons form|Chern-Simons 3-form]]_

$$
  C = cs(A) = \langle A \wedge F_A \rangle + \frac{1}{6}\langle A \wedge [A \wedge A]\rangle 
  \,.
$$

Therefore the [[action functional]] of the 3-dimensional $\sigma$-model given by the [[background gauge field]] $\frac{1}{2}\hat \mathbf{p}_1 : \mathbf{B}G_{conn} \to  \mathbf{B}^3 U(1)_{conn}$ is given by

$$
  \exp(i S(-))_{\Sigma_3} : A \mapsto
  \exp(i \int_{\Sigma_3} cs(A))
  \,.
$$

The [[quantum field theory]] defined by this action functional is known as _[[Chern-Simons theory]]_ . 






### AKSZ theory as a higher Chern-Simons $\sigma$-model
 {#AKSZSigmaModel}

#### Summary

Every [[symplectic Lie n-algebroid]] $\mathfrak{P}$ serves as the [[target space]] of a canonically defined topological $\sigma$-model of dimension $n+1$. This is called the [[AKSZ theory|AKSZ sigma-model]] of $\mathcal{P}$.

This subsumes the following examples:

* for $\mathfrak{P}$ a [[semisimple Lie algebra]], the AKSZ $\sigma$-model is ordinary [[Chern-Simons theory]];

* for $\mathfrak{P}$ a [[Poisson Lie algebroid]], the AKSZ $\sigma$-model is corresponding [[Poisson sigma-model]];

* for $\mathfrak{P}$ a [[Courant Lie 2-algebroid]], the AKSZ $\sigma$-model is corresponding [[Courant sigma-model]].

Also the [[A-model]] and the [[B-model]] 2-dimensional topological $\sigma$-models are examples.

The AKSZ [[action functional]] turns out to be very fundamental:

by [[∞-Chern-Weil theory]] every [[invariant polynomial]] on an [[L-∞ algebroid]] induces an [[∞-Chern-Weil homomorphism]] and the corresponding [[∞-Chern-Simons theory]] action functional. Moreover, every [[symplectic Lie n-algebroid]] canonically carries a binary invariant polynomial. The AKSZ  $\sigma$-model action functional is precisely the value of the $\infty$-Chern-Weil homomorphism on this invariant polynomial.

This is shown at [∞-Chern-Simons theory -- Examples -- AKSZ theory](http://ncatlab.org/schreiber/show/infinity-Chern-Simons+theory+--+examples#ASKZTheory).

#### Definition

A [[sigma-model]] [[quantum field theory]] is, roughly, one 

* whose fields are maps $\phi : \Sigma \to X$  to some space $X$;

* whose [[action functional]] is, apart from a 
  [[kinetic action|kinetic term]], the [[transgression]] 
  of some kind of [[cocycle]]  on $X$
  to the [[mapping space]] $\mathrm{Map}(\Sigma,X)$.

Here the terms "space", "maps" and "cocycles"
are to be made precise in a suitable context.
One says that $\Sigma$ is the _[[worldvolume]]_, 
$X$ is the _[[target space]]_ and the cocycle is
the _[[background gauge field]]_ .

For instance the ordinary charged [[particle]] 
(for instance an electron) is described by a $\sigma$-model 
where $\Sigma = (0,t) \subset \mathbb{R}$ is the abstract
_[[worldline]]_, where $X$ is a smooth
([[pseudo-Riemannian manifold|pseudo]]-)[[Riemannian manifold]]
(for instance our [[spacetime]]) and where the background cocycle
is a [[circle bundle]] with [[connection on a bundle|connection]] 
on $X$ (a degree-2 cocycle in [[ordinary differential cohomology]] of $X$, representing a background _[[electromagnetic field]]_ : 
up to a kinetic term the action functional is the [[holonomy]] of the connection over  a given [[curve]] $\phi : \Sigma \to X$. 

The $\sigma$-models to be considered here are 
_higher_ generalizations of this example,
where the background gauge field is a cocycle of higher degree
(a [[connection on an infinity-bundle|higher bundle with connection]]) 
and where the worldvolume is
accordingly higher dimensional -- and where $X$ is allowed to be 
not just a manifold but an approximation to a 
_higher [[orbifold]] (a [[smooth ∞-groupoid]]).

More precisely, here we take the [[category]] of [[space]]s
to be [[dg-geometry|smooth dg-manifolds]].
One may imagine that we can equip this 
with an [[internal hom]]
$\mathrm{Maps}(\Sigma,X)$ given by $\mathbb{Z}$-graded objects. 
Given [[dg-geometry|dg-manifolds]] $\Sigma$ and $X$ 
their canonical degree-1 vector fields
$v_\Sigma$ and $v_X$ acting on the mapping space from the
left and right. In this sense their linear combination 
$v_\Sigma + k \, v_X$ for some $k \in \mathbb{R}$
equips also $\mathrm{Maps}(\Sigma,X)$ with the structure of 
a differential graded smooth manifold.

Moreover, we take the "cocycle" on $X$ to be a 
graded [[symplectic structure]] $\omega$, 
and assume that there is a kind of Riemannian structure on $\Sigma$
that allows to form the [[transgression]]

$$
  \int_\Sigma \mathrm{ev}^* \omega
  :=
  p_! \mathrm{ev}^* \omega
$$

by [[integral transform|pull-push]] through the canonical 
[[correspondence]]

$$
  \mathrm{Maps}(\Sigma,X)
  \stackrel{p}{\leftarrow}
  \mathrm{Maps}(\Sigma,X) \times \Sigma
  \stackrel{ev}{\to}
   X
  \,,
$$

where on the right we have the [[evaluation map]].

Assuming that one succeeds in making precise sense of all this 
one expects to 
find that $\int_\Sigma \mathrm{ev}^* \omega$ is in turn a symplectic 
structure on the mapping space. This implies that the vector field
$v_\Sigma + k\, v_X$ on mapping space has a 
[[Hamiltonian]] 
$\mathbf{S} \in C^\infty(\mathrm{Maps}(\Sigma,X))$.
The grade-0 components $S_{\mathrm{AKSZ}}$ of $\mathbf{S}$ 
then constitute a functional on the space
of maps of graded manifolds $\Sigma \to X$. This is
the **AKSZ action functional** defining the AKSZ $\sigma$-model
with target space $X$ and background field/cocycle $\omega$.

In ([AKSZ](#AKSZ)) this procedure is indicated only somewhat vaguely. 
The focus of attention there is a discussion, from this perspective,
of the action functionals
of the 2-dimensional $\sigma$-models called the 
_[[A-model]]_ and the _[[B-model]]_ .

In ([Roytenberg](#Roytenberg)), a more detailed discussion of the general construction is given, including an explicit 
and general formula for $\mathbf{S}$ and hence for $S_{\mathrm{AKSZ}}$ . 
For $\{x^a\}$ a coordinate chart on $X$ that formula is
the following.

+-- {: .num_defn #TheAKSZAction}
###### Definition

For $(X,\omega)$ a [[symplectic Lie n-algebroid|symplectic dg-manifold]] of grade $n$, $\Sigma$ a smooth compact manifold of dimension $(n+1)$
and $k \in \mathbb{R}$, the
**AKSZ action functional**

$$
  S_{\mathrm{AKSZ},k} : 
   \mathrm{SmoothGrMfd}(\mathfrak{T}\Sigma, X)
  \to
  \mathbb{R}
$$

(where $\mathfrak{T}\Sigma$ is the shifted tangent bundle)

is

$$
  S_{\mathrm{AKSZ},k} 
   :
  \phi
  \mapsto
  \int_\Sigma 
  \left(
    \frac{1}{2}\omega_{ab} \phi^a \wedge d_{\mathrm{dR}}\phi^b
    + 
    k
    \,
    \pi(\phi\wedge \cdots \wedge \phi)
  \right)
  \,,
$$

where $\pi$ is the [[Hamiltonian]] for $v_X$ with respect to $\omega$
and where on the right we are interpreting fields as forms on $\Sigma$.

=--

This formula hence defines an infinite class of $\sigma$-models
depending on the target space structure $(X, \omega)$, and on the 
relative factor $k \in \mathbb{R}$.  In ([AKSZ](#AKSZ)) it was
already noticed that ordinary [[Chern-Simons theory]] is a special
case of this for $\omega$ of grade 2,  as is the 
[[Poisson sigma-model]]
for $\omega$ of grade 1 (and hence, as shown there, also the [[A-model]]
and the [[B-model]]). 
The main example in ([Roytenberg](#Roytenberg)) is spelling out the
general case for $\omega$ of grade 2, which is called the
_[[Courant sigma-model]]_ there. 

One nice aspect of this construction is that it follows immediately
that the full Hamiltonian $\mathbf{S}$ on mapping space satisfies
$\{\mathbf{S}, \mathbf{S}\} = 0$. Moreover, using the standard formula
for the internal hom of chain complexes one finds that the cohomology
of $(\mathrm{Maps}(\Sigma,X), v_\Sigma + k v_X)$ in degree 0
is the space of functions on those fields that satisfy the 
[[Euler-Lagrange equations]] of $S_{\mathrm{AKSZ}}$. 
Taken together this implies that 
$\mathbf{S}$ is a solution of the "master equation"
of a [[BV-BRST complex]] for the quantum field theory
defined by $S_{\mathrm{AKSZ}}$. This is a crucial ingredient for the 
quantization of the model, and this is what the AKSZ construction
is mostly used for in the literature.


### Dijkgraaf-Witten theory as a $\sigma$-model
 {#SigmaDW}

THe 3-dimensional [[TQFT]] [[Dijkgraaf-Witten theory]] can be understood as being the [[∞-Chern-Simons theory]]-$\sigma$-model whose [[target space]] is $\mathbf{B}G$ for $G$ a [[discrete group]]. 

See [∞-Chern-Simons theory -- Examples -- Dijkgraaf-Witten theory](http://ncatlab.org/schreiber/show/infinity-Chern-Simons+theory+--+examples#DiscreteTargets)


### The Yetter model as a $\sigma$-model

(...)

### $\infty$-Dijkgraaf-Witten theory


(...)

### $\infty$-Chern-Simons theory

See [[schreiber:∞-Chern-Simons theory]].

## References

The [[AKSZ sigma-model]] is discussed in

* M. Alexandrov, [[Maxim Kontsevich|M. Kontsevich]], [[Albert Schwarz|A. Schwarz]], O. Zaboronsky, _The geometry of the master equation and topological quantum field theory_, Int. J. Modern Phys. A 12(7):1405--1429, 1997 ([arXiv:hep-th/9502010](http://arxiv.org/abs/hep-th/9502010))
 {#AKSZ}

* [[Dmitry Roytenberg]], _AKSZ-BV Formalism and Courant Algebroid-induced Topological Field Theories_ Lett.Math.Phys.79:143-159,2007 ([arXiv](http://arxiv.org/abs/hep-th/0608150)).
 {#Roytenberg}

General $\infty$-Chern-Simons theory is discussed in 

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:infinity-Chern-Simons theory]]_