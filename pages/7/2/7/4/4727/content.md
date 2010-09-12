
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


The [[∞-Lie groupoid]] whose objects are [[∞-Lie algebroid]]-valued [[differential form]]s, whose morphisms are gauge transformations of these, whose 2-morphisms are gaugr transformations of gauge transformations, and so on.

A [[cocycle]] with coefficients in this is a [[connection on an ∞-bundle]].

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

from the [[tangent Lie algebroid]] to the [[groupal model for universal principal infinity-bundles|inner automorphism infinity-Lie algebra]].

Its [[curvature]] is the composite of [[graded vector space]]s

$$
  \Omega^\bullet(X) \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{F_{(-)}}{\leftarrow}
  \mathfrak{a}^*[1]
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

The [[∞-groupoid]] of $\mathfrak{a}$-valued forms on $X$ is given by the [[Kan complex]] which in degree $k$ is the set of diagrams of [[dg-algebra]] morphisms

$$
  \exp_{diff}(\mathfrak{a})(X)_k
  \subset
  \left\{
    \array{
      C^\infty(X) \otimes \Omega^\bullet(\Delta^k)
      &\stackrel{A_{vert}}{\leftarrow}&
      CE(\mathfrak{a})
      &&&
      gauge\;transformation
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(X) \otimes \Omega^\bullet(\Delta^k)
      &\stackrel{A}{\leftarrow}&
      W(\mathfrak{a})
      &&&
      \mathfrak{g}-valued\;form
      \\
      \uparrow && \uparrow
      \\
      (\Omega^\bullet(U)\otimes C^\infty(\Delta^k))_{close}
      &\stackrel{\langle F_A\rangle}{\leftarrow}&
      inv(\mathfrak{g})
      &&&
      curvature\;characteristic\;forms
    }
  \right\}
  \,.
$$


For the moment, see [[Lie integration]] and [[∞-Chern-Weil theory]] for more discussion of this.

## Examples

* For $\mathfrak{g}$ an ordinary [[Lie algebra]], a $\mathfrak{g}$-valued differential form in the sense described here is precisely an ordinary [[Lie-algebra valued 1-form]].

* For $\mathfrak{g}$ [[Lie 2-algebra]], a $\mathfrak{g}$-valued differential form in the sense described here is precisely an [[Lie 2-algebra valued form]].

* For $n \in \mathbb{N}$, a $b^{n-1}\mathbb{R}$-valued differential form is the same as an ordinary differential $n$-form.

* What is called an  "extended soft group manifold" in the literature on the [[D'Auria-Fre formulation of supergravity]] is really precisely a collection of $\infty$-Lie algebroid valued forms with values in a super $\infty$-Lie algebra such as the [[supergravity Lie 3-algebra]] (for 11-dimensional [[supergravity]]). The way [[curvature]] and [[Bianchi identity]] are read off from "extded soft group manifolds" in this literature is -- apart from this difference in terminology -- precisely what is described above. 




## References

The definitions in terms of [[∞-Lie theory]] as given above appear in

* SSSI (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">web</a>)

A collection of precursors to these notions is collected at

* [[schreiber:differential cohomology in an (∞,1)-topos -- references]]: <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#InfLieAlgValuedForms">∞-Lie algebra valued forms</a>

The [[Sullivan construction]] in [[rational homotopy theory]] involves really the same concepts as used here. For literature on its interpretation in terms of $\infty$-Lie theory see 

* [[Lie integration]].


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