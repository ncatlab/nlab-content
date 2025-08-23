
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[foundations]] of [[mathematics]] may seem to be a topic curiously disconnected from the core of mathematical practice. But in fact, the foundations of mathematics has a significant impact upon core mathematics; different [[foundational axiom|foundational rules and axioms]] included in the foundations of mathematics would result in certain [[theorems]] being [[true]] in one foundation of mathematics, [[false]] in another foundation of mathematics, and [[independent]] in a third foundation of mathematics. This page lists numerous examples where questions of foundations do affect questions and problems in core mathematics.

The term “core mathematics” is discussed in [Quinn 2012](#Quinn12).

## Examples

### Large cardinal axioms
 {#LargeCardinalAxiom}

[[large cardinal axiom|Large cardinal axioms]], traditionally not assumed in various foundations, have effects in real mathematics:

* That every [[extremally disconnected]] [[profinite set]] has a [[hypercover]] whose terms are extremally disconnected requires that beth cardinals exist. See Peter Scholze's comment [here](https://golem.ph.utexas.edu/category/2021/06/large_sets_2.html#c060032). In particular, it is provable in Zermelo-Frankel set theory, but not provable in Zermelo set theory or [[ETCS]], because replacement implies that beth cardinals exist, and while Zermelo-Frankel set theory has replacement, neither Zermelo set theory nor ETCS have replacement or beth cardinals. 

### Excluded middle

* That every [[net]] in a [[compact space]] has a [[subnet]] that [[converges]] is equivalent to [[excluded middle]]. 

### Axiom of choice

See the nLab's [[axiom of choice#equivalents|list of statements equivalent to the axiom of choice]]. 

See also Wikipedia's [list of statements equivalent to the axiom of choice](https://en.wikipedia.org/wiki/Axiom_of_choice#Equivalents). 

There are a number of theorems that are strictly weaker than the axiom of choice but traditionally proved using the axiom of choice; these could be assumed as [[foundational axioms]] of intermediate strength between nothing and the [[axiom of choice]]. Wikipedia has a list of them [here](https://en.wikipedia.org/wiki/Axiom_of_choice#Weaker_forms). 

The [Consequences of the Axiom of Choice Project](http://consequences.emich.edu/conseq.htm) provides an interactive data base that can be used to search for implications between various (weakened) forms of the Axiom of Choice. [Choiceless grapher](http://cgraph.inters.co/) builds on this data and provides a graphical presentation. 

See also Wikipedia\'s [list of statements undecidable in ZFC](http://en.wikipedia.org/wiki/List_of_statements_undecidable_in_ZFC).

### Whitehead's theorem

In [[set theory]], [[Whitehead's theorem]] is a theorem valid for all [[infinity-groupoids]], modeled as [[Kan complexes]] or [[CW-complexes]]. However, in [[homotopy type theory]], Whitehead's theorem is not provable when regarded as a statement about types in homotopy type theory, since it admits models in non-[[hypercomplete (∞,1)-toposes]]. As a result, the truth of Whitehead's theorem is a [[foundational axiom]] that may be regarded as a "classicality" property, akin to [[excluded middle]] or the [[axiom of choice]], and is usually called *Whitehead's principle* by homotopy type theorists. 

### Univalence

* Given the [[univalence axiom]] in [[homotopy type theory]], one could prove that every [[proset]] is a [[poset]]. 

### Whitehead problem

The following question is called the **Whitehead problem**

Every [[free abelian group]] $A$ satisfies $Ext^1(A,\mathbb{Z}) = 0$. Is, conversely, every abelian group $A$ that satisfies $Ext^1(A,\mathbb{Z}) = 0$ a free abelian group?

When formalizing [[group theory]] within [[ETCS]] as a [[set theory]], then this question is undecidable.  (It is still undecidable in [[ZFC]], equivalently in ETCS + Collection.)  In some models it is true, while other models have counterexamples. As a result, it is also undecidable in [[homotopy type theory]]. 

### Fermat's last theorem

It was [conjectured](http://en.wikipedia.org/wiki/Elementary_function_arithmetic#Friedman.27s_grand_conjecture) by Harvey Friedman that all theorems involving finitary objects published in _Annals of Mathematics_ (for argument's sake) can be proved in [[Elementary Function Arithmetic]] (EFA), a weak fragment of [[Peano arithmetic]]. One implication is that [[Fermat's last theorem]] is provable in PA. There is a current program of research by Angus MacIntyre to show this last fact directly. From a category theoretic point of view, [[Colin McLarty]] has shown that all of the material in [[SGA]] relies only on quite weak foundations, namely MacLane set theory ([McLarty 2020](#McLarty20)) with one [[universe]] (weaker than the theory $V_{\omega\cdot 3}$ considered in [[ZFC]]).


[McLarty 2010](#McLarty10) comments extensively on the possibility of proving Fermat's last theorem, and more generally the Modularity theorem, in PA.

### Busy Beaver function

The value of the Busy Beaver function at $n = 745$ is independent of the [[ZFC]] axioms (see [Aaronson 2023](#Aaronson23)). This was later claimed to be reduced down to $n = 549$, as of 16 July 2025 (see [the Busy Beaver Challenge wiki](#BBCWiki)); however, none of this work has been written down in a paper yet. 

[Aaronson 2020](#Aaronson20) has conjectured that the value of the Busy Beaver function is independent of the [[ZFC]] axioms at $n \leq 20$. 

## See also

* [[foundations of mathematics]]


## References

* {#McLarty10} [[Colin McLarty]], _What does it take to prove Fermat's last theorem? Grothendieck and the logic of number theory_, Bulletin of Symbolic Logic, **16** 3 (2010) 359 - 377 &lbrack;[doi:10.2178/bsl/1286284558](https://projecteuclid.org/journals/bulletin-of-symbolic-logic/volume-16/issue-3/What-does-it-take-to-prove-Fermats-Last-Theorem-Grothendieck/10.2178/bsl/1286284558.short), [pdf](http://www.cwru.edu/artsci/phil/Proving_FLT.pdf)&rbrack;

* {#McLarty20} [[Colin McLarty]], _The large structures of Grothendieck founded on finite-order arithmetic_, The Review of Symbolic Logic **13**  2 (2020) 296 - 325 &lbrack;[arXiv:1102.1773v4](https://arxiv.org/abs/1102.1773v4), [doi:10.1017/S1755020319000340](https://doi.org/10.1017/S1755020319000340)&rbrack;



* {#Quinn12} [[Frank Quinn]]: *A Revolution in Mathematics? What Really Happened a Century Ago and Why It Matters Today*, Notices of the AMS (2012) &lbrack;[pdf](http://www.ams.org/notices/201201/rtx120100031p.pdf)&rbrack;

* {#Aaronson20} [[Scott Aaronson]], *The Busy Beaver Frontier*, ACM SIGACT News, Volume 51, Issue 3, Pages 32 - 54, 29 September 2020 &lbrack;[doi:10.1145/3427361.3427369](https://doi.org/10.1145/3427361.3427369)&rbrack;

* {#Aaronson23} [[Scott Aaronson]], *Life, blogging, and the Busy Beaver function go on*, blog entry (5 July 2023) &lbrack;[web](https://scottaaronson.blog/?p=7388)&rbrack;

* {#BBCWiki} *Independence from ZFC*, the Busy Beaver Challenge Wiki. &lbrack;[web](https://wiki.bbchallenge.org/wiki/Independence_from_ZFC)&rbrack;

[[!redirects effects of foundations on "real" mathematics]]


