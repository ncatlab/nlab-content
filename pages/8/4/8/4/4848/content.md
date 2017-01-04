
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Poincar&#233; Lie algebra_ $\mathfrak{iso}(\mathbb{R}^{d-1,1})$ is the [[Lie algebra]] of the [[isometry group]] of [[Minkowski spacetime]]: the [[Poincaré group]]. This happens to be the [[semidirect product]] of the [[special orthogonal Lie algebra]] $\mathfrak{so}(d-1,1)$ with the the abelian translation Lie algebra $\mathbb{R}^{d-1,1}$. 


## Definition

+-- {: .num_defn}
###### Definition

For $d \in \mathbb{N}$, write $\mathbb{R}^{d-1,1}$ for [[Minkowski spacetime]], regarded as the [[inner product space]] whose underlying [[vector space]] is $\mathbb{R}^d$ and equipped with the [[bilinear form]] given in the canonical [[linear basis]] of $\mathbb{R}^d$ by 

$$
  \eta \coloneqq diag(-1,+1,+1, \cdots, +1)
  \,.
$$

The [[Poincaré group]] $Iso(\mathbb{R}^{d-1,1})$ is the [[isometry group]] of this inner product space. The _Poincar&#233; Lie algebra_ $\mathfrak{iso}(\mathbb{R}^{d-1,1})$ is the [[Lie algebra]] of this [[Lie group]] (its [[Lie differentiation]])

$$
  \mathfrak{iso}(\mathbb{R}^{d-1,1})
  \coloneqq
  Lie(Iso(\mathbb{R}^{d-1,1}))
  \,.
$$
 
=--

+-- {: .num_remark}
###### Remark

The [[Poincaré group]] is the [[semidirect product group]]

$$
  Iso(\mathbb{R}^{d-1,1})
    \simeq
  \mathbb{R}^{d-1,1} \rtimes O(d-1,1)
$$

of the [[Lorentz group]] $O(d-1,1)$ (the group of [[linear map|linear]] [[isometries]] of [[Minkowski spacetime]]) with the $\mathbb{R}^d$ regarded as the [[translation group]] along itself, via the defining [[action]].

Accordingly, the Poincar&#233; Lie algebra is the [[semidirect product Lie algebra]]

$$
  \mathfrak{iso}(\mathbb{R}^{d-1,1})
  \simeq
  \mathbb{R}^{d-1,1}
    \rtimes
  \mathfrak{so}^+(d-1,1)
$$

of the abelian Lie algebra on $\mathbb{R}^d$ with the (orthochronous) [[special orthogonal Lie algebra]] $\mathfrak{so}(d-1,1)$.

=--

+-- {: .num_prop}
###### Proposition

For $\{P_a\}$ the canonical [[linear basis]] of $\mathbb{R}^d$, and for $\{L_{a b} = - L_{b a}\}$ the corresponding canonical basis of $\mathfrak{so}(d-1,1)$, then the [[Lie bracket]] in $\mathfrak{iso}(\mathbb{R}^{d-1,1})$ is given as follows:

$$
  \begin{aligned}
    [P_a, P_b] & = 0
    \\
    [L_{a b}, L_{c d}] 
     & = 
      \eta_{d a} L_{b c}
      -\eta_{b c} L_{a d}
      +\eta_{a c} L_{b d}
      -\eta_{d b} L_{a c}
     \\
    [L_{a b}, P_c] & = \eta_{a c} P_b -\eta_{bc} P_a
  \end{aligned}
$$

=--

+-- {: .proof}
###### Proof

Since [[Lie differentiation]] sees only the [[connected component]] of a [[Lie group]], and does not distinguish betwee a Lie group and any of its discrete [[covering spaces]], we may equivalently consider the Lie algebra of the [[spin group]] $Spin(d-1,1) \to SO^+(d-1,1)$ (the double cover of the [[proper orthochronous Lorentz group]]) and its [[action]] on $\mathbb{R}^{d-1,1}$.

By the discussion at _[[spin group]]_, the Lie algebra of $Spin(d-1,1)$ is the Lie algebra spanned by the [[Clifford algebra]] [[bivectors]] 

$$
  L_{a b} \leftrightarrow \Gamma_a \Gamma_b
$$

and its [[action]] on itself as well as on the vectors, identified with single Clifford generators

$$
  P_a \leftrightarrow \Gamma_a
$$

is given by forming [[commutators]] in the [[Clifford algebra]]:

$$
  [L_{a b}, P_c]
    \leftrightarrow
  \tfrac{1}{2}[\Gamma_{a b}, \Gamma_c  ]
$$


$$
  [L_{a b}, L_{c d}]
  \leftrightarrow
  \tfrac{1}{2}[\Gamma_{a b}, \Gamma_{c d}  ]
  \,.
$$

Via the Clifford relation

$$
  \Gamma_a \Gamma_b + \Gamma_b \Gamma_a = -2 \eta_{a b}
$$

this yields the claim.

=--

+-- {: .num_remark}
###### Remark

Dually, the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{iso}(\mathbb{R}^{d-1})$ is generated from $\mathbb{R}^{d,1}$ and $\wedge^2 \mathbb{R}^{d,1}$. For $\{t_a\}$ the standard basis of $\mathbb{R}^{d-1,1}$ we write $\{\omega^{a b}\}$ and $\{e^a\}$ for these generators. With $(\eta_{a b})$ the components of the [[Minkowski metric]] we write

$$
  \omega^{a}{}_b \coloneqq \omega^{a c}\eta_{c b}
  \,.
$$

In terms of this the CE-differential that defines the Lie algebra structure is

$$
  d_{CE} \colon \omega^{a b} = \omega^a{}_c \wedge \omega^{c b}
$$

$$
  d_{CE} \colon e^a \mapsto \omega^{a}{}_b  \wedge t^b
$$

=--

## Properties

### Cohomology

We discuss some elements in the [[Lie algebra cohomology]] of $\mathfrak{iso}(d-1,1)$.

The canonical degree-3 $\mathfrak{so}(d-1,1)$-cocycle is

$$
  \omega^a{}_b \wedge \omega^b{}_c \wedge \omega^c{}_a
  \in 
  CE(\mathfrak{iso}(d-1,1))
  \,.
$$

The _volume cocycle_ is the [[volume form]]

$$
  vol = \epsilon_{a_1 \cdots a_{d}} e^{a_1} \wedge \cdots \wedge e^{a_d} \in CE(\mathfrak{iso}(d-1,1))
  \,.
$$
{#VolumeCocycle}

### Invariant polynomials and Chern-Simons elements

With the basis elements $(e^a, \omega^{a b})$ as above, denote the shifted generators of the [[Weil algebra]] $W(\mathfrak{iso}(d-1,1))$ by $\theta^a$ and $r^{a b}$, respectively.

We have the [[Bianchi identity]]

$$
  d_W : r^{a b} 
   \mapsto
   \omega^{a c} \wedge R_c{}^d
   - 
   R^{a c} \wedge \omega_c{}^b
$$

and

$$
  d_W : \theta^a 
   \mapsto
    \omega^a{}_b \theta^b
    - 
    R^{a}{}_b e^b
   \,.
$$


The element $\eta_{a b} \theta^a \wedge \theta^b \in W(\mathfrak{iso}(d-1,1))$ is an [[invariant polynomial]]. A [[Chern-Simons element]] for it is $cs = \eta_{a b} e^a \wedge \theta^b$. So this transgresses to the trivial cocycle.

Another invariant polynomial is $r^{a b} \wedge r_{a b}$. This is the [[Killing form]] of $\mathfrak{so}(d-1,1)$. Accordingly, it transgresses to a multiple of $\omega^a{}_b \wedge \omega^b{}_c \wedge \omega^c{}_a$.

This is the first in an infinite series of Pontryagin invariant polynomials

$$
  P_n 
  :=
  r^{a_1}{}_{a_2} \wedge r^{a_2}{}_{a_3}
  \wedge \cdots \wedge r^{a_n}{}_{a_1}
  \,.
$$

There is also an infinite series of mixed invariant polynomials

$$
  C_{2n + 2}
  :=
  \theta_{a_1} \wedge r^{a_1}{}_{a_2} \wedge r^{a_2}{}_{a_3}
  \wedge \cdots \wedge r^{a_{n-1}}{}_{a_n} \wedge \theta^{a_n}
  \,.
$$

[[Chern-Simons element]]s for these are

$$
  B_{2n + 1}
  :=
  \theta_{a_1} \wedge r^{a_1}{}_{a_2} \wedge r^{a_2}{}_{a_3}
  \wedge \cdots \wedge r^{a_{n-1}}{}_{a_n} \wedge e^{a_n}
  \,.
$$



### Lie algebra valued forms

A [[Lie algebra-valued form]] with values in $\mathfrak{iso}(d-1,1)$

$$
  \Omega^\bullet(X) \leftarrow W(\mathfrak{iso}(d-1,1)) : (E,\Omega)
$$

is

* a [[vielbein]] $E$ on $X$;

* a "[[spin connection]]" $\Omega$ on $X$.

The [[curvature]] 2-form $(T, R)$ consists of

* the [[torsion of a metric connection|torsion]] $T = d E + [\Omega \wedge E]$;

* the [[Riemannian curvature]] $R = d \Omega + [\Omega \wedge \Omega]$.

If the torsion vanishes, then $\Omega$ is a [[Levi-Civita connection]] for the [[metric]] $E^a \otimes E^b \eta_{a b}$ defined by $E$.

The [[volume form]] is the image of the [volume cocycle](#VolumeCocycle) 

$$
  \Omega^\bullet(X)
  \stackrel{(E,\Omega)}{\leftarrow}
  W(\mathfrak{iso}(d-1,1))
  \stackrel{vol}{\leftarrow}
  W(b^{d-1} \mathbb{R})
  :
  vol(E)
  \,.
$$

We have

$$
  vol(E) = \epsilon_{a_1 \cdots a_d} E^{a_1} \wedge \cdots \wedge E^{a_d}
  \,.
$$

If the torsion vanishes, this is indeed a closed form.

## Related structures

* [[special orthogonal Lie algebra]]

* [[super Poincaré Lie algebra]]


[[!redirects Poincaré Lie algebras]]

[[!redirects Poincare Lie algebra]]
[[!redirects Poincaré Lie algebra]]
