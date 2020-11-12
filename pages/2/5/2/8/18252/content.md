
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The canonical [[line bundle]] over a [[projective space]] is sometimes called its "tautological line bundle". For more see at _[[classifying space]]_.

## Definition

### As a topological line bundle
  {#AsAtopologicalLieBundle}

We discuss the tautological line bundle as a [[topological vector bundle]]. Hence let $k$ be the [[topological field]] either

* $k = \mathbb{R}$ the [[real numbers]]

* or $k = \mathbb{C}$ the [[complex numbers]]

equipped with their [[Euclidean space|Euclidean]] [[metric topology]].

+-- {: .num_defn #ToplogicalProjectiveSpace}
###### Definition
**(topological [[projective space]])**

Let $n \in \mathbb{N}$. Consider the [[Euclidean space]] $k^{n+1}$ equipped with its [[metric topology]], let $k^{n+1} \setminus \{0\} \subset k^{n+1}$ be the [[topological subspace]] which is the [[complement]] of the origin, and consider on its underlying set the [[equivalence relation]] which identifies two points if they differ by [[multiplication]] with some $c \in k$ (necessarily non-zero):

$$
  (\vec x_1 \sim \vec x_2)
   \;\Leftrightarrow\;
  \left(
    \underset{c \in k}{\exists}
    ( \vec x_2 = c \vec x_1 )
  \right)
  \,.
$$

The [[equivalence class]] $[\vec x]$ is traditionally denoted

$$
  [x_1 : x_2 : \cdots : x_{n+1}]
  \,.
$$


Then the _[[projective space]]_ $k P^n$ is the corresponding [[quotient topological space]] 

$$
  k P^n \;\coloneqq\; \left(k^{n+1} \setminus \{0\}\right) / \sim
  \,.
$$



=--

+-- {: .num_defn #TopologicalProjectiveSpaceStandardOpenCover}
###### Definition
**(standard open cover of topological projective space)**

For $n \in \mathbb{N}$ the _standard open cover_ of the projective space $k P^n$ (def. \ref{ToplogicalProjectiveSpace}) is 

$$
  \left\{
    U_i \subset k P^n
  \right\}_{i \in \{1, \cdots, n+1\}}
$$

with 

$$
  U_i 
    \coloneqq 
  \left\{ 
    [x_1 : \cdots : x_{n+1}] \in k P^n
    \;\vert\;
    x_i \neq 0
  \right\}
  \,.
$$

To see that this is an open cover:

1. This is a cover because with the orgin removed in $k^n \setminus \{0\}$ at every point $[x_1: \cdots : x_{n+1}]$
   at least one of the $x_i$ has to be non-vanishing.

1. These subsets are open in the [[quotient topology]] $k P^n = (k^n \setminus \{0\})/\sim$, since their [[pre-image]] under the quotient co-projection $k^{n+1} \setminus \{0\} \to k P^n$ coincides with the pre-image $(pr_i\circ\iota)^{-1}( k \setminus \{0\} )$ under the [[projection]] onto the $i$th coordinate in the [[product topological space]] $k^{n+1} = \underset{i \in \{1,\cdots, n\}}{\prod} k$ (where we write $k^n \setminus \{0\} \overset{\iota}{\hookrightarrow} k^n \overset{pr_i}{\to} k$).


=--

+-- {: .num_defn #TautologicalTopologicalLineBundle}
###### Definition
**(tautological topological line bundle)

For $k$ a [[topological field]] and $n \in \mathbb{N}$, the _tautological line bundle_ over the [[projective space]] $k P^n$ is topological $k$-[[line bundle]] whose total space is the following [[subspace]] of the [[product space]] of the [[projective space]] $k P^n$ with $k^n$:

$$
  T
   \coloneqq
  \left\{
    ( [x_1: \cdots : x_{n+1}], \vec v)
    \in
    k P^n \times k^{n+1}
    \;\vert\;
    \vec v \in \langle \vec x\rangle_k
  \right\}
  \,,
$$

where $\langle \vec x\rangle_k \subset k^{n+1}$ is the $k$-[[linear span]] of $\vec x$.

(The space $T$ is the space of pairs consisting of the "name" of a $k$-line in $k^{n+1}$ together with an element of that $k$-line)

This is a bundle over [[projective space]] by the projection function

$$
  \array{
    T &\overset{\pi}{\longrightarrow}& k P^n
    \\
    ([x_1: \cdots : x_{n+1}], \vec v) &\mapsto& [x_1: \cdots : x_{n+1}]
  }
  \,.
$$

=-- 

+-- {: .num_prop #WellDefinedTautologicalTopologicalLineBundle}
###### Proposition
**(tautological topological line bundle is well defined)**

The tautological line bundle in def. \ref{TautologicalTopologicalLineBundle} is well defined in that it indeed admits a [[local trivialization]].

=--

+-- {: .proof}
###### Proof

We claim that there is a local trivialization over the canonical cover of def. \ref{TopologicalProjectiveSpaceStandardOpenCover}. This is given for $i \in \{1, \cdots, n\}$ by

$$
  \array{
    U_i \times k &\overset{}{\longrightarrow}& T\vert_{U_i}
    \\
    ( [x_1 : \cdots x_{i-1}: 1 : x_{i+1} : \cdots : x_{n+1}] , c )
      &\mapsto&
    ( [x_1 : \cdots x_{i-1} : 1 : x_{i+1} : \cdots : x_{n+1} ], (c x_1, c x_2, \cdots , c x_{n+1}) )
  }
  \,.
$$

This is clearly a [[bijection]] of underlying sets.

To see that this function and its inverse function are continuous, hence that this is a [[homeomorphism]] notice that this map is the [[extension]] to the [[quotient topological space]] of the analogous map

$$
  \array{
    ( (x_1, \cdots, x_{i-1}, x_{i+1}, \cdots, x_{n+1}) , c)
     &\mapsto&
    ( (x_1, \cdots, x_{i-1}, x_{i+1}, \cdots, x_{n+1}) , (c x_1, \cdots c x_{i-1}, c, c x_{i+1}, \cdots, c x_{n+1}) )
  }
  \,.
$$

This is a [[polynomial]] function on [[Euclidean space]] and since [[polynomials are continuous]], this is continuous. Similarly the [[inverse function]] lifts to a [[rational function]] on a subspace of Euclidean space, and since [[rational functions are continuous]] on their domain of definition, also this lift is continuous. 

Therefore by the [[universal property]] of the [[quotient topology]], also the original functions are continuous.


=--



## Examples

### Line bundle over Riemann sphere

* The [[basic complex line bundle on the 2-sphere]] is the tautological [[complex line bundle]] over the [[complex projective space]] $\mathbb{C}P^1 \simeq S^2$ (the [[Riemann sphere]]).

## Related concepts

* [[Bott element]]

* [[tautological equivariant line bundle]]

* [[resolution of singularities]]


## References

Lecture notes include

* {#Wirthmuller12} [[Klaus Wirthmüller]], section 2 of _Vector bundles and K-theory_, 2012 ([pdf](ftp://www.mathematik.uni-kl.de/pub/scripts/wirthm/Top/vbkt_skript.pdf))


See also

* Wikipedia, _[Tautological bundle](https://en.wikipedia.org/wiki/Tautological_bundle)_

[[!redirects tautological line bundles]]
