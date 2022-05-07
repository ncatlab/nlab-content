
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

### General idea

What is called a  **homotopy quantum field theory** is a [[TQFT]] defined on [[cobordisms]] that are equipped with the extra [[structure]] of a [[continuous function]] into a fixed [[topological space]] $B$. 

Hence if $Bord_n(B)$ denotes a [[category of cobordisms]] suitably equipped with maps into $B$, then an HQFT is a [[monoidal functor]]
$$
  Z \;\colon\; Bord_n(B)^{\coprod} \longrightarrow Vect^{\otimes}
  \,.
$$



### History 

HQFTs were first defined (under a different name) by [[Graeme Segal]] as early as 1988 in ([Segal 88](#Segal88)).

Starting from 1991, several papers by [[Dan Freed]],
including \cite{FreedQuinn1991}, further developed the notion of a [[functorial field theory]], where bordisms in the domain category are equipped with a map
to a target space (such as the [[Eilenberg–MacLane space]] $K(G,1)$ for a finite group $G$).
See, in particular, Theorem 1.7 and the preceding discussion on page 6 of \cite{FreedQuinn1991}.

From 1999, HQFTs were studied systematically by [[Vladimir Turaev]] ([Turaev 99](#Turaev99)) for 2-dimensional [[manifolds]]/[[cobordisms]] and extended to 3-dimensional ones in ([Turaev 00](#Turaev00)).
Turaev also introduced the term “homotopy quantum field theory”.

At about the same time, ([Brightwell-Turner 00](#BrightwellTurner00)) looked at what they called the [[homotopy]] surface category and its [[representation]]s. There are two viewpoints which interact and complement each other. Turaev's seems to be to see HQFTs as an extension of the tool kit for studying [[manifolds]] already given by [[TQFT]]s, whilst in Brightwell and Turner's,  it is the 'background space', which is probed by the surfaces in the sense of [[sigma-models]].

In the proof of the [[cobordism hypothesis]] in ([[On the Classification of Topological Field Theories|Lurie 09]]) the concept of HQFTs was refined to [[extended TQFT]] by considering an [[(∞,n)-category of cobordisms]] $Bord_n(X)$ with maps to a given [[homotopy type]] $X$. For these the [[cobordism hypothesis]] essentially says (see at [For framed cobordisms in a topological space](cobordism+hypothesis#StatementForCobordismsInAManifold)) that $Bord_n(X)^\coprod$ is the [[free construction]] [[(∞,n)-category with duals]] on the [[fundamental ∞-groupoid]] $\Pi(X)$ of $X$.


## Definition

An HQFT is going to be defined as assigning data to $B$-cobordisms. We first introduce these

* [B-cobordisms](#BCobordism)

and then define

* [HQFTs](#HQFTs)

themselves in terms of these.

### $B$-Cobordisms
 {#BCobordism}


Let $B$ be a [[pointed topological space]].

+-- {: .num_defn }
###### Definition

A **$B$-manifold** is a pair $(X, g)$, where $X$ is a closed oriented $n$-[[manifold]] (with a choice of base point $m_i$ in each connected component $X_i$ of $X$), and $g$ is a [[continuous function]] $g : X \to B$, called the **characteristic map**, such that $g(m_i) = \ast$ for each base point $m_i$.

=--

+-- {: .num_defn }
###### Definition

A **$B$-isomorphism** between $B$-manifolds, $\phi : ( X, g) \to ( Y, h)$ is an [[isomorphism]] $\phi : X \to Y$ of the manifolds, preserving the orientation, taking base points into base points and such that $h\phi = g$.

=--

+-- {: .num_remark }
###### Remark

If as  is often the case, the manifolds under consideration will be [[smooth manifolds]]  and then '[[isomorphism]]' is interpreted as '[[diffeomorphism]]', but equally well we can position the theory in the category of PL-manifolds or triangulable topological manifolds with the obvious changes.  In fact for some of the time it is convenient to  develop constructions for simplicial complexes rather than manifolds, as it is triangulations that provide the basis for the combinatorial descriptions of the structures that we will be using.

=--

+-- {: .num_defn }
###### Definition

Denote by $\mathbf{Man}(n,B)$ the [[category]] of $n$-dimensional $B$-manifolds and $B$-isomorphisms.  We define a 'sum' operation on this category using [[disjoint union]].  The disjoint union of $B$-manifolds is defined by
$$( X, g) \amalg ( Y, h) := ( X\amalg Y, g\amalg h),$$
with the obvious characteristic map, $g\amalg h : X \amalg Y \to B$.  With this 'sum' operation, $\mathbf{Man}(n,B)$ becomes a symmetric monoidal category with the unit being given by the empty $B$-manifold, $\emptyset$, with the empty characteristic map.  Of course, this is an $n$-manifold by default.

=--


These $B$-manifolds are the objects of interest, but they have to be related by the analogue of [[cobordisms]] for this setting.

+-- {: .num_defn }
###### Definition

A **$B$-cobordism**, $(W,F)$, from $(X_0,g)$ to $(X_1,h)$ is a [[cobordism]] $W : X_0 \to X_1$ endowed with a [[homotopy class]] relative to the boundary of a [[continuous function]] $F : W \to B$  such that 

$$
  F|_{X_0} =  g \,, \;\;\;\;  F|_{X_1} = h
$$

=--

+-- {: .num_remark }
###### Remark

Generally, unless necessary in this entry, we will not make a notational distinction between the [[homotopy class]] $F$ and any of its representatives.  

=--

+-- {: .num_defn }
###### Definition

A **$B$-isomorphism of $B$-cobordisms**, $\psi : (W,F) \to (W^\prime, F^\prime)$, is an isomorphism $\psi : W \to W^\prime$ such that 

$$\psi (\partial_+W) = \partial_+W^\prime, \quad \psi (\partial_-W) = \partial_-W^\prime,$$

and $F^\prime \psi = F$, in the obvious sense of homotopy classes relative to the boundary.

=--

We can glue $B$-cobordisms along their boundaries, or more generally, along a $B$-isomorphism between their boundaries, in the usual way. This gives rise to a [[symmetric monoidal category]] $\mathbf{HCobord}(n,B)$ of $B$-cobordisms

The detailed structure of $B$-[[cobordisms]] and the resulting category $\mathbf{HCobord}(n,B)$ is given in ([Rodrigues 03, appendix](#Rodrigues03)), at least in the important case of [[smooth manifold|smooth]] $B$-manifolds.  This category is a [[monoidal category]] with strict [[dual objects]].

### Homotopy Quantum Field Theories 
 {#HQFTs}

The general absract definition of an HQFT is now the following.

Fix an integer $n \geq 0$ and a [[field]], $K$. All vector spaces will be tacitly assumed to be finite dimensional.  In general $K$ can be replaced by a [[commutative ring]] merely by replacing finite dimensional vector spaces by projective $K$-[[modules]] of finite type, but we will not do this here.


+-- {: .num_defn }
###### Definition

A **homotopy quantum field theory** is  a [[symmetric monoidal functor]] from $\mathbf{HCobord}(n,B)$  to the category, [[Vect]], of finite dimensional vector spaces over the [[field]] $K$. 

=--

This definiting unwinds to the following structure in components

+-- {: .num_defn }
###### Definition

 A **$(n + 1)$-dimensional homotopy quantum field theory**, $\tau$, with background $B$  assigns 

* to any $n$-dimensional $B$-manifold, $(X,g)$, a vector space, $\tau{(X,g)}$, 

* to any $B$-isomorphism, $\phi : (X, g) \to ( Y, h)$, of $n$-dimensional $B$-manifolds, a $K$-linear isomorphism $\tau(\phi)  : \tau{(X, g)} \to \tau{( Y, h)}$,

 and

* to any $B$-cobordism, $(W,F) : (X_0,g_0) \to (X_1,g_1)$, a $K$-linear transformation, $\tau(W) : \tau{(X_0,g_0)} \to \tau{(X_1,g_1)}$.

These assignments are to satisfy the following axioms:

1. $\tau$ is functorial in $\mathbf{Man}(n,B)$, i.e., for two $B$-isomorphisms, $\psi: (X, g) \to ( Y, h)$ and $\phi : ( Y, h) \to (P,j)$, we have $\tau(\phi\psi) = \tau(\phi)\tau(\psi),$
and if $1_{(X,g)}$ is the identity $B$-isomorphism on $(X,g)$, then $\tau(1_{(X,g)}) = 1_{\tau{(X,g)}}$

 1.  There are natural isomorphisms
$$c_{(X,g),(Y,h)} : \tau((X,g)\amalg (Y,h)) \cong \tau(X,g)\otimes \tau(Y,h),$$
and an isomorphism, $u : \tau(\emptyset) \cong K$, that satisfy the usual axioms for a [[symmetric monoidal functor]].

1.  For $B$-cobordisms, $(W,F) : (X,g) \to (Y,h)$ and $(V,G): (Y^\prime, h^\prime) \to (P,j)$ glued along a $B$-isomorphism $\psi :(Y,h) \to (Y^\prime,h^\prime)$, we have 
$\tau((W,F)\amalg_\psi (V,G))= \tau(V,G)\tau(\psi)\tau(W,F).$

1.  For the identity $B$-cobordism, $1_{(X,g)} = (I\times X, 1_g)$, we have 
$\tau( 1_{(X,g)}) = 1_{\tau(X,g)}.$

1.  For $B$-cobordisms $(W,F) : (X,g) \to (Y,h)$ and $(V,G) : (X^\prime,g^\prime) \to (Y^\prime,h^\prime)$ and $(P,J): \emptyset \to \emptyset$, some fairly obvious diagrams are commutative.

=--

+-- {: .num_remark }
###### Remark

These axioms are slightly different from those given in the original paper of Turaev in 1999.  The really significant difference is in axiom 4, which is weaker than as originally formulated, where any $B$-cobordism structure on $I \times X$ was considered as trivial.  The effect of this change is important as it is now the case that the HQFT is determined by the $(n+1)$-type of $B$, cf. ([Rodrigues 03](#Rodrigues03)).

With the revised version of the axioms, it becomes possible to attempt to classify HQFTs with a given $n$ and $B$. Turaev did this in the original paper with $n = 2$ and $B$ an [[Eilenberg-MacLane space]], $K(G,1)$.  The results of Brightwell and Turner essentially gave the solution for $B$ a $K(A,2)$.

=--

## Examples

### 1+1 dimensional HQFTs with background a $K(G,1)$

If we look at the case $n= 1$ and with background an [[Eilenberg-Mac Lane space]] $K(G,1)$ for a [[discrete group]] $G$, then HQFTs correspond to [[crossed G-algebra|crossed G-algebras]], in much the same way that commutative [[Frobenius algebras]] correspond to [[2d TQFT]]s.  There the correspondence is given by a [[2d TQFT]], $Z$, corresponds to the [[Frobenius algebra]], $Z(S^1)$. This is because the circle $S^1$ is a [[Frobenius algebra]], sometimes called a  Frobenius object, in the category $Bord_2$ of 2d-[[cobordism]]s between 1-manifolds. 

In the case of HQFTs, the role of the circle is replaced by the family of  circles with characteristic maps to $B$.  Each one gives, combinatorially, a circle together with a labelling of the boundary by an element of $G$. (It does not seem to be known how to get a $G$-graded version of an abstract Frobenius object that will correspond to this situation, although this is probably not too hard to do.)


### Equivariant 

In ([Moore-Segal 06](#MooreSegal06)) are discussed $G$-[[equivariant TFT]]s and it is shown that they naturally correspond to a simple case of Turaev's HQFTs.  They relate (1+1) equivariant TFTs to Turaev's [[crossed G-algebras]] (which they call Turaev algebras).


## History

The original definition is due to [[Graeme Segal]], who introduced them under the term _[[elliptic objects]]_.
Specifically, in [Segal 88](#Segal88), we read in §6:

> 6\. Speculation about the definition of elliptic cohomology

> For any space $X$ let $\mathcal{P}_X$ be the category
whose objects are the points of $X$ and whose morphisms from $x_0$ to $x_1$ are the paths in $X$ from $x_0$ to $x_1$,
two such paths being identified if they differ only by reparametrization.
A functor from $\mathcal{P}_X$ to finite dimensional vector spaces is essentially the same thing as a vector bundle on $X$ with a connection.
(The functor must be continuous in a suitable sense.)
It is well known how K-theory is constructed from such objects.

> I have described elsewhere [23] a category $\mathcal{C}$
whose objects are all compact oriented one-dimensional manifolds,
and whose morphisms from $S_0$ to $S_1$ are pairs $(\Sigma,\alpha)$,
where $\Sigma$ is a Riemann surface with boundary $\partial\Sigma$,
and $\alpha$ is an isomorphism between $\partial X$ and $S_1-S_0$.
Two pairs $(\Sigma,\alpha)$, $(\Sigma',\alpha')$ are identified if they are isomorphic.
For any space $X$ one can now define a category $\mathcal{C}_X$.
Its objects are pairs $(S,s)$, where $S$ is an object of $\mathcal{C}$ and $s \colon S \to X$ is a map.
Its morphisms from $(S_0,s_0)$ to $(S_1,s_1)$ are triples $(\Sigma,\alpha,\sigma)$,
where $(\Sigma,\alpha)\colon S_0 \to S_1$ is a morphism in $\mathcal{C}$,
and $\sigma\colon\Sigma\to X$ is a map compatible with $(s_O,s_1)$.
The category $\mathcal{C}_X$ is a natural analogue of the category $\mathcal{P}_X$ which gives rise to vector bundles.

> It is appropriate to consider functors from $\mathcal{C}$ to the category $\mathcal{V}$ of topological vector spaces and trace-class maps.
If such a functor $E$ is holomorphic in the natural sense then $E(S^1)$ is a positive energy representation of $Diff(S^1)$ of finite type.
More precisely, as is familiar in the representation theory of $Diff(S^1)$,
one must consider projective representations of $\mathcal{C}$ of some definite positive integral level $k$.
Imposing a further condition — the contraction condition below — on the functor $E$ ensures that the character of $E(S^1)$ is a modular form of weight $k$.

> Now let us define an elliptic object of level $k$ on $X$
as a projective functor $E\colon\mathcal{C}_X\to \mathcal{V}$ of level $k$ which is holomorphic and satisfies the contraction condition.
Such an object consists of an infinite dimensional vector bundle on the loop space $\mathcal{L}X$, equivariant under $Diff(S^1)$,
together with some additional data amounting to a kind of connection.
The primary example is the spin bundle of $\mathcal{L}X$, which is defined when $X$ is a spin manifold with $p_1=0$.

> I have nothing precise to say about elliptic objects,
but it seems to me quite likely that the objects of each level lead to an interesting cohomology theory,
and that the theories for different levels are related by “Bott maps”.
That would fit in well with Theorem (5.3), for just as elements of $K(B G)$ are
elated to flat bundles, so elements of $Ell^*(B G)$ seem to be related to flat elliptic objects,
i.e. ones such that the operator associated to $(\Sigma,\alpha,\sigma)$ depends on $\sigma$ only up to homotopy, and is therefore a homomorphism $\pi_1(\Sigma)\to G$.

> I should mention that the category $\mathcal{C}$ can be modified by equipping the Riemann surfaces $\Sigma$ with chosen spin structures.
That is certainly needed to obtain genuine elliptic cohomology.

> Finally I return to the “contraction property”.
This is motivated by the path-integral point of view.
If a surface $\Sigma$ is a morphism from $S$ to itself
then the trace of the operator $E(\Sigma)\colon E(S)\to E(S)$ associated to $\Sigma$
must depend only on the _closed_ surface $\check\Sigma$ obtained by attaching the two boundary pieces of $\Sigma$ to each other.
Thus if $\Sigma_\tau$ is the annulus $\{z \in \mathbf{C} \mid |e^{i\tau}|\le |z|\le 1\}$ then $\check\Sigma_\tau\cong \check\Sigma_{\tau'}$, when $\tau'=-1/\tau$,
and therefore the trace of $E(\Sigma_\tau)$ is invariant under $\tau\mapsto -1/\tau$.

> Brylinski [9] has proposed a similar approach to elliptic cohomology.

> Postscript.
After giving this talk, I learnt of the work [29] 1 which gives a good account of the Dirac operator on loop space from the path integral point of view.


##  References

The original definition is due to [[Graeme Segal]] (who introduced them under the name (flat) _[[elliptic objects]]_), see §6 of

* {#Segal88} [[Graeme Segal]], _Elliptic cohomology (after Landweber–Stong, Ochanine, Witten, and others)_, Séminaire Bourbaki, 40e année, 1987–88, No. 695 ([numdam:SB_1987-1988__30__187_0](http://www.numdam.org/item/?id=SB_1987-1988__30__187_0))

These ideas were further developed in

* {#FreedQuinn1991} [[Daniel S. Freed]], [[Frank Quinn]], _Chern-Simons Theory with Finite Gauge Group_, [arXiv:hep-th/9111004](https://arxiv.org/abs/hep-th/9111004).

The theory of HQFTs was developed in

*  {#Turaev99} [[Vladimir Turaev]], _Homotopy field theory in dimension 2 and group-algebras_ ([arXiv:math.QA/9910010](http://arxiv.org/abs/math.QA/9910010))

* {#Turaev00} [[Vladimir Turaev]], _Homotopy field theory in dimension 3 and crossed group-categories_ ([arXiv:math.GT/0005291](http://arxiv.org/abs/math.GT/0005291)). 

* V. Turaev, Homotopy Quantum Field Theory, Tracts in Mathematics 10, (with Appendices by Michael Muger and Alexis Vurelizier), European Mathematical Society, June 2010.

* {#BrightwellTurner00} M. Brightwell and P. Turner, _Representations of the homotopy surface category of a simply connected space_, J. Knot Theory and its Ramifications, 9 (2000), 855--864. 

* {#Rodrigues03} G. Rodrigues, _Homotopy Quantum Field Theories and the Homotopy Cobordism Category  in Dimension 1 + 1_, J. Knot Theory and its Ramifications, 12 (2003) 287--317 ([arXiv:math.QA/0105018](http://arxiv.org/abs/math.QA/0105018)). 

* [[T. Porter]] and V. Turaev, Formal Homotopy Quantum Field Theories, I: Formal Maps and Crossed $C$-algebras, Journal of Homotopy and Related Structures 3(1), 2008, 113--159. ([arXiv:math.QA/0512032](http://arxiv.org/abs/math.QA/0512032)).

* [[T. Porter]], Formal Homotopy Quantum Field Theories II: Simplicial Formal Maps, in Cont. Math. 431, p. 375 - 404 (Streetfest volume: Categories in Algebra, Geometry and Mathematical Physics - edited by A. Davydov, M. Batanin, and M. Johnson, S. Lack, and A. Neeman) ([arXiv:math.QA/0512034](http://arxiv.org/abs/math.QA/0512034))

A treatment of HQFTs that includes some details of the links with TQFTs is given in [[HQFT-XMenagerie.pdf|HQFTs meet the Menagerie:file]], which is a set of notes prepared by [[Tim Porter]] for a school and workshop in Lisbon, Feb. 2011.

Related ideas are discussed in

* {#MooreSegal06} [[Greg Moore]], [[Graeme Segal]], _D-branes and K-theory in 2D topological field theory_ ([arXiv:hep-th/0609042](http://arxiv.org/abs/hep-th/0609042))


[[!redirects HQFTs]]

[[!redirects homotopy quantum field theory]]
[[!redirects homotopy quantum field theories]]