<div class="rightHandSide toc">
[[!include infinity-Lie theory - contents]]
</div>


#Contents#
* tic
{: toc}

>this entry needs to be merged with [[Chevalley-Eilenberg cochain complex]]


## Ordinary concept

The [[cohomology]] of a $k$-[[Lie algebra]] $\mathfrak{g}$ with coefficients in the left $\mathfrak{g}$-module $M$ is defined as $H^*_{Lie}(\mathfrak{g},M) = Ext_{U\mathfrak{g}}^*(k,M)$ where $k$ is the ground field understood as a trivial module over the universal enveloping algebra $U\mathfrak{g}$; therefore it is a derived functor. Before this was understood in Cartan-Eilenberg's _Homological algebra_, Lie algebra cohomology and homology were defined by Chevalley-Eilenberg with a help of concrete Koszul-type resolution which is in this case a chain complex $Hom_{\mathfrak{g}}(U\mathfrak{g}\otimes_k \Lambda^* \mathfrak{g},M)$ where the first argument $U\mathfrak{g}\otimes_k \Lambda^* \mathfrak{g}$ is naturally equipped with a differential to start with (see below). This first argument underlines in fact a differential graded commutative algebra called the Chevalley-Eilenberg algebra, which is in $n$lab denoted (as well as its higher categorical analogues) by $CE(\mathfrak{g})$. 

## Definition 

Let $\mathfrak{g}$ be a finite-dimensional [[Lie algebra]] (i.e., an ordinary Lie algebra object in $Vect$), with underlying vector space $U\mathfrak{g}$. The Lie bracket is an alternating bilinear operation, hence defines a linear map 

$$[-, -]: U\mathfrak{g} \wedge U\mathfrak{g} \to U\mathfrak{g}$$

The linear transpose defines a linear map $d_1: U\mathfrak{g}^* \to U\mathfrak{g}^* \wedge U\mathfrak{g}^*$. 

Let $U\mathfrak{g}^*[1]$ denote the graded vector space whose only nonzero component is $U\mathfrak{g}^*$ concentrated in degree 1. The free commutative graded algebra $S(U\mathfrak{g}^*[1])$ on this graded vector space is given by the [[exterior algebra]], whose component in degree $k$ is the $k^{th}$ exterior power $\Lambda^k U\mathfrak{g}$. The map $d_1$ gives a degree 1 map 

$$d: U\mathfrak{g}^*[1] \to S(U\mathfrak{g}^*[1])$$ 

which in turn, by freeness, extends uniquely to a degree 1 [[derivation]] on the free commutative algebra, which we again call $d$. The Jacobi identity on $\mathfrak{g}$ is equivalent to the statement that $d^2 = 0$, hence we have defined a [[dg-algebra]]. This is the **Chevalley-Eilenberg algebra** (or CE-algebra) of the Lie algebra $\mathfrak{g}$. 

## Synthetic version

see 

* [[Chevalley-Eilenberg algebra in synthetic differential geomet|Chevalley-Eilenberg algebra in synthetic differential geometry]]


## Generalization in $\infty$-context

In the context of general [[Lie theory]] one notices that Chevalley&#8211;Eilenberg algebras generalized to arbitrary "quasi-free differential graded commutative algebras" are usefully thought of as providing a language that naturally allows to pass from Lie algebras to $L_\infty$-[[Lie infinity-algebroid|algebroid]]s: Chevalley&#8211;Eilenberg algebras are taken in this context to be the algebras of functions on [[NQ-supermanifolds]].

Closely related are [[Weil algebra]]s, which are the algebras of functions on the shifted tangent bundles of these [[NQ-supermanifolds]].


## Appearance in physics

In the physics literature Chevalley&#8211;Eilenberg algebras of $L_\infty$-[[Lie infinity-algebroid|algebroid]]s are addressed as [[BRST complexes]].

In this context

* the generators in degree 0 are called **fields**;

* the generators in degree $1$ are called **ghosts**;

* the generators in degree $2$ are called **ghosts of ghosts**;

* etc.


[[!redirects Chevalley--Eilenberg algebra]]
[[!redirects Chevalley–Eilenberg algebra]]
[[!redirects Chevalley-Eilenberg algebras]]
[[!redirects Chevalley--Eilenberg algebras]]
[[!redirects Chevalley–Eilenberg algebras]]