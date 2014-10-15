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


##Idea
When the lattice of open subsets of topological spaces is the primordial example of a [[Heyting algebra]] then its dual lattice of closed subsets is the primodial example of a **co-Heyting algebra**.

Co-Heyting algebras play a role in [[modal logic|modal]], paraconsistent, and co-intuitionistic logic, [[linguistics]], [[topos theory]], [[continuum physics]] and in mereology.

##Definition
A **co-Heyting algebra** is a bounded [[distributive lattice]] $L$ equipped with a binary _subtraction_ operation $ \backslash :L\times L\to L$ such that $x\backslash y\leq z$ iff $x\leq y\vee z$.

A **bi-Heyting algebra** is a bounded distributive lattice $L$ that carries a Heyting algebra structure with implication $\Rightarrow$ and a co-Heyting algebra structure with subtraction $\backslash$.

##Example

* A Boolean algebra provides a (degenerate) example of a bi-Heyting algebra by setting $x\Rightarrow y:=\neg x\vee y$ and $x\backslash y:=x\wedge\neg y$.

##Properties

* The subtraction operation permits to define a weak negation operator $\sim: L\to L$, called _non a_ in Lawvere (1991), by setting $\sim a:=1\backslash a$. $\sim a$ minimally supplements $a$ to truth in the sense that $\sim a$ is the least $x$ with $a\vee x=1$. In turn $\sim$ can then be used to define the [[co-Heyting boundary|co-Heyting boundary operator]] $\partial :L\to L$ by $\partial a:=a\wedge\sim a$. That $\partial a$ is not necessary trivial is dual to the invalidity of the _tertium non datur_ for general Heyting algebras and already points to the use of co-Heyting algebras for paraconsistent logic.

* Accordingly, a bi-Heyting algebra is naturally equipped with two negation operators: the Heyting complement $\neg$ and the co-Heyting supplement $\sim$. Both coincide in a Boolean algebra considered as a bi-Heyting algebra.

##Related entries

* [[co-Heyting boundary]]
* [[Heyting algebra]]
* [[Heyting category]]
* [[distributive category]]

##References

* G. Bellin, _Categorical Proof Theory of Co-Intuitionistic Linear Logic_ , arXiv:1407.341 (2014). ([pdf](http://arxiv.org/pdf/1407.3416v1))

* {#RRZ94} M. La Palme Reyes, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _The non-Boolean logic of natural language negation_ , Phil. Math. **2** no.1 (1994) pp.45-68.

* {#RRZ04} M. La Palme Reyes, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _Generic Figures and their Glueings_ , Polimetrica Milano 2004.

* {#Law86} [[William Lawvere|F. W. Lawvere]], _Introduction_ , pp.1-16 in Lawvere, Schanuel (eds.), _Categories in Continuum Physics_ , Springer LNM **1174** 1986.

* {#Law91a} F. W. Lawvere, _Intrinsic Co-Heyting Boundaries and the Leibniz Rule in Certain Toposes_ , pp.279-281 in Carboni, Pedicchio, Rosolini (eds.) , _Category Theory Como Conference_, Springer LNM **1488** (1991).

* T. Mormann, _Heyting Mereology as a Framework for Spatial Reasoning_ , Axiomathes **23** no.1 (2013) pp.237-264. ([draft](http://philpapers.org/go.pl?id=MORCMA-3&proxyId=&u=http%3A%2F%2Fphilpapers.org%2Farchive%2FMORCMA-3.pdf))

* [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari,  _Bi-Heyting Algebras, Toposes and Modalities_ , J. Phi. Logic **25** (1996) pp.25-43.

* C. Rauszer, _Semi-Boolean algebras and their applications to intuitionistic logic with dual operations_ , Fund. Math. **83** no.3 (1974) pp.219-249. ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm83/fm83120.pdf))

* J.G. Stell, M.F. Worboys, _The algebraic structure of sets of regions_ , pp.163-174 in Hirtle, Frank (eds.), _Spatial Information Theory_, Springer LNCS **1329** (1997).

* M. Zarycki, _Quelque notions fondamentales de l'Analysis Situs au point de vue de l'Alg&#232;bre de la Logique_ , Fund. Math. **IX** (1927) pp.3-15. ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm9/fm912.pdf))