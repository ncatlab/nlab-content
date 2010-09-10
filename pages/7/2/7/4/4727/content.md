[[!redirects ∞-Lie algebroid valued differential forms]]

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

(...)

## Definition

For $X$ a [[smooth manifold]] and $\mathfrak{a}$ an [[∞-Lie algebroid]], a  **$\infty$-Lie algebroid valued differential form** on $X$ is a morphism of [[dg-algebra]]s

$$
  \Omega^\bullet(X)
  \leftarrow
  W(\mathfrak{g})
  : 
  A
$$

i.e. dually a morphism of [[∞-Lie algebroid]]s

$$
  A : T X \to inn(\mathfrak{a})
  \,.
$$

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

The [[∞-groupoid]] of $\mathfrak{a}$-valued forms on $X$ is given by the [[Kan complex]] which in degree $k$ is the set of diagrams of [[dg-algebra]] morphisms

$$
  \exp_{diff}(\mathfrak{a})(X)_k
  \subset
  \left\{
    \array{
      C^\infty(X) \otimes \Omega^\bullet(\Delta^k)
      &\leftarrow&
      CE(\mathfrak{a})
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(X) \otimes \Omega^\bullet(\Delta k)
      &\leftarrow&
      W(\mathfrak{a})
    }
  \right\}
  \,,
$$

where the subset is that on those elements for which the bottom morphism hits forms that have no leg along the simplex.

For the moment, see [[Lie integration]] and [[∞-Chern-Weil theory]] for more discussion of this.


[[!redirects ∞-groupoid of ∞-Lie-algebra valued forms]]
[[!redirects ∞-groupoid of ∞-Lie algebroid valued forms]]
[[!redirects ∞-groupoid of ∞-Lie algebroid valued differential forms]]

