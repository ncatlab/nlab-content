
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

## Motivation

The original motivation for the notion of *separable functors* &lbrack;[Năstăsescu, van den 
Bergh & van Oystaeyen (1989)](#NăstăsescuVanDenBerghVanOystaeyen89)&rbrack;
was the functorial form of [[Maschke's theorem]] over [[rings]] and its various cousins: namely the classical Maschke's theorem about finite [[group rings]] over [[fields]], generalizes to the statements that when the [[order of a group|order of the group]] is [[invertible element|invertible]] in the [[ground ring]] then the [[split exact sequence|splitting]] of an [[exact sequence]] of [[group representation|$k G$-modules]] can be obtained [[functor|functorially]] from its splitting as an exact sequence of [[underlying]] 
[[module|$k$-modules]].

This "Maschke property" of the  [[forgetful functor]] ${}_{k G} Mod\to {}_{k}Mod$ is what is generalized by the notion of separable functors.

A further example appears in the study of [[ring extensions]] $f \colon R\to S$: Such is separable iff the corresponding [[restriction of scalars]]-functor $\operatorname{Res}_R^S \colon {}_{S}Mod \to {}_{R}Mod$ is a separable functor. 

## Definition

Let $F \colon C\to D$ be a [[functor]] with [[hom-set]] components
$$
\array{
F_{x,y} 
\colon
&
C(x,y)&\longrightarrow& D(F x,F y)
\\
&
(x\stackrel{f}\to y)&\mapsto& (F x\stackrel{F f}\to F y)
\mathrlap{\,.}
}
$$
Then $F$ is called *separable* &lbrack;[Năstăsescu, van den 
Bergh & van Oystaeyen (1989), p. 398](#NăstăsescuVanDenBerghVanOystaeyen89)&rbrack; if each $F_{x,y}$ has a [[section]] which is "natural" in $x$ and $y$, in a suitable sense.

## Properties

\begin{theorem}
**(Rafael's theorem)** 
Let $F\dashv G$ be a pair of [[adjoint functors]]. Then 

* $F$ is separable iff the [[adjunction unit]] $\eta \con id \to G F$ has a [[section]] (= a [[natural transformation]] $\nu$ which is its right inverse, $\eta\circ\nu = 1$),

* $G$ is separable iff the [[adjunction counit]] $\epsilon \colon F G \to id$ has a [[retraction]] (i.e. a natural transformation $\zeta$ that is its left inverse, $\zeta\circ\epsilon =1$). 

\end{theorem}

The latter condition is reminiscent of one of the many equivalent definitions of a [[separable algebra]] $A$ over a field, namely one for which multiplication, viewed as an $(A,A)$-[[bimodule]] map $A \otimes A^{\mathrm{op}} \to A$, has a  right inverse. 


## Literature

Separable functors were defined in 

* {#NăstăsescuVanDen BerghVanOystaeyen89} [[Constantin Năstăsescu]], [[Michel van den Bergh]], [[F. van Oystaeyen]], _Separable functors applied to graded rings_, J. Algebra __123__ (1989) 397-413 &lbrack;<a href="http://dx.doi.org/10.1016/0021-8693(89)90053-7">doi:10.1016/0021-8693(89)90053-7</a>&rbrack;

Now there is a monograph available:

* S. Caenepeel, G. Militaru, S. Zhu, _Frobenius and separable functors for generalized module categories and nonlinear equations_, Lec. Notes in Math. __1787__, Springer (2002) xiv+354 pp. 

Other references

* M. D. Rafael, _Separable functors revisited_, Comm. in Algebra __18__ (1990), 1445-1459.

* S. Caenepeel, B. Ion, G. Militaru, _The structure of Frobenius algebras and separable algebras_,  $K$-Theory __19__ (2000),  no. 4, 365--402. 

* J. G&#243;mez-Torrecillas, _Separable functors in [[corings]]_, 
Int. J. of Math. and Math. Sci. __30__ (2002), 4, Pages 203-225, [doi](http://dx.doi.org/10.1155/S016117120201270X), [pdf](http://www.emis.de/journals/HOA/IJMMS/Volume30_4/225.pdf)

* A. Ardizzoni, _Separable functors and [[formal smoothness]]_,  J. K-Theory  1  (2008),  no. 3, 535--582, [math.QA/0407095](http://arxiv.org/abs/math.QA/0407095), [doi](http://dx.doi.org/10.1017/is007011015jkt012), [MR2009k:16069](http://www.ams.org/mathscinet-getitem?mr=2009k:16069)

* A. Ardizzoni, [[G. Böhm]], C. Menini, _A Schneider type theorem for Hopf algebroids_, J. Algebra __318__ (2007), no. 1, 225&#8211;269 [MR2008j:16103](http://www.ams.org/mathscinet-getitem?mr=2363132) [doi](http://dx.doi.org/10.1016/j.jalgebra.2007.05.017) [math.QA/0612633](http://arxiv.org/abs/math/0612633) (arXiv version is unified, corrected); _Corrigendum_, J. Algebra __321__:6 (2009) 1786-1796 [MR2010b:16060](http://www.ams.org/mathscinet-getitem?mr=2498268) [doi](http://dx.doi.org/10.1016/j.jalgebra.2008.11.040)

The following article studies formal smoothness and generalizes the separable functors to the context of the so-called [[S-category|S-categories]] which are introduced therein:

* [[T. Brzeziński]], _Notes on formal smoothness_, *in*: Modules and Comodules (series _Trends in Mathematics_). T Brzezi&#324;ski, JL Gomez Pardo, I Shestakov, PF Smith (eds), Birkh&#228;user, Basel, 2008, pp. 113-124 ([doi](http://dx.doi.org/10.1007/978-3-7643-8742-6), [arXiv:0710.5527](http://arxiv.org/abs/0710.5527)) 

[[!redirects separable functors]]