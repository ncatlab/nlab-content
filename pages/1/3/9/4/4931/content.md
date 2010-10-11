+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
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

For $n \in \mathbb{N}$ a [[natural number]], the $n$-[[dimension]]al **ball** or **$n$-disk** is the [[topological space]]

$$
  D^n := \{ \vec x \in \mathbb{R}^n | \sum_{i} (x^i)^2 \leq 1\}
  \subset \mathbb{R}^n
$$ 

equipped with the [[induced topology]] as a subspace of the [[Cartesian space]] $\mathbb{R}^n$.

Its [[interior]] is the **open $n$-ball**

$$
  \mathbb{B}^n := \{ \vec x \in \mathbb{R}^n | \sum_{i} (x^i)^2 \lt 1 \}
  \subset \mathbb{R}^n
  \,.
$$ 

Its [[boundary]] is the $(n-1)$-[[sphere]].

## Properties {#Properties}



+-- {: .un_lemma}
###### Observation

The open $n$-ball is [[homeomorphic]] and even [[diffeomorphic]] to the [[Cartesian space]] $\mathbb{R}^n$

$$
  \mathbb{B}^n \simeq \mathbb{R}^n
  \,.
$$

=--

+-- {: .proof}
###### Proof

Use for instance the map 

$$
  f : \mathbb{R}^n \to \mathbb{B}^n
$$

given by

$$
  (x^1, \cdots, x^n) 
  \mapsto
  \left(
    \frac{x^1}{\sqrt{1 + r^2}},
    \cdots
    \frac{x^n}{\sqrt{1 + r^2}}
  \right)
  \,,
$$

where $r^2 = \sum_{i = 1}^n (x^i)^2$.

=--

So the open $n$-ball is naturally a ([[smooth manifold|smooth]]) [[manifold]]. And every (smooth) $n$-dimensional manifold is locally isomorphic to $\mathbb{B}^n$.

From very general existence results about [[smooth structure]]s on [[Cartesian space]]s we have that

+-- {: .un_theorem}
###### Theorem

In [[dimension]] $d \in \mathbb{N}$ for $d \neq 4$ we have:

every open subset of $\mathbb{R}^d$ which is [[homeomorphic]] to $\mathbb{B}^d$ is also [[diffeomorphic]] to it.

=--

See the first page of ([Ozols](#Ozols)) for a list of references. 


+-- {: .un_remark}
###### Remark

In dimension 4 the analog statement fails due to the existence of [[exotic smooth structure]]s on $\mathbb{R}^4$. 

=--

+-- {: .un_theorem}
###### Theorem

Let $C \subset \mathbb{R}^n$ be a [[star-shaped]] [[open subset]] of a [[Cartesian space]]. Then $C$ is [[diffeomorphic]] to $\mathb{R}^n$.

=--

This appears as [theorem 237](http://www.math.tu-berlin.de/~ferus/ANA/Ana3.pdf#page=154) of ([Ferus](#Ferus)).  Even an explicit construction of a diffeomorphism as asserted by the theorem is given there.



+-- {: .un_example}
###### Example


Let $I(\Delta^n) \subset \mathbb{R}^n$ be the [[interior]] of the standard $n$-[[simplex]]. Then there is a diffeomorphism to $\mathbb{B}^n$ defined as follows:

Parameterize the $n$-simplx as

$$
  I(\Delta^n) 
  =
  \left\{
    (x^1, \cdots, x^n) \in \mathbb{R}
    |
     (\forall i : x^i \gt 0)\; and \; ( \sum_{i=1}^n x^i \lt 1)
  \right\}
  \,.
$$

Then define the map $f : I(\Delta^n) \to \mathbb{R}^n$ by

$$
  (x^1, \ldots, x^n) 
  \mapsto 
  (\log(\frac{x^1}{1 - x^1 - \ldots -x^n}), 
  \ldots, 
  \log(\frac{x^n}{1 - x^1 - \ldots - x^n}))
  \,.
$$ 

=--

(Thanks to [[Todd Trimble]].)

## References

* V. Ozols, _Largest normal neighbourhoods_ ,
Proceedings of the American Mathematical Society
Vol. 61, No. 1 (Nov., 1976), pp. 99-101  ([jstor](http://www.jstor.org/stable/2041672))
{#Ozols}

* [[Dirk Ferus]], _Analysis III_ ([pdf](http://www.math.tu-berlin.de/~ferus/ANA/Ana3.pdf)) 
{#Ferus}


[[!redirects  balls]]

[[!redirects open ball]]
[[!redirects open balls]]

[[!redirects open n-ball]]
[[!redirects open n-balls]]

[[!redirects closed ball]]
[[!redirects closed balls]]

[[!redirects closed n-ball]]
[[!redirects closed n-balls]]

[[!redirects disk]]
[[!redirects disks]]

[[!redirects n-disk]]
[[!redirects n-disks]]