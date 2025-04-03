
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
* table of contents
{:toc}

## Definition

An object $c$ in an ordinary $Set$-enriched [[category]] $C$ is called **[[tiny object|atomic]]** if $hom(c,-)$ preserves small colimits.  The category $C$ itself is called **atomic** if it has a [[small set|small]] [[dense subcategory|dense]] [[full subcategory]] of atomic objects, $Atom(C)$, so that every object $c$ of $C$ is a small colimit of the functor 

$$Atom(C) \downarrow c \stackrel{proj}{\to} Atom(C) \stackrel{i}{\hookrightarrow} C.$$

More generally, for $V$ a [[cosmos]], a $V$-[[enriched category]] $C$ is _atomic_ if it admits a small $V$-dense full subcategory of atomic objects $Atom(C)$, such that every object $c$ is an enriched coend 

$$\int^{a \in Atom(C)} C(i a, c) \cdot i a.$$ 

## Properties

### Relation to presheaf toposes


\begin{theorem}
A category is [[equivalence of categories|equivalent]] to a [[category of presheaves]], hence of the form $[C^{op}, Set]$, if and only if it is [[cocomplete category|cocomplete]] and atomic. 
\end{theorem}

See [Centazzo, Rosický & Vitale 2004](#Centazzo-Rosický-Vitale04) for a proof.  


## Related concepts

* [[atom]] 

* [[tiny object]]

* [[compact object]]

* [[Cauchy completion]]


## References

* {#Centazzo-Rosický-Vitale04} Claudia Centazzo, [[Jiří Rosický]], [[Enrico M. Vitale]]: *A characterization of locally $D$-presentable categories*, [[Cahiers]] de topologie et géométrie différentielle catégoriques **45** 2 (2004) 141-146 &lbrack;[numdam:CTGDC_2004__45_2_141_0](https://www.numdam.org/item/CTGDC_2004__45_2_141_0), [pdf](https://perso.uclouvain.be/enrico.vitale/ClaudiaJiri.pdf)&rbrack;


[[!redirects atomic categories]]
