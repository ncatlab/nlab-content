
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents 
{:toc}

## Idea

$n$-plectic geometry is a generalization of [[symplectic geometry]] to [[higher category theory]].

It is closely related to [[multisymplectic geometry]] and [[n-symplectic manifold]]s.

## Definition


+-- {: .num_defn}
###### Definition

For $n \in \mathbb{N}$, an **[[n-plectic vector space]]**
is a [[vector space]] $V$ (over the [[real numbers]]) equipped with an $(n+1)$-linear skew function

$$
  \omega : \wedge^{n+1} V \to \mathbb{R}
$$

such that regarded as a function

$$
  V \to \wedge^n V^*
$$

is has trivial [[kernel]].

=--

Let $X$ be a [[smooth manifold]], $\omega \in \Omega^{n+1}(X)$ a [[differential form]].

+-- {: .num_defn}
###### Definition


We say $(X,\omega)$ is a **$n$-plectic manifold** if

* $\omega$ is closed: $d \omega = 0$;

* for all $x \in X$ 
  the map

  $$
    \hat \omega : T_x X \to \Lambda^n T_x^* X
  $$
  
  given by contraction of vectors with forms
  
  $$
    v \mapsto \iota_v \omega
  $$

  is [[injective]].  

=--

+-- {: .num_defn}
###### Definition


For $(X,\omega)$ a **$n$-plectic manifold** and $U\subset X$ a submanifold, we say $U$ is a $k$-isotropic, $k$-Lagrangian, and $k$-coisotropic submanifold is for every $p\in U$, the tangent space $T_p U\subset T_p X$ is a $k$-isotropic, $k$-Lagrangian, and $k$-coisotropic subspace, respectively (see [[n-plectic vector space]] for the definition). 

=--

+-- {: .num_defn}
###### Proposition


Given a diffeomorphism $f:X\to X$ for $(X,\omega)$ a **$n$-plectic manifold**, its [[graph of a function|graph]] $\Gamma(f)\subset X\times X$ is a $n$-Lagrangian submanifold of the $n$-plectic manifold $(X\times X, \pi_1 ^*\omega - \pi_2 ^* \omega)$ if and only if $f$ is an $n$-plectomorphism, meaning
$$
f^*(\omega) = \omega
$$

See e.g. Proposition 3.7 in [de León & Vilariño 2012](#deLeon12).

=--






See also the definition at _[[multisymplectic geometry]]_.

## Examples

* $n = 1$ -- this is the case of an ordinary [[symplectic manifold]] this appears in [[Hamiltonian mechanics]];

* $n = 2$, this appears naturally in 1+1 dimensional [[quantum field theory]].

1. For $X$ orientable, take $\omega$ the [[volume form]]. This is $(dim(X)-1)$-plectic.

1. $\wedge^n T^* X \to X$

1. $G$ a [[compact space|compact]] [[simple group|simple]] [[Lie group]],

   let $\nu : (x,y,z) \mapsto \langle x, [y,z]\rangle$ be the canonical 
   [[Lie algebra cohomology|Lie algebra 3-cocycle]] 
   and extend it left-invariantly
   to a 3-form $\omega_\nu$ on $G$.  Then $(G,\omega_\nu)$ is 2-plectic.
   









## Poisson $L_\infty$-algebras   
 {#PoissonLInfinityAlgebras}
   
To an ordinary [[symplectic manifold]] is associated its [[Poisson algebra]]. Underlying this is a [[Lie algebra]], whose Lie bracket is the _Poisson bracket_.

We discuss here how to an $n$-plectic manifold for $n \gt 1$ there is correspondingly assoociated not a Lie algebra, but a [[Lie n-algebra]]: the **[[Poisson bracket Lie n-algebra]]**. It is natural to call this a **Poisson Lie $n$-algebra** (see for instance at _[[Poisson Lie 2-algebra]]_). 

(Not to be confused with the Lie algebra of a [[Poisson Lie group]], which is a Lie group that itself is equipped with a compatible [[Poisson manifold]] structure. It is a bit unfortunate that there is no better established term for the Lie algebra underlying a Poisson algebra apart from "Poisson bracket".)

Consider the ordinary case in $n=1$ for how a [[Poisson algebra]] is obtained from a [[symplectic manifold]] $(X, \omega)$.

Here

$$
  \hat \omega : T_x X \to T^*_x X
$$
   
is an [[isomorphism]].
   
Given $f \in C^\infty(X)$, $\exists ! \nu_f \in \Gamma(T X)$ such that  $d f = - \omega(v_f, -)$
   
Define $\{f,g\} := \omega(v_f, v_g)$. Then $(C^\infty(X,), \{-,-\})$ is a [[Poisson algebra]].


We can generalize this to $n$-plectic geometry.

Let $(X,\omega)$ be $n$-plectic for $n \gt 1$.

Observe that then $\hat \omega : T_x X \to \wedge^n T_x X$ is no longer an [[isomorphism]] in general.

**Definition**

Say

$$
  \alpha \in \Omega^{n-1}(X)
$$

is **Hamiltonian** precisely if 

$$
  \exists v_\alpha \in \Gamma(T X) 
$$

such that 

$$
  d \alpha = - \omega(v_\alpha, -)
  \,.
$$

This makes $v_\alpha$ uniquely defined.

Denote the collection of [[Hamiltonian forms]] by $\Omega^{n-1}_{Hamilt}(X)$.


















Define a bracket

$$
  \{-,-\} : \Omega^{n-1}_{Hamilt}(X)^{\otimes_2} \to \Omega^{n-1}_{Hamilt}(X)
$$

by

$$
  \{\alpha, \beta\} = - \omega(v_\alpha, v_\beta, -, \cdots, -)
  \,.
$$

This satisfies

1. k 

   $$
    d \{\alpha, \beta\} = - \omega([v_\alpha, v_\beta], -, \cdots, -)
    \,.
   $$

1. $\{-,-\}$ is skew-symmetric;

1. $\{\alpha_1, \{\alpha_2, \alpha_3\}\}$ + cyclic permutations  
   $d \omega(v_{\alpha_1}, v_{\alpha_2}, v_{\alpha_3}, -, \cdots)$.
   
So the Jacobi dientity fails up to an exact term. This will yield the structure of an [[L-infinity algebra]].


**Proposition**

Given an $n$-plectic manifold $(X,\omega)$ we get a [[Lie n-algebra]] structure on the complex

$$
  C^\infty(X) \stackrel{d_{dR}}{\to} \Omega^1(X) \stackrel{d_{dR}}{\to}
  \to \cdots \to 
  \Omega^{n-1}_{Hamilt}(X)
$$

(where the rightmost term is taken to be in degree 0).

where

* the unary bracket is $d_{dR}$;

* the $k$-ary bracket is 

  $$
    [\alpha_1, \cdots, \alpha_k]
    = 
    \left\{
      \array{
        \pm \omega(v_{\alpha_1}, \cdots, v_{\alpha_k}) & if \forall i : \alpha_i \in \Omega^{n-1}_{Hamilt}(X)
        \\
        0 & otherwise
      }
    \right.
  $$

This is the **[[Poisson bracket Lie n-algebra]]**.

This appears as ([Rogers 11, theorem 3.14](#Rogers11)).


For $n = 1$ this recovers the definition of the [[Lie algebra]] underlying a [[Poisson algebra]].

## Prequantization

### Review of the symplectic situation

Recall for $n=1$ the mechanism of [[geometric quantization]] of a [[symplectic manifold]].

Given a 2-form $\omega$ and the corresponding complex [[line bundle]] $P$, consider the [[Atiyah Lie algebroid]] sequence

$$
  ad P \to T P/U(1) \to T X
$$

The smooth [[section]]s of  $T P/U(1) \to X$ are the $U(1)$ invariant [[vector field]]s on the total space of $P$.

Using a [[connection on a bundle|connection]] $\nabla$ on $P$ we may write such a section as

$$
  s(v) + f \partial_t
$$ 

for $v \in \Gamma(T X)$ a vector field downstairs, $s(v)$ a horizontal lift with respect to the given connection and $f \in C^\infty(X)$.

Locally on a suitable patch $U \subset X$ we have that $s(V)|_U = v|_U + \iota_v \theta_i|_U$ .

We say that $\tilde v = s(v) + f \partial_t$ **preserves the splitting** iff $\forall u \in \Gamma(X)$ we have

$$
  [\tilde v, s(u)] = s([v,u])
  \,.
$$


One finds that this is the case precisely if

$$
  d f = - \iota_v \omega
  \,.
$$

This gives a [[homomorphism]] of [[Lie algebra]]s 

$$
  C^\infty(X) \to \Gamma(T P / U(1))
$$

$$
  f \mapsto s(v_f) + f \partial_t
  \,.
$$

### 2-plectic geometry and Courant algebroids

We consder now [[geometric quantization|prequantization]] of [[2-plectic manifolds]].

Let $(X,\omega)$ be a 2-plectic manifold such that the [[de Rham cohomology]] class $[\omega]/2 \pi i$ is in the image of [[integral cohomology]] (Has integral periods.)

We can form a cocycle in [[Deligne cohomology]] from this, encoding a [[bundle gerbe]] with connection.

On a [[cover]] $\{U_i \to X\}$ of $X$ this is given in terms of [[Cech cohomology]] by data

* $(g_{i j k} : U_{i j k} \to U(1)) \in C^\infty(U_{i j k}, U(1))$

* $A_{i j} \in \Omega^1(U_{i j})$;

* $B_i \in \Omega^2(U_i)$

satisfying a cocycle condition.

Now recall that an exact [[Courant algebroid]] is given by the following data:

* a [[vector bundle]] $E \to X$;

* an _anchor_ morphism $\rho : E \to T X$ to the [[tangent bundle]];

* an _inner product_ $\langle -,-\rangle$ on the fibers of $E$;

* a bracket $[-,-]$ on the sections of $E$.

Satisfying some conditions.

The fact that the [[Courant algebroid]] is _exact_ means that


$$
  0 \to T^* X \to E \to T X \to 0
$$

is an [[exact sequence]].

The **standard Courant algebroid** is the example where 

* $E = T X \oplus T^* X$;

* $\langle v_1 + \alpha_1, v_2 + \alpha_2\rangle = \alpha_2(v_1) + \alpha_1(v_2)$;

* the bracket is the skew-symmetrization of  the Dorfman bracket

  $$
    (v_1 + \alpha_1, v_2 + \alpha_2) = [v_1, v_2] - \mathbb{L}_{v_1}\alpha_2 
    - (d \alpha_1)(v_2,-)
  $$


Now with respect to the above Deligne cocycle, build a Courant algebroid as follows:

* on each patch $U_i$ is is the standard Courant algebroid 
  $E_i := T U_i \oplus T^* U_i$;

* glued together on double intersections using the $d A_{i j}$

This gives an exact Courant algebroid $E \to X$ as well as a splitting $s : T X \to E$ given by the $\{B_i\}$.

The bracket on this $E$ is given by the skew-symmetrization of

$$
  [ [ s(v_1)  \alpha_1, s(v_2) + \alpha_2 ] ] = s([v_1, v_2])
  + 
  \mathcal{L}_{v_1} \alpha_2 - (d \alpha_2)(v_2, -) -   
  \omega(v_1, v_2, \cdots)
  \,.
$$

Here a section $e = s(v) + ... $ preserves the splitting precisely if

for all $u \in \Gamma(T X)$ we have

$$
  [ [ e, s(u)] ]_D = s([v,u]) 
$$

exactly if $\alpha$ is Hamiltonian and $v = v_\alpha$.

**Theorem**

Recall that to every [[Courant algebroid]] $E$ is associated a [[Lie 2-algebra]] $L_\infty(E)$.

Then: we have an embedding of [[L-infinity algebra]]s

$$
  \phi : L_\infty(X,\omega) \to L_\infty(E)
$$

given by $\phi(\alpha) = s(v_\alpha) + \alpha$.

## Related entries

* [[geometry of physics -- prequantum geometry]]

## Properties

### Central extensions under geometric quantization

[[!include geometric quantization extensions - table]]


## Related concepts

* [[2-plectic geometry]]

* [[symplectic infinity-groupoid]]

* [[higher geometric quantization]]

[[!include Isbell duality - table]]

[[!include infinity-CS theory for binary non-degenerate invariant polynomial - table]]

## References
 {#References}

### General
 {#ReferencesGeneral}

The observation that the would-be Poisson bracket induced by a higher degree closed form extends to the [[Poisson bracket Lie n-algebra]] is due to

* {#Rogers10} [[Chris Rogers]], _$L_\infty$ algebras from multisymplectic geometry_ , Letters in Mathematical Physics  **100** 1 (2012) 29-50  &lbrack;[arXiv:1005.2230](http://arxiv.org/abs/1005.2230), [journal](http://link.springer.com/article/10.1007%2Fs11005-011-0493-x)&rbrack;

* {#Rogers11} [[Chris Rogers]], _Higher symplectic geometry_ PhD thesis (2011) ([arXiv:1106.4068](http://arxiv.org/abs/1106.4068))
 
with first discussion of application to [[prequantization]] in

* [[Chris Rogers]], _2-plectic geometry, Courant algebroids, and categorified prequantization_ ,  [arXiv:1009.2975](http://arxiv.org/abs/1009.2975).

* [[Chris Rogers]], _Higher geometric quantization_, talk at _Higher Structures 2011_ in G&#246;ttingen ([pdf slides](http://www.crcg.de/wiki/Higher_geometric_quantization))

Discussion in the more general context of [[higher differential geometry]]/[[extended prequantum field theory]] is in 

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]],

  _[[schreiber:Higher geometric prequantum theory]]_, 

  _[[schreiber:L-∞ algebras of local observables from higher prequantum bundles]]_

See also

* {#deLeon12} M. de León, S. Vilariño. *Lagrangian submanifolds in k-symplectic settings* (2012). ([arXiv:1202.3964](https://arxiv.org/abs/1202.3964)).


See also the references at [[multisymplectic geometry]] and [[n-symplectic manifold]].

A [[higher differential geometry]]-generalization of [[contact geometry]] in line with [[multisymplectic geometry]]/$n$-plectic geometry is discussed in 

* Luca Vitagliano, _L-infinity Algebras From Multicontact Geometry_ ([arXiv.1311.2751](http://arxiv.org/abs/1311.2751))


### Applications

Some more references on application, on top of those mentioned in the articles [above](#ReferencesGeneral).

A survey of some (potential) applications of 2-plectic geometry in [[string theory]] and [[M2-brane]] models is in section 2 of

* [[Christian Saemann]], [[Richard Szabo]], _Groupoid quantization of loop spaces_ ([arXiv:1203.5921](http://arxiv.org/abs/1203.5921))

and in 

* [[Christian Saemann]], [[Richard Szabo]], _Quantization of 2-Plectic Manifolds_ ([arXiv:1106.1890](http://arxiv.org/abs/1106.1890))

### Examples

On $n$-plectic formulation of [[gravity]], [[Maxwell theory]] and [[Einstein-Maxwell theory]]:

* [[Petr Hořava]], _On a covariant Hamilton-Jacobi framework for the Einstein-Maxwell theory_ Classical and Quantum Gravity **8** 11 (1991) 2069 &lbrack;[doi:10.1088/0264-9381/8/11/016](https://iopscience.iop.org/article/10.1088/0264-9381/8/11/016)&rbrack;

* [[Dmitri Vey]], _$n$-Plectic Maxwell Theory_ &lbrack;[arxiv:1303.2192](https://arxiv.org/abs/1303.2192)&rbrack;

* [[Dmitri Vey]], *Multisymplectic formulation of vielbein gravity. De Donder-Weyl formulation, Hamiltonian $(n-1)$-forms*,  Classical and Quantum Gravity **32** 9 (2015) &lbrack;[arxiv:1404.3546](https://arxiv.org/abs/1404.3546), [doi:10.1088/0264-9381/32/9/095005](https://iopscience.iop.org/article/10.1088/0264-9381/32/9/095005)&lbrack;

* Patrick Cabau, Fernand Pelletier. *Partial Nambu-Poisson structures on a convenient manifold* (2024). ([arXiv:2404.08688](https://arxiv.org/abs/2404.08688)).

For [[teleparallel gravity]]

* [[Igor V. Kanatchikov]]. *The De Donder-Weyl Hamiltonian formulation of TEGR and its quantization* (2023) &lbrack;[arXiv:2308.10052](https://arxiv.org/abs/2308.10052)&rbrack;

[[!redirects n-plectic manifold]]
[[!redirects n-plectic manifolds]]

[[!redirects Hamiltonian 1-form]]
[[!redirects Hamiltonian 1-forms]]
[[!redirects Hamiltonian n-form]]
[[!redirects Hamiltonian n-forms]]

[[!redirects n-plectic structure]]
[[!redirects n-plectic structures]]

[[!redirects 3-plectic geometry]]

[[!redirects pre-n-plectic manifold]]
[[!redirects pre-n-plectic manifolds]]