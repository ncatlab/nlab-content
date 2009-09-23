A multiplicative closed subset $S\subset R$ containing a unit element in a [[monoid]] $R$ is a **left Ore set** if it satisfies the 

* (left cancellability) If $ns = ms$ for $n,m\in R$ and $s\in S$, then $\exists s'\in S$ such that $s'n=s'm$.

* (left Ore condition) For any $r\in R$ and $s\in S$ there
$\exists r'\in R$, $\exists s'\in S$ such that $s'r = r's$. 

Sometimes both conditions are called "Ore conditions". 
Notice that in both conditions the new elements whose existence is equired are on the left. 

If $S$ is a left Ore set in a monoid than there is a well-defined equivalence relation $\sim$ on pairs $(s,r)\in S\times R$ such that the set of equivalence classes, which are denoted by $s^{-1}r := [(s,r)]\in S^{-1}R:=S\times R/\sim$ becomes a monoid together with a monoid map $j_S: R\to S^{-1}R$ given by $r\mapsto 1^{-1}r$ is a homomorphism of monoids; moreover this monoid map satisfies a universal property, see [[Ore localization]]. The Ore localization of monoids has been generalized to categories, see [[category of fractions]].

If $R$ is a (unital) ring and $S\subset R$ is left Ore in a multiplicative monoid underlying $R$, then the addition on $S^{-1}R$ is also well defined, commutative and associative (checking all this is rather complicated) on $S^{-1}R$ such that the localization map is the map of rings and satisfies the universal property for the Ore localization of *rings*.

A **right Ore (sub)set** in a monoid or $R$ is a subset $S\subset R$ such that $S$ is left Ore subset in the opposite ring $R^{op}$.

An **Ore set** is a subset $S\subset R$ which is simultaneously left and right Ore subset. If $S\subset R\subset R'$ where $R$ and $R'$ are rings is a multiplicative subset then the satisfaction of Ore conditions in $R$ and Ore conditions in $R'$ are independent in general: the reason is that in a bigger ring one has simultaneously more conditions, but also a bigger set of possible solutions for the conditions. In general it is not sufficient to check the Ore condition on generators. If $S,T\subset R$ are two left Ore sets, it is not true in general that the image $i_T(S)$ in $T^{-1}R$ is left Ore; if it is then automatically $i_S(T)$ is left Ore in $S^{-1}R$ (mutually compatible left Ore sets) and $(i_S(T))^{-1}S^{-1} R$ is a ring canonically isomorphic to $(i_T(S))^{-1}T^{-1}T$. 

The left and right Ore conditions for rings were introduced by O. Ore in 1931 in order to study the linear equations class of rings which are now called Ore domains. 

(nlab note: there are many results on Ore conditions which are independent from the study of Ore localization; thus the entries should be separated)

[[!redirects Ore sets]]

