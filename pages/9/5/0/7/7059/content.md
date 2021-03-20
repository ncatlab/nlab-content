
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

_Cohesive homotopy type theory_ is an [[axiom|axiomatic]] [[theory]] of [[higher geometry]], the pairing of [[geometry]] in general and of [[differential geometry]] in particular with [[homotopy theory]].
The _[[objects]]_ or _[[types]]_ that it describes are _[[cohesive topos|cohesive]] [[homotopy types]]_, hence [[cohesive ∞-groupoids]], such as for instance [[smooth ∞-groupoids]]. See also at _[[motivation for cohesive toposes]]_ for a non-technical discussion.

To the extent that plain [[homotopy type theory]] is a formalization of [[homotopy theory]] in that it is the [[internal language of an (∞,1)-topos]], _cohesive_ homotopy type theory is the [[internal logic|internal language]] of a _[[cohesive (∞,1)-topos]]_.

One way to arrive at cohesive homotopy type theory is to start with the external axioms for [[cohesive toposes|cohesion]] on a given [[topos]] in terms of an [[adjoint quadruple]] of functors _on_ the given [[topos]] and attempt to formulate them instead in the [[internal logic|internal]] [[Mitchell-Bénabou language|Mitchell-Bénabou]] [[type theory]] language of the topos. This fails, since for formulating the [[reflective subcategories]] of [[discrete objects]] and [[codiscrete objects]] internally one needs instead of the [[type of propositions]] a full [[type of types]], as exists only in [[homotopy type theory]]. Passing to this, the axioms for cohesion can be formulated ([Shulman](#ShulmanInternalizing)) and are automatically that of [[cohesive (∞,1)-topos|homotopy cohesion]].


## The Axioms
  {#TheAxioms}

We discuss the formulation in [[homotopy type theory]] of the [internal axioms](http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos#InternalDefinition) on a [[cohesive (∞,1)-topos]].

Cohesive homotopy type theory is a [[modal type theory]] which adds to [[homotopy type theory]] an [[adjoint triple]] of [[modalities]]

$$
  &#643; \dashv \flat \dashv \sharp
$$

called 

* [[shape modality]] $\dashv$ [[flat modality]] $\dashv$ [[sharp modality]],

where $&#643;$ and $\sharp$ are [[idempotent monad|idempotent]] [[monads (in computer science)|monads]] and where $\flat$ is an idempotent [[comonad]], subject to some compatibility condition.

### A) Codiscrete objects

**Axiom A.** _The ambient [[homotopy type theory]] has a 
[[geometric embedding|left-exact]] [[reflective sub-(∞,1)-category]],
to be called the [[base (∞,1)-topos]] "of [[codiscrete objects]]"._

Coq code at [Codiscrete.v](https://github.com/mikeshulman/HoTT/blob/master/Coq/Subcategories/Codiscrete.v)



We write

$$
  X \to \sharp X
$$

for the [[reflector]] into codiscrete objects. 

The homotopy type theory of the [[codiscrete objects]] we call the _external_ theory.


### B) Discrete objects

**Axiom B.** There is also a [[coreflective sub-(∞,1)-category]] of
_[[discrete objects]]_ such that with the codiscrete reflection
it makes the ambient theory that of a [[local (∞,1)-topos]].

[[Coq]] code at [LocalTopos.v](https://github.com/mikeshulman/HoTT/blob/master/Coq/Subcategories/LocalTopos.v).

The coreflector from discrete objects we write

$$
  \flat A \to A
  \,.
$$

### C) Cohesion

**Axiom C** The discrete objects are also reflective, the reflector is [[left adjoint]] to the coreflector and preserves [[product types]].

[[Coq]] code at [CohesiveTopos.v](https://github.com/mikeshulman/HoTT/blob/master/Coq/Subcategories/CohesiveTopos.v).

We write 

$$
  X \to \Pi X
$$

for the reflector into [[discrete objects]].

## Example phenomena

Before looking at the consequences of the axioms formally, 
we mention some example phenomena to illustrate the meaning of the axioms.

### Geometric spaces and their cohesive homotopy types
 {#GeometricSpacesAndTheirHomotopyTypes}

We indicate one central aspect of geometric homotopy theory that is not visible in plain [[homotopy type theory]], but is captured by its cohesive refinement.

The standard [[interval]] $I = [0,1]$ in [[Top|topological spaces]]
plays two rather different roles, depending on what kind of
equivalence between spaces is considered. To make this more vivid,
it serves to think of $[0,1]$ as equipped 
even with its canonical structure
of a [[smooth manifold]] ([[manifold with boundary|with boundary]]).

The canonical map $I \to *$ to the [[point]] is certainly not
a [[diffeomorphism]], and from the point of view of
[[differential geometry]] the interval carries non-trivial structure.
Notably its endpoints $0,1 : I$ are not equivalent points ([[terms]])
in differential geometry, but are distinct. From the point of view of differential
geometry the interval is a [[homotopy n-type|homotopy 0-type]]
(has [[h-level]] 2) -- but one that is in some way equipped with geometric
structure.

This geometric structure, however, induces also a notion of 
_[[path groupoid|geometric paths]]_ in the interval, such that 
any two of its points are connected by such a path, after all.
In other words, one can form the smooth [[fundamental ∞-groupoid]]
$\Pi(I)$ of the interval and regard _that_ as a [[homotopy type]]
_without_ further geometric structure (a [[discrete ∞-groupoid]]). This $\Pi(I)$ is an _[[interval type]]_, while $I$ itself is not.

As such, the canonical map $\Pi(I) \to *$ is an [[equivalence]]
after all, namely a [[weak homotopy equivalence]]. Therefore,
after application of $\Pi$, what used to be a geometric 0-type
becomes a [[(-1)-groupoid|(-1)-type]] and actually a
[[(-2)-groupoid|(-2)-type]] ([[h-level]] 0) --  up to equivalence the [[interval type]], but without any geometry.

This latter property is what makes the interval important in bare
[[homotopy theory]], where it serves to model notions
such as [[cylinder objects]], [[left homotopies]], etc. The former
property, however, is what makes the interval important in [[geometry]], where it serves to model [[Cartesian spaces]], [[manifolds]], etc.

In cohesive homotopy type theory these two roles of the interval
can both be seen, via the reflective embedding of [[discrete objects]], 
and the transition between them is present, via the 
[[fundamental infinity-groupoid in a locally infinity-connected (infinity,1)-topos|fundamental ∞-groupoid reflector]] $\mathbf{\Pi}$.

Specifically, there is a [[model]] for 
[[cohesive (∞,1)-topos|homotopy cohesion]], called 
[[Smooth∞Grpd]], in which [[smooth manifolds]] 
([[manifold with boundary|with boundary]]) are 
[[full and faithful functor|fully faithfully embedded]],
where hence $I = [0,1]$ exists as a [[type]]
that behaves as the interval in [[differential geometry]],
and where $\mathbf{\Pi}(I)$ is equivalent to the [[unit type]].

More generally, in this model every [[smooth manifold]]
$X$ is a [[homotopy n-type|homotopy 0-type]]/[[0-truncated]]
object, but the type $\mathbf{\Pi}(X)$ is a [[discrete ∞-groupoid]]
whose [[homotopy type]] is that of the topological space underlying
$X$, as regarded in the 
[[model structure on topological spaces|standard]] [[homotopy category]] 
of topological spaces.

In particular, the smooth [[circle]] $S^1$ in this model is a 
[[0-truncated|0-type]] such that $\mathbf{\Pi}(S^1)$ is the
[[1-truncated|1-type]] $\mathbf{B}\mathbb{Z}$ (the [[delooping]]
[[groupoid]] of the [[integers]]).

One can turn this around and axiomatize a [[continuum]] [[line object]]
in cohesive homotopy type theory as a [[ring object]] 
$\mathbb{Z} \hookrightarrow \mathbb{A}^1$ such that 
$\mathbf{\Pi}(\mathbb{A}^1) \simeq *$.



## Structures in cohesive homotopy type theory
 {#Structures} 

We discuss implications of the axioms of cohesive homotopy type theory and go through the discussion of the various [[structures in a cohesive (∞,1)-topos]].

### Cohomology

For $X$ and $A$ two [[types]], the externalization $\sharp(X \to A)$ of the [[function type]] $X \to A$ is the _type of [[cocycles]]_ on $X$ with coefficients in $A$. Its [[h-level]] 2 [[truncated|truncation]] $\tau_0 \sharp(X \to Y)$ is the [[cohomology]] of $X$ with coefficients in $A$.

### Flat cohomology and local systems

We give the [[Coq]]-formalization of [Flat cohomology and local systems](http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+structures#FlatDifferentialCohomology).

For $A$ a [[type]], we say that [[cohomology]] with coefficients in 
$\flat A$ is _flat cohomology_. A [[cocycle]] [[term]] $c : \sharp(X \to \flat A)$ is called a [[local system]] of coefficients $A$ on $X$.

(...)

### de Rham cohomology

We give the [[Coq]]-formalization of [intrinsic de Rham cohomology](http://ncatlab.org/nlab/show/cohesive+%28infinity,1%29-topos+--+structures#deRhamCohomology).

Let $A = \mathbf{B}G$ be a [[0-connected|connected]] [[type]].

The [[homotopy fiber]] type of the coreflection $\flat \mathbf{B}G \to \mathbf{B}G$ we call the _de Rham coefficient type_ of $G$, denoted $\flat_{dR} \mathbf{B}G$. So there is a [[fiber sequence]]

$$
  \flat_{dR} \mathbf{B}G \to \flat \mathbf{B}G \to \mathbf{B}G
  \,.
$$

[[Coq]]-code:

    Require Import Homotopy Subtopos Codiscrete LocalTopos CohesiveTopos.

    Hypothesis BG : Type.
    Hypothesis BG_is_0connected : is_contr (pi0 BG).
    Hypothesis pt : BG.

    Definition flat_dR : #Type
      := ipullback (<nowiki>[[fun _:unit => pt]]</nowiki>) (from_flat ([BG])).

### Differential cohomology

We give the [[Coq]]-formalization of [Differential cohomology](http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+structures#DifferentialCohomology).

(...)

## Related concepts

* [[geometric homotopy type theory]]

* [[modal homotopy type theory]]

* [[stable homotopy type]]

* [[differential homotopy type theory]]

## References
 {#References}

A survey with discussion of applications to [[gauge theory]] and [[quantum field theory]] is at

* [[Urs Schreiber]], [[Mike Shulman]], _[[schreiber:Quantum gauge field theory in Cohesive homotopy type theory]]_ 

The formulation of [[cohesive topos|axiomatic cohesion]] on 1-[[categories]] is due to [[Bill Lawvere]], see [there](http://ncatlab.org/nlab/show/cohesive+topos#References) for a detailed bibliography.

The [[Coq]] formalization of [[cohesive (infinity,1)-topos|axiomatic homotopy cohesion]] is discussed in 

* {#ShulmanInternalizing} [[Mike Shulman]], _Internalizing the external, or The Joys of Codiscreteness_ ([blog post](http://golem.ph.utexas.edu/category/2011/11/internalizing_the_external_or.html))


A formalization in homotopy type theory with [[adjoint logic]] added is in 

* {#Shulman15} [[Mike Shulman]], _Brouwer's fixed-point theorem in real-cohesive homotopy type theory_, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

* {#LicataShulman} [[Dan Licata]], [[Mike Shulman]], _Adjoint logic with a 2-category of modes_, in _[Logical Foundations of Computer Science 2016](http://lfcs.info/lfcs-2016/)_ ([pdf](http://dlicata.web.wesleyan.edu/pubs/ls15adjoint/ls15adjoint.pdf), [slides](http://dlicata.web.wesleyan.edu/pubs/ls15adjoint/ls15adjoint-lfcs-slides.pdf))

See also

* {#Wellen18} [[Felix Wellen]], _[[schreiber:thesis Wellen|Cartan Geometry in Modal Homotopy Type Theory]]_ ([arXiv:1806.05966](https://arxiv.org/abs/1806.05966), [thesis pdf](http://www.math.kit.edu/iag3/~wellen/media/diss.pdf))

* [[David Jaz Myers]], _Good Fibrations through the Modal Prism_ ([arXiv:1908.08034v2](https://arxiv.org/abs/1908.08034v2))


In the [pseudocode](http://en.wikipedia.org/wiki/Pseudocode) formerly known as traditional mathematics, homotopy cohesion is discussed in

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ ([arXiv:1310.7930](http://arxiv.org/abs/1310.7930))

See also 

* [[Urs Schreiber]], _[[schreiber:Modern Physics formalized in Modal Homotopy Type Theory ]]_

* {#Shulman19} [[Mike Shulman]], _Comonadic modalities and cohesion_, talk at _[Geometry in Modal Homotopy Type Theory](http://felix-cherubini.de/modal-workshop.html)_, 2019 ([pdf slides](http://home.sandiego.edu/~shulman/papers/cmu2019a.pdf), [talk recording](https://youtu.be/GA93Hjh-Alk))

Formalization of the shape/flat-[[fracture square]] ([[differential cohomology hexagon]]):

* [[David Jaz Myers]], _Modal Fracture of Higher Groups_,  talk at _[CMU-HoTT Seminar](https://www.cmu.edu/dietrich/philosophy/hott/seminars/index.html), 2021 ([pdf](http://davidjaz.com/Talks/CMU_March_2021.pdf), [[MyersModalFracture2021.pdf:file]])


[[!redirects cohesive homotopy type theories]]

[[!redirects cohesive homotopy type]]
[[!redirects cohesive homotopy types]]
