+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

# Cubical-type model categories

* table of contents
{: toc}

## General

A cubical-type model category is a [[model category]] [[mathematical structure|structure]] whose fibrations are defined by lifting against a generalized form of open box inclusions. 

The term is not a precise technical one, but refers to model structures arising from a family of constructions, the first of which is due to [Sattler (2017)](#sattlerEEP).
These constructions are motivated by [[cubical type theory]] and can in particular be applied in certain [[categories]] of [[cubical sets]].

## Outline

The inputs to the construction are

1. a [[finitely complete]] and [[finitely cocomplete]] [[category]] $\mathcal{E}$;

1. a monomorphism $p_{\mathbb{F}} \colon 1 \to \mathbb{F}$ in $\mathcal{E}$;

1. an [[premodel category#AdjointFunctorialCylinder|adjoint functorial cylinder]]
\begin{tikzcd}
Id_{\mathcal{E}} \ar[dr,"id"{below left}] \ar[r,"\delta_0"] & C \ar[d,"\epsilon"] & \ar[l,"\delta_1"{above}] Id_{\mathcal{E}} \ar[dl,"id"{below right}] \\
& Id_{\mathcal{E}}
\end{tikzcd}
with right adjoint $P$ on $\mathcal{E}$.

The map $p_{\mathbb{F}}$ is intended as a classifier for the [[cofibrations]], while the cylinder is used to define [[fibrations]] and [[acyclic cofibrations]].
The construction proceeds by building a [[premodel category|cylindrical premodel category]] and then showing that it forms a model category.

The cofibrations, fibrations, and weak equivalences can be defined using just the data above, but further conditions on $\mathcal{E}$, $p_{\mathbb{F}}$, and $C \dashv P$ are required to construct factorizations, to check that the premodel structure is cylindrical, and to prove 2-out-of-3 for weak equivalences.

The step from a premodel structure to a model structure is mediated by the following definition and proposition.

+-- {: .num_prop}
###### Definition

A [[premodel category]] has the **fibration extension property** if for every fibration $f \colon Y \to X$ and acyclic cofibration $i \colon X \to X'$, there is a pullback square

\begin{tikzcd}
  Y \ar[dr,phantom,"\lrcorner"{near start}] \ar[d,two heads,"f"'] \ar[dashed,r] & Y' \ar[d,two heads,"f'"] \\
  X \ar[r,"i"'] & X'
\end{tikzcd}

in which $f'$ is a fibration.

=--

+-- {: .num_prop}
###### Proposition

Let $\mathcal{E}$ be a cylindrical premodel category in which all objects are cofibrant.
If $\mathcal{E}$ has the fibration extension property, then the class $W \coloneqq AF \circ AC$ has the 2-out-of-3 property (i.e., $\mathcal{E}$ is a model category).

=--

+-- {: .proof}
###### Proof

([Cavallo & Sattler 2022, Theorem 3.31](#CavalloSattler2022))

=--

The fibration extension property is then connected to the existence of fibrant classifiers for fibrations; see for example ([Awodey et al. 2024, Section 3.6](#ACCRS2024)).

## Definitions

### Cofibrations and acyclic fibrations

We first define the factorization system (AC,F).

+-- {: .num_prop}
###### Definition

A map is a **cofibration** when it can be written as a pullback of $p_{\mathbb{F}} \colon 1 \to \mathbb{F}$ in $\mathcal{E}$.

=--

+-- {: .num_prop}
###### Definition

A map in $\mathcal{E}$ is an **acyclic fibration** when it has the right lifting property against all cofibrations.

=--

+-- {: .num_prop}
###### Proposition

Assume $\mathcal{E}$ is a locally cartesian closed category and the cofibrations are closed under composition.
Then the cofibrations and acyclic fibrations define a weak factorization system.

=--

+-- {: .proof}
###### Sketch
We need to show that

* any morphism $f \colon Y \to X$ can be factored as a cofibration followed by an acyclic fibration;
* any map lifting against all trivial fibrations is a cofibration.

For the first point, regard $f$ as an object $(Y,f) \in \mathcal{E}/X$ in the slice over $X$.
Then we have $\sum_{\mathbb{F}} \prod_{p_{\mathbb{F}}} (Y,f) \in \mathcal{E}/X$, where $\sum_{\mathbb{F}}$ is the [[dependent sum]] along $\pi_0 \colon X \times \mathbb{F} \to X$ and $\prod_{p_{\mathbb{F}}}$ is the [[dependent product]] along $X \times p_{\mathbb{F}} \colon X \to X \times \mathbb{F}$.
When $p_{\mathbb{F}}$ is the subobject classifier, this is the [[partial map classifier]] for $(Y,f)$.
One may check that the map $\sum_{\mathbb{F}} \prod_{p_{\mathbb{F}}} (Y,f) \to X$ has the right lifting property against all cofibrations; this step uses the closure of cofibrations under composition.

By the [[Beck--Chevalley conditions]], we have a pullback square

\begin{tikzcd}
  Y \ar[dashed,d,"{ c }"'] \ar[dr,phantom,"{ \lrcorner }"{near start}] \ar[dashed,r] & 1 \ar[d,"{ p_{\mathbb{F}} }"] \\
  {\sum_{\mathbb{F}} \prod_{p_{\mathbb{F}}} (Y,f)} \ar[r,"{ \pi }"'] & \mathbb{F}
\end{tikzcd}

The map $c$ is a cofibration by construction.
One may check that the composite $Y \overset{c}{\to} \sum_{\mathbb{F}} \prod_{p_{\mathbb{F}}} (Y,f) \to X$ is $f$.

The second point follows from the [[retract argument]] after checking that the class of cofibrations is closed under [[retracts]].

=--

### Fibrations and acyclic cofibrations

Variations on the construction differ in their definition of the fibrations and acyclic fibrations.
We give the definition used in [Sattler (2017)](#sattlerEEP).

+-- {: .num_prop}
###### Definition

A map $f \colon Y \to X$ is a **fibration** when it has the right lifting property against the [[pushout-product#PushoutApplication|pushout application]] $\widehat{ev}(\delta_k, m)$ for all $k \in \{0,1\}$ and cofibrations $m$.
A map is a **trivial cofibration** when it has the left lifting property against the fibrations.

=--

The above definition is appropriate when the cylinder functor admits *connections* in the sense of [Gambino & Sattler (2017)]({#GambinoSattler2017}), which is related to the notion of [[connection on a cubical set]].
Other definitions are used in cases without connections; see for example ([Awodey 2023](#Awodey2023)).

Further assumptions on $\mathcal{E}$ and the cylinder are needed to construct the (trivial cofibration, fibration) factorizations using the [[small object argument]] or [[algebraic small object argument]]; see for example Sections 3 and 7 of ([Gambino & Sattler 2017]({#GambinoSattler2017})) respectively.
The algebraic route may be necessary to define the factorizations [[constructive mathematics|constructively]].

### Cylindricality

For the (cofibration, trivial fibration) weak factorization system to be [[premodel category#WFSCylindrical|cylindrical]], it is necessary to assume that the class of cofibrations is closed under pushout application $\widehat{ev}(\partial,-) \colon \mathcal{E}^{\mathbf{2}} \to \mathcal{E}^{\mathbf{2}}$.

For the premodel structure to be cylindrical, it then suffices to require that the cylinder functor admits a *symmetry*, meaning an isomorphism $C \circ C \cong C \circ C$ interacting with the cylinder structure in an appropriate way. See ([Sattler 2017, Remark 4.3](#sattlerEEP)).

### The Frobenius condition

The proofs of the fibration extension property require first establishing that the (trivial cofibration, fibration) [[weak factorization system]] satisfies the [[Frobenius condition#InWeakFactorizationSystems|Frobenius condition]].

A proof for a setting with connections can be found in ([Gambino & Sattler 2017](#GambinoSattler2017)).
Proofs for settings without connections can be found in ([Awodey 2023](#Awodey2023)), ([Hazratpour & Riehl 2024](#HazratpourRiehl2024)), and ([Barton 2024](#Barton2024)).

## Instances of the assumptions

A concrete application is to categories of [[cubical sets]], i.e. [[presheaves]] over a [[category of cubes]] $\Box$.

A simple and central choice for $\Box$ is the [[full subcategory]] of the category of [[posets]] $Pos$ on powers of $\mathbb{I} = (0 \lt 1)$. This is also the [[Lawvere theory]] of [[distributive lattices]].
The [[idempotent completion]] is the full subcategory of $Pos$ on finite lattices.

Other prominent examples are the Lawvere theories of [[de Morgan algebra|de Morgan]], [[Kleene algebra|Kleene]], and [[boolean algebra|boolean]] algebras.

For computational purposes we can take $\mathbb{F} \rightarrowtail \Omega$ to be the smallest lattice of subobjects containing the cylinder endpoints (the faces of cubes).
To get [[Cisinski model structures]] we can take $\mathbb{F} = \Omega$.
If we want the model to be effective, we also require that each [[proposition]] $\psi = 1$ with $\psi \in \mathbb{F}(I)$ is [[decidability|decidable]]. (This rules out taking $\mathbb{F} = \Omega$.)

## Equivalence with simplicial sets

One may wonder whether these model structures are equivalent to the [[classical model structure on simplicial sets]], i.e., whether they present classical [[homotopy theory]].

This is not the case for cartesian cubes; see [mailing-list](https://groups.google.com/d/msg/homotopytypetheory/RQkLWZ_83kQ/tAyb3zYTBQAJ). However, this model does form a Grothendieck [[(infinity,1)-topos]], because it satisfies the Giraud axioms. For deMorgan cubical sets the geometric realization is not a Quillen equivalence (because of the reversal map); the counterexample is the unit interval quotient by the symmetry); see [Sattler](#sattlerHIM). Whether they are equivalent by another map is not yet excluded.

A modified model structure for cartesian cubes, the _equivariant fibration_ model structure, does present classical homotopy theory ([Awodey, Cavallo, Coquand, Riehl & Sattler (2024)](#ACCRS2024)).
This model structure agrees with the [[test category|test model structure]] on cartesian cubical sets.

The model structure for cartesian cubes with one connection also presents classical homotopy theory ([Cavallo & Sattler (2022)](#CavalloSattler2022)).
In this case an explicit equivariance condition on fibrations is not required (but is automatically satisfied).
Again, the model structure agrees with the [[test category|test model structure]] on the same category.

The question whether the geometric realization for the cubical sets based on distributive lattices is an equivalence is still open, cf. also [Hackney and Rovelli](#hrInduced) and [Streicher and Weinberger](#swCuSi).


## References

Sattler's construction is in

* {#sattlerEEP} [[Christian Sattler]], *The equivalence extension property and model structures* &lbrack;[arXiv:1704.06911](https://arxiv.org/abs/1704.06911)&rbrack;

and some elements appear in the earlier paper

* {#GambinoSattler2017} [[Nicola Gambino]] and [[Christian Sattler]], _The Frobenius condition, right properness, and uniform ﬁbrations_, Journal of Pure and Applied Algebra **221** (2017). &lbrack;[doi:10.1016/j.jpaa.2017.02.013](https://dx.doi.org/10.1016/j.jpaa.2017.02.013),[arXiv:1510.00669](https://arxiv.org/abs/1510.00669)&rbrack; -- beware of section numbering discrepancy between the published and arXiv versions.

The following two notes describe the construction,  specialized to cubical sets, in more type-theoretic language.

* {#mod2} [[Thierry Coquand]], *A model structure on some presheaf categories*, [pdf](http://www.cse.chalmers.se/~coquand/mod2.pdf)

* {#cis3} [[Thierry Coquand]], *Some examples of complete Cisinski model structures*, [pdf](http://www.cse.chalmers.se/~coquand/cis3.pdf)

A refactoring of part of Sattler's construction through the notion of "cylindrical [[premodel category]]" is described in Section 3 of

* {#csElegance} [[Evan Cavallo]] and [[Christian Sattler]], *Relative elegance and cartesian cubes with one connection*, $[$[arXiv:2211.14801](https://arxiv.org/abs/2211.14801)$]$

and in the unpublished note

* {#sattlerInterval} [[Christian Sattler]], *Cylindrical model structures*, [pdf](https://www.cse.chalmers.se/~sattler/docs/interval-model-structure.pdf)

Adaptations of the construction to cartesian cubical sets without connections can be found in

* {#Awodey2023} [[Steve Awodey]], _Cartesian cubical model categories_ (2023) &lbrack;[arXiv:2305.00893](https://arxiv.org/abs/2305.00893)&rbrack;

* [[Evan Cavallo]], [[Anders Mörtberg]], [[Andrew W Swan]], _Unifying Cubical Models of Univalent Type Theory_, 28th EACSL Annual Conference on Computer Science Logic (CSL 2020). &lbrack;[doi:10.4230/LIPIcs.CSL.2020.14](https://dx.doi.org/10.4230/LIPIcs.CSL.2020.14)&rbrack;

Cubical-type model categories that present classical homotopy theory:

* {#CavalloSattler2022} [[Evan Cavallo]] and [[Christian Sattler]], _Relative elegance and cartesian cubes with one connection_ (2022). &lbrack;[arXiv:2211.14801](https://arxiv.org/abs/2211.14801)&rbrack;

* {#ACCRS2024} [[Steve Awodey]], [[Evan Cavallo]], [[Thierry Coquand]], [[Emily Riehl]], and [[Christian Sattler]], _The equivariant model structure on cartesian cubical sets_ (2024). &lbrack;[arXiv:2406.18497](https://arxiv.org/abs/2406.18497)&rbrack;

On equivalences with the model structure on simplicial sets:

* {#sattlerHIM} [[Christian Sattler]], *Do cubical models of type theory also model homotopy types*, lecture at Hausdorff Trimester Program: Types, Sets and Constructions, [youtube](https://www.youtube.com/watch?v=wkPDyIGmEoA)

* {#hrInduced} [[Philip Hackney]] and [[Martina Rovelli]], *Induced model structures for ∞-categories and ∞-groupoids*, $[$[arXiv:2102.01104](https://arxiv.org/abs/2102.01104)$]$, [Proc. Amer. Math. Soc., June 10, 2022](https://www.ams.org/journals/proc/0000-000-00/S0002-9939-2022-15982-6/home.html)

* {#swCuSi} [[Thomas Streicher]] and [[Jonathan Weinberger]], *Simplicial sets inside cubical sets* $[$[arXiv:1911.09594](https://arxiv.org/abs/1911.0959)$]$, [Theory and Applications of Categories, Vol. 37, 2021, No. 10, pp 276–286](http://www.tac.mta.ca/tac/volumes/37/10/37-10abs.html)


Proofs of the [[Frobenius condition#InWeakFactorizationSystems|Frobenius condition]]:

* {#HazratpourRiehl2024} [[Sina Hazratpour]], [[Emily Riehl]], *A 2-categorical proof of Frobenius for fibrations defined from a generic point*, Mathematical Structures in Computer Science *34*, Special Issue 4 (2024) 258--280 &lbrack;[doi:10.1017/S0960129524000094](https://doi.org/10.1017/S0960129524000094),[arXiv:2210.00078](https://arxiv.org/abs/2210.00078)&rbrack;

* {#Barton2024} [[Reid Barton]], *A short proof of the Frobenius property for generic fibrations* (2024) &lbrack;[arXiv:2402.04227](https://arxiv.org/abs/2402.04227)&rbrack;

Formalization of a version of the construction in the [[Coq]] proof assistant:

* {#BoulierTabareau2021} [[Simon Boulier]], [[Nicolas Tabareau]], _Model structure on the universe of all types in interval type theory_, MSCS, vol. 31, 2021 ([doi:10.1017/S0960129520000213](https://doi.org/10.1017/S0960129520000213))

[[!redirects type-theoretic model structures]]
[[!redirects type theoretic model structures]]
[[!redirects type theoretic model structure]]
[[!redirects type-theoretic model structure]]
[[!redirects cubical-type model categories]]
[[!redirects cubical-type model structure]]
[[!redirects cubical-type model structures]]
