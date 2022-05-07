
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Coherent logic
* table of contents
{: toc}

## Definitions

**Coherent logic** is a fragment of (finitary) [[first-order logic]] which allows only the connectives and quantifiers 

* $\wedge$ ([[and]]), 

* $\vee$ ([[or]]), 

* $\top$ ([[true]]), 

* $\bot$ ([[false]]), 

* $\exists$ ([[existential quantifier]]).  

A **coherent formula** is a [[formula]] in coherent logic.

A **coherent sequent** is a [[sequent]] of the form $\varphi \vdash \psi$, where $\varphi$ and $\psi$ are coherent formulas, possibly with [[free variables]] $x_1,\dots,x_n$.  

In full first-order logic, such a sequent is equivalent to the single formula 

$$
  \forall x_1, \dots, \forall x_n (\varphi \Rightarrow \psi)
$$ 

(in the empty [[context]]).  Of course, this latter formula is not coherent, but this shows that when we deal with coherent *sequents* rather than merely formulas, it can also be thought of as allowing one instance of $\Rightarrow$ and a string of $\forall$s at the very outer level of a formula.

Coherent logic (including sequents, as above) is the [[internal logic]] of a [[coherent category]].  The [[classifying topos]] of a coherent theory is a [[coherent topos]].


## Examples

* Any (finitary) [[algebraic theory]] is a coherent, in that every [[cartesian monoidal category]] can be conservatively completed to a [[coherent category]].

* A good example of a coherent theory that is not [[algebraic theory|algebraic]] (in any of the usual senses, although it comes from algebra) is the theory of a [[local ring]]; similar examples are the theories of a [[discrete integral domain]] and a [[discrete field]].

* The theory of a [[total order]] is coherent, though also not algebraic.  The theory of a [[partial order]] is [[essentially algebraic theory|essentially algebraic]], but the totality axiom $\vdash_{x,y} (x\le y) \vee (y\le x)$ is coherent but not essentially algebraic.

* The theory of a [[linear order]] is (seemingly) not coherent if we use the "connectedness" axiom $(x\nless y), (y\nless x) \vdash (x=y)$, which is not coherent since negation is not allowed in coherent formulas.  We can express one outer negation, however, as in the irreflexivity axiom $(x\lt x)\vdash \bot$. Another solution is to use the "trichotomy" axiom $\top \vdash (x=y) \vee (x\lt y) \vee (y\lt x)$ instead, in order to get an axiomatisation of "coherent" linear orderings.

## Properties

Coherent logic has many pleasing properties.

* Every finitary [[first-order logic|first-order theory]] is equivalent, over [[classical logic]], to a coherent theory.  This theory is called its *Morleyization* and can be obtained by adding new relations representing each first-order formula and its negation, with axioms that guarantee (over classical logic) these relations are interpreted correctly (using the facts that $(P\Rightarrow Q) \dashv\vdash (\neg P \vee Q)$ and $(\forall x, P) \dashv\vdash (\neg \exists x, \neg P)$ in classical logic).  See D1.5.13 in [[Sketches of an Elephant]], or Prop. 3.2.8 in Makkai-Par&#233;.

* By (one of the theorems called) [[Deligne completeness theorem|Deligne's theorem]], every [[coherent topos]] has [[point of a topos|enough points]].  In particular, this applies to the classifying toposes of coherent theories.  It follows that models in [[Set]] are sufficient to detect provability in coherent logic.  By Morleyization, we can obtain from this the classical [[completeness theorem for first-order logic]].  See for instance 6.2.2 in Makkai-Reyes.

* Coherent logic also satisfies a *definability theorem*: if a relation can be constructed in every [[Set]]-model of a coherent theory $T$, in a [[natural transformation|natural]] way, then that relation is named by some coherent formula in $T$.  See chapter 7 of Makkai-Reyes or D3.5.1 in [[Sketches of an Elephant]].

* It follows that if a morphism of coherent theories (i.e. an interpretation of one coherent theory in another) induces an equivalence of their categories of models in $Set$, then it is a [[Morita equivalence]] of theories (i.e. induces an equivalence of classifying toposes, hence an equivalence of categories of models in all [[Grothendieck toposes]]).  This is called [[conceptual completeness]]; see 7.1.8 in Makkai-Reyes or D3.5.9 in [[Sketches of an Elephant]].  (Note, though, that two coherent theories can have equivalent categories of models in $Set$ without being Morita equivalent, if the former equivalence is not induced by a morphism of theories; see for instance D3.5.4 in the Elephant.)

However, here is a property which one might expect coherent theories to have, but which they do not.

* The category of models of a coherent theory (in [[Set]]) is always an [[accessible category]] (this is true more generally for models of any logical theory).  However, it need not be *finitely* accessible (i.e. $\omega$-accessible).  An example is given in Adamek-Rosicky 5.36: the theory of sets equipped with a binary relation $\prec$ such that for all $x$ there exists a $y$ with $x\prec y$.  Then the model $(\mathbb{N},\lt)$ of this theory does not admit any morphism from an ($\omega$-)compact object.  (However, many coherent theories do have a finitely accessible category of $Set$-models.)

## Variations

* Sometimes coherent logic is called *geometric logic*, but that term is now more commonly used for the analogous fragment of infinitary logic which allows disjunctions over arbitrary sets (though still only finitary conjunctions).  See [[geometric logic]].

* Conversely, geometric logic is sometimes called _coherent_ , e.g. in Reyes ([1977](#Reyes)), so that coherent logic in the nLab terminology corresponds to the _finitary_ fragment only.

* Occasionally the [[existential quantifiers]] in coherent logic are further restricted to range only over *finitely presented types*.

## Related concepts

* [[finitely complete category]], [[cartesian functor]], [[cartesian logic]], [[cartesian theory]]

* [[regular category]], [[regular functor]], [[regular logic]], [[regular theory]], [[regular coverage]], [[regular topos]]

* [[coherent category]], [[coherent functor]], **coherent logic**, [[coherent theory]], [[coherent coverage]], [[coherent topos]]

* [[geometric category]], [[geometric functor]], [[geometric logic]], [[geometric theory]]


## References

An early reference is

* M.-F. Coste, [[Michel Coste|M. Coste]], _Théories cohérentes et topos cohérents_ , Séminaire de théorie des catégories dirigé par Jean Bénabou Mai 1975. ([pdf](https://perso.univ-rennes1.fr/michel.coste/publis/coherent.pdf))

A survey of results on geometric and coherent logic is in

* {#Reyes77}[[Gonzalo Reyes]], _Sheaves and concepts: A model-theoretic interpretation of Grothendieck topoi_ , Cah. Top. Diff. G&#233;o. Cat. **XVIII** no.2 (1977) pp.405-437. ([numdam](http://www.numdam.org/item?id=CTGDC_1977__18_2_105_0))

A standard textbook account of coherent logic (called 'geometric logic' there) can be found in

* {#MM94} [[Saunders Mac Lane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ , Springer Heidelberg 1994.

Properties of the generic model of a coherent theory are investigated in

* Marc Bezem, [[Ulrik Buchholtz]], [[Thierry Coquand]], _Syntactic Forcing Models for Coherent Logic_ , arXiv:72.07743 (2017). ([abstract](https://arxiv.org/abs/1712.07743))

Else consider the monographs

* [[Michael Makkai]] and [[Gonzalo Reyes]], *First Order Categorical Logic:  Model-theoretical methods in the theory of topoi and related categories*, Springer-Verlag, 1977.

* [[Michael Makkai]] and [[Robert Paré]], *Accessible categories*

* [[Peter Johnstone]], [[Sketches of an Elephant]] vol 2. Part D

* [[Jiri Adamek]] and [[Jiri Rosicky]], *Locally presentable and accessible categories*



[[!redirects coherent logic]]
[[!redirects coherent logics]]
[[!redirects coherent theory]]
[[!redirects coherent theories]]
[[!redirects coherent formula]]
[[!redirects coherent formulas]]
[[!redirects coherent sequent]]
[[!redirects coherent sequents]]
[[!redirects Morleyization]]
