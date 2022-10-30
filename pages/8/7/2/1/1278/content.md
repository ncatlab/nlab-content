
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

Differential cohomology is a refinement of plain [[cohomology]] such that a differential cocycle is to its underlying ordinary [[cocycle]] as a [[connection on an infinity-bundle|bundle with connection]] is to its underlying [[principal infinity-bundle|bundle]].

The best known version of differential cohomology is a differential refinement of [[generalized (Eilenberg-Steenrod) cohomology]], hence of [[cohomology]] in [[stable homotopy theory]] (as opposed to more general [[nonabelian cohomology]]). For [[ordinary cohomology]] the refinement to [[ordinary differential cohomology]] is modeled for instance by [[complex line bundles]] with [[connection on a bundle]], [[bundle gerbes with connection]], etc, and generally by [[Deligne cohomology]]. Similarly, differential refinements of [[topological K-theory]] to [[differential K-theory]] may be presented by [[vector bundles]] [[connection on a bundle|with connection]] (e.g [Simons-Sullivan 08](#SimonsSullivan08)).

A systematic characterization and construction of differential [[generalized (Eilenberg-Steenrod) cohomology]] in terms of 
suitable [[homotopy fiber products]] of the [[mapping spectra]] [[Brown representability theorem|representing]] the underlying [[cohomology theory]] with [[differential form]] data was then given in ([Hopkins-Singer 02](#HopkinsSinger02)) (motivated by discussion of the [[quantization]] of the [[M5-brane]] via holographically dual [[7d Chern-Simons theory]] by [[Edward Witten]]). 

In this stable case one characteristic property of differential cohomology that was first observed empirically in [[ordinary differential cohomology]] ([Simons-Sullivan 07](#SimonsSullivan07)) and [[differential K-theory]] ([Simons-Sullivan 08](#SimonsSullivan08)) is that it is a kind of cohomology theory which fits into a _[[differential cohomology diagram]]_ which is an interlocking system of two [[fiber sequences]] that expresses how the data of a geometric bundle with connection may be decomposed into the underlying bundle and the [[curvature]] of the connection and how connections on trivial bundles as well as bundles with [[flat infinity-connection|flat connections]] are examples of the general concept. (The [[homotopy fiber product]] used in ([Hopkins-Singer 02](#HopkinsSinger02)) provides one of the two commuting squares in this diagram.)

Schematically the characteristic [[differential cohomology hexagon]] (see there for details) looks as follows

$$
  \array{
    &&  connection\;on\;trivial\;bundle && \stackrel{de\;Rham\;differential}{\longrightarrow} && differential\;forms
    \\
    & \nearrow & & \searrow & & \nearrow_{curvature} && \searrow
    \\
    flat\;differential\;forms  && && geometric\;bundle\;with \;connection && && rational\;shape\;of\;bundle
    \\
    & \searrow &  & \nearrow & & \searrow^{\mathrlap{}} && \nearrow_{\mathrlap{Chern\;character}}
    \\
    && geometric\;bundle\;with\;flat\;connection && \underset{forget\;connection}{\longrightarrow} && shape\;of\;bundle
  }
$$



It turns out  that such [[differential cohomology diagrams]] are exactly what all [[stable homotopy types]] in [[cohesive (∞,1)-toposes]] $\mathbf{H}$ naturally sit in ([Bunke-Nikolaus-V&#246;lkl 13](#BunkeNikolausVoelkl13)). All the traditional differential cohomology theories and their joint generalization due to ([Hopkins-Singer 02](#HopkinsSinger02)) are special cases of this for the case that $\mathbf{H} = T Smooth \infty Grpd$ is the [[tangent cohesive (∞,1)-topos]] of that of [[smooth ∞-groupoids]] ([[∞-stacks]] over the [[site]] of [[smooth manifolds]]).

It is therefore natural to _define_ differential cohomology to be the intrinsic [[cohomology]] of [[cohesive (∞,1)-toposes]]. (Notice that while the [[differential cohomology diagram]] itself only involves the [[shape modality]] and the [[flat modality]] of [[cohesion]], the [[sharp modality]] is needed to produce, via [[differential concretification]], the correct [[moduli stacks]] of differential cocycles over a given base object from the [[mapping stack]] of that into the representing [[stable homotopy type]]).

Viewed in this generality, differential cohomology makes sense for instance also in [[supergeometry]] where it subsumes structures such as [[super line 2-bundles]] and more generally [[Super Gerbes|higher super gerbes]] with connection, which naturally appear as differential refinements of the geometric [[twisted cohomology|twists]] of (differential) [[K-theory]] and [[tmf]]. 


## Examples

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

For $c \in \bar \Gamma^\bullet(X)$ a differential cocycle representing a [[gauge field]], one says that

* its image $F(c)$ in differential forms is the corresponding [[field strength]];

* its image $cl(c)$ in non-differential cohomology is the "topological twist" of the [[gauge theory|gauge field]]. In special cases this can be identified with [[magnetic charge]].

Other examples:

* [[differential algebraic K-theory]]


## Differential stable cohomology 

> the following are ancient notes that need to be brushed up and polished.


### Characterization following Hopkins-Singer 
 {#HopSin}

A standard definition of differential cohomology is in terms of a [[homotopy pullback]] of a [[generalized (Eilenberg-Steenrod) cohomology theory]] with the complex of [[differential forms]] over [[real cohomology]]:

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

For more details on this see at _[[differential function complex]]_.

### Characterization following Bunke-Schick

> The following are old notes once taken in a talk by [[Thomas Schick]] at _[[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology]]_. Needs to be brushed-up, polished, improved, rewritten...

The following theory of differential cohomology
(also called **smooth cohomology**) is developed and used
in the work of [[Ulrich Bunke]] and [[Thomas Schick]]. Contrary to the above, it does not take the notion of homotopy limit as fundamental, but instead characterizes the universality of the above commuting diagram by other means. On the other hand, this means that their axiomatization at the moment only capture cohomology classes, not the representing cocycles. It is sort of known that for various applications specific cocycle representatives do play an important role, and one may imagining refining to discussion below eventually to accommodate for that.

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
with a differential form representative of its image in [[real cohomology]].

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

+-- {: .num_defn}
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


+-- {: .num_defn}
###### Definition

If $E^*$ is multiplicative, we say $\hat E^*$ is multiplicative with 
product $\vee$
if $\hat E$ takes values in graded rings and the transformations are
compatible with multiplicative structure, where

$$
  a(\omega) \vee x = a(\omega \wedge R(x))
$$
=--


+-- {: .num_defn}
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


+-- {: .num_remark}
###### Remark

Ordinary cohomology theories are supposed to be homotopy
invariant, but differential forms are not, so in general the differential
cohomology is not.
=--


+-- {: .num_lemma}
###### Lemma
Given $\hat E$ a smooth cohomology theory. 
The **homotopy formula**:

given $h : M \times [0,1] \stackrel{smooth}{\to} N$
a [[smooth homotopy]] we have

$$
  h^*_1(X) - h^*_0(X)
  =
  a( \int_{M \times [0,1]/M}  h^*(R(x)))
$$
=--

+-- {: .num_cor}
###### Corollary
$ker(R)$ (i.e. flat cohomology) is a homotopy invariant
functor.
=--

+-- {: .num_defn}
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


+-- {: .num_theorem}
###### Theorem 
(Hopkins--Singer)

For each generalized cohomology theory $E^*$ 
a differential version  $\hat E^*$ as in the above definition does exist.

Moreover $\hat E_{flat}^* = E \mathbb{R}/\mathbb{Z}^{\bullet -1}$.
=--

+-- {: .num_remark}
###### Remark
It's not evident how to obtain more structure like multiplication.
=--

+-- {: .num_theorem}
###### Theorem
Using geometric models, multiplicative smooth extensions
with $S^1$-integration are constructed for

* K-theory (Bunke--Schick)

* MU-bordisms (unitary bordisms)  
  (Bunke--Schr&#246;der--Schick--Wiethaupts; and from there Landweber exact cohomology theories)
=--


+-- {: .num_theorem}
###### Theorem 
(Uniqueness theorem due to Bunke--Schick. Simons--Sullivan proved this for ordinary integral cohomology.)

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

+-- {: .num_example}
###### Example

If we don't require compatibility with $S^1$-integration, then there
are "exotic" abelian group structures on $\hat K^1$.
=--

#### Examples

##### Differential cobordism cohomology theory

A model for a multiplicative differential refinement of [[complex cobordism cohomology theory]], the theory represented by the [[Thom spectrum]] is in 

* [[Ulrich Bunke]], [[Thomas Schick]], Ingo Schr&#246;der,  Moritz Wiethaup,  _Landweber exact formal group laws and smooth cohomology theories_ ([arXiv:0711.1134](http://arxiv.org/abs/0711.1134))

See [[differential cobordism cohomology theory]]


## Related concepts

* [[tangent cohesion]], [[smooth spectrum]]

* [[differential orientation]]

* [[twisted differential cohomology]]

[[!include gauge field - table]]


## References 
 {#References}

### General

Differential cohomology was first developed for the special cases of [[ordinary differential cohomology]]  and of [[differential K-theory]] (interest into which came from discussion of [[D-brane charge]] in [[type II superstring theory]]). See the references there. A survey is in 

* [[Ulrich Bunke]], _Differential cohomology in geometry and analysis_ ([pdf slides](http://www.uni-regensburg.de/Fakultaeten/nat_Fak_I/Bunke/Vortrag-Erlangen.pdf))

The suggestion that differential cohomology is or should be characterized by the [[differential cohomology diagram]] is due to

* {#SimonsSullivan07} [[James Simons]], [[Dennis Sullivan]], _Axiomatic Characterization of Ordinary Differential Cohomology_ ([arXiv:math/0701077](http://arxiv.org/abs/math/0701077))

  (discussed there for [[ordinary differential cohomology]])

and

* {#SimonsSullivan08} [[James Simons]], [[Dennis Sullivan]], _Structured vector bundles define differential K-theory_ ([arXiv:0810.4935](http://arxiv.org/abs/0810.4935))

  (discussed there for [[differential K-theory]]).

A first systematic account characterizing and constructing stable differential cohomology in terms of [[homotopy fiber products]] of bare [[spectra]] with [[differential form]] data (which is really the homotopy-theoretic refinement of one of right square in the [[differential cohomology diagram]]) was given in

* {#HopkinsSinger02} [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology,and M-Theory]]_, J. Differential Geom. Volume 70, Number 3 (2005), 329-452.   ([arXiv:math/0211216](http://arxiv.org/abs/math/0211216), [euclid:1143642908](https://projecteuclid.org/euclid.jdg/1143642908))

motivated by applications in [[higher gauge theory]] and [[string theory]], as explained further in 

* [[Dan Freed]], _[[Dirac charge quantization and generalized differential cohomology]]_ ([arXiv:hep-th/0011220](http://arxiv.org/abs/hep-th/0011220))

with further reviews including

* [[Alessandro Valentino]], _Differential cohomology and quantum gauge fields_ ([pdf](http://www.uni-math.gwdg.de/sandro/seminarGoett.pdf))

* [[Richard Szabo]], _Quantization of Higher Abelian Gauge Theory in Generalized Differential Cohomology_ ([arXiv:1209.2530](http://arxiv.org/abs/1209.2530))

The homotopy-pullback definition of differential generalized cohomology from 

* [Hopkins-Singer 02, Section 4.1](#HopkinsSinger02)

is picked up in

* [[Ulrich Bunke]], [[David Gepner]], Section 2.2 of: _Differential function spectra, the differential Becker-Gottlieb transfer, and applications to differential algebraic K-theory_ ([arXiv:1306.0247](https://arxiv.org/abs/1306.0247))

* {#Bunke12} [[Ulrich Bunke]], Section 4.3 of: _Differential cohomology_ ([arXiv:1208.3961](http://arxiv.org/abs/1208.3961))

* [Bunke-Nikolaus-Völkl 13, Section 4.4](#BunkeNikolausVoelkl13)


The suggestion that differential cohomology is naturally the intrinsic [[cohomology]] of those [[(∞,1)-toposes]] which are [[cohesive (∞,1)-topos|cohesive]] appeared in

* {#Schreiber13} [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ ([arXiv:1310.7930](http://arxiv.org/abs/1310.7930))

and the observation that indeed every [[stable homotopy type]] in a [[cohesive (∞,1)-topos]] canonically sits inside a [[differential cohomology diagram]] is due to 

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], _Differential cohomology theories as sheaves of spectra_,  J. Homotopy Relat. Struct. 11, 1–66 (2016) ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))






### Lectures and talks 


* Simons Center Workshop on Differential Cohomology January 10, 2011- January 14, 2011 ([web](http://www.scgp.stonybrook.edu/?q=node/21))

* {#DG18} [[Daniel Grady]], _Differential cohomology and Applications_, talk at _Geometry, Topology & Physics_, NYU Abu Dhabi, April 2018 ([[DiffCohomologyAndApplications18.pdf:file]])


[[!redirects differential cohomology theory]]
[[!redirects differential cohomology theories]]