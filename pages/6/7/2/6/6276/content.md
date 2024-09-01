
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Magnus algebras and Magnus group

Let $X$ be a set of symbols and let $k$ denote the [[ground field]]. 

The [[free construction|free]] [[associative algebra|associative k-algebra]] $k\langle X \rangle$ on the [[set]] $X$ where $k$ is a [[commutative ring|commutative]] [[unital ring|unital]] [[ring]], will be denoted $A(X)$. It is clearly [[graded algebra|graded]] (by the length of the word) as $A(X) = \oplus_n A^n(X)$. The product of $k$-modules $\hat{A}(X) = \prod_n A^n(X)$ has a natural multiplication 

$$
(ab)_n = \sum_{i = 0}^n a_i b_{n-i}
$$

where $a = (a_n)_n$ and $b = (b_n)_n$. Furthermore, $\hat{A}(X)$ has the topology of the product of [[discrete topological space]]s. This makes $\hat{A}(X)$ a [[Hausdorff space|Hausdorff topological]] algebra, where 
the ground field is considered discrete and $A(X)$ is dense in $\hat{A}(X)$. We say that $\hat{A}(X)$ is the __Magnus algebra__ with coefficients in $k$. (Bourbaki-Lie gr. II.5). 

An element in $\hat{A}(X)$ is invertible (under multiplication) iff it's free term is invertible in $k$. 

The __Magnus group__ is the (multiplicative) subgroup of the Magnus algebra consisting of all elements in the Magnus algebra with free 
term $1$. 

### Hausdorff group and Hausdorff series

The [[free Lie algebra]] $L(X)$ naturally embeds in (the Lie algebra corresponding to the associative algebra) $A(X)\hookrightarrow \hat{A}(X)$; one defines $\hat{L}(X)$ as the closure of $L(X)$ in $\hat{A}(X)$. The exponential series and the makes sense in $\hat{A}(X)$; when restricted to $\hat{L}(X)$ it gives a bijection between $\hat{L}(X)$ and a closed subgroup of the Magnus group which is sometimes called the Hausdorff group $exp(\hat{L}(X))$.  

__Hausdorff series__ $H(U,V)$ is an element $log(exp(U)exp(V))$ in $\hat{L}(\{U,V\})$. 

The formula $exp(X)exp(Y) = (exp(Y)exp(X))^{-1}$ implies the basic symmetry of the Hausdorff series: $H(-Y,-X) = -H(X,Y)$.

The specializations of the Hausdorff series 
in Lie algebras which are not necessarily free are known as 
the __Baker-Campbell-Hausdorff__ series and play the role in the corresponding BCH formula $exp(U)exp(V) = exp(H(U,V))$.  

The BCH formula can be written in many ways, the most important which belong to Dynkin. The part which is linear in one of the variables involves [[Bernoulli number]]s.

There is a decomposition $H(X,Y) = \sum_{N=0}^\infty H_N(X,Y)$ where
__Dynkin's Lie polynomials__ $H_N = H_N(X,Y)$ are defined
recursively by $H_1 = X+Y$ and
$$
(N+1)H_{N+1} = \frac{1}{2}[X-Y,H_N] +
\sum_{r = 0}^{\lfloor N/2 -1\rfloor}
\frac{B_{2r}}{(2r)!}\sum_s
[H_{s_1},[H_{s_2},[ \ldots, [H_{s_{2r}},X+Y]\ldots]]]
$$

where the sum over $s$ is the sum over all
$2r$-tuples $s = (s_1,\ldots,s_{2r})$
of strictly positive integers whose sum $s_1 +\ldots+s_{2r} = N$. 

Hausdorff series satisfies the symmetry $H(-Y,-X) = -H(X,Y)$.

First few terms of Hausdorff series are

$$
H(X,Y) = X + Y + \frac{1}{2}[X,Y] + \frac{1}{12}([X,[X,Y]]+[Y,[Y,X]]) + \frac{1}{24}[Y,[X,[Y,X]]] + \ldots
$$


## Related entries

* [[Lie theory]] 

* [[Malcev completion]]

* [[exponential map]]

* [[Magnus expansion]]


## Literature

> The following references concern the classical part of the subject. For the references connecting Hausdorff series to [[Drinfeld associators]], the [[Grothendieck-Teichmueller group]] and the [[Kashiwara-Vergne conjecture]] see there.

Early discussion:

* Rüdiger Achilles, Andrea Bonfiglioli: *The early proofs of the theorem of Campbell, Baker, Hausdorff, and Dynkin*, Arch. Hist. Exact Sci. **66** (2012) 295–358 &lbrack;[doi:10.1007/s00407-012-0095-8](https://doi.org/10.1007/s00407-012-0095-8)&rbrack;

* [[Eugene B. Dynkin]], _Calculation of the coefficents in the Campbell-Hausdorff formula_, Doklady Akad. Nauk SSSR (N.S.) **57** (1947) 323-326 


* [[Wilhelm Magnus]], *A connection between the Baker-Hausdorff formula and a problem of Burnside*, Ann. of Math. __52__ (1950) 111-126

* [[Nicolas Bourbaki]], _Lie groups and algebras_, chapter II

* [[M M Postnikov]], Lectures on geometry, Semester V, Lie groups and algebras

* [[Kuo-Tsai Chen]], _Integration of paths, geometric invariants and a generalized Baker--Hausdorff formula_, Annals of Mathematics __65__:1 (1957) 163--178 [doi](https://doi.org/10.2307/1969671) [jstor](http://www.jstor.org/stable/1969671) 


Review:

* [[Terence Tao]], 254A, Notes 1, _Lie groups, Lie algebras, and the Baker-Campbell-Hausdorff formula_, blog entry

* Terry Tao's blog: [the-c11-baker-campbell-hausdorff-formula](https://terrytao.wordpress.com/2011/06/21/the-c11-baker-campbell-hausdorff-formula)

* [Wikipedia](https://en.wikipedia.org/wiki/Baker%E2%80%93Campbell%E2%80%93Hausdorff_formula)

See also:

* V. Kurlin, _The Baker-Campbell-Hausdorff formula in the free metabelian Lie algebra
_ &lbrack;[http://arxiv.org/abs/math/0606330](http://arxiv.org/abs/math/0606330)&rbrack;


* Federico Zadra et al. _The flow method for the Baker-Campbell-Hausdorff formula: exact results_, J. Phys. A: Math. Theor. __56__ (2023) 385206 [doi](https://doi.org/10.1088/1751-8121/acf102)

category: algebra
[[!redirects Baker-Campbell-Hausdorff series]]
[[!redirects BCH formula]]
[[!redirects Baker-Campbell-Hausdorff formula]]
[[!redirects BCH theorem]]
[[!redirects Campbell-Hausdorff formula]]
[[!redirects Hausdorff formula]]