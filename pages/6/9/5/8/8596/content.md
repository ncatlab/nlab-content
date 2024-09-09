## Overview

Given an [[associative algebra|associative]] unital $k$-algebra $A$, with enveloping algebra $A^e = A\otimes A^{op}$, the Takeuchi product $\times_A$ is a certain bifunctor in the category of $A^e$-[[ring over a ring|ring]]s defined as an [[end]] of a [[coend]]. 

It generalizes a construction of [[M. E. Sweedler]] where $A$ is commutative; Sweedler's article may be itself viewed in a sense a "generalization of the relative [[Brauer group]] and the associated theory". 

## Definition

Let $M$ be an $A$-bimodule and $N$ an $A^{op}$-bimodule.

$$
M\times_A N = \int_b \int^a {}_{a^{op}}M_{b^{op}} \otimes {}_a N_{b}
$$
where we use MacLane's conventions for [[end]] $\int_b$ and [[coend]] $\int^a$ (while most Hopf algebraic references interchange the notion upside down, writing $\int^b\int_a$ instead).

This calculates to
$$
M\times_A N = \{\sum_i m_i\otimes n_i\in M\otimes_A N \,|\, (\forall b\in A)\sum_i m_i.b^{op} \otimes n_i = \sum_i m_i\otimes n_i.b \}\subset M\otimes_A N
$$

If $M$ is in fact $A^e$-bimodule we define the $A$-bimodule structure on $M\times_A N$ by acting on $M$ factor; likewise if $N$ is an $A^e$-bimodule we define the $A^{op}$-bimodule structure on $M\times_A N$ by acting on $N$ factor. Thus if both are $A^e$-bimodules, $M\times_A N$ is canonically an $A^e$-bimodule.

Now if $M= R,N = S$ are moreover $A^e$-rings, then they are in particular $A^e$-bimodules. While $R\otimes_A S$ is not carrying a well defined algebra structure, $R\times_A S$ is an associative unital algebra by factorwise multiplication.

## Properties

As it involves both a limit and a colimit construction, limits commute with limits, colimits with colimits, but not limit with colimits in general, Takeuchi's product is not associative up to isomorphism, hence it does not provide a monoidal category in general. 

## Applications

Takeuchi product is used in the theory of associative [[bialgebroid]]s over a noncommutative base.

## Literature

* [[Mitsuhiro Takeuchi]], _Groups of algebras over $A \times \bar{A}$, J. Math. Soc. Japan __29__, 459&#8211;492, 1977, [MR0506407](http://www.ams.org/mathscinet-getitem?mr=0506407), [euclid](http://projecteuclid.org/euclid.jmsj/1240432948)
* [[M. E. Sweedler]], _Groups of simple algebras_, Publ. IHES __44__, 79--189, [MR51:587](http://www.ams.org/mathscinet-getitem?mr=51:587), [numdam](http://www.numdam.org/item?id=PMIHES_1974__44__79_0)
* [[T. Brzeziński]], G. Militaru, _Bialgebroids, $\times_{R}$-bialgebras and duality_, J. Algebra 251: 279-294, 2002, [math.QA/0012164](http://arxiv.org/abs/math/0012164)
* [[Peter Schauenburg]], _Bialgebras over noncommutative rings and a structure theorem for Hopf bimodules_, Appl. Categ. Structures __6__ (1998), 193--222, [ps](http://www.mathematik.uni-muenchen.de/%7Eschauen/papers/bnrsthb.ps) [doi](https://doi.org/10.1023/A:1008608028634)

category: algebra