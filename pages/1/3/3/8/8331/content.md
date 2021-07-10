
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

For $C_{\bullet, \bullet}$ a [[double complex]] (in some [[abelian category]] $\mathcal{A}$), its _total complex_ $Tot(C)_\bullet$ is an ordinary complex which in degree $k$ is the [[direct sum]] of all components of total degree $k$.
 

## Definition

Let $\mathcal{A}$ be an [[abelian category]] with arbitrary [[direct sums]].

Write $Ch_\bullet(\mathcal{A})$ for the [[category of chain complexes]] in $\mathcal{A}$ and $C_{\bullet, \bullet} \in Ch_\bullet(Ch_\bullet(\mathcal{A}))$ for the category of [[double complexes]]. (Hence we use the convention that in a double complex the vertical and horizontal [[differential]] commute with each other.)

+-- {: .num_defn}
###### Definition

For $C_{\bullet, \bullet} \in Ch_\bullet(Ch_\bullet(\mathcal{A}))$ a [[double complex]], its associated **total complex** $Tot(C)_\bullet \in Ch_\bullet(\mathcal{A})$ is the [[chain complex]] whose components are the [[direct sums]], [[direct products]] or a mixture of those

The sum total complex
$$
  Tot^{\oplus}(C)_n = \bigoplus_{k+l = n} C_{k,l}
$$
the product total complex
$$
  Tot^{\pi}(C)_n = \prod_{k+l = n} C_{k,l}
$$
the product-sum total complex
$$
  Tot^{\pi\oplus}(C)_n = \prod_{k+l = n, k \lt 0} C_{k,l}\oplus\bigoplus_{k+l = n, k\geq 0} C_{k,l}
$$
and the sum-product total complex
$$
  Tot^{\oplus\pi}(C)_n = \bigoplus_{k+l = n, k \lt 0} C_{k,l}\oplus\prod_{k+l = n, k\geq 0} C_{k,l}
$$

and whose [[differentials]] are given by the [[linear combination]]

$$
  \partial^{Tot}
  \coloneqq
  \partial^C_{vert} + (-1)^{vertical\;degree} \partial^C_{hor}  
  \,. 
$$
Using the four different types of total complexes gives the flexibility to make more nuanced exactness statements for the total complex under various assumptions on the double complex.

=--

## Properties
 {#Properties}

### Total homology and spectral sequences
 {#TotalHomology}

+-- {: .num_remark #TotalHomology}
###### Remark

The [[chain homology]] of the total complex $Tot(C)_\bullet$ is sometimes called the **total homology** of the [[double complex]] $C_{\bullet, \bullet}$.

=--

+-- {: .num_remark }
###### Remark

A tool for computing the homology of a total complex, hence for computing the total homology of a double complex, is the _[[spectral sequence of a double complex]]_.
See there for more details.

=--

### Exactness

+-- {: .num_prop #TotOfBoundedDegreewiseExactIsExact}
###### Proposition

First let $C$ be a double complex in any abelian category

* If $C_{\bullet,\bullet}$ is bounded and has [[exact sequence|exact]] rows or columns then also $Tot(C)_\bullet$ is exact.

Now let $C$ be a double complex of abelian groups.

* If $C_{\bullet,\bullet}$ has exact rows then the product-sum total complex is exact.
* If $C_{\bullet,\bullet}$ has exact rows and kernels (or equivalently) images between row complexes are exact, then the sum and product total complexes are exact
* If $C_{\bullet,\bullet}$ has exact rows and for each $i$ taking $H_i$ of the columns gives an exact complex, then the sum-product total complex is exact.

=--

+-- {: .proof}
###### Proof

Use the [[acyclic assembly lemma]].

=--

### Relation to total simplicial sets and homotopy colimits
 {#RelationToTotalSimplicialSets}

The total chain complex is, under the [[Dold-Kan correspondence]], equivalent to the [[diagonal of a bisimplicial set]] -- see [[Eilenberg-Zilber theorem]]. As discussed at _[[bisimplicial set]]_, this is [[weak homotopy equivalence|weakly homotopy equivalent]] to  the _[[total simplicial set]]_ of a bisimplicial set.

## References

For instance secton 1.2 of 

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_


[[!redirects total complexes]]
[[!redirects total chain complex]]
[[!redirects total chain complexes]]
