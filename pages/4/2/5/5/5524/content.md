
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

+-- {: .un_def}
###### Definition

Let [[CartSp]]${}_{synthdiff}$ be the [[full subcategory]] of the category of [[smooth loci]] on those objects of the form $\mathbb{R}^n \times D$ for $n \in \mathbb{N$ and $D$ an [[infinitesimal space]]: the formal dual of a Weil algebra.

Equip this category with the [[coverage]] where a family of morphisms in is [[covering]] precisely if it is of the form $\{U_i \times D \stackrel{(f_i, Id_D)}{\to} U \times D\}$ for $\{f_i : U_i \to U\}$ a covering in [[CartSp]]$()_{smooth}$ (a [[good open cover]]).

=--

This appears as ([Kock, (5.1)]{#Kock}). 

+-- {: .un_remark}
###### Remark

The [[sheaf topos]] over [[CartSp]]${}_{synthdiff}$ is [[equivalence of categories|equivalent]] to the [[Cahiers topos]].

=--

+-- {: .un_def}
###### Definition

We say the [[(∞,1)-topos]] of **synthetic differential $\infty$-groupoids** is the [[(∞,1)-category of (∞,1)-sheaves]]

$$
  SynthDiff \infty Grpd := Sh_{(\infty,1)}(CartSp_{synthdiff})
$$

on $CartSp_{synthdiff}$. 

=--

Since $ThCartSp$ is an [[∞-cohesive site]], this is a [[cohesive (∞,1)-topos]]. We may think of its (concrete) objects as being [[∞-groupoid]]s equipped with [[smooth structure]] in the fashion of [[Models for Smooth Infinitesimal Analysis|standard models]] of [[synthetic differential geometry]].

Therefore we call an object in $SynthDiff \infty Grpd$ a **synthetic differential $\infty$-groupoid**.

By restriction along the morphism of sites [[CartSp]]${}_{smooth}\to$[[CartSp]]${}_{synthdiff}$ every synthetic differential $\infty$-groupoid has an underlying [[smooth ∞-groupoid]].


## Properites


### Cohesiveness over $\infty Grpd$

+-- {: .un_prop}
###### Proposition

$SynthDiff \infty Grpd$ is a [[cohesive (∞,1)-topos]].

=--

+-- {: .proof}
###### Proof

Because [[CartSp]]${}_{synthdiff}$ is an [[∞-cohesive site]]. See there for details.

=--


## Structures

We discuss what some of the general abstract <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#Structures">Structures in a cohesvive (∞,1)-topos</a> look like in the model $SynthDiff \infty Grpd$.

### Concrete objects {#StrucConcreteObjects}

(...)

### Geometry and structure sheaves {#StrucGeometry}

(...)

### Cohesive $\infty$-groups {#StrucInfinGroups}

(...)

### Cohomology and principal $\infty$-bundles {#StrucCohomology}

(...)

### Concordance {#StrucConcordance}

(...)

### Geometric homotopy and Galois theory {#StrucGeometricHomotopy}

(...)

### van Kampen theorem {#StrucVanKampen}

(...)

### Paths and geometric Postnikov towers {#StrucPaths}

(...)


### Universal coverings and geometric Whitehead towers {#StrucWhitehead}

(...)


### Flat $\infty$-connections and local systems {#StrucFlat}

(...)

### de Rham cohomology {#StrucDeRham}

(...)


### $\infty$-Lie algebras {#StrucLieAlg}

(...)


### Maurer-Cartan forms and curvature characteristic forms {#StrucCurvatureForms}

(...)

### Differential cohomology {#StrucDifferentialCohomology}

(...)


### Chern-Weil homomorphism and $\infty$-connections {#StrucChernWeil}

(...)

### Higher holonomy and Chern-Simons functional {#StrucChernSimons}

(...)


## References

Section 3.4 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

The site [[CartSp]]${}_{synthdiff}$ is discussed in section 5 of

* [[Anders Kock]], _Convenient vector spaces embed into the Cahiers topos_ ([numdam](http://www.numdam.org/item?id=CTGDC_1986__27_1_3_0)).


[[!redirects synthetic differential ∞-groupoid]]

[[!redirects SynthDiff∞Grpd]]