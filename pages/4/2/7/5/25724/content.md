
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Both [[quasi-categories]] as well as [[sSet-enriched categories]] serve as models for [[(infinity,1)-categories|$(\infty,1)$-categories]] (exhibited by the [[Joyal model structure for quasi-categories]] and the [[Dwyer–Kan–Bergner model structure on sSet-enriched categories]], respectively) and in fact as [[Quillen equivalence|Quillen equivalent]] models (see the *[[relation between quasi-categories and simplicial categories]]*) whose [[right Quillen functor]] is the [[homotopy coherent nerve]]-operation. Its [[left adjoint]]

$$
  \mathfrak{C} 
     \;\colon\; 
  sSet \longrightarrow sSet\text{-}Cat
$$

&lbrack;[Lurie (2009), pp. 20](#Lurie09)&rbrack; thus encodes any [[quasi-category]] equivalently in an [[sSet]]-[[enriched category]]. Since in the latter model, but not in the former, [[horizontal composition]] is a strictly [[associativity|associative]] and [[unitality|unital]] operation, one may think of $\mathfrak{C}(-)$ as (partially) "rigidifying" the data in a quasi-category, in the sense of [[semi-strict infinity-category|semi-strictification of $\infty$-categories]], whence it is also known as the operation of *rigidification of quasi-categories* &lbrack;[Dugger & Spivak (2011a)](#DuggerSpivak11a)&rbrack;.

## Definition

(...)


## Properties
 {#Properties}

The rigidification operation does not strictly preserve [[Cartesian products]] (cf. *[[products of simplicial sets]]*) but it does so up to equivalence:

\begin{proposition}\label{PreservationOfProducts}
  For $S\, S' \,\in\, sSet$ there is a [[natural transformation]]
$$
  \mathfrak{C}(S \times S')
  \longrightarrow
  \mathfrak{C}(S) \times \mathfrak{C}(S')
$$
which is a [[Dwyer-Kan equivalence]].
\end{proposition}
&lbrack;[Lurie (2009), Cor. 2.2.5.6](#Lurie09); [Dugger & Spivak (2011a), Prop. 6.2](#DuggerSpivak11a)&rbrack;


## References

The construction is briefly mentioned and attributed to [[André Joyal]] in:

* {#Bergner07} [[Julie Bergner]], Theorem 7.8 in: *A survey of $(\infty,1)$-categories*, in: [[John Baez]], [[Peter May]] (eds.),  _[[Towards Higher Categories]]_ The IMA Volumes in Mathematics and its Applications **152**, Springer (2007) &lbrack;[arXiv:math/0610239](http://arxiv.org/abs/math/0610239), [doi:10.1007/978-1-4419-1524-5_2](https://doi.org/10.1007/978-1-4419-1524-5_2)&rbrack; 

First detailed discussion (not using a name beyond the symbol "$\mathfrak{C}$") is due to:

* {#Lurie09} [[Jacob Lurie]], §1.1.5 and §2.2 of: _[[Higher Topos Theory]]_, Annals of Mathematics Studies **170**, Princeton University Press (2009) &lbrack;[pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf)&rbrack;

Further discussion and the terminology "rigidification" is due to

* {#DuggerSpivak11a} [[Dan Dugger]], [[David Spivak]], *Rigidification of quasi-categories*, Algebr. Geom. Topol. **11** (2011) 225-261 &lbrack;[arXiv:0910.0814](http://arxiv.org/abs/0910.0814), [doi:10.2140/agt.2011.11.225](http://dx.doi.org/10.2140/agt.2011.11.225)&rbrack;

aimed at discussing [[quasi-categorical hom-spaces]]:

* {#DuggerSpivak11b} [[Dan Dugger]], [[David Spivak]], *Mapping spaces in quasi-categories*, Algebr. Geom. Topol. **11** (2011) 263-325 &lbrack;[arXiv:0911.0469](http://arxiv.org/abs/0911.0469), [doi:10.2140/agt.2011.11.263](http://dx.doi.org/10.2140/agt.2011.11.263)&rbrack;

See also:

* {#MinichielloRiveraZeinalian23} [[Emilio Minichiello]], [[Manuel Rivera]], [[Mahmoud Zeinalian]], §3.2 in: *Categorical models for path spaces*, Advances in Mathematics **415** (2023) 108898 &lbrack;[arXiv:2201.03046](https://arxiv.org/abs/2201.03046), [doi:10.1016/j.aim.2023.108898](https://doi.org/10.1016/j.aim.2023.108898)&rbrack;

