
# &#268;ech nerve
* automatic table of contents goes here
{:toc}

## Definition

### In category theory

In a [[category]] $C$ with [[pullback]]s (possibly [[homotopy pullback]]s), given a [[morphism]] $U \to X$ in $C$ its corresponding **&#268;ech nerve** $C(U)$ is the [[simplicial object]] in $C$ that in degree $k$ is given by the $k$-fold [[fiber product]] of $U$ over $X$ with itself :

$$
  C(U) :=
  \left(
    \cdots
    U \times_X U \times_X U 
   \overset{\to}\rightrightarrows U \times_X U \rightrightarrows U
  \right)
  \,.
$$


### In $(\infty,1)$-category theory

The notion of Cech nerve makes sense in any [[(∞,1)-category]] with [[limit in a quasi-category|(∞,1)-pullbacks]].

See [[groupoid object in an (∞,1)-category]].


## Applications and occurences

* The [[cohomology]] theory obtained by mapping out of [[?ech cover]]s instead of general [[hypercover]]s is [[?ech cohomology]].

* A [[groupoid object in an (infinity,1)-category]] that is a &#268;ech nerve $U \to X$ exhibits $X$ as a [[delooping]].

  * In an [[infinity-stack]] [[(infinity,1)-topos]] every [[groupoid object in an (infinity,1)-category]] is a &#268;ech nerve.


## Examples

* For $U = \coprod_i U_i$ the disjoint union of over a covering [[sieve]] $\{U_i \to X\}$ with respect to a [[coverage]], the objectwise [[simplicial homotopy group|connected components]] of the &#268;ech nerve is the subfunctor corresponding to the sieve
  $$
    \Pi_0 C(U) = \bigcup_i hom(-,U_i)
    \,.
  $$

  This is described in more detail in the section "Interpretation in terms of higher descent and codescent" at [[sieve]].


[[!redirects Cech nerve]]
[[!redirects Cech-nerve]]
[[!redirects ?ech nerve]]
[[!redirects ?ech-nerve]]
[[!redirects ?ech nerve]]
[[!redirects ?ech-nerve]]
