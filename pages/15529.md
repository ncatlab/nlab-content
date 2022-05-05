[[!redirects empty 112]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}


## Idea

> Lex-total categories are the good notion of topos. ([[Ross Street]], [1981](#Street81) p.201)

A **lex total category** is a category whose [[Yoneda embedding]] is a [[localization]] thereby generalizing [[Giraud's theorem|Giraud's characterization]] of [[Grothendieck topos|Grothendieck toposes]] as localizations of [[presheaf topos|presheaf toposes]] hence they can be viewed as a candidate for a notion of "topos".

## Definition

Recall that a locally small category $\mathcal{C}$ is called [[total category|total]] if the [[Yoneda embedding]] $Y:\mathcal{C}\hookrightarrow Set^{\mathcal{C}^{op}}$ has a left adjoint $L$.

+-- {: .num_defn}
###### Definition
A locally small category $\mathcal{C}$ is called _lex total_ if the [[Yoneda embedding]] $Y:\mathcal{C}\hookrightarrow Set^{\mathcal{C}^{op}}$ has a [[left exact]] (=finite limit preserving) left adjoint $L$.

=--

## Examples

In particular, [[totally distributive category|totally distributive categories]] where $L$ has a further left adjoint $W$ are lex total.

Below we will see that all [[Grothendieck toposes]] are lex total. 

## Properties

+-- {: .num_prop}
###### Theorem
A lex total category $\mathcal{E}$ is a [[Grothendieck topos]] iff $\mathcal{E}$ has a small set of [[generator|generators]].
=--

The result was announced by Walters on the [[Isle of Thorns]] in 1976, a proof can be found in Street ([1981](#Street81), p.206). More detailed information on this characterization in particular concerning the size issues involved and the algebraic perspective it avails can be found at [[Grothendieck topos]] or the [blog posts](#Walters14) by Bob Walters.

## Related entries

* [[total category]]

* [[totally distributive category]]

## Link

* {#Walters14}[[Bob Walters]], _Lex total categories and Grothendieck toposes I-IV_ , series of blog posts 2014. ([link](http://rfcwalters.blogspot.com/2014/07/lex-total-categories-and-grothendieck.html))

## References

* {#LW11} [[Rory Lucyshyn-Wright]], _Totally distributive toposes_ , arXiv:1108.4032 (2011). ([abstract](https://arxiv.org/abs/1108.4032))

* [[Ross Street]], _The family approach to total cocompleteness and toposes_ , Trans. A. M. S. **284** (1978) pp.355-369.

* {#Street81}[[Ross Street|R. Street]], _Notions of topos_ , Bull. Austral. Math. Soc. **23** no.2 (1981) pp.199-208.

* {#SW78}[[Ross Street|R. Street]], [[Bob Walters|R. Walters]], _Yoneda structures on 2-Categories_ , JA **50** no.2 (1978) pp.350-379.

* R.J. Wood, _Some remarks on total categories_ , JA **75** no.2 (1982) pp.538-545.

[[!redirects lex total categories]]
[[!redirects lex-total categories]]
[[!redirects lex-total category]]
[[!redirects Lex total category]]
[[!redirects Lex total categories]]