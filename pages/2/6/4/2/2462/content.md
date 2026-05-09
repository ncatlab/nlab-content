

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

\tableofcontents


# Idea #

There are a couple of different ways to think about differential systems:

* the [[category theory|general abstract way]] which we shall put forward here:
 
  an exterior differential system is a sub-[[Lie-∞-algebroid]] $\mathfrak{a} \hookrightarrow T X$ of the [[tangent Lie algebroid]] $T X$ of a [[manifold]] that is the [[kernel]] of a [[morphism]] $p \colon T X \longrightarrow \mathfrak{j}$ of [[Lie-∞-algebroids|$L_\infty$-algebroids]]:
  
  $$
    \mathfrak{a} 
      \coloneqq 
    ker(p) 
      \hookrightarrow 
    T X 
      \overset{p}{\longrightarrow}
    \mathfrak{j}
    \mathrlap{\,,}
  $$
  
* In the literature (cf. the [references](#references) below) the term _exterior differential system_ is instead introduced and understood in the context of [[differential graded algebra|dg-algebra]] as a [[dg-ideal]] $J \subset \Omega^\bullet(X)$ inside the [[deRham dg-algebra]] of $X$ and all concepts there are developed from this perspective.
  
  From this the above perspective is obtained by noticing that from a dg-ideal $J$ we are naturally led to form the quotient [[dg-algebra]] $\Omega^\bullet(X)/J$ which is the [[cokernel]] of the inclusion $p^* \colon J \hookrightarrow \Omega^\bullet(X)$:

  $$
    J 
      \xhookrightarrow{\phantom{-}p^*\phantom{-}}
    \Omega^\bullet(X) 
      \longrightarrow 
    coker(p^*) 
      = 
    \Omega^\bullet(X)/J
    \,.
  $$ 
  
  The existing literature on exterior differential systems 
  is actually a bit unclear about which [additional assumptions](#commonfurtherassumptions) on $J$ are supposed to be a crucial part of the definition. However, in most applications of interest (cf. the [examples](#examples) below) it turns out that $J$ is in fact a [[semifree dga]] (over $C^\infty(X)$).
  
  Here we take this as indication that
  
  * it makes good sense to understand exterior differential systems  in the restricted sense where the [[dg-ideal]] $J$ is required to be a [[semifree  dga]];
    
  * the reason that the existing literature does present the  desired extra assumptions on the [[dg-ideal]] $J$ in an incoherent fashion is due to a lack of global structural insight into the role of the definition of exterior differential systems.
  
  Because, recall that a [[Lie-∞-algebroid|$L_\infty$-algebroid]] of [[finite type]] is -- effectively by definition -- the formal dual of a [[semifree dga|semifree]] $\mathbb{N}$-graded commutative [[dg-algebra]]. So precisely with that extra condition on $J$ all [[dg-algebras]] in the above may be understood as [[Chevalley-Eilenberg algebras]] of [[Lie-∞-algebroids]] and then the above [[cokernel]] sequence of [[dg-algebras]] is precisely the formal dual of the  [[kernel]] sequence of [[Lie-∞-algebroid|$L_\infty$-algebroids]].
  
* Historically, one can trace back the basic idea of  exterior differential systems to [[Élie Cartan]]'s work on [[partial differential equations]] in terms of [[differential forms]]:
  
  for each system of [[partial differential equations]]
  
  $$
    \left\{
      F^\rho
      \left(
        \{x^\mu\}_{\mu}, 
        \{f^j\}_j, 
        \left\{
          \frac{\partial f^j}{\partial x^\mu}
        \right\} 
      \right) 
        = 0
    \right\}_\rho
  $$
  
  there is a [[smooth manifold]] $X$ and a [[dg-ideal]] $J \in \Omega^\bullet(X)$ such that solutions of the system of equations are given by **integral manifolds** of the exterior differential system determined by $J$.
  
The notion of an integral manifold of an exterior differential system is crucial in the theory: in terms of $J$ it is a [[smooth map]] $\phi \colon \Sigma \to X$ of [[smooth manifolds]] such that the [[pullback of differential forms|pullback]] of the ideal vanishes, $\phi^* J = 0$.

But this says precisely that $\phi$ extends to morphism of [[Lie-∞-algebroids|$L_\infty$-algebroids]]:

$$
  \phi \colon T \Sigma \to \mathfrak{a}  
$$

with $CE(\mathfrak{a}) = \Omega^\bullet(X)/J$ as above. Therefore, the relevance of the notion of _integral manifolds_ in the theory we take as another indication that 
exterior differential systems are usefully thought of as being about [[Lie-∞-algebroids|$L_\infty$-algebroids]].

## Definition

+-- {: .num_defn}
###### Definition (exterior differential system)

An **exterior differential system** on a [[smooth manifold]] $X$ is a [[dg-ideal]] $J \subset \Omega^\bullet(X)$ of the 
[[deRham dg-algebra]] $\Omega^\bullet(X)$ of $X$.

=--

Notice that $J$ being a [[dg-ideal]] means explicitly that

* $\forall \theta\in J \subset \Omega^\bullet(X), \omega \in \Omega^\bullet(X)\colon \theta \wedge \omega \in J$

* the $\mathbb{N}$-grading $J = \oplus_{k \in \mathbb{N}} J_k $ on the [[dg-algebra]] $J$ is induced from that of $\Omega^\bullet(X)$ in that $J_k = J \cap \Omega^\bullet(k)$

* $\forall \theta \in J \subset \Omega^\bullet(X) : d \theta \in J$

+-- {: .num_defn}
###### Definition 

An **integral manifold** of an exterior differential system is 
a [[submanifold]] $\phi \colon Y \hookrightarrow X$ such that the [[pullback of differential forms|pullback]] of all $\theta \in J$ to $Y$ vanishes: $\that|_Y = 0$. 

=--


In other words, for an integral manifold the [[pullback of differential forms|pullback]] of the ideal $J$ along the inclusion map $\phi$ vanishes: $\phi^* J = 0$.



## Common further assumptions
  {#commonfurtherassumptions}

Often further assumptions are imposed on exterior differential systems. Here are some:

* An exterior differential system is called **finitely generated** if there is a finite set $\{\theta_k \in \Omega^\bullet(X)\}$ of [[differential form]]s such that $J$ is the [[dg-ideal]] generated by these, so that

  $$
    J 
      \;=\;
    \left\{ 
      \sum_i f_i \theta_i 
        + 
      \sum_j g_j d \theta_j 
      \big\vert 
      f_i, g_j \in C^\infty(X)
    \right\}
    \,.
  $$

* Often it is assumed that $J_0 = \mathbb{R}$. 

  Dually in terms of [[Lie-∞-algebroids|$L_\infty$-algebroids]],  this assumption means that $J$ is the [[Chevalley-Eilenberg algebra]] of an [[Lie-∞-algebroid|$L_\infty$-algebroid]] that happens to be just an [[L-∞-algebra|$L_\infty$-algebra]].

* +-- {: .num_defn}
  ###### Definition (strict independence condition)

  A **strict independence condition** on an exterior differential system $J \subset \Omega^\bullet(X)$ is an $n$-form $\omega \in \Omega^n(X)$ for some $n$ such that 

  * $\omega$ is decomposable into a wedge product of $n$ 1-forms mod $J^n$

  * $\omega$ is pointwise not an element of $J$.

  For $(J, \omega)$ am exterior differential system with strict independence condition $\omega$, an **integral manifold** is now more restrictively an integral manifold $\phi : \Sigma \to X$ for $J$ but now such that $\phi^* \omega$ is a volume form on $\Sigma$ (i.e. pointwise non-vanishing).

  =--


## Special cases 

Some special types of exterior differential systems carry their own names.


### Frobenius system ##

A **Frobenius system** is an exterior differential system $J \subset \Omega^\bullet(X)$ that is locally generated as a graded-commutative algebra from a set $\{\theta_j \in \Omega^1(U)\}_j $ of 1-forms.

Frobenius systems are in [[bijection]] with involutive subbundles of the [[tangent bundle]] of $X$, i.e. subbundles $E \hookrightarrow T X$ such that for $v,w \in \Gamma(E) \subset \Gamma(T X)$ also the [[Lie bracket]] of [[vector fields]] of $v$ and $w$ lands in $E$:
$[v,w] \in \Gamma(E) \subset \Gamma(T X)$:

* given a Frobenius system the sections of $\Gamma(E)$ are defined locally to be the joint [[kernel]] of the maps $\{\theta_i : \Gamma(T U) \to \mathbb{R}\}$.
  
* given ab involutive subbundle $E$ the corresponding Frobenius
  system is the collection of 1-forms that vanishes on $E$:
  
  $J = \big\{\theta \in \Omega^1(X) \big| \theta|_{E} = 0 \big\}$.
  
Notice that the involutive subbundle may be thought of precisely  as a sub-[[Lie algebroid]]

$$
  \array{
     E &&\hookrightarrow&& T X
     \\
     & \searrow && \swarrow
     \\
     && X
  }
$$

of the [[tangent Lie algebroid]] (i.e. as a sub [[Lie-∞-algebroid]] that happens to be an ordinary [[Lie algebroid]]). And indeed, the [[Chevalley-Eilenberg algebra]] of $E$ is the quotient $\Omega^\bullet(X)/J$ of the [[deRham dg-algebra]] by the Frobenius system:

$$
  CE(E) = \Omega^\bullet(X)/J
  \,.
$$


### Vertical tangent Lie algebroid ###

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


### Systems of partial differential equations

A system 

$$
  \big\{
    F^\rho 
      \colon 
    \mathbb{R}^n 
      \times 
    \mathbb{R}^s 
      \times 
    \mathbb{R}^{n \cdot s}
    \longrightarrow
    \mathbb{R}
  \}_\rho
$$ 

of [[partial differential equations]] in terms of [[variables]] $\{x^\mu\}_{\mu = 1}^n$ and functions $\{f^i\}_{i = 1}^s$ of the form

$$
  \left\{
    F^\rho\left(
     (x^\mu), 
     (f^i), 
     \left(
       \frac{\partial f^i}{\partial x^\mu}
     \right)
    \right)
    = 0
  \right\}
$$

is encoded by an exterior differential system on the 
0-locus 

$$
  X 
    \coloneqq 
  \big\{
    (x,f,p) 
      \in 
    \mathbb{R}^n \times \mathbb{R}^s \times \mathbb{R}^{n s} 
  \big|
    \forall \rho \colon F^\rho(x,f,p) = 0 
  \big\}
$$

of the $\{F^\rho\}_\rho$ (assuming that this is a manifold) with the [[dg-ideal]] $J = \langle \theta_i \rangle_i$ generated by the 1-forms

$$
  \theta^i 
    \coloneqq 
  \mathrm{d} f^i 
    - 
  \textstyle{\sum_{\mu=1}^n} p^i_\mu d x^\mu
  \,.
$$ 

Namely, a solution to the system of PDEs is precisely a [[section]] of the projection

$$
  X \to \mathbb{R}^n
$$

which defined an integral manifold of the exterior differential system.


## References 

The standard textbook:

* [[Robert L. Bryant]], [[Shiing-Shen Chern]], [[Robert B. Gardner]], [[Hubert L. Goldschmidt]], [[Phillip A. Griffiths]]: *Exterior Differential Systems*, Springer (1990) \[<a href="https://doi.org/10.1007/978-1-4613-9714-4">doi:10.1007/978-1-4613-9714-4</a>\]

Introductions and lecture notes:

* [[Robert L. Bryant]]: *Nine Lectures on Exterior Differential Systems* (1999) &lbrack;[pdf](https://sites.math.duke.edu/~bryant/Eilenberg/MSRI_Lectures.pdf)&rbrack;

* [[Robert L. Bryant]]: *Notes on exterior differential systems* &lbrack;[arXiv:1405.3116](https://arxiv.org/abs/1405.3116), alternative: [[EDS-notes.pdf:file]]&rbrack;

* [[Benjamin McKay]]: *Introduction to exterior differential systems*, Banach Center Publications **117** (2019) 45--55  &lbrack;[arXiv:1706.09697](https://arxiv.org/abs/1706.09697), [doi:10.4064/bc117-2](https://doi.org/10.4064/bc117-2)&rbrack;



[[!redirects exterior differential systems]]

