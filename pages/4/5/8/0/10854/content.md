
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Cohomology
+-- {: .hide}
[[!include cohomology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

### In physics

In [[physics]] and especially in [[continuum mechanics]] and [[thermodynamics]], a physical quantity associated with a [[physical system]] extended in [[space]] is called

* _intensive_ if it is a [[function]] on (the physical system extended in) space;

* _extensive_ if it is a [[density]] or [[linear distribution]] on (the physical system extended in) space.

For instance, for a [[solid body]] its [[temperature]] is intensive, but its [[mass]] is extensive: there is a temperature assigned to every point of the body (in the idealization of [[classical mechanics|classical]] [[continuum mechanics]] anyway) but a mass is assigned only to every little "extended" piece of the body, not to a single point.

This terminology in [[physics]] appears vaguely in ([Hegel 1812](#Hegel1812)), [Hegel 1817](#Hegel1817)), more precisely in ([Grassmann 1844](#Grassmann1844)) and in its fully modern form is maybe due to [[Richard Tolman]] ([1917](#Tolman1917)).

If we take into account that a physical system may or may not have a particular kind of quantity (for example, a thermodynamic system may or may not have a temperature), a system has a value of an intensive quantity if and only if all of its subsystems have a value of that quantity, and then all of these values are equal.  However, it's generally safe to assume that every system has a value of every extensive quantity.

To be precise, given a system $S_0$ made up of the subsystems $S_1$ and $S_2$:

*  For an intensive quantity $q$, $S_0$ has a value $q_0$ of $q$ if and only if $S_1$ and $S_2$ also have values of $q$, and then we have $q_1 = q_0$ and $q_2 = q_0$.

*  For an extensive quantity $Q$, all three systems have values of $Q$, and we have $Q_0 = Q_1 + Q_2$.


### In geometry and algebra

In ([Lawvere 86](#Lawvere86)) it is amplified that this [[duality]] is generally a fundamental one also in [[mathematics]]: given a [[topos]] $\mathbf{H}$ with a [[commutative ring|commutative]] [[ring object]] $R \in CRing(\mathbf{H})$, then 

* the space of _intensive quantities_ on an [[object]] $X \in \mathbf{H}$ is the [[mapping space]] $[X,R]_{\mathbf{H}} \in CRing(\mathbf{H})$ formed in $\mathbf{H}$;

* the space of _extensive quantities_ on $X$ is the $R$-linear dual, namely the mapping space $[X,R]^\ast \coloneqq [[X,R], R]_{R Mod}$ formed in $R$-[[modules]] in $\mathbf{H}$.

  (here the operation $[[-,R],R]_{R Mod}$ happens to be what is also called the "[[continuation monad]]" for $R$)

* the [[integration]] map is the canonical [[evaluation]] pairing

  $$
    \int_X \;\colon\; [X,R] \times [X,R]^\ast  \longrightarrow R
    \,.
  $$

$$ (x, f) \mapsto f(x) $$

See also at _[[Lawvere distribution]]_.

The elusive connection between integration and (co)ends can here be explained:

**Proposition:** Let $V$ be a monoidal closed category with tensor $\otimes_V$ and internal hom $[-, -]_V$. Suppose that the Kan extension $\text{Lan}_{\text{Id}_V} (\text{Id}_V)$ exists and is pointwise. Then
 $$ X \cong \text{Id}_V (X) \cong \text{Lan}_{\text{Id}_V} (\text{Id}_V)(X) \cong \int^{Y \in V} [Y, X]_V \otimes_V Y$$
and the structure maps are 
$$ \epsilon_Y : [Y, X]_V \otimes_V Y \rightarrow X$$
Occuring as counits in the supposed monoidal closed adjunction.

This is an instance of the [coend formula for a Kan extension](https://ncatlab.org/nlab/show/Kan+extension#PointwiseByCoEnds). 

We may think of $V$ as the category of $R$-module objects in a topos $\mathbf{H}$, or, more generally, some category $\mathbf{H}$ resembling spaces. In that case, we get:

**Corollary:** Let $\mathbf{H}$ be a category with internal hom $[-, -]_{\mathbf{H}}$, and let $R$ be a commutative ring object in $\mathbf{H}$. Let $R \text{-mod}$ be the category of $R$-module objects in $\mathbf{H}$, with a chosen monoidal closed structure $\otimes_R$ (tensor product) and $[-, -]_R$ (internal Hom). Then, taking $V = R \text{-mod}$ above, and supposing that $\text{Lan}_{\text{Id}_{R \text{-mod}}} (\text{Id}_{R \text{-mod}})$ we have

$$ R \cong  \int^{X \in R \text{-mod}} [X, R]_R  \otimes_R X  $$ 

with structure maps:

$$ \epsilon_X : [X, R]_R \otimes_R X \rightarrow R $$

In the above notation, $ \epsilon_X = \int_X$. To make the analogy quite clear, consider the following example, which could naturally be called the example of "Lawvere Banach spaces", in direct analogy with "Lawvere metric spaces":

**Example:** Let $\mathbf{H}$ be the category of [Lawvere metric spaces](https://ncatlab.org/nlab/show/metric+space#LawvereMetricSpace) (Note: this category is not a topos, but the corollary above will still apply).  Maps are short maps. $\mathbf{H}$ has an internal Hom consisting of bounded maps. Let $\mathbb{R}$ be the real numbers, with $d(x, y) = ||x - y||$ as Lawvere metric. $\mathbb{R} \text{-mod}$ is here the category of normed $\mathbb{R}$-modules, with short maps as maps, with the exception that $||x|| = 0$ does not imply that $x = 0$, and that $||x|| = \infty$ is possible. (This temporary notation is not to be confused with the category of real vector spaces over the real numbers, in which norms play no role).

There is a natural notion of [completion](https://ncatlab.org/nlab/show/Cauchy+complete+category) on such spaces. The category of complete objects is essentially the category of Banach spaces over $\mathbb{R}$, except for the previously mentioned differences that $||x|| = 0$ does not imply that $x = 0$, and $||x|| = \infty$ is possible. Completion makes this category into a reflective subcategory of $\mathbb{R}$-mod. Write $\text{LawvBan}$ for the this category - it is a natural continuation of Lawvere metric spaces.

There is a natural choice of monoidal closed structure on $\text{LawvBan}$; the tensor product is [projective tensor product](https://ncatlab.org/nlab/show/tensor+product+of+Banach+spaces) (note: slight tweaking is necessary to account for the differences between Lawvere Banach spaces and Banach spaces). The internal Hom consists of bounded maps. The corollary above applies to this setup, so that 

$$ R \cong  \int^{X \in R \text{-mod}} [X, R]_R  \otimes_R X  $$ 

where $\otimes_R$ is projective tensor product and $[X, R]_R$ consists of bounded maps from $X$ to $R$. There are structure maps

$$ \epsilon_X : [X, R]_R \otimes_R X \rightarrow R $$

sending $f \otimes x$ to $f(x)$, for which we suggestively write 

$$ \int_X : [X, R]_R \otimes_R X \rightarrow R $$


### In higher geometry and higher algebra

Viewed this way, this naturally generalizes to the case where $\mathbf{H}$ is in fact an [[(∞,1)-topos]] and $R \in CRing(\mathbf{H})$ an [[E-∞ ring]]. In this case $[X,R]$ is called the  $R$-[[cohomology]] [[spectrum]] of $X$ and $[X,R]^\ast$ is the corresponding [[generalized homology]] spectrum. In this form intensive and extensive properties appear in [[physics]] in the context of [[motivic quantization]] of [[local prequantum field theory]]. 

More generally, for $\chi$ an $R$-[[(∞,1)-line bundle]] over $X$ then the corresponding extensive object is the $\chi$-twisted [[Thom spectrum]] $R_{\bullet + \chi}(X)$ and the intensive object is the $\chi$-[[twisted cohomology]] [[spectrum]] $R^{\bullet + \chi}(X) = [R_{\bullet+ \chi}(X),R]_{R Mod}$. See at _[[motivic quantization]]_ for how this appears in [[physics]].

## In modal homotopy type theory

Assume we are working in the context of a [[cohesive (∞,1)-topos]], $\mathbf{H}$, with the three [[adjoint modalities]], [[shape modality]] $\dashv$ [[flat modality]] $\dashv$ [[sharp modality]] $\int \dashv \flat \dashv \sharp$.

We may characterize the codomains of those [[functions]] which are _intensive_ or _extensive quantities_ in terms of $\sharp$.

* **Intensive**: functions whose value is genuinely given by their restriction to all possible points have as codomains types $X$ that are fully determined by their moment of continuity, that is those for which $X \to \sharp X$ is a [[monomorphism]]. In [[categorical semantics]] these are the [[concrete objects]] or equivalently the [[separated presheaves]] for $\sharp$: they are determined by their global points. 

* **Extensive**: objects which have purely the [[negative moment]] of continuity $\overline{\sharp}$, or, in other words, which are maximally  non-concrete, form codomains for "functions" which vanish on points and receive their contribution only from regions that _extend_ beyond a single point. For example, the smooth moduli space of differential $n$-forms is maximally non-concrete. This concept of _extension_ is precisely that which gave the name to [[Hermann Grassmann]]'s _[[Ausdehnungslehre]]_ that introduced the concept of [[exterior algebra|exterior]] [[differential form]].

So, the adjunction $(\flat \dashv \sharp)$ expresses _quantity_, discrete quantity and continuous quantity, and the latter is further subdivided into intensive and extensive quantity.


## References

The concepts of intensive and extensive quantity are highlighted in

* {#Grassmann1814} [[Hermann Grassmann]], _[[Ausdehnungslehre]]_, 1844

which states (p. xxiv, xxv) that intensive quantity is the topic of [[differential calculus]] and [[integration]] theory, while extensive quantity is the topic of this very _Ausdehnungslehre_.

General discussion includes

* Wikipedia, _[Intensive and extensive properties](http://en.wikipedia.org/wiki/Intensive_and_extensive_properties)_

A formalization in [[categorical logic]]/[[topos theory]] is proposed in

* {#Lawvere86} [[William Lawvere]], Introduction to _[[Categories in Continuum Physics]], Lectures given at a Workshop held at SUNY, Buffalo 1982. Lecture Notes in Mathematics 1174. 1986

See also the exposition of his ideas at [Higher toposes of laws of motion](Higher+toposes+of+laws+of+motion#iii_extensiveintensive_duality_and_cohomological_quantization).
 
Lawvere's terminology is probably (see at _[[objective logic]]_) inspired by  

* {#Hegel1812} [[Georg Hegel]], section _[Extensives und Intensives Quantum](Science+of+Logic#ExtensiveAndIntensiveQuantity)_, in _[[Science of Logic]]_, 1812

* {#Hegel1817} [[Georg Hegel]], part II "Philosophy of Nature", second section "Physics", B, [&#167;298b](Science+of+Logic#PN298b) in _[[Encyclopedia of the Philosophical Sciences]]_

and meant to be a formalization of this part of the "[[objective logic]]", see also at _[[Science of Logic]]_.

The first use of the terms 'intensive' and 'extensive' appears to be

* [[Richard Tolman]] (1917). The Measurable Quantities of Physics. Physical Review 9 (3): 237--253.


[[!redirects intensive or extensive]]
[[!redirects intensive or extensive quantity]]
[[!redirects intensive or extensive quantities]]
[[!redirects intensive and extensive]]
[[!redirects intensive and extensive quantities]]
[[!redirects extensive or intensive]]
[[!redirects extensive or intensive quantity]]
[[!redirects extensive or intensive quantities]]
[[!redirects extensive and intensive]]
[[!redirects extensive and intensive quantities]]

[[!redirects intensive and extensive quantity]]
[[!redirects extensive and intensive quantity]]

[[!redirects intensive]]
[[!redirects intensive quantity]]
[[!redirects intensive quantities]]

[[!redirects extensive]]
[[!redirects extensive quantity]]
[[!redirects extensive quantities]]

[[!redirects intensive and extensive quantity]]
[[!redirects intensive and extensive quantities]]
