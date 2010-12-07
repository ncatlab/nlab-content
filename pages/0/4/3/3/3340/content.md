
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Cyclic homology_ is [[Hochschild homology]] on cyclically invariant chains.

We may understand [[Hochschild homology]] as the [[cohomology]] of [[free loop space object]]s (as described there). These free loop space objects are canonically equipped with a [[circle group]]-[[action]] that rotates the loops. _Cyclic homology_ is the corresponding $S^1$-[[equivariant cohomology]] of free loop space objects.

## Definition

### The chain complex for cyclic homology

Let $A$ be an [[associative algebra]] over a [[ring]] $k$. Write $C_\bullet(A,A)$ for the [[Hochschild homology]] [[chain complex]] of $A$ with coefficients in $A$.

For each $n \in \mathbb{N}$ let $\lambda : C_n(A,A) \to C_n(A,A)$ be the $k$-linear map that cyclically permutes the elements and introduces a sign:

$$
  \lambda : (a_0, a_1, \cdots, a_{n-1}, a_n)
  \mapsto 
   (-1)^n
   (a_n, a_0  , \cdots, a_{n-1})
  \,.
$$


+-- {: .un_defn}
###### Definition

The **cyclic homology complex** $C^\lambda_\bullet(A)$ of $A$ is the quotient of the Hochschild homology complex of $A$ by cyclic permutations:

$$
  C_\bullet^\lambda(A) := C_\bullet(A,A)/im(Id-\lambda)
  \,.
$$

The [[homology]] of the cyclic complex, denoted

$$
  HC_n(A) := H_n( C_\bullet^\lambda(A) )
$$

is called the **cyclic homology** of $A$.
=--

If $I\subset A$ is an ideal, then the **relative cyclic homology** groups $HC_n(A,I)$ are the homology groups of the complex $C_\bullet(A,I) = ker(C_\bullet(A)\to C_\bullet(A/I))$.

## Related concepts

* [[cycle category]]

* [[cyclic object]].

## References

The complex for cyclic homology was considered by [[Alain Connes]] and [[Boris Tsygan]] around 1981, 1982. 

A standard textbook is

* [[J-L. Loday]], _Cyclic homology_, Grundleheren Math.Wiss. __301__, Springer, 2nd ed.

Quick lectures notes are in

* [[D. Kaledin]], _Tokyo lectures "Homological methods in non-commutative geometry"_, ([pdf](http://imperium.lenin.ru/~kaledin/tokyo/final.pdf)), ([TeX](http://imperium.lenin.ru/~kaledin/tokyo/final.tex)); and related but different [Seoul lectures](http://imperium.lenin.ru/~kaledin/seoul)

A survey is in

* [[Masoud Khalkhali]], _A short survey of cyclic cohomology_, [arxiv/1008.1212](http://arxiv.org/abs/1008.1212)


An influential original reference is 

* [[Boris Tsygan]], [[Boris Feigin]],  _[[Additive K-theory]]_, in LNM 1289 (1987), edited by Yu. I. Manin, pp. 67--209, seminar 1984-1986 in Moscow), [MR89a:18017](http://www.ams.org/mathscinet-getitem?mr=923136)

In the discu

* [[Alain Connes]], _Noncommutative geometry_, Acad. Press 1994, 661 p. [PDF](http://www.alainconnes.org/docs/book94bigpdf.pdf) 


* [[D. Kaledin]], _Cyclic homology with coefficients_, [math.KT/0702068](http://arxiv.org/abs/math.KT/0702068), to appear in Yu. Manin's 70th anniversary volume.

* [[Max Karoubi]], _Homologie cyclique et K-th&#233;orie_, Ast&#233;rique __149__, Soci&#233;t&#233; Math&#233;matique de France (1987). 

[[!redirects cyclic homology]]

[[!redirects cyclic (co)homology]]