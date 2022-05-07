
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Internal $(\infty,1)$-Categories
+-- {: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--

* table of contents
{: toc}

## Idea

The concept of _$\Gamma$-spaces_ is a model for [[∞-groupoids]] equipped with a multiplication that is unital, associative, and commutative up to higher [[coherence|coherent]]  [[homotopies]]:  they are models for [[E-∞ spaces]] and hence, if grouplike ("very special" $\Gamma$-spaces), for [[infinite loop spaces]] / [[connective spectra]] / [[abelian ∞-groups]].

The notion of $\Gamma$-space is a close variant of that of [[Segal category]] for the case that the underlying [[(∞,1)-category]] happens to be an [[∞-groupoid]], happens to be [[n-connected object of an (∞,1)-category|connected]] and is equipped with extra structure.

$\Gamma$-spaces differ from [[operad|operadic]] models for $E_\infty$-spaces, such as in terms of  [[algebra over an operad|algebras]] over an [[E-∞ operad]], in that their multiplication is specified "[[geometric definition of higher categories|geometrically]]" rather than [[algebraic definition of higher categories|algebraically]].

## Definition

Let $\Gamma^{op}$ (see [[Segal's category]]) be the [[skeleton]] of the category of [[finite set|finite]] [[pointed sets]].  We write $\underline{n}$ for the finite pointed set with $n$ non-basepoint elements.  Then a **$\Gamma$-space** is a functor $X\colon \Gamma^{op}\to Top$ (or to [[simplicial sets]], or whatever other model one prefers).

We think of $X(\underline{1})$ as the "underlying space" of a $\Gamma$-space $X$, with $X(\underline{n})$ being a "model for the cartesian power $X^n$".  In order for this to be valid, and thus for $X$ to present an infinite loop space, a $\Gamma$-space must satisfy the further condition that all the [[Segal map]]s
$$ X(\underline{n}) \to X(\underline{1}) \times \dots \times X(\underline{1})$$
are [[weak equivalences]].  We include in this the $0$th Segal map $X(\underline{0}) \to *$, which therefore requires that $X(\underline{0})$ is contractible.  Sometimes the very definition of *$\Gamma$-space* includes this homotopical condition as well.

## Delooping

One of the main advantages of $\Gamma$-spaces (and,
more generally, $\Gamma$-objects) is that the [[delooping]] construction
is very easy to express in this language.

The delooping construction is a functor
$$B\colon Fun(\Gamma^{op},M) \to Fun(\Gamma^{op},M),$$
where $M$ is the [[relative category]] for which we are considering $\Gamma$-objects.
The most common choices are $M=sSet$, the [[model category of simplicial sets]],
and $M=Top$, the [[model category of topological spaces]].

We define
$$(B A)(S) := hocolim (T\mapsto A(S\times T)),$$
where $T\in\Delta^\op$ and the argument of the [[homotopy colimit]] functor
is a [[simplicial object]] in $M$.
Here $T\in\Delta$ is converted first to an object of $\Gamma$
via the functor $\Delta\to\Gamma$ described below.

## Properties

### Relation to simplicial sets

We have a functor $\Delta\to\Gamma$, where $\Delta$ is the [[simplex category]], which takes $[n]$ to $\underline{n}$.  Thus, every $\Gamma$-space has an underlying simplicial space. This simplicial space is in fact a [[special Delta-space]] which exhibits the 1-fold delooping of the corresponding $\Gamma$-space.

### Model category structure

A [[model category]] structure on $\Gamma$-spaces is due to ([Bousfield-Friedlander 77](#BousfieldFriedlander77)). See at _[[model structure for connective spectra]]_.

## Related notions

* [[Gamma-set]]

[[!include k-monoidal table]]


## References

The concept goes back to 

* [[Graeme Segal]], _Categories and cohomology theories_, Topology 13 (1974).

Another early reference considers $\Gamma$-objects in [[simplicial groups]].
It is also the first reference that uses the terms “special Γ-spaces”
and “very special Γ-spaces”, which it attributes to Segal.

* [[Donald W. Anderson]], _Chain functors and homology theories_, Symposium on Algebraic Topology, Lecture Notes in Mathematics (1971), 1–12.  [doi](http://dx.doi.org/10.1007/bfb0060890).

The [[model category]] structure on $\Gamma$-spaces (a [[generalized Reedy model structure]]) was established in

* {#BousfieldFriedlander77} [[A. K. Bousfield]], [[E. M. Friedlander]], _Homotopy Theory of &#915;-spaces, Spectra, and Bisimplicial Sets_, Geometric Applications of Homotopy Theory (1977) ([pdf](http://dodo.pdmi.ras.ru/~topology/books/bousfield-friedlander.pdf))

Discussion of the [[smash product of spectra]] on connective spectra via $\Gamma$-spaces is due to

* {#Lydakis98} Lydakis, _Smash products and $\Gamma$-spaces_, Math. Proc. Cam. Phil. Soc. 126 (1999), 311-328 ([pdf](http://hopf.math.purdue.edu/Lydakis/smash_gamma.pdf))

and of the corresponding [[monoid objects]], hence [[ring spectra]], in 

* {#Schwede99} [[Stefan Schwede]], _Stable homotopical algebra and $\Gamma$-spaces_, Math. Proc. Camb. Phil. Soc. (1999), 126, 329 ([pdf](http://www.math.uni-bonn.de/people/schwede/Gamma.pdf))

* {#Lawson09} [[Tyler Lawson]], _Commutative &#915;-rings do not model all commutative ring spectra_, Homology Homotopy Appl. Volume 11, Number 2 (2009), 189-194. ([Euclid](http://projecteuclid.org/euclid.hha/1296138517))

Discussion in relation to [[symmetric spectra]] includes

* {#Schwede12} [[Stefan Schwede]], chapter I, section 7.4 of _[[Symmetric spectra]]_ (2012)


Discussion of $\Gamma$-spaces in the broader context of [[higher algebra]] in [[(infinity,1)-operad]] theory is around remark 2.4.2.2 of

* {#Lurie} [[Jacob Lurie]], _[[Higher Algebra]]_
 
See also

*  C. Balteanu, Z. Fiedorowicz, [[R. Schwanzl]] and [[R. Vogt]], _Iterated
Monoidal Categories_, Advances in Mathematics (2003).

* B. Badzioch, _Algebraic Theories in Homotopy Theory_, Annals of Mathematics, 155, 895--913 (2002).

[[!redirects Gamma-spaces]]
[[!redirects Γ-space]]
[[!redirects Γ-spaces]]
[[!redirects ∞-space]]
[[!redirects ∞-spaces]]

[[!redirects Gamma space]]
[[!redirects Gamma spaces]]

[[!redirects Segal's category Gamma]]
[[!redirects Segal's category Γ]]

[[!redirects model structure for Gamma-spaces]]
[[!redirects model structure for ∞-spaces]]