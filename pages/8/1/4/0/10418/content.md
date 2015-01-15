
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a [[G-structure]], it is _integrable_ or _locally flat_ if over [[germs]] it restricts to the canonical (trivial) $G$-structure. If it restricts to the canonical structure only over order-$k$ [[infinitesimal disks]], then it is called _order $k$ integrable_. The [[obstruction]] to first-order integrability is the [[torsion of a G-structure]], and hence first-order integrable $G$-structures are also called _torsion-free $G$-structures_.

Beware that some authors use the term "integrable" for "torsion-free". This originates in concentration on the case of [[almost symplectic structure]], i.e. $G$-structure for $G = Sp(2n)$ the [[symplectic group]], in which case the [[Darboux theorem]] gives that first order integrability (to [[symplectic structure]]) already implies full integrability. However, in general this is not the case. For instance for [[orthogonal structure]], i.e. $G$-structure for $G = O(n)$ the [[orthogonal group]], then the [[fundamental theorem of Riemannian geometry]] gives that the torsion obstruction to first-order integrability vanishes, exhibited by the [[Levi-Civita connection]], but full integrability here is equivalent to this being a [[flat connection]], which is a strong additional constraint. This is the case from which the terminology "locally flat" for "integrable" derives from.



## Definition
 {#Definition}

A $G$-structure is called _locally flat_ ([Sternberg 64, section VII, def. 2.4](#Sternberg64)) or _integrable_ (e.g. [Alekseevskii](#Alekseevskii)) if it is locally equivalent to the standard $G$-structure on the given model space (see also [Lott 90, page 4 of the exposition](#Lott90)).


Let $V$ be a linear local model space, e.g. a [[vector space]] in plain [[differential geometry]] or [[super vector space]] in [[supergeometry]], etc.. Write $GL(V)$ for its [[general linear group]]. Consider a [[group]] [[homomorphism]] $G \longrightarrow GL(V)$.

Let $\mathbf{c}_V$ be the _standard flat $G$-structure_ on $V$ (see at _[G-Structure -- Examples -- Standard flat G-structure](G-structure#TheStandardFlatGStructure)_).

+-- {: .num_defn}
###### Definition

A[[G-structure]] $\mathbf{c}$ on a [[manifold]] $X$ modeled on $V$ (e.g. a [[smooth manifold]] or [[supermanifold]]) is called integrable if

1. there exists [[cover]] $\{U_i \hookrightarrow X\}$ by [[open subsets]]  $U_i \hookrightarrow V$;

1. such that the $G$-structure $\mathbf{c}$ on $X$ restricts on each patch to the default $G$-structure $\mathbf{c}_0$ on $V$:

   $$
     \mathbf{c}|_{U_i} \simeq \mathbf{c}_0|_{U_i}
     \,.
   $$

=--


### In terms of subbundles

For instance if $G$-structure is modeled by $G$-subbundles $P$ of the [[frame bundle]] (as discussed at _[G-structure -- In terms of subbundles of the frame bundle](G-structure#InTermsOfSubbundlesOfTheFrameBundle)_ ), then it is integrable if each $P \hookrightarrow Fr(X)$ restricts on each patch to $P_0 \hookrightarrow Fr(V)$

$$
  \array{
     P_0|_{U_i} &\hookrightarrow& Fr(V)|_{U_i}
     \\
     {}^{\mathllap{\simeq}}\downarrow && \downarrow
     \\
     P|_{U_i} &\hookrightarrow& Fr(X)|_{U_i}
  }
  \,.
$$


### In terms of differential cohesion
 {#IntermOfDifferentialCohesion}


One may formalize the concept of integrable $G$-structure in the generality of [[higher differential geometry]], formalized in [[differential cohesion]].  See also  there at _[differential cohesion -- G-Structure](differential+cohesive+%28infinity%2C1%29-topos#structures)_.


## Properties

### Existence and torsion

The [[obstruction]] for a $G$-structure to be integrable to first order is its [[torsion of a G-structure]].

### In terms of adapted coordinate systems

A $G$-structure on $X$ is integrable previsely if there exists an [[atlas]] of $X$ by [[coordinate charts]] with the property that their canonical [[frame fields]] are $G$-frames.

([Sternberg 64, section VII, exercise 2.1](#Sternberg64))

## Examples
For instance 

### Complex structure
 {#ExampleComplexStructure}

A $GL(n,\mathbb{C}) \to GL(2n,\mathbb{R})$-[[G-structure|structure]] is an _[[almost complex structure]]_. Its [[torsion of a G-structure]] vanishes precisely if its [[Nijenhuis tensor]] vanishes, hence, by the [[Newlander-Nirenberg theorem]], precisely if it is a [[complex structure]]. Since a [[complex manifold]] admits holomorphic [[coordinate charts]], this first-order integrability already implies full integrability.

### Symplectic structure
 {#ExampleSymplecticStructure}

An $Sp(n) \hookrightarrow GL(2n)$-[[G-structure|structure]] is an _[[almost symplectic structure]]_. Its [[torsion of a G-structure]] is the [[de Rham differential]] $\mathbf{d}\omega$ of the corresponding 2-form $\omega$ (recalled e.g. in [Albuquerque-Picken 11](symplectic+manifold#AlbuquerquePicken11)). Hence first-order integrability here amounts precisely to [[symplectic structure]]. The [[Darboux theorem]] asserts that this is already a fully integrable structure.


### Orthogonal structure
 {#ExamplesOrthogonalStructure}

An $O(n)\to GL(n)$-[[G-structure|structure]] is an [[orthogonal structure]], hence a [[vielbein]], hence a [[Riemannian metric]]. The [[fundamental theorem of Riemannian geometry]] says that in this case the [[torsion of a G-structure]] vanishes, exhibited by the existence of the [[Levi-Civita connection]]. The corresponding first-order integrability is the existence of [[Riemann normal coordinates]] (since these identify the given [[vielbein]] at any point to first order with the trivial (identity) vielbein). The higher order obstructions to integrability turn out to all be proportional to combinations of the [[Riemann curvature]]. Full integrability is equivalent to the vanishing of Riemann tensor, hence to the LC-connection being a [[flat connection]]. 

### $G_2$-Structure
 {#ExampleG2Structure}

A An $G_2 \to GL(7)$-[[G-structure|structure]] is a [[G2-structure]]. Its [[torsion of a G-structure]] vanishes if the corresponding definite 3-form $\omega$ is [[covariant derivative|covariantly constant]] with respect to the induced [[Riemannian metric]], in which case the structure is a [[G2-manifold]]. Beware that some authors refer to this first-order integrable $G_2$-structure (or even weaker conditions) as "integrable $G_2$-structure".



## References

* {#Sternberg64} [[Shlomo Sternberg]], chapter VII of _Lectures on differential geometry_, Prentice-Hall (1964)

* {#Guillemin65} [[Victor Guillemin]], _The integrability problem for $G$-structures, Trans. Amer. Math. Soc. 116 (1965), 544&#8211;560. ([JSTOR](http://www.jstor.org/stable/1994134))

* {#Alekseevskii} D. V: Alekseevskii, _$G$-structure on a manifold_ in M. Hazewinkel (ed.) _Encyclopedia of Mathematics, Volume 4_

Lecture notes include

* {#Pasquotto} Federica Pasquotto, _Linear $G$-structures by example_ ([pdf](http://www.few.vu.nl/~pasquott/course16.pdf))


Discussion with an eye towards [[torsion constraints in supergravity]] is in

* {#Lott90} [[John Lott]], _The Geometry of Supergravity Torsion Constraints_, Comm. Math. Phys. 133 (1990), 563&#8211;615, (exposition in [arXiv:0108125](http://arxiv.org/abs/math/0108125))

Discussion with an eye towards [[special holonomy]] is in

* {#Joyce00} [[Dominic Joyce]], _Compact manifolds with special holonomy_, Oxford University Press 2000

See also the references at _[[torsion of a Cartan connection]]_ and at _[[torsion constraints in supergravity]]_.

[[!redirects integrability of G-structures]]

[[!redirects integrable G-structure]]
[[!redirects integrable G-structures]]

[[!redirects integrable G-stucture]]
[[!redirects integrable G-stuctures]]