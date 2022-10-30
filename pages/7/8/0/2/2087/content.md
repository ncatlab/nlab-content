# Contents 
* table of contents 
{:toc} 

## Idea 

A __prime ideal theorem__ is a theorem stating that every [[proper ideal]] is contained in some [[prime ideal]].  A prime ideal theorem is typically equivalent to the [[ultrafilter principle]] (UF), a weak form of the [[axiom of choice]] (AC).

We say 'a' prime ideal theorem (PIT) instead of 'the' prime ideal theorem, since we have not said what the ideals are in. We list some representative examples of prime ideal theorems, all of which are equivalent to (UF) in ZF or even in BZ (bounded Zermelo set theory): 

*  The PIT for (commutative) [[rings]].

*  The PIT for [[distributive lattices]].

*  The PIT for [[Boolean algebras]].

*  The PIT for [[rigs]], which subsumes all of the above. In fact one can generalize quite a bit further, as we indicate below when we discuss prime element theorems. 

The usual way to prove a prime ideal theorem is with the help of [[Zorn's Lemma]], unless one is specifically trying to use something weaker like UF (as we do in this article). In fact [[Zorn's lemma]] can be used to prove a [[maximal ideal theorem]], which is stronger: in all the usual examples maximal ideals are prime so that a [[prime ideal theorem]] becomes a corollary. 


## A ladder of prime ideal theorems 

Prime ideal theorems may be arranged as a sequence of results and techniques that gradually increase in sophistication; we sketch one possible development here, filling in details in the remainder of the article. 

A first easy (almost tautological) result is the equivalence between the Boolean PIT (or BPIT) and UF. While this is easy, the BPIT is a theoretical underpinning of fundamental techniques such as the [[compactness theorem]] for [[first-order logic]], which leads to the next rung on the ladder. 

The next step derives the PIT for distributive lattices as a simple application of the compactness theorem and other model-theoretic techniques. In effect we write down a simple [[propositional theory]] where a [[model]] is tantamount to a prime ideal in a given distributive lattice. Part of the work involves checking finite satisfiability of the theory, where we may invoke a simple [[Stone duality]] between finite distributive lattices and finite posets. 

With the PIT for distributive lattices in hand, we prove a key result due to Banaschewski, which may be summarized roughly as saying that a (nontrivial) compact frame admits a prime element. This is an early result in [[Stone Spaces]], related to the spatiality of compact regular locales. 

This last result is a key of entry into prime ideal theorems of quite general type. The general idea is that ideals in a monoid (now in suitably nice monoidal categories) tend to form compact [[quantales]], whose prime elements correspond to prime ideals. One then invokes a simple construction which associates to each compact quantale a quotient compact frame, in such a way that the existence of a prime element in the quantale is reduced to existence of a prime element in the compact frame. As promised, this gives prime ideal theorems of fairly general type (call it "GPIT"). 

As suggested earlier, any one of these prime ideal theorems implies the BPIT as a special case, and so we come full circle: 

$$UF \Rightarrow BPIT \Rightarrow PIT(DistLat) \Rightarrow GPIT \Rightarrow BPIT \Rightarrow UF.$$ 

Offshoots of this development include stronger forms of a PIT in which a prime ideal is produced that does not intersect a given multiplicatively closed subset $\mathfrak{m}$. However, these can often be reduced to an ordinary PIT, by first localizing or inverting the elements in $\mathfrak{m}$, and then applying a PIT to the localization. 

We now turn to details. 


### Boolean PIT and the ultrafilter principle 

First, prime ideals in Boolean algebras (or Boolean rings) $B$ are the same as maximal ideals. For, the corresponding Boolean quotient ring is an integral domain only if it is the field $\mathbb{Z}/(2)$, since idempotency of elements yields $e(1-e) = 0$ and then $e = 0$ or $e = 1$ assuming no zero divisors. 

Second, maximal ideals are complementary to ultrafilters (see [here](/nlab/show/Boolean+algebra#aremax)). So UF, which says that every filter in $B = P X$ 
is contained in an ultrafilter, translates into a special case of the BPIT: every ideal of $P X$ (consisting of negations of elements of a corresponding filter) is contained in a prime/maximal ideal. 

That the Tychonoff theorem for compact Hausdorff spaces implies BPIT was proven [here](/nlab/show/Tychonoff+theorem#nonempty), noting that to prove that every proper ideal $I$ of $B$ is contained in a prime ideal, it suffices to find a prime ideal (or ultrafilter) of $B/I$, pulling it back along the quotient $B \to B/I$ to a prime ideal of $B$. This brings us full circle: BPIT implies UF implies Tychonoff(CH) implies BPIT. 

### BPIT implies prime ideal theorem for commutative rings

Now let us prove that the Tychonoff theorem for CH spaces implies the PIT for commutative rings: that any proper ideal $I$ of $R$ is contained in a prime ideal of $R$. By passing to the quotient rig $R/I$, it suffices to show that $R/I$ has a prime ideal $P$, since the inverse image $\phi^{-1}(P)$ of a prime ideal $P$ along the quotient map $\phi: R \to R/I$ is again prime. 

The method we use here is a somewhat pedestrian application of the [[compactness theorem]] and the circle of methods surrounding it. 

+-- {: .num_theorem} 
###### Theorem 
(UF) 
Any commutative ring $R$ has a prime ideal $P$. 
=-- 

To prove this, we'll write down a propositional theory of "a prime ideal $P$ of $R$" (or, just as well, consider its [[Lindenbaum algebra]]). Form a free Boolean algebra $Bool(U R)$ freely generated by the underlying set of $R$. So each $x \in U R$ corresponds to a generator $P_x \in Bool(U R)$, which we will think of as standing for a proposition $P_x = $ "$x \in P$". The conditions that enforce "$P$ is a prime ideal" are then the axioms of our theory: 

* ($P$ is closed under finite sums) $P_0$, $P_a \wedge P_b \Rightarrow P_{a+b}$. 

* ($P$ is closed under multiplication by scalars) For each $b \in U R$, $P_a \Rightarrow P_{a b}, P_a \Rightarrow P_{b a}$. 

* ($P$ is proper) $\neg P_1$. 

* (primality condition) $P_{a b} \Rightarrow (P_a \vee P_b)$. 

These axioms (certain elements of $Bool(U R)$) then generate a [[filter]] $F$. As soon as we know $F$ is proper ("finite satisfiability of the theory"), the BPIT ensures that $F$ is contained in an ultrafilter $\mathcal{U}$, corresponding to a [[model]] or a Boolean ring homomorphism $Bool(U R)/F \to \mathbf{2}$ out of the Lindenbaum algebra. For that model, the collection $\{a \in R: P_a \in \mathcal{U}\}$ then forms a prime ideal $P$ of $R$, as desired. So: 

+-- {: .proof} 
###### Proof 
(That the theory is finitely satisfiable.) This follows if we show that any finitely generated commutative ring $R$ has a prime ideal. In fact we will do more and show that any provably [[countable set|countable]] commutative ring $R$ with unit admits a prime ideal. For this we use WKL (weak K&#246;nig's lemma), in the form given [here](/nlab/show/compactness+theorem#weak). 

The case where $R$ is finite is left to the reader. So WLOG, assume that we are given an enumeration $a_0, a_1, a_2, \ldots$ of the elements of $R$. The strategy is to build an infinite but finitely branching tree with nodes labeled by suitable ideals of $R$, in such a way that the union of subsets that label the nodes of an infinite branch (which exists by WKL) is manifestly a (proper) prime ideal. 

Let $2^{\lt \omega}$ be the maximal infinite planar binary tree, i.e., the set of finite 0-1 sequences or words. Each word $\sigma \in 2^{\lt \omega}$ may be lengthened by 1 in two ways, denoted $\sigma 0$ and $\sigma 1$. Our tree $T$ will be a subtree of $2^{\lt \omega}$, i.e., $T$ is a subset of words closed under taking prefixes. The set of words of length $k$ in $T$ is denoted $T_k$, so $T$ is the disjoint union of the $T_k$. 

For $\sigma \in T$, we denote its ideal-label by $P_\sigma$. We define $T_k$ and the $P_\sigma$ for $\sigma \in T_k$ by recursion. $T_0$ consists of just the empty word $e$, and we set $P_e = \{0\}$. Now suppose given $T_{k-1}$ and $P_\sigma$ for all $\sigma \in T_{k-1}$. We define $T_k$ and the ideals $P_\tau: \tau\in T_k$ by distinguishing two cases; accordingly we write $k = 2m + n$ where $n \in \{0, 1\}$ where $m$ codes a pair of natural numbers $(i, j)$ by the usual trick: $m = \binom{i+j+1}{2} + j$. 

1. If $n = 0$, then for every $\sigma \in T_{k-1}$ such that $a_i a_j$ belongs to $P_\sigma$, put $\sigma 0, \sigma 1$ in $T_k$, and put $P_{\sigma 0} = P_{\sigma} + \langle a_i \rangle$, and put $P_{\sigma 1} = P_{\sigma} + \langle a_j \rangle$. For any other $\sigma \in T_{k-1}$, put $\sigma 0$ in $T_k$, and put $P_{\sigma 0} = P_{\sigma}$. 

1. If $n = 1$, then put $\sigma 0$ in $T_k$ for each $\sigma \in T_{k-1}$ such that $1 \notin P_\sigma$, and put $P_{\sigma 0} = P_\sigma$. If $1 \in P_\sigma$, then put neither $\sigma 0$ nor $\sigma 1$ in $T_k$. 

To apply WKL, we check that $T$ is an infinite tree: we prove by induction that for every $k$ there exists $\sigma \in T_k$ such that $1 \notin P_\sigma$. This is trivial if $k = 0$. If $1 \notin P_\sigma$ for $\sigma \in T_{k-1}$ and we are in case 2 ($k = 1 \mod 2$), then clearly for $\sigma 0 \in T_k$ we have $P_{\sigma 0} = P_\sigma$ and so $1 \notin P_{\sigma 0}$. Now suppose $1 \notin P_\sigma$ for $\sigma \in T_{k-1}$ and we are in case 1. If $1 \in P_\sigma + \langle a_i \rangle$ and $1 \in P_\sigma + \langle a_j \rangle$, i.e., if $1 = p + r a_i$ and $1 = q + s a_j$ for $p, q \in P_\sigma$, then $1 = (p q + p s a_j + q r a_i) + r s a_i a_j$ clearly belongs to $P_\sigma + \langle a_i a_j \rangle = P_\sigma$, a contradiction. So either $1 \notin P_{\sigma 0}$ or $1 \notin P_{\sigma 1}$, and the induction goes through.  

By WKL, there is an infinite branch $b$ through $T$, and we put $P = \bigcup_{\sigma \in b} P_\sigma$. Clearly $1 \notin P$ since otherwise if $1 \in P_\sigma$ for $\sigma \in b$, then we can go no further up the branch by case 2. So $P$ is a proper ideal. It is a prime ideal by case 1. 
=-- 

### PIT for rings and Banaschewski's lemma 

Deducing PIT for commutative rings from UF goes back a long ways (work of Dana Scott and Alfred Tarski in the 1950's), but deducing the PIT for [[rings]] turned out to be harder. A particularly efficient method was provided largely by [Banaschewski](#Ban), who discovered the following result (a breakthrough in the study of prime ideal theorems, according to [Marcel Ern&#233;](http://www.researchgate.net/publication/242573716_Prime_Ideal_Theorems_and_systems_of_finite_character)). 

+-- {: .num_theorem} 
###### Theorem 
**(Banaschewski's lemma)** 
Every nontrivial distributive complete lattice $L$ whose top element $1$ is [[compact element|compact]], e.g., a compact [[frame]], has a prime element. 
=-- 

+-- {: .num_remark} 
###### Remarks 
Here "nontrivial" means $0 \neq 1$: distinct top and bottom elements. This is needed because prime ideals are required to be proper (see [[too simple to be simple]]). An element $p$ is *prime* if the principal ideal it generates is prime, i.e., if $a \wedge b \leq p$ implies $a \leq p$ or $b \leq p$. In a distributive lattice, this is the same as saying $p = a \wedge b$ implies $p = a$ or $p = b$ (meet-irreducibility). 
=-- 

+-- {: .proof} 
###### Proof 
First we observe that a coproduct of nontrivial bounded distributive lattices $\{X_i\}_{i \in I}$ (in the category of bounded distributive lattices) is also nontrivial. This is a finite satisfiability result: if such a coproduct were trivial, i.e., if $0 = 1$ were satisfied in the coproduct (constructed syntactically as the free distributive lattice $F = F(\sum_i X_i)$ modulo equations that identify finite meets and joins in each $X_i$ with formal meets and joins in $F$), then $0 = 1$ would be derivable from finitely many equations involving finitely many elements $x_i$ in the $X_i$, and hence $0 = 1$ would be derivable in a finite coproduct of finite bounded nontrivial distributive lattices generated by these elements. This cannot happen, by considering their [[Stone duality]] with finite [[posets]] and products thereof: finite products of [[inhabited set|inhabited]] finite posets are also inhabited. 

With that in hand, consider the [[coproduct]] $M = \sum_{a \in L} \uparrow a$ of all the principal filters of $L$, taken in the category of bounded distributive lattices; let $i_a: \uparrow a \to M$ denote the coproduct inclusion. $M$ has a prime ideal $P$ by the PIT for distributive lattices; the pullback $P_a \coloneqq i_a^{-1}(P)$ is a prime ideal of $\uparrow a$. Of course $P_a \subseteq L \setminus \{1\}$ by properness of prime ideals. 

Put $S = L \setminus \{1\}$. This is a [[dcpo]] by completeness of $L$ and compactness of $1$; since proper ideals $I \subseteq S$ are directed subsets, we see that $S$ admits a sup $\sigma(a) \coloneqq \bigvee P_a$ for each $a \in S$. We have $a \leq \sigma(a)$ for all $a \in S$. By the Bourbaki-Witt fixed point theorem, the inflationary operator $\sigma: S \to S$ has a fixed point, say $c: c = \sigma(c)$. For that $c$, note that $P_c \subseteq \uparrow c$ is just $\{c\}$. 

So $\{c\}$ is a prime ideal in $\uparrow c$. By meet-irreducibility, this means $c$ is a prime element in $L$. 
=-- 

+-- {: .num_remark} 
###### Remark 
When the statement is about compact frames, it can be rephrased as saying that every nontrivial compact locale has at least one point; compare [[Stone Spaces]], Lemma 1.9. 
=-- 

+-- {: .num_theorem} 
###### Theorem 
**(PIT for rings)** 
Every unital ring $R$ has a prime ideal under ZF + (UF). 
=-- 

We sketch a proof of this due to Banaschewski. 

+-- {: .proof} 
###### Proof 
Let $k: Ideal(R) \to Ideal(R)$ be the [[closure operator]] that takes an ideal $I$ to its Jacobson radical (i.e., the intersection of all maximal left ideals containing $I$). This operator preserves directed joins and in addition satisfies the following properties: 

* $k(I \cap J) = k(I J) = k(I) \cap k(J)$, 

* $k(J) = 1$ implies $J = 1$. 

The lattice of ideals forms a [[quantale]] whose multiplication is multiplication of ideals $I J$; accordingly, if $Jac(R)$ denotes the lattice of fixed points of $k$, then the first property implies that $Jac(R)$ is a [[locale]]. Moreover $1$ is a compact element of the quantale $Ideal(R)$, hence is a compact element of the locale $Jac(R)$ by the second property. Thus Banaschewski's lemma implies that $Jac(R)$ has a prime element. Such a prime element is a prime ideal equal to its Jacobson radical, by [Banaschewski-Harting](#BH). 
=-- 




## References 

* [[Bernhard Banaschewski]] and Roswitha Harting, _Lattice Aspects of Radical Ideals and Choice Principles_, Proc. London Math. Soc. s3-50 (3) (1985), 385-404. ([web](http://plms.oxfordjournals.org/content/s3-50/3/385.extract)) 
 {#BH}

* Bernhard Banaschewski, _Prime Elements from Prime Ideals_, Order 2 (1985), 211-213. ([Springer link](http://link.springer.com/article/10.1007%2FBF00334858))
 {#Ban} 