
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### AQFT
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{: toc}

## Definition

The category of **von Neumann algebras** (also known as **W\*-algebras**)
is the [[subcategory]] of the category of [[C*-algebra|C*-algebras]]
consisting of C\*-algebras that admit a predual and morphisms of C\*-algebras that admit a predual.

More precisely, a von Neumann algebra is a C\*-algebra $A$
such that there exits a [[Banach space]] $V$ (a **predual**)
whose dual Banach space $V^*$ is isomorphic to the underlying Banach space of $A$.
Similarly, a morphism of von Neumann algebras $f\colon A\to B$
is a morphism of C\*-algebras such that there exists a
morphism of Banach spaces $V\to W$ whose dual is isomorphic to the underlying morphism of Banach spaces of $f$.

In the above definition a Banach space is a complex Banach space
and a morphism of Banach spaces is a short map (linear map of norm at most 1).
By a C\*-algebra we mean a complex unital C\*-algebra,
and by a morphism of C\*-algebras we mean a unital morphism.

## Sakai's theorem and properties of preduals

Sakai's theorem states that preduals considered in the above definition
are necessarily unique.
More precisely, given a von Neumann algebra $A$
we consider the category whose objects are pairs $(V,f)$,
where $V$ is a Banach space and $f\colon V^*\to A$ is an isomorphism
of Banach spaces.  A morphism from $(V,f)$ to $(W,g)$
is a morphism $h\colon V\to W$ of Banach spaces
such that $fh^*=g$.

Sakai's theorem then states that in the above category
there is exactly one morphism
between any pair of objects, which is necessarily an isomorphism.
In particular, the category of preduals is canonically isomorphic
to the [[terminal category]].

Sakai's theorem can be extended to morphisms of von Neumann algebras.
Thus preduals of von Neumann algebras and their morphisms
are unique up to a unique isomorphism, in particular we can talk
about [[the]] predual of a von Neumann algebra and [[the]] predual
of a morphism of von Neumann algebras.

The weak topology induced on a von Neumann algebra by its predual
is called the **ultraweak topology**.
The role of the ultraweak topology for von Neumann algebras
is analogous to the role of the norm topology for C\*-algebras.
In particular, morphisms of von Neumann algebras are precisely
those morphisms of C\*-algebras that are continuous
in the ultraweak topology.

Consider the dual space $V$ of a von Neumann algebra $A$ equipped
with the ultraweak topology.
The [[topological vector space]] $V$ canonically embeds
into the dual of $A$ as a Banach space, the embedding map being
induced by the canonical continuous map from $A$
equipped with the norm topology to $A$
equipped with the ultraweak topology.
Thus $V$ is also a Banach space.
There is a canonical morphism of Banach spaces from $A$ to $V^*$
given by evaluating an element of $V$ on the given element of $A$.
This morphism is in fact an isomorphism, hence $V$ is the predual of $A$.
In other words, the predual of a von Neumann algebra is canonically
isomorphic to its dual in the ultraweak topology.
Similarly, the predual of a morphism of von Neumann algebras
is canonically isomorphic to its dual in the ultraweak topology.

## Elementary examples

The easiest example of a von Neumann algebra is given by the C\*-algebra $B(H)$
of bounded operators on a complex [[Hilbert space]] $H$.
The predual can be canonically identified with the Banach space
of [[trace class operator|trace class operators]].

Any C\*-subalgebra of $B(H)$ closed in the ultraweak topology
is again a von Neumann algebra.

## Properties of morphisms of von Neumann algebras

## W\*-categories

## Modules over von Neumann algebras

## Bimodules over von Neumann algebras and Connes fusion

## Modular algebra and Tomita-Takesaki theory

* [[modular theory]]

## Gelfand duality for commutative von Neumann algebras

## Relevance

The [[Gelfand-Naimark theorem|Gel'fand–Naimark theorem]] states that there is a contravariant [[equivalence of categories|equivalence]] between the [[category]] of commutative von Neumann algebras and the category of localizable [[measurable space|measurable spaces]]; that is, the [[opposite category]] of one is equivalent to the other. See [Relation to Measurable Spaces](#RelationToMeasureSpaces) below. General von Neumann algebras are seen then as a 'noncommutative' measurable spaces in a sense analogous to [[noncommutative geometry]].

The importance of von Neumann algebras for ([[higher category theory|higher]]) [[category theory]] and topology lays in the evidence that von Neumann algebras are deeply connected with the low dimensional [[quantum field theory]] (2d [[CFT]], [[TQFT]] in low dimensions, inclusions of [[von Neumann algebra factor|factor]]s, [[quantum group]]s and [[knot theory]]; [[elliptic cohomology]]: works of Wenzl, Vaughan Jones, Anthony Wasserman, Kerler, Kawahigashi, Ocneanu, Szlachanyi etc.). 

The highlights of their structure theory include the results on classification of [[von Neumann algebra factor|factors]] ([[Alain Connes]], 1970s) and theory of inclusions of subfactors (V. Jones). (Hilbert) [[bimodule]]s over von Neumann algebras have a remarkable tensor product due Connes ([[Connes fusion]]). Following Segal's manifesto

* Graeme Segal, _Elliptic cohomology (after Landweber-Stong, Ochanine, Witten, and others)_. S&#233;minaire Bourbaki, Vol. 1987/88.  Ast&#233;risque  No. 161-162  (1988), Exp. No. 695, 4, 187--201 (1989).

and its update

* [[Graeme Segal]], _What is an elliptic object?_  Elliptic cohomology,  306--317, London Math. Soc. Lecture Note Ser., 342, Cambridge Univ. Press, Cambridge, 2007. 

on hypothetical connections between [[CFT]] and [[elliptic cohomology]], Stolz and Teichner have made a case for a role von Neumann algebras seem to play in a partial realization of that program:

* [[Stefan Stolz]] and [[Peter Teichner]], _What is an elliptic object?_ ([pdf](http://math.berkeley.edu/~teichner/Papers/Oxford.pdf))

See also the [Wikipedia entry](http://en.wikipedia.org/wiki/Von_Neumann_algebra) entry for more on von Neumann algebras and a list of references and links.

## General

The _[[bicommutant theorem]]_ (as known as the _double commutant theorem_ , or _von Neumann's double commutant theorem_ ) is the following result. 

Let $A \subseteq B(H)$ be a sub-[[star-algebra]] of the [[C-star algebra]] of [[bounded linear operator|bounded linear operators]] on a [[Hilbert space]] $H$. Then $A$ is a [[von Neumann algebra]] on $H$ if and only if $A = A''$, where $A'$ denotes the [[commutant]] of $A$. 

Notice that the condition of $A$ being a von Neumann algebra (being closed in the [[weak operator topology]]; "weak" here can be replaced by "strong", "ultrastrong", or "ultraweak" as described in [[operator topology]]), which is a [[topology|topological]] condition, is by this result equivalent to an algebraic condition (being equal to its bicommutant).  

## Relation to measure spaces
 {#RelationToMeasureSpaces}

The [[Gelfand-Naimark theorem|Gel'fand–Naimark theorem]] states that the category of [[localizable measurable spaces]] is contravariantly [[equivalence of categories|equivalent]] to (that is equivalent to the [[opposite category|opposite]] of) the category of commutative von Neumann algebras.  As such, arbitrary von Neumann algebras may be interpreted as 'noncommutative' measurable spaces in a sense analogous to [[noncommutative geometry]].


## Topics of interest for the understanding of AQFT

This paragraph will collect some facts of interest for the aspects of [[AQFT]].

In this paragraph $\mathcal{M}$ will always be a von Neumann algebra acting on a [[Hilbert space]] $\mathcal{H}$ with [[commutant]] $\mathcal{M}'$.

### Vectors

+-- {: .un_defn}
###### Definition

A [[vector]] $x \in \mathcal{H}$ is a **[[cyclic vector]]** if $\mathcal{M}x$ is dense in $\mathcal{H}$.

=--

+-- {: .un_defn}
###### Definition

A [[vector]] $x \in \mathcal{H}$ is a **[[separating vector]]** if $M(x) = 0$ implies $M = 0$ for all $M \in \mathcal{M}$.

=--


+-- {: .un_theorem}
###### Theorem

The notions of cyclic and separating are dual with respect to the commutant, that is a vector is cyclic for $\mathcal{M}$ iff it is separating for $\mathcal{M}'$.

=--


### Projections in von Neumann algebras

One crucial feature of von Neumann algebras is that they contain 
"every projection one could wish for": there are three points that make this statement precise:

* the linear combinations of projections are norm dense in a von Neumann algebra

* [[Gleason's theorem]]

* Murray--von Neumann classification of [[von Neumann algebra factor|factors]] 

#### Projections are norm dense

First let us note that every element $A$ of a von Neumann algebra can trivially be written as a linear combination of two selfadjoint elements:
$$
A = \frac{1}{2} (A + A^*) + i\frac{1}{2i} (A - A^*)
$$

Then, by the [[spectral theorem]] every selfadjoint element A is represented by it's spectral measure E via
$$
A = \integral_{-\|A\|}^{\|A\|} \lambda E(d\lambda)
$$
The integral converges in norm to A and all spectral projections are elements of the von Neumann algebra. It immediatly follows that the set of finite sums of multiples of projections is norm dense in every von Neumann algebra. 

#### Gleason's theorem {#GleasonsTheorem}

See [[Gleason's theorem]].

#### Murray--von Neumann classification of factors 
To be done...

### Miscellaneous

* [[split inclusion of von Neumann algebras]]

## Remarks

* W\*-algebras should not be confused with W-algebras in (logarithmic) conformal field theory.

* Some authors use the term "von Neumann algebra" (as opposed to the term "W\*-algebra") for what we call
here a (faithful) module over a von Neumann algebra.
Similarly, the term "spatial morphism of von Neumann algebras" may be used
to refer to a morphism of such modules.
The [[nPOV]] dictates that a clear distinction between
the categories of algebras and modules must be maintained,
in particular, modules should not be confused with algebras.
Hence we stick to the modern terminology, which also seems
to be preferred in new papers on von Neumann algebras,
see for example [arXiv:1110.5671v1](http://arxiv.org/abs/1110.5671).


## Related concepts

* [[von Neumann algebra factor]]

## References
 {#References}

* [[Jacob Lurie]], _von Neumann algebras_, lecture series (2011) ([web](http://www.math.harvard.edu/~lurie/261y.html))

[[!redirects W*-algebra]]
[[!redirects W*-algebras]]
[[!redirects W* algebra]]
[[!redirects W* algebras]]
[[!redirects W-star-algebra]]
[[!redirects W-star-algebras]]
[[!redirects W-star algebra]]
[[!redirects W-star algebras]]
[[!redirects von Neumann algebra]]
[[!redirects von Neumann algebras]]
[[!redirects von Neumann-algebra]]