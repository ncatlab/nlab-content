
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _integral transform_ on [[functions]] is a [[linear map]] between functions on [[spaces]] $X$, $Y$ encoded by a function $K$ (or [[generalized function]], e.g. [[distribution of two variables]]) on the [[product]] space $X \times Y$ and given by a formula of the type

$$
  (function\;f\;on\;X) \mapsto
  \left(y \mapsto
  \int_{X} f(x) K(x,y) \right)
  \,,
$$

where on the right we have some kind of [[integration]] over $X$.

Here $K$ is called the integral **kernel** of the transformation.


Typically the definition of an integral transform on functions involves some delicate technical issues concerning the precise nature of the function space, the [[measure]] with respect to which the integral is defined, etc.

On the other hand, one may understand the general form of an integral transform as the [[decategorification]] of a very natural general abstract construction in [[higher category theory]]: that of [[integral transforms on sheaves]] given by spans of [[base change geometric morphism]]s.

Special cases of such [[categorification|categorified]] integral transforms are discussed at

* [[Schwartz kernel]] ([[distribution of two variables]])

* [[Fourier-Mukai transform]], [[topological T-duality]]

* [[groupoidification]]

* [[geometric infinity-function theory]].

## Examples

* The simplest example is [[matrix multiplication]], which corresponds to the case where $X$ and $Y$ are [[discrete space]]s.

* Standard examples involving genuine [[functional analysis]] are for instance the [[Fourier transform]] and related [[Laplace transform]], [[Mellin transform]], [[Hankel transform]], [[Hilbert transform]].

* Also the [[path integral]] in [[quantum mechanics]] and [[quantum field theory]] is supposed to be a class of examples of a (secondary) integral kernel.

* [[Fourier-Mukai transform]]

* [[Penrose transform]]

* [[Hecke transform]]

* [[Harish Chandra transform]]

## History
 {#History}

In [[noncommutative algebraic geometry]], one of the most important results is [[Dmitri Orlov]]'s representability theorem (1997) which states that every fully faithful [[triangulated functor]] between the [[derived categories]] of [[coherent sheaves]] on two [[smooth scheme|smooth]] [[projective varieties]] is representable by some "[[integral kernel]]", i.e., a coherent complex on the [[product]].  One would like to remove the "fully faithful" assumption, but this has proved extremely difficult so far.  In the context of [[dg-categories]] the analogous result, discovered by [[Bertrand Toen]] in 2004, does have the clean form one would like it to.  Along with other problems with [[triangulated categories]], this has been one of the motivations for people like [[Maxim Kontsevich]] and [[Goncalo Tabuada]] to start doing [[noncommutative geometry]] with [[pretriangulated dg-categories]] instead of triangulated categories.

On the other hand [[pretriangulated dg-categories]] are known to provide a model for linear [[stable (infinity,1)-categories]].  Using a different model, like [[quasi-categories]], would be more convenient for extending Toen's theorem from (smooth proper) schemes to (smooth proper) [[derived stacks]].  This was done in [Ben-Zvi & Francis & Nadler 08](#BZFN08).  In the followup ([Ben-Zvi & Nadler & Preygel 13](#BZNP13)) the authors have also extended these results to the non-smooth case.

## Related concepts

* [[polynomial functor]]

* [[Schwartz kernel]]

* [[heat kernel]]

* [[kernel method]]

## References
 {#References}

Discussion of integral kernels in the sense of [[functional analysis]] (as in the [[Schwartz kernel theorem]]) is in

* {#Treves67} [[François Trèves]], _Topological Vector Spaces, Distributions and Kernels_ (Academic Press, New York, 1967)


Discussion of integral transforms in [[derived algebraic geometry]] (see also at _[[geometric infinity-function theory]]_) is in

* {#BZFN08} [[David Ben-Zvi]], [[John Francis]], [[David Nadler]], _Integral Transforms and Drinfeld Centers in Derived Algebraic Geometry_ ([arXiv:0805.0157](http://arxiv.org/abs/0805.0157))
  

* {#BZNP13} [[David Ben-Zvi]], [[David Nadler]], Anatoly Preygel, _Integral transforms for coherent sheaves_ ([arXiv:1312.7164](http://arxiv.org/abs/1312.7164))
 

Comments on the formalization of integral transforms and [[quantization]] in [[dependent linear type theory]] are at

* _[[schreiber:Type-semantics for quantization]]_ 

category: analysis, geometry
[[!redirects integral transforms]]
[[!redirects integral kernel]]
[[!redirects integral kernels]]