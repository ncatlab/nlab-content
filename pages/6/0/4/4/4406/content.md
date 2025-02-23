
# Contents
* automatic table of contents goes here
{: toc}

## Definition 

An [[ordered field]] $F$ is **real closed** if it satisfies the following two properties: 

* Any non-negative element $x \geq 0$ in $F$ has a [[square root]] in $F$; 

* Any odd-degree [[polynomial]] with coefficients in $F$ has a root in $F$. 

Notice that the order on a real closed field is definable from the algebraic structure: $x \leq y$ if and only if $\exists_z x + z^2 = y$. (In particular, there is a _unique_ ordering on a real closed field, defined by taking the positive elements to be precisely the nonzero squares.) In fact, the [[category]] of real closed fields and order-preserving field homomorphisms is a [[full subcategory]] of the category [[Field]] of [[fields]] and field homomorphisms. 


## Properties 

Real closed fields can be equivalently characterized by any of the following properties: 

1. $F$ is not [[algebraically closed field|algebraically closed]], but some finite [[field extension|extension]] is. This extension is necessarily $F[\sqrt{-1}]$. See also [[fundamental theorem of algebra]]. 

2. As a field, $F$ is [[elementary equivalence|elementarily equivalent]] to the field of real numbers. 

3. The [[intermediate value theorem]] holds for all [[polynomial functions]] with coefficients in $F$. 

4. $F$ is an ordered field that has no ordered algebraic extension. 

In fact, there is a [[completion]] of any [[ordered field]] to a real closed field, in the following sense: 

+-- {: .un_theorem}
###### Theorem

The full inclusion of the category of real closed fields and field homomorphisms to the category of ordered fields and ordered field homomorphisms has a left adjoint. 
=-- 

+-- {: .proof} 
###### Proof

We give a brief sketch of proof, referring to Lang's _Algebra_ ($3^{rd}$ edition), section IX.2, for more details. 

First, for each ordered field $F$, there is a real closed algebraic extension $F \to R$ that is order-preserving (theorem 2.11). This is called a **real closure** of the ordered field $F$. 

Second, any two real closures of $F$ are uniquely isomorphic (theorem 2.9); in fact, the proof shows there is at most one order-preserving homomorphism over $F$ between any two real closures. Therefore we may speak of _the_ real closure of $F$, which we denote as $\widebar{F}$. 

Finally, let $F \to R$ be any order-preserving field homomorphism to a real closed field $R$. We must show that $F \to R$ extends uniquely to a homomorphism $i: \widebar{F} \to R$. Any such homomorphism $i$ must factor through the subfield $R' \hookrightarrow R$ consisting of elements $\alpha \in R$ that are algebraic over $F$, since $\widebar{F}$ is algebraic over $F$. But this subfield is also real closed. Therefore, by the preceding paragraph, there is at most one homomorphism $\widebar{F} \to R'$ extending $F \to R'$, and the proof is complete. 
=--


## Examples 

1. The [[real number]]s form a real closed field. 

2. Real [[algebraic number]]s form a real closed field, which is the real closure of the ordered field of [[rational numbers]]. 

3. A field of nonstandard real numbers (as in Robinson [[nonstandard analysis]]) is real closed. 

4. [[surreal number|Surreal numbers]] form a (large) real closed field. 

5. If $F$ is real closed, then the field of [[Puiseux series]] over $F$ is also real closed. 

6. More generally, given a real closed field $F$, the field of [[Hahn series]] over $F$ with [[valuation ring|value group]] $G$ (a linearly ordered group) is real closed provided that $G$ is [[divisible group|divisible]].

7. Any [[o-minimal structure|o-minimal]] ordered ring structure $R$ is a real closed field. 

8. Given an o-minimal ordered ring $R$, the field of [[germ]]s at infinity of definable functions $R \to R$ in any o-minimal expansion of $(R, 0, 1, +, -, \cdot, \lt)$ is real closed. (By "germ at infinity", we mean an equivalence class of functions for which $f \equiv g$ if and only if $f(x) = g(x)$ for all sufficiently large $x$.)

## Infinites and infinitesimals 

Each real closed field $R$ contains a [[valuation ring|valuation]] subring $B \hookrightarrow R$ consisting of the "bounded" or archimedean elements, i.e., elements $x \in R$ such that $-n \leq x \leq n$ for some integer multiple $n$ of the identity. An element in the complement of $B$ is an **infinite** element of $R$, and the reciprocal of an infinite element is an **infinitesimal** element. The field of fractions of $B$ is clearly $R$. 

We remark that any real closed field contains a copy of the field of real [[algebraic numbers]], which as before we denote by $\widebar{\mathbb{Q}}$ (not to be confused with the algebraic closure of $\mathbb{Q}$). Each of the elements of $\widebar{\mathbb{Q}}$ is archimedean. 

Let $B^\ast$ be the group of units of $B$. The quotient $R^\ast/B^\ast$ is the **value group** of $R$. It can be viewed as the "group of orders of infinities and infinitesimals" of $R$. If $R$ is real closed, then the value group is a linearly ordered [[divisible group]] (divisible because we can take $n^{th}$ roots of positive elements in $R$). The structure of the value group as ordered group is an important invariant of the real closed field. 

In the other direction, to each ordered divisible abelian group $G$, there exists a real closed field having $G$ as its value group. For example, one may form the [[Hahn series]] over $\widebar{\mathbb{Q}}$ with value group $G$. 

## In constructive mathematics

In constructive mathematics, the various definitions of real closed field bifurcate, because of different definitions of an odd-degree polynomial. One could define an odd-degree polynomial as a polynomial whose coefficient for an odd number $n$ is [[denial inequality|not equal to]] zero and whose coefficient for all $i \gt n$ for is equal to zero. On the other hand, one could also define an odd-degree polynomial as a polynomial whose coefficient for an odd number $n$ is [[tight apartness relation|apart from]] zero and whose coefficient for all $i \gt n$ for is equal to zero. These two definitions are different from each other, the real numbers satisfy the second, while they do not satisfy the first. 

## Related concepts

* [Euclidean geometry -- Tarski's axioms](Euclidean+geometry#TarskiAxioms)

## References 

* [[Serge Lang]]: _Algebra_, 3rd ed. Springer (2002) &lbrack;[doi:10.1007/978-1-4613-0041-0](https://doi.org/10.1007/978-1-4613-0041-0)&rbrack;

* David Marker, _Notes on Real Algebra_ [(link)](http://www.math.uic.edu/~marker/orsay/real_algebra.pdf) 


[[!redirects real closed field]]
[[!redirects real closed fields]]
[[!redirects real-closed field]]
[[!redirects real-closed fields]]
