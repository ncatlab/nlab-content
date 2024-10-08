
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _Henselian ring_ is a [[local ring]] for which the conclusion of [[Hensel's lemma]] (classically stated for a [[complete local ring]]) holds.

## Definition 

+-- {: .num_defn}
###### Definition 

Let $R$ be a local ring with [[maximal ideal]] $m$. Let $k = R/m$ be the residue class [[field]], and for a [[polynomial]] $f \in R[x]$, let $\bar{f} \in k[x]$ obtained by [[reduction mod p|reduction]] of the coefficients of $f$ modulo $m$. Then $R$ is _Henselian_ if, for any [[monic polynomial|monic]] $f \in R[x]$ such that $\bar{f}$ factorizes as $g_0 h_0$ with $g_0, h_0$ monic and relatively prime in $k[x]$, there exist monic $g, h \in R[x]$ such that $f = g h$ with $\bar{g} = g_0$, $\bar{h} = h_0$, and the ideal $(g, h)$ is the unit ideal in $R[x]$. 

=-- 

Often this definition is given just for the case when one of $g_0$, $h_0$ is a linear factor $x - a$, where the idea is that the (simple) root $a$ can be lifted to $R$. 

+-- {: .num_defn}
###### Definition 

A Henselian ring $R$ with residue class field $k$ is _strictly Henselian_ if $k$ is separably closed. 

=-- 

## Examples 

* Any field $k$ is trivially Henselian. 

* A complete local ring, such as [[p-adic number]] rings, is Henselian. This includes rings of formal power series over a field, $k[ [x_1, \ldots, x_n] ]$. 

* Rings of convergent power series over a [[local field]] are Henselian. 

## Properties 

+-- {: .num_prop} 
###### Proposition
 
The quotient of a Henselian ring is also Henselian. 

=-- 

+-- {: .proof}
###### Proof 

In the first place, a quotient $R'$ of a local ring $R$ is local (and has the same residue class field $k$). Secondly, $R'$ is clearly Henselian since we can lift factorizations $\bar{f} = g_0 h_0$ in $k[x]$ to factorizations in $R[x]$, and then push them down to $R'[x]$. 

=-- 

+-- {: .num_prop}
###### Proposition 

If $R$ is local and its reduced ring (i.e., $R$ modulo its ideal of nilpotent elements) is Henselian, then $R$ itself is Henselian. 

=-- 

+-- {: .num_prop} 
###### Proposition 

If $R$ is Henselian and $S$ is a local ring that is integral over $R$ (meaning that $S$ is an $R$-algebra and each $x \in S$ is an [[integral closure|integral element]] over $R$), then $S$ is Henselian. 

=-- 

## Henselization 

Let $LocRing$ denote the category of local rings (commutative of course) and local ring homomorphisms ($f: R \to S$ is _local_ if the pullback along $f$ of the maximal ideal of $S$ is the maximal ideal of $R$). 

+-- {: .num_theorem} 
###### Theorem 

The full subcategory of $LocRing$ consisting of Henselian rings is reflective. The left adjoint to the full inclusion is called _Henselization_. 

=-- 

+-- {: .num_example}
###### Example 

Let $R$ be a [[valuation ring|discrete valuation ring]], with $K$ its field of fractions. Let $\hat{R}$ be the $m$-adic completion of $R$ with respect to its maximal ideal. Then the Henselization of $R$ is isomorphic to the subring of $\hat{R}$ whose elements are roots of separable polynomials with coefficients in $K$. 

=-- 

A rule of thumb, as suggested by this example, is that the Henselization is the algebraic part of a local ring completion. 

## Related concepts

* [[restricted formal power series]]
* [[Henselian pair]]

## References

An original reference is

* [[Alexandre Grothendieck]],  (1967), [[EGA]]: IV. _&#201;tude locale des sch&#233;mas et des morphismes de sch&#233;mas_ , Quatri&#232;me partie", Publications Math&#233;matiques de l'IH&#201;S 32: 5&#8211;361. ([web](http://www.numdam.org/numdam-bin/feuilleter?id=PMIHES_1967__32_)) 

Lecture notes are in 

* [[James Milne]], section 4 of _[[Lectures on Étale Cohomology]]_

Other sources include

* Michel Raynaud, _Anneaux locaux hens&#233;liens_, Lecture Notes in Mathematics Volume **169** 1970 doi:[10.1007/BFb0069571](https://dx.doi.org/10.1007/BFb0069571)

* [[Jacob Lurie]], [[Descent Theorems]], section 3.

* Alonso, Lombardi, Perdry, _Henselian local rings_ ([pdf](http://drops.dagstuhl.de/volltexte/2006/437/pdf/05021.PerdryHerve.Paper.437.pdf))

* Krzysztof Jan Nowak, _Remarks on Henselian rings_ ([pdf](http://www.emis.de/journals/UIAM/PDF/46-79-85.pdf));

* [[Ieke Moerdijk]], _Rings of smooth functions and their localizations_ ([pdf](http://nlab.mathforge.org/nlab/files/RingsOfSmoothFunctionsI.pdf))

[[!redirects Hensel ring]]
[[!redirects Hensel rings]]
[[!redirects Henselian rings]]
[[!redirects henselian ring]]
[[!redirects henselian rings]]