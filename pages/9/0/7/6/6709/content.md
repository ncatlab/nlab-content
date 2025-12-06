
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A family of [[characteristic class]]es that obstruct [[orientation]], [[spin structure]], [[spin^c structure]], [[w4-orientation of EO(2)-theory|orientation of EO(2)-theory]] etc.

Stiefel-Whitney classes have coefficients in $\mathbb{Z}_2$, but via the [[Bockstein homomorphism]] they are lifted to [[integral Stiefel-Whitney class]]es.

## Definition
 {#Definition}

+-- {: .num_defn #AxiomaticDefinition}
###### Definition
**(axiomatic definition)**

The _Stiefel-Whitney classes_ are [[characteristic classes]] $w_i \in H^{i}(B O(n), \mathbb{Z}_2)$ on the [[classifying space]] of the [[orthogonal group]] in [[dimension]] $n$, defined by

1. $w_0 = 1$ and if $i \gt n$ then $w_i = 0$;

1. for $n = 1$,  $w_1 \neq 0$;

1. for the inclusion $\iota : B O(n) \hookrightarrow B O(n+1)$ we have $\iota^* w_i^{(n+1)} = w_i^{(n)}$;

1. **sum rule**: for all $k,l \in \mathbb{N}$ with the canonical inclusion

   $$
     \iota : B O(k) \times B O(l) \to B O(k+l)
   $$ 

   we have for all $i \in \mathbb{N}$ that 

   $$
    \iota^* w_i = \sum_{j = 0}^i w_j \cup w_{i-j}
   $$ 

   (on the right the [[cup product]]).

=--

+-- {: .num_defn #TotalSWClass}
###### Definition

For $E \to X$ a real [[vector bundle]]/[[orthogonal group]]-[[principal bundle]], the **total universal Stiefel-Whitney class** $w(E)$ is

$$ 
  w(E) \coloneqq \sum_i w_i(E) \in H^\bullet(X, \mathbb{Z}_2) 
$$

as an element in the [[cohomology ring]]. 

=--

+-- {: .num_remark}
###### Remark

For the total SW class of def. \ref{TotalSWClass}, the sum rule of def. \ref{AxiomaticDefinition} says equivalently  that for $E_1, E_2$ two real [[vector bundles]], then the total SW class of their [[direct sum of vector bundles]] is the [[cup product]] of the separate classes:

$$
  w(E_1 \oplus E_2) = w(E_1) \cup w(E_2)
  \,.
$$

=--

## Constructions

(...)

## Properties

### Spanning the cohomology ring of $B SO$

+-- {: .num_prop}
###### Proposition

Every class in the [[ordinary cohomology]] $H^\bullet(B O(n), \mathbb{Z}_2)$ and $H^\bullet(B S O(n), \mathbb{Z}_2)$ of the [[classifying spaces]] of the ([[special orthogonal group|special]]) [[orthogonal group]] with [[coefficients]] in [[cyclic group of order 2|$\mathbb{Z}_2$]] is  uniquely a [[polynomial]] in the Stiefel-Whitney classes. In fact the [[cohomology rings]] are [[polynomial]] algebras over $\mathbb{Z}_2$ in the SW classes:

$$
  H^\bullet(B O(n), \mathbb{Z}_2)  
  \simeq
  \mathbb{Z}_2[w_1, \cdots, w_n]  
  \,,
$$
$$
  H^\bullet(B S O(n), \mathbb{Z}_2)  
  \simeq
  \mathbb{Z}_2[w_2, \cdots, w_n]  
  \,.
$$

=--

([Milnor & Stasheff 74, Theorem 7.1. & Theorem 12.4.](#MilnorStasheff74))

### Whitney duality formula

For $X \hookrightarrow \mathbb{R}^q$ an [[embedding]] of a compact manifold, write $\tau := T X$ for the [[tangent bundle]] and $\nu$ for the corresponding [[normal bundle]]. Then since

$$
  \tau \oplus \nu \simeq T \mathbb{R}^q
$$

and the class of the vector bundle on the right is trivial, the sum rule for the SW classes says gives the [[cup product]] duality

$$
  w(\tau) \cup w(\nu) = 1
  \,.
$$

### Relation to Chern-classes
 {#RelationToChernClasses}

+-- {: .num_prop}
###### Proposition

If $E_{\mathbb{C}}$ is a complex [[vector bundle]]/ $U(n)$-[[principal bundle]] and $E_{\mathbb{R}}$ is the underlying real vector bundle / $O(2n)$-[[principal bundle]] then the second Stiefel-Whitney class is given by the [[first Chern class]] mod 2:

$$ 
  w_2(E_{\mathbb{R}}) = c_1(E_{\mathbb{C}}) \; mod 2
  \,.
$$

=--

+-- {: .num_cor}
###### Corollary

An [[almost complex structure]] on the  [[tangent bundle]] of a [[manifold]] induces a [[spin^c structure]]. 

=--

This is discussed at _[Spin^c-structure -- From almost complex structures](spin^c+structure#FromAlmostComplexStructures)_.

+-- {: .num_remark}
###### Remark

More generally, the SW classes are then given by the [[Chern character]]. See for instance [Milnor-Stasheff, p. 171](#MilnorStasheff).

=--

## Related concepts

* [[orientation]], [[Spin structure]], [[w4-structure]]

* [[Chern class]]

* [[Pontryagin class]], [[Wu class]], [[one-loop anomaly polynomial I8]]

* [[orthogonal calculus]]

## References 

Named after [[Eduard Stiefel]] and [[Hassler Whitney]].

Textbook accounts include

* {#MilnorStasheff} [[John Milnor]], [[Jim Stasheff|James D. Stasheff]], _Characteristic Classes_, Annals of Mathematics Studies 76, Princeton University Press (1974). 

* {#Kochmann96} [[Stanley Kochmann]], section 2.3 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996  

* [[Peter May]], chapter 23, section 3 of _A concise course in algebraic topology_ ([pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))

Discussion with an eye towards [[mathematical physics]]

* {#RudolhSchmidt} Gerd Rudolph, Matthias Schmidt, _Differential Geometry and Mathematical Physics: Part II. Fibre Bundles, Topology and Gauge Fields_, Theoretical and Mathematical Physics series, Springer 2017 ([doi:10.1007/978-94-024-0959-8](https://link.springer.com/book/10.1007/978-94-024-0959-8))

Stiefel-Whitney classes generating the [[cohomology ring]] of $BO(n)$

* {#MilnorStasheff74} [[John Milnor]], [[Jim Stasheff]], _Characteristic classes_, Princeton Univ. Press (1974) ([ISBN:9780691081229](https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes-am-76-volume-76), [doi:10.1515/9781400881826](https://doi.org/10.1515/9781400881826), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/milnstas.pdf))


See also

* Wikipedia, _[Stiefel-Whitney class](http://en.wikipedia.org/wiki/Stiefel%E2%80%93Whitney_class)_

[[!redirects Stiefel-Whitney classes]]

[[!redirects first Stiefel-Whitney class]]
[[!redirects second Stiefel-Whitney class]]

[[!redirects Stiefel-Whitney number]]
[[!redirects Stiefel-Whitney numbers]]
