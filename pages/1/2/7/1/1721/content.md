
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

In [[algebraic topology]], what is called generalized Eilenberg-Steenrod cohomology started out as an axiomatization of the basic properties of the [[functors]] that send [[topological spaces]] to their [[cohomology groups]] for  [[ordinary cohomology]] and for [[topological K-theory]]. Any functor satisfying these is called a _generalized [[cohomology theory]]_. 

Notice however that one may drop further axioms, such as the [[suspension isomorphism]] to arrive at something yet more general, e.g. [[nonabelian cohomology]] such as unstable [[cohomotopy]]. To disambiguate these further generalizations it might be worthwhile to say _generalized stable cohomology_ or the like, but this is not common terminology.

The [[Brown representability theorem]] showed that these generalized cohomology theories are precisely those functors are [[representable functor|represented]] by maps from topological spaces into [[spectra]].

This means that from a general abstract perspective, generalized Eilenberg-Steenrod cohomology is the [[cohomology]] in an [[(∞,1)-category]] $\mathbf{H}$ that happens to be a [[stable (∞,1)-category]].

The archetypical example of this is $\mathbf{H} = Sp(Top)$, the [[stable (∞,1)-category of spectra]] and this is the context in which generalized Eilenberg-Steenrod cohomology is usually understood. So

+-- {: .standout}

Generalized Eilenberg-Steenrod cohomology is 
[[cohomology]] $H(X,A)$ with coefficient object $A$ a [[spectrum object]].

=--

## The Eilenberg-Steenrod axioms 

One may conceptualize the axioms as ensuring that certain nice properties that hold in the category Top will be preserved by our cohomology functor.

Let $U$ and $X$ be topological spaces, such that $U$ is a subspace of $X$. Notation: $(X,U) := U \hookrightarrow X$.

Note that if only one space is listed, the subspace is assumed to be the empty set $(X, \emptyset)$.

The Eilenberg-Steenrod axioms are the following:

+-- {: .num_defn}
###### Definition

A [[cohomology theory]] is a collection $\{A^n\}_{n \in \mathbb{Z}}$ of [[functor]]s

$$
  A^n : (Top^{\hookrightarrow})^{op} \to Ab
$$

from the [[homotopy category]] $Top^{\hookrightarrow}$ of pairs of [[topological space]]s to the category [[Ab]] of abelian groups, as well as a [[natural transformation]] $\delta: A^n(X, \emptyset) \to A^{n+1}(X, U)$. These functors and natural transformations satisfy and are characterized by the following axioms.

1. *Exactness*: The following sequence is exact. Note that the inclusions $U \hookrightarrow X$ and $(X, \emptyset) \hookrightarrow (X, U)$ induce the unlabeled arrows. 

$ \cdots \to A^n(X, U) \to A^n(X, \emptyset) \to A^n(U, \emptyset) \xrightarrow{\delta} A^{n+1}(X, U) \to \cdots $

1. *Weak homotopy equivalence*: if $f : X \to Y$ is a [[weak homotopy equivalence]] then $A^n(f) : A^n(Y) \to A^n(X)$ is an [[isomorphism]]

1. *Additivity*: If $ (X, U) = \coprod_i (X_i, U_i)$, then $A^n(X, U) = \coprod_i A^n(X_i, U_i)$.

1. *Excision*: Let $S$ be a subspace of $U$, the natural inclusion of the pair $i:(X-S, U-S) \hookrightarrow (X, U)$ induces an isomorphism $A^n(i): A^n(X-S, U-S) \to A^n(X, U)$.


=--

Ordinary cohomology theories require and additional axiom, the dimension axiom $A^n(pt) = 0$.

## Examples 


* [[ordinary cohomology]]: [[Eilenberg?Mac Lane spectrum]]

* [[K-theory]]: [[K-theory spectrum]]
* [[tmf]]

* [[cobordism cohomology theory]]

* [[Morava K-theory]], [[integral Morava K-theory]]

* [[Morava E-theory]]

* [[stable cohomotopy]]

## Properties

### Expression by ordinary cohomology via Atiyah-Hirzebruch

The [[Atiyah-Hirzebruch spectral sequence]] serves to express generalized cohomology $E^\bullet$ in terms of ordinary cohomology with coefficients in $E^\bullet(\ast)$.

## Related concepts

* [[Brown representability theorem]]

* [[homology theory]]

* [[bivariant cohomology theory]]

[[!include twisted generalized cohomology in linear homotopy type theory -- table]]

**remark** Originally Eilenberg and Steenrod had written down axioms that characterized the behaviour of ordinary integral cohomology, what is now understood to be cohomology with coefficients in the [[Eilenberg-MacLane spectrum]]. Generalized Eilenberg-Steenrod cohomology is originally defined as anything that satisfies this list of axioms except the first one. Later it was proven, by the [[Brown representability theorem]], that all the models for these axioms arise in terms of homotopy classes of maps into a [[spectrum]]. In our revisionist perspective above, we take this historically secondary point of view as the conceptually primary one.


## References 

A pedagogical introduction to [[spectrum|spectra]] and generalized (Eilenberg-Steenrod) cohomology is in

* [[John Baez]], [TWF 149](http://math.ucr.edu/home/baez/twf_ascii/week149) 

Textbook accounts include

* {#May99} [[Peter May]] chapter 18 of _A Concise Course on Algebraic Topology_, Chicago Lecture Notes  1999 ([pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))

* Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 12.1 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))

* {#KonoTamaki02} Akira Kono, Dai Tamaki, _Generalized cohomology_, AMS 2002, esp. chapter 2 ([[GeneralizedCohomology.pdf:file]])


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