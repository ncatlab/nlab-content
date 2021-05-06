+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

[[!redirects coHeyting algebra]]
[[!redirects Co-Heyting algebra]]
[[!redirects CoHeyting algebra]]
[[!redirects bi-Heyting algebra]]
[[!redirects biHeyting agebra]]
[[!redirects Brouwerian algebra]]


##Idea

When the [[lattice of open subsets]] of a [[topological space]] is the primordial example of a [[Heyting algebra]] then its dual _lattice of [[closed subsets]]_ is the primordial example of a **co-Heyting algebra**.

In general, co-Heyting algebras are [[duality|dual]] to Heyting algebras and like them come equipped with non-Boolean logical operators that make them interesting players in [[modal logic|modal]], [[paraconsistent logic|paraconsistent]], and co-intuitionistic logic, [[linguistics]], [[topos theory]], [[continuum physics]], [[quantum theory]] and in [[mereology]].

##Definition

A **co-Heyting algebra** is a bounded [[distributive lattice]] $L$ equipped with a binary _[[subtraction]]_ operation $ \backslash :L\times L\to L$ such that $x\backslash y\leq z$ iff $x\leq y\vee z$.[^Dist]

[^Dist]: Existence of $\backslash$ amounts to an [[adjunction]] \_$\backslash y\dashv y\vee$\_ and the existence of a left adjoint implies that $y\vee$\_ preserves limits $\wedge$ hence the assumption of distributivity in the definition is redundant and has been put in for emphasis only.

A **bi-Heyting algebra** is a bounded distributive lattice $L$ that carries a Heyting algebra structure with implication $\Rightarrow$ and a co-Heyting algebra structure with subtraction $\backslash$.

## Remarks

* Co-Heyting algebras were initially called _Brouwerian algebras_ . Bi-Heyting algebras were introduced and studied in a series of papers by Cecylia Rauszer in the 1970s who called them _semi-Boolean algebras_ which suggests to view them as a generalization of [[Boolean algebra|Boolean algebras]].

* A [[topos]] $\mathcal{E}$ such that the lattice $sub(X)$ of subobjects is a bi-Heyting algebra for every object $X\in\mathcal{E}$ is called a [[bi-Heyting topos]].

## Examples

* The lattice of closed subsets of a topological space is a co-Heyting algebra with $X\backslash Y=\overline{X\cap Y^c}\quad$.

* A Boolean algebra provides a (degenerate) example of a bi-Heyting algebra by setting $x\Rightarrow y:=\neg x\vee y$ and $x\backslash y:=x\wedge\neg y$.

* An [[irreflexive]] [[comparison]], such as an [[apartness relation]] or a [[linear order]], is a [[(0,1)-category]] [[enriched category|enriched]] on the co-Heyting algebra $\Omega^\op$, where $\Omega$ is the Heyting algebra of [[truth values]].

##Properties

* $a\backslash b=0$ iff $a\backslash b\leq 0$ iff $a\leq b\vee 0$ iff $a\leq b$. In particular, $a\backslash a=0$.

* As \_$\backslash x$ has a right adjoint it preserves colimits hence: $(a\vee b)\backslash x =(a\backslash x)\vee (b\backslash x)\quad$.

* $a\backslash 0\leq a\backslash 0$ iff $a\leq 0\vee (a\backslash 0)$ iff $a\leq a\backslash 0\quad$. On the other hand, $a\leq 0\vee a$ and the adjunction yield $a\backslash 0\leq a\quad$, hence $a\backslash 0 = a\quad$.

* Suppose $a\leq b\vee x $ then $a\backslash b\leq x$. As from $a\backslash b\leq a\backslash b$ follows $a\leq b\vee (a\backslash b)$, hence $a\backslash b =\Wedge\{x|a\leq b\vee x\}\quad$.

* The subtraction operation permits to define the [[co-Heyting negation]] $\sim: L\to L$, called _non a_ in Lawvere (1991), by setting $\sim a:=1\backslash a$.

* $\sim$ in turn can then be used to define the [[co-Heyting boundary|co-Heyting boundary operator]] $\partial :L\to L$ by $\partial a:=a\wedge\sim a$. That $\partial a$ is not necessary trivial is dual to the non-validity of the _tertium non datur_ for general Heyting algebras and points to the utility of co-Heyting algebras for [[paraconsistent logic]].

* In [[bi-Heyting toposes]] like e.g. [[essential subtoposes]] of presheaf toposes ([Lawvere](#Law91a), [Reyes](#Reyes)), the co-Heyting algebra operations are generally not preserved by [[inverse image functor|inverse image functors]], so that the co-Heyting logical operators are subject to _[[de re and de dicto]]_ effects. The parallel between this and the [[commutator]] in quantum mechanics has been suggested by Lawvere thereby somewhat anticipating the view of D&#246;ring (2013). 

##Related entries

* [[co-Heyting negation]]
* [[co-Heyting boundary]]
* [[Heyting algebra]]
* [[Heyting category]]
* [[distributive category]]
* [[mereology]]
* [[bi-Heyting topos]]
* [[bitopological space]]

##References

* G. Bellin, _Categorical Proof Theory of Co-Intuitionistic Linear Logic_ , arXiv:1407.341 (2014). ([pdf](http://arxiv.org/pdf/1407.3416v1))

* G. Bezhanishvili, N. Beshanishvili, D. Gelaia, A. Kurz, _Bitopological duality for distributive lattices and Heyting algebras_ , Math. Struc. Comp. Sci. **20** no.3 (2010) pp.359-393. ([preprint](http://www.cs.le.ac.uk/people/nb118/Publications/PairwiseStone.pdf))

* [[Andreas Döring|A. Döring]], _Topos-based Logic for Quantum Systems and Bi-Heyting Algebras_ , arXiv:1202.2750 (2013). ([pdf](http://arxiv.org/pdf/1202.2750.pdf))

* {#RRZ94} M. La Palme Reyes, J. Macnamara, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _The non-Boolean logic of natural language negation_ , Phil. Math. **2** no.1 (1994) pp.45-68.

* M. La Palme Reyes, J. Macnamara, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _Models for non-Boolean negation in natural languages based on aspect analysis_ , pp.241-260 in Gabbay, Wansing (eds.), _What is Negation?_, Kluwer Dordrecht 1999. 

* {#RRZ04} M. La Palme Reyes, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _Generic Figures and their Glueings_ , Polimetrica Milano 2004.

* {#Law86} [[William Lawvere|F. W. Lawvere]], _Introduction_ , pp.1-16 in Lawvere, Schanuel (eds.), _Categories in Continuum Physics_ , Springer LNM **1174** 1986.

* {#Law91a} [[William Lawvere|F. W. Lawvere]], _Intrinsic Co-Heyting Boundaries and the Leibniz Rule in Certain Toposes_ , pp.279-281 in A. Carboni, M. Pedicchio, G. Rosolini (eds.) ,  _[[Como|Category Theory - Proceedings of the International Conference held in Como 1990]]_ , LNM **1488** Springer Heidelberg 1991.

* T. Mormann, _Heyting Mereology as a Framework for Spatial Reasoning_ , Axiomathes **23** no.1 (2013) pp.237-264. ([draft](http://philpapers.org/go.pl?id=MORCMA-3&proxyId=&u=http%3A%2F%2Fphilpapers.org%2Farchive%2FMORCMA-3.pdf))

* {#Reyes}[[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari,  _Bi-Heyting Algebras, Toposes and Modalities_ , J. Phi. Logic **25** (1996) pp.25-43.

* C. Rauszer, _Semi-Boolean algebras and their applications to intuitionistic logic with dual operations_ , Fund. Math. **83** no.3 (1974) pp.219-249. ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm83/fm83120.pdf))

* J.G. Stell, M.F. Worboys, _The algebraic structure of sets of regions_ , pp.163-174 in Hirtle, Frank (eds.), _Spatial Information Theory_, Springer LNCS **1329** (1997).

* [[Marshall Stone|M. H. Stone]], _Topological representation of distributive lattices and Brouwerian logics_ , Cas. Mat. Fys. **67** (1937) pp.1-25. ([pdf](http://dml.cz/bitstream/handle/10338.dmlcz/124080/CasPestMatFys_067-1938-1_1.pdf))

* F. Wolter, _On logics with coimplication_ , J. Phil. Logic **27** (1998) pp.353-387. ([draft](http://lips.informatik.uni-leipzig.de/files/1998-24.pdf))