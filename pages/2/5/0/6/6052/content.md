## Idea

A bialgebroid may be viewed as a multiobject generalization of a concept of a [[bialgebra]], or a possibly noncommutative generalization of a space-algebra dual version of the concept of an internal category in spaces.

#### Nomenclature

This entry is about "associative" bialgebroid, see also the different concept of a [[Lie bialgebroid]]. 

#### Motivation in Tannakian formalism

When a monoidal category has a [[fiber functor]] to a category of vector spaces over a field, one tries to "reconstruct" the category as the category of representations of the endomorphism object of a fiber functor. One often does not have a fiber functor to vector spaces but only to bimodules over some base algebra $A$. Sometimes in such cases, the object of endomorphisms of the fiber functor form a bialgebroid over $A$ and the category is equivalent to the category of representations of that bialgebroid.

## Definition

Given a unital (possibly noncommutative) ring $R$ an __$R$-bialgebroid__ is an $R$-$R$-bimodule $H$ (object of ${}_R \mathcal{M}_R$) equipped with a structure of a comonoid in ${}_R \mathcal{M}_R$ (i.e. an $R$-coring) and of a monoid in ${}_{R^e}\mathcal{M}_{R^e}$ (i.e. an $R^e$-ring), where $R^e = R^{op}\otimes R$ is the enveloping ring of $R$; and the structures of a monoid and a comonoid satisfy certain compatibility conditions. These compatibility conditions are equivalent to the fact that the monad ${}_\otimes_{R^e} H : \mathcal{M}_{R^e}\to \mathcal{M}_{R^e}$ is [[opmonoidal monad|opmonoidal]]. The category of $R$-comodules is by definition the category of comodules over the underlying $R$-coring. 

## Literature

Related notions: [[Hopf algebroid]]

#### Commutative case

The commutative case is rather classical. See for example the appendix to 

* Douglas C. Ravenel, _Complex cobordism and stable homotopy  groups of spheres_, Pure and Applied Mathematics __121__. Academic Press Inc., Orlando, FL, 1986. 

#### Noncommutative case

The first version of a bialgebroid over a noncommutative base was more narrow:

* M. Sweedler, _Groups of simple algebras_, Publ. IHES 44:79&#8211;189, 1974, [numdam](http://www.numdam.org/item?id=PMIHES_1974__44__79_0)

A modern generality, but in different early formalism, is due Takeuchi, under the name of $\times_A$-bialgebra (as it involves the $\times_A$-product, nowdays called [[Takeuchi product]]):

* M. Takeuchi, _Groups of algebras over $A \times \bar{A}$, J. Math. Soc. Japan __29__, 459&#8211;492, 1977, [MR0506407](http://www.ams.org/mathscinet-getitem?mr=0506407), [euclid](http://projecteuclid.org/euclid.jmsj/1240432948)

See also [[Hopf algebroid]]. 

* [[Gabriella Böhm]], _Internal bialgebroids, entwining structures and corings_, [math.QA/0311244](http://arxiv.org/abs/math/0311244), in: Algebraic structures and their representations, 207&#8211;226,
Contemp. Math. __376__, Amer. Math. Soc. 2005.
* [[G. Böhm]], _Hopf algebroids_, (a chapter of) Handbook of algebra, [arxiv:math.RA/0805.3806](http://arxiv.org/abs/0805.3806)
* [[Kornél Szlachányi]], _The monoidal Eilenberg&#8211;Moore construction and bialgebroids_, J. Pure Appl. Algebra __182__, no. 2&#8211;3 (2003) 287&#8211;315; _Fiber functors, monoidal sites and Tannaka duality for bialgebroids_, [arxiv/0907.1578](http://arxiv.org/abs/0907.1578)
* [[T. Brzeziński]], G. Militaru, _Bialgebroids, $\times_{R}$-bialgebras and duality_, J. Algebra 251: 279-294, 2002, [math.QA/0012164](http://arxiv.org/abs/math/0012164)

There is also a notion of quasibialgebroid, where the coassociativity is weakened by a [[bialgebra cocycle|bialgebroid 3-cocycle]]. 

[[!redirects bialgebroids]]
[[!redirects associative bialgebroid]]