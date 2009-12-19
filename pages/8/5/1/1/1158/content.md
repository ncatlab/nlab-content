#Idea#

The standard _Deligne complex_ (of [[abelian sheaf cohomology|abelian sheaves]]) is under the [[Dold-Kan correspondence]] the sheaf of
[[n-groupoid]]s of smooth [[n-functor]]s from the [[path n-groupoid]] to the $n$-fold [[delooping]] $\mathbf{B}^n U(1)$:

$$
  \mathbb{Z}(n+1)_D^\infty
  \simeq
  \bar \mathbf{B}^n U(1)
  \stackrel{N}{\to^\simeq}
  [P_n(-), \mathbf{B}^n U(1)]
  \,.
$$


Smooth Deligne cohomology in degree $n$, 
of a [[smooth space]] $X$ is [[cohomology]] with
coefficients in $\bar \mathbf{B}^n U(1)$.


$$
  Deligne cohomology = H(X, \bar \mathbf{B}^n U(1)) 
  \,.
$$

Here the notation on the right is as at the end of [[motivation for sheaves, cohomology and higher stacks]].

This is a realization of the 
[[differential cohomology|differential refinement]] (or smooth extension) $\bar H^n(X,\mathbb{Z})$ of the 
[[integral cohomology]] $H^n(X, \mathbb{Z})$ of $X$ in terms of
[[abelian sheaf cohomology]].

[[differential cohomology|Recall]] 
that analgous to how $H^n(X,\mathbb{Z})$ classifies line $(n-1)$-bundles 
and equivalently line $(n-2)$-gerbes on $X$, $\bar H^n(X, \mathbb{Z})$
classifies line $(n-2)$-gerbes with connection.

Accordingly, the _Deligne complex_ of sheaves $\mathbb{Z}(n)^\infty_D$
is a complex of sheaves of differential forms.

#Definition#

+-- {: .un_defn}
###### Definition

For $k \in \mathbb{N}$
write $\Omega^k(-) : U \mapsto \Omega^k(U)$ for the [[sheaf] of smooth differential $k$-forms on $X$
and $C^\infty(-,V)$ for the sheaf of smooth $V$-valued functions on  $X$. 

The degree $(n+1)$ **Deligne complex** is the complex of sheaves

$$
  \mathbb{Z}(n+1)_D^\infty
  \;
    :=
  \;
  \left(
  \cdots \to 0 \to C^\infty(-,\mathbb{Z}) \hookrightarrow
   C^\infty(-,\mathbb{R}) \stackrel{d }{\to}
    \Omega^1(-) \stackrel{d}{\to} \cdots \stackrel{d}{\to}
    \Omega^n(-)
  \right)
  \,.
$$

=--


Often it is useful to consider the [[quasi-isomorphism|quasi-isomorphic]] complex

$$
  \bar \mathbf{B}^n U(1)
  \;\;
  :=
  \;\;
  \left(
  \cdots 0 \to   C^\infty(-,U(1)) \stackrel{d log}{\to}
    \Omega^1(-) \stackrel{d}{\to} \cdots \stackrel{d}{\to}
    \Omega^n(-)
  \right)
$$

Here $C^\infty(-,U(1)) \stackrel{d log}{\to} \Omega^1(-)$ 
is the 
morphism of sheaves induced by regarding a $U(1) \simeq \mathbb{R}/\mathbb{Z}$-valued function locally
as a $\mathbb{R}$-valued function and applying the deRham differential $d$ to that.

The obvious morphism of complexes

$$
  \array{
    C^\infty(-,\mathbb{Z})    
    &\hookrightarrow&
    C^\infty(-,\mathbb{R}) 
      &\stackrel{d log}{\to}&
     \Omega^1(-) 
     &\stackrel{d}{\to}& 
       \cdots 
     &\stackrel{d}{\to}&
     \Omega^n(-)
    \\
    \downarrow
    &&
    \downarrow^{(-)/\mathbb{Z}}
    &&
    \downarrow^{Id}
    &&
    &&
    \downarrow^{Id}
    \\
    0 
    &\to&
    C^\infty(-,U(1)) 
      &\stackrel{d log}{\to}&
     \Omega^1(-) 
     &\stackrel{d}{\to}& 
       \cdots 
     &\stackrel{d}{\to}&
     \Omega^n(-)
  }
$$

clearly induces isomorphism on [[homology]] groups: the homology in degree $n$ is locally constant $\mathbb{R}$-valued functions modulo locally constant $\mathbb{Z}$-valued functions in the first case and constant $U(1)$-valued functions in the second case, which is the same.

+-- {: .un_defn}
###### Definition

**Deligne cohomology** in degree $n+1$ of $X$ is the 
[[cohomology]] (which is [[abelian sheaf cohomology]] in this case) with coefficients in $\bar \mathbf{B}^n U(1)$.

=--

$$
  H(X, \mathbb{Z}(n+1)_D^\infty)
  \simeq 
  H(X, \bar \mathbf{B}^n U(1))
  \,.
$$

Here the notation on the right is motivated from the discussion at the end of [[motivation for sheaves, cohomology and higher stacks]].


# Characteristic classes of Deligne cocycles #

There are two natural morphisms of abelian [[cohomology group]]s out of Deligne cohomology:

* the map to the underlying non-differential cocycle, the class of the underlying [[principal infinity-bundle]]:

 $$
  cl
  :
  H(X,\bar \mathbf{B}^n U(1))
  \to 
  H(X,\mathbf{B}^n U(1))
  \simeq
  H(X, \mathbf{B}^{n+1} \mathbb{Z})
  \simeq
  H^{n+1}(X,\mathbb{Z})
 $$

* the map to the curvature characteristic class

$$
  [F]
  :
  H(X,\bar \mathbf{B}^n U(1))
  \to 
  H_{dR}^{n+1}(X)
  \,.
$$

These are induced from the canonical morphisms of coefficient objects

$$
  \bar \mathbf{B}^n U(1) \simeq
  \mathbb{Z}(n+1)_D^\infty
  \to 
  \mathbf{B}^{n+1} \mathbb{Z}
$$

given by

$$
  \array{
    C^\infty(-,\mathbb{Z})    
    &\hookrightarrow&
    C^\infty(-,\mathbb{R}) 
      &\stackrel{d }{\to}&
     \Omega^1(-) 
     &\stackrel{d}{\to}& 
       \cdots 
     &\stackrel{d}{\to}&
     \Omega^n(-)
    \\
    \downarrow^{Id}
    &&
    \downarrow^{0}
    &&
    \downarrow^{0}
    &&
    &&
    \downarrow^{0}
    \\
    C^\infty(-, \mathbb{Z})
    &\to&
    0 
      &\to&
     0
     &\to& 
       \cdots 
     &\to&
     0  }
$$

and

$$
  \bar \mathbf{B}^n U(1) \simeq
  \mathbb{Z}(n+1)_D^\infty
  \to 
  (\Omega^0(-)
   \stackrel{d}{\to}
   \Omega^1(-)
   \stackrel{d}{\to}
   \cdots
   \stackrel{d}{\to}
   \Omega^{n+1}(-)
  )
$$

given by

$$
  \array{
    C^\infty(-,\mathbb{Z})    
    &\hookrightarrow&
    C^\infty(-,\mathbb{R}) 
      &\stackrel{d }{\to}&
     \Omega^1(-) 
     &\stackrel{d}{\to}& 
       \cdots 
     &\stackrel{d}{\to}&
     \Omega^n(-)
    \\
    \downarrow^{0}
    &&
    \downarrow^d
    &&
    \downarrow^d
    &&
    &&
    \downarrow^d
    \\
    C^\infty(-,\mathbb{R}) 
     &\stackrel{d}{\to}&
      \Omega^1(-)
     &\stackrel{d}{\to}& 
      \Omega^2(-)
     &\stackrel{d}{\to}& 
       \cdots 
     &\stackrel{d}{\to}&
     \Omega^{n+1}(-)
}
$$

+-- {: .un_theorem }
###### Theorem

These two morphisms exhibit Deligne cohomology as a refinement in [[differential cohomology]] of ordinary (i.e. integral [[Eilenberg-MacLane spectrum|Eilenberg-MacLane]]) [[cohomology]], in that the diagram

$$
  \array{
    H(X,\bar \mathbf{B}^\bullet U(1))
    &\stackrel{[F]}{\to}&
    H^{\bullet+1}_{dR}(X)
    \\
    \downarrow^{cl} && \downarrow
    \\
    H^{\bullet+1}(X,\mathbb{Z})
    &\to&
    H^{\bullet + 1}(X,\mathbb{R})
  }
$$

is the cohomology of a homotopy pullback diagram, i.e. satisfies the axioms described at [[differential cohomology]].

=--


#Interpretation in terms of parallel transport#

There is a natural way to understand the Deligne complex of sheaves as a sheaf which assigns to each patch the Lie $n$-groupoid of smooth parallel transport $n$-functors. This perspective is helpful for understanding how Deligne cohomology relates to the bigger picture of [[differential cohomology]].

We start by discussing this in low degree.

There is [[path groupoid]] $P_1(X)$ whose smooth 
space of objects is $X$ and whose smooth space of morphisms is
a space of classes of smooth paths in $X$. 
Every smooth 1-form $A \in \Omega^1(X)$ induces 
a smooth [[functor]] $tra_A : P_1(X) \to \mathbf{B}U(1)$
from $P_1(X)$ to to the smooth [[groupoid]] $\mathbf{B} U(1)$
with one object and $U(1)$ as its smooth space of morphisms
by sending each path $\gamma : [0,1] \to X$
to $\exp (2 \pi i\int_0^1 \gamma^* A)$. This map 
from 1-forms to smooth functors turns out to be bijective:
every smooth functor of this form uniquely arises this way.
Similarly, one finds that smooth [[natural transformation]]
$\eta_f : tra_A \to tra_{A'}$ between two such functors
is in components precisely a 
smooth function $f : X \to U(1)$ such that $A' = A + d log f$.

Since the analogous statements are true for every open subset 
$U \subset X$ this defines a [[sheaf]] of [[Lie groupoid]]s 
$$
  Funct^\infty(P_1(-), \mathbf{B}U(1)) : Op(X)^{op} \to LieGrpd
  \,.
$$
By the [[Dold-Kan correspondence]] this sheaf of groupoids
corresponds to a sheaf of complexes of groups. This complex
of sheaves is nothing but the degree 2 Deligne complex

$$
  Funct^\infty(\Pi_1(-), \mathbf{B}U(1)) \simeq \mathbb{Z}(2)^\infty_D
  \,.
$$
 
This way Deligne cohomology is realized as computing the
[[(infinity,1)-sheafification|stackification]] of the pre-stack
$Funct^\infty(P_1(-), \mathbf{B}(1))$ of smooth $U(1)$-valued 
parallel transport functors.

The identification generalizes: for all $n$ there is a [[path n-groupoid]] $P_n(X)$ whose $k$-morphisms are 
$k$-dimensional smooth paths in $X$. Smooth $n$-functors
$tra_C : _n(X) \to \mathbf{B}^n U(1)$ are canonically identified
with smooth $n$-forms $C \in \Omega^n(X)$ and 
under the [[Dold-Kan correspondence]] the Deligne-complex in degree
$n+1$ is identified with the sheaf of $n$-groupoids of such smooth 
$n$-functors
$$
  n Funct^\infty(P_n(-), \mathbf{B}^n)
  \simeq
  \mathbb{Z}(n+1)^\infty_D
  \,.
$$

See

* John Baez, Urs Schreiber, _Higher Gauge Theory_ ([arXiv](http://arxiv.org/abs/math/0511710))

The full proof for $n=1$ this is in

* Urs Schreiber, Konrad Waldorf, _Parallel transport and functors_ ([arXiv](http://arxiv.org/abs/0705.0452));

for $n=2$ in 

* Urs Schreiber, Konrad Waldorf, _Smooth functors versus differential forms_ ([arXiv](http://arxiv.org/abs/0802.0663))

For more on this see [[schreiber:Differential Nonabelian Cohomology|differential nonabelian cohomology]].

For higher $n$ there is as yet no detailed proof in the literature, but the
low dimensional proofs have obvious generalizations.


# Examples #

As described in smoe detail at [[electromagnetic field]] in abelian higher [[gauge theory|gauge theories]] the background field naturally arises as a [[Čech cohomology|Čech]]--Deligne cocycle, i.e. a [[Čech cohomology|Čech cocycle]] representative with values in the Deligne complex.

* Degree 2 Deligne cohomology classifies $U(1)$-[[principal bundle]]s [[connection on a bundle|with connection]]. The Deligne complex $\bar \mathbf{B}U(1)$ in this case coincides with the [[groupoid of Lie-algebra valued forms]] for the Lie algebra of $U(1)$.

  * In physics the [[electromagnetic field]] is modeled by a degree 2 Deligne cocycle. See there for a derivation of [[Čech cohomology|Čech]]--Deligne cohomology from physical input.

* Degree 3 Deligne cohomology classifies [[bundle gerbe]]s with connection.

  * In [[electromagnetism]] Degree 3 Deligne cocycles model [[magnetic charge]]. In formal high energy physics the [[Kalb-Ramond field]] is modeled by a Deligne 3-cocycle.

* Degree 4 Deligne cohomology classifies [[bundle 2-gerbe]]s with connection. In particular Chern-Simons bundle 2-gerbes whose degree 4 curvature characteristic class is a multiple of the Pontryagin 4-form on some $SO(n)$-[[principal bundle]]. 

  * In formal high energy physics degree 4 Deligne classes model the [[supergravity C-field]].


#References#

A standard textbook reference is section 5 of

* J.-L. Brylinski, _Loop Spaces, Characteristic Classes and geometric Quantization_, Birkhaeuser

A concise review is for instance section 2 of

* K. Gomi, _Projective unitary representations of smooth Deligne cohomology groups_ ([arXiv](http://arxiv.org/abs/math/0510187))


[[!redirects Deligne complex]]