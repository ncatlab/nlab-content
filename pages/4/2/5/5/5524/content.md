
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

Let $C := $[[ThCartSp]] be the [[site]] of infintiesimally thickened [[Cartesian space]]s and [[smooth function]]s between them, equipped with the [[coverage]] of [[good open cover]]s on the finite factors. (A site of definition of the [[Cahiers topos]].)

Write

$$
  SynthDiff \infty Grpd := Sh_{(\infty,1)}(ThCartSp)
$$

for the [[(∞,1)-category of (∞,1)-sheaves]] on $ThCartSp$. 

Since $ThCartSp$ is an [[∞-cohesive site]], this is a [[cohesive (∞,1)-topos]]. We may think of its (concrete) objects as being [[∞-groupoid]]s equipped with [[smooth structure]] in the fashion of [[Models for Smooth Infinitesimal Analysis|standard models]] of [[synthetic differential geometry]].

Therefore we call an object in $SynthDiff \infty Grpd$ a **synthetic differential $\infty$-groupoid**.

By restriction along the morphism of sites [[CartSp]]${}_{smooth}\to$[[CartSp]]${}_{synthdiff}$ every synthetic differential $\infty$-groupoid has an underlying [[smooth ∞-groupoid]].


## Properites


The [[(n,1)-topos|(1,1)-topos]] $\tau_{\leq 0} SynthDiff\infty Grpd\hookrightarrow SynthDiff \infty Grpd$ of 0-[[truncated]] objects is the [[Cahiers topos]].


### $\infty$-Connectedness over $Smooth \infty Grpd$

+-- {: .un_prop}
###### Proposition

The morphism of [[site]]s

$$
  CartSp_{smooth} \stackrel{\overset{}{\leftarrow}}{\hookrightarrow}
  CartSp_{synthdiff}
$$

is a [[reflective subcategory|coreflective embedding]] and exhibits $SynthDiff \infty Grpd$ as being a [[locally ∞-connected (∞,1)-topos]] over [[Smooth∞Grpd]]

$$
 (\Pi_{inf} \dashv Disc_{inf} \dashv \Gamma_{inf})
  SynthDiff \infty Grpd
  \stackrel{\overset{\Pi_{inf}}{\to}}{\stackrel{\overset{Disc_{inf}}{\leftarrow}}{\underset{\Gamma_{inf}}{\to}}}
  Smooth \infty Grpd
  \,.
$$

=--

(...)

This induces the following infinitesimal analogs of the structures in $SynthDiff \infty Grpd$.


+-- {: .un_def}
###### Definition

Write

$$
  (\mathbf{\Pi}_{inf} \dashv \mathbf{\flat}_{inf})
  :=
  (LConst_{inf} \circ \Pi_{inf} \dashv LConst_{inf} \circ \Gamma_{inf})
  :
  SynthDiff \infty Grpd
  \stackrel{\leftarrow}{\to}
  SynthDiff \infty Grpd
$$

for the composite [[adjunction]]. For $X,A \in SynthDiff\infty Grpd$ we call $\mathbf{\Pi}$.

For $X \in \infty Grpd$ we write $\mathbf{\Pi}_{inf,dR}(X)$ for the [[homotopy cofiber]] of the unit $X \to \mathbf{\Pi}_{inf}(X)$, i.e. for the [[pushout]]

$$
  \array{
    X &\to& *
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \mathbf{\Pi}_{inf}(X) &\to& \mathbf{\Pi}_{inf,dR}(X)
  }
$$

in $SynthDiff \infty Grpd$.

For $* \to A \in SynthDiff \infty Grpd$ a [[pointed object]], we write $\mathbf{\flat}_{inf,dR} A$ for the [[homotopy fiber]] of the counit $\mathbf{\flat}_{inf} A \to A$, i.e. for the [[pullback]]

$$
  \array{
    \mathbf{\flat}_{inf,dR}A &\to& \mathbf{\flat}_{inf} A
    \\
    \downarrow &\swArrow& \downarrow
    \\
    * &\to& A
  }
$$

in $\infty Grpd$\,.

=--

(...)


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

* [[Urs Schreiber]], [[schreiber:differential cohomology in a cohesive topos]]

For references for the [[sheaf topos]] over [[CartSp]]${}_{synthdiff}$ see [[Cahiers topos]].



[[!redirects synthetic differential ∞-groupoid]]

[[!redirects SynthDiff∞Grpd]]