
# $\Lambda$-maximal consistent formulae
* table of contents
{: toc}

## Definition

Given a [[normal modal logic]], $\Lambda$,  a set, $\Gamma$, of formulae is said to be __$\Lambda$-consistent__ if $\neg(\Gamma\vdash_\Lambda \bot)$, i.e., $\bot$ is not [[modal logic|deducible]] from $\Gamma$.

A set, $\Gamma$, of formulae is said to be __$\Lambda$-maximal__ if it is consistent and, for any $\phi \in \mathcal{L}_\omega(n)$ either $\phi\in \Gamma$ or $\neg\phi\in \Gamma$.

+-- {.un_remark #important}
###### Important

If $\Gamma$ is a $\Lambda$-maximal set of formulae, then within the [[Lindenbaum-Tarski algebra]], $\mathfrak{A}^\Lambda_\omega$, the set $x_\Lambda = \{{\|\phi\|} \mid \phi \in \Lambda\}$ is an [[ultrafilter]].
=--


## Canonical frame

Let $S^\Lambda_\omega = \{\Gamma \mid \Gamma \in \Lambda maximal\}$,  then $\Gamma\leftrightarrow x_\Gamma$ is a bijection between $S^\Lambda_\omega$ and the set of [[ultrafilters]] of $\mathfrak{A}^\Lambda_\omega$.

This set forms the set of states / worlds for the **canonical frame** of $\Lambda$.  The relations are given by 

$$R_i \Gamma\Delta \;iff\; \Diamond_i\Delta \subseteq \Gamma.$$


[[!redirects maximal consistent]]
[[!redirects maximal consistent formula]]
[[!redirects maximal consistent formulas]]
[[!redirects maximal consistent formulae]]
