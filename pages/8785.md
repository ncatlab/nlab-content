
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
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

## Idea

The _Dolbeault complex_ is the analog of the [[de Rham complex]] in [[complex geometry]].


## Definition

### Dolbeault complex

On a [[complex manifold]] $X$ the [[de Rham complex]] $\Omega^\bullet(X)$ refines to a [[bigraded object|bigraded]] complex $\Omega^{\bullet, \bullet}(X)$, where a [[differential form]] of bidegree $(p,q)$ has holomorphic degree $p$ and antiholomorphic degree $q$, hence is given on a local [[coordinate chart]] by an expression of the form

$$
  \omega = \sum f_{I J} d z_{i_1} \wedge \cdots \wedge d z_{i_p} \wedge d \bar z_{j_1} \wedge \cdots \wedge d \bar z_{j_q}
 \,.
$$

Moreover, the [[de Rham differential]] $\mathbf{d}$ decomposes as

$$
  \mathbf{d} = \partial + \bar \partial
  \,,
$$

where $\partial \colon \Omega^{\bullet, \bullet}\to \Omega^{\bullet + 1, \bullet}$ and $\bar \partial \colon \Omega^{\bullet, \bullet}\to \Omega^{\bullet, \bullet + 1}$.

The _Dolbeault complex_ of $X$ is the [[chain complex]] $(\Omega^{\bullet, \bullet}(X), \bar \partial)$. The _[[Dolbeault cohomology]]_ of $X$ is the [[cochain cohomology]] of this complex.

### Holomorphic differential forms

Here $\Omega^{p,0}(X)$ defines a [[holomorphic vector bundle]] and a [[holomorphic section]] is a differential form with local expression as above, such that the coefficient functions $f_{I J}$ are [[holomorphic functions]]. This is called a _holomorphic differential form_.

For $p \lt dim_{\mathbb{C}}(X)$ equivalently this is a differential form in the [[kernel]] of the antiholomorphic Dolbeault operator $\bar \partial$.

## Properties

### Dolbeault theorem
 {#DolbeaultTheorem}

The complex analog of the [[de Rham theorem]] is the [[Dolbeault theorem]]:

for $X$ a [[complex manifold]] then its [[Dolbeault cohomology]] in bi-degree $(p,q)$ is [[natural isomorphism|naturally isomorphic]] to the [[abelian sheaf cohomology]] in degree $q$ of the [[abelian sheaf]] $\Omega^p \coloneqq \Omega^{p,0}$ of [[holomorphic p-forms]]

$$
  H^{p,q}(X)\simeq H^q(X,\Omega^p)
  \,.
$$

(...)

Let $Disk_{compl}$ be the [[category]] of complex [[polydiscs]] in $\mathbb{C}^n$ and [[holomorphic functions]] between them.

For $p \in \mathbb{N}$ write $\Omega^p \colon Disk_{complex}^{op} \to Set$ for the [[sheaf]] of holomorphic [[differential n-form|differential p-forms]].


+-- {: .num_prop}
###### Proposition

For $X$ a [[complex manifold]], let $\{U_i \to X\}$ be a holomorphic good open cover. Then the [[Cech cohomology]] of this cover with [[coefficients]] in $\Omega^p$ in degree $q$ is the [[Dolbeault cohomology]] in bidegree $(p,q)$

$$
  H^{p,q}(X) \simeq \pi_0 sPSh(Disk_{comp})(C(\{U_i\}, \Omega^p[q]))
  \,.
$$

=--

For instance ([Maddock, theorem 1.0.1](#Maddock)).

### On Stein manifolds

+-- {: .num_prop}
###### Proposition
**([[Cartan theorem B]])**

For $X$ a [[Stein manifold]],

$$
  H^k(\Omega^{p,\bullet}(X), \bar \partial)
  =
  \left\{
    \array{  
      0 & k \neq 0 
      \\
      \Omega^p_{hol}(X) & k = 0
    }
  \right.
  \,.
$$

=--

For instance ([Gunning-Rossi](#GunningRossi)).

+-- {: .num_prop}
###### Proposition

For $X$ a [[Stein manifold]] of complex [[dimension]] $n$, the [[compactly supported cohomology|compactly supported]] Dolbeault [[cohomology]] is

$$
  H^k(\Omega_c^{p, \bullet}(X), \bar \partial)
  = 
  \left\{
    \array{
      0 , & k \neq n
      \\
      (\Omega_{hol}^{n-p}(X))^\ast
    }
  \right.
  \,,
$$

where on the right $(-)^\ast$ denotes the continuous linear dual.

=--

First noticed in ([Serre](#Serre)).

### Todd genus

By the [[Hirzebruch-Riemann-Roch theorem]] the [[index]] of the Dolbeault operator is the [[Todd genus]].

### Relation to $Spin^c$-structures

A [[complex manifold]], being in particular an [[almost complex manifold]], carries a canonical [[spin^c structure]]. The corresponding [[Spin^c Dirac operator]] identifies with the Dolbeault operator under the identification of the [[spinor bundle]] with that of [[holomorphic differential forms]]

$$
  S(X) \simeq \wedge^{0,\bullet} T^\ast X
  \,.
$$

## Related concepts

* [[Dolbeault cohomology]]

* [[Dolbeault-Dirac operator]]

* [[chiral Dolbeault complex]]

* [[holomorphic de Rham complex]]

## References

* {#Voisin02} [[Claire Voisin]], section 2.3 of _[[Hodge theory and Complex algebraic geometry]] I,II_, Cambridge Stud. in Adv. Math. __76, 77__, 2002/3

* {#Maddock} Zachary Maddock, _Dolbeault cohomology_ ([pdf](http://www.math.columbia.edu/~maddockz/notes/dolbeault.pdf))
 

* {#GunningRossi} Robert C. Gunning and Hugo Rossi, _Analytic functions of several complex variables_, Prentice-Hall Inc., Englewood Cliffs, N.J., (1965)
 

* {#Serre} [[Jean-Pierre Serre]], _Quelques probl&#232;mes globaux relatifs aux vari&#233;t&#233;s de Stein_, Colloque sur les fonctions de plusieurs variables, tenu &#224; Bruxelles, 1953, Georges Thone, Li&#232;ge, 1953, pp. 57&#8211;68. MR 0064155 (16,235b)
 

A [[formal geometry]] version:

* Shilin Yu, _Dolbeault dga of a formal neighborhood_, [arxiv/1206.5155](http://arxiv.org/abs/1206.5155); _The Dolbeault dga of the formal neighborhood of a diagonal_, [arxiv/1211.1567](http://arxiv.org/abs/1211.1567)

[[!redirects Dolbeault cohomology]]

[[!redirects holomorphic smooth function]]
[[!redirects holomorphic function]]
[[!redirects holomorphic smooth functions]]
[[!redirects holomorphic functions]]

[[!redirects holomorphic differential 1-form]]
[[!redirects holomorphic 1-form]]
[[!redirects holomorphic differential form]]

[[!redirects holomorphic differential 1-forms]]
[[!redirects holomorphic 1-forms]]
[[!redirects holomorphic differential forms]]

[[!redirects holomorphic form]]
[[!redirects holomorphic forms]]

[[!redirects holomorphic differential p-form]]
[[!redirects holomorphic differential p-forms]]
[[!redirects holomorphic p-form]]
[[!redirects holomorphic p-forms]]


[[!redirects Dolbeault differential]]
[[!redirects Dolbeault differentials]]

[[!redirects Dolbeault operator]]
[[!redirects Dolbeault operators]]