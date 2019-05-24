
#Contents#
* table of contents
{:toc}

## Idea

The notion of _weak bialgebra_ is a generalization of that of  [[bialgebra]] in which the comultiplication $\Delta$ is weak in the sense that $\Delta(1)\neq 1\otimes 1$ in general;
similarly the compatibility of counit with the multiplication
map is weakened (counit might fail to be a morphism of algebras). (Still a special case of [[sesquialgebra]].)

Correspondingly [[weak Hopf algebras]] generalize [[Hopf algebras]] accordingly. Every weak Hopf algebra defines a
[[Hopf algebroid]]. 

### Physical motivation

This kind of structures naturally comes in [[CFT]] models relation to quantum groups a root of unity: the full symmetry algebra is not quite a quantum group at root of unity, because if it were one would have to include the nonphysical quantum dimension zero finite-dimensional quantum group representations into the (pre)Hilbert space; those are the zero norm states which do not contribute to physics (like ghosts). If one quotients by these states then the true unit of a quantum group becomes an idempotent (projector), hence one deals with weak Hopf algebras instead as a price of dealing with true, physical, Hilbert space.

## Definitions

A __weak bialgebra__ is a tuple $(A,\mu,\eta,\Delta,\epsilon)$
such that $(A,\mu,\eta)$ is an associative unital algebra,
$(A,\Delta,\epsilon)$ is a coassociative counital coalgebra
and the following compatibilities, (i),(ii) and (iii), hold:

(i) the coproduct $\Delta$ is multiplicative $\Delta(x)\Delta(y)= \Delta(x y)$. If only (i) is satisfied, following Böhm, Caenapeel and Janssen 2011, we may speak of a __prebialgebra__.

(ii) the counit $\epsilon$ satisfies weak multiplicativity
$$
\epsilon(x y z) = \epsilon(x y_{(1)})\epsilon(y_{(2)} z),
$$
$$
\epsilon(x y z) = \epsilon(x y_{(2)})\epsilon(y_{(1)} z).
$$
A prebialgebra satisfying the first (the second) of the above properties is said to be left (right) monoidal. 

(iii) Weak comultiplicativity of the unit:

$$
\Delta^{(2)} (1) = (\Delta(1) \otimes 1)(1\otimes \Delta(1))
$$
$$
\Delta^{(2)} (1) = (1 \otimes\Delta(1))(\Delta(1) \otimes 1)
$$
A prebialgebra satisfying the first (the second) of the above properties is said to be left (right) comonoidal.

As usually in the context of coassociative coalgebras, we denoted $\Delta^{(2)} := (id\otimes\Delta)\Delta = 
(\Delta\otimes id)\Delta$.

A weak $k$-bialgebra $A$ is a __weak Hopf algebra__ if it has a $k$-linear map $S:A\to A$ (which is then called an antipode)
such that for all $x\in A$
$$
x_{(1)} S(x_{(2)}) = \epsilon(1_{(1)} x)1_{(2)},
$$
$$
S(x_{(1)})x_{(2)} = 1_{(1)} \epsilon(x 1_{(2)}),
$$
$$
S(x_{(1)})x_{(2)} S(x_{(3)}) = S(x)
$$
It follows that the antipode is antimultiplicative, $S(x y)=S(y)S(x)$, and
anticomultiplicative, $\Delta(S(x)) = S(x)_{(1)}\otimes S(x)_{(2)} = 
S(x_{(2)})\otimes S(x_{(1)})$.

## Properties

### Idempotents ("projections")

For every weak bialgebra there are $k$-linear maps 
$\Pi^L,\Pi^R:A\to A$ defined by
$$
\Pi^L(x) := \epsilon(1_{(1)} x) 1_{(2)},\,\,\,\,
\Pi^R(x) := 1_{(1)}\epsilon(x 1_{(2)}).
$$
Expressions for $\Pi^L(x),\Pi^R(x)$ are already met above as the right hand sides in two of the axioms for the antipode. Maps $\Pi^L,\Pi^R$
are idempotents, $\Pi^R\Pi^R = \Pi^R$ and $\Pi^L\Pi^L = \Pi^L$:
$$\array{
\Pi^L(\Pi^L(x)) &=& \epsilon\left(1_{(1')}\epsilon(1_{(1)}x) 1_{(2)}\right)1_{(2')}
= \epsilon(1_{(1)}x)\epsilon(1_{(1')}1_{(2)}) 1_{(2')} 
\\ &=&\epsilon(1_{(1)}x)\epsilon(1_{(2)}) 1_{(3)} 
= \epsilon(1_{(1)}x)1_{(2)} = \Pi^L(x).
}$$

Notice $\epsilon(x z) = \epsilon(x 1 z)  = \epsilon(x 1_{(2)})\epsilon(1_{(1)}z)) = \epsilon(x \epsilon(1_{(1)}z))1_{(2)} = \epsilon(x\Pi^L(z)) = \epsilon(\Pi^R(x)z)$. 
The images of the idempotents $A^R = \Pi^R(A)$ and $A^L = \Pi^L(R)$ are dual as $k$-linear spaces: there
is a canonical nondegenerate pairing $A^L\otimes A^R\to k$ 
given by $(x,y) \mapsto \epsilon(y x)$.

Also $\Pi^L(x\Pi^L(y)) = \Pi^L(x y)$ 
 and $\Pi^R(\Pi^R(x)y) = \Pi^R(x y)$,
 dually $\Delta(A^L)\subset A\otimes A^L$ 
        and $\Delta(A^R)\subset A^R\otimes A$,
 and in particular $\Delta(1)\in A^R\otimes A^L$.

Sometimes it is also useful to consider the idempotents $\bar\Pi^L,\bar\Pi^R:A\to A$ defined by
$$
\bar\Pi^L(x) := \epsilon(1_{(2)} x) 1_{(1)},\,\,\,\,
\bar\Pi^R(x) := 1_{(2)}\epsilon(x 1_{(1)}).
$$
$$\array{
\bar\Pi^L(\bar\Pi^L(x))&=&\epsilon(1_{(2')}\epsilon(1_{(2)}x)1_{(1)})1_{(1')} = \epsilon(1_{(2)}x)\epsilon(1_{(2')}1_{(1)})1_{(1')} \\
&=& \epsilon(1_{(3)}x)\epsilon(1_{(2)})1_{(1)}=
\epsilon(1_{(2)}x)1_{(1)} = \bar\Pi^L(x).
}$$

### Relation to fusion categories

Under [[Tannaka duality]] (semisimple) weak Hopf algebras correspond to (multi-)[[fusion categories]] ([Ostrik](#Ostrik)).

## Literature

Weak comultiplications were introduced in

* G. Mack, [[Volker Schomerus]], _Quasi Hopf quantum symmetry in quantum theory_, Nucl. Phys. B370(1992) 185.

where also weak quasi-bialgebras are considered and physical motivation is discussed in detail. Further work in this vain is in

* [[G. Böhm]], [[K. Szlachányi]], _A coassociative $C^\ast$-quantum group with non-integral dimensions_, Lett. Math. Phys. __35__ (1996) 437--456, [arXiv:q-alg/9509008](http://arxiv. rg/abs/q-alg/9509008); _Weak $C*$-Hopf algebras: the coassociative symmetry of non-integral dimensions_, in: Quantum groups and quantum spaces (Warsaw, 1995), 9-19, Banach Center Publ. __40__, Polish Acad. Sci., Warszawa 1997. 
* Florian Nill, _Axioms for weak bialgebras_, [math.QA/9805104](http://arxiv.org/abs/math/9805104)
* [[G. Böhm]], F. Nill, [[K. Szlachányi]], _Weak Hopf algebras. I. Integral theory and $C^\ast$-structure, J. Algebra __221__ (1999), no. 2, 385-438, [math.QA/9805116](http://arxiv.org/abs/math/9805116) #{BohmNillSzlachanyi}

Now these works are understood categorically from the point of view of weak monad theory:

* [[Gabriella Böhm]], Stefaan Caenepeel, Kris Janssen, _Weak bialgebras and monoidal categories_, Comm. Algebra __39__ (2011), no. 12 (special volume dedicated to Mia Cohen), 4584-4607. [arXiv:1103.226](http://arxiv.org/abs/1103.2261) 
* [[Gabriella Böhm]], [[Stephen Lack]], [[Ross Street]], _Weak bimonads and weak Hopf monads_, J. Algebra 328 (2011), 1-30, [arXiv:1002.4493](http://arxiv.org/abs/1002.4493)  
* [[Gabriella Böhm]], Jos&#233; G&#243;mez-Torrecillas, _On the double crossed product of weak Hopf algebras_, [arXiv:1205.2163](arXiv/1205.2163)  

The relation to [[fusion categories]] is discussed in 

* Takahiro Hayashi, _A canonical Tannaka duality for finite semisimple tensor categories_ ([arXiv:math/9904073](http://arxiv.org/abs/math/9904073))

* [[Victor Ostrik]], _Module categories, weak Hopf algebras and modular invariants_ ([arXiv:math/0111139](http://arxiv.org/abs/math/0111139)) 
 {#Ostrik}

category: algebra

[[!redirects weak bialgebras]]

[[!redirects weak Hopf algebra]]
[[!redirects weak Hopf algebras]]


