Given a unital ring (or only a monoid) $R$ and a **central** [[multiplicative subset]] $S\subset Z(R)\subset R$ (i.e. set containing $1\in R$ and with every two elements containing their product, and such that all its elements are central in $R$) the ring of fractions (monoid of fractions, respectively) $S^{-1} R$ is sometimes said to be the __commutative localization__ of $R$ at $S$; the same name is also given to the canonical map $R\to S^{-1} R$ of rings (monoids resp.). The ring of fractions is defined as the set of equivalence classes $(s,r)\in S\times R$ where $(s,r)\sim (t,r')$ iff $\exists u\in S$, $u s r' = u t r$ (if $R$ is an [[integral domain]] one can skip mentioning $u$ in this condition); the equivalence classes are called fractions and denoted $s^{-1}r$; by centrality of $S$ it is easy to guess the multiplication rule $s^{-1}r t^{-1} r' = (t s)^{-1} (r r')$ and for the addition one first takes the representatives with the same denominator and then adds the numerators. E.g. the formula $s^{-1}r + t^{-1}r' = (t s)^{-1} (t r + s r')$ will do, and we indeed get a ring $S^{-1} R$ with unit $1^{-1} 1$ together with the canonical  homomorphism of rings $R\to S^{-1} R$ given by $r\mapsto 1^{-1} r$. 

[[Localization of commutative rings]] at [[multiplicative subsets]] is the standard example, but the centrality of $S$ is enough for the whole theory to pass through. 

Commutative localization can be extended to left modules.

__Module of fractions__ $S^{-1} M$ is the left $S^{-1} R$-module $S^{-1} M$ equipped with the natural map of $R$-modules $M\to S^{-1}M$ and defined as follows:

The underlying set of $S^{-1} M$ consists of equivalence classes $s^{-1} m$ of pairs $(s,m)\in S\times M$ where $(s,m)\cong (t,n)$ iff there exist $u\in S$ such that $u t m = u s n$, the multiplication by scalar is defined by $(s^{-1} r)(t^{-1} m):= (t s)^{-1} (r m)$ and the addition is $s^{-1} m + t^{-1} n := (s t)^{-1}(t m + s n)$. The correspondence $Q_S : M\mapsto S^{-1} M$ extends to a functor ${}_R Mod\to {}_{S^{-1} R}Mod$. The forgetful functor $U: {}_{S^{-1} R}Mod \to {}_R Mod$ is [[fully faithful functor]] and there is a natural transformation of functors $Id\to U Q_S$ whose components are the $R$-module maps $M\to S^{-1}M$ given by $m\mapsto 1^{-1}m$. 

It can be then shown that this elementary approach is equivalent to the definition via the [[extension of scalars]] formula $S^{-1}M = S^{-1} R\otimes_R M$. 

The basic result is that the commutative localization $S^{-1} R$ is a [[flat module|flat]] left module over $R$, the property which holds for more general [[Ore localization]]. 

Commutative localization in which also $R$ is commutative is a basic procedure used in defining [[algebraic scheme]] as a [[locally ringed space]]. Another special case of this procedure is forming the [[quotient field]] of a commutative [[integral domain]]. 

