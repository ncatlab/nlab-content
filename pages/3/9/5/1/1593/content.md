
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

An _orientifold_ is a background for [[string theory|string]] [[sigma-model]]s that combines aspects of $\mathbb{Z}_2$-[[orbifold]]s with _orientation reversal_ on the worldsheet (therefore the name): it consists of a [[bundle gerbe]] on a space with a $\mathbb{Z}_2$-action that satisfies a peculiar twisted equvariance condition with respect to this action.

Such orientifold gerbes with connection are the right structure for the definition of surface holonomy of _unoriented_ surfaces. Therefore they serve for defining the gauge part of the [[path integral|action functional]] for unoriented [[string theory|strings]].

More precisely, the [[gauge field]]s that constitute the background for a string $\sigma$-model, such as the [[Kalb-Ramond field]] and the [[RR-field]]s are modeled as [[cocycle]]s in the [[differential cohomology]] of the target space, and an _orientifold_ is the data given by an [[orbifold]] [[spacetime]] that involves the [[group]] $\mathbb{Z}_2$ and equipped with certain [classes in its( [[twisted cohomology|twisted]]) [[differential cohomology]] that is suitably $\mathbb{Z}_2$-[[equivariant cohomology|equivariant]].


## Orientifold circle $n$-bundles with connection

We discuss the notion of [[circle n-bundles with connection]] over double covering spaces with orientifold structure.

+-- {: .num_prop #ExtensionOfZTwo}
###### Proposition

The [[smooth infinity-groupoid|smooth]] [[automorphism 2-group]] of the [[circle group]] $U(1)$ is that corresponding to the smooth [[crossed module]]

$$
  AUT(U(1)) \simeq [U(1) \to \mathbb{Z}_2]
  \,,
$$

where the differential $U(1) \to \mathbb{Z}_2$ is trivial and where the [[action]] of $\mathbb{Z}_2$ on $U(1)$ is given under the identification of $U(1)$ with the unit circle in the plane by reversal of the sign of the angle.

This is an <a href="http://nlab.mathforge.org/nlab/edit/cohesive+%28infinity%2C1%29-topos+--+structures#InfinityGroupExtensions">extension of smooth ∞-groups</a>

$$
  \mathbf{B}U(1) \to AUT(U(1)) \to \mathbb{Z}_2
  \,.
$$

=--

+-- {: .proof}
###### Proof

The nature of $AUT(U(1))$ is clear. Let $\mathbf{B}U(1) \to AUT(U(1))$ be the evident inclusion. We have to show that its [[delooping]] is the [[homotopy fiber]] of $\mathbf{B}AUT(U(1)) \to \mathbf{B}\mathbb{Z}_2$.

For this it is sufficient to show that $\mathbf{B}^2 U(1)$ is equivalent to the  ordinary [[pullback]] of simplicial presheaves 
$\mathbf{B}AUT(U(1))\times_{\mathbf{B}\mathbb{Z}_2} \mathbf{E}\mathbb{Z}_2$ of the $\mathbb{Z}$_2-[[universal principal bundle]].

This pullback is the [[2-groupoid]] whose 

* [[object]]s are elements of $\mathbb{Z}_2$;

* [[morphism]]s $\sigma_1 \to \sigma_2$ are labeled by $\sigma \in \mathbb{Z}_2$ such that $\sigma_2 = \sigma \sigma_1$;

* all [[2-morphism]]s are [[endomorphism]]s, labeled by $c \in U(1)$;

* [[vertical composition]] of 2-morphisms is given by the group operation in $U(1)$, 

* horizontal composition of 1-morphisms with 1-morphisms is given by the group operation in $\mathbb{Z}_2$

* horizontal composition of 1-morphisms with 2-morphisms ([[whiskering]]) is given by the [[action]] of $\mathbb{Z}_2$ on $U(1)$.

This 2-groupoid has vanishing $\pi_1$, and $\pi_2 = U(1)$.
The inclusion of $\mathbf{B}^2 U(1)$ into this pullback is the obvious one, includion elements in $U(1)$ as endomorphisms of the trivial element in $\mathbb{Z}_2$. This is manifestly an isomorphism on $\pi_2$ and trivially an isomorphism on all other homotopy groups, hence is a [[weak equivalence]].

=--

+-- {: .num_prop }
###### Observation

A $U(1)$-[[gerbe]] in the full sense Giraud (as opposed to a $U(1)$-[[bundle gerbe]] in the sense of Murray) is equivalent to an $AUT(U(1))$-[[principal 2-bundle]], not in general to a circle 2-bundle, wich is only a special case.

=--

More generally we have:

+-- {: .num_prop }
###### Observation

For every $n \in \mathbb{N}$ the automorphism $(n+1)$-group of $\mathbf{B}^n U(1)$ is given by the [[crossed complex]]

$$
  AUT(\mathbf{B}^n U(1))
  \simeq
  [U(1) \to 0 \to \cdots \to 0 \to \mathbb{Z}_2]
$$

with $U(1)$ in degree $n+1$ and $\mathbb{Z}_2$ acting by automorphisms.

This is an extension of cohesive $\infty$-groups

$$
  \mathbf{B}^{n+1} U(1) \to AUT(\mathbf{B}^n U(1)) \to \mathbb{Z}_2
  \,.
$$

=--

+-- {: .num_defn }
###### Definition

For $X \in Smooth\infty Grpd$ a **double cover** $\hat X \to X$ is a $\mathbb{Z}_2$-[[principal bundle]]. 

For $n \in \mathbb{N}$, $n \geq 1$, an **orientifold circle $n$-bundle (with connection)** is an $AUT(\mathbf{B}^{n-1}U(1))$-[[principal ∞-bundle]] (with [[connection on an ∞-bundle|∞-connection]]) on $X$ that <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+structures#Cohomology">extends</a> $\hat X \to X$ with respect to the extension def. \ref{ExtensionOfZTwo} of $\mathbb{Z}^2$ by $AUT(\mathbf{B}^n U(1))$.

=--

This means that if $X \to \mathbf{B}\mathbb{Z}^2$ is the cocycle for the double cover $\hat X$, this factors as

$$
  X \stackrel{g}{\to} \mathbf{B} AUT(\mathbf{B}^{n-1} U(1)) \to \mathbf{B}\mathbb{Z}^2
$$

where $g$ is the [[cocycle]] for the given $AUT(\mathbf{B}^n U(1))$-[[principal ∞-bundle]].

+-- {: .num_prop }
###### Proposition

Every orientifold circle $n$-bundle (with connection) on $X$ induces an ordinary [[circle n-bundle with connection|circle n-bundle (with connection)]] $\hat P \to \hat X$ on the given double cover $\hat X$ such that restricted to any [[fiber]] of $\hat X$ this is equivalent to $AUT(\mathbf{B}^{n-1}U(1)) \to \mathbb{Z}_2$.

=--

This is a special case of a general statement about extensions of $\infty$-bundles, discussed at [[cohesive (infinity,1)-topos]] <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos+--+structures#ExtendedBundlesByBundlesOfExtensions">here</a>.

+-- {: .num_prop }
###### Observation

Orientifold circle 2-bundles (with connection) over [[smooth manifold]] are equivalent to the _Jandl gerbes_  (with connection) discussed in ([SSW05](#Jandl)) 

=--

The name _Jandl gerbe_ refers to the poem _<a href="http://www.worte-projekt.de/jandl.html">lichtung</a>_ by <a href="http://de.wikipedia.org/wiki/Ernst_Jandl">Ernst Jandl</a>.

+-- {: .proof}
###### Proof

By the general discussion at [[Euclidean-topological ∞-groupoid]] and [[smooth ∞-groupoid]] we have that $[U(1) \to \mathb{Z}_2]$-[[principal ∞-bundle]]s on $X$ are given by [[Cech cohomology|Cech cocycles]] relative to any [[good open cover]] of $X$ with coefficients in the sheaf of [[2-groupoid]]s $\mathbf{B}[U(1) \to \mathbb{Z}_2]$. Writing this out in components it is straightforward to check that this coincides with the data of a Jandl gerbe (with connection) locally trivialized with over this cover.

=--

+-- {: .num_remark }
###### Remark

Orientifold circle $n$-bundles are not $\mathbb{Z}_2$-[[equivariant cohomology|equivariant]] circle $n$-bundles: in the latter case the orientation reversal acts by an _[[automorphism]]_ between the bundle and its pullback along the orientation reversal, whereas for an orientifold circle $n$-bundle the orientation reversal acts by an equivalence to the _dual_ of the pulled-back bundle.

=--

+-- {: .num_prop }
###### Observation

The [[geometric realization]] 

$$
  \tilde R := |\mathbf{B}[U(1) \to \mathbb{Z}_2]|
$$

of $\mathbf{B}[U(1) \to \mathbb{Z}]$ is the [[homotopy n-type|homotopy 3-type]] with [[homotopy group]]s

$$
  \pi_0(\tilde R)  = 0
  \,;
$$

$$
  \pi_1(\tilde R)  = \mathbb{Z}_2
  \,;
$$

$$
  \pi_2(\tilde R)  = 0
  \,;
$$

$$
  \pi_3(R')  = \mathbb{Z}
$$

and nontrivial action of $\pi_1$ on $\pi_3$.

=--

+-- {: .proof}
###### Proof

By the theorem discussed <a href="http://nlab.mathforge.org/nlab/show/Euclidean-topological+infinity-groupoid#GeometricHomotopy">here</a> at [[ETop∞Grpd]] we have that 

1. specifically 

   1. $|\mathbf{B} \mathbb{Z}_2| \simeq B \mathbb{Z}_2$; 

   1. $|\mathbf{B}^2 U(1)| \simeq B^2 U(1) \simeq K(\mathbb{Z};3)$;

   where on the right we have the ordinary [[classifying space]]s going by these names;

1. generally geometric realization preserves [[fiber sequence]]s of nice  enough objects, such as those under consideration, so that we have a fiber sequence

   $$
     K(\mathbb{Z},3) \to \tilde R \to B \mathbb{Z}_2
   $$ 

   in [[Top]].

Since $\pi_3(K(\mathbb{Z}), 3) \simeq \mathbb{Z}$ and $\pi_1(B \mathbb{Z}_2) \simeq \mathbb{Z}_2$ and all other [[homotopy group]]s of these two spaces are trivial, the homotopy groups of $\tilde R$ follow by the [[long exact sequence of homotopy groups]] associated to our fiber sequence.

Finally, since the action of $\mathbb{Z}_2$ in the [[crossed module]] is nontrivial, $\pi_1(\tilde R)$ must act notriviall on $\pi_3(\mathbb{Z})$. It can only act nontrivial in a single way, up to homotopy.

=--

+-- {: .num_remark }
###### Remark

The space 

$$
  R := \mathbb{Z}_2 \times \tilde R
$$

is taken to be the coefficient object for orientifold ([[differential cohomology|differential]]) cohomology as appearing in [[string theory]] in ([DFM I](#Precis)). More details are in ([DFM II](#DistlerFreedMooreII)).

=--

## References

A definition and study of orientifold [[bundle gerbe]]s, modeling the [[Kalb-Ramond field]], is in

* [[Urs Schreiber]], [[Christoph Schweigert]], [[Konrad Waldorf]], _Unoriented WZW models and Holonomy of Bundle Gerbes_ ([arXiv](http://arxiv.org/abs/hep-th/0512283))
 {#Jandl}

* [[Krzysztof Gawedzki]], Rafal R. Suszek,  [[Konrad Waldorf]], _Bundle Gerbes for Orientifold Sigma Models_ ([arXiv](http://arxiv.org/abs/0809.5125))

A more encompassing formalization in terms of [[differential cohomology]] in general and [[twisted K-theory|twisted]] [[differential K-theory]] in particular that also takes the spinorial degrees of freedom into account is being announced in 

* [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Precis_ in: [[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]] ([arXiv](http://arxiv.org/abs/0906.0795), [slides](http://www.ma.utexas.edu/users/dafr/bilbao.pdf))
 {#Precis}

A summary talk on this is

* [[Greg Moore]], _The RR-charge of an orientifold_ ([ppt](http://www.physics.rutgers.edu/~gmoore/AnnArbor_Feb2010_FINAL.ppt))

More details are in

* [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Spin structures and superstrings_ ([arXiv:1007.4581](http://arxiv.org/abs/1007.4581))
 {#DistlerFreedMooreII}

A formulation of some of the relevant aspects of orientifolds in terms of the  [[schreiber:differential cohomology in an (∞,1)-topos -- survey|differential nonabelian cohomology]] with coefficients in the [[2-group]] $AUT(U(1))$ coming from the [[crossed module]] $[U(1) \to \mathbb{Z}_2]$ is indicated in 

* [[Urs Schreiber]],  talk [[schreiber:Background fields in twisted differential nonabelian cohomology|Background fields in twisted differential nonabelian cohomology]] at [[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology]] 

More on this in section 3.3.10 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

[[!redirects orientifolds]]

[[!redirects Jandl gerbe]]
[[!redirects Jandl gerbes]]