The _Dold-Kan correspondence_ is the name of the [[equivalence]] of 

* the category [[SAb]] of [[simplicial set|simplicial]] abelian groups;

and

* the category $Ch_+(Ab)$ of non-negatively graded chain complexes of abelian groups.

There is an adjoint equivalence

$$
  N : SAb \stackrel{\leftarrow}{\to} Ch_+(An) : \Gamma
$$

where $N$ is the normalized chains functor.

#Remarks#

* There is a whole list of generalizations of this by Brown and Higgins, showing equivalences of various strict infinity-categories [[internal category|internal to]] $Ab$ with $Ch_+(Ab)$. 

...
---
[[!redirects Dold Kan correspondence]]
* There is a version of the Dold--Kan correspondence in the context of $(\infty,1)$-[[nLab:(infinity,1)-category|categories]]:

  let $C$ be a [[nLab:stable (∞,1)-category]]. Then the $(\infty,1)$-categories of [[nLab:complexes]] in $C$ is equivalent to the $(\infty,1)$-category of [[nLab:simplicial objects]] in $C$

  $$
    Fun(N(\mathbb{Z}_{\geq 0}), C)
    \simeq
    Fun(N(\Delta)^{op}, C)  
    \,.
  $$

  This is [theorem 12.8, p. 50](http://www.math.harvard.edu/~lurie/topoibook/DAGI.pdf) of 

  * [[nLab:Jacob Lurie]], [[nLab:Stable ∞-Categories]] 


* There is a version of the Dold--Kan correspondence with [[nLab:simplicial sets]] generalized to [[nLab:dendroidal sets]]. This is described in

  * [[nLab:Javier Gutierrez|Javier Gutiérrez]], [[nLab:Andor Lukacs]], [[nLab:Ittay Weiss]], _Dold-Kan correspondence for dendroidal abelian groups_ ([arXiv](http://arxiv.org/abs/0909.3995))

---
An adjoint equivalence $N: sAb \leftrightarrows Ch_{+} : \Gamma$. The Eilenberg-MacLane space $K(A,n)$ can be defined as $\Gamma( A[-n] )$ where $A[-n]$ is $A$ placed in degree $n$.

Details are written out in Weibel (chapter 8?) and also in Goerss-Schemmerhorn, section 4 and p. 16. One way of thinking of this is that since simplicial groups are fibrant as simplicial sets, their homotopy groups can be computed combinatorially, and the recipe for doing this is given by the Dold-Kan correspondence.

For details on the model cat of simplicial abelian groups and the Dold-Kan corr, see Goerss-Jardine section III.2. Consequences include the description of cohomology as a Hom into an EM space, and the fact that every simplicial abelian group is non-canonically homotopy equivalent to a product of EM spaces.

Stable version in Tierney LNM0087.

[Moore complex](http://www.ncatlab.org/nlab/show/Moore+complex) in nlab

&lt;http://ncatlab.org/nlab/show/Dold-Kan+correspondence>

A preprint of Shoikhet related to monoidal properties of Dold-Kan: &lt;http://front.math.ucdavis.edu/1109.5441>

&lt;http://ncatlab.org/nlab/show/monoidal+Dold-Kan+correspondence>

I mentioned some more general versions of DK in the Homotopical cats blog post I think, with refs.

[Dendroidal Dold-Kan correspondence](http://front.math.ucdavis.edu/0909.3995)

D-K corr holds in general for simplicial objects in a semiabelian category, see remark at [nLab](http://ncatlab.org/nlab/show/semi-abelian+category)

&lt;http://mathoverflow.net/questions/32755/is-there-any-generalization-of-the-dold-kan-correspondence>

[arXiv:1109.5441](http://front.math.ucdavis.edu/1109.5441) A bialgebra axiom and the Dold-Kan correspondence
from arXiv Front: math.KT by Boris Shoikhet
We introduce a bialgebra axiom for a pair $(c,\ell)$ of a colax-monoidal and
a lax-monoidal structures on a functor $F\colon \mathscr{M}_1\to \mathscr{M}_2$
between two (strict) symmetric monoidal categories. This axiom can be regarded
as a weakening of the property of $F$ to be a strict symmetric monoidal
functor. We show that this axiom transforms well when passing to the adjoint
functor or to the categories of monoids. Rather unexpectedly, this axiom holds
for the Alexander-Whitney colax-monoidal and the Eilenberg-MacLane lax-monoidal
structures on the normalized chain complex functor in the Dold-Kan
correspondence. This fact, proven in Section 2, opens up a way for many
applications, which we will consider in our sequel paper(s).

nLab page on [[nlab:Dold-Kan correspondence]]
