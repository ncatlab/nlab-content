 
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

## Idea {#Idea}

As for [[localization]] of ordinary [[categories]], there are slightly different notions of what a localization of an [[(∞,1)-category]] is.

One definition is in terms of [[simplicial localizations]] or [[quasicategory of fractions]]; another is in terms of [[reflective (∞,1)-subcategories]]:

A [[localization]] in the first sense is a functor $L:C \to D $ of $\infty$-categories that is initial among the functors inverting a prescribed set of morphisms of $C$.

A _[[localization]]_ , in the second sense, of an [[(∞,1)-category]] $C$ is a functor $L : C \to C_0$ to an $(\infty,1)$-subcategory $C_0 \hookrightarrow C$ such that with $c$ any object there is a morphism connecting it to its localization 

$$
  c \to L(c)
$$

in a suitable way. This "suitable way" just says that 
$f$ is left adjoint to the fully faithful inclusion functor.


Since localizations are entirely determined by which morphisms in $C$ are sent to equivalences in $C_0$, they can be thought of as sending $C$ to the result of "inverting" all these morphisms, a process familiar from forming the [[homotopy category]] of a [[homotopical category]].



## Definitions

As explained in [Idea](#Idea), there are two common definitions that are referred to as localizations of $\infty$-categories.

The following definition appears in [kerodon, tag01MP](https://kerodon.net/tag/01MP).

+-- {: .un_defn}
###### Definition

Let $C$ be an $\infty$-category and $W$ a set of morphisms of $C$. A functor $L:C\to D$ is said to exhibit $D$ as a **(Dwyer--Kan)** **localization of $C$ with respect to $W$** if for each $\infty$-category $E$, the functor

$$\operatorname{Fun}(D,E)\to \operatorname{Fun}(C,E)$$

is fully faithful and its essential image consists of those functors $C\to E$ that carry each morphism of $W$ into equivalences of $E$.
=--

The following second definition appears in [[Higher Topos Theory|HTT, def. 5.2.7.2]]:

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

+-- {: .un_rem}
###### Remark
Reflective localizations are a special case of Dwyer--Kan localizations. This is  [kerodon, tag04JL](https://kerodon.net/tag/04JL).
=--

## Examples

* Localizations of $(\infty,1)$-categories are modeled by the notion of left [[Bousfield localization of model categories]]. 

  One precise statement is: localizations of [[(∞,1)-category of (∞,1)-presheaves]] $C = PSh_{(\infty,1)}(K)$ are [[presentable (∞,1)-category|presented]] by the left Bousfield localizations of the global projective [[model structure on simplicial presheaves]] on the [[simplicial category]] incarnation of $K$.

* [[∞-stackification]] (or [[(∞,1)-sheafification]]) is the localization of an [[(∞,1)-category]] of [[(∞,1)-presheaves]] to the $(\infty,1)$-subcategory [[(infinity,1)-category of (infinity,1)-sheaves|of (∞,1)-sheaves]].

* [[cohomology localization]]

* [[homotopy localization]]

## References

Reflective localization is the topic of 

* [[Jacob Lurie]], §5.2.7 & §5.5.4 of: *[[Higher Topos Theory]]* (2009)
* [[Jacob Lurie]], _Kerodon_,&lbrack;[Reflective Localizations, tag:02FY](https://kerodon.net/tag/02FY)&rbrack;

Dwyer--Kan localization (also called [[simplicial localizations]] or [[quasicategory of fractions]]) are treated in

* [[Jacob Lurie]], _Kerodon_,&lbrack;[Localization, tag:01M4](https://kerodon.net/tag/01M4)&rbrack;
* [[Markus Land]], Section 2.4 of _Introduction to Infinity-Categories_, Compact Textbooks in Mathematics,Birkh\"auser/Springer, Cham, (2021) &lbrack;[doi:10.1007/978-3-030-61524-6](https://doi.org/10.1007/978-3-030-61524-6)&rbrack;
* [[Jacob Lurie]], pp. 485 of: *[[Higher Algebra]]* (2017)

With an eye towards [[modal homotopy type theory]]:

* [[Marco Vergura]], *Localization Theory in an Infinity Topos*, 2019 ([pdf](https://ir.lib.uwo.ca/cgi/viewcontent.cgi?article=8583&context=etd), [ir.lib.uwo.ca:etd/6257](https://ir.lib.uwo.ca/etd/6257))

Via a [[calculus of fractions]] for [[quasi-categories]]:

* [[Daniel Carranza]], [[Chris Kapulkin]], [[Zachery Lindsey]], *Calculus of Fractions for Quasicategories* &lbrack;[arXiv:2306.02218](https://arxiv.org/abs/2306.02218)&rbrack;


[[!redirects localization of an (∞,1)-category]]
[[!redirects localisation of an (infinity,1)-category]]
[[!redirects localisation of an (∞,1)-category]]
[[!redirects localizations of an (infinity,1)-category]]
[[!redirects localizations of an (∞,1)-category]]
[[!redirects localisations of an (infinity,1)-category]]
[[!redirects localisations of an (∞,1)-category]]
[[!redirects localizations of (infinity,1)-categories]]
[[!redirects localizations of (∞,1)-categories]]
[[!redirects localisations of (infinity,1)-categories]]
[[!redirects localisations of (∞,1)-categories]]
[[!redirects localization of (infinity,1)-categories]]
[[!redirects localization of (∞,1)-categories]]
[[!redirects localisation of (infinity,1)-categories]]
[[!redirects localisation of (∞,1)-categories]]

[[!redirects localization of a quasi-category]]
[[!redirects localization of quasi-categories]]

