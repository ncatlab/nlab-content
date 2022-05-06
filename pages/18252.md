
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


### Definition
  {#BareDefinition}

Let $k$ be a [[field]] (or more generally a [[ring]]) and $n \in \mathbb{N}$ a [[natural number]].
Then the _tautological $k$-line bundle_ over the [[projective space]] $k P^n$ is the following vertical [[bundle]] map:

\[
  \label{TautologicalBundleProjection}
  \array{
    \mathcal{L}_{k P^n}
    & \coloneqq & 
    \frac{
      (k^{n+1} \setminus \{0\}) \times k^\ast
    }{
      k^\times
    }
    &
    \overset{
      [v,z]
      \mapsto
      \big(
        [v], v \cdot z
      \big)
    }{\hookrightarrow}
    &
    \frac{
      k^{n+1} \setminus \{0\}
    }{
      k^\times
    }    
    \times
    k^{n+1}
    \\
    \big\downarrow
    &&
    \big\downarrow {}^{\mathrlap{
       \frac{id \times pt}{ k^\times }
    }}
    \\
    k P^n
    &=&
    \frac{
      (k^{n+1} \setminus \{0\}) \times \ast
    }{
      k^\times
    }
  }
\]

Here:

* $k^{n+1} \coloneqq \underset{k\;summands}{\underbrace{k \oplus \cdots \oplus k}}$ is the canonical $n+1$-[[dimension|dimensional]] $k$-[[vector space]];

* $k^\times \,\coloneqq\, k \setminus \{0\}$ is the [[group of units]] of $k$;

* $\frac{(-) \times (-)}{k^\times}$ denotes the [[quotient space]] of a [[product space]] by the [[diagonal action]];

* and $k^\ast$ is $k$ equipped with the _dual_ $k^\times$-action

  \[
    \label{DualActionOnk}
    \array{
      k^\times \times k^\ast 
      &\longrightarrow&
      k^\ast
      \\
      (g,z) &\mapsto& z/g
    }
  \]

* so that, for $z \neq 0$,

  $$
    [v,z] 
      \;=\; 
    [v, z \cdot 1] 
      \;=\; 
    [v \cdot z, 1] 
      \;\;\in\;\;
    \frac{
      (V \setminus \{0\}) \times k^\ast
    }{
      k^\times
    }
  $$

This is "tautological" in the sense that the [[fiber]] of the bundle over a point $[v]$ in the projective base space, which is the name of the line through some vector $v$, consists of all the points $z \cdot v$ on that line -- as made explicit by the horizontal map in (eq:TautologicalBundleProjection).

The further [[corestriction]] of that horizontal map to $k^{n+1}$

$$
    \mathcal{L}_{k P^n}
    \coloneqq 
    \frac{
      (k^{n+1} \setminus \{0\}) \times k^\ast
    }{
      k^\times
    }
    \overset{
      [v,z]
      \mapsto
       v \cdot z
    }{\longrightarrow}
    k^{n+1}
$$

exhibits the total space of the tautological bundle as the "[[blow-up]]" of the origin of $k^{n+1}$.

{#Illustration} The following illustration shows the tautological [[real line bundle]] over 1-dimensional [[real projective space]], but the general picture is "the same", up to higher dimensionality of all spaces involved:

\begin{imagefromfile}
  "file_name": "TautologicalLineBundleOverRP1.jpg",
  "width": 700
\end{imagefromfile}


### Dual tautological line bundle
 {#DualTautologicalLineBundle}

The [[dual vector bundle|dual line bundle]] of the tautological line bundle is 

\[
  \label{DualTautologicalBundleProjection}
  \array{
    \mathcal{L}^\ast_{k P^n}
    & \coloneqq & 
    \frac{
      (k^{n+1} \setminus \{0\}) \times k
    }{
      k^\times
    }
    &
    \overset{
      [v,z]
      \mapsto
      [ (v , z) ]
    }{\hookrightarrow}
    &
    \frac{
      k^{n+2} \setminus \{0\}
    }{
      k^\times
    } 
    &
    =
    \,
    k P^{n+1}   
    \\
    \big\downarrow
    &&
    \big\downarrow {}^{\mathrlap{
       \frac{id \times pt}{ k^\times }
    }}
    \\
    k P^n
    &=&
    \frac{
      (k^{n+1} \setminus \{0\}) \times \ast
    }{
      k^\times
    }
  }
\]

with [[typical fiber]] $k$ instead of $k^\ast$, meaning that the [[action]] of $k^\times$ on the fibers is now the direct multiplication action, instead of the dual action (eq:DualActionOnk).

The horizontal map in (eq:DualTautologicalBundleProjection) [[embedding of topological spaces|embeds]] the [[complement]] of the single point $[(v=0,1)] \in k P^{n+1}$. That point however is the [[limit of a sequence|limit]] as $z \to \infty$, hence is the image of the base point as (eq:DualTautologicalBundleProjection) [[extension|extends]] to a map on the [[Thom space]] of the dual tautological line bundle:

$$
  Th
  \left(
    \mathcal{L}^\ast_{k P^n}
  \right)
    \underoverset
    {\simeq}
    {
      [v,z]
      \mapsto
      \left\{
      \array{
        [(0,1)] &\vert& z = \infty
        \\
        [ (v , z) ] &\vert& else
      }
      \right.
    }{\longrightarrow}
   k P^{n+1}
  \,.
$$


### As a topological line bundle
  {#AsAtopologicalLieBundle}

We make fully explicit how the tautological line bundle is a [[topological vector bundle]]. Hence regard $k$ as a [[topological field]], either

* $k = \mathbb{R}$ the [[real numbers]],

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

### Möbius strip

The tautological line bundle over the 1-dimensional [[real projective space]] $\mathbb{R}P^1$ is the [[Möbius strip]].


### Over Riemann sphere

The [[basic complex line bundle on the 2-sphere]] is the tautological [[complex line bundle]] over the [[complex projective space]] $\mathbb{C}P^1 \simeq S^2$ (the [[Riemann sphere]]).

This plays a key role in [[topological K-theory]] and more generally in [[complex oriented cohomology theory]].

## Related concepts

* [[Bott element]]

* [[tautological equivariant line bundle]]

* [[resolution of singularities]]


## References

Lecture notes:

* {#Wirthmuller12} [[Klaus Wirthmüller]], section 2 of _Vector bundles and K-theory_, 2012 ([pdf](ftp://www.mathematik.uni-kl.de/pub/scripts/wirthm/Top/vbkt_skript.pdf))


See also:

* Wikipedia, _[Tautological bundle](https://en.wikipedia.org/wiki/Tautological_bundle)_

[[!redirects tautological line bundles]]
