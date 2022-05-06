
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

_Grothendieck categories_ are those [[abelian category|abelian categories]] $\mathcal{A}$

* such that for [[presheaf|presheaves]] on a [[site]] with values in $\mathcal{A}$ there is an existence theorem for the  [[sheafification]] functor;

* such that all [[complexes]] in $\mathcal{A}$ (with respect to a [[category with translation|translation]]) are [[quasi-isomorphism|quasi-isomorphic]] to [[injective object|homotopically injective]] complexes (so that [[derived functor on a derived category|derived functor]] can be computed on homotopically injective replacements).


## Definition

In terms of the AB$n$ hierarchy discussed at [[additive and abelian categories]] we have

A **Grothendieck category** is an [[additive and abelian categories|AB5-category]] which has a [[separator|generator]].

This means that a **Grothendieck category** is an [[abelian category]]

* that admits a [[separator|generator]];

* that admits small [[colimits]];

* such that small [[filtered category|filtered]] [[colimits]] are _[[exact functor|exact]]_ in the following sense:

  * for $I$ a [[direction|directed set]] and $0 \to A_i \to B_i \to C_i \to 0$ an [[exact sequence]] for each $i \in I$, then $0 \to colim_i A_i \to colim_i B_i \to colim_i C_i \to 0$ is also an [[exact sequence]].

Dually a *co-Grothendieck category* is an AB5$^*$ category 
with a [[cogenerator]]. The category of abelian groups is not a co-Grothendieck category. Any abelian category which is simultaneously Grothendieck and co-Grothendieck has just a single object (see Freyd's book, p.116). 


## Properties

A Grothendieck category $C$ satisfies the following properties.

* it admits small [[limits]];

* if a functor $F : C^{op} \to Set$ commutes with small [[limits]], the $F$ is [[representable functor|representable]];

* if a functor $F : C^{op} \to Set$  commutes with small [[colimits]], then $F$ has a [[adjoint functor|right adjoint]].

* The [[Gabriel-Popescu theorem]] exhibits any [[Grothendieck abelian category]] as a [[reflective subcategory]] of a [[category of modules]] over a [[ring]].  In particular, [[Vopěnka's principle]] implies that any [[Grothendieck abelian category]] is [[locally presentable]].

* If $C$ is equipped with [[category with translation|translation]] $T : C \to C$, then for every [[complex]] $X \in Cplx(C)$ there exists a [[quasi-isomorphism]] of [[complex]]es $X \to I$ such that $I$ is [[injective object|homotopically injective]].

* it satisfies Pierre Gabriel's sup property: every small family of subobjects of a given object $X$ has a [[supremum]] which is a subobject of $X$; 

* it admits an [[injective object|injective]] [[cogenerator]] (see [Kashiwara-Schapira](#KS), Theorem 9.6.3). 

Much of the localization theory of rings generalizes to general Grothendieck categories. 

## Examples

* For $R$ a [[commutative ring]], its [[category of modules]] $R$[[Mod]] is a Grothendieck category. (see e.g [Kiersz 06, prop. 4](#Kiersz) for the proof that filtered colimits here are exact.)

* For $C$ a [[small category|small]] [[abelian category]], the category $Ind(C)$ of [[ind-objects]] in $C$ is a Grothendieck category.

* for $C$ a Grothendieck category, the category $C_c$ of [[complex]]es in $C$ is again a Grothendieck category.

## Related concepts

* [[sheaf of abelian groups]]

* [[abelian sheaf cohomology]]


## References

Grothendieck categories are mentioned at the end of section 8.3 in

* {#KS} [[Masaki Kashiwara]], [[Pierre Schapira]], _[[Categories and Sheaves]]_

The relation to complexes is in section 14.1.

The proof that filtered colimits in $R Mod$ are exact is spelled out for instance in 

* {#Kiersz} Andy Kiersz, _Colimits and homological algebra_, 2006 ([pdf](http://www.math.uchicago.edu/~may/VIGRE/VIGRE2006/PAPERS/Kiersz.pdf))

See also 

* [[Peter Freyd]], _Abelian categories_, Harper (1966O) 
* Nicolae Popescu, _An introduction to Abelian categories with applications to rings and modules_, Academic Press 1973

The duality of Grothendieck categories with categories of modules over [[linearly compact ring]]s is discussed in

*  U. Oberst, _Duality theory for Grothendieck categories and linearly compact rings_, J. Algebra __15__ (1970), p. 473 --542, []()

Discussion of [[model structures on chain complexes]] in Grothendieck abelian categories is in

* [[Denis-Charles Cisinski]], F. D&#233;glise, _Local and stable homologial algebra in Grothendieck abelian categories_, Homology, Homotopy and Applications, vol. 11 (1) (2009)  ([pdf](http://www.intlpress.com/HHA/v11/n1/a11/v11n1a11.pdf))

[[!redirects Grothendieck categories]]

[[!redirects Grothendieck abelian category]]
[[!redirects Grothendieck abelian categories]]
