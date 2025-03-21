This entry is about the notion of spectrum in [[stable homotopy theory]]. For other uses of the term ''spectrum'' see [[spectrum - disambiguation]].


***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea 

A [[topological space|topological]] spectrum is an [[object]] in the universal [[stable (∞,1)-category]] $Sp(Top) \simeq Sp(\infty Grpd)$ that stabilizes the [[(∞,1)-category]] [[Top]] or $\simeq$ [[∞-Grpd]] of [[topological spaces]] or [[∞-groupoids]] under the operations of forming [[loop space objects]] and [[reduced suspensions]]: the [[stable (∞,1)-category of spectra]].

More generally, one may consider [[spectrum objects]] in any [[presentable (∞,1)-category]].

### Connective and non-connective spectra; infinite loop spaces

As opposed to the [[homotopy groups]] of a [[topological space]], the [[homotopy groups of a spectrum]] are defined and may be non-trivial in _negative_ integer degree. This follows from the fact that the [[loop space]] operation is by construction invertible on spectra, which implies that for every spectrum $E$ these and all $n$, the $n$-fold looping $\Omega^n$ has [[stable homotopy groups]] given by $\pi_{k-n}(\Omega^n E) \simeq \pi_k(E)$.

Those spectra for which the [[homotopy groups of spectra]] in negative degree happen to vanish are called _[[connective spectra]]_. They are equivalent to [[infinite loop spaces]], i.e. grouplike [[E-∞ spaces]].

Connective spectra in the image of the [[nerve]] operation of the classical [[Dold-Kan correspondence]]: this identifies [[∞-groupoids]] that are not only connective spectra but even have a _strict_ symmetric monoidal [[group]] structure with non-negatively graded [[chain complex|chain complexes]] of abelian groups. 

$$
 \array{
  Ch_+ &\stackrel{Dold-Kan \; nerve}{\to}&
  ConnectSp(\infty Grp) \subset \infty Grpd
  \\
  (\cdots A_2 \stackrel{\partial}{\to} A_1 \stackrel{\partial}{\to} A_0 \to 0 \to 0 \to \cdots)
  &\stackrel{}{\mapsto}&
  N(A_\bullet)
 }
$$

The [[homology]] groups of the chain complex correspond precisely to the [[homotopy groups]] of the corresponding [[topological space]] or [[∞-groupoid]].

The free stabilization of the [[(∞,1)-category]] of non-negatively graded chain complexes is simply the [[stable (∞,1)-category]] of arbitrary chain complexes. There is a [[stable Dold-Kan correspondence]] (see at _[[module spectrum]]_ the section _[stable Dold-Kan correspondence](module+spectrum#StableDoldKanCorrespondence)_ ) that identifies these with special objects in $Sp(Top)$. 

$$
 \array{
  Ch &\stackrel{Dold-Kan \; nerve}{\to}&
   Sp(\infty Grp) 
  \\
  (\cdots A_2 \stackrel{\partial}{\to} A_1 \stackrel{\partial}{\to} A_0 \stackrel{\partial}{\to} A_{-1} 
  \stackrel{\partial}{\to} A_{-2} \to \cdots)
  &\stackrel{}{\mapsto}&
  N(A_\bullet)
 }
$$

So it is the homologically nontrivial parts of the chain complexes in negative degree that corresponds to the non-connectiveness of a spectrum.

## Definition 

There are many "models" for spectra, all of which present the same ([[stable homotopy theory|stable]]) [[homotopy theory]] (and in fact, nearly all of them are [[Quillen equivalence|Quillen equivalent]] [[model category|model categories]]).  For more details see at _[[Introduction to Stable Homotopy Theory]]_.

### Sequential pre-spectra
 {#SequentialPreSpectra}

A simple first definition is to define a [[pre-spectrum]] $\mathbf{E}$ to be a sequence of pointed spaces $(E_n)_{n\in\mathbb{N}}$ together with structure maps $\Sigma{}E_n\to{}E_{n+1}$ (where $\Sigma$ denotes the [[reduced suspension]]). See at _[[model structure on sequential spectra]]_.

There are various conditions that can be put on the spaces $E_n$ and the structure maps, for example if the spaces are CW-complexes and the structure maps are inclusions of subcomplexes, the spectrum is called a **[[CW-spectrum]]**.

Without any condition, this is just called a **spectrum**, or sometimes a **[[pre-spectrum]]**. In order to distinguish from various other richer definitions (such as [[coordinate-free spectra]], one also speaks of _[[sequential spectra]]_).

For details see _[[Introduction to Stable homotopy theory -- 1-1|Introduction to stable homotopy theory -- 1.1 Sequential Spectra]]_.

### $\Omega$-spectra
 {#OmegaSpectrum}

If $\Omega$ denotes the [[loop space]] functor on the category of pointed spaces, we know that $\Sigma$ is left adjoint to $\Omega$.
In particular, given a spectrum $\mathbf{E}$, the structure maps can be transformed into maps $E_n\to\Omega{}E_{n+1}$.
If these maps are isomorphisms (depending on the situation it can be weak equivalences or homeomorphisms), then $\mathbf{E}$ is called an **$\Omega$-spectrum**.

The idea is that $E_0$ contains the information of $\mathbf{E}$ in dimensions $k\ge 0$, $E_1$ contains the information of $\mathbf{E}$ in $k\ge -1$ (but shifted up by one, so that it is modeled by the $\ge 0$ information in the space $E_1$), and so on.

$\Omega$-spectra are special cases of [[sequential spectrum|sequential]] pre-spectra as [above](#SequentialPreSpectra), and are in fact the [[fibrant objects]] for some [[model structure on spectra]].

Given any sequential pre-spectrum $\mathbf{E}$, it induces an equivalent $\Omega$-spectrum $\mathbf{F}$ (a fibrant replacement of $\mathbf{E}$, its _[[spectrification]]_) given by ([Lewis-May-Steinberger 86, p. 3](#LewisMaySteinberger86))

$$
  F_n \coloneqq \lim_{m\to\infty}\Omega^m E_{n+m}
$$ 

(using that $\Omega$ commutes with the [[filtered colimits]]).


### Coordinate-free spectra 

A definition of spectrum consisting of spaces indexed by index sets less "coordinatized" than the integers is a 

* [[coordinate-free spectrum]].

See there for details.

### Combinatorial spectra

There might be a type of categorical structure related to a spectrum in the same way that $\infty$-categories are related to $\infty$-groupoids.  In other words, it would contain $k$-cells for all integers $k$, not necessarily invertible.  Some people have called this conjectural object a **$Z$-category**.   "Connective" $Z$-categories could perhaps then be identified with stably monoidal $\infty$-categories.

One realization of this kind of idea is the notion of [[combinatorial spectrum]].

### General context

See [[spectrum object]].

## Examples 

* [[suspension spectrum]]

* [[sphere spectrum]]

* [[Eilenberg-MacLane spectrum]]

* [[K-theory spectrum]]

* [[elliptic spectrum]]

* [[tmf]]

* [[Thom spectrum]], [[complex cobordism spectrum]]


## Properties

### Stabilization

In direct analogy to how topological spaces form the archetypical example, [[Top]], of an [[(∞,1)-category]], spectra form the archetypical example $Sp(Top)$ of a [[stable (∞,1)-category]]. In fact, there is a general procedure for turning any [[pointed category|pointed]] [[(∞,1)-category]] $C$ into a stable $(\infty,1)$-category $Sp(C)$, and doing this to the category $Top_*$ of [[pointed object|pointed]] spaces yields $Sp(Top)$.

### Symmetric monoidal structure

* [[smash product of spectra]]

* [[symmetric monoidal smash product of spectra]]


### Closed structure

* [[mapping spectrum]]

### Model category structure

* [[model structure on spectra]]

### Relation to symmetric monoidal ∞-groupoids

* [[stable homotopy hypothesis]]

## Related concepts

* [[homotopy group of a spectrum]]

* [[sheaf of spectra]], [[parametrized spectrum]]

  * [[smooth spectrum]]

* [[spectrum with G-action]], [[G-spectrum]]

* [[ring spectrum]], [[algebra spectrum]], [[module spectrum]]

* [[zero spectrum]]

* [[finite spectrum]]

* [[p-local spectrum]]

* [[Bousfield localization of spectra]]

* [[motivic spectrum]]

* [[Brown representability theorem]]

* [[stable homotopy hypothesis]]

[[!include k-monoidal table]]

## References

According to ([Adams 74, p. 131](#Adams74)) the notion of spectrum is due to 

* {#Lima58} E. L. Lima, _Duality and Postnikov invariants_, Thesis, University of Chicago, Chicago 1958

> It is generally supposed that [[George Whitehead|G. W. Whitehead]] also had something to do with it, but the latter takes a modest attitude about that. ([Adams 74, p. 131](#Adams74))

Early notes include

* {#Boardman65} [[Michael Boardman]], _Stable homotopy theory_, mimeographed notes, University of Warwick, 1965 onward

* {#Adams74} [[Frank Adams]], Part III, section 2 _[[Stable homotopy and generalised homology]]_, 1974

See the references at _[[stable homotopy theory]]_.

Lecture notes include

* _[[Introduction to Stable homotopy theory -- 1-1|Introduction to stable homotopy theory -- 1.1 Sequential Spectra]]_

More modern developments are due to

* {#LewisMaySteinberger86} [[L. Gaunce Lewis]], [[Peter May]], M. Steinberger, _Equivariant stable homotopy theory_, Springer Lecture Notes in Mathematics, 1986 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/equi.pdf))

The quick idea is surveyed for instance in

* [[Cary Malkiewich]], _The stable homotopy category_, 2014 ([pdf](http://math.stanford.edu/~carym/stable.pdf))

* [[Aaron Mazel-Gee]], _An introduction to spectra_ ([pdf](https://math.berkeley.edu/~aaron/writing/an-introduction-to-spectra.pdf))

The first review of stable homotopy theory with [[symmetric monoidal smash product of spectra]] is (in terms of [[S-modules]]) in

* {#ElmendorfKrizMay95} [[Anthony Elmendorf]], [[Igor Kriz]], [[Peter May]], _[[Modern foundations for stable homotopy theory]]_, in [[Ioan Mackenzie James]], _[[Handbook of Algebraic Topology]]_, Amsterdam: North-Holland, (1995) pp. 213&#8211;253,  ([pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf))

A comprehensive account of the symmetric model in terms of [[symmetric spectra]] is in

* [[Stefan Schwede]], _Symmetric spectra_ ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))

and in terms of [[orthogonal spectra]] in

* [[Stefan Schwede]], _[[Global homotopy theory]]_ (take $\mathcal{F} = \{1\}$, on p. 4, to be the trivial collection of groups, in order to specialize from [[global equivariant stable homotopy theory]] to plain stable homotopy theory).

See also

* [[Robert Thomason]], _Symmetric Monoidal Categories Model All Connective Spectra_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.37.8193))

* [[Frank Adams]], _Infinite loop spaces_, Princeton University Press, 1978 


* {#Ayoub} [[Joseph Ayoub]], _Les six op&#233;rations de Grothendieck et le formalisme des cycles &#233;vanescents dans le monde motivique, I_. Ast&#233;risque, Vol. 314 (2008). Soci&#233;t&#233; Math&#233;matique de France. ([pdf](http://user.math.uzh.ch/ayoub/PDF-Files/THESE.PDF))


[[!redirects spectra]]

