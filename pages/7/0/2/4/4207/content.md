

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea ##

Duality for [[nets]] of [[von Neumann algebras]] is a concept that was introduced for [[local nets]] in the [[Haag-Kastler approach]] to [[quantum field theory]]. Many results of this approach need some sort of duality in the sense described here or close to it as a precondition.

## Definition ##
Let $(M_k)$ be a [[net]] of [[von Neumann algebras]] with a [[causal index set]] $I$ that is a [[causal net of algebras]]. Let $R$ be the global algebra of the net, that is
$$
R = (\bigcup_k M_k){''}
$$
An index $i \in I$ satisfies **duality** if
$$
M_i = (\bigcup_{j \perp i} M_j)' \bigcap R = (\bigcap_{j \perp i} M_j^') \bigcap R = \bigcap_{j \perp i} M^c_j
$$
Here $M^c_j$ is the [[relative commutant]] of $M_j$ with respect to $R$.

The net is called **dual** if every index is dual i.e. satisfies duality.

A weaker concept is that of **essentially dual**:

Define an extension $(\hat M_k)$ of the net $(M_k)$ via 

$$
\hat M_i = (\bigcup_{j \perp i} M_j)'
$$
This extension is not necessarily a [[causal net]] anymore. If it is, then it is dual by definition. The net $(M_k)$ is **essentially dual**, if the extended net $(\hat M_k)$ is dual, which is true iff $(\hat M_k)$ is causal.

The net $(M_k)$ is called **maximal** if there is no proper extension which satisfies the [[causality condition]].

## Examples ##
A [[Haag-Kastler vacuum representation]] satisfies **Haag duality** if every double cone aka diamond is a dual index. The reason for this relaxation is that full duality of every index is often too restrictive, so that the less restrictive Haag duality plays an important role in the theory.

Let $J_0$ be the index set of diamonds, a [[Haag-Kastler vacuum representation]] is **essentially Haag dual** if the net $M(J_0)$ (that is the original net restricted to diamonds as indices) is essentially dual.

[[!redirects Haag duality]]
[[!redirects Haag dual]]
[[!redirects essentially Haag dual]]
[[!redirects essential Haag duality]]
[[!redirects maximal net]]
[[!redirects maximal nets]]
[[!redirects dual net]]
[[!redirects dual nets]]
[[!redirects essentially dual net]]
[[!redirects essentially dual nets]]