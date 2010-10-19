
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

> under construction

#Contents#
* automatic table of contents goes here
{:toc}


## Idea

Differential cohomology is a refinement of ordinary [[cohomology]] such that a differential cocycle is to its underlying ordinary [[cocycle]] as a [[connection on a bundle|bundle with connection]] is to its underlying [[principal bundle|bundle]].

The details of a formulation of differential cohomology depend on how the generalized [[cohomology]] theory itself is formulated.

The best known version of differential cohomology is a differential refinement of generalized cohomology in the sense of  the generalized Eilenberg--Steenrod axioms. This is a [[stable (infinity,1)-category|stable]] version of generalized cohomology.


## Differential stable cohomology 

A standard definition of differential cohomology is in terms of a [[homotopy pullback]] of a generalized Eilenberg-Steenrod cohomology theory with the complex of differential forms over real cohomology:

Let $\Gamma^\bullet$ be a generalized cohomology theory in the sense of the generalized Eilenberg--Steenrod axioms, and let 
$\Gamma^\bullet \to H^\bullet(-,\mathbb{R}) \otimes \Gamma^\bullet(*)$ be a morphism to real singular cohomology with coefficients in the ring of $\Gamma$-cohomology of the point. Then the differential refinement of $\Gamma^q$, the degree $q$**differential $\Gamma$-cohomology** is the [[homotopy pullback]] $\bar \Gamma^\bullet$ in

$$
  \array{
  \bar \Gamma^\bullet(-)
  &\stackrel{F}{\to}&
  \Omega^{\geq q}(-)\otimes \Gamma^\bullet(*)
  \\
  \downarrow^{cl} && \downarrow
  \\
  \Gamma^\bullet(-)
  &\stackrel{ch}{\to}&
  Z^\bullet(-, \mathbb{R}) \otimes \Gamma^\bullet(*)
  }
  \,,
$$

where 

* $Z^\bullet(-,\mathbb{R})$ is the complex underlying real singular cohomology $H^\bullet(-,\mathbb{R})$ 

* $\Omega^\bullet(-,\mathbb{R})$ is the complex underlying deRham cohomology 

* $\Omega^\bullet(-) \to H^\bullet(-,\mathbb{R})$ is [[deRham theorem]] morphism

* $ch: \Gamma^\bullet(-)
  \to
  Z^\bullet(-, \mathbb{R}) \otimes \Gamma^\bullet(*)$ is the [[Chern character]] map.

There are variations of this definition, with some technical differences in the assumptions. See the description below.

### Examples

* The [[ordinary differential cohomology]] $\bar H^\bullet(-,\mathbb{Z})$ is modeled by 

  * [[Deligne cohomology]];

  * [[Cheeger-Simons differential character]]s;
 
  * higher circle [[bundle gerbe]]s with connection;

  * [[circle n-bundles with connection]].

* apart from that people studied mainly [[differential K-theory]].

In [[physics]] differential cocycles model [[gauge theory|gauge fields]]. 

* Cocycles in [[ordinary differential cohomology]] (e.g. [[Deligne cohomology]]) model

  * in degree 2: the [[electromagnetic field]] 

  * in degree 3: the [[Kalb-Ramond field]] 

  * in degree 4: the [[supergravity C-field]] 

* Cocycles in [[differential K-theory]] model the

  * [[RR-field]] .

For $c \in \bar \Gamma^\bullet(X)$ a differential cocycle representing a gauge, one says that

* its image $F(c)$ in differential forms is the corresponding [[field strength]];

* its image $cl(c)$ in non-differential cohomology is the "topological twist" of the [[gauge theory|gauge field]]. In special cases this can be identified with [[magnetic charge]].


### Detailed construction following Hopkins-Singer {#HopSin}

We survey some aspects of the constructions in

* [[Mike Hopkins]], I. Singer, _[[Quadratic Functions in Geometry, Topology,and M-Theory]]_

#### Definitions

**Definition

For 

* $X$ be a [[topological space]] and 

* $\iota \in Z^n(X,\mathbb{R})$ a [[cocycle]] on $X$ for real-valued [[singular cohomology]] on $X$,

a **differential function** on a smooth [[manifold]] $S$ with values in $(X,\iota)$ is a triple $(c,h,\omega)$ with

* $c : S \to X$ a continuous map;

* $h \in C^{n-1}(S,\mathbb{R})$ a cochain in real cohomology on $S$;

* $\omega \in \Omega^n(S)$ a smooth [[differential form]] on $S$;

such that in the abelian group $Z^n(S,\mathbb{R})$ the equation

$$
  \omega = c^*\iota + \delta h
$$

holds, where $\omega$ is here regarded as a singular cochain (that sends a chain to the integral of $\omega$ over it), and where $\delta$ denotes the coboundary operator, i.e. the [[Moore complex]] differential of the [[singular simplicial complex]].

In words this is: a continuous map to the topological space together with a _smooth_ refinement of the pullback of the chosen singular cochain.

The **differential function complex** or **[[infinity-groupoid]] of differential functions** $(X,\iota)^S$ of all differential functions $S \to (X,\iota)$ is the [[simplicial set]] whose $k$-cells are differential functions

$$
  S \times \Delta^k_{\Diff} \to (X,\iota)
  \,.
$$

Let

$$
  filt_0 (X,\iota)^S \subset (X,\iota)^S
$$

be the sub-simplicial set of those simplices $(c,\omega,h) S \times \Delta^k_{Diff} \to (S,\iota)$ for which $\omega \on \Omega^n(S \times \Delta^k_{Diff})$ is pulled back from a form on just $S$, i.e. has no components along the $\Delta^k_{Diff}$-direction.

This $filt_0 (X,\iota)^S$ is the [[homotopy pullback]] in the category [[sSet]] equipped with the standard [[model structure on simplicial sets]] in the diagram

$$
  \array{
    filt_0 (X,\iota)^S &\to& filt_0 \Omega^n_{cl}(S \times \Delta^\bullet_{Diff})
   \\
   \downarrow && \downarrow
   \\
   Hom_{Top}(S \times \Delta^\bullet_{Top}, X)
   &\to&
   Z^n(S \times\Delta^\bullet, \mathbb{R})
  }
  \,.
$$

#### Properties

**Proposition**

The [[simplicial homotopy group]]s of $filt_0 \Omega^n_{cl}(S \times \Delta^\bullet_{Diff})$ are 

$$
  \pi_k filt_0 \Omega^n_{cl}(S \times \Delta^\bullet_{Diff})
  =
  \left\{
    \array{
       \Omega^n_{cl}(S) & | k = 0
       \\
       0 & | k \gt 0
    }
  \right\}
  \,.
$$

The homotopy groups of $Z^n(S \times\Delta^\bullet, \mathbb{R})$ are

$$
  \pi_k Z^n(S \times\Delta^\bullet, \mathbb{R})
  = 
  H^{n-k}(S)
  \,.
$$

**Proof** This appears in [[Quadratic Functions in Geometry, Topology,and M-Theory|SopSin, p. 36]] based on corollary D,15 there.

> This should mean that the first complex is equivalent to the _set_ of closed forms and the second to $sSet(Sing S, \mathcal{B}^n \mathbb{R})$. 


#### Examples

##### Line bundles with connection


Let $X = \mathcal{B} U(1) \simeq K(\mathbb{Z},2)$ be the [[Eilenberg-MacLane space]] that is the [[classifying space]] for $U(1)$-[[principal bundle]]s. It carries the canonical [[cocycle]] $\iota := Id : \mathcal{B}U(1) \to \mathcal{B}U(1) \simeq K(\mathbb{Z},2)$ representing in $H^2(X,\mathbb{Z})$ the class of the universal complex [[line bundle]] $L \to X$ on $X$.

Accordingly, for $c : S\to \mathcal{B}U(1)$ a continuous map, we have the corresponding line bundle $c^* L$ on $S$. 

One checks (...details...Example 2.7 in HopSin) that a refinement of $c$ to a differential function $(c,\omega,h)$ corresponds to equipping $c^* L$ with a [[connection on a bundle|smooth connection]].

Now consider $((c,\omega,h) \to (c',\omega', h')) \in filt_0  (\mathcal{B}U(1),Id)^S$ a morphism between two such $(\mathcal{B}U(1),Id)$-differential functions. By definition this is now a $U(1)$-principal bundle $\hat L$ with connection on $S \times \Delta^i_{Diff}$, whose curvature form $\hat \omega \in \Omega^2(S \times \Delta^1_{Diff})$ is of the form $g \cdot \tilde \omega$, where $\tilde \omega$ is a 2-form on $S$ and $g$ is a smooth function on $\Delta^1_{Diff}$, both pulled back to $S \times \Delta^1_{Diff}$ and multiplied there.

But since $\hat \omega$ is necessarily _closed_ it follows with $d (g \wedge \tilde \omega) = d t \frac{\partial g}{\partial t} \wedge \tilde \omega + g \wedge d_{S} \tilde \omega$ that $g$ is actually constant. 

This means that that the parallel transoport of the connection $\hat \nabla$ on $S \times \Delta^1_{Diff}$ induces a insomorphism between the two line bundles on $S$ over the endpoints of $S \times \Delta^1_{Diff}$ that respects the connections. 

...

##### Differential K-cocycles


### Detailed construction following Bunke--Schick

The following theory of differential cohomology
(also called **smooth cohomology**) is developed and used
in the work of [[Ulrich Bunke]] and [[Thomas Schick]]. Contrary to the above, it does not take the notion of homotopy limit as fundamental, but instead characterizes the universality of the above commuting diagram by other means. On the other hand, this means that their axiomatization at the moment only capture cohomology classes, not the representing cocycles. It is sort of known that for various applications specific cocycle representatives do play an important role, and one may imagining refining to discussion below eventually to accomodate for that.

* idea:

  * combine cohomology + differential forms
  
main diagram


$$
  \array{
    \hat H(M) &\stackrel{I}{\to}& H^\bullet(M)
    \\
    \downarrow^{R} && \downarrow
    \\
    \Omega^\bullet_{d=0}(M)
    &\stackrel{}{\to}&
    H^\bullet_{dR}(M)
    \simeq H^\bullet(M,\mathbb{R})
  }
$$

so differential cohomology $\hat H^\bullet(M)$ combines the ordinary cohomology $H^\bullet(M)$
with a differential form representative of its image in real cohomology.

* $I$ projects a differential cohomology to its underlying ordinary cohomology class;

* $R$ send the differential cohomology class to its _curvature_ differential form data

we want an exact sequence

$$
 \array{
   H^{\bullet-1}(M)
   &\stackrel{ch}{\to}&
   \Omega^{\bullet-1}(M)/{im(d)}
   &\stackrel{d}{\to}&
   \hat H(M) 
   &\stackrel{I}{\to}& 
   H^\bullet(M) \to 0
   \\
   &&&
   {}_{d}\searrow
   &
   \downarrow^R
   \\
   &&&&
   \Omega^\bullet_{d=0}(M)
 }
$$

+-- {: .un_defn}
###### Definition

Given cohomology theory $E^\bullet$, a smooth refinement
$\hat E^\bullet$ is a functor $\hat E : Diff \to Grps$
with transformations $I, R$ such that 

$$
  \array{
    \hat E(M) &\stackrel{I}{\to}& E^\bullet(M)
    \\
    \downarrow^{R} && \downarrow
    \\
    \Omega^\bullet_{d=0}(M, V)
    &\stackrel{}{\to}&
    E^\bullet_{dR}(M)
    \simeq E^\bullet(M,\mathbb{R})
  }
$$

where 

$V = E^\bullet(pt)\otimes \mathbb{R}$

is the graded non-torsion cohomology of $E$ on the point (so now all the
gradings above denote total grading)

and such that there is a transformation

$$
  a : \Omega^{\bullet -1}(M)/{im(d)}
  \to
  \hat E^*(M)
$$

that gives the above kind of exact sequence.
=--


+-- {: .un_defn}
###### Definition

If $E^*$ is multiplicative, we say $\hat E^*$ is multiplicative with 
product $\vee$
if $\hat E$ takes values in graded rings and the transformations are
compatible with multiplicative structure, where

$$
  a(\omega) \vee x = a(\omega \wedge R(x))
$$
=--


+-- {: .un_defn}
###### Definition

$\hat E$ has $S^1$-integration if there is a natural (in $M$) transformation

$$
  \int : \hat E^*(M \times S^1) \to \hat E^{\bullet -1}(M)
$$

compatible with $\int$ of forms  and for $E$ it is given by the suspension isomorphism

$$
  \int \circ p^* = 0
$$

for $p : M \times S^1 \to M$ and

$$
  \int \circ (  id \times (z \mapsto \bar z) )^* = - \int
$$
=--


+-- {: .un_remark}
###### Remark

Ordinary cohomology theories are supposed to be homotopy
invariant, but differential forms are not, so in general the differential
cohomology is not.
=--


+-- {: .un_lemma}
###### Lemma
Given $\hat E$ a smooth cohomology theory. 
The **homotopy formula**:

given $h : M \times [0,1] \stackrel{smooth}{\to} N$
a smooth homotopy we have

$$
  h^*_1(X) - h^*_0(X)
  =
  a( \int_{M \times [0,1]/M}  h^*(R(x)))
$$
=--

+-- {: .un_cor}
###### Corollary
$ker(R)$ (i.e. flat cohomology) is a homotopy invariant
functor.
=--

+-- {: .un_defn}
###### Definition
$\hat H{flat} := ker(R)$
=--

+-- {: .proof}
###### Proof of lemma

It suffices to show 

$$
  \iota_1^*(x) - \iota_0^*(x) = a(\int_{M\times [0,1]/M} R(x))
$$

for all $x \in \hat E(M \times [0,1])$.

Observe if $x = p^* y$ the left hand side vanishes, $\int R(p^* y) = 0$.

For general $x$ $\exists y \in \jhat E(M)$; $x - p^*(y) = a (\omega)$
$\omega \in \Omega(M \times [0,1])$.

Stokes' theorem gives $i^*_1 \omega - i^*_0 \omega = \int_{[0,1]} d \omega$
$= \int R(a(\omega)) = \int R(x-p^* \omega) = \int R(x)$.

On the other hand

$$
  i^*_1(x) - i^*_0(x) = i^*_1(a(\omega))
    - i^*_0(a(\omega))
    = a(\int R(x))
$$

A calculation: $\hat H^1_{flat}(pt) = \hat H^1(pt) = \mathbb{R}/\mathbb{Z} = \hat K^1(pt)$.
=--


+-- {: .un_theorem}
###### Theorem (Hopkins--Singer)

For each generalized cohomology theory $E^*$ 
a differential version  $\hat E^*$ as in the above definition does exist.

Moreover $\hat E_{flat}^* = E \mathbb{R}/\mathbb{Z}^{\bullet -1}$.
=--

+-- {: .un_remark}
###### Remark
It's not evident how to obtain more structure like multiplication.
=--

+-- {: .un_theorem}
###### Theorem
Using geometric models, multiplicative smooth extensions
with $S^1$-integration are constructed for

* K-theory (Bunke--Schick)

* MU-bordisms (unitary bordisms)  
  (Bunke--Schr&#246;der--Schick--Wiethaupts; and from there Landweber exact cohomology theories)
=--


+-- {: .un_theorem}
###### Uniqueness theorem (Bunke--Schick)

(Simons--Sullivan proved this for ordinary integral cohomology.)

Assume $E^*$ is _rationally even_, meaning that

$$
  E^k(pt)\otimes \mathbb{Q} = 0 \;\; for odd k 
$$

plus one further technical assumption.

Then any two smooth extensions $\hat E^*$, $\tilde E^*$ are naturally
isomorphic.

If required to be compatible with integration the ismorphism is unique.

If $\hat E, \tilde E$ are multiplicative, then this isomorphism is,
as well.
=--

+-- {: .un_example}
###### Example

If we don't require compatibility with $S^1$-integration, then there
are "exotic" abelian group structures on $\hat K^1$.
=--

#### Examples

##### Differential cobordism cohomology theory

A model for a multiplicative differential refinement of [[complex cobordism cohomology theory]], the theory represented by the [[Thom spectrum]] is in 

* [[Ulrich Bunke]], [[Thomas Schick]], Ingo Schr&#246;der,  Moritz Wiethaup,  _Landweber exact formal group laws and smooth cohomology theories_ ([arXiv:0711.1134](http://arxiv.org/abs/0711.1134))

See [[differential cobordism cohomology theory]]

## References {#References}

A detailed discussion of the axiomatization of differential stable cohomology is

* [[Mike Hopkins]] and I. Singer, _[[Quadratic Functions in Geometry, Topology,and M-Theory]]_ ([arXiv](http://arxiv.org/abs/math/0211216))

Based on this Dan Freed interpreted large classes of gauge fields in [[physics]] in terms of differential stable cohomology in 

* [[Dan Freed]], _Dirac Charge Quantization and Generalized Differential Cohomology_ ([arXiv](http://arxiv.org/abs/hep-th/0011220))

The differential refinement of K-theory was and is studied in a series of articles by Bunke and Schick. See for instance

* [[Ulrich Bunke]], _Differential cohomology in geometry and analysis_ ([pdf slides](http://www.uni-regensburg.de/Fakultaeten/nat_Fak_I/Bunke/Vortrag-Erlangen.pdf))

and many more...

* [[James Simons]], [[Dennis Sullivan]], _The Mayer-Vietoris Property in Differential Cohomology_ ([arXiv:1010.3300](http://arxiv.org/abs/1010.3300))

## talk notes ##

* The talks by [[Dan Freed]], Schick, [[Ulrich Bunke]] and Schreiber at [[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology]]. Much of the above material is taken from Thomas Schick's lecture there.



