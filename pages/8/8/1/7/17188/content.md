
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In ([Cartan-Eilenberg 56, XV.7](#CartanEilenberg56)) axioms for certain systems of bigraded [[modules]] $H(p,q)$ ("Cartan-Eilenberg systems") are given which imply the existence of a [[spectral sequence]] converging to $H(-\infty,\infty)$. See also ([Switzer 75, section 15, 1-7](#Switzer75)).

## Definition

A _Cartan-Eilenberg system_ $(H,\eta,\partial)$ consists of [[modules]] $H(p,q)$ for each $p\le q$, morphisms $\eta\colon H(p',q')\to H(p,q)$ for all $p\le p'$, $q\le q'$, and boundary morphisms $\partial\colon H(p,q) \to H(q,r)$ for all $p\le q\le r$, such that

1. $\eta=\mathrm{id}\colon H(p,q)\to H(p,q)$,

2. $\eta=\eta\circ\eta\colon H(p'',q'')\to H(p',q')\to H(p,q)$,

3. $\eta$ and $\partial$ commute,

4. there are long exact sequences $\cdots\to H(q,r)\stackrel\eta\to H(p,r)\stackrel\eta\to H(p,q)\stackrel\partial\to H(q,r)\to\cdots$.

Subject to convergence conditions...


The [[spectral sequence]] induced from $(H,\eta,\partial)$, is defined by

$$
  Z^r_p=\mathrm{im}\bigl(H(p,p+r)\stackrel\eta\to H(p,p+1)\bigr)\;,
$$

$$
  B^r_p=\mathrm{im}\bigl(H(p-r+1,p)\stackrel\partial\to H(p,p+1)\bigr)\;,
$$

$$
  E^r_p=Z^r_p/B^r_p\;,
$$

$$
  d^r_p\colon Z^r_p/B^r_p\twoheadrightarrow Z^r_p/Z^{r+1}_p\cong
B^{r+1}_{p+r}/B^r_{p+r}\hookrightarrow Z^r_{p+r}/B^r_{p+r}\;.
$$

In particular
$$\ker(d^r_p)=Z^{r+1}_p/B^r_p\qquad\text{and}\qquad
\mathrm{im}(d^r_p)=B^{r+1}_p/B^r_p\;.$$
For $a=\eta(a_0)\in H(p,p+1)$, $a_0\in H(p,p+r)$, one has
$$d^r_p([a])=[\partial a_0]\in E^r_p\qquad\text{with}\qquad\partial a_0\in H(p+r,p+r+1)\;.$$






## Examples

### Atiyah-Hirzebruch spectral sequences

The key example of such a system are the [[relative cohomology]] groups $E^\bullet(X^q, X^p)$ of a [[filtered topological space]] (see at [[spectral sequence of a filtered complex]]) for $E$ any [[generalized cohomology theory]]  ([Cartan-Eilenberg 56, XV.7, Example 2](#CartanEilenberg56)). That $E^\bullet(X^q, X^p)$ forms a suitable system of modules is the statement of the [exact sequence for triples](generalized+%28Eilenberg-Steenrod%29+cohomology#ExactnessForTriples) of any generalized cohomology theory.

This case of the Cartan-Eilenberg spectral sequence came to be known as the _[[Atiyah-Hirzebruch spectral sequence]]_.

+-- {: .num_defn #CESystemForMultiplicativeGeneralizedCohomology}
###### Definition

For $\pi\colon X\to B$ a [[Serre fibration]] over a [[CW-complex]] $B$.  And for $(\tilde h^\bullet,\delta,\wedge)$ a [[multiplicative cohomology theory|multiplicative]] [[reduced cohomology|reduced]]  [[generalized (Eilenberg-Steenrod) cohomology]] theory. 


define a [[Cartan-Eilenberg system]] $(H,\eta,\partial)$ by

$$
  H(p,q)=\tilde h^\bullet(X^{q-1}/X^{p-1})
$$

(where $X^k=\pi^{-1}(B^k)$) for $p\le q$ with the obvious maps $\eta\colon H(p',q')\to H(p,q)$ for $p\le p'$, $q\le q'$. 

The [[Cartan-Eilenberg spectral sequence]] of this Cartan-Eilenberg system is the [[Serre spectral sequence|Serre]]-[[Atiyah-Hirzebruch spectral sequence]].

=--

The corresponding [[long exact sequences]] take the form
$$\cdots\to\tilde h^\bullet(X^{r-1},X^{q-1})\to\tilde h^\bullet(X^{r-1},X^{p-1})
\to\tilde h^\bullet(X^{q-1},X^{p-1})\stackrel\delta\to
\tilde h^\bullet(X^{r-1},X^{q-1})\to\cdots$$




## Related concepts

* [[multiplicative spectral sequence]]

## References

* {#CartanEilenberg56} [[Henri Cartan]], [[Samuel Eilenberg]], _Homological algebra_, Princeton Univ. Press (1956)

* {#Switzer75} [[Robert Switzer]], _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975. 


[[!redirects Cartan-Eilenberg spectral sequences]]


[[!redirects Cartan-Eilenberg system]]
[[!redirects Cartan-Eilenberg systems]]
