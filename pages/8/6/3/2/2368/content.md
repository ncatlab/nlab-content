+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--





#Contents#
* table of contents
{:toc}


## Idea

In [[higher algebra]] and [[stable homotopy theory]] one is interested in [[monoid in a monoidal (∞,1)-category|monoid objects]] in the [[stable (∞,1)-category of spectra]] -- called $A_\infty$-[[A-∞-ring|rings]] -- and [[commutative monoid in an (infinity,1)-category|commutative monoid objects]] -- called $E_\infty$-[[E-∞-ring|rings]]. These monoid objects satisfy associativity, uniticity and, in the $E_\infty$-case, commutativity up to coherent higher homotopies. 

For concretely working with these objects, it is often useful to have concrete  [[category theory|1-categorical]] algebraic models for these intricate [[higher category theory|higher categorical]]/homotopical entities. The _symmetric monoidal smash product of spectra_ is a structure that allows to model [[A-infinity ring]]s as ordinary [[monoid]]s and [[E-infinity ring]]s as ordinray [[commutative monoid]]s in a suitable [[category]].

## Prehistory

As a first step one wants a [[model category]] $\mathcal{S}$ of spectra that [[presentable (infinity,1)-category|presents]] the full [[(infinity,1)-category]] of [[spectrum|spectra]]. This allows to model the notion of equivalence of spectra and of [[homotopy|homotopies]] between maps of spectra.  Several such model categories 
have been known for a long time; all are Quillen equivalent and their common [[homotopy category]] is called "the" [[stable homotopy category]] $Ho \mathcal{S}$.

It was also known that the stable homotopy category $Ho \mathcal{S}$ is a [[symmetric monoidal category]], via a "derived [[smash product of spectra]]."  Ordinary (commutative) [[monoid]]s in $Ho \mathcal{S}$ were called (commutative) **[[ring spectrum|ring spectra]]**.  While their product has associativity and uniticity up to homotopy, these homotopies are not specified and not required to satisfy higher coherence laws up to higher homotopies themselves.

One could, however, try to build in coherent associativity (resp. commutativity) homotopies by the use of an [[operad]], by using an $A_\infty$-operad (resp. an $E_\infty$-operad).  This resulted in the notions of **$A_\infty$-[[A-infinity-ring|ring spectrum]]** and **$E_\infty$-[[E-infinity-ring|ring spectrum]]**, which have a much better-behaved theory.

## Symmetric monoidal categories of spectra

Now, for some of the model categories $\mathcal{S}$ of spectra, the smash product on $Ho \mathcal{S}$ can be lifted to a functor
$$
  \wedge\colon \mathcal{S} \times \mathcal{S} \to \mathcal{S}
  \,,
$$
but for the most part these functors were neither associative nor unital nor commutative at the level of the 1-category $\mathcal{S}$.  In fact, Gaunce Lewis proved a theorem that there could be *no* symmetric monoidal category $\mathcal{S}$ modeling the stable homotopy category and satisfying a couple of other natural requirements.

However, in the 1990s it was realized that by dropping one or another of Lewis' other requirements, symmetric monoidal categories of spectra could be produced.  The first such category was the category of **[[S-module]]s** described by Elmendorf, Kriz, Mandell, and May, but others soon followed, including **[[symmetric spectrum|symmetric spectra]]** and **[[orthogonal spectrum|orthogonal spectra]]**.  All of these form symmetric [[monoidal model categories]] which are symmetric-monoidally Quillen equivalent.

Moreover, in all of these cases, the monoidal structure on the model category $\mathcal{S}$ absorbs all the higher coherent homotopies that used to be supplied by the action of an $A_\infty$ or $E_\infty$ operad.  Thus, honest (commutative) monoids in $\mathcal{S}$ model the same "(commutative) ring objects up to all coherent higher homotopies" that are modeled by the classical $A_\infty$ and $E_\infty$ ring spectra, and for this reason they are often still referred to as $A_\infty$ or $E_\infty$ ring spectra, respectively.

### $S$-modules

The construction of $S$-modules by EKMM begins with the notion of [[coordinate-free spectrum|coordinate free Lewis-May spectra]].  Using the [[linear isometries operad]], one can construct a [[monad]] $\mathbb{L}$ on the category $\mathcal{S}$ of such spectra, and the category of $\mathbb{L}$-algebras is a well-behaved model for the stable homotopy category, and moreover admits a smash product which is associative up to isomorphism, but unital only up to weak equivalence.  However, the subcategory of the $\mathbb{L}$-algebras for which the unit transformations are isomorphisms is again a well-behaved model for $Ho \mathbb{S}$, which is moreover symmetric monoidal.

Since the unit transformation is of the form $S\wedge E \to E$, where $S$ is the [[sphere spectrum]], and this map looks like the action of a ring on a module, the objects of this subcategory are called **$S$-modules** and the category is called $Mod_S$.  The intuition is that just as an abelian group is a [[module]] over the archetypical ring $\mathbb{Z}$ of [[integer|integers]], a spectrum should be regarded as a module over the archetypal ring spectrum, namely the sphere spectrum.

Similarly, just as an ordinary [[ring]] is a [[monoid]] in the category $Mod_\mathbb{Z}$ of $\mathbb{Z}$-[[module]]s, i.e. a $\mathbb{Z}$-algebra, an $A_\infty$ or $E-\infty$ ring spectrum is a (possibly commutative) monoid in the category of $S$-modules, and thus referred to as an **$S$-algebra**.  More generally, for any $A_\infty$-[[A-infinity-ring|ring spectrum]] $R$, there is a notion of $R$-[[module]] spectra forming a category $Mod_R$, which in turn carries an associative and commutative smash product $\wedge_R$ and a [[model category]] structure on $Mod_R$ such that $\wedge_R$ becomes unital in the [[homotopy category]].  All this is such that an $A_\infty$-[[A-infinity-algebra|algebra]] over $R$ is a [[monoid object]] in $(Mod_R, \wedge_R)$.  Similarly $E_\infty$-[[E-infinity-algebra|algebras]] are commutative monoid objects in $(Mod_R, \wedge_R)$.

### Symmetric spectra

...

### Orthogonal spectra

...

## Related concepts

* [[mapping spectrum]]

## References

### Original sources


In the mid-1990s, several categories of spectra with nice smash products were discovered, and simultaneously,
model categories experienced a major renaissance. 1993, Elmendorf, Kriz, Mandell and May
introduced the S-modules and [[Jeff Smith]] gave the first talks about symmetric spectra; the details of
the model structure were later worked out and written up in 

* [[Mark Hovey]], [[Brooke Shipley]], [[Jeff Smith]], _Symmetric spectra_, J. Amer. Math. Soc. 13 (2000), 149-208.



### Reviews and introductions

A survey of the general theory, also of its history, is

* A. Elmendorf, [[Igor Kriz]], [[Peter May|P. May]], _Modern foundations for stable homotopy theory_ ([pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf))

The definition of $S$-modules and their theory can be found in 

* A. Elmendorf, [[Igor Kriz]], M. Mandell, [[Peter May|P. May]], *Rings, modules and algebras in stable homotopy theory* (aka "EKMM")

A textbook account of the theory of symmetric spectra is  

* [[Stefan Schwede]], _Symmetric spectra_ ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))

Seminar notes on symmetric spectra are in

* [[Sander Kupers]], _[[SymmetricSpectra.pdf:file]]_

See also

* wikipedia [highly structured ring spectrum](http://en.wikipedia.org/wiki/Highly_structured_ring_spectrum)


[[!redirects S-module]]
[[!redirects S-modules]]
[[!redirects symmetric spectrum]]
[[!redirects symmetric spectra]]
[[!redirects orthogonal spectrum]]
[[!redirects orthogonal spectra]]

[[!redirects smash product of spectra]]

[[!redirects structured ring spectrum]]
[[!redirects structured ring spectra]]

[[!redirects symmetric monoidal smash product of spectra]]
