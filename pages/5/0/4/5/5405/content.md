
#Contents#
* table of contents
{:toc}

## Statement


+-- {: .un_def}
###### Definition

For $C,D$ two [[symmetric monoidal category|symmetric monoidal]] [[abelian categories]], write

$$
  Func_\otimes(C,D) \subset Func(C,D)
$$

the [[core]] of the [[subcategory]] of the [[functor category]] on those [[functor]]s that are 

* [[symmetric monoidal functor]]s;

* [[additive functor]]s;

* [[exact functor]];

* preserve flat objects.

=--

+-- {: .un_def}
###### Definition


* For $k$ a [[ring]], write $k Mod$ for its [[abelian category|abelian]] [[symmetric monoidal category]] of [[module]]s

* For $X$ an [[algebraic stack]], write $QC(X)$ for its [[abelian category|abelian]] [[symmetric monoidal category]] of [[quasicoherent sheaves]].

=--

+-- {: .un_theorem}
###### Theorem

Let $X$ be an [[algebraic stack]] that is quasi-compact with affine representable diagonal.

Then for every ring $A$ there is an [[equivalence of categories]]

$$
  X(Spec A) \simeq Hom_\otimes(QC(X); A Mod)
  \,.
$$

=--

This is a special case of ([Lurie, theorem 5.11](#Lurie)).

+-- {: .un_remark}
###### Remark

This statement justifies thinking of $QC(X)$ as being the "2-algebra" of functions on $X$. This perspective is the basis for [[derived noncommutative geometry]].

=--


## References

* [[Jacob Lurie]], _Tannaka duality for geometric stacks_, ([arXiv:math.AG/0412266](http://arxiv.org/abs/math/0412266))
{#Lurie}
