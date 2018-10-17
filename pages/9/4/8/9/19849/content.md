+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}



## Idea

A **two-valued topos** is a topos with exactly two [[truth value|truth values]].



## Definition

A topos $\mathcal{E}$ is called _two-valued_ if its [[subobject classifier]] $\Omega$ has precisely two global elements $1\overset{true}{\to}\Omega$ and $1\overset{false}{\to}\Omega$.


## Properties

* In particular, a two-valued topos $\mathcal{E}$ is consistent i.e. $\mathcal{E}\neq 1$.

* Since truth values correspond to elements of $Hom_\mathcal{E}(1,\Omega)$ by exponential adjointness and $\Omega$ classifies subobjects, a topos $\mathcal{E}$ is two-valued precisely if the [[terminal object]] $1$ has exactly the two subobjects $0$ and $1$.

* Let $\mathbb{T}$ be a [[geometric theory]] in the signature $\Sigma$. Then $\mathbb{T}$ is called _complete_ if every geometric sentence $\varphi$ over $\Sigma$ is $\mathbb{T}$-provably equivalent to either $\top$ or $\bottom$ but not both. A geometric theory $\mathbb{T}$ is complete precisely iff its [[classifying topos]] $Set[\mathbb{T}]$ is two-valued (Caramello [2012](#Ca12), remark 2.5).

* A [[Boolean topos]] is not necessarily two-valued - the easist consistent example possibly being $Set\times Set$, which is four-valued, more complicated ones often arising in intermediates steps in set-theoretic [[forcing]] (cf. [[continuum hypothesis]]). There exists a general _filter quotient construction_ turning a Boolean topos into a two-valued Boolean topos (cf. Mac Lane-Moerdijk [1994](#MM94), pp.256ff.,274). 


## Examples

* Though the  forcing models resulting from the above mentioned filter-quotient construction provide a plethora of examples of Boolean two-valued toposes other than $Set$, two-valued toposes are by no means bound to be Boolean. 

* In fact, there exists a rich supply of two-valued toposes that are not Boolean as well, provided by the **toposes of actions of monoids** $M$: It is well known that these are not Boolean when $M$ is not a group and, since the underlying set of $\Omega$ consists of all right ideals of $M$ with $m\in M$ acting on a right ideal $I$ by mapping it to $I\cdot m=\{x\in M|mx\in I\}$, a global element picks out a right ideal $J$ that satisfies $J\cdot y= J$ for all $y\in M$ inheriting by equivariance the triviality of the action on $1$ with underlying $M$-set a singleton, implying $J=\empty$ or $J=M$.


## Related entries

* [[two-valued logic]]

* [[well-pointed topos]]

* [[Boolean topos]]

* [[continuum hypothesis]]

* [[Deligne completeness theorem]]

## References

* {#Ca12}[[Olivia Caramello]], _Atomic toposes and countable categoricity_ , Appl. Cat. Struc. **20** no. 4 (2012) pp.379-391. ([arXiv:0811.3547](http://arxiv.org/abs/0811.3547))

* {#MM94} [[Saunders Mac Lane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ , Springer Heidelberg 1994.




[[!redirects Two-valued topos]]
[[!redirects two valued topos]]
[[!redirects Two valued topos]]
[[!redirects Two-valued topos]]