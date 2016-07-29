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

[[!redirects coHeyting negation]]
[[!redirects Co-Heyting negation]]
[[!redirects supplement]]
[[!redirects bi-Heyting negation]]
[[!redirects Brouwerian negation]]

## Idea

In a [[co-Heyting algebra]] it is possible to define a [[negation|negation operator]] $\sim$ which validates the _law of excluded middle_ but invalidates the _law of non-contradiction_ dual to the negation in a [[Heyting algebra]].

## Definition

Let $a$ be an element of a [[co-Heyting algebra]] $L$ with subtraction $\backslash$. The **co-Heyting negation** of $a$ , called _non a_ (Lawvere 1991) or the _supplement_ of $a$, is defined as $\sim a:=1\backslash a$.

## Remark

A [[co-Heyting algebra|bi-Heyting algebra]] is naturally equipped with two negation operators: the Heyting negation $\neg$ and the co-Heyting supplement $\sim$. Both coincide in a Boolean algebra considered as a bi-Heyting algebra.

In applications, such co-occuring pairs of negation operators $\neg$ and $\sim$ are the most interesting cases as their combination give rise to [[adjoint modalities]] e.g. in mereology they yield _thickened boundaries_ (Stell&Worboys 1997). Beside [[mereology]] they have found applications in [[linguistics]], [[intuitionistic logic]] and [[physics]].

## Properties

*  $\sim a$ minimally supplements $a$ to truth in the sense that $\sim a$ is the least $x$ with $a\vee x=1$. This follows from the adjointness of $\backslash$ which unwinds as $\sim a\leq x$ iff $1=a\vee x$.

* $\sim 1=0$ and $\sim 0= 1$.

* $\sim$ can be used to define the [[co-Heyting boundary|co-Heyting boundary operator]] $\partial :L\to L$ by $\partial a:=a\wedge\sim a$. That $\partial a$ is not necessary trivial is dual to the non-validity of the _tertium non datur_ for general Heyting algebras and already points to the utility of the co-Heyting negation for [[paraconsistent logic]].

* The co-Heyting supplement satisfies the dual **de Morgan rule** $\sim (a\wedge b)=(\sim a)\vee(\sim b)$, but not $\sim (a\vee b) = (\sim a)\wedge (\sim b)$ in general.

* For $a\in L$ define its **core** as $\sim\sim a$. Then $a=\partial a\vee(\sim\sim a)$. Call $a$ with $a=\sim\sim a$ **regular**. Lawvere (1986) proposes in the vein of classical mereology e.g. Tarski 1927 on regions as regular open sets, to consider only regular subbodies as bodies in the full sense.

* Suppose the element $a$ of a co-Heyting algebra has a [[complement]] $x$ i.e. $a\vee x = 1$ and $a\wedge x = 0$, then the complement $x$ coincides with $\sim a$. Because from $a\vee x=1$ follows $\sim a\leq x$ since $\sim a$ is the least element with this property; conversely, $\sim a=\sim a\vee (a\wedge x)=(\sim a\vee a)\wedge (\sim a\vee x)=\sim a\vee x$ whence $x\leq \sim a$. {#co-Heyting_complement}

* A complemented element is obviously regular. Conversely, a regular element $a$ is complemented since $0=\sim 1=\sim (a\vee\sim a)=(\sim a )\wedge (\sim\sim a)=\sim a\wedge a$.

* In a bi-Heyting algebra: $\neg a=\neg a\wedge 1=\neg a\wedge (a\vee\sim a)=(\neg a\wedge a)\vee (\neg a\wedge \sim a)= 0\vee (\neg a\wedge\sim a)=\neg a\wedge\sim a$ hence $\neg a\leq\sim a$ and we see that $\neg$ is more strongly negative than $\sim$.


## Related entries

* [[co-Heyting boundary]]
* [[co-Heyting algebra]]
* [[negation]]
* [[Heyting algebra]]
* [[Heyting category]]
* [[mereology]]
* [[adjoint modality]]
* [[paraconsistent logic]]

## References

* [[Andreas Döring|A. Döring]], _Topos-based Logic for Quantum Systems and Bi-Heyting Algebras_ , arXiv:1202.2750 (2013). ([pdf](http://arxiv.org/pdf/1202.2750.pdf))

* Y. Gauthier, _A Theory of Local Negation: The Model and some Applications_ , Arch. Math. Logik **25** (1985) pp.127-143. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/pdf/?PPN=GDZPPN002045923))

* {#Law86} [[William Lawvere|F. W. Lawvere]], _Introduction_ , pp.1-16 in Lawvere, Schanuel (eds.), _Categories in Continuum Physics_ , LNM **1174** Springer Heidelberg 1986.

* {#Law91a} F. W. Lawvere, _Intrinsic Co-Heyting Boundaries and the Leibniz Rule in Certain Toposes_ , pp.279-281 in Springer LNM **1488** (1991).

* {#RRZ94} M. La Palme Reyes, J. Macnamara, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _The non-Boolean logic of natural language negation_ , Phil. Math. **2** no.1 (1994) pp.45-68.

* M. La Palme Reyes, J. Macnamara, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _Models for non-Boolean negation in natural languages based on aspect analysis_ , pp.241-260 in Gabbay, Wansing (eds.), _What is Negation?_, Kluwer Dordrecht 1999. 

* {#RRZ04} M. La Palme Reyes, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _Generic Figures and their Glueings_ , Polimetrica Milano 2004.

* [[Matías Menni|M. Menni]], C. Smith, _Modes of Adjointness_ , J. Philos. Logic **43** no.3-4 (2014) pp.365-391.

* {#Mor13} T. Mormann, _Heyting Mereology as a Framework for Spatial Reasoning_ , Axiomathes **23** no.1 (2013) pp.237-264. ([draft](http://philpapers.org/go.pl?id=MORCMA-3&proxyId=&u=http%3A%2F%2Fphilpapers.org%2Farchive%2FMORCMA-3.pdf))

* C. Rauszer, _Semi-Boolean algebras and their applications to intuitionistic logic with dual operations_, Fund. Math. **83** no.3 (1974) pp.219-249. ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm83/fm83120.pdf))

* [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari,  _Bi-Heyting Algebras, Toposes and Modalities_ , J. Phi. Logic **25** (1996) pp.25-43.

* J.G. Stell, M.F. Worboys, _The algebraic structure of sets of regions_ , pp.163-174 in Hirtle, Frank (eds.), _Spatial Information Theory_, Springer LNCS **1329** (1997).

* H. Wansing, _Negation_ , pp.415-436 in Goble (ed.), _The Blackwell Guide to Philosophical Logic_ , Blackwell Oxford 2001.

