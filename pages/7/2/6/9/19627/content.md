
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

# The Fundamental Theorem of Arithmetic
* table of contents
{: toc}

## Idea

The so-called _Fundamental Theorem of Arithmetic_ (sometimes _FTA_, although this can also mean the [[Fundamental Theorem of Algebra]]) is the statement that the [[ring of integers]] is a [[unique factorization domain]] (UFD).  The theorem is much older than the abstract concepts of [[ring theory]], and indeed the concept of UFD is an abstraction of this theorem.  Inasumuch as '[[arithmetic]]' can refer to [[number theory]], this is a pretty basic theorem in that field.


## Statements

Let $\mathbb{N}_+$ be the positive natural numbers, let $\mathbb{N}_+ \times \mathbb{N}_+$ be the [[cartesian product]] of $\mathbb{N}_+$, with canonical product projection functions $\pi_1:\mathbb{N}_+ \times \mathbb{N}_+ \to \mathbb{N}_+$ and $\pi_2:\mathbb{N}_+ \times \mathbb{N}_+ \to \mathbb{N}_+$, and let $A^*$ be the [[free monoid]] on the set $A$. Let $p:\mathbb{N}_+ \to \mathbb{N}_+$ be the function which takes a positive natural number $n$ to the $n$-th [[prime number]]. 

Since the positive natural numbers form a [[monoid]] with respect to multiplication, finite products exist, given by the [[monoid homomorphism]] 

$$\prod_{i = 0}^{\mathrm{len}(-) - 1}(-)(i):\mathbb{N}_+^* \to \mathbb{N}_+$$ 

inductively defined on $\mathbb{N}_+^*$ by

$$\prod_{i = 0}^{\mathrm{len}(\epsilon) - 1} \epsilon(i) = 1$$

$$\prod_{i = 0}^{\mathrm{len}(h(a)) - 1} (h(a))(i) = a$$

$$\left(\prod_{i = 0}^{\mathrm{len}(a) - 1} a(i)\right) \cdot \left(\prod_{i = 0}^{\mathrm{len}(b) - 1} b(i)\right) = \prod_{i = 0}^{\mathrm{len}(a b) - 1} (a b)(i)$$

+-- {: .num_theorem}
###### Theorem
There is a [[bijection]] $\mathrm{uf}:\mathbb{N}_+ \cong (\mathbb{N}_+ \times \mathbb{N}_+)^*$ such that for every positive natural number $n$, 

$$n = \prod_{i = 0}^{\mathrm{len}(\mathrm{uf}(n)) - 1} p(\pi_1(\mathrm{uf}(n)(i)))^{\pi_2(\mathrm{uf}(n)(i))}$$

equivalently, for every list of pairs of positive natural numbers $a:(\mathbb{N} \times \mathbb{N})^*$

$$\mathrm{uf}^{-1}(a) = \prod_{i = 0}^{\mathrm{len}(a) - 1} p(\pi_1(a(i)))^{\pi_2(a(i))}$$
=--

Equivalently, instead of using lists of pairs of positive natural numbers, one could just use [[finite multisets]] of positive natural numbers, which are lists of lists of positive natural numbers. 

+-- {: .num_theorem}
###### Theorem
There is a [[bijection]] $\mathrm{uf}:\mathbb{N}_+ \cong (\mathbb{N}_+^*)^*$ such that for every positive natural number $n$, 

$$n = \prod_{i = 0}^{\mathrm{len}(\mathrm{uf}(n))} \prod_{j = 0}^{\mathrm{len}(\mathrm{uf}(n)(i)) - 1} p(\mathrm{uf}(n)(i)(j))$$

equivalently, for every finite multiset of positive natural numbers $a:(\mathbb{N}_+^*)^*$

$$\mathrm{uf}^{-1}(a) = \prod_{i = 0}^{\mathrm{len}(a) - 1} \prod_{j = 0}^{\mathrm{len}(a(i)) - 1} p(a(i)(j))$$
=--

+-- {: .num_theorem}
###### Theorem
The [[free commutative monoid]] on the [[prime numbers]] is [[isomorphic]] to the [[multiplicative subset]] of [[positive number|positive]] [[natural numbers]].   
=--

+-- {: .num_cor}
###### Corollary

The [[ring of integers]] is a [[unique factorization domain]].
=--


[[!redirects fundamental theorem of arithmetic]]
[[!redirects Fundamental Theorem of Arithmetic]]
