
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
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

The notion of _elliptic chain complex_ is the generalization of the notion of [[elliptic operator]] from single [[linear maps]] to [[chain complexes]] of linear maps. 

## Definition

For $X$ a [[smooth manifold]] and $\{E_k\}_{k \in \mathbb{Z}}$ a collection of [[vector bundles]] over $X$, a [[chain complex]] of [[differential operators]] between the spaces of [[sections]] of these bundles

$$
  \cdots \to \Gamma(E_{k+1}) \stackrel{P_k}{\to} \Gamma(E_k) \to \cdots 
$$

is called an **elliptic chain complex** if the corresponding sequence of [[symbol of a differential operator|symbols]]

$$
  \cdots \to \pi^* E_{k+1} \stackrel{\sigma(P_k)}{\to} \pi^* E_k \to \cdots
$$

(where $\pi \colon T^* X \to X$ is the [[cotangent bundle]]) is an [[exact sequence]].

For instance ([Pati, def. 9.4.1](#Pati)).

For a single differential operator $P$ this says that $0 \to \pi^* E_1 \stackrel{\sigma(P)}{\to} \pi^* E_0 \to 0$ is exact, which means that $\sigma(P)$ is an [[isomorphism]], hence that $P$ is an [[elliptic operator]].

## Properties

If $(\mathcal{E}, d)$ is an elliptic complex of smooth [[sections]] $\mathcal{E} = \Gamma_X(E)$ of a [[vector bundle]] $E \to X$ overa [[compact topological space|compact]] [[closed manifold]] $X$, then the inclusion

$$
  (\mathcal{E},d) \hookrightarrow (\overline{\mathcal{E}}, d)
$$

into the complex of [[distribution|distributional]] [[sections]] is a [[quasi-isomorphism]], in fact a [[homotopy equivalence]]. 

([Atiyah-Bott](#AtiyahBott))

## Examples

The classical examples of elliptic complexes are discussed also in ([Gilkey section 3](#Gilkey)).

### de Rham complex

Let $X$ be a compact smooth manifold. Then the [[de Rham complex]] is an ellptic complex. The corresponding [[index of an elliptic complex]] is the [[Euler characteristic]]

$$
  Ind(\Omega^\bullet(X),d)  
  = 
  \chi(X)
  = 
  \sum_{p = 0}^{dim X} (-1)^p  dim H_{dR}^p(X, \mathbb{C})
$$

### The Yang-Mills complex

(...)

### The Dolbeault complex

(...) [[Dolbeault complex]]

The [[index of an elliptic complex]] of the Dolbeault complex is the [[arithmetic genus]]

### Spin complex

(...) index is [[A-hat genus]] (...)


## Related concepts

* [[index of an elliptic complex]]

## References

* V. Pati, _Elliptic complexes and index theory_ ([pdf](http://www.isibang.ac.in/~statmath/resource/elliptic.pdf))
 {#Pati}

* [[Peter Gilkey]], _The Atiyah-Singer Index Theorem -- Chapter 5_ ([pdf](http://www.maths.ed.ac.uk/~aar/papers/gilkey3.pdf))
 {#Gilkey}

* [[Michael Atiyah]], [[Raoul Bott]], _A Lefschetz fixed point formula for elliptic complexes. I_, Ann. of Math. (2) 86 (1967),
374&#8211;407. MR 0212836 (35 #3701)
 {#AtiyahBott}

[[!redirects elliptic chain complexes]]
[[!redirects elliptic complex]]
[[!redirects elliptic complexes]]

