
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--



* [[groupoid of Lie-algebra valued forms]]

* [[2-groupoid of Lie 2-algebra valued forms]]

* [[3-groupoid of Lie 3-algebra valued forms]]

* **$\infty$-groupoid of ∞-Lie-algebra valued forms**

***

#Contents#
* table of contents
{:toc}

## Idea

For $\mathfrak{g}$ an [[∞-Lie algebra]] (or more generally [[∞-Lie algebroid]]), the **$\infty$-groupoid of $\mathfrak{g}$-valued forms** is the [[∞-groupoid]] whose 

* [[object]]s are [[differential forms]] with values in $\mathfrak{g}$;

* [[morphism]]s are [[gauge transformation]]s between these;

* [[k-morphisms]] are order $k$ higher gauge transformations.

This naturally refines to a non-[[concrete sheaf|concrete]] [[∞-Lie groupoid]] whose $U$-parameterized smooth families of objects are [[∞-Lie algebroid]]-valued [[differential form]]s on $Z$.

A [[cocycle]] with coefficients in this is a [[connection on an ∞-bundle]].

For an introduction see the section <a href="http://ncatlab.org/nlab/show/infinity-Chern-Weil+theory+introduction#LieConnections">∞-Lie algebra valued forms</a> at [[∞-Chern-Weil theory introduction]].

## Definition


For $X$ a [[smooth manifold]] and $\mathfrak{a}$ an [[∞-Lie algebroid]], a  **$\infty$-Lie algebroid valued differential form** on $X$ is a morphism of [[dg-algebra]]s

$$
  \Omega^\bullet(X)
  \leftarrow
  W(\mathfrak{g})
  : 
  A
$$

from the [[Weil algebra]] of $\mathfrak{g}$ to the [[de Rham complex]] of $X$. Dually this is a morphism of [[∞-Lie algebroid]]s

$$
  A : T X \to inn(\mathfrak{a})
$$

from the [[tangent Lie algebroid]] to the [[Weil algebra|inner automorphism infinity-Lie algebra]].

Its [[curvature]] is the composite of [[graded vector space]]s

$$
  \Omega^\bullet(X) \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{F_{(-)}}{\leftarrow}
  \wedge^1 \mathfrak{a}^*
  : 
  F_{A}
  \,.
$$

Precisely if the curvatures vanish does the morphism factor through the [[Chevalley-Eilenberg algebra]] $W(\mathfrak{g}) \to CE(\mathfrak{g})$.

$$
  (F_A = 0) 
  \;\;\Leftrightarrow
  \;\;
  \left(
  \array{
     && CE(\mathfrak{g})
     \\
     & {}^{\mathllap{\exists A_{flat}}}\swarrow & \uparrow
     \\
     \Omega^\bullet(X) &\stackrel{A}{\leftarrow}& W(\mathfrak{g})     
  }
  \right)
$$

in which case we call $A$ **flat**.

The [[curvature characteristic form]]s of $A$ are the composite

$$
  \Omega^\bullet(X)
  \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{\langle F_{(-)} \rangle}{\leftarrow}
  inv(\mathfrak{g})
  :
  \langle F_A\rangle
  \,,
$$

where $inv(\mathfrak{g}) \to W(\mathfrak{g})$ is the inclusion of the [[invariant polynomial]]s. 


+-- {: .un_defn}
###### Definition


Let $U$ be a [[smooth manifold]]. The **∞-groupoid of $\mathfrak{a}$-valued forms** on $X$ is given by the [[Kan complex]] whose set of [[k-morphism]]s is the set of diagrams of [[dg-algebra]] morphisms

$$
  \exp(\mathfrak{a})_{conn}(U)
  :
  [k]
  \mapsto
  \left\{
    \array{
      \Omega^\bullet(U \times \Delta^k)_{vert}
      &\stackrel{A_{vert}}{\leftarrow}&
      CE(\mathfrak{a})
      &&&
      gauge\;transformation
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U \times \Delta^k)
      &\stackrel{A}{\leftarrow}&
      W(\mathfrak{a})
      &&&
      \mathfrak{g}-valued\;form
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U)
      &\stackrel{\langle F_A\rangle}{\leftarrow}&
      inv(\mathfrak{g})
      &&&
      curvature\;characteristic\;forms
    }
  \right\}
  \,.
$$

Here $\Omega^\bullet(U \times \Delta^k)_{vert}$ denotes the dg-algebra of [[vertical differential form]]s on the trivial bundle $U \times \Delta^k \to U$.

=--

If we just consider the top horizontal morphism in this diagram we obtain the object

$$
  \exp(\mathfrak{a})(U)
  :
  [k]
  \mapsto
  \left\{
    \array{
      \Omega^\bullet(U \times \Delta^k)_{vert}
      &\stackrel{A_{vert}}{\leftarrow}&
      CE(\mathfrak{a})
     }
  \right\}
$$

discussed in detail at [[Lie integration]]. If we consider the top square of the diagram we obtain the object

$$
  \exp(\mathfrak{a})_{diff}(U)
  :
  [k]
  \mapsto
  \left\{
    \array{
      \Omega^\bullet(U \times \Delta^k)_{vert}
      &\stackrel{A_{vert}}{\leftarrow}&
      CE(\mathfrak{a})
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U \times \Delta^k)
      &\stackrel{A}{\leftarrow}&
      W(\mathfrak{a})
   }
  \right\}
  \,.
$$

This forms a [[resolution]] of $\exp(\mathfrak{g})$ and may be thought of as the $\infty$-groupoid of [[pseudo-connection]]s.

We have the evident forgetful morphisms 

$$
  \exp(\mathfrak{g})_{conn}
  \hookrightarrow
  \exp(\mathfrak{g})_{diff}
  \stackrel{\simeq}{\to}
  \exp(\mathfrak{g})
  \,.
$$


## Properties

We spell out what this definition means in detail.

### Objects: differential forms

An [[object]] of $\exp(\mathfrak{g})(U)$ is a dg-algebra morphism

$$
  \Omega^\bullet(U)
  \leftarrow
  W(\mathfrak{g})
  :
  A
  \,.
$$

Since the [[Weil algebra]] $W(\mathfrak{g})$ is a free dg-algebra, this is equivalently a morphism of [[graded vector space]]s

$$
  \Omega^\bullet(U)
  \leftarrow
  \wedge^1 \mathfrak{g}^*
  :
  A
  \,.
$$

This is equivalently an element of degree 1

$$
  A \in \Omega^\bullet(U) \otimes \mathfrak{g}
  \,,
$$

where the graded vector space $\mathfrak{g}$ is regarded as being in non-positive degrees.


### 1-Morphisms: integration of infinitesimal gauge transformations

The 1-[[morphism]]s in $\exp(\mathfrak{g})(X)$ may be thought of as [[gauge transformation]]s between $\mathfrak{a}$-valued forms. We unwind what these look like concretely.

For ease of notation, let $\mathfrak{a} = \mathfrak{g}$ be an [[∞-Lie algebra]].

+-- {: .un_defn}
###### Definition

Given a 1-morphism in $\exp(\mathfrak{g})(X)$, represented by $\mathfrak{g}$-valued forms

$$
  \Omega^\bullet(U \times \Delta^1) 
  \leftarrow
  W(\mathfrak{g})
  : 
  A
$$

consider the unique decomposition

$$
  A = A_U + ( A_{vert} := \lambda \wedge d t)  \; \; \in \Omega
  \,,
$$

with $A_U$ the horizonal differential form component and $t : \Delta^1 = [0,1] \to \mathbb{R}$ the canonical coordinate.

We call $\lambda$ the **gauge parameter** .

=--

We describe now how this enccodes a gauge transformation

$$
  A_0(s=1) \stackrel{\lambda}{\to} A_U(s = 1)
  \,.
$$

+-- {: .un_lemma}
###### Observation

The condition that all [[curvature characteristic form]]s descent to $U$ in that $A$ completes to a diagram

$$
  \array{
      \Omega^\bullet(U \times \Delta^k)
      &\stackrel{A}{\leftarrow}&
      W(\mathfrak{a})
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U)
      &\stackrel{\langle F_A\rangle}{\leftarrow}&
      inv(\mathfrak{g})
  }
$$

may be solved by requiring all components 

$$
  \Omega^\bullet(U \times \Delta^1)
  \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{r^a}{\leftarrow}
  \wedge^1 \mathfrak{g}^*
  F_A^a
$$

of the [[curvature]] forms to vanish when evaluated on the [[vector field]] $\partial_s$ along $\partial_s$.

By the nature of the [[Weil algebra]], this condition is a bunch of [[differential equation]]s of the form

$$
  \frac{\partial}{\partial s} A_U
  =
  d_U \lambda + [\lambda \wedge A] + [\lambda \wedge A \wedge A] + \cdots
  \,.
$$

=--

This is known as the equation for **infinitesimal [[gauge transformation]]s** of an $\infty$-Lie algebra valued form. 

+-- {: .un_lemma}
###### Observation

By [[Lie integration]] we have that $A_{vert}$ -- and hence $\lambda$ -- defines an element $\exp(\lambda)$ in the [[∞-Lie group]] that integrates $\mathfrak{g}$. 

The unique solution $A_U(s = 1)$ of the above differential equation at $s = 1$ for the initial values $A_U(s = 0)$ we may think of as the result of acting on $A_U(0)$ with the gauge transformatin $\exp(\lambda)$. 

=--

+-- {: .un_example}
###### Example
**(in ordinary bundles)**

Let $X $ be a [[smooth manifold]] and $\{U_i \to X\}$ an [[open cover]], $C(U)$ its [[Cech nerve]] and consider [[∞-anafunctor]]s from $X$ to $\exp(\mathfrak{g})_{conn}$

$$
  \array{
    C(U) &\stackrel{(\hat g, \hat \nabla)}{\to}& \exp(\mathfrak{g})_{conn}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\  
    X
  }
  \,.
$$

This is, in low degree, explicitly the following data:

* on each patch $U_i$ a $\mathfrak{g}$-valued form datum $\Omega^\bullet(U_i) \leftarrow W(\mathfrak{g}) : A_i$;

* on each double intersection $U_i \cap U_j$ 

  * a path of gauge transformations $\Omega^\bullet(U_i \cap U_j \times \Delta^1)_{vert} \leftarrow CE(\mathfrak{g}) : \lambda$, where the value of $\lambda$ at a point is the infinitesimal gauge transformation;

  * a path of $\mathfrak{g}$-valued forms $\Omega^\bullet(U_i \cap U_j \times \Delta^1)_{vert} \leftarrow CE(\mathfrak{g}) : A_{i j}$ lifting that

  * such that the vetical curvature component vanishes;

  * and such that the mixed curvature component vanishes. 

    This is equivalent to the [[differential equation]]

    $$
      \frac{\partial}{\partial t} A_{i j}
      =
      d_U \lambda + [\lambda, A]
      \,.
    $$

    for the initial value $A_{i j}(0) = A_i$ this has the unique solution

    $$
      A_{i j}(t) = g_{ij}(t)^{-1} (A_{i j} + d_{U}) g_{i j}(t)
      \,,
    $$

    where $g_{i j}(t)$ is the [[parallel transport]] of $\lambda$:

    $$
      \begin{aligned}
        &
        \frac{\partial}{\partial t}
        \left(
           g_{ij}(t)^{-1} (A_{i j} + d_{U}) g_{i j}(t)
        \right)
        \\
        = &
        g_{ij}(t)^{-1} (A_{i j} + d_{U}) \lambda g_{i j}(t)
        -
        g_{ij}(t)^{-1} \lambda (A_{i j} + d_{U}) g_{i j}(t)    
      \end{aligned}
    $$

    (where for ease of notaton we write actions as if $G$ were a [[matrix Lie group]]).

    In particular this implies that the endpoints of the path of $\mathfrak{g}$-valued 1-forms are related by the usual cocycle condition in $\mathbf{B}G_{conn}$

    $$
      A_{i j}(1) = A_j = g_{i j}^{-1}(1) (A_i + d_U) g_{i j}(1)
      \,.
    $$

* etc. 

=--


### $k$-Morphisms: higher order gauge transformations

(..)


## Examples

* For $\mathfrak{g}$ an ordinary [[Lie algebra]], a $\mathfrak{g}$-valued differential form in the sense described here is precisely an ordinary [[Lie-algebra valued 1-form]].

* For $\mathfrak{g}$ [[Lie 2-algebra]], a $\mathfrak{g}$-valued differential form in the sense described here is precisely an [[Lie 2-algebra valued form]].

* For $n \in \mathbb{N}$, a $b^{n-1}\mathbb{R}$-valued differential form is the same as an ordinary differential $n$-form.

* What is called an  "extended soft group manifold" in the literature on the [[D'Auria-Fre formulation of supergravity]] is really precisely a collection of $\infty$-Lie algebroid valued forms with values in a super $\infty$-Lie algebra such as the [[supergravity Lie 3-algebra]] (for 11-dimensional [[supergravity]]). The way [[curvature]] and [[Bianchi identity]] are read off from "extded soft group manifolds" in this literature is -- apart from this difference in terminology -- precisely what is described above. 




## References

The definitions in terms of [[∞-Lie theory]] as given above appear in

* Hisham Sati, Urs Schreiber, Jim Staasheff, $L_\infty$-connections (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">web</a>)

A collection of precursors to these notions is collected at

* [[schreiber:differential cohomology in an (∞,1)-topos -- references]]: <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#InfLieAlgValuedForms">∞-Lie algebra valued forms</a>

The [[Sullivan construction]] in [[rational homotopy theory]] involves really the same concepts as used here. For literature on its interpretation in terms of $\infty$-Lie theory see [[Lie integration]].




[[!redirects ∞-groupoid of ∞-Lie-algebra valued forms]]
[[!redirects ∞-groupoid of ∞-Lie algebroid valued forms]]
[[!redirects ∞-groupoid of ∞-Lie algebroid valued differential forms]]

[[!redirects ∞-Lie algebroid valued differential forms]]


[[!redirects ∞-Lie algebra valued differential form]]
[[!redirects ∞-Lie algebra valued differential forms]]

[[!redirects ∞-Lie algebra valued forms]]
[[!redirects ∞-Lie algebroid valued forms]]

[[!redirects ∞-groupoid of ∞-Lie algebra valued forms]]
[[!redirects ∞-Lie algebroid valued differential form]]