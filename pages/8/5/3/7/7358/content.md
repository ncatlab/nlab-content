
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Internal $(\infty,1)$-Categories
+-- {: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--

# $\Gamma$-spaces
* table of contents
{: toc}

## Idea

A $\Gamma$-space is a model for an [[∞-groupoid]] equipped with a multiplication that is unital, associative, and commutative up to higher [[coherence|coherent]]  [[homotopies]]:  they are models for groupal [[E-∞ spaces]] / [[infinite loop spaces]] / [[abelian ∞-groups]].

The notion of $\Gamma$-space is a close variant of that of [[Segal category]] for the case that the underlying [[(∞,1)-category]] happens to be an [[∞-groupoid]], happens to be [[n-connected object in an (∞,1)-category|connected]] and is equipped with extra structure.

Therefore a $\Gamma$-space can be [[delooping|delooped]] infinitely many times to produce a [[connective spectrum]].  

$\Gamma$-spaces differ from [[operad|operadic]] models for $E_\infty$-spaces, such as in terms of  [[algebra over an operad|algebras]] over an [[E-∞ operad]], in that their multiplication is specified "[[geometric definition of higher categories|geometrically]]" rather than [[algebraic definition of higher categories|algebraically]].

## Definition

Let $\Gamma^{op}$ (see [[Segal's category]]) be the [[skeleton]] of the category of [[finite set|finite]] [[pointed sets]].  We write $\underline{n}$ for the finite pointed set with $n$ non-basepoint elements.  Then a **$\Gamma$-space** is a functor $X\colon \Gamma^{op}\to Top$ (or to simplicial sets, or whatever other model one prefers).

We think of $X(\underline{1})$ as the "underlying space" of a $\Gamma$-space $X$, with $X(\underline{n})$ being a "model for the cartesian power $X^n$".  In order for this to be valid, and thus for $X$ to present an infinite loop space, a $\Gamma$-space must satisfy the further condition that all the [[Segal map]]s
$$ X(\underline{n}) \to X(\underline{1}) \times \dots \times X(\underline{1})$$
are [[weak equivalences]].  We include in this the $0$th Segal map $X(\underline{0}) \to *$, which therefore requires that $X(\underline{0})$ is contractible.  Sometimes the very definition of *$\Gamma$-space* includes this homotopical condition as well.

## Properties

* Note that we have a functor $\Delta\to\Gamma$, where $\Delta$ is the [[simplex category]], which takes $[n]$ to $\underline{n}$.  Thus, every $\Gamma$-space has an underlying simplicial space. This simplicial space is in fact a [[special Delta-space]] which exhibits the 1-fold delooping of the corresponding $\Gamma$-space.

* The [[topos]] $\Set^{\Gamma^{op}}$ of $\Gamma$-sets is the [[classifying topos]] for pointed objects ([MO question](http://mathoverflow.net/questions/85600/what-do-gamma-sets-classify)).

* A model structure on $\Gamma$-spaces can be found in Bousfield and Friedlander below.

## Related notions

[[!include k-monoidal table]]


## References

The notion goes back to 

* [[G. Segal]], "Categories and Cohomology Theories", Topology 13 (1974).


The [[model category]] structure on $\Gamma$-spaces (a [[generalized Reedy model structure]]) was established in

*  [[A. K. Bousfield]], [[E. M. Friedlander]], _Homotopy Theory of &#915;-spaces, Spectra, and Bisimplicial Sets_, Geometric Applications of Homotopy Theory (1977).

See also

*  C. Balteanu, Z. Fiedorowicz, R. Schwanzl and [[R. Vogt]], _Iterated
Monoidal Categories_, Advances in Mathematics (2003).

* B. Badzioch, _Algebraic Theories in Homotopy Theory_, Annals of Mathematics, 155, 895--913 (2002).

Discussion of $\Gamma$-spaces in the broader context of [[higher algebra]] in [[(infinity,1)-operad]] theory is around remark 2.4.2.2 of

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#Lurie}


[[!redirects Gamma-space]]
[[!redirects Gamma-spaces]]
[[!redirects ∞-space]]
[[!redirects ∞-spaces]]

[[!redirects Gamma space]]
[[!redirects Gamma spaces]]

[[!redirects Segal's category Gamma]]
[[!redirects Segal's category ?]]

[[!redirects model structure for Gamma-spaces]]
[[!redirects model structure for ∞-spaces]]
