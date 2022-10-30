

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
The _[[objects]]_ or _[[types]]_ that it descrives are _[[cohesive topos|cohesive]] [[homotopy types]]_, hence [[cohesive ∞-groupoids]], such as for instance [[smooth ∞-groupoids]].

To the extent that plain [[homotopy type theory]] is a formalization of [[homotopy theory]] in that it is the [[internal language of an (∞,1)-topos]], _cohesive_ homotopy type theory is the [[internal logic|internal language]] of a _[[cohesive (∞,1)-topos]]_.

One way to arrive at cohesive homotopy type theory is to start with the external axioms for [[cohesive toposes|cohesion]] on a given [[topos]] in terms of an [[adjoint quadruple]] of functors _on_ the given [[topos]] and attempt to formulate them instead in the [[internal logic|internal]] [[Mitchell-Bénabou language|Mitchell-Bénabou]] [[type theory]] language of the topos. This fails, since for formulating the [[reflective subcategories]] of [[discrete objects]] and [[codiscrete objects]] internally one needs instead of the [[type of propositions]] a full [[type of types]], as exists only in [[homotopy type theory]]. Passing to this, the axioms for cohesion can be formulated ([Shulman](#ShulmanInternalizing)) and are automatically that of [[cohesive (∞,1)-topos|homotopy cohesion]].

## The Axioms

We discuss the formulation in [[homotopy type theory]] of the [internal axioms](http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos#InternalDefinition) on a [[cohesive (∞,1)-topos]].

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


## Structures in cohesive homotopy type theory

We discuss implications of the axioms of cohesive homotopy type theory and go through the discussion of the various [[structures in a cohesive (∞,1)-topos]].

### Cohomology

For $X$ and $A$ two [[types]], the externalization $\sharp(X \to A)$ of the [[function type]] $X \to A$ is the _type of [[cocycles]]_ on $X$ with coefficients in $A$. Its [[h-level]] 2 [[truncated|truncation]] $\tau_0 \sharp(X \to Y)$ is the [[cohomology]] of $X$ with coefficients in $A$.

### Flat cohomology and local systems

For $A$ a [[type]], we say that [[cohomology]] with coefficients in 
$\flat A$ is _flat cohomoloy_. A [[cocycle]] [[term]] $c : \sharp(X \to \flat A)$ is called a [[local system]] of coefficients $A$ on $X$.

### de Rham cohomology

We give the [[Coq]]-formalization of [intrinsic de Rham cohomology](http://ncatlab.org/nlab/show/cohesive+%28infinity,1%29-topos+--+structures#deRhamCohomology).

Let $A = \mathbf{B}G$ be a [[0-connected|connected]] [[type]].

The [[homotopy fiber]] type of the coreflection $\flat \mathbf{B}G \to \mathbf{B}G$ we call the _de Rham coefficient type_ of $G$, denoted $\flat_{dR} \mathbf{B}G$. So there is a [[fiber sequence]]

$$
  \flat_{dR} \mathbf{B}G \to \flat \mathbf{B}G \to \mathbf{B}G
  \,.
$$

Coq-code:

    Require Import Homotopy Subtopos Codiscrete LocalTopos CohesiveTopos.

    Hypothesis BG : Type.
    Hypothesis BG_is_0connected : is_contr (pi0 BG).
    Hypothesis pt : BG.

    Definition flat_dR : #Type
      := ipullback ([[fun _:unit => pt]]) (from_flat ([BG])).

### Differential cohomology

(...)

## References

The [[Coq]]-[[homotopy type theory]] formalization is discussed in 

* [[Mike Shulman]], _Internalizing the external, or The Joys of Codiscreteness_ ([blog post](http://golem.ph.utexas.edu/category/2011/11/internalizing_the_external_or.html))
 {#ShulmanInternalizing}

The Coq-code library is at 

* [[Mike Shulman]], _[HoTT/Coq/Subcatgeories](https://github.com/mikeshulman/HoTT/tree/master/Coq/Subcategories)_

In the [pseudocode](http://en.wikipedia.org/wiki/Pseudocode) formerly known as traditional mathematics, homotopy cohesion is discussed in

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

