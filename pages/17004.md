
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The [[generalized cohomology theory]] which is [[Brown representability theorem|represented]] by the [[sphere spectrum]] is also called _stable cohomotopy_, as it is the [[stable homotopy theory]] version of [[cohomotopy]].


## Properties

### As algebraic K-theory over the field with one element
 {#AsAlgebraicKTheoryOverTheFieldWithOneElement}

+-- {: .num_prop #StableCohomotopyIsKTheoryOfFinSet}
###### Proposition
**([[stable cohomotopy]] is K-theory of [[FinSet]])**

Let $\mathcal{C} = $ [[FinSet]] be a [[skeleton]] of the category of [[finite sets]], regarded as a [[permutative category]]. Then the [[K-theory of a permutative category|K-theory of this permutative category]] 

$$
  K(FinSet) \;\simeq\; \mathbb{S}
$$

is represented by the [[sphere spectrum]], hence is stable cohomotopy.

=--

(due to [Segal 74, Prop. 3.5](#Segal74), see also [Priddy 73](#Priddy73))

+-- {: .num_remark #StableCohomotopyIsAlgebraicKTheoryOverFieldWithOneElement}
###### Remark
**([[stable cohomotopy]] as [[algebraic K-theory]] over the [[field with one element]])**

Notice that for $F$ a [[field]], the [[K-theory of a permutative category]] of its [[category of modules]] $F Mod$ is its [[algebraic K-theory]] $K F$ (see [this example](K-theory+of+a+permutative+category#OrdinaryAlgebraicKTheoryFromPermutativeCategoryOfProjectiveModules))

$$
  K F \;\simeq\; K(F Mod)
  \,.
$$ 

Now ([[pointed sets|pointed]]) [[finite sets]] may be regarded as the modules over the "[[field with one element]]" $\mathbb{F}_1$ (see [there](field+with+one+element#Modules)):

$$
  \mathbb{F}_1 Mod
  \;=\;
  FinSet^{\ast/}
$$

If this is understood, example \ref{StableCohomotopyIsKTheoryOfFinSet} says that [[stable cohomotopy]] is the algebraic K-theory of the [[field with one element]]:

$$
  \mathbb{S} \;\simeq\; K \mathbb{F}_1
  \,.
$$

This perspective is highlighted for instance in ([Deitmar 06, p. 2](#Deitmar06), [Guillot 06](#Guillot06)).

=--




### Kahn-Priddy theorem

The [[Kahn-Priddy theorem]] characterizes a comparison map between stable cohomotopy and [[cohomology]] with [[coefficients]] in the infinite [[real projective space]] $\mathbb{R}P^\infty \simeq B \mathbb{Z}/2$.

## Related concepts


* [[equivariant stable cohomotopy]]


## References

The basic concept appears in

* {#Adams74} [[Frank Adams]], part III, section 6 of _[[Stable homotopy and generalised homology]]_, 1974

The identification of stable cohomotopy with the [[K-theory of a permutative category|K-theory of the permutative category]] of [[finite set]] is due to 

* {#Segal74} [[Graeme Segal]], _Catgeories and cohomology theories_, Topology vol 13 (1974)  ([pdf](http://ncatlab.org/nlab/files/SegalCategoriesAndCohomologyTheories.pdf))

see also

* {#Priddy73} [[Stewart Priddy]], _Transfer, symmetric groups, and stable homotopy theory_, in _Higher K-Theories_, Springer, Berlin, Heidelberg, 1973. 244-255 ([pdf](https://link.springer.com/content/pdf/10.1007/BFb0067060.pdf))

The [[Kahn-Priddy theorem]] is due to

* {#KahnPriddy72} [[Daniel Kahn]], [[Stewart Priddy]], _Applications of the transfer to stable homotopy theory_, Bull. Amer. Math. Soc. Volume 78, Number 6 (1972), 981-987 ([Euclid](https://projecteuclid.org/euclid.bams/1183534135))


A lift of [[Seiberg-Witten invariants]] to classes in [[circle group]]-[[equivariant stable cohomotopy]] is discussed in

* _A stable cohomotopy refinement of Seiberg-Witten invariants: I_ ([arXiv:math/0204340](http://arxiv.org/abs/math/0204340))

* _A stable cohomotopy refinement of Seiberg-Witten invariants: II_ ([arXiv:math/0204267](http://arxiv.org/abs/math/0204267))

