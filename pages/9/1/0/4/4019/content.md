
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea ##

Bornological vector spaces are a kind of [[topological vector spaces]].

On [[normed space|normed spaces]]
 [[linear operators]] are [[continuous map|continuous]] iff they are bounded. On bornological spaces this property is retained by definition.

+-- {: .standout}
The discussion below is about bornological CVSes, but there is a more general notion of *[[bornological space]]*.
=--

## Definition ##

A [[locally convex]] [[topological vector space]] $E$ is **bornological** if every circled, [[convex subset]] $A \subset E$ that absorbs every [[bounded set]] in $E$ is a [[neighbourhood]] of $0$ in $E$. Equivalently, every [[seminorm]] that is bounded on bounded sets is continuous.

The **bornology** of a given [[TVS]] is the family of bounded subsets.

Given a locally convex [[TVS]] $E$ with initial topology $T_0$, there is a [[finest topology]] $T$ such that the family of bounded subsets of $T$ coincides with $T_0$. The space $E$ equipped with the topology $T$ is called the **bornologification** of $E$, or the **bornological space associated with** $(E, T_0)$

## Properties ##

### Maps on bornological spaces

+-- {: .num_theorem}
###### Theorem
Let $U$ be a linear map from a bornological space $E$ to any locally convex [[TVS]], then the following statements are equivalent:

* $U$ is continuous,

* $U$ is bounded on bounded sets,

* $U$ maps [[null sequence|null sequences]] to null sequences.
=--

### Relation to Banach spaces

Every [[inductive limit]] of [[Banach spaces]] is a bornological vector space. ([Alpay-Salomon 13, prop. 2.3](#AlpaySalomon13))

Conversely, every bornological vector space is an inductive limit of [[normed spaces]], and of [[Banach spaces]] if it is quasi-complete ([Schaefer-Wolff 99](#SchaeferWolff99))


## Examples ##

Every metrizible locally convex space is bornological, that is every [[Fréchet space]] and thus every [[Banach space]].

## Related concepts

* [[bornological set]]

* [[bornological group]]

* [[bornological space]]

## References ##

* Wikipedia, *[Bornological spaces] (http://en.wikipedia.org/wiki/Bornological_space)*

* {#SchaeferWolff99} H. H. Schaefer, M. P. Wolff, section 8 of: _Topological vector spaces_, Springer (1999)

* {#AlpaySalomon13} Daniel Alpay, Guy Salomon, _On algebras which are inductive limits of Banach spaces_ ([arXiv:1302.3372](http://arxiv.org/abs/1302.3372))


Discussion of bornological vector spaces forming a [[quasi-abelian category]]: 

* {#ProsmansSchneiders} [[Fabienne Prosmans]], [[Jean-Pierre Schneiders]], _A homological study of bornological spaces_, December 2000, Prepublications Mathematiques de l'Universite Paris 13, 46 ([pdf](http://www.analg.ulg.ac.be/jps/rec/hsbs.pdf))

with review and generalization to [[bornological abelian groups]]:

* {#Bambozzi14} [[Federico Bambozzi]], section 1 of _On a generalization of affinoid varieties_ ([arXiv:1401.5702](http://arxiv.org/abs/1401.5702))

See also:


* {#Houzel73} Christian Houzel: *Espaces analytiques relatifs et théorème de finitude*. Math. Ann. **205** (1973) 13-54 &lbrack;[doi:10.1007/BF01432513](https://doi.org/10.1007/BF01432513)&rbrack;

* {#Meyer99} [[Ralf Meyer]]: *Analytic cyclic cohomology* &lbrack;[arXiv:math/9906205](https://arxiv.org/abs/math/9906205)&rbrack;

* {#Meyer04} [[Ralf Meyer]]: *Embeddings of derived categories of bornological modules* &lbrack;[arXiv:math/0410596](https://arxiv.org/abs/math/0410596)&rbrack;




  
[[!redirects bornologification]]

[[!redirects bornological vector space]]
[[!redirects bornological vector spaces]]
[[!redirects bornological topological vector spaces]]
[[!redirects Bornological topological vector space]]


