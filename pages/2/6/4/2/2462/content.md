# Contents #

* automatics table of contents goes here
{:toc}

# Idea #

There are several different ways to think about differential systems:

* the [[category theory|general abstract way]] which we shall put forward here:
 
  an exterior differential system is a sub-[[Lie-∞-algebroid]] $\mathfrak{a} \hookrightarrow T X$ of
  the [[tangent Lie algebroid]] $T X$ of a [[manifold]] that is
  the [[kernel]] of a morphism $p : T X \to \mathfrak{j}$ 
  of [[Lie-∞-algebroid]]s:
  
  $$
    \mathfrak{a} := ker(p) \hookrightarrow T X \stackrel{p}{\to}
      \mathfrak{j}
  $$
  
* In the literature -- the the [references](#references)  below -- the term _exterior differential system_ is instead
  introduced and understood in the context of [[differential graded algebra|dg-algebra]]
  as a [[dg-ideal]] $J \subset \Omega^\bullet(X)$ inside the [[deRham dg-algebra]]
  of $X$ and all concepts there are developed from this perspective.
  
  From this the above perspective is obtained by noticing that from a dg-ideal $J$ 
  we are naturally led to form the quotient [[dg-algebra]] $\Omega^\bullet(X)/J$
  which is the [[cokernel]] of the inclusion $p^* : J \hookrightarrow \Omega^\bullet(X)$:

  $$
    J \stackrel{p^*}{\hookrightarrow} \Omega^\bullet(X) \to coker(p^*) = 
    \Omega^\bullet(X)/J
    \,.
  $$ 
  
  The existing literature on exterior differential systems 
  is actually a bit unclear about which [additional assumptions](#common further assumptions) on $J$ are supposed to be a crucial part of the definition. However, in most applications of interest -- see the [examples](#examples) below -- it turns out that $J$ is in fact a [[semifree dga]] (over $C^\infty(X)$).
  
  Here we take this as indication that
  
  * it makes good sense to understand exterior differential systems 
    in the restricted sense where the [[dg-ideal]] $J$ is required
    to be a [[semifree  dga]];
    
  * the reason that the existing literature does present the 
    desired extra assumptions on the [[dg-ideal]] $J$ in an
    incoherent fashion is due to a lack of global structural
    insight into the role of the definition of exterior differential
    systems.
  
  Because, recall that a [[Lie-∞-algebroid]] is -- effectively by definition -- the formal dual of a [[semifree dga|semifree]] 
  $\mathbb{N}$-graded commutative [[dg-algebra]]. So precisely
  with that extra condition on $J$ all [[dg-algebra]]s in the above
  may be understood as [[Chevalley-Eilenberg algebra]]s of
  [[Lie-∞-algebroid]]s and then the above [[cokernel]] sequence
  of [[dg-algebra]]s is precisely the formal dual of the 
  [[kernel]] sequence of [[Lie-∞-algebroid]]s.
  
* Historically, one can trace back the basic idea of 
  exterior differential systems to [[Eli Cartan]]'s work on
  [[partial differential equation]]s in terms of [[differential form]]s:
  
  for each system of partial differential equations
  
  $$
    \{
      F^\rho(\{x^\mu\}_{\mu}, \{f^j\}_j, \{\frac{\partial f^j}{\partial x^\mu}\} ) = 0
    \}_\rho
  $$
  
  there is a space $X$ and a [[dg-ideal]] $J \in \Omega^\bullet(X)$ such that solutions of the system of equations are given by **integral manifolds** of the exterior differential syetem determined by $J$.
  
The notion of an integral manifold of an exterior differential system
is crucial in the theory: in terms of $J$ it is a morphism 
$\phi : \Sigma \to X$ of [[manifold]]s such that the 
pullback of the ideal vanishes, $\phi^* J = 0$.

But this says precisely that $\phi$ extends to morphism of [[Lie-∞-algebroid]]s

$$
  \phi : T \Sigma \to \mathfrak{a}  
$$

with $CE(\mathfrak{a}) = \Omega^\bullet(X)/J$ as above. Therefore the relevance of the notion of _integral manifolds_ in the theory we take as another indication that 
exterior differental systems are usefully thought of as being about [[Lie-∞-algebroid]]s.

# Definition #

+-- {: .un_defn}
###### Definition (exterior differential system)

An **exterior differential system** on a smooth [[manifold]] $X$ 
is a [[dg-ideal]] $J \subset \Omega^\bullet(X)$ of the 
[[deRham dg-algebra]] $\Omega^\bullet(X)$ of $X$.

=--

Notice that $J$ being a [[dg-ideal]] means explicitly that

* $\forall \theta\in J \subset \Omega^\bullet(X), \omega \in \Omega^\bullet(X): 
  \theta \wedge \omega \in J$

* the $\mathbb{N}$-grading $J = \oplus_{k \in \mathbb{N}} J_k $ on 
  the [[dg-algebra]] $J$
  is induced from that of $\Omega^\bullet(X)$ in that $J_k = J \cap \Omega^\bullet(k)$

* $\forall \theta \in J \subset \Omega^\bullet(X) : d \theta \in J$

+-- {: .un_defn}
###### Definition 


An **integral manifold** of an exterior differential system is 
a submanifold $\phi : Y \hookrightarrow X$ such that the restriction of
all $\theta \in J$ to $Y$ vanishes: $\that|_Y = 0$. 

=--


In other words, for an integral manifold the pullback of the
ideal $J$ along the inclusion map $\phi$ vanishes: $\phi^* J = 0$.



## common further assumptions ##

Often further assumptions are imposed on exterior differential systems.
Here are some:

* An exterior differential system is called **finitely generated**
if there is a finite set $\{\theta_k \in \Omega^\bullet(X)\}$
of [[differential form]]s such that $J$ is the [[dg-ideal]]
generated by these, so that

  $$
    J = \{ \sum_i f_i \theta_i  + \sum_j g_j d \theta_j| f_i, g_j \in C^\infty(X)\}
    \,.
  $$

* Often it is assumed that $J_0 = \mathbb{R}$. 

  Dually in terms of [[Lie-∞-algebroid]]s  this assumption means that $J$ is the [[Chevalley-Eilenberg algebra]] of a [[Lie-∞-algebroid]] that is just an [[L-∞-algebra]].

* +-- {: .un_defn}
  ###### Definition (strict independence codition)

    A **strict independen condition** on an exterior differential system $J \subset \Omega^\bullet(X)$ is an $n$-form $\omega \in \Omega^n(X)$ for some $n$ such that 

    * $\omega$ is decomposable into a wedge product of $n$ 1-forms mod $J^n$

    * $\omega$ is poitwise not an element of $J$.

   For $(J, \omega)$ am exterior differential system with strict independence condition $\omega$, an **integral manifold** is now morre restrictively an integral manifold $\phi : \Sigma \to X$ for $J$ but now such that $\phi^* \omega$ is a volume form on $\Sigma$ (i.e. pointwise non-vanishing).

  =--


# special cases #

Some special types of exterior differential systems carry their
own names.


## Frobenius system ##

A **Forbenius system** is an exterior differential system
$J \subset \Omega^\bullet(X)$ that is locally generated as
a graded-commutative algebra from a set $\{\theta_j \in \Omega^1(U)\}_j $
of 1-forms.

Frobenius systems are in bijection with involutive subbundles of the
[[tangent bundle]] of $X$, i.e. subbundles $E \hookrightarrow T X$
such that for $v,w \in \Gamma(E) \subset \Gamma(T X)$ also the 
Lie bracket of vector fields of $v$ and $w$ lands in $E$:
$[v,w] \in \Gamma(E) \subset \Gamma(T X)$:

* given a Frobenius system the sections of $\Gamma(E)$ are defined
  locally to be the joint [[kernel]] of the maps $\{\theta_i : \Gamma(T U) \to \mathbb{R}\}$.
  
* given ab involutive subbundle $E$ the corresponding Frobenius
  system is the collection of 1-forms that vanishes on $E$:
  
  $J = \{\theta \in \Omega^1(X) | \theta|_{E} = 0\}$.
  
Notice that the involutive subbundle may be thought of precisely 
as a sub-[[Lie algebroid]]

$$
  \array{
     E &&\hookrightarrow&& T X
     \\
     & \searrow && \swarrow
     \\
     && X
  }
$$

of the [[tangent Lie algebroid]] (i.e. as a sub [[Lie-∞-algebroid]]
that happens to be an ordinary [[Lie algebroid]]). And indeed,
the [[Chevalley-Eilenberg algebra]] of $E$ is the quotient
$\Omega^\bullet(X)/J$ of the [[deRham dg-algebra]] by the Frobenius
system:

$$
  CE(E) = \Omega^\bullet(X)/J
  \,.
$$


### vertical tangent Lie algebroid ###

A special case of a [[Lie algebroid]] corresponding to a Frobenius system
is the [[vertical tangent Lie algebroid]] $T_{vert} Y$ of a map $\pi : Y \to X$.
This corresponds to the subbundle $ker(\pi_*) \subset T Y$ of vertical
vector fields on $Y$, with respecct to $\pi$. The corresponding
Frobenius system is that of **horizontal differential forms**

$$
  J = \Omega^\bullet_{hor}(Y) = \{\omega \in \Omega^1(Y)| \forall v \in ker(\pi_*): \omega(v) = 0\}
$$

and

$$
  CE(T_{vert} Y) = \Omega^\bullet(Y)/\Omega^\bullet_{hor}(Y)
$$

is the [[dg-algebra]] of **vertical differential forms** with respect to 
$Y$.

This plays a central role in the theory of [[Ehresmann connection]]s and
[[schreiber:Cartan-Ehresmann ∞-connection|Cartan-Ehresmann ∞-connection]].


## systems of partial differential equations ##

A system 

$$
  \{
    F^\rho : \mathbb{R}^n \times \mathbb{R}^s \times \mathbb{R}^{n \cdot s}
    \to 
    \mathbb{R}
  \}_\rho
$$ 

of [[partial differential equation]]s
in terms of variables $\{x^\mu\}_{\mu = 1}^n$ and functions 
$\{f^i\}_{i = 1}^s$
of the form

$$
  \{
    F^\rho((x^\mu), (f^i), \left(\frac{\partial f^i}{\partial x^\mu}\right))
    = 0
  \}
$$

is encoded by an exterior differential system on the 
0-locus 

$$
  X := \{(x,f,p) \in \mathbb{R}^n \times \mathbb{R}^s \times \mthbb{R}^{n s} |
    \forall \rho : F^\rho(x,f,p) = 0 \}
$$

of the $\{F^\rho\}_\rho$ (assuming that this is a manifold) with the
[[dg-ideal]] $J = \langle \theta_i \rangle_i$ generated by the 1-forms

$$
  \theta^i := d f^i - \sum_{\mu=1}^n p^i_\mu d x^\mu
  \,.
$$ 

Namely a solution to the system of partial differential equations is
precisely a [[section]] of the projection

$$
  X \to \mathbb{R}^n
$$

which defined an integral manifold of the exterior differential system.


# References #

A standard textbook is

* Bryant et al., _Exterior differential systems_ 
