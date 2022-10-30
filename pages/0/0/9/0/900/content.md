

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

A **pro-object** of a [[category]] $C$ is a "formal [[filtered category|cofiltered]] [[limit]]" of [[objects]] of $C$.  

The category of pro-objects of $C$ is written $pro$-$C$. Such a category is sometimes called a 'pro-category', but notice that that is *not* the same thing as a pro-object in [[Cat]].

"Pro" is short for "projective". 
( _[[projective limit|Projective limit]]_ is an older term for _[[limit]]_.) It is in contrast to "ind" in the dual notion of [[ind-object]], standing for "inductive", (and corresponding to _[[inductive limit]]_, the old term for _[[colimit]]_).  In some (often older) sources, the term 'projective system' is used more or less synonymously for pro-object.

## Definition 

### Via formal filtered limits

The [[objects]] of the [[category]] $pro$-$C$ are [[diagrams]] $F:D\to C$ where $D$ is a [[small category|small]] [[filtered category|cofiltered]] category.  The [[hom set]] of [[morphisms]] between $F:D\to C$ and $G:E\to C$ is 

\[pro\text{-}C(F,G) = lim_{e\in E} colim_{d\in D} C(F d, G e)\]

The [[limit]] and [[colimit]] is taken in the category [[Set]] of sets. 


Cofiltered limits in [[Set]] are given by sets of [[thread]]s and filtered colimits by [[germs]] (classes of equivalences), thus a representative of $s\in\mathrm{pro}C(F,G)$ is a thread whose each component is a germ:  
$s = (germ_e(s))_{e\in E}$ which can be more concretely written as $([s_{d_e,e}])_e$; thus $[s_{d_e,e}]\in colim_{d\in D} C(F d, G e)$ where $s_{d_e,e}\in C(F d_e, G e)$ is some representative of the class; there is at least one $d_e$ for each $e$; if the domain $E$ is infinite, we seem to need an axiom of choice in general to find a function $e\mapsto d_e$ which will choose one representative in each class $germ_e(s)$. Thus $s$ is given by the (equivalence class) of the following data

* function $e\mapsto d_e$ 

* correspondence $e\mapsto s_{d_e,e}\in C(F d_e, G e)$ 

such that $([s_{d_e,e}])_e$ is a thread, i.e. for any $\gamma: e\to e'$ we have an equality of classes (germs) $[G(\gamma)\circ s_{d_e,e}] = [s_{d_{e'},e'}]$. This equality holds if 
there is a $d'$ and morphisms $\delta_e: d'\to d_e$, 
$\delta_{e'}: d'\to d_{e'}$ such that $G(\gamma)\circ s_{d_e,e}\circ F\delta_e = s_{d_{e'},e'}\circ F\delta_{e'}$. (Usually in fact people consider the dual of $D$ and the dual of $C$ as filtered domains). Now if we chose a different function $e\mapsto\tilde{d}_e$ instead then,  $([s_{d_e,e}])_e = ([s_{\tilde{d}_e,e}])_e$, hence by the definition od classes, for every $e$ there is a $d''\in D$ and morphisms $\sigma_e : d''\to d_e$, $\tilde\sigma_e:d''\to \tilde{d}_e$ such that $s_{\tilde{d}_e,e}\circ F(\tilde\sigma_e) = s_{d_e,e}\circ F(\sigma_e)$.

This definition is perhaps more intuitive in the dual case of [[ind-object|ind-objects]] (pro-objects in $C^{op}$), where it can be seen as stipulating that the objects of $C$ are [[finitely presentable object|finitely presentable]] in $ind$-$C$.

### Via filtered limits of presheaves

Another, equivalent, definition is to let $pro$-$C$ be the [[full subcategory]] of the [[opposite category|opposite]] [[functor category]]/[[category of presheaves|presheaf category]] $[C,Set]^{op}$ determined by those functors which are cofiltered limits of [[representable functor|representables]]. This is reasonable since the [[presheaf category|copresheaf category]] $[C,Set]^{op}$ is the [[free completion]] of $C$, so $pro$-$C$ is the "free completion of $C$ under cofiltered limits." See also at
[[pro-representable functor]].

## Examples

* [[profinite set]], [[profinite space]]

* [[profinite group]], [[progroup]]

* [[pro-étale morphism of schemes]], [[pro-étale site]]


##Applications

### &#201;tale homotopy theory. 

Procategories were used by Artin and Mazur in their work on [[étale homotopy]] theory. They associated to a scheme a 'pro-homotopy type'.  (This is discussed briefly at [[étale homotopy]].) The important thing to note is that this was a pro-object in the _homotopy category_ of simplicial sets, i.e., in the pro-homotopy category. Friedlander rigidified their construction to get an object in the pro-category of simplicial sets, and this opened the door to use of 'homotopy pro-categories'.

###Shape theory. 

The form of [[shape theory]] developed by  Marde&#353;i&#263; and Segal, at about the same time as the work in algebraic geometry, again used the pro-homotopy category. Strong shape, developed by Edwards and Hastings, Porter and also in further work by Marde&#353;i&#263; and Segal, used various forms of rigidification to get to the pro-category of spaces, or of simplicial sets.  There methods of model category theory could be used.
  
  

## Related concepts

* [[ind-object]] / [[ind-object in an (∞,1)-category]]

* **pro-object** / [[pro-object in an (∞,1)-category]]

* [[pro-representable functor]]

* [[ind-pro-object]]

* [[pro-left adjoint]]

* [[pro-homotopy theory]], [[profinite completion of a group]]

* [[ind-pro-object]]

## References
*   A. Grothendieck, _Techniques de d&#233;scente et th&#233;or&#232;mes d'existence en g&#233;om&#233;trie alg&#233;brique, II: le th&#233;or&#232;me d'existence en th&#233;orie formelle des modules_, Seminaire Bourbaki __195__, 1960, [(pdf)](http://archive.numdam.org/ARCHIVE/SB/SB_1958-1960__5_/SB_1958-1960__5__369_0/SB_1958-1960__5__369_0.pdf).


* (SGA4-1) A. Grothendieck, J. L. Verdier, _Pr&#233;faisceaux_, Exp. 1 ([retyped pdf](http://www.math.polytechnique.fr/~orgogozo/SGA4/01/01.pdf)) in _Th&#233;orie des topos et cohomologie &#233;tale des sch&#233;mas. Tome 1: Th&#233;orie des topos_, S&#233;minaire de G&#233;om&#233;trie Alg&#233;brique du Bois-Marie 1963&#8211;1964 ([[SGA 4]]). Dirig&#233; par M. Artin, A. Grothendieck, et J. L. Verdier. Avec la collaboration de N. Bourbaki, P. Deligne et B. Saint-Donat. Lecture Notes in Mathematics __269__, Springer 1972. [pdf of SGA 4, Tome 1](http://www.iecn.u-nancy.fr/~gaillapy/SGA/grothendieck_sga_4.1.pdf)
*  [[Michael Artin]], [[Barry Mazur]], _&#201;tale homotopy theory_, Lecture Notes in Maths. 100, Springer-Verlag, Berlin 1969.

* [[Jean-Marc Cordier]], [[Tim Porter]],  _Shape Theory_ , categorical methods of approximation, Dover (2008) (This is a reprint of the 1989 edition without amendments.)

* [[Masaki Kashiwara]], [[Pierre Schapira]], _[[Categories and Sheaves]]_

* [[Peter Johnstone]], _[[Stone Spaces]]_.

* [[S. Marde?i?]], J. Segal, _Shape theory_, North Holland 1982

* J.-L. Verdier, _Equivalence essentielle des syst&#232;mes projectifs_, C. R.A.S. Paris261 (1965), 4950 - 4953.

* J. Duskin, _Pro-objects (after Verdier)_, S&#233;m. Heidelberg- Strasbourg1966 -67, Expos&#233; 6, I.R.M.A.Strasbourg. 

* A. Deleanu, P. Hilton, Borsuk shape and Grothendieck categories of pro-objects, Math. Proc. Camb. Phil. Soc.79-3 (1976), 473-482 [MR400220](http://www.ams.org/mathscinet-getitem?mr=400220)

* Tholen

[[!redirects pro-objects]]
[[!redirects pro object]]