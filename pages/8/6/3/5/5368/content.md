
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

This entry discusses [[model category]] structures on categories of [[algebras over an operad]] in the [[category of chain complexes]] (unbounded).

This is a special case of the general discussion at [[model structure on algebras over an operad]], but the category of (unbounded) chain complexes warrents some special attention.

For the operad of ordinary (commutative) algebras see also [[model structure on dg-algebras]].

## Definition

Let $k$ be a commutative ring. 

Write $Ch_\bullet(k)$ for the [[category of chain complexes|category of unbounded chain complexes]] of $k$-[[module]]s.

+-- {: .un_defn #SigmaSplitOperad}
###### Definition

An [[operad]] $P$ over $Ch_\bullet(k)$ is called **$\Sigma$-split** if (...)

=--

+-- {: .un_prop}
###### Proposition

* The [[associative operad]] $Assoc_k$ is $\Sigma$-split for all $k$.

* If $k$ contains the ring of [[rational number]]s, $\mathbb{Q} \hookrightarrow k$, then every $Ch_\bullet(k)$-operad is $\Sigma$-split.

=--

This is ([Hinich, example 4.2.5](#Hinich)).

+-- {: .un_prop #ModelStructure}
###### Proposition

Let $P$ be a $\Sigma$-[split operad](#SigmaSplitOperad) in $Ch_\bullet(k)$. Then the category $Alg_{Ch_\bullet(k)}(P)$ of [[algebras over an operad|algebras over the operad]] admits a [[model category]] structure whose weak equivalences are the [[quasi-isomorphism]]s and whose fibrations are the degreewise surjections in $Ch_\bulle(k)$.

=--

This appears as ([Hinich, theorem 4.1.1](#Hnich)).


## Properties

### Simplicial enrichment {#SimplicialEnrichment}

We discuss how the [above model structure](#ModelStructure) on $Alg_{Ch_\bullet(k)}(P)$ is enhanced to a [[simplicial model category]] structure.

+-- {: .un_defn}
###### Definition

For $n \in \mathbb{N}$ let $\Omega_{poly}^\bullet(\Delta^n)$ be the commutative [[dg-algebra]] of **[[polynomial]] [[differential form]]s** on the $n$-[[simplex]]:

as a graded algebra it is 

$$
  \Omega_{poly}^{\bullet}(\Delta^n)
  :=
  k[t_0, \cdots, t_n, d t_0, \cdots, d t_n]/(\sum t_i -1, \sum d t_i)
$$

with the differential the usual de Rham differential under the embedding $\Omega^\bullet_{poly}(\Delta^n) \hookrightarrow \Omega^\bullet(\Delta^n)$.

For $f : [k] \to [l]$ a [[morphism]] in the [[simplex category]] let

$$
  \Omega^\bullet_{poly}(f) : \Omega^\bullet_{poly}(\Delta^k) \to \Omega^\bullet_{poly}(\Delta^l)
$$

be the morphism of dg-algebras given on generators by 

$$
  \Omega^\bullet_{poly}(f) : t_i \mapsto \sum_{f(j) = i} t_j
  \,..
$$

This yields a [[simplicial object|simplicial]] commutative dg-algebra

$$
  \Omega^\bullet_{poly}(\Delta^{(-)}) : \Delta \to cdgAlg_k
  \,.
$$

=--

+-- {: .un_defn #SimplicialEnrichment}
###### Definition

For $P$ a dg-operad as above, define [[sSet]]-[[hom-object]]s between objects $A,B \in Alg(P)$ by

$$
  Alg_P(A,P) := ([n] \mapsto Hom_{Alg_P}(A, B \otimes \Omega^\bullet_{poly}(\Delta^n))
  \in sSet
  \,.
$$
 
=--

+-- {: .un_prop}
###### Proposition

With the [above model structure](#ModelStructure) and the [above simplicial enrichment](#SimplicialEnrichment), $Alg_{Ch_\bullet(K)}(P)$ becomes a [[simplicial model category]].

=--

This is ([Hinich, lemma 4.8.4](#Hinich)).

## Related concepts

* [[model structure on dg-operads]]

* **model structure on dg-algebras over an operad**

  * [[model structure on dg-algebras]]

  * [[model structure on dg-categories]]

## References

The model structure on dg-algebras over an operad is discussed in

* [[Vladimir Hinich]],  _Homological algebra of homotopy algebras_ Communications in algebra, 25(10). 3291-3323 (1997)([arXiv:q-alg/9702015](http://arxiv.org/abs/q-alg/9702015), _Erratum_ ([arXiv:math/0309453](http://arxiv.org/abs/math/0309453)))
{#Hinich}


based on results in

* A.K. Bousfield, V.K.A.M. Gugenheim, _On PL de Rham theory and rational homotopy type_ , Memoirs AMS, t.8, 179(1976)