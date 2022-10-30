# Contents 
* table of contents 
{:toc} 

## Idea 

A __prime ideal theorem__ is a theorem stating that every [[proper ideal]] is contained in some [[prime ideal]].  A prime ideal theorem is typically equivalent to the [[ultrafilter principle]] (UF), a weak form of the [[axiom of choice]] (AC).

We say 'a' prime ideal theorem (PIT) instead of 'the' prime ideal theorem, since we have not said what the ideals are in. We list some representative examples of prime ideal theorems, all of which are equivalent to (UF) in ZF or even in BZ (bounded Zermelo set theory): 

*  The PIT for (commutative) [[rings]].

*  The PIT for (bounded) [[distributive lattices]].

*  The PIT for [[Boolean algebras]].

*  The PIT for [[rigs]], which subsumes all of the above. In fact one can generalize quite a bit further, as we indicate below when we discuss prime element theorems. 

The usual way to prove a prime ideal theorem is with the help of [[Zorn's Lemma]], unless one is specifically trying to use something weaker like UF (as we do in this article). In fact [[Zorn's lemma]] can be used to prove a [[maximal ideal theorem]], which is stronger: in all the usual examples maximal ideals are prime so that a [[prime ideal theorem]] becomes a corollary. 


## A ladder of prime ideal theorems 

Prime ideal theorems may be arranged as a sequence of results and techniques that gradually increase in sophistication; we sketch one possible development here, filling in details in the remainder of the article. 

A first easy wave of results concerns the equivalence between the Boolean PIT (or BPIT) and UF. While these are easy, the BPIT is a theoretical underpinning of fundamental techniques such as the [[compactness theorem]] for [[first-order logic]], which leads to the next rung on the ladder. 

The next step derives the PIT for distributive lattices as a simple application of the compactness theorem and other model-theoretic techniques. In effect we write down a simple [[propositional theory]] where a [[model]] is tantamount to a prime ideal in a given distributive lattice. Part of the work involves checking finite satisfiability of the theory, where we may invoke a simple [[Stone duality]] between finite distributive lattices and finite posets. 

With the PIT for distributive lattices in hand, we prove a key result due to Banaschewski, which may be summarized roughly as saying that a (nontrivial) compact frame admits a prime element. This is an early result in [[Stone Spaces]], related to the spatiality of compact regular locales. 

This last result is a key of entry into prime ideal theorems of quite general type. The general idea is that ideals in a monoid (now in suitably nice monoidal categories) tend to form compact [[quantales]], whose prime elements correspond to prime ideals. One then invokes a simple construction which associates to each compact quantale a quotient compact frame, in such a way that the existence of a prime element in the quantale is reduced to existence of a prime element in the compact frame. As promised, this gives prime ideal theorems of fairly general type (call it "GPIT"). 

As suggested earlier, any one of these prime ideal theorems implies the BPIT as a special case, and so we come full circle: 

$$UF \Rightarrow BPIT \Rightarrow PIT(DistLat) \Rightarrow GPIT \Rightarrow BPIT \Rightarrow UF.$$ 

Offshoots of this development include stronger forms of a PIT in which a prime ideal is produced that does not intersect a given multiplicatively closed subset $\mathfrak{m}$. However, these can often be reduced to an ordinary PIT, by first localizing or inverting the elements in $\mathfrak{m}$, and then applying a PIT to the localization. 

We now turn to details. 


### Boolean PIT and the ultrafilter principle 

The Boolean prime ideal theorem or BPIT is equivalent to the [[ultrafilter principle]] UF. 

The reasoning may be summarized as follows: the ultrafilter principle implies the [[Tychonoff theorem]] for compact Hausdorff spaces; see this [Remark](/nlab/show/Tychonoff+theorem#TyCH) and the argument immediately preceding it. The Tychonoff theorem for compact Hausdorff spaces in turn implies that every Boolean ring $B$ has a maximal (and therefore prime) ideal; see [here](/nlab/show/Tychonoff+theorem#nonempty). Consequently, for any ideal $I$ of a Boolean algebra $B$, the quotient Boolean ring $B/I$ has a prime ideal $P$, and the pullback $q^{-1}(P) \subseteq B$ of the quotient map $q: B \to B/I$ produces a prime ideal in $B$ which contains a given ideal $I$, thus proving the BPIT from UF. 

(In passing, one may note that prime ideals in Boolean algebras (or Boolean rings) $B$ are the same as maximal ideals. For, the corresponding Boolean quotient ring is an integral domain only if it is the field $\mathbb{Z}/(2)$, since idempotency of elements yields $e(1-e) = 0$ and then $e = 0$ or $e = 1$ assuming no zero divisors.)  

Finally, maximal ideals are complementary to ultrafilters (see [here](/nlab/show/Boolean+algebra#aremax)). So UF, which says that every filter in $B = P X$ 
is contained in an ultrafilter, translates into a special case of the BPIT: every ideal of $P X$ (consisting of negations of elements of a corresponding filter) is contained in a prime/maximal ideal. This brings us full circle: BPIT implies UF implies Tychonoff(CH) implies BPIT. 


### BPIT implies prime ideal theorem for distributive lattices 

Now let us prove that the Tychonoff theorem for CH spaces implies the PIT for distributive lattices $D$: that any proper ideal $I$ of $D$ is contained in a prime ideal of $D$. By passing to the quotient lattice $D/I$, it suffices to show that $D/I$ has a prime ideal $P$, since the inverse image $\phi^{-1}(P)$ of a prime ideal $P$ along the quotient map $\phi: D \to D/I$ is again prime. 

The method we use here is a somewhat pedestrian application of the [[compactness theorem]] and the circle of methods surrounding it. 

+-- {: .num_theorem} 
###### Theorem 
(UF) 
Any nontrivial distributive lattice $D$ has a prime ideal $P$. 
=-- 

To prove this, we write down a propositional theory of "a prime ideal $P$ of $D$" (and consider its [[Lindenbaum algebra]]). Form a free Boolean algebra $Bool(U D)$ freely generated by the underlying set $U D$ of $D$. So each $x \in U D$ corresponds to a generator $P_x \in Bool(U D)$, which we will think of as standing for a proposition $P_x = $ "$x \in P$". The conditions that enforce "$P$ is a prime ideal of $D$" are the axioms of our theory: 

* ($P$ is closed under finite joins) $P_0$, $P_a \wedge P_b \Rightarrow P_{a \vee b}$. 

* ($P$ is downward closed) For each $b \in U D$, $P_a \Rightarrow P_{a \wedge b}$. 

* ($P$ is proper) $\neg P_1$. 

* (primality condition) $P_{a \wedge b} \Rightarrow (P_a \vee P_b)$. 

These axioms (certain elements of $Bool(U D)$) then generate a [[filter]] $\mathcal{F}$. As soon as we know $\mathcal{F}$ is proper ("finite satisfiability of the theory"), the BPIT ensures that $F$ is contained in an ultrafilter $\mathcal{U}$, corresponding to a [[model]] or a Boolean ring homomorphism $Bool(U D)/\mathcal{F} \to \mathbf{2}$ out of the Lindenbaum algebra. For that model, the collection $\{a \in D: P_a \in \mathcal{U}\}$ then forms a prime ideal $P$ of $D$, as desired. So: 

+-- {: .proof} 
###### Proof 
(The filter $\mathcal{F}$ is proper.) To see that the filter generated by finitely many axioms does not contain $0 \in Bool(U D)$, consider the sublattice of $D$ generated by the finitely many elements $a$ named in atomic subformulas of such axioms. A finitely generated distributive lattice is finite (indeed, by [[Stone duality]], the free distributive lattice on a finite number $n$ or elements is isomorphic to the poset of downward-closed subsets of the poset $\mathbf{2}^n$). So all we need to do is show that any nontrivial finite lattice $L$ has a prime ideal. This also follows from Stone duality: each lattice homomorphism $L \to \mathbf{2}$ corresponds to a point of the Stone dual $S$, and if $L$ is nontrivial then $S$ must be inhabited by a point $x$, so lattice homomorphisms $L \to \mathbf{2}$ exist and the kernel of such is a maximal and therefore prime ideal. 
=-- 

### Banaschewski's lemma 

During the 1980's, [Banaschewski](#Ban) discovered the following result (a breakthrough in the study of prime ideal theorems, according to [Marcel Ern&#233;](http://www.researchgate.net/publication/242573716_Prime_Ideal_Theorems_and_systems_of_finite_character)). We state and prove the lemma for now, and show how it is used in later sections. 

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
First we observe that a coproduct of nontrivial bounded distributive lattices $\{X_i\}_{i \in I}$ (in the category of bounded distributive lattices) is also nontrivial. Again this is a kind of finite satisfiability result: if such a coproduct were trivial, i.e., if $0 = 1$ were satisfied in the coproduct (constructed syntactically as the free distributive lattice $F = F(\sum_i X_i)$ modulo equations that identify finite meets and joins in each $X_i$ with formal meets and joins in $F$), then $0 = 1$ would be derivable from finitely many equations involving finitely many elements $x_i$ in the $X_i$, and hence $0 = 1$ would be derivable in a finite coproduct of finite bounded nontrivial distributive lattices generated by these elements. This cannot happen, by considering their [[Stone duality]] with finite [[posets]] and products thereof: finite products of [[inhabited set|inhabited]] finite posets are also inhabited. 

With that in hand, consider the [[coproduct]] $M = \sum_{a \in L} \uparrow a$ of all the principal filters of $L$, taken in the category of bounded distributive lattices; let $i_a: \uparrow a \to M$ denote the coproduct inclusion. $M$ has a prime ideal $P$ by the PIT for distributive lattices; the pullback $P_a \coloneqq i_a^{-1}(P)$ is a prime ideal of $\uparrow a$. Of course $P_a \subseteq L \setminus \{1\}$ by properness of prime ideals. 

Put $S = L \setminus \{1\}$. This is a [[dcpo]] by completeness of $L$ and compactness of $1$; since proper ideals $I \subseteq S$ are directed subsets, we see that $S$ admits a sup $\sigma(a) \coloneqq \bigvee P_a$ for each $a \in S$. We have $a \leq \sigma(a)$ for all $a \in S$. By the Bourbaki-Witt fixed point theorem, the inflationary operator $\sigma: S \to S$ has a fixed point, say $c: c = \sigma(c)$. For that $c$, note that $P_c \subseteq \uparrow c$ is just $\{c\}$. 

So $\{c\}$ is a prime ideal in $\uparrow c$. By meet-irreducibility, this means $c$ is a prime element in $L$. 
=-- 

+-- {: .num_remark} 
###### Remark 
When the statement is about compact frames, it can be rephrased as saying that every nontrivial compact locale has at least one point; compare [[Stone Spaces]], Lemma 1.9. 
=-- 

### Prime elements in quantales of ideals 

To show how Banaschewski's lemma is applied, we consider for example the prime ideal theorem for (possibly noncommutative) rings. We follow the common convention that rings have units. 

Let $R$ be a ring, and let $Idl(R)$ be the sup-lattice of two-sided ideals of $R$. Under multiplication of ideals $A \cdot B$, we obtain a [[quantale]] structure on $Idl(R)$ whose multiplicative unit is the top element $R$. In general we will call a quantale *affine* if its unit is the top element. 

The top element $1$ of $Idl(R)$ is also a *[[compact element]]*. In general, and generalizing a definition from the theory of [[frames]]/[[locales]], we will say that a quantale is *compact* if its top element is a compact element. 

Finally, in a quantale $Q$, we say an element $p \in Q$ is *prime* if for all $a, b \in Q$ we have $a b \leq p$ implies $a \leq p$ or $b \leq p$. Prime elements in $Idl(R)$ are precisely prime ideals of $R$. 

+-- {: .num_theorem} 
###### Theorem 
(ZF + UF) Every nontrivial compact affine quantale has a prime element. 
=-- 

The strategy is to reduce the claim to an application of Banaschewski's lemma. 

We begin by introducing an equivalence relation on $Q$: say $a \equiv b$ if $(\forall_c)\; 1 = a \vee c \Leftrightarrow 1 = b \vee c$. 

+-- {: .num_lemma} 
###### Lemma 
The relation $\equiv$ is a quantale congruence. 
=-- 

+-- {: .proof} 
###### Proof 
First we show that $\equiv$ respects the quantale multiplication $\cdot$. Suppose $a \equiv b$ and $x \equiv y$. So for any $c$, if $1 \leq a x \vee c$, it follows that $1 \leq a \vee c$ and $1 \leq x \vee c$, whence $1 \leq b \vee c$ and $1 \leq y \vee c$. Then 

$$1 \leq b \vee c = (b \cdot 1) \vee c = b(y \vee c) \vee c = b y \vee b c \vee c = b y \vee c$$ 

and similarly $1 = b y \vee c$ implies $1 = a x \vee c$. So $a x \equiv b y$. 

Now we show that $\equiv$ respects joins, i.e., if $x_i \equiv y_i$ for all $i \in I$, then $\bigvee_i x_i \equiv \bigvee_i y_i$. Suppose $1 = c \vee \bigvee_i x_i$. Since $Q$ is compact, there is a finite set of the $x_i$, say $x_1, \ldots, x_n$, such that $1 = c \vee x_1 \vee \ldots \vee x_n$. From $x_n \equiv y_n$ and $1 = (c \vee x_1 \vee \ldots \vee x_{n-1}) \vee x_n$, we derive 

$$1 = (c \vee x_1 \vee \ldots \vee x_{n-1}) \vee y_n = (y_n \vee c) \vee x_1 \vee \ldots \vee x_{n-1}$$ 

and we proceed by induction to show $1 = c \vee y_1 \vee \ldots \vee y_n$, which implies $1 \leq c \vee \bigvee_{i \in I} y_i$. Similarly, $1 = c \vee \bigvee_i y_i$ implies $1 = c \vee \bigvee_i x_i$, and so we are done. 
=-- 

+-- {: .num_prop} 
###### Proposition 
The quotient quantale $Q/\equiv$ is a nontrivial compact frame. 
=-- 

+-- {: .proof} 
###### Proof 
Clearly $1 \leq x x \vee c$ implies $1 \leq x x \vee c \leq x \vee c$. But also if $1 \leq x \vee c$, then 

$$1 \leq x \vee c = x \cdot 1 \vee c = x\cdot (x \vee c) \vee c = x x \vee x c \vee c = x x \vee c$$ 

and thus $x x \equiv x$ for all $x$. Being an idempotent affine quantale, $Q/\equiv$ is a frame. 

We have $\neg (0 \equiv 1)$ since ($0 \vee c = 1$ iff $1 \vee c = 1$) fails for $c = 0$, under the assumption $Q$ is nontrivial. So $Q/\equiv$ is nontrivial. 

To show $Q/\equiv$ is compact, suppose $\{x_i\}_{i \in I}$ is a family in $Q$ such that $\bigvee_i x_i \equiv 1$, in other words such that $c \vee \bigvee_i x_i = 1$ for all $c \in Q$. Setting $c = 0$ and applying compactness of $Q$, there is a finite subfamily $F$ such that $\bigvee_{i \in F} x_i = 1$, and then $\bigvee_{i \in F} x_i \equiv 1$ which proves compactness of $Q/\equiv$. 
=-- 

+-- {: .num_prop} 
###### Proposition 
Denote the $\equiv$-class of $p \in Q$ by $[p]$, and suppose $[p]$ is a prime element of $Q/\equiv$. Then $p$ is a prime element of $Q$. 
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