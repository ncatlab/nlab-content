# Contents
* table of contents
{: toc}

## Idea

Continuous logic is a logic whose truth values can take continuous values in $[0,1]$. The main variant used in model theory is motivated by the model theory of Banach spaces and similar structures. The language has connectives for each continuous function $c: [0,1]^n \to [0,1]$ and the quantifiers are interpreted as infimum and supremum. The models of this logic are bounded complete metric structures equipped with uniformly continuous maps and $[0,1]$-valued predicates. 

As well as satisfying a form of [[completeness theorem]], 

>...continuous first-order logic satisfies suitably phrased forms of the compactness theorem, the L&ouml;wenheim-Skolem  theorems, the diagram arguments, Craig's interpolation theorem, Beth's definability theorem, characterizations of quantifier elimination and model completeness, the existence of saturated and homogeneous  models results, the omitting types theorem, fundamental results of stability theory, and nearly all other results of elementary model theory. ([Yaacov &amp; Pedersen 10](#YaacovPed10))

## In terms of enriched category theory

Building on the proposal of [[Lawvere]] to understand a form of [metric space](metric+space#LawvereMetricSpace) as a category [[enriched category theory|enriched]] in the [[monoidal category|monoidal]] [[poset]] $([0, \infty], \geq)$, there have been attempts to consider continuous logic as a similarly enriched logic. In ([Albert &amp; Hart](#AlbertHart)), the authors develop a parallel for [[conceptual completeness]] via the notion of a *metric* [[pretopos]].

[[Simon Cho]] argues that the object of truth values of continuous logic, $[0,1]$, should be seen as a "continuous subobject classifier" in a similar sense to the [[subobject classifier]] of topos theory where subobjects are classified via [[pullbacks]] ([Cho 19](#Cho19)).

## References

Continuous logic is introduced in

* C. W. Henson, J. Iovino, _Ultraproducts in analysis_ in: Analysis and Logic, London Math. Soc. Lecture Note Series __262__, Cambridge University Press 2002.

motivated by

* Chen-Chung Chang, Jerome H. Keisler, _Continuous Model Theory_,
Annals of Mathematics Studies __58__, 1966.

A recent version is in

* [[Itaï Ben Yaacov]], _Uncountable dense categoricity in cats_, J. Symb. Logic __70__, 829--860, 2005
* [[Itaï Ben Yaacov]], _Continuous first-order logic and logical stability_, [pdf](http://math.univ-lyon1.fr/~begnac/articles/cfo.pdf)
* {#YaacovPed10} [[Itaï Ben Yaacov]], Arthur Pedersen, _A proof of completeness for continuous first order logic_, Journal of Symbolic Logic 75, 168–190, 2010, ([arXiv:0903.4051](https://arxiv.org/abs/0903.4051)).
* [[Itaï Ben Yaacov]], Alex Usvyatsov. _Logic of metric spaces and Hausdorff CATs_
* [[Itaï Ben Yaacov]], Alexander Berenstein, Ward C. Henson, Alexander Usvyatsov,
_Model Theory for metric structures_, in Model Theory with Applications to Algebra and Analysis, Volume 2, Cambridge University Press, 2008, [pdf](http://matematicas.uniandes.edu.co/~aberenst/mtfms.pdf)
* Alexander Berenstein, Andres Villaveces, _Hilbert spaces with random predicates_, [pdf](http://matematicas.uniandes.edu.co/~aberenst/amalg10.pdf) 
* [[Jerome Keisler]], _Model Theory for Real-valued Structures_, ([arXiv:2005.11851](https://arxiv.org/abs/2005.11851))

A discussion of [[conceptual completeness]] in the setting of continuous logic is found in

* {#AlbertHart} Jean-Martin Albert, Bradd Hart. _Metric logical categories and conceptual completeness for first order continuous logic_, ([arXiv:1607.03068](https://arxiv.org/abs/1607.03068)) 



A treatment of metric space semantics for continuous logic as a variety of [[enriched categories]] is given in

* {#Cho19} [[Simon Cho]], _Categorical semantics of metric spaces and continuous logic_, ([arXiv:1901.09077](https://arxiv.org/abs/1901.09077))

See also his thesis

* [[Simon Cho]], _Continuity in enriched categories and metric model theory_, ([thesis](http://math.lsa.umich.edu/~simoncho/thesis.pdf))

For [[syntax-semantics duality]] in the case of [[infinitary logic|infinitary]] continuous logic, see

* Ruiyuan Chen, _Representing Polish groupoids via metric structures_, ([arXiv:1908.03268](https://arxiv.org/abs/1908.03268))

An older and rather _different system_ also called continuous logic of a Russian school is surveyed

* Vitaly I. Levin, _Basic concepts of continuous logic_, Studies in logic grammar and rethoric, 11 (24) 2007, [pdf](http://math.univ-lyon1.fr/~begnac/articles/cfo.pdf)

There is a version of [[abstract elementary classes]] in the setting of continuous logic, [[metric abstract elementary class]]es. 

An analysis which avoids enriched logic is 

* Daniel Figueroa, [[Benno van den Berg]], _A topos for continuous logic_ ([arXiv:2107.10543](https://arxiv.org/abs/2107.10543))