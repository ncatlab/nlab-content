[[!redirects effects of foundations on &quot;real&quot; mathematics]]

#Contents#
* table of contents
{:toc}

## Idea

The [[foundations]] of [[mathematics]] may seem to be a topic curiously disconnected from the core mathematics. This is not quite so. This page lists examples where questions of foundations do affect questions and problems in core mathematics.

The term “core mathematics” is discussed in an [article](http://www.ams.org/notices/201201/rtx120100031p.pdf) by [[Frank Quinn]]

See also Wikipedia\'s [list of statements undecidable in ZFC](http://en.wikipedia.org/wiki/List_of_statements_undecidable_in_ZFC).

## Large cardinal axioms

[[Large cardinal axioms]], traditionally not assumed in various foundations, have effects in real mathematics:

* That every [[extremally disconnected]] [[profinite set]] has a [[hypercover]] whose terms are extremally disconnected requires that beth cardinals exist. See Peter Scholze's comment [here](https://golem.ph.utexas.edu/category/2021/06/large_sets_2.html#c060032). In particular, it is provable in Zermelo-Frankel set theory, but not provable in Zermelo set theory or [[ETCS]], because replacement implies that beth cardinals exist, and while Zermelo-Frankel set theory has replacement, neither Zermelo set theory nor ETCS have replacement or beth cardinals. 

* The existence of [[large categories]] such as [[Grothendieck topoi]] requires the existence of a strongly [[inaccessible cardinal]]/[[universe]]

## Propositional resizing

* The [[Dedekind real numbers]] become [[small]] with [[propositional resizing]]. 

* All [[posets]] are small with propositional resizing. In particular, the [[frame]] of [[truth values]] is small, and thus the [[powerset]] of a [[set]] is small. 

## Excluded middle

* That every [[net]] in a [[compact space]] has a [[subnet]] that [[converges]] is equivalent to [[excluded middle]]. 

## Axiom of choice

See the nLab's [[axiom of choice#equivalents|list of statements equivalent to the axiom of choice]]. 

See also Wikipedia's [list of statements equivalent to the axiom of choice](https://en.wikipedia.org/wiki/Axiom_of_choice#Equivalents). 

There are a number of theorems that are strictly weaker than the axiom of choice but traditionally proved using the axiom of choice; these could be assumed as [[foundational axioms]] of intermediate strength between nothing and the [[axiom of choice]]. Wikipedia has a list of them [here](https://en.wikipedia.org/wiki/Axiom_of_choice#Weaker_forms). 

## Whitehead's theorem

In [[set theory]], [[Whitehead's theorem]] is a theorem valid for all [[infinity-groupoids]], modeled as [[Kan complexes]] or [[CW-complexes]]. However, in [[homotopy type theory]], Whitehead's theorem is not provable when regarded as a statement about types in homotopy type theory, since it admits models in non-[[hypercomplete (∞,1)-toposes]]. As a result, the truth of Whitehead's theorem is a [[foundational axiom]] that may be regarded as a "classicality" property, akin to [[excluded middle]] or the [[axiom of choice]], and is usually called *Whitehead's principle* by homotopy type theorists. 

## Whitehead problem

The following question is called the **Whitehead problem**

Every [[free abelian group]] $A$ satisfies $Ext^1(A,\mathbb{Z}) = 0$. Is, conversely, every abelian group $A$ that satisfies $Ext^1(A,\mathbb{Z}) = 0$ a free abelian group?

When formalizing [[group theory]] within [[ETCS]] as a [[set theory]], then this question is undecidable.  (It is still undecidable in [[ZFC]], equivalently in ETCS + Collection.)  In some models it is true, while other models have counterexamples. As a result, it is also undecidable in [[homotopy type theory]]. 

## Fermat's last theorem

It was [conjectured](http://en.wikipedia.org/wiki/Elementary_function_arithmetic#Friedman.27s_grand_conjecture) by Harvey Friedman that all theorems involving finitary objects published in _Annals of Mathematics_ (for argument's sake) can be proved in [[Elementary Function Arithmetic]] (EFA), a weak fragment of [[Peano arithmetic]]. One implication is that [[Fermat's last theorem]] is provable in PA. There is a current program of research by Angus MacIntyre to show this last fact directly. From a category theoretic point of view, [[Colin McLarty]] has shown that all of the material in [[SGA]] relies only on quite weak foundations, namely MacLane set theory with one [[universe]] (weaker than the theory $V_{\omega\cdot 3}$ considered in [[ZFC]])

* [[Colin McLarty]], _Set Theory for Grothendieck's Number Theory_, ([pdf](http://www.cwru.edu/artsci/phil/Groth%20found26.pdf)), draft dated Jan 26 2011

McLarty comments extensively on the possibility of proving Fermat's last theorem, and more generally the Modularity theorem, in PA in the article

* Colin McLarty, _What does it take to prove Fermat's last theorem? Grothendieck and the logic of number theory_, Bulletin of Symbolic Logic, Volume 16, Issue 3, September 2010, pp. 359 - 377, DOI:10.2178/bsl/1286284558 ([pdf](http://www.cwru.edu/artsci/phil/Proving_FLT.pdf)) 

## See also

* [[foundations of mathematics]]