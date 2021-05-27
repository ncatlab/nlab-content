[[!redirects Poincare lemma]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
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

The **Poincar&#233; Lemma** in [[differential geometry]] and [[complex analytic geometry]] asserts that "every [[differential form]] $\omega$ which is closed, $d_{dR}\omega = 0$, is _locally_ exact, $\omega|_U = d_{dR}\kappa$."

In more detail: if $X$ is contractible then for every closed [[differential form]] $\omega \in \Omega^k_{cl}(X)$ with $k \geq 1$ there exists a differential form $\lambda \in \Omega^{k-1}(X)$ such that 

$$
  \omega = d_{dR} \lambda
  \,.
$$

Moreover, for $\omega$ a smooth family of closed forms, there is a smooth family of $\lambda$s satisfying this condition.

This statement has several more abstract incarnations. One is that it says that on a [[Cartesian space]] (or a complex [[polydisc]]) the [[de Rham cohomology]] (the [[holomorphic de Rham complex|holomorphic de Rham cohomology]]) vanishes in positive degree.

Still more abstractly this says that the canonical morphisms of [[sheaves of chain complexes]]

$$
  \mathbb{R} \to \Omega^\bullet_{dR}
$$

$$
  \mathbb{C} \to \Omega^\bullet_{hol}
$$

from the [[locally constant sheaf]] on the [[real numbers]] (the [[complex numbers]]) to the [[de Rham complex]] ([[holomorphic de Rham complex]]) is a [[stalk]]-wise [[quasi-isomorphism]] -- hence an [[equivalence]] in the [[derived category]] and hence induce an equivalence in [[hypercohomology|hyper]]-[[abelian sheaf cohomology]]. (The latter statement _fails_ in general in complex [[algebraic geometry]], see ([Illusie 12, 1.](#Illusie12)) and see also at _[[GAGA]]_.) (A variant of such [[resolutions]] of constant sheaves for the case over [[Klein geometries]] are [[BGG resolutions]].)

The Poincar&#233; lemma is a special case of the more general statement that the pullbacks of differential forms along [[homotopy|homotopic]] [[smooth function]] are related by a [[chain homotopy]].


## Statement
 {#Statement}

+-- {: .num_theorem}
###### Theorem

Let $f_1, f_2 : X \to Y$ be two [[smooth function]]s between [[smooth manifolds]] and $\Psi : [0,1] \times X \to Y$ a (smooth) [[homotopy]] between them.

Then there is a [[chain homotopy]] between the induced morphisms 

$$
  f_1^*, f_2^* : \Omega^\bullet(Y) \to \Omega^\bullet(X)
$$

on the [[de Rham complex]]es of $X$ and $Y$.

In particular, the action on [[de Rham cohomology]] of $f_1^*$ and $f_2^*$ coincide,

$$
  H_{dR}^\bullet(f_1^*) \simeq H_{dR}^\bullet(f_2^*)
  \,.
$$


Moreover, an explicit formula for the [[chain homotopy]] $\psi : f_1 \Rightarrow f_2$ is given by the "[[homotopy operator]]"

$$
  \psi 
   :
  \omega \mapsto (x \mapsto \int_{[0,1]} \iota_{\partial_t} (\Psi^*\omega)(x) ) d t
  \,. 
$$

=--

Here $\iota_{\partial t}$ denotes contraction (see [[Cartan calculus]]) with the canonical [[vector field]] tangent to $[0,1]$, and the [[integration]] is that of functions with values in the [[vector space]] of differential forms.

+-- {: .proof}
###### Proof

We compute

$$
  \begin{aligned}
    d_{Y} \psi(\omega)
    + 
    \psi( d_X \omega )
     & =
    \int_{[0,1]} d_Y \iota_{\partial_t} \Psi^*(\omega) d t 
    + 
    \int_{[0,1]} \iota_{\partial_t} \Psi^*(d_X \omega) d t
    \\
    & = \int_{[0,1]} (d_Y \iota_{\partial_t} + \iota_{\partial_t}d_Y) \Psi^* (\omega) d t
    \\
    & = \int_{[0,1]} \mathcal{L}_{t} \Psi^* (\omega) d t
    \\
    & = \int_{[0,1]} \partial_t \Psi^* (\omega) d t
    \\
    & = \int_{[0,1]} d_{[0,1]} \Psi^* (\omega) 
    \\
    & = \Psi_1^* \omega - \Psi_0^* \omega
    \\
    & = f_2^* \omega - f_1^* \omega
  \end{aligned}
  \,,
$$

where in the [[integral]] we used first that the [[exterior differential]] commutes with pullback of [[differential forms]], then [[Cartan's magic formula]] $d_Y \iota_{\partial_t} + \iota_{\partial_t}d_Y = \mathcal{L}_t$ for the [[Lie derivative]] along the [[cylinder]] on $X$ and finally the [[Stokes theorem]].

=--

The **Poincar&#233; lemma** proper is the special case of this statement for the case that $f_2 = const_y$ is a function constant on a point $y \in Y$:

+-- {: .num_prop}
###### Corollary

If a [[smooth manifold]] $X$ admits a smooth contraction 

$$
  \array{
    X
    \\
    \downarrow^{\mathrlap{(id,0)}} & \searrow^{\mathrlap{id}}
    \\
    X \times [0,1] & \stackrel{\Psi}{\to} & X
    \\
    \uparrow^{\mathrlap{(id,1)}} & \nearrow_{\mathrlap{const_x}}
    \\
    X
  }
$$

then the [[de Rham cohomology]] of $X$ is concentrated on the 
ground field in degree 0. Moreover, for $\omega$ any closed 
form on $X$ in positive degree an explicit formula for a form
$\lambda$ with $d \lambda = \omega$ is given by

$$
  \lambda = - \int_{[0,1]} \iota_{\partial_t}\Psi^*(\omega) d t
  \,.
$$

=--

+-- {: .proof}
###### Proof

In the general situation discussed above we now have $f_2^* = 0$
in positive degree.

=--

## Related concepts

* **Poincar&#233; lemma**

  * [[Kähler potential]]

* [[Stokes theorem]]

* [[de Rham theorem]]

* [[Hodge theorem]]

* [[variational sequence]]


## References

A nice account collecting all the necessary background (in [[differential geometry]]) is in

* Daniel Litt, _The Poincar&#233; lemma and de Rham cohomology_ ([pdf](http://math.stanford.edu/~dlitt/exposnotes/poincare_lemma.pdf))

Discussion in [[complex analytic geometry]] is in 

* {#Illusie12} [[Luc Illusie]], _Around the Poincar&#233; lemma, after Beilinson_, talk notes 2012 ([pdf](http://www.math.u-psud.fr/~illusie/derived-deRham3.pdf))

following

* {#Beilinson12} [[Alexander Beilinson]], _$p$-adic periods and de Rham cohomology_, J. of the AMS 25 (2012), 715-738

[[!redirects Poincaré lemma]]