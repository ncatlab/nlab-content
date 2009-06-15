Here are notes by [[Urs Schreiber]] for Wednesday, June 10, from [[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology|Oberwolfach]].


## Alexander Kahle: superconnections and index theory ##


* 1) superconnections 

* 2) index theory

* 3) sketch some proofs

### 1) superconnections ###

**definition** A **superconnection** $\nabla_s$ on a
$\mathbb{Z}_2$-graded vector bundle $V \to M$ is an odd derivation
on $\Omega^\bullet(M,V)$

superconnections form an affine space modeled on $\Omega^\bullet(M, End(V))^{odd}$

$$
  End(V)
$$


$$
  \nabla_s = \omega_0 + \nabla + \omega_2 + \omega_3
$$

class in $K$-theory given by a map $V \stackrel{f}{\to} W$

unitary superconnection on $\mathbb{Z}_2$-graded unitary bundles $V$
with map as a above look like

$$
  \nabla_s
  =
  \left(
    \array{
      & f^*
      \\
      f & 
    }
  \right)
  + \nabla
$$

**Chern character** by the usual formulas

$$
  ch(\nabla_s) := sTr e^{\nabla^2}
$$



### 2) index theory ###


**definition** Let $M$ be smooth Riemannian and $Spin$,
The Dirac operator associated to $(V \to M, \nabla_s)$
is defined by

* - $$ D(\nabla_s) : \Gamma(S \otimes V) 
  \stackrel{\nabla_s \otimes 1 \oplus 1 \otimes \nabla_s}{\to} \Omega^\bullet(M, S \otimes V) 
  \stackrel{c(.)}{\to} \Gamma(S \otimes V)
  $$


This is

* an elliptic operator;

* formally self adjoint

* of the form $$ D(\nabla_s) = \left(
    \array{
       & D'(\nabla_s)
       \\
       D'(\nabla_s)
    }
  \right)
  $$
  
* **theorem** (corollary of Atiyah-singer index theory)
  $$
    index(D(\nabla_s))
    =
    index(D(\nabla))
    =
    \int_M \hat A(\Omega^m) ch(\nabla_s)
  $$




so superconnections don't give new topological data: they are geometric objects
with the same underlyying topology as ordinary connections but refined "geometry"


recall that Atiyah-Singer says that

$$
  Tr \exp(-t D(\nabla_s)^2 ) = index(D(\nabla_s))
$$

the heat semi-group is smoothing, therefore it is represented by 
a kernel

$$
  \exp(-t D(\nabla_s)^2) \psi(x)
  =
  \int_M p_t(x,y) \psi(y) d y
$$

$$
  Tr \exp(-t  D(\nabla_s)^2) =
  \int_M Tr p_t(x,x) d vol
$$

the following expected formula which holds for ordinary
connections (due to Ezra Getzler) 
_no longer_ holds directly for superconnections

$$
  \lim_{t \to 0}
  Tr p_t(x,x) d vol
  \neq
  (2 \pi i)^{-n/2}
  [
    \hat A(\Omega^m) ch(\nabla_s)
  ]_n
$$

here $n = dim X$ is the dimension of the manifold


problem is that components in a superconnections scale in a different 

to make it true, we need to rescale

$$
  \nabla_s^t := |t|^{-1/2} \omega_0 + \nabla + |t|^{1/2} \omega_2 + \cdots
$$


A Riemannian map is a triple $(\pi, g, P)$

$
  \pi : M  \to B
$

a family with fibers close Spin manifolds,
$
  g^{M/B} 
$
a metric onm the fibers,
$$
  p : T(M) \to T(M/B)
$$

$$
  \array{
    V, \nabla_s
    \\
    \downarrow
    \\
    M
    \\
    \downarrow^\pi
    \\
    B
  }
$$


  $\pi_* (V)$ : a fibre at $y \in B$ is
  
  $\Gamma_y(S^{M/B} \otimes V)$

due to Bismut we get from a connection on the top a superconnecction
on the bottom (which is one of the main original motivations to be interested
in superconnection in the first place), 
which we tweak here a bit to get a superconnection on $B$
from a superconnection on $V$

$$
  \pi_! \nabla_s = \pi_! \nabla + \pi_! \omega
$$

with $\nabla_s = \nabla + \omega$

$$
  [\pi_! \omega_!]_{\omega}(\xi_1, \cdots, \xi_i)
  =
  c^{M/B}(2 (\tilde \xi_1), 2(\tilde \xi_2) \cdots 2(\tilde \xi_k))
$$

$$
  \pi^r = (\pi, r g^{M/B}, P)
$$

$$
  \lim_{t \to 0}
  ch(\pi_!^t \nabla_s)
  =
  (2 \pi i)^{dim M/B}
  \pi_*
  [
    \hat A(\Omega^{M/B} ch(\nabla_s))
  ]
$$

the scalings are related by

$$
  \pi_!^t(\nabla_s) = [\pi_! \nabla_s^{1/t}]^t
$$





### determinant line bundles ###


(...skipping a bunch of remarks...)




### 3) sketch of some proofs###

(no time, as expected)




### $\infty$-operads ###

Baronikov-Kontsevich passage





## Gabriel Drummond-Cole; $\infty$-operads, $BV_\infty$ and $HyperComm_\infty$ ##

>(was hard to take typed notes of this otherwise pretty cool talk, does anyone have handwriitten notes?)




## Scott Wilson: Categorical algebra, mapping spaces and applications ##


(for closely related blog entry see

* [Higher Hochschild Cohomology and Differential Forms on Mapping Spaces](http://golem.ph.utexas.edu/category/2008/04/higher_hochschild_cohomology_a.html)


)

outline

* language for some elementary algebraic topology

* application to generalizatons of Hochschild complexes

* Examples

  * invariants on mapping spaces
  
  * contributions related to def of Laplacian


**def/lema**

A commutative associative 
[[differential graded algebra]] is (equivalently given by) a 
strict monoidal functor

$$
  (FinSet, \coprod) \to (ChainComplexes, \otimes)
$$

generalize this

**def** a **partial DGA** is a  monoidal functor
with coherence map given by weak equivalence in the 
model structure

$$
 A :  (FinSet, \coprod) \to (ChainComplexes, \otimes)  
$$

i.e. there exists a natural weak equivalence

$$
  A(j \sqcup k) \stackrel{T}{\to} A(j) \otimes A(k)
$$

that respects the obvious coherence properties


generalized

* 1) co-algebras

* 2) any operad

* 3) note that $FinSet_*$ (pointed finite sets) is a module over $FinSet$, so generalize
  to modules, comodules, etc.
  
Then weak partial algebras can be functorially replaced by $E_\infty$-algebras

**example**

$X$ be a space $j \stackrel{f}{\to} k$

$$
  X^j = Map(j,X) \leftarrow Map(k,X) = X^k
$$

pass to the chains version of this

$$
  Ch_*(X^j) \leftarrow Ch_*(X^k)
$$

$$
  Ch^*(X^j) \to Ch^*(X^k)
$$

by Kuenneth formula we have a chain equivalence

$$
  C_*(X^j) \otimes C_*(X^k) \to C_*(X^{j+k})
$$

and similarly for cochains.

so this gives two things: 

* a partial coalgebra on $C_*(X)$

* a partial algebra on $C^*(X)$



Let $Y$ be any finite simplicial space. A partial algebra

$$
  \Delta \stackrel{\gama}{\to} FinSet \stackrel{A}{\to} ChainCompl
$$

simplicial object in $ChainCompl$, so total complex

$$
  CH^\gamma(A)
$$

meaning generalization of Hochschild complex

* this is joint work with Tradler and Zanelli (spelling? probably wrong)

goes back to Pitashvili and more recently Gregory Ginot

For $A = \Omega(X)$, then $CH^\gamma(A)$ computes cohomology of 
$X^\gamma $, if $X$ is sufficiently connected

**example**

let $A$ be a strict algebra, and $\gamma = Y = S^1$ then

$$
  CH^{S^1}(A) = \prod_{n \geq 0} A \otimes A^{\otimes n}
$$

is the Hochschild complex

there is also a shuffle product  in the game, so this implies there is an 
exponential map

calculate:

$$
  \exp(| \otimes x)
  =
  | + | \otimes x + | \otimes  x \otimes x + | \otimes  x \otimes x \otimes x + \cdots + 
$$

$$
  D \exp(1 \otimes x) = (1 \otimes d x + x \cdot x) \cdot e^{1 \otimes x}
$$

then: if $d x + x \cdot x = 0$ then $D e^{1 \otimes x} = 0$

this reminds us of curvature and connection

this can be taken further



let $A = \Omega^\bullet(M)$ be differential forms on $M$

$$
  \array{
    && CH^{S^1}(A) (\simeq \Omega(M^{S^1}))
    \\
    &\nearrow & \downarrow
    \\
    K(M)&\stackrel{ch}{\to}&\Omega(M)
  }
$$

commutes (due to some people)

**example 2**

$Y = I$ (the interval)

then $CH^I(A)$ is the 2-sided bar construction

more generally $CH(A, M, N) = \prod_{n \geq 0} M \otimes A^{\otimes n} \otimes N$

with $M$ and $N$ $A$-modules sitting on the end of the interval

consider the case $A = \Omega^\bullet(Riemannian manifold)$
and $M = A$ and $N = (\Omega^\bullet(...), d^* , (x\in A) \cdot (y\in N) = \star^{-1}(x \wedge \star y)))$

(the operatoin on $N$ here is the intersection product of forms)

Let $D$ be differential on $CH^I$

let $D$ be differential on $CH^I$ for normal structure, and 
and $D^*$ for $A, M, N$ as just described.

Set 

$$
  \Delta = [D, D^*]
$$


then acting with this $\Delta$ on something produces interesting non-linear
differential equations related to Witten't Morse-theory deformation 
of susy quantum mechanics and to Navier-Stokes' equations in fluid dynamics...

***

[[Oberwolfach Workshop, June 2009 -- Tuesday, June 9|Previous day]] --- [[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology|Main workshop page]] --- [[Oberwolfach Workshop, June 2009 -- Thursday, June 11|Next day]]