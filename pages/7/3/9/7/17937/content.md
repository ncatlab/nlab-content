
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A fundamental theorem of [[topology]]: for $n_1, n_2 \in \mathbb{N}$ two different natural numbers, $n_1 \neq n_2$, then the [[Cartesian spaces]] $\mathbb{R}^{n_1}$ and $\mathbb{R}^{n_2}$ of [[dimension]] $n_1$ and $n_2$, respectively, are _not_ [[homeomorphism|homeomorphic]] (while for $n_1 = n_2$ then of course they are). Hence [[dimension]] of [[topological manifolds]] is a _topological [[invariant]]_.

This seems intuitively obvious, but the [[formal proof]] (due to [[Brouwer]] around 1910) is comparatively hard, and the problem was an important open problem in the 19th century. To appreciate that the problem is harder than it may superficially seem it serves to notice that for every $n \in \mathbb{N}$ there are [[surjective]] [[continuous maps]] $\mathbb{R}^1 \to \mathbb{R}^n$ (the [[Peano curves]]), in addition to the obvious [[injective]] continuous maps $\mathbb{R}^1 \to \mathbb{R}^n$ for $n \geq 1$ (or indeed $\mathbb{R}^m \to \mathbb{R}^n$ for $m \leq n$), because of which there are also [[bijective]] (but discontinuous) maps $\mathbb{R}^m \to \mathbb{R}^n$ for $m, n \geq 1$ (by the [[Schroeder–Bernstein theorem]]).


## Statement
 {#Statement}

+-- {: .num_theorem #InvarianceOfDimension}
###### Theorem
**(topological invariance of dimension)**

For $n_1, n_2 \in \mathbb{N}$ then the [[Euclidean space]] $\mathbb{R}^{n_1}$ and $\mathbb{R}^{n_2}$ (regarded as [[topological spaces]] with their [[metric topology]]) are [[homeomorphism|homeomorphic]] if and only if $n_1 = n_2$.


=--

More generally:

+-- {: .num_theorem #InvarianceOfDomain}
###### Theorem
**(Brouwer invariance of domain theorem)**

For $U \subset \mathbb{R}^n$ an [[open subset]] of a [[Cartesian space]], for any $n \in \mathbb{N}$, and for $f \colon U \to \mathbb{R}^n$ a [[continuous map|continuous]] [[injective map]], then its [[image]] $f(U)$ is also an [[open subset]].

In other words, continuous injections between Cartesian spaces of the same [[dimension]] are [[open maps]].  

=--

This implies theorem \ref{InvarianceOfDimension}:

+-- {: .num_lemma #LemmaForTheCorollary}
###### Lemma

For $n_1, n_2 \in \mathbb{N}$, there is a [[continuous map|continuous]] [[injection]] from $\mathbb{R}^{n_1}$ to $\mathbb{R}^{n_2}$ if and only if $n_1 \leq n_2$.

=--

+-- {: .proof}
###### Proof

If $n_1 \leq n_2$, use $\iota_{n_1,n_2}\colon (x_1, \ldots, x_{n_1}) \mapsto (x_1, \ldots, x_{n_1}, \vec{0})$, where $\vec{0}$ consists of $n_2 - n_1$ copies of $0$.  If $n_1 \gt n_2$, then supposing a continuous injection $f\colon \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$, compose $f$ with $\iota_{n_2,n_1}$ to get a map from $\mathbb{R}^{n_1}$ to itself, also a continuous injection.  By invariance of domain (theorem \ref{InvarianceOfDomain}), the [[image]] of this map is open in $\mathbb{R}^{n_1}$, yet contained in the range of $\iota_{n_2,n_1}$, and the only open subset of that range is [[empty subset|empty]], a contradiction since $\mathbb{R}^{n_1}$ is not empty.
=--


+-- {: .proof}
###### Proof
of theorem \ref{InvarianceOfDimension} from theorem \ref{InvarianceOfDomain}

A homeomorphism is a continuous injection both ways, so $n_1 \leq n_2$ and $n_2 \leq n_1$ by lemma \ref{LemmaForTheCorollary}.

=--

This only-if half of this argument immediately generalizes to any [[inhabited subset|inhabited]] open subsets of $\mathbb{R}^{n_1}$ and $\mathbb{R}^{n_2}$.


## Proofs
 {#Proofs}

We discuss various [[proofs]] of the topological invariance of dimension (theorem \ref{InvarianceOfDimension}).

### Via ordinary cohomology

+-- {: .proof}
###### Proof
of theorem \ref{InvarianceOfDimension}

Consider [[relative cohomology|relative]] [[ordinary cohomology]] $H_\bullet$ 
with [[coefficients]] in, says, the [[integers]] $\mathbb{Z}$. Recall that for $A \hookrightarrow X$ an inclusion of [[CW-complexes]], then there is a [[long exact sequence]] of the form

$$
  \cdots 
   \to H^{n-1}(X) \longrightarrow H^{n-1}(A) \longrightarrow H^n(X,A) \longrightarrow H^n(X) \to \cdots
$$

Applied to the point inclusion $\{0\} \hookrightarrow \mathbb{R}^n$ and using that

1. $H^k(\mathbb{R}^n) = \left\{  \array{ \mathbb{Z} & \vert\, \text{if}\, k = 0 \\ 0 & \vert\, \text{otherwise}} \right.$ 

   because $\mathbb{R}^n$ is [[homotopy equivalence|homotopy equivalent]] to the point;

1. $H^k(\mathbb{R}^n \backslash \{0\}) = \left\{ \array{ \mathbb{Z} &\vert\, \text{if} \, k \in \{0,n-1\}  \\ 0 & |\, \text{otherwise} } \right.$

   because $\mathbb{R}^n \backslash \{0\}$ is [[homotopy equivalence|homotopy equvaent]] to th [[n-sphere|(n-1)-sphere]] $S^{n-1}$

this gives for $n \geq 2$ that $H^k(\mathbb{R}^n , \mathbb{R}^n - \{0\}) = \left\{ \array{ \mathbb{Z} &\vert\, \text{if} \, k \in \{0,n\} \\ 0 & \vert\, \text{otherwise}  }\right.$

Hence $\mathbb{R}^{n_1}$ and $\mathbb{R}^{n_2}$ do not have the same [[relative cohomology]] unless $n_1 = n_2$. Since  every [[homeomorphism]] induces an isomorphism on (relative) cohomology, they cannot be homeomorphic (using [[excluded middle]] here).


=--

### Via K-Theory


A proof also follows from the properties of the [[Adams operations]] on [[topological K-theory]], see for instance ([Wirthmuller 12, p. 46](#Wirthmuller12)).


## Related concepts

* [[Tietze extension theorem]]

* [[Brouwer's fixed point theorem]]


## References

The first proof is due to [[Brouwer]] around 1910.

* [[Terry Tao]], _[Brouwer's fixed point and invariance of domain theorems, and Hilbert's fifth problem](https://terrytao.wordpress.com/2011/06/13/brouwers-fixed-point-and-invariance-of-domain-theorems-and-hilberts-fifth-problem/)_

* Wikipedia, _[Invariance of domain](https://en.wikipedia.org/wiki/Invariance_of_domain)_

A proof also follows from the properties of the [[Adams operations]] on [[topological K-theory]], see for instance

* {#Wirthmuller12} [[Klaus Wirthmüller]], p. 46 of _Vector bundles and K-theory_, 2012 ([pdf](ftp://www.mathematik.uni-kl.de/pub/scripts/wirthm/Top/vbkt_skript.pdf))



[[!redirects invariance of dimension]]
[[!redirects invariance of domain]]
