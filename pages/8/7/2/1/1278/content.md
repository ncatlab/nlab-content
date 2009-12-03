<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}


## Idea

Differential cohomology is a refinement of ordinary [[cohomology]] such that a differential cocycle is to its underlying ordinary cocycle as a bundle with connection is to its underlying bundle.

The details of a formulation of differential cohomology depend on how the generalized [[cohomology]] theory itself is formulated.

The best known version of differential cohomology is a differential refinement of generalized cohomology in the sense of  the generalized Eilenberg--Steenrod axioms. This is a [[stable (infinity,1)-category|stable]] version of generalized cohomology.

A differential refinement of non-stable, i.e. [[nonabelian cohomology]] is developed [[schreiber:Differential Nonabelian Cohomology|here]].

## Differential stable cohomology 

A standard definition of differential cohomology is in terms of a homtopy fiber product of a generalized Eilenberg--Steenrod cohomology theory with the complex of differential forms over real cohomology:

Let $\Gamma^\bullet$ be a generalized cohomology theory in the sense of the generalized Eilenberg--Steenrod axioms, and let 
$\Gamma^\bullet \to H^\bullet(-,\mathbb{R}) \otimes \Gamma^\bullet(*)$ be a morphism to real singular cohomology with coefficients in the ring of $\Gamma$-cohomology of the point. Then the differential refinement of $\Gamma^\bullet$, the **differential $\Gamma$-cohomology** is the [[homotopy pullback]] $\bar \Gamma^\bullet$ in

$$
  \array{
  \bar \Gamma^\bullet(-)
  &\stackrel{F}{\to}&
  \Omega^\bullet(-)\otimes \Gamma^\bullet(*)
  \\
  \downarrow^{cl} && \downarrow
  \\
  \Gamma^\bullet(-)
  &\to&
  Z^\bullet(-, \mathbb{R}) \otimes \Gamma^\bullet(*)
  }
  \,,
$$

where $Z^\bullet(-,\mathbb{R})$ is the complex underlying real singular cohomology $H^\bullet(-,\mathbb{R})$ and 
where $\Omega^\bullet(-,\mathbb{R})$ is the complex underlying deRham cohomology and $\Omega^\bullet(-) \to H^\bullet(-,\mathbb{R})$ is the deRham map.

There are variations of this definition, with some technical differences in the assumptions. See the description below.

## Examples

* Differential integral cohomology $\bar H^\bullet(-,\mathbb{Z})$ is modeled by 

  * [[Deligne cohomology]];

  * [[Cheeger-Simons differential character]]s;
 
  * higher circle [[bundle gerbe]]s with connection;

* apart from that people studied mainly [[differential K-theory]].

In [[physics]] differential cocycles model [[gauge theory|gauge fields]]. 

* Cocycles in ordinary differential cohomology (e.g. [[Deligne cohomology]]) model

  * in degree 2: the [[electromagnetic field]] 

  * in degree 3: the [[Kalb-Ramond field]] 

  * in degree 4: the [[supergravity C-field]] 

* Cocycles in [[differential K-theory]] model the

  * [[RR-field]] .

For $c \in \bar \Gamma^\bullet(X)$ a differentia cocycle representing a gauge, one says that

* its image $F(c)$ in differential forms is the corresponding [[field strength]];

* its image $cl(c)$ in non-differential cohomology is the "topological twist" of the [[gauge theory|gauge field]]. In special cases this can be identified with [[magnetic charge]].


## Differential cohomology following Bunke--Schick

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


## References

A detailed discussion of the axiomatization of differential stable cohomology is

* [[Mike Hopkins]] and I. Singer, _Quadratic functions in geometry, topology,and M-theory_ ([arXiv](http://arxiv.org/abs/math/0211216))

Based on this Dan Freed interpreted large classes of gauge fields in [[physics]] in terms of differential stable cohomology in 

* [[Dan Freed]], _Dirac Charge Quantization and Generalized Differential Cohomology_ ([arXiv](http://arxiv.org/abs/hep-th/0011220))

The differential refinement of K-theory was and is studied in a series of articles by Bunke and Schick. See for instance

* [[Ulrich Bunke]], _Differential cohomology in geometry and analysis_ ([pdf slides](http://www.uni-regensburg.de/Fakultaeten/nat_Fak_I/Bunke/Vortrag-Erlangen.pdf))

and many more...


## talk notes ##

* the talks by [[Dan Freed]], Schick, [[Ulrich Bunke] and Schreiber at [[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology]]. Much of the above material is taken from Thomas Schick's lecture there.



## blog discussion

* [(Generalized) Differential Cohomology and Lie Infinity-Connections](http://golem.ph.utexas.edu/category/2008/02/lie_infinityconnections_and_ge.html)


## Differential non-abelian cohomology

for the moment, see [[schreiber:Differential Nonabelian Cohomology]]
