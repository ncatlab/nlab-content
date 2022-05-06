## Idea

A bialgebroid may be viewed as a multiobject generalization of a concept of a [[bialgebra]], or a possibly noncommutative generalization of a space-algebra dual version of the concept of an internal category in spaces.

#### Nomenclature

This entry is about "associative" bialgebroid, see also the different concept of a [[Lie bialgebroid]]. 

#### Motivation in Tannakian formalism

When a monoidal category has a [[fiber functor]] to a category of vector spaces over a field, one tries to "reconstruct" the category as the category of representations of the endomorphism object of a fiber functor. One often does not have a fiber functor to vector spaces but only to bimodules over some base algebra $A$. Sometimes in such cases, the object of endomorphisms of the fiber functor form a bialgebroid over $A$ and the category is equivalent to the category of representations of that bialgebroid.

## Definition

### Via monoidal categories

Given a unital (possibly noncommutative) ring $R$ an __$R$-bialgebroid__ is an $R$-$R$-bimodule $H$ (object of ${}_R \mathcal{M}_R$) equipped with a structure of a comonoid in ${}_R \mathcal{M}_R$ (i.e. an $R$-coring) and of a monoid in ${}_{R^e}\mathcal{M}_{R^e}$ (i.e. an $R^e$-ring), where $R^e = R^{op}\otimes R$ is the enveloping ring of $R$; and the structures of a monoid and a comonoid satisfy certain compatibility conditions. These compatibility conditions are equivalent to the fact that the monad ${}_{\otimes_{R^e}} H : \mathcal{M}_{R^e}\to \mathcal{M}_{R^e}$ is [[opmonoidal monad|opmonoidal]]. The category of $R$-comodules is by definition the category of comodules over the underlying $R$-coring. 

### An explicit definition

If $A$ is an [[associative algebra]] over some [[ground field]] $k$, then a left associative $A$-bialgebroid is another associative $k$-algebra $H$ together with the following additional maps:
an algebra map $\alpha:A\to H$ called the source map, 
an algebra map $\beta:A^{op}\to H$ called the target map, so that the elements of the images of $\alpha$ and $\beta$ commute in $H$, therefore inducing an $A$-bimodule structure on $H$ via the rule $a.h.b = \alpha(a)\beta(b) h$ for $a,b\in A, h\in H$; an $A$-bimodule morphism $\Delta:H\to H\otimes_A H$ which is required to be a counital coassociative comultiplication on $H$ in the monoidal category of $A$-bimodules with monoidal product $\otimes_A$. The map $H\otimes A\ni h\otimes a\mapsto \epsilon(h\alpha(a))\in $ must be a left action extending the multiplication $A\otimes A\to A$ along $\alpha\otimesid_A$. Furthermore, a compatibility between the comultiplication $\Delta$ and multiplications on $H$ and on $H\otimes H$ is required. For a noncommutative $L$ the tensor square $H\otimes_A$ is not an algebra, hence asking for a bialgebra-like compatibility that $\Delta:H\to H\otimes_A H$ is a morphism of $k$-algebras does not make sense. Instead, one requires that $H\otimes_A H$ has a $k$-subspace $T$ which contains the image of $\Delta$ and has a well-defined multiplication induced from its preimage under the projection from the usual tensor square algebra $H\otimes H$. Then one requires that the [[corestriction]] $\Delta|^T :H\to T$ is a homomorphism of unital algebras. Under these conditions, one can make a canonical choice for $T$, namely the so called Takeuchi's product $H\times_A H\subset H\otimes_A H$, which always inherits an associative multiplication along the projection from $H\otimes H$. 

### Via $A\otimes A^{op}$-rings

All modules and morphisms will be over a fixed ground commutative ring $k$. 

A __left $A$-bialgebroid__ is 
an $A\otimes_k A^{op}$-[[ring]] $(H,\mu_H,\eta)$, 
together with the $A$-bimodule map "comultiplication" $\Delta : H\to H\otimes_A H$, which is coassociative and counital with a counit $\epsilon$, such that 

(i) the $A$-bimodule structure used on $H$ is $a.h.a':= s(a)t(a')h$, where $s := \eta(-\otimes 1_A):A\to H$ and $t:=\eta(1_A\otimes -):A^{op}\to H$ are the algebra maps induced by the unit $\eta$ of the $A\otimes A^{op}$-ring $H$

(ii) the coproduct $\Delta : H\to H\otimes_A H$ corestricts to the [[Takeuchi product]] and the corestriction $\Delta : H\to H\times_A H$ 
is a $k$-algebra map, where the Takeuchi product $H\times_A H$ has a multiplication induced factorwise

(iii) $\epsilon$ is a left [[character]] on the $A$-ring $(H,\mu_H,s)$. 

Notice that $H\otimes_A H$ is in general not an algebra, just an  $A$-bimodule. That is why (ii) is needed. An equivalent condition to (ii) is the following: the formula $h.(\sum_i k_i \otimes l_i) = \sum_i h_{(1)}\cdot k_i \otimes h_{(2)} \cdot l_i$ defines a well-defined action of $H$ on $H\otimes_A H$. 

The definition of a __right $A$-bialgebroid__ differs by the $A$-bimodule structure on $H$ given instead by $a.h.a':= h s(a')t(a)$ and the counit $\epsilon$ is a _right_ character on the $A$-coring $(H,\mu_H,t)$ ($t$ and $s$ can be interchanged in the last requirement). 

## Literature

Related notions: [[Hopf algebroid]]

#### Commutative case

The commutative case is rather classical. See for example the appendix to 

* Douglas C. Ravenel, _Complex cobordism and stable homotopy  groups of spheres_, Pure and Applied Mathematics __121__. Academic Press Inc., Orlando, FL, 1986. 

#### Noncommutative case

The first version of a bialgebroid over a noncommutative base was more narrow:

* M. Sweedler, _Groups of simple algebras_, Publ. IHES 44:79&#8211;189, 1974, [numdam](http://www.numdam.org/item?id=PMIHES_1974__44__79_0)

A modern generality, but in different early formalism, is due Takeuchi (who was motivated to generalize the results from the Sweedler's paper), under the name of $\times_A$-bialgebra (as it involves the $\times_A$-product, nowdays called [[Takeuchi product]]):

* M. Takeuchi, _Groups of algebras over $A \times \bar{A}$, J. Math. Soc. Japan __29__, 459&#8211;492, 1977, [MR0506407](http://www.ams.org/mathscinet-getitem?mr=0506407), [euclid](http://projecteuclid.org/euclid.jmsj/1240432948)

Lu introduces the name bialgebroid for a structure which is equivalent to the Takeuchi's $\times_A$-bialgebra (though differently axiomatized there): 

*  Jiang-Hua Lu, _Hopf algebroids and quantum groupoids_, Int. J. Math. __7__, 1 (1996) pp. 47-70, [q-alg/9505024](http://arxiv.org/abs/q-alg/9505024), [MR95e:16037](http://www.ams.org/mathscinet-getitem?mr=95e:16037), [doi](http://dx.doi.org/10.1142/S0129167X96000050)

Modern treatments are in 

* [[Gabriella Böhm]], _Internal bialgebroids, entwining structures and corings_, [math.QA/0311244](http://arxiv.org/abs/math/0311244), in: Algebraic structures and their representations, 207&#8211;226,
Contemp. Math. __376__, Amer. Math. Soc. 2005.
* [[G. Böhm]], _Hopf algebroids_, (a chapter of) Handbook of algebra, [arxiv:math.RA/0805.3806](http://arxiv.org/abs/0805.3806)
* [[Kornél Szlachányi]], _The monoidal Eilenberg&#8211;Moore construction and bialgebroids_, J. Pure Appl. Algebra __182__, no. 2&#8211;3 (2003) 287&#8211;315; _Fiber functors, monoidal sites and Tannaka duality for bialgebroids_, [arxiv/0907.1578](http://arxiv.org/abs/0907.1578)
* [[T. Brzeziński]], G. Militaru, _Bialgebroids, $\times_{R}$-bialgebras and duality_, J. Algebra 251: 279-294, 2002, [math.QA/0012164](http://arxiv.org/abs/math/0012164)
* J. Donin, A. Mudrov, _Quantum groupoids and dynamical categories_,  
J. Algebra __296__ (2006), no. 2, 348&#8211;384, [math.QA/0311316](http://arxiv.org/abs/math/0311316), [MR2007b:17022](http://www.ams.org/mathscinet-getitem?mr=2201046), [doi](http://dx.doi.org/10.1016/j.jalgebra.2006.01.001); MPIM-2004-21, [dvi](http://www.mpim-bonn.mpg.de/preblob/1921) with hyperlinks, [ps](http://www.mpim-bonn.mpg.de/preblob/1922)

There is also a notion of quasibialgebroid, where the coassociativity is weakened by a [[bialgebra cocycle|bialgebroid 3-cocycle]]. See also [[Hopf algebroid]]. 

[[!redirects bialgebroids]]
[[!redirects associative bialgebroid]]