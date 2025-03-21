
# Contents
* table of contents 
{: toc}

## Idea 

In [[number theory]], the quadratic reciprocity law determines a precise relationship between the truth of $p R q$ and the truth of $q R p$, where $p R q$ is this [[binary relation]] on odd [[prime numbers]]: "$p$ is a square [[modular arithmetic|modulo]] $q$". 

The law of quadratic reciprocity is a celebrated result due to [[Gauss]]; the ideas required to prove it helped to inaugurate modern [[number theory]]. It is today largely considered within the context of [[class field theory]], involving how [[prime number|primes]] decompose in [[Galois extension|abelian extensions]] of [[number fields]]. 


## Statement 

For $p \geq 1$ an odd [[prime number]], and for any [[integer]] $a$, define the __Legendre symbol__ (or _quadratic reciprocity symbol_) $\left(\frac{a}{p}\right)$ to be the unique element in $\{-1, 0, 1\}$ for which 

$$
\left(\frac{a}{p}\right) \equiv a^{\frac{p-1}{2}} \; mod \; p
$$ 

Notice that the Legendre symbol defines a surjective [[homomorphism]] on a [[cyclic group]] 

$$(\mathbb{Z}/p)^\ast \cong C_{p-1} \to \{-1, 1\}$$ 

whose [[kernel]] is the set of squares in the multiplicative group $(\mathbb{Z}/p)^\ast$, so that $\left(\frac{a}{p}\right) = 1$ means $a$ is a square modulo $p$, and $\left(\frac{a}{p}\right) = -1$ means $a$ is a non-square modulo $p$. 

+-- {: .num_theorem} 
###### Theorem (Quadratic Reciprocity) 
For $p$, $q$ distinct odd primes, 

$$\left(\frac{p}{q}\right) \left(\frac{q}{p}\right) = (-1)^{\frac{p-1}{2}\frac{q-1}{2}}.$$

$$\,$$ 

$$\left(\frac{2}{p}\right) = (-1)^{\frac{p^2-1}{8}}$$ 

i.e., $2$ is a square modulo $p$ if and only if $p \equiv \pm 1 \; mod \; 8$. 
=-- 

The case for odd primes $p$, $q$ can be restated as: 

* if $p,q$ are odd and $p \equiv 1 \; mod \; 4$, then $\left(\frac{p}{q}\right) = \left(\frac{q}{p}\right)$

* if $p,q \equiv 3 \; mod \; 4$ then  $\left(\frac{p}{q}\right) = -\left(\frac{q}{p}\right)$

The law of quadratic reciprocity was first fully proven by [Gauss](#Gauss), although special cases were proven by [[Fermat]] (who effectively realized when $-1$ was a square modulo $p$ based on his [[two squares theorem]] -- well before Legendre introduced his eponymous symbol), and [[Euler]] (who proved the case for $q = 2$). 

None of these early authors were in full possession of modern notations such as the congruence symbol or the Legendre symbol, which greatly economize the amount of thought needed to prove this theorem. Recognition of quadratic reciprocity was likely rooted in empirical observations, for example the study of periods of expansions of $1/q$ in base $p$ (source?). 


## Sample classroom application 

Consider the problem of computing the length of the period of $1/65537$ in its decimal expansion. This period is the same as the least positive exponent $n$ such that $10^n \equiv 1 \; mod \; 65537$, and is a divisor of $65536$ (thus, a power of $2$). Indeed, $65537$ is a [[Fermat prime]]: $2^{2^4} + 1$. 

The period is a proper divisor of $65536$ if and only if $10$ is a square modulo $p = 65537$, leading one to contemplate 

$$\left(\frac{10}{p}\right) = \left(\frac{2}{p}\right) \left(\frac{5}{p}\right)$$ 

where the first factor is pretty clearly $1$ (already $2^{32} \equiv 1 \; mod \; p$, so certainly $2^{\frac{p-1}{2}} \equiv 1 \; mod \; p$). The other factor is 

$$\left(\frac{5}{p}\right) = \left(\frac{p}{5}\right) = \left(\frac{2}{5}\right) = -1$$ 

and we therefore conclude $10$ is a non-square modulo $65537$, or in other words that the length of the period of $1/65537$ is $65536$. 


## Proofs 

There are today several hundred published proofs of the quadratic reciprocity laws; it is rightly regarded as a capstone result in undergraduate introductions to number theory. We give two proofs here. 


### Proof via Gauss sums 

This proof, following [Lang](#Lang) (pp. 76--78), is middling in sophistication but at least indicates the relevance of [[cyclotomic extension]]s of the rationals $\mathbb{Q}$ and [[quadratic extension]]s therein. Let $p$ be a fixed odd prime, and let $\zeta$ be a primitive $p^{th}$ [[root of unity]]. Using the Legendre symbol, we introduce a particular [[character]] sum called a **[[Gauss sum]]**, 

$$S \coloneqq \sum_a \left(\frac{a}{p}\right) \zeta^a,$$

where the sum is over non-zero elements $a$ of $\mathbb{Z}/p$. 

+-- {: .num_lemma}
###### Lemma 
$S^2 = \left(\frac{-1}{p}\right) p$. 
=-- 

+-- {: .proof} 
###### Proof 
We have $S^2 = \sum_{a, b} \left(\frac{a b}{p}\right) \zeta^{a + b}$. For any fixed non-zero $a$, as $b$ ranges over all non-zero residue classes, so does $a b$. We may therefore replace $b$ by $a b$ to get 

$$\array{
S^2 & = & \sum_{a, b} \left(\frac{a^2 b}{p}\right) \zeta^{a + a b} \\ 
 & = & \sum_{a, b} \left(\frac{b}{p}\right) \zeta^{a(1 + b)} \\ 
 & = & \sum_a \left(\frac{-1}{p}\right) \zeta^0 + \sum_{b \neq -1} \left(\frac{b}{p}\right) \sum_a \zeta^{a(1 + b)}
}.$$ 

Now, for $b \neq -1$, the character sum $\sum_a \zeta^{a(1+b)}$ evaluates to $-1$ since $1 + \zeta + \ldots + \zeta^{p-1} = 0$. Thus the calculation continues: 

$$\array{
S^2 & = & \left(\frac{-1}{p}\right) (p-1) + (-1)\sum_{b \neq -1} \left(\frac{b}{p}\right) \\ 
 & = & \left(\frac{-1}{p}\right) p - \sum_b \left(\frac{b}{p}\right) \\ 
 & = & \left(\frac{-1}{p}\right) p
}$$ 

which completes the proof. 
=-- 

Thus $S$ belongs to a quadratic extension of $\mathbb{Q}$, either $\mathbb{Q}(\sqrt{p})$ or $\mathbb{Q}(\sqrt{-p})$ depending on the Legendre symbol. In particular, the prime $p$ is [[ramification|ramified]] in $\mathbb{Q}(\zeta)$. 

+-- {: .proof} 
###### Proof of quadratic reciprocity law 
First let $p$, $q$ be two distinct odd primes. With $S$ defined as above, we calculate $S^q \; mod \; q$, where $mod \; q$ indicates the quotient of the [[ideal]] generated by $q$ in the above-mentioned quadratic extension of $\mathbb{Q}$, in two ways. 

On the one hand, by the preceding lemma, 

$$\array{
S^q & = & S(S^2)^{\frac{q-1}{2}} \\
 & = & S\left(\frac{-1}{p}\right)^{\frac{q-1}{2}} p^{\frac{q-1}{2}} \\ 
 & = & S(-1)^{\frac{p-1}{2}\frac{q-1}{2}} p^{\frac{q-1}{2}} \\ 
 & \equiv & S (-1)^{\frac{p-1}{2}\frac{q-1}{2}} \left(\frac{p}{q}\right) \; mod \; q
.}$$ 

On the other hand, since raising to the power $q$ is an [[isomorphism|automorphism]] on the [[quotient]] [[ring]] obtained modulo $q$ (either $\mathbb{F}_q \times \mathbb{F}_q$ or $\mathbb{F}_{q^2}$, depending on whether $p$ is a square modulo $q$ or not), we have 

$$\array{ 
S^q & \equiv & \sum_a \left(\frac{a}{p}\right) \zeta^{a q} \; mod \; q \\ 
 & \equiv & \left(\frac{q}{p}\right) \sum_a \left(\frac{a q}{p}\right) \zeta^{a q} \; mod \; q \\
 & \equiv & \left(\frac{q}{p}\right) S \; mod \; q
}$$ 

and now we can cancel $S$ (which is invertible modulo $q$, since $S^2$ is) to arrive at 

$$\left(\frac{q}{p}\right) = (-1)^{\frac{p-1}{2}\frac{q-1}{2}} \left(\frac{p}{q}\right)$$ 

which gives the first clause of the reciprocity law. 

As for the second clause, we can give a similar analysis. The prime $q = 2$ is ramified in the cyclotomic extension $\mathbb{Q}[i]$ since $(1 + i)^2 = 2 i$, and for any prime $p$ we may calculate $(1 + i)^p \; mod \; p$ in two ways. On the one hand, 

$$\array{
(1 + i)^p & = & (1+i)(2 i)^{\frac{p-1}{2}} \\ 
 & \equiv & (1+i)i^{\frac{p-1}{2}} \left(\frac{2}{p}\right) \; mod \; p
}$$ 

and on the other hand, 

$$\array{
(1+i)^p & \equiv & 1^p + i^p \; mod \; p
}$$ 

and by examining the cases $p \equiv 1, 3, 5, 7 \; mod \; 8$ separately, we easily deduce the second clause. 
=-- 


### Zolotarev's proof 

The (in hindsight obvious!) structural meaning of the Legendre symbol was first given by [Zolotarev](#Zolotarev): 

+-- {: .num_lemma}
###### Lemma (Zolotarev) 
For $p$ an odd prime and $a$ relatively prime to $p$, $\left(\frac{a}{p}\right)$ is the sign or [[signature of a permutation]] on $\mathbb{Z}/p$ given by multiplying by $a$. 
=-- 

Since $0$ is the unique fixed point of this permutation, this statement is equivalent to the same statement but with $\mathbb{Z}/p$ replaced by $(\mathbb{Z}/p)^\ast$. 

+-- {: .proof} 
###### Proof 
Both the Legendre symbol $\left(\frac{ }{p}\right) \colon (\mathbb{Z}/p)^\ast \to \{-1, 1\}$ and 

$$(\mathbb{Z}/p)^\ast \stackrel{Cayley}{\to} Perm((\mathbb{Z}/p)^\ast) \stackrel{sign}{\to} \{-1, 1\}$$ 

are homomorphisms [whose domain is a cyclic group](http://ncatlab.org/nlab/show/root#roots_of_unity_in_fields_11), so it suffices to show they agree on a generator $g$. But $Cayley(g)$ is a cyclic [[permutation]] on $p-1$ elements, hence has sign $(-1)^{p-2} = -1$, which agrees with $\left(\frac{g}{p}\right)$. 
=-- 

We turn now to Zolotarev's  proof of the "hard" case of quadratic reciprocity where $p$ and $q$ are distinct odd primes. What is interesting is that from this point forward, we don't use primality of $p$ and $q$ at all, i.e., the remainder of the argument carries over if $p$ and $q$ are replaced by odd, relatively prime integers $m$ and $n$, and we simply define $\left(\frac{a}{n}\right)$ as a sign of a permutation of multiplying by $a$ on $\mathbb{Z}/n$. Indeed, one often defines the **Jacobi symbol** by 

$$\left(\frac{a}{n}\right) \coloneqq \prod_{i} \left(\frac{a}{p_i}\right)$$ 

where $n = p_1 \ldots p_r$ is the prime factorization of an odd integer, and what we really do is generalize quadratic reciprocity from the Legendre symbol to the Jacobi symbol. Thus, the primality assumption is concentrated purely in the preceding lemma. 

+-- {: .proof}
###### Proof of quadratic reciprocity 
For $m \gt 1$ an odd number, we consider the set $\mathbb{Z}/m = \{0, 1, \ldots, m-1\}$ as carrying on the one hand a ring structure, and on the other as carrying a structure of linear order (no compatibility between these structures!). Now suppose $m$ and $n$ are odd and relatively prime; then by the [[Chinese remainder theorem]], there is a unique ring isomorphism 

$$\mathbb{Z}/m n \to \mathbb{Z}/m \times \mathbb{Z}/n.$$ 

If we endow $\mathbb{Z}/m \times \mathbb{Z}/n$ with the dictionary or [[lexicographic order]], then there is also a unique isomorphism of linear or [[total orders]] 

$$(\mathbb{Z}/m \times \mathbb{Z}/n)_{Dict} \to \mathbb{Z}/m n$$ 

which takes an element $(x, y) \in \mathbb{Z}/m \times \mathbb{Z}/n$ to $n x + y \in \{0, 1, \ldots, m n - 1\}$. (Intuitively, imagine assembling a rectangular array of cards, with $m$ columns and $n$ cards in each column, into a single stack of $m n$ cards, by gathering up the first column, followed by gathering up the second column and placing it underneath, etc.) 

The composite $\alpha$ of the functions 

$$(\mathbb{Z}/m \times \mathbb{Z}/n)_{Dict} \stackrel{ord \cong}{\to} \mathbb{Z}/m n \stackrel{ring \cong}{\to} \mathbb{Z}/m \times \mathbb{Z}/n$$ 

is thus $(x, y) \mapsto n x + y \mapsto (n x + y, y)$. The composite is thus a juxtaposition of $n$ row permutations, one for each fixed $y$, where $x$ in row $y$ is taken to $n x + y$ in row $y$. The sign of such a permutation $x \mapsto n x + y$ is 

$$sign((-) + y) \cdot sign(n(-)) = sign(n(-)) = \left(\frac{n}{m}\right)$$ 

(since the permutation $(-) + y$ is a cyclic permutation on an odd number of elements, hence is even). Thus 

$$sign(\alpha) = \left(\frac{n}{m}\right)^n = \left(\frac{n}{m}\right)$$ 

where the second equation follows since $n$ is odd. 

Similarly, consider $\mathbb{Z}/m \times \mathbb{Z}/n$ with the _reverse_ dictionary order, where $(x, y) \lt (x', y')$ if $y \lt y'$ or $y = y'$ and $x \lt x'$. We again have a unique order isomorphism and unique ring isomorphism, and we can analyze their composition $\beta$,  

$$(\mathbb{Z}/m \times \mathbb{Z}/n)_{RevDict} \stackrel{ord \cong}{\to} \mathbb{Z}/m n \stackrel{ring \cong}{\to} \mathbb{Z}/m \times \mathbb{Z}/n,$$ 

as taking $(x, y) \mapsto (x, x + m y)$. We similarly calculate 

$$sign(\beta) = \left(\frac{m}{n}\right).$$ 

Finally, $\beta^{-1} \circ \alpha$ is the unique order-preserving isomorphism 

$$(\mathbb{Z}/m \times \mathbb{Z}/n)_{Dict} \to (\mathbb{Z}/m \times \mathbb{Z}/n)_{RevDict}$$ 

which gives a permutation on the underlying set $\mathbb{Z}/m \times \mathbb{Z}/n$, and it remains to show that its sign is $(-1)^{\frac{m-1}{2}\frac{n-1}{2}}$. 

But this is easy to see. Recall that given a permutation $\sigma$ on a linearly ordered set (such as $(\mathbb{Z}/m \times \mathbb{Z}/n)_{Dict}$), an _inversion_ is a pair $(x \lt y)$ such that $\sigma(x) \gt \sigma(y)$, and if $I(\sigma)$ is the total number of inversions, then 

$$\sign(\sigma) = (-1)^{I(\sigma)}.$$ 

In the present case $\sigma = \beta^{-1} \alpha$, we see $I(\sigma)$ counts pairs of pairs $(i, j)$, $(i', j')$ where $(i, j) \lt (i', j')$ in dictionary order but $(i, j) \gt (i', j')$ in reverse dictionary order; in other words when $i \lt i'$ but $j' \lt j$. The number of such occurrences is 

$$I(\sigma) = \frac{m(m-1)}{2} \frac{n(n-1)}{2}$$ 

whence (again since $m, n$ are odd) 

$$(-1)^{I(\sigma)} = (-1)^{\frac{m-1}{2}\frac{n-1}{2}}$$ 

which completes the proof. 
=-- 


## Other reciprocity laws 

As mentioned earlier, quadratic reciprocity law is due to Gauss and is the first of a number of reciprocity laws in number theory. The Wikipedia article lists a bevy of reciprocity laws, gradually increasing in modernity and abstraction (and power), and culminating in [[Artin reciprocity]], a capstone of the classical [[class field theory]]. 

## Related concepts

* [[Gauss sum]]

* [Jacobi theta function -- Functional equation and Reciprocity](Jacobi+theta+function#FunctionalEquation)



## References 

* wikipedia: [reciprocity laws (mathematics)](http://en.wikipedia.org/wiki/Reciprocity_law_%28mathematics%29)

* Serge Lang, _Algebraic number theory_, Addison-Wesley (1970). 
{#Lang}

* {#Gauss} [[Carl Friedrich Gauss]], _Disquisitiones arithmeticae_ (1801), Article IV. 
 

* E.I. Zolotareff, _Nouvelle d&#233;monstration de la loi de de r&#233;ciprocit&#233; de Legendre_, Nouvelles Annales de Math&#233;matiques. 2e s&#233;rie 11 (1872) 354&#8211;362. 
{#Zolotarev} 


[[!redirects quadratic reciprocity]]
[[!redirects quadratic reciprocity law]]
[[!redirects Legendre symbol]]
[[!redirects Legendre symbols]]
