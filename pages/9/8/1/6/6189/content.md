
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--



# Reductions, deformations, and resolutions in the service of physics 
* table of contents
{:toc}


## Outline ##

These aim of these notes is to summarize the various mathematical
structures and constructions employed in physics to build models of
[[classical field theory|classical]] and [[quantum field theories]]. To avoid the (yet non-existent)
rigorous construction of non-linear (interacting) field theories,
non-linearities are treated as formal perturbations. Theories with [[gauge theory|gauge invariance]] ([[first class constraints]]) are treated within the [[BV-BRST formalism]].

### Reductions, deformations, resolutions ###

There are multiple operations on classical and quantum field theories
that produce new ones. I roughly classify them into three kinds. These
terms are not meant to be rigorously defined or taken literally. They
mostly reflect how these operations are viewed in the physics
literature.

* **reductions**
:	These are easy/natural operations that are essentially uniquely
:	defined. The uniqueness may not always be mathematically precise, but
:	precision can be achieved by considering extra physical input.
:	Suggestive examples are _differentiation_ and _computing cohomology_.
* **deformations**
:	These are generally difficult operations inverse to a reduction, that
:	are themselves essentially uniquely defined. Uniqueness is considered
:	in the same sense as above. A suggestive examples is _integration_.
* **resolutions**
:	These are operations inverse to a reduction that are not uniquely
:	defined and involve making significant choices in their application.
:	Suggestive examples are _solving underdetermined equations_ and
:	_choosing a resolution_ in homological algebra.

The relevant examples that will appear in these notes are the following.
A solid arrow represents a reduction, while a dashed arrow represents
the inverse deformation or resolution, in the senses described above.

+--{: style="text-align:center"}
[[!include reductions deformations resolutions in physics > cq-arr]]
=--

The transition to the _[[classical limit]]_ corresponds to taking the
limit $\hbar\to0$, which is a parameter explicitly appearing in all
physically relevant quantum systems. The inverse operation is
_quantization_, which corresponds to the mathematical field
technically called [[deformation quantization]].

+--{: style="text-align:center"}
[[!include reductions deformations resolutions in physics > ln-arr]]
=--

Explicit solutions or other kinds of information is readily available
for linear field theories. Thus, often, the first step to understanding a
non-linear field theory is to consider its _linearization_. The
inverse operation of deforming the linear theory with a _non-linear
perturbation_ is often very difficult and thus considered in the physics
literature mostly at the level of formal power series in the
perturbation parameter.

+--{: style="text-align:center"}
[[!include reductions deformations resolutions in physics > pg-arr]]
=--

Many physical theories are difficult to describe without introducing
extra/non-physical/redundant so-called [[gauge theory|gauge degrees of freedom]] and at
the same time so-called [[gauge symmetry]] acting on them. However, given such a description, the physical theory must be recovered from the
_quotient by gauge transformations_. The description involving
gauge degrees of freedom is highly non-unique, but a particularly
convenient (though still not unique) one is provided by the
_BV-BRST_ resolution.

### Summary of construction ###

The operations described above can be used as the axes of a
three-dimensional space, inhabited by what can be called the
resolution-deformation-reduction cube of [[quantization]]. Note that [[gauge fixing]] can be considered as one of the (non-uniquely defined) steps of the BV-BRST construction.

+--{: style="text-align:center"}
[[!include reductions deformations resolutions in physics > bv-axes]]
=--

One corner of the cube corresponds to some classical, non-linear,
physical theory. The goal of quantization is to jump to the corner with
the quantum version of this theory. This is difficult to do directly
because of the non-linearity and when gauge degrees of freedom are
present. The usual procedure is then to construct the remaining
auxiliary vertices of the cube and to take the indirect path, indicated
in pale blue. The meaning of the solid and dashed lines is the same as
above.

+--{: style="text-align:center"}
[[!include reductions deformations resolutions in physics > bv-diag]]
=--

### Scope and contents ###

* Classical and quantum mechanics
:	* algebraic structure of [[classical mechanics]]
:	* algebraic structure of [[quantum mechanics]]
:	* [[classical limit]] and ([[deformation quantization|deformation]]) [[quantization]]
* Classical and quantum field theory
:	* geometry of [[space-time]]
:	* algebraic and geometric structure of [[classical field theory]]
:	* algebraic and geometric structure of [[quantum field theory]]
* Construction of field theories (simplified)
:	* space-time, field content, dynamics
:	* [[phase space|(covariant) phase space]]
:	* algebra of [[observables]]
:	* (deformation) [[quantization]]
* Examples of field theories
:	* [[scalar field]] (Klein-Gordon)
:	* vector field ([[electromagnetism|Maxwell]], [[Yang-Mills theory|Yang-Mills]])
:	* [[gravity]] (general relatvity)
:	* [[spinor]] field (Dirac)
* [[fermion|Fermi fields]] and [[supergeometry]]
* [[gauge invariance|Gauge invariance]]/degeneracy
:	* [[Noether's theorem|Nöther's second theorem]]
:	* algebra and geometry of [[gauge transformation]]s
:	* physical theory from quotient by gauge
* [[BV-BRST formalism|BV-BRST construction]] of gauge theories
:	* BV-BRST (Koszul-Tate) resolution of physical theory
:	* [[gauge fixing]], well-posedness, [[Poisson algebra|Poisson structure]]
:	* [[cohomology]]
* BV-BRST, (deformation) quantization and [[quantum anomaly|gauge anomalies]]
