
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

##Idea

The notion of _Cartan-Eilenberg categories_  is a tool in [[homotopical algebra]].

The structure of a _Cartan-Eilenberg category_ ([SAPR 10](#SAPR)) on a [[category]] is the structure of a [[category with weak equivalences]] equipped with the further data of "strong" equivalences inducing a notion of [[cofibrant objects]], such that the [[localization]] of the category at the weak equivalences is equivalently that of the [[full subcategory]] of cofibrant objects at just the strong equivalences.

The motivation for this axiomatics in ([SAPR 10](#SAPR)) is that it is the general context in which the original construction in ([Cartan-Eilenberg 56](#CartanEilenberg56)) of [[derived functors]] of [[additive functors]] between [[categories of modules]] generalizes.

Every [[model category]] is in particular a Cartan-Eilenberg category, the strong equivalences in this case are the left [[homotopy equivalences]].
But the notion of CE-categories is weaker and exists in situations where a full model category structure is not available. In this way the notion of Cartan-Eilenberg category structures is analogous to other such structures in between [[categories with weak equivalences]] and fully-fledged model categories, such as [[categories of fibrant objects]], [[Waldhausen categories]] etc.

In this  approach to [[homotopical algebra]], there is a ambient [[category]], $\mathcal{C}$, in which there are two classes $\mathcal{S}$ and $\mathcal{W}$ of distinguished [[morphisms]] called the _strong_ and the _[[weak equivalences]]_ and with $S\subseteq W$.  An [[object]] of the category $\mathcal{C}$ is said to be _[[cofibrant object|cofibrant]]_ if any morphism from it to the [[codomain]] of a [[weak equivalence]] [[lifting property|lifts]] uniquely to one from it to the domain within the category $\mathcal{C}[\mathcal{S}^{-1}]$, obtained by [[localization|inverting]] the _strong_ equivalences. (Note as the context is slightly different _cofibrant_ means something slightly different here.)



## Definition



A triple $(\mathcal{C},\mathcal{S},\mathcal{W})$ is called a (left) _Cartan-Eilenberg category_ if every object has a cofibrant left model that is, for each object, $X$, of $\mathcal{C}$, there is a cofibrant object, $M$, and a morphism $q: M\to X$ in $\mathcal{C}[\mathcal{S}^{-1}]$, which is an isomorphism in $\mathcal{C}[\mathcal{W}^{-1}]$. 


## Properties


 These Cartan-Eilenberg categories have the property that $\mathcal{C}[\mathcal{W}^{-1}]$ is equivalent to a relative [[localisation]] of the category of cofibrant objects with respect to strong equivalences.

## References

The original constructions from which "Cartan-Eilenberg categories" got their name are due to

* [[Henri Cartan]], [[Samuel Eilenberg]], _Homological Algebra_. Princeton University Press, 1956
 {#CartanEilenberg56}

The abstraction of _Cartan-Eilenberg categories_ then appears in

* F. Guill&#233;n Santos, Vicente Navarro Aznar, Pere Pascual, Agusti Roig, _A Cartan-Eilenberg approach to Homotopical Algebra_, [arxiv/0707.3704](http://arxiv.org/abs/0707.3704) and J. Pure Applied. Alg. 214 (2010) 140 - 164.
 {#SAPR}

Further discussion is in

* Pere Pascual, _Some remarks on Cartan-Eilenberg categories_, [pdf](http://upcommons.upc.edu/e-prints/bitstream/2117/9290/1/prepr201001pascual.pdf) and Collect. Math. 63, No. 2, 203-216 (2012); 

* Pere Pascual, _Cartan-Eilenberg categories and descent categories_, [pdf](http://www.ma1.upc.edu/recerca/reports-recerca/repre-2009/Fitxers/rep200902pascual.pdf)

* Joana Cirici, Francisco Guill&#233;n, _Homotopy theory of mixed Hodge complexes_, [arxiv/1304.6236](http://arxiv.org/abs/1304.6236)

[[!redirects Cartan-Eilenberg structure]]
[[!redirects Cartan-Eilenberg categories]]