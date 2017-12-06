
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}


##Idea#

A _symmetric monoidal $(\infty,1)$-category_ is 

* an [[(∞,1)-category]]

* which is "$\infty$-[[k-tuply monoidal n-category|tuply monoidal]]", or "stably monoidal".

This means that it is

* a [[monoidal (∞,1)-category]];

* for which the [[tensor product]] is commutative up to infinite coherent homotopy.

This can be understood as a special case of an [[(∞,1)-operad]] (...to be expanded on...)

Equivalently, a symmetric monoidal $(\infty,1)$-category is a [[commutative algebra in an (infinity,1)-category]] in the [[(infinity,1)-category of (infinity,1)-categories]].

Just as many ordinary $(\infty,1)$-categories (particularly, all of those that are [[locally presentable (infinity,1)-category|locally presentable]]) can be presented by [[model categories]], many symmetric monoidal $(\infty,1)$-categories can be presented by symmetric [[monoidal model categories]].  See for instance [NikolausSagave15](#NikolausSagave15).


## Definition in terms of quasi-categories 

Recall that in terms of [[quasi-category|quasi-categories]] a general [[monoidal (infinity,1)-category]] is conceived as a coCartesian fibration $C^\otimes \to N(\Delta)^{op}$ of [[simplicial set]]s over the ([[opposite category|opposite]] of) the [[nerve]]  $N(\Delta)^{op}$ of the [[simplex category]] satisfying a certain property. 

The fiber of this fibration over the 1-[[simplex]] $[1]$ is the [[monoidal (infinity,1)-category]] $C$ itself, its value over a map $[n] \to [1]$ encodes the tensor product of $n$ factors of $C$ with itself.

The following definition encodes the _commutativity_ of all these operations by replacing $\Delta$ with the category $FinSet_*$ of pointed finite sets.

+-- {: .num_defn}
###### Definition

A **symmetric monoidal $(\infty,1)$-category** is a 
[[coCartesian fibration]] of [[simplicial set]]s 

$$
  p : C^\otimes \to N(FinSet_*)
$$

such that

* for each $n \geq 0$  the associated functors $C^\otimes_{[n]} \to C^\otimes_{[1]}$ determine an equivalence of $(\infty,1)$-categories $C^\otimes_{[n]} \stackrel{\simeq}{\to} C_{[1]}^n$.

=--

+-- {: .num_remark}
###### Remark

In other words, a symmetric monoidal $(\infty,1)$-category is an 
$\mathcal{O}$-[[monoidal (∞,1)-category]] for 

$$
  \mathcal{O} = Com
$$

the [[commutative operad|commutative]] [[(∞,1)-operad]].

=--

See ([Lurie, def. 2.0.0.7](#LurieAlgebra)).

+-- {: .num_prop}
###### Proposition

  The [[homotopy category of an (infinity,1)-category|homotopy category]] of a symmetric monoidal $(\infty,1)$-category is an ordinary [[symmetric monoidal category]].

=--


+-- {: .num_remark}
###### Remark

There is a functor $\varphi : \Delta^{op} \to FinSet_*$ such that the [[monoidal (infinity,1)-category]] _underlying_ a symmetric monoidal $(\infty,1)$-category $p : C^\otimes \to N(FinSet_*)$ is the [[(infinity,1)-pullback]] of $p$ along $\varphi$.
=--


## Examples
 {#Examples}

### Classes of examples

* [[cartesian monoidal (∞,1)-category]]

### Specific examples

* [[stable (infinity,1)-category of spectra]]

* [[symmetric monoidal (infinity,1)-category of presentable (infinity,1)-categories]]

## Properties

### Model category structure


A [[presentable (infinity,1)-category|presentation]] of the [[(∞,1)-category]] of all symmetric monoidal $(\infty,1)$-categories is provided by the [[model structure for dendroidal coCartesian fibrations]].

### Commutative $\infty$-monoids

See [[commutative monoid in a symmetric monoidal (∞,1)-category]].


## Related concepts

* [[monoidal category]], [[monoidal (∞,1)-category]]

* [[symmetric monoidal category]], **symmetric monoidal $(\infty,1)$-category**, [[symmetric monoidal (∞,n)-category]]

* [[tensor (∞,1)-category]]

* [[closed monoidal category]] ,  [[closed monoidal (∞,1)-category]]

* [[K-theory of a symmetric monoidal (∞,1)-category]]

* [[prime spectrum of a symmetric monoidal stable (∞,1)-category]]

## References

The defintion of symmetric monoidal quasi-category is definition 1.2 in 

* [[Jacob Lurie]], _[[Commutative Algebra]]_

and definition 2.0.0.7 in 

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#LurieAlgebra}


A concise treatment is also available in

* [[Moritz Groth]], _A short course on infinity-categories_, [pdf](http://www.math.ru.nl/~mgroth/preprints/groth_scinfinity.pdf).

Relation to [[monoidal model categories]] (in particular, that every locally presentable symmetric monoidal $(\infty,1)$-category arises from a symmetric monoidal model category) is discussed in

* {#NikolausSagave15} [[Thomas Nikolaus]], [[Steffen Sagave]], _Presentably symmetric monoidal infinity-categories are represented by symmetric monoidal model categories_. Algebr. Geom. Topol. 17 (2017), no. 5, 3189--3212. ([arXiv:1506.01475](http://arxiv.org/abs/1506.01475))


[[!redirects symmetric monoidal (infinity,1)-categories]]
[[!redirects symmetric monoidal (∞,1)-category]]
[[!redirects symmetric monoidal (∞,1)-categories]]