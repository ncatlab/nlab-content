
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $T$ be an abelian [[Lawvere theory]] (one containing the theory of [[abelian group]]s). Write $\mathbb{A}^1$ for its canonical [[line object]] and $\mathbb{G}_m$ for the corresponding multiplicative group object.

The **projective space** $\mathbb{P}_n$ of $T$ is the [[quotient]]

$$
  \mathbb{P}_n := (\mathbb{A}^{n+1} - \{0\})/\mathbb{G}_m
$$

of the $(n+1)$-fold [[product]] of the line with itself by the canonical [[action]] of $\mathbb{G}_m$. Any point $(x_0,x_1,\ldots,x_n)\in \mathbb{A}^{n+1} - \{0\}$ gives _homogeneous coordinates_ for its image under the quotient map. When considered in this fashion, one often writes $[x_0:x_1:\ldots:x_n]$. Homogeneous  coordinates were introduced in [M&#246;bius 27](#Mobius27)

More generally, for $(X,0)$ a pointed space with (pointed) $\mathbb{G}_m$-[[action]], the quotient 

$$
 \mathbb{P}(X) :=  (X-\{0\})/\mathbb{G}_m
$$ 

is the corresponding projective space.

If instead of forming the [[quotient]] one forms the weak quotient/[[action groupoid]], one speaks of the [[projective stack]]

$$
  \hat \mathbb{P}(X) := (X-\{0\})//\mathbb{G}_m
  \,.
$$




## Examples

### For commutative rings and algebras

For $T$ the theory of commutative [[ring]]s or more generally commutative [[associative algebra]]s over a ring $k$, $\mathbb{A}_k^1$ is the standard [[affine line]] over $k$. In this case $\mathbb{P}^n_k$ is (...) A closed sub[[scheme]] of $\mathbb{P}^n_k$ is a [[projective scheme]].

+-- {: .un_prop}
###### Proposition

For $R$ a commutative $k$-algebra, there is a [[natural isomorphism]] between

* $\mathbb{Z}$-[[graded algebra|gradings]] on $R$;

* $\mathbb{G}_m$-[[action]]s on $Spec R$.

=--

The proof is spelled out at [[affine line]].

### Over the real and complex numbers

* $\mathbb{C}P^1$ is the [[Riemann sphere]]

* for $\mathbb{C}P^n$  see at _[[complex projective space]]_

* for $\mathbb{R}P^n$ see at _[[real projective space]]_

Let $k$ be the [[topological field]] such as

* $k = \mathbb{R}$ the [[real numbers]]

* or $k = \mathbb{C}$ the [[complex numbers]]

equipped with their [[Euclidean space|Euclidean]] [[metric topology]].

We discuss the projective spaces $k P^n$ as [[topological spaces]], [[topological manifolds]] and [[differentiable manifolds]].

+-- {: .num_defn #ToplogicalProjectiveSpace}
###### Definition
**(topological projective space)**

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


## Related concepts

* [[projective plane]]

* [[projective variety]]

* [[Grassmannian]]

* [[projective geometry]], [[synthetic projective geometry]]

* [[projective linear group]]

* [[tautological line bundle]]

* [[projective bundle]]

## References

* {#Mobius27} [[August Ferdinand Möbius]], _Der barycentrische Calc&#252;l_ (1827)

An introduction to projective spaces over the theory of ordinary commutative rings is in

* Miles Reid, _Graded rings and varieties in weighted projective space_ ([pdf](http://www.warwick.ac.uk/~masda/surf/more/grad.pdf))

* [[Aurelio Carboni]], [[Marco Grandis]] , _Categories of projective spaces_ , JPAA **110** (1996) pp.241-258. 

[[!redirects projective spaces]]

[[!redirects homogeneous coordinates]]

