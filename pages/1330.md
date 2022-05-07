
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

As for [[localization]] of ordinary [[categories]], there are slightly different notions of what a localization of an [[(∞,1)-category]] is.

One definition is in terms of [[reflective (∞,1)-subcategories]]:

A _[[localization]]_ , in this sense, of an [[(∞,1)-category]] $C$ is a functor $L : C \to C_0$ to an $(\infty,1)$-subcategory $C_0 \hookrightarrow C$ such that with $c$ any object there is a morphism connecting it to its localization 

$$
  c \to L(c)
$$

in a suitable way. This "suitable way" just says that 
$f$ is left adjoint to the fully faithful inclusion functor.


Since localizations are entirely determined by which morphisms in $C$ are sent to equivalences in $C_0$, they can be thought of as sending $C$ to the result of "inverting" all these morphisms, a process familiar from forming the [[homotopy category]] of a [[homotopical category]].



## Definition

+-- {: .un_defn}
###### Definition

An [[(∞,1)-functor]] $L : C \to C_0$ is called a **localization** of the [[(∞,1)-category]] $C$ if it has a right [[adjoint (∞,1)-functor]] $i : C_0 \hookrightarrow C$ that is [[full and faithful (∞,1)-functor|full and faithful]].

$$
  (L \dashv i) : C_0 \stackrel{\overset{L}{\leftarrow}}{\underset{i}{\hookrightarrow}}
  C
  \,.
$$

In other words: $L$ is a localization if it is the **reflector** of a [[reflective (∞,1)-subcategory]] $C_0 \hookrightarrow C$.

=--

This is [[Higher Topos Theory|HTT, def. 5.2.7.2]].


## Examples

* Localizations of $(\infty,1)$-categories are modeled by the notion of left [[Bousfield localization of model categories]]. 

  One precise statement is: localizations of [[(∞,1)-category of (∞,1)-presheaves]] $C = PSh_{(\infty,1)}(K)$ are [[presentable (∞,1)-category|presented]] by the left Bousfield localizations of the global projective [[model structure on simplicial presheaves]] on the [[simplicial category]] incarnation of $K$.

* [[∞-stackification]] (or [[(∞,1)-sheafification]]) is the localization of an [[(∞,1)-category]] of [[(∞,1)-presheaves]] to the $(\infty,1)$-subcategory [[(infinity,1)-category of (infinity,1)-sheaves|of (∞,1)-sheaves]].

* [[cohomology localization]]

* [[homotopy localization]]

## References

This is the topic of section 5.2.7  and 5.5.4 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

With an eye towards [[modal homotopy type theory]]:

* [[Marco Vergura]], *Localization Theory in an Infinity Topos*, 2019 ([pdf](https://ir.lib.uwo.ca/cgi/viewcontent.cgi?article=8583&context=etd), [ir.lib.uwo.ca:etd/6257](https://ir.lib.uwo.ca/etd/6257))


[[!redirects localization of an (∞,1)-category]]
[[!redirects localisation of an (infinity,1)-category]]
[[!redirects localization of an (∞,1)-category]]
[[!redirects localizations of an (infinity,1)-category]]
[[!redirects localizations of an (∞,1)-category]]
[[!redirects localisations of an (infinity,1)-category]]
[[!redirects localizations of an (∞,1)-category]]
[[!redirects localizations of (infinity,1)-categories]]
[[!redirects localizations of (∞,1)-categories]]
[[!redirects localisations of (infinity,1)-categories]]
[[!redirects localizations of (∞,1)-categories]]
[[!redirects localization of (infinity,1)-categories]]
[[!redirects localization of (∞,1)-categories]]
[[!redirects localisation of (infinity,1)-categories]]
[[!redirects localization of (∞,1)-categories]]