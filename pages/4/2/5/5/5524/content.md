
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

By restriction along the morphism of sites [[CartSp]] $\to$ [[ThCartSp]] every synthetic differential $\infty$-groupoid has an underlying [[smooth ∞-groupoid]].


## Properites


The [[(n,1)-topos|(1,1)-topos]] $\tau_{\leq 0} SynthDiff\infty Grpd\hookrightarrow SynthDiff \infty Grpd$ of 0-[[truncated]] objects is the [[Cahiers topos]].


### $\infty$-Connectedness over $Smooth \infty Grpd$

+-- {: .un_prop}
###### Proposition

The morphism of [[site]]

$$
  CartSp_{smooth} \stackrel{\overset{}{\leftarrow}}{\hookrightarrow}
  CartSp_{synthdiff}
$$

is a [[reflective subcategory|coreflective embedding]] and exhibits $SynthDiff \infty Grpd$ as being a [[locally ∞-connected (∞,1)-topos]] over [[Smooth∞Grpd]]

$$
  SynthDiff \infty Grpd
  \stackrel{\overset{\Pi_{inf}}{\to}}{\stackrel{\overset{LConst_{inf}}{\leftarrow}}{\underset{\Gamma_{inf}}{\to}}}
  Smooth \infty Grpd
  \,.
$$

=--

This induces the following infinitesimal analogs of the structures in $SynthDiff \infty Grpd$.


+-- {: .un_def}
###### Definition

Write

$$
  (\mathbf{\Pi}_{inf} \dashv \mathbf{\flat}_{inf})
  :=
  (LConst_{inf} \circ \Pi_{inf} \dashv LConst_{inf} \circ \Gamma_{inf})
  :
  \infty SDLieGrpd
  \stackrel{\leftarrow}{\to}
  \infty SDGrpd
$$

for the composite [[adjunction]]. For $X,A \in \infty SDGrpd$ we call $\mathbf{\Pi}$ the **Lie [[schreiber:path ∞-groupoid|infinitesimal homotopy ∞-groupoid]]** of $X$ and we call $\mathbf{\flat}A$ the **infinitesimally flat $\infty$-Lie groupoid** of $A$.

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

in $\infty SDGrpd$.

For $* \to A \in \infty SDGrpd$ a [[pointed object]], we write $\mathbf{\flat}_{inf,dR} A$ for the [[homotopy fiber]] of the counit $\mathbf{\flat}_{inf} A \to A$, i.e. for the [[pullback]]

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



## Structures

We discuss what some of the general abstract <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#Structures">Structures in a cohesvive (∞,1)-topos</a> look like in the model $SynthDiff \infty Grpd$.


(...)

[[!redirects synthetic differential ∞-groupoid]]

[[!redirects SynthDiff∞Grpd]]