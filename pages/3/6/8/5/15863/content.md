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



##Idea
When the lattice of open subsets of a topological space is the primordial example of a [[Heyting algebra]] then its dual _lattice of closed subsets_ is the primordial example of a **co-Heyting algebra**.

Co-Heyting algebras play a role in [[modal logic|modal]], paraconsistent, and co-intuitionistic logic, [[linguistics]], [[topos theory]], [[continuum physics]] and in [[mereology]].

##Definition
A **co-Heyting algebra** is a bounded [[distributive lattice]] $L$ equipped with a binary _subtraction_ operation $ \backslash :L\times L\to L$ such that $x\backslash y\leq z$ iff $x\leq y\vee z$.[^Dist]

[^Dist]: Existence of $\backslash$ amounts to an [[adjunction]] \_$\backslash y\dashv y\vee$\_ and the existence of a left adjoint implies that $y\vee$\_ preserves limits $\wedge$ hence the assumption of distributivity in the definition is redundant and has been put in for emphasis only.

A **bi-Heyting algebra** is a bounded distributive lattice $L$ that carries a Heyting algebra structure with implication $\Rightarrow$ and a co-Heyting algebra structure with subtraction $\backslash$.

##Examples

* The lattice of closed subsets of a topological space is a co-Heyting algebra with $X\backslash Y=\overline{X\cap Y^c}\quad$.

* A Boolean algebra provides a (degenerate) example of a bi-Heyting algebra by setting $x\Rightarrow y:=\neg x\vee y$ and $x\backslash y:=x\wedge\neg y$.

##Properties

* $a\backslash b=0$ iff $a\backslash b\leq O$ iff $a\leq b\vee 0$ iff $a\leq b$. In particular, $a\backslash a=0$.

* As \_$\backslash x$ has a right adjoint it preserves colimits hence: $(a\vee b)\backslash x =(a\backslash x)\vee (b\backslash x)\quad$.

* $a\backslash 0\leq a\backslash 0$ iff $a\leq 0\vee (a\backslash 0)$ iff $a\leq a\backslash 0\quad$. On the other hand, $a\leq 0\vee a$ and the adjunction yield $a\backslash 0\leq a\quad$, hence $a\backslash 0 = a\quad$.

* Suppose $a\leq b\vee x $ then $a\backslash b\leq x$. As from $a\backslash b\leq a\backslash b$ follows $a\leq b\vee (a\backslash b)$, hence $a\backslash b =\Wedge\{x|a\leq b\vee x\}\quad$.

* The subtraction operation permits to define a weak negation operator $\sim: L\to L$, called _non a_ in Lawvere (1991), by setting $\sim a:=1\backslash a$. $\sim a$ minimally supplements $a$ to truth in the sense that $\sim a$ is the least $x$ with $a\vee x=1$. In turn $\sim$ can then be used to define the [[co-Heyting boundary|co-Heyting boundary operator]] $\partial :L\to L$ by $\partial a:=a\wedge\sim a$. That $\partial a$ is not necessary trivial is dual to the non-validity of the _tertium non datur_ for general Heyting algebras and already points to the utility of co-Heyting algebras for paraconsistent logic.

* Accordingly, a bi-Heyting algebra is naturally equipped with two negation operators: the Heyting complement $\neg$ and the co-Heyting supplement $\sim$. Both coincide in a Boolean algebra considered as a bi-Heyting algebra.

* The co-Heyting supplement satisfies the dual de Morgan rule $\sim (a\wedge b)=(\sim a)\vee(\sim b)$, but only $\sim\sim (a\vee b) = (\sim\sim a)\wedge (\sim\sim b)$ in general.

* For $a\in L$ define its _core_ as $\sim\sim a$. Then $a=\partial a\vee\sim\sim a$. Call $a$ with $a=\sim\sim a$ _regular_. Lawvere (1986) proposes in the vain of classical mereology e.g. Tarski 1927 on regions as regular open sets, to consider only regular subbodies as bodies in the full sense.

* In toposes like e.g. essential subtoposes of presheaf toposes, where the lattices of subobjects carry a bi-Heyting structure, the co-Heyting algebra operations are generally not preserved by [[inverse image functor|inverse image functors]], so that the co-Heyting logical operators are subject to _de re_ and _de dicto_ effects.

##Related entries

* [[co-Heyting boundary]]
* [[Heyting algebra]]
* [[Heyting category]]
* [[distributive category]]
* [[mereology]]
* [[bitopological space]]

##References

* G. Bellin, _Categorical Proof Theory of Co-Intuitionistic Linear Logic_ , arXiv:1407.341 (2014). ([pdf](http://arxiv.org/pdf/1407.3416v1))

* {#RRZ94} M. La Palme Reyes, J. Macnamara, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _The non-Boolean logic of natural language negation_ , Phil. Math. **2** no.1 (1994) pp.45-68.

* M. La Palme Reyes, J. Macnamara, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _Models for non-Boolean negation in natural languages based on aspect analysis_ , pp.241-260 in Gabbay, Wansing (eds.), _What is Negation?_, Kluwer Dordrecht 1999. 

* {#RRZ04} M. La Palme Reyes, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _Generic Figures and their Glueings_ , Polimetrica Milano 2004.

* {#Law86} [[William Lawvere|F. W. Lawvere]], _Introduction_ , pp.1-16 in Lawvere, Schanuel (eds.), _Categories in Continuum Physics_ , Springer LNM **1174** 1986.

* {#Law91a} F. W. Lawvere, _Intrinsic Co-Heyting Boundaries and the Leibniz Rule in Certain Toposes_ , pp.279-281 in Carboni, Pedicchio, Rosolini (eds.) , _Category Theory Como Conference_, Springer LNM **1488** (1991).

* T. Mormann, _Heyting Mereology as a Framework for Spatial Reasoning_ , Axiomathes **23** no.1 (2013) pp.237-264. ([draft](http://philpapers.org/go.pl?id=MORCMA-3&proxyId=&u=http%3A%2F%2Fphilpapers.org%2Farchive%2FMORCMA-3.pdf))

* [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari,  _Bi-Heyting Algebras, Toposes and Modalities_ , J. Phi. Logic **25** (1996) pp.25-43.

* C. Rauszer, _Semi-Boolean algebras and their applications to intuitionistic logic with dual operations_ , Fund. Math. **83** no.3 (1974) pp.219-249. ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm83/fm83120.pdf))

* J.G. Stell, M.F. Worboys, _The algebraic structure of sets of regions_ , pp.163-174 in Hirtle, Frank (eds.), _Spatial Information Theory_, Springer LNCS **1329** (1997).

* M. Zarycki, _Quelque notions fondamentales de l'Analysis Situs au point de vue de l'Alg&#232;bre de la Logique_ , Fund. Math. **IX** (1927) pp.3-15. ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm9/fm912.pdf))