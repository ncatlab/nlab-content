
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Massey product_ of length $n$ is a certain $n$-ary products on the [[cohomology ring]] of an [[A-infinity algebra]] (in particular a [[dg-algebra]]).

### In components

Roughly, Massey Products are to [[cohomology]] as [[Toda Brackets]] are to [[homotopy]].

Somewhat more fully, while Toda brackets are relations between mapping space groups $Map_* (\Sigma^n A_0, A_{n+2}) $ and chains of maps $ A_0 \to \cdots \to A_{n+2} $, and generalizing nullhomotopy of composition, Massey products are a relation between cohomology groups
$ H^{p_0 + \cdots + p_k - k + 1}(X) $ and $ H^{p_0} (X) \otimes \cdots \otimes H^{p_k}(X) $, generalizing the vanishing of pairwise [[cup product]]s.

The case $k=2$ is straight-forward enough: given three homogeneous classes $ [u],[v],[w] $ such that $ [u]\smile[v] = [v]\smile[w] = 0$, there are (various) choices of cochains $ s , t $ with $ d s = u \cdot v $ and $ d t = v \cdot w $.  The Massey triple product is the set of sums $ [ u \cdot t \pm s \cdot w ] $, 
where the sign is chosen for cocyclicity.

## Properties

### Relation to Steenrod squares
 {#RelationToSteenrodSquares}

Let $\omega, \omega_1, \omega_2 \in H^\bullet(X,\mathbb{Z}/2)$ such that their triple Massey product exists. 
Then the [[cup product]] of $\omega$ with the triple Massey product is independent of the ambiguity in the Massey products and equals the cup product of $\omega_1$ with $\omega_2$ and with the [[Steenrod square]] of $\omega$ of degree $deg(\omega)-1$:

$$
  \omega \cup
  \left\langle
    \omega_1, \omega, \omega_2
  \right\rangle
  \;=\;
  \omega_1 \cup \omega_2 \cup Sq^{ deg(\omega) -1 }( \omega )
  \,.
$$

([Taylor 11, slide 10](#Taylor11), following [Milgram 68](#Milgram68))



### Relation to $A_\infty$-algebra

For $A$ a [[dg-algebra]], its [[chain homology]] $H_\bullet(A)$ inherits an [[A-infinity algebra]] structure by [[Kadeishvili's theorem]]. Then for every $n \in \mathbb{N}$ the $n$-ary $A_\infty$-product on elements $ (a_1, \cdots, a_n) \in H_\bullet(A)^n$ is given, up to a sign, by the Massey product $\langle a_1, \cdots, a_n\rangle$. 

For $n = 3$ this is due to ([Stasheff](#Stasheff)). For general $n$  this appears as ([LPWZ, theorem 3.1](#LPWZ)). 


## Related concepts

* [[cup product]]

* [[cohomology operation]]


## References
 {#References}

### General

* {#Kraines66} [[David Kraines]], _Massey higher products_,  Transactions of the American Mathematical Society Vol. 124, No. 3 (Sep., 1966), pp. 431-449 ([jstor](http://www.jstor.org/stable/1994385 ))

* Edward J. O'Neill, _On Massey products_,  Pacific J. Math. Volume 76, Number 1 (1978), 123-127. ([EUCLID](http://projecteuclid.org/euclid.pjm/1102807031))

* {#Kochmann96} [[Stanley Kochmann]], section 5.4 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Milgram68} [[R. James Milgram]], _Steenrod squares and higher Massey products_, Bol. Soc. Mat. Mexicana (2) 13 (1968), 32–57.MR0263074 ([web](https://www.researchgate.net/publication/268753745_Steenrod_squares_and_higher_Massey_products))

* {#Taylor11} [[Laurence Taylor]], _Massey Triple Products_, Princeton 2011 ([pdf](https://www3.nd.edu/~taylor/talks/2011-03-22-Princeton.pdf))



See also 

* Wikipedia, _[Massey product](https://en.wikipedia.org/wiki/Massey_product)_

### Relation to $A_\infty$-algebra
 {#ReferencesRelationToAInfinity}

The relation of Massey products to [[A-infinity algebra]] structures is in Chapter 12 of

* {#Stasheff} [[Jim Stasheff]], _H-spaces from a homotopy point of view_
 

for $n = 3$, and for general $n$ in Theorem 3.1 and Corollary A.5 of 

* {#LPWZ} D.-M. Lu, J. H. Palmieri, Q.-S. Wu, J. J. Zhang, _$A_\infty$-structures in Ext algebras_, J. Pure Appl. Alg. 213 (2009), 2017--2037 (Theorem 3.1 and Corollary A.5) ([arXiv:math/0606144](http://arxiv.org/abs/math/0606144))
 

as well as from item 1.4 on in 

* [[Bruno Vallette]], _Algebra+Homotopy=Operad_ ([arXiv:1202.3245](http://arxiv.org/abs/1202.3245))

and sections 9.4.10 to 9.4.12 of 

* {#ValetteLoday} [[Bruno Vallette]], [[Jean-Louis Loday]], _Algebraic Operads_ ([pdf](http://math.unice.fr/~brunov/Operads.pdf))
 

Notice that the definition of Massey product on top of p.282 of [Vallette-Loday](#ValetteLoday), $\langle x,y,z\rangle$ depends on choices of $a,b$ which don't appear in the notation. Then lemma 9.4.11 talks about a particular choice of $a,b$ which is made in the body of the proof. The actual statement of the lemma only can be deduced after reading the proof. It then says that for these particular choices of a,b the said equality holds. (See [this MO discussion](http://mathoverflow.net/questions/92315/massey-products-vs-a-infty-structures)).

### In ordinary differential cohomology
 {#ReferencesInOrdinaryDifferentialCohomology}

Massey products in [[ordinary differential cohomology]]/[[Deligne cohomology]] are discussed in 

* Wenger, _Massey products in Deligne cohomology_.

* C. Deninger, _Higher order operations in Deligne cohomology_, Inventiones
Math. 122 N1 (1995).

* Alexander Schwarzhaupt, _Massey products in Deligne-Beilinson cohomology_ ([web](http://www.researchgate.net/publication/29799379_Massey_products_in_Deligne-Beilinson_cohomology), [[SchwarzhauptMasseyDeligne.pdf:file]]).

* [[Daniel Grady]], [[Hisham Sati]], _Massey products in differential cohomology via stacks_, J. Homotopy Relat. Struct. 13 (2017) 169-223 ([arXiv:1510.06366](http://arxiv.org/abs/1510.06366), [doi:10.1007/s40062-017-0178-y](https://doi.org/10.1007/s40062-017-0178-y)).


[[!redirects Massey products]]