
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A **rational topological space** is a [[topological space]] 
all whose (reduced) [[integral cohomology|integral homology]] groups are [[vector spaces]] over the [[rational numbers]] $\mathbb{Q}$. 

Every [[simply connected topological space|simply connected]] [[topological space]] has a [[rationalization]]
and passing to that rationalization amounts to forgetting all
[[torsion subgroup|torsion]] in the [[homology groups|homology]]- and [[homotopy group|homotopy]]-groups of that space. 

Thereby  rational spaces serve as  approximations to the [[homotopy type]] of general [[topological spaces]] in [[rational homotopy theory]].

The idea is that comparatively little information
(though sometimes crucial information) is lost by passing to 
rationalizations, while there are powerful tools to handle and compute with rational spaces. 

In particular, there is a precise sense in which
the [[homotopy types]] of ([[nilpotent space|nilpotent]], [[finite type]]) rational spaces are modeled simply by  [[differential graded cochain algebras]]: This is the [[fundamental theorem of dg-algebraic rational homotopy theory]].


## Definition

A [[topological space]] is called _rational_ if 

1. it is [[simply connected topological space|simply connected]] in that the 1st [[homotopy group]] vanishes, $\pi_1 X = 0$  (more generally we may use [[nilpotent topological spaces]] here)

1. and the following equivalent conditions are satisfied

   1. the collection of [[homotopy group]]s form a $\mathbb{Q}$-[[vector space]],

   1. the [[reduced cohomology|reduced homology]] of $X$, $\tilde H_*(X,\mathbb{Z})$ is a $\mathbb{Q}$-[[vector space]],

   1. the [[reduced cohomology|reduced homology]] of the [[loop space]] $\Omega X$ of $X$, $\tilde H_*(\Omega X,\mathbb{Z})$ is a $\mathbb{Q}$-[[vector space]].


A morphism $\ell : X \to Y$ of simply connected [[topological space]] is
called a **[[rationalization]]** of $X$ if $Y$ is a rational topological space and if $\ell$ induces an [[isomorphism]] in rational homology

$$
  H_*(\ell,\mathbb{Q}) : H_*(X,\mathbb{Q}) \stackrel{\simeq}{\to} H_*(Y,\mathbb{Q})
  \,.
$$

Equivlently, $\ell$ is a rationalization of $X$ if it induces an [[isomorphism]] 
on the rationalized [[homotopy group]]s, i.e. when the morphism

$$
  \pi_* \ell \otimes \mathbb{Q} : \pi_* X \otimes \mathbb{Q}
   \to \pi_* Y \otimes \mathbb{Q} \simeq \pi_* Y
$$

is an [[isomorphism]].

A continuous map $\phi : X \to Y$ between simply connected space is a 
**rational homotopy equivalence** if the following equivalent conditions are satisfied:

1. it induces an isomorphism on rationalized homotopy groups in that 
   $\pi_*(\phi) \otimes \mathbb{Q}$ is an isomorphism;
   
1. it induces an isomorphism on rationalized homology groups in that 
   $H_*(\phi,\mathbb{Q})$ is an isomorohism;

1. it induces an isomorphism on rationalized [[cohomology group]]s in that 
   $H^*(\phi,\mathbb{Q})$ is an isomorphism;

1. it induces a weak [[homotopy equivalence]] on rationalizations $X_0, Y_0$ in that
   $\phi_0 : X_0 \to Y_0$ is a [[weak homotopy equivalence]].

## Properties

One of the central theorems of [[rational homotopy theory]] says:

+-- {: .un_theorem }
###### Theorem

Rational homotopy types of simply connected spaces $X$ are in bijective corespondence with minimal [[Sullivan model]]s $(\wedge^\bullet V,d)$

$$
  (\wedge^\bullet V , d) \stackrel{\simeq}{\to}
  \Omega^\bullet_{Sullivan}(X)
  \,.
$$

And homotopy classes of morphisms on both sides are in bijection.

=--

+-- {: .proof}
###### Proof

This appears for instance as corollary 1.26 in 

* [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv](http://arxiv.org/abs/math.AT/0604626))


=--



## Examples 

### Rational $n$-sphere 

The **[[rational n-sphere]]** $(S^n)_0$ can be written as

$$
  (S^n)_0  :=
  \left(
     \vee_{k\geq 1} S^n_k
  \right) 
  \cup
  \left(
    \coprod_{k \geq 2} D^{n+1}_k
  \right)
  \,,
$$

where...

For $n = 2 k +1$ odd, a [[Sullivan model]] for the $n$-sphere is the very simple [[dg-algebra]] with a single generator $c$ in degree $n$ and vanishing differential, i.e. the morphism

$$
  (\wedge^\bullet \langle c\rangle, d = 0)
  \to 
  \Omega^\bullet_{Sullivan}(S^{2k + 1})
$$

that picks any representative of the degree $n$-cohomology of $S^{n}$ is a [[quasi-isomorphism]].

For $n = 2k$ with $k \geq 1$ there is a second generator $c_{4k+1}$ with differential


$$
  d c_{2k} = 0
$$
$$
  d c_{4k-1} = c_{2k} \wedge c_{2k}
 \,.
$$

### Rational $n$-disk 

The rational $n$-disk is computed as the [[cone]] of the rational sphere:

$$
  D^{n+1}_{\mathbb{Q}} = C(S^n_{\mathbb{Q}}) = (S^n_{\mathbb{Q}}\times I)/(S^n_{\mathbb{Q}}\times\{0\}).
$$

Since the cochain complex of the $n$-disk consists of two generators $b$ and $c$ of degree $n$ and $(n+1)$, respectively, such that $\mathrm{d} b = c$, the [[cdga]] corresponding to the rational $n$-disk consists of linear combinations of $b^k$ and $c b^k$ when $n$ is even, with differentials:

$$
  \mathrm{d}(b^k) 
    \;=\;
  k \cdot c b^{k-1}
$$
$$
  \mathrm{d} (c b^k) 
  \;=\; 
  0
  \,,
$$

and of linear combinations of $c^k b$ and $c^k$ when $n$ is odd, with differentials
$$
  \mathrm{d}(c^k b)=c^{k+1}
$$
$$
  d(c^k)=0
  \,.
$$


### Rational compact Lie-groups

For $G$ a [[compact space|compact]] [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$, let $\{\mu_{k_i}\}_{i=1}^{rank G}$ be generators of its [[Lie algebra cohomology]] with $deg \mu_{k_i} = 2 k_i-1$. Accordingly there are generators $\{P_{k_i}\}_i$ of [[invariant polynomial]]s on $\mathfrak{g}$. 

Such $G$ is rationally equivalent to the product

$$
  \prod_{i = 1}^{rank G} S^{2 k_i -1}
$$

of rational $n$-spheres. 

Moreover, Lie groups are [[formal homotopy type]]s, whose [[Sullivan model]] has a [[quasi-isomorphism]] to its [[cochain cohomology]].

### Rational classifying spaces of compact Lie groups {#RationalClassifyingSpace}

With $G$ as above, let $\mathcal{B}G$ be the corresponding [[classifying space]].  Then

$$
  H^\bullet(\mathcal{B}G, \mathbb{Q}) \simeq \mathbb{Q}[P_{k_1},  P_{k_2}, \cdots]
  \,,
$$

where $P_{k_i}$ is an [[invariant polynomial]] generator in degre $2 k_i$.

Indeed, also these classifying spaces are [[formal homotopy type]]s and hence a [[Sullivan model]] for $\mathcal{B}G$ is given by $(H^\bullet(\mathcal{B}G,\mathbb{R}), d=0)$.


### Quotient spaces

We may think of $\mathcal{B}G$ as the [[action groupoid]] $*// G$. The above discussion generalizes to more general such quotients.

...


### Biquotient spaces

Let $H$ be a [[compact Lie group]] and $G \subset H \times H$ a [[closed subspace|closed]] [[subgroup]] of the [[direct product group]]. This $G$ acts on $H$ by left and right multiplication

$$
  (g_1, g_2) : h \mapsto g_1 h g_2^{-1}
  \,.
$$

The corresponding [[quotient space]] is also called a _[[biquotient]]_.

...

See 

* Vitali Kapovitch, _A note on rational homotopy of biquotients_ ([pdf](http://www.math.utoronto.ca/vtk/biquotient.pdf))


## Related concepts

* [[rational topological G-space]]



[[!redirects rational topological spaces]]

[[!redirects rational space]]
[[!redirects rational spaces]]
[[!redirects rational topological space]]