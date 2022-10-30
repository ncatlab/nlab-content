
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

The collection of [[functors]] from ([[pointed topological space|pointed]]) [[topological spaces]] to [[abelian groups]] which assign [[cohomology groups]] of [[ordinary cohomology]] (e.g. [[singular cohomology]]) may be [[axiom|axiomatized]] by a small set of natural conditions, called the _Eilenberg-Steenrod axioms_ ([Eilenberg-Steenrod 52, I.3](#EilenbergSteenrod52)), see [below](#TheEilenbergSteenrodAxioms). One of these conditions, the "dimension axiom" ([Eilenberg-Steenrod 52, I.3 Axiom 7](#EilenbergSteenrod52)) says that the (co)homology groups assigned to the point are concentrated in degree 0. The class of functors obtained by discarding this "dimension axiom" came to be known as _generalized (co)homology theories_ ([Whitehead 62](#Whitehead62)) or _extraordinary (co)homology theories_. 

Examples include [[topological K-theory]] ([Atiyah-Hirzebruch 61, 1.8](https://ncatlab.org/nlab/show/topological+K-theory#AtiyahHirzebruch61)), [[elliptic cohomology]] and [[cobordism cohomology theory]]. Dually one speaks of _[[generalized homology]]_.

Notice that, while the terminology "generalized cohomology" is standard in [[algebraic topology]] with an eye towards [[stable homotopy theory]], it is somewhat unfortunate in that there are various _other_ and _further_ generalizations of the axioms that all still deserve to be and are called "[[cohomology]]". For instance dropping the [[suspension isomorphism|suspension]] axiom leads to [[nonabelian cohomology]] and dropping the "homotopy axiom" (and taking the domain spaces to be [[smooth manifolds]]) leads to the further generality of [[differential cohomology]]. 
This entry here is concerned with the generalization obtained from the Eilenberg-Steenrod axioms by _just_ discarding the dimension axiom. For lack of a better term, we say "generalized (Eilenberg-Steenrod) cohomology" here.

In ([Whitehead 62](#Whitehead62)) it was observed that every [[spectrum]] induces a generalized homology theory.  The _[[Brown representability theorem]]_ ([Brown 62](#Brown62)) asserts that every generalized (co)homology arises this way, being [[representable functor|represented]] by [[mapping spectra]] into/[[smash product]] with a [[spectrum]].  But beware that the cohomology theory represented by a spectrum in general contains strictly less information than the spectrum, due to the existence of "[[phantom maps]]".

On the other hand, if one refines the concept of a generalized homology theory from taking values in graded abelian groups to taking values in [[homotopy types]] then it does become equivalent to the concept of _spectrum_, this is the statement at _[excisive functor -- Examples -- Spectrum objects](excisive+%28?%2C1%29-functor#SpectrumObjects)_.

This means that from a perspective of [[higher category theory]], generalized Eilenberg-Steenrod cohomology is the intrinsic [[cohomology]] of the [[(∞,1)-category of spectra]], or better: [[twisted cohomology|twisted]] generalized Eilenberg-Steenrod cohomology is the intrinsic cohomology of the [[tangent (∞,1)-topos]] of [[parameterized spectra]].


+-- {: .standout}

Generalized Eilenberg-Steenrod cohomology is 
[[cohomology]] $E(X)= H(X,E)$ with [[coefficients]] $E$ a [[spectrum object]].

=--

## The Eilenberg-Steenrod axioms 
 {#TheEilenbergSteenrodAxioms}

([Eilenberg-Steenrod 52, I.3](#EilenbergSteenrod52)) One may conceptualize the following axioms as ensuring that certain nice properties that hold in the category $Top$ will be preserved by the cohomology functor.

There are two versions of the statement of the axioms, essentially equivalent, one for [[reduced cohomology]], the other for unreduced cohomology.

### Reduced cohomology
 {#ReducedCohomology}

+-- {: .num_defn #ReducedGeneralizedCohomology}
###### Definition

A _reduced generalized [[cohomology theory]]_ is a [[functor]]

$$
  \tilde E^\bullet \colon (Top^{\ast/})^{op} \longrightarrow Ab
$$

from the [[opposite category]] of [[pointed topological spaces]] ([[CW-complexes]]) to $\mathbb{Z}$-[[graded abelian groups]] ("[[cohomology groups]]")

$$
  \tilde E 
    \;\colon\; 
  (X \stackrel{f}{\longrightarrow} Y)
    \mapsto
  (\tilde E^\bullet(Y) 
    \stackrel{f^\ast}{\longrightarrow}
  \tilde E^\bullet(X))
$$

and equipped with [[natural isomorphisms]], to be called the _[[suspension isomorphism]]_

$$
  \tilde E^\bullet(-) \stackrel{\simeq}{\longrightarrow} \tilde E^{\bullet +1}(\Sigma -) 
$$

(for $\Sigma \colon Top^{\ast/} \to Top^{\ast/}$ the [[reduced suspension]] functor)

such that:

1. **(homotopy invariance)** If $f_1,f_2 \colon X \longrightarrow Y$ are two morphisms of pointed topological spaces such that there is a (base point preserving) [[homotopy]] $f_1 \simeq f_2$ between them, then the induced [[homomorphisms]] of abelian groups are [[equality|equal]] 

   $$
     f_1^\ast = f_2^\ast
     \,.
   $$

1. **(exactness)** For $i \colon A \hookrightarrow X$ an inclusion of pointed topological spaces, with $j \colon X \longrightarrow cone(i)$ the induced [[mapping cone]], then this gives an [[exact sequence]] of graded abelian groups

   $$
     \tilde E^\bullet(cone(i)) 
      \stackrel{j^\ast}{\longrightarrow} 
     \tilde E^\bullet(X)
       \stackrel{i^\ast}{\longrightarrow}
     \tilde E^\bullet(A)
     \,.
   $$

=--


(e.g. [AGP 02, def. 12.1.4](#AGP02))

Write $\mathbb{S}^0$ for the [[0-sphere]], canonically regarded as a [[pointed topological space]].

+-- {: .num_defn}
###### Definition

A reduced generalized cohomology theory $\tilde E^\bullet$, def. \ref{ReducedGeneralizedCohomology}, is called _ordinary_ if

* **(dimension)** $\tilde E^{\bullet\neq 0}(\mathbb{S}^0) \simeq 0$.

=--

### Unreduced cohomology

In the following a _pair_ $(X,U)$ refers to a [[subspace]] inclusion of [[topological spaces]]  $U \hookrightarrow X$.  Whenever only one space is mentioned, the subspace is assumed to be the [[empty set]] $(X, \emptyset)$. Write $Top^{\hookrightarrow}$ for the category of such pairs (the [[full subcategory]] of the [[arrow category]] of [[Top]] on the inclusions). We identify $Top \hookrightarrow Top^{\hookrightarrow}$ by $X \mapsto (X,\emptyset)$.


+-- {: .num_defn #GeneralizedCohomologyTheory}
###### Definition

A _[[cohomology theory]]_ (unreduced) is a [[functor]]

$$
  E^\bullet : (Top^{\hookrightarrow})^{op} \to Ab^{\mathbb{Z}}
$$

to the category of $\mathbb{Z}$-[[graded abelian groups]], as well as a [[natural transformation]] 

$$
  \delta \colon  E^\bullet(U, \emptyset) \to E^{\bullet + 1}(X, U)
  \,.
$$ 

such that:

1. {#ExactnessUnreduced} **(exactness)** For $U \hookrightarrow X$ the induced sequnce

   $$ 
     \cdots 
       \to 
     E^n(X, U) 
       \longrightarrow 
     E^n(X) 
       \longrightarrow
     E^n(U) 
       \stackrel{\delta}{\longrightarrow} 
     E^{n+1}(X, U) 
       \to 
     \cdots 
   $$

   is a [[long exact sequence]] of abelian groups.

1. **(homotopy equivalence)** For $f \colon X \to Y$ a [[weak homotopy equivalence]] then 

   $$
     E^\bullet(f) \colon E^\bullet(Y) \stackrel{\simeq}{\longrightarrow} E^\bullet(X)
   $$

   is an [[isomorphism]].

1. **(additivity)** If $ (X, U) = \coprod_i (X_i, U_i)$, then $E^n(X, U) = \coprod_i E^n(X_i, U_i)$.

1. **(excision)** For $S \hookrightarrow U \hookrightarrow X$. the natural inclusion of the pair $i \colon (X-S, U-S) \hookrightarrow (X, U)$ induces an isomorphism $E^n(i) \colon E^n(X-S, U-S) \to E^n(X, U)$.


=--

e.g. [AGP 02, def. 12.1.1 ](#AGP02). 

A generalized cohomology theory is called _ordinary_ if in addition 

* **Dimension**: $E^n(pt) = 0$.

## Examples 


* [[ordinary cohomology]]: [[Eilenberg?Mac Lane spectrum]]

* [[K-theory]]: [[K-theory spectrum]]
* [[tmf]]

* [[cobordism cohomology theory]]

* [[Morava K-theory]], [[integral Morava K-theory]]

* [[Morava E-theory]]

* [[stable cohomotopy]]

## Properties

### Relation between reduced and unreduced cohomology
 {#RelationBetweenReducedAndUnreduced}

+-- {: .num_defn}
###### Definition

For $E^\bullet(-,-) \colon Top^{\hookrightarrow} \to Ab^{\mathbb{Z}}$ a cohomology theory in the sense of def. \ref{GeneralizedCohomologyTheory}, then the functor $\tilde E^\bullet(-)$ on [[pointed topological spaces]] $(X,\ast)$ given by

$$
  \tilde E^\bullet(X,x_0) \coloneqq E^\bullet(X,\{x_0\})
$$

is a reduced cohomology theory in the sense of def. \ref{ReducedGeneralizedCohomology}.

=--

(e.g [AGP 02, theorem 12.1.12](#AGP02))

+-- {: .num_prop #UnreducedCohomologyIsReducedPlusPointValue}
###### Proposition

For $(X,\ast)$ a pointed topological space, then

$$
  E^\bullet(X) \simeq \tilde E^\bullet(X) \oplus E^\bullet(\ast)
$$

=--

+-- {: .proof}
###### Proof

The pair $\ast \hookrightarrow X$ induces the seqence

$$
  \cdots
   \to 
  E^{\bullet-1}(\ast)
    \stackrel{\delta}{\longrightarrow}
  \tilde E^\bullet(X)
    \stackrel{}{\longrightarrow}
  E^\bullet(X) 
    \stackrel{}{\longrightarrow}
  E^\bullet(\ast)
    \stackrel{\delta}{\longrightarrow}
  \tilde E^{\bullet+1}(X)
    \to
  \cdots
$$

which by the exactness clause in def. \ref{GeneralizedCohomologyTheory} is [[exact sequence|exact]]. 

Now since the composite $\ast \to X \to \ast$ is the identity, the morphism 
$E^\bullet(X) \to E^\bullet(\ast)$ has a [[section]] and so is in particular an [[epimorphism]]. Therefore, by exactness, the [[connecting homomorphism]] vanishes, $\delta = 0$ and we have a [[short exact sequence]]

$$
  0 
    \to 
  \tilde E^\bullet(X)
    \stackrel{}{\longrightarrow}
  E^\bullet(X) 
    \stackrel{}{\longrightarrow}
  E^\bullet(\ast)
    \to
  0
$$

with the right map an epimorphism. Hence this is a [[split exact sequence]] and the statement follows.


=--


### Exact sequence for triples
 {#ExactnessForTriples}

+-- {: .num_prop #ExactSequenceOfATriple}
###### Proposition
**(exact sequence of a triple)**

For $E$ a generalized cohomology theory, def. \ref{GeneralizedCohomologyTheory}, then every inclusion of two consecutive subspaces

$$
  B \hookrightarrow A \hookrightarrow X
$$

induces a [[long exact sequence]] of cohomology groups of the form

$$
  \cdots
   \to
  E^{q-1}(A,B) 
    \stackrel{\bar \delta}{\longrightarrow}
  E^q(X,A)
    \stackrel{}{\longrightarrow}
  E^q(X,B)
    \stackrel{}{\longrightarrow}
  E^q(A,B)
    \to
  \cdots
$$

where 

$$
  \bar \delta 
    \;\colon \;
  E^{q-1}(A,B) 
   \longrightarrow
  E^{q-1}(A)
   \stackrel{\delta}{\longrightarrow}
  E^{q}(A,X)
  \,.
$$

=--

(e.g. [AGP 02, prop. 12.1.11](#AGP02)).

+-- {: .num_remark}
###### Remark

The property expressed by prop. \ref{ExactSequenceOfATriple} is what gives rise to the [[Cartan-Eilenberg spectral sequence]] for $E$-cohomology of a [[CW-complex]] $X$.

=--


### Expression by ordinary cohomology via Atiyah-Hirzebruch

The [[Atiyah-Hirzebruch spectral sequence]] serves to express generalized cohomology $E^\bullet$ in terms of ordinary cohomology with coefficients in $E^\bullet(\ast)$.

## Related concepts

* [[Brown representability theorem]]

* [[homology theory]]

* [[bivariant cohomology theory]]

[[!include twisted generalized cohomology in linear homotopy type theory -- table]]

**remark** Originally Eilenberg and Steenrod had written down axioms that characterized the behaviour of ordinary integral cohomology, what is now understood to be cohomology with coefficients in the [[Eilenberg-MacLane spectrum]]. Generalized Eilenberg-Steenrod cohomology is originally defined as anything that satisfies this list of axioms except the first one. Later it was proven, by the [[Brown representability theorem]], that all the models for these axioms arise in terms of homotopy classes of maps into a [[spectrum]]. In our revisionist perspective above, we take this historically secondary point of view as the conceptually primary one.


## References 

The axioms including the dimension axiom are due to 

* {#EilenbergSteenrod52} [[Samuel Eilenberg]], [[Norman Steenrod]], _Foundations of algebraic topology_, Princeton 1952 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/eilestee.pdf))

The concept of generalized homology obtained by discrading the dimension axiom and the observation that every [[spectrum]] induces an example is due to

* {#Whitehead62} [[George Whitehead]], _Generalized homology theories_, Transactions of the American Mathematical Society, 102 (1962) 227-283 ([pdf](http://www.ams.org/journals/tran/1962-102-02/S0002-9947-1962-0137117-6/S0002-9947-1962-0137117-6.pdf))

The proof that every generalized (co)homology theory arises this way ([[Brown representability theorem]]) is due to

* {#Brown62} [[Edgar Brown]], _Cohomology theories_, Annals of Mathematics, Second Series 75: 467&#8211;484 (1962)

* {#Brown65} [[Edgar Brown]], _Abstract homotopy theory_, Trans. AMS 119 no. 1 (1965)

An early lecture note account is in

* {#Adams74} [[Frank Adams]], part III, sections 2 and 6 of _[[Stable homotopy and generalised homology]]_, 1974

Textbook accounts include

* {#Kochmann96} [[Stanley Kochmann]], section 3.4 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#May99} [[Peter May]] chapter 18 of _A Concise Course on Algebraic Topology_, Chicago Lecture Notes  1999 ([pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))

* {#AGP02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 12.1 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))

* {#KonoTamaki02} Akira Kono, Dai Tamaki, _Generalized cohomology_, AMS 2002, esp. chapter 2 ([[GeneralizedCohomology.pdf:file]])

A pedagogical introduction to [[spectrum|spectra]] and generalized (Eilenberg-Steenrod) cohomology is in

* [[John Baez]], [TWF 149](http://math.ucr.edu/home/baez/twf_ascii/week149) 


More references relating to the [[nPOV]] on cohomology include:

* [[Mike Hopkins]], _[[Complex oriented cohomology theories and the language of stacks]]_ course notes ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/coctalos.pdf))

* [[Jacob Lurie]],  _[[A Survey of Elliptic Cohomology - cohomology theories]]_


[[!redirects generalized (Eilenberg?Steenrod) cohomology]]
[[!redirects generalized (Eilenberg--Steenrod) cohomology]]
[[!redirects generalized (Eilenberg-Steenrod) cohomology theory]]
[[!redirects generalized (Eilenberg?Steenrod) cohomology theory]]

[[!redirects generalized (Eilenberg--Steenrod) cohomology theory]]
[[!redirects generalized (Eilenberg--Steenrod) cohomology theories]]
[[!redirects generalized (Eilenberg-Steenrod) cohomology theory]]
[[!redirects generalized (Eilenberg-Steenrod) cohomology theories]]

[[!redirects generalised (Eilenberg-Steenrod) cohomology]]
[[!redirects generalised (Eilenberg?Steenrod) cohomology]]
[[!redirects generalised (Eilenberg--Steenrod) cohomology]]
[[!redirects generalised (Eilenberg-Steenrod) cohomology theory]]
[[!redirects generalised (Eilenberg?Steenrod) cohomology theory]]
[[!redirects generalised (Eilenberg--Steenrod) cohomology theory]]
[[!redirects Eilenberg-Steenrod cohomology]]
[[!redirects Eilenberg?Steenrod cohomology]]
[[!redirects Eilenberg--Steenrod cohomology]]
[[!redirects Eilenberg-Steenrod cohomology theory]]
[[!redirects Eilenberg?Steenrod cohomology theory]]
[[!redirects Eilenberg--Steenrod cohomology theory]]

[[!redirects Eilenberg-Steenrod axioms]]

[[!redirects generalized cohomology theory]]
[[!redirects generalized cohomology theories]]
[[!redirects generalised cohomology theory]]
[[!redirects generalised cohomology theories]]
[[!redirects cohomology theories]]
[[!redirects cohomology theory]]

[[!redirects generalized (Eilenberg-Steenrod) cohomology theory]]
[[!redirects generalized (Eilenberg-Steenrod) cohomology theories]]

[[!redirects generalized (Eilenberg-Steenrod) cohomlogy theory]]
[[!redirects generalized (Eilenberg-Steenrod) cohomlogy theories]]