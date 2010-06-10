#Contents#
* the following line creates the automatic table of contents
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
M_i = (\bigcup_{j \perp i} M_j)' \bigcap R = (\bigcap_{j \perp i} M_j^') \bigcap R = \bigcap_j M^c_j
$$
Here $M^c_j$ is the [[relative commutant]] of $M_j$ with respect to $R$.

The net is called **dual** if every index is dual i.e. satisfies duality.

A weaker concept is that of **essentially dual**:

Define an extension $\cap M_k$ of the net $M_k$ via 

$$
\hat M_k = (\bigcup_{j \perp i} M_j)'
$$
This extension is not necessarily a [[causal net]] anymore. If it is, then it is dual by definition. The net $M_k$ is **essentially dual**, if the extended net $\hat M_k$ is dual, which is true iff $\hat M_k$ is causal.

The net $M_k$ is called **maximal** if there is no proper extension which satisfies the [[causality condition]].


[[!redirects maximal net]]
[[!redirects maximal nets]]
[[!redirects dual net]]
[[!redirects dual nets]]
[[!redirects essentially dual net]]
[[!redirects essentially dual nets]]