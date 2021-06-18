
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #BUn}
###### Definition

For $n \in \mathbb{N}$ write $U(n)$ for the [[unitary group]] in dimension $n$ and $O(n)$ for the [[orthogonal group]] in dimension $n$, both regarded as [[topological group]]s in the standard way. Write $B U(n) , B O(n) \in$ [[Top]] for the corresponding [[classifying space]].

Write 

$$
  [X, B O(n)] := \pi_0 Top(X, B O(n))
$$

and

$$
  [X, B U(n)] := \pi_0 Top(X, B U(n))
$$

for the set of [[homotopy]]-classes of [[continuous function]]s $X \to B U(n)$.

=--

+-- {: .num_prop #BUnClassifyingSpace}
###### Proposition

This is equivalently the set of [[isomorphism]] classes of $O(n)$- or $U(n)$-[[principal bundles]]  on $X$ as well as of rank-$n$ real or complex [[vector bundles]] on $X$, respectively:

$$
  [X, B O(n)] \simeq O(n) Bund(X) \simeq Vect_{\mathbb{R}}(X,n)
  \,,
$$

$$
  [X, B U(n)] \simeq U(n) Bund(X) \simeq Vect_{\mathbb{C}}(X,n)
  \,.
$$

=--

+-- {: .num_defn #InclusionOfUns}
###### Definition

For each $n$ let 

$$
  U(n) \to U(n+1)
$$

be the inclusion of [[topological group]]s given by inclusion of $n \times n$ [[matrices]] into $(n+1) \times (n+1)$-matrices given by the block-diagonal form

$$
  \left[g\right] \mapsto 
  \left[
    \array{
      1 & [0]
      \\ 
      [0] & [g]
    }
  \right]
  \,.
$$

This induces a corresponding sequence of morphisms of classifying spaces, def. \ref{BUn}, in [[Top]]

$$
  B U(0) \hookrightarrow B U(1) \hookrightarrow B U(2) \hookrightarrow \cdots
  \,.
$$

Write 

$$
  B U := {\lim_{\to}}_{n \in \mathbb{N}} B U(n)
$$

for the [[homotopy colimit]] (the "homotopy [[direct limit]]") over this diagram (see at _[[homotopy colimit]]_ the section _[Sequential homotopy colimits](homotopy+limit#SequentialHocolims)_).

=--

+-- {: .num_remark }
###### Remark

The [[topological space]] $B U$ is **not** equivalent to $B U(\mathcal{H}) $, where $U(\mathcal{H})$ is the [[unitary group]] on a separable infinite-dimensional [[Hilbert space]] $\mathcal{H}$. In fact the latter is [[contractible]], hence has a  [[weak homotopy equivalence]] to the point

$$  
  B U(\mathcal{H}) \simeq *
$$

while $B U$ has nontrivial [[homotopy group]]s in arbitrary higher degree (by [[Kuiper's theorem]]). 

But there is the group $U(\mathcal{H})_{\mathcal{K}} \subset U(\mathcal{H})$ of unitary operators that differ from the [[identity]] by a [[compact operator]]. This is essentially $U = \Omega B U$. See [below](#Uk). 

=--

## Properties

### Classifying space for topological K-theory

+-- {: .num_prop }
###### Proposition

Write $\mathbb{Z}$ for the set of [[integers]] regarded as a [[discrete topological space]].

The product spaces

$$
  B O \times \mathbb{Z}\,,\;\;\;\;\;B U \times \mathbb{Z}
$$

are [[classifying spaces]] for real and complex [[topological K-theory]], respectively: for every compact Hausdorff topological space $X$, we have an isomorphism of groups

$$
  \tilde K(X)
  \simeq
  [X, B U ]
  \,.
$$


$$
  K(X)
  \simeq
  [X, B U \times \mathbb{Z}]
  \,.
$$

=--

See for instance ([Friedlander, prop. 3.2](#Friedlander)) or ([Karoubi, prop. 1.32, theorem 1.33](#Karoubi)).

+-- {: .proof}
###### Proof

First consider the statement for reduced cohomology $\tilde K(X)$:

Since a [[compact topological space]] is a [[compact object]] in [[Top]] (and using that the [[classifying space]]s $B U(n)$ are (see there) [[paracompact topological space]]s, hence normal, and since the inclusion morphisms are closed inclusions (...)) the [[hom-functor]] out of it commutes with the [[filtered colimit]]

$$
  \begin{aligned}
    Top(X, B U)
    &=
    Top(X, {\lim_\to}_n B U(n))
    \\
    & \simeq {\lim_\to}_n Top(X, B U (n))
  \end{aligned}
  \,.
$$

Since $[X, B U(n)] \simeq U(n) Bund(X)$, in the last line the colimit is over [[vector bundle]]s of all ranks and identifies two if they become isomorphic after adding a trivial bundle of some finite rank.

For the full statement use that by prop. \ref{missing} we have

$$
  K(X) \simeq H^0(X, \mathbb{Z}) \oplus \tilde K(X)
  \,.
$$

Because $H^0(X,\mathbb{Z}) \simeq [X, \mathbb{Z}]$ it follows that

$$
  H^0(X, \mathbb{Z}) \oplus \tilde K(X)
  \simeq
  [X, \mathbb{Z}] \times [X, B U]
  \simeq
  [X, B U \times \mathbb{Z}]
  \,.
$$

=--

There is another variant on the classifying space 

+-- {: .num_defn #Uk}
###### Definition

Let 

$$
  U_{\mathcal{K}}
  = 
  \left\{
    g \in U(\mathcal{H}) | g - id \in \mathcal{K}
  \right\}
$$ 

be the group of unitary operators on a [[separable Hilbert space]] $\mathcal{H}$ which differ from the identity by a [[compact operator]].

=--

Palais showed that


+-- {: .num_prop }
###### Proposition

$U_\mathcal{K}$ is a [[homotopy equivalence|homotopy equivalent]] model for $B U$. It is in fact the [[norm closure]] of the evident model of $B U$ in $U(\mathcal{H})$. 

Moreover $U_{\mathcal{K}} \subset U(\mathcal{H})$ is a [[Banach Lie group|Banach Lie]] [[normal subgroup]].

=--

Since $U(\mathcal{H})$ is [[contractible]], it follows that 

$$
  B U_{\mathcal{K}} \coloneqq U(\mathcal{H})/U_{\mathcal{K}}
$$

is a model for the [[classifying space]] of reduced complex [[topological K-theory]] [[KU]].

## Related concepts

* [[stable orthogonal group]]

## References

Discussion in the context of [[topological K-theory]]:

* {#Hatcher} [[Allen Hatcher]], _Vector bundles and K-theory_ ([web](http://www.math.cornell.edu/~hatcher/VBKT/VBpage.html))
 
* {#Friedlander} [[Eric Friedlander]], _An introduction to K-theory_ ([pdf](http://users.ictp.it/~pub_off/lectures/lns023/Friedlander/Friedlander.pdf))
 
* {#Karoubi} [[Max Karoubi]], _K-Theory -- An introduction_, Grundlehren der mathematischen Wissenschaften 226, Springer 1978 ([pdf](https://webusers.imj-prg.fr/~max.karoubi/K.book/MK.book.pdf), [doi:10.1007%2F978-3-540-79890-3](https://link.springer.com/book/10.1007%2F978-3-540-79890-3))
 
* [[H. Blaine Lawson]], [[Marie-Louise Michelsohn]], _[[Spin geometry]]_, Princeton University Press (1989)

Discussion in the broader context of [[twisted equivariant topological K-theory]]:

* Noe Barcenas, Jesus Espinoza, [[Michael Joachim]], [[Bernardo Uribe]], _Universal twist in Equivariant K-theory for proper and discrete actions_, Proceedings of the London Mathematical Society, Volume 108, Issue 5 (2014) ([doi:10.1112/plms/pdt061](https://doi.org/10.1112/plms/pdt061), [arXiv:1202.1880](https://arxiv.org/abs/1202.1880))


On the [[H-space]] structure on $B U \times \mathbb{Z}$:

* [[Peter May]],  p. 205 (213 of 251) in: _[[A Concise Course in Algebraic Topology]]_.


[[!redirects stable unitary groups]]
