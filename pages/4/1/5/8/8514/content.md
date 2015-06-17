
#Contents#
* table of contents
{:toc}


## Idea

The _abc conjecture_ (or _ABC conjecture_) is a [[number theory|number theoretic]] conjecture due to ([Oesterl&#233;-Masser 1985](#Oesterl&#233;Masser)), which says that there are only [[finite set|finitely many]] integer solutions to the [[equation]] 

$$
  a + b = c   \;\;\; for   a,b,c \geq 1 \in \mathbb{N}
$$

(or instead $a+b+c= 0$)
if one requires the [[integer numbers]] $a,b,c$ to have no common factor as well as having "joint power" greater than a given bound.

Here the _power_ of $a,b,c$ is

$$
  P(a,b,c) \coloneqq \frac{log|c|}{log(rad(a\cdot b\cdot c))}
  \,,
$$

where the [[radical]] $rad(n)$ of an [[integer]] $n$ is the product of all its distinct [[prime factors]]. 

The precise form of the conjecture is:

+-- {: .un_theorem}
###### Conjecture
**(abc conjecture)**

For any number $\epsilon\gt 0$ there are only finitely many positive relatively prime ([[coprime integers|coprime]]) [[integer]] solutions $(a,b,c)$ to the [[equation]] $a + b = c$   with power $P(a,b,c)\geq 1+\epsilon$.

=--



According to ([Mazur](#Matzur)):

> The beauty of such a Conjecture is that it captures the intuitive sense that triples of numbers which satisfy a linear relation, and which are divisible by high perfect powers, are rare; the precision of the Conjecture goads one to investigate this rarity quantitatively. Its very statement makes an attractive appeal to perform a range of numerical experiments that would test the empirical waters. On a theoretical level, it is enlightening to understand its relationship to the constellation of standard arithmetic theorems, conjectures, questions, etc., and we shall give some indications of this below.

## Mason's Theorem 

According to [Lang](#Lang), one important antecedent of the abc conjecture is a simple but at the time unexpected relation for the function field case, published in 1984. Consider polynomials $f \in k[t]$ over an algebraically closed field $k$ of characteristic $0$, and define $n_0(f)$ to be the number of _distinct_ roots of $f$, counted _without_ regard to multiplicity.  

+-- {: .un_theorem}
###### Theorem ([Mason](#Mason)) 
Let $a, b, c \in k[t]$ be relatively prime polynomials, not all constant, such that $a + b = c$. Then $\max \{deg(a), deg(b), deg(c)\} \leq n_0(a b c) - 1$. 
=-- 

+-- {: .proof} 
###### Proof 
Let $f = a/c$, $g = b/c$, so that $f + g = 1$. Taking the derivative, we obtain 

$$\frac{f'}{f} f + \frac{g'}{g} g = 0$$ 

whence 

$$b/a = g/f = -\frac{f'/f}{g'/g}.$$ 

Put 

$$a(t) = c_1 \prod (t - \alpha_i)^{m_i}, \qquad b(t) = c_2 \prod (t - \beta_j)^{n_j}, \qquad c(t) = c_3 \prod (t - \gamma_k)^{p_k}.$$ 

Then 

$$\frac{b}{a} = -\frac{f'/f}{g'/g} = -\frac{\sum \frac{m_i}{t - \alpha_i} - \sum \frac{p_k}{t - \gamma_k}}{\sum \frac{n_j}{t - \beta_j} - \sum \frac{p_k}{t - \gamma_k}} .$$

A common denominator for $f'/f$ and $g'/g$ is given by 

$$N_0 = \prod (t - \alpha_i) \prod (t - \beta_j) \prod (t - \gamma_k)$$ 

whose degree is $n_0(a b c)$. We then have 

$$\frac{b}{a} = -\frac{N_0 f'/f}{N_0 g'/g}$$ 

where the numerator and denominator on the right are polynomials. However, since $b$ and $a$ are relatively prime, the fraction $b/a$ is already in lowest terms. From this we conclude that $deg(b) \leq deg(N_0 f'/f) \leq n_0(a b c) - 1$, and similarly $deg(a) \leq deg(N_0 g'/g) \leq n_0(a b c) - 1$, which completes the proof. 
=-- 

+-- {: .un_cor} 
###### Corollary (FLT for polynomials) 
Assume $x, y, z \in k[t]$ are relatively prime polynomials, not all constant, and suppose $x^n + y^n = z^n$. Then $n \leq 2$. 
=-- 

+-- {: .proof} 
###### Proof 
From Mason's theorem, we conclude $n deg(x) = deg(x^n) \leq deg(x) + deg(y) + deg(z) - 1$, and similarly upon replacing $x$ by $y$ and $z$ on the left. Adding the results, we have 

$$n(deg(x) + deg(y) + deg(z)) \leq 3(deg(x) + deg(y) + deg(z)) - 3$$ 

which is impossible if $n \geq 3$. 
=-- 

Guided by analogies between the ring of integers and the ring of polynomials in one variable, and building on insights of Mason, Frey, Szpiro, and others, Masser and Oesterl&#233; were led to formulate the abc conjecture for integers as follows. Again define $N_0(m)$ for $m$ a non-zero integer to be the number of distinct primes dividing $m$. 

* Conjecture: For all $\epsilon \lt 0$ there exists $C(\epsilon) \lt 0$ such that for relatively prime integers $a, b, c$ satisfying $a + b = c$, we have 
$$\max({|a|}, {|b|}, {|c|}) \leq C(\epsilon)N_0(a b c)^{1+\epsilon}.$$ 

Of course, this differs from the polynomial case because of the presence of $1+ \epsilon$ in the exponent, but this is a necessary evil. For example, for any $C \gt 0$, we can find relatively prime $a$, $b$, $c$ with $a + b = c$ and ${|a|} \gt C N_0(a b c)$: take $a = 3^{2^n}$, $b = -1$, and observe by repeated application of $x^2 - y^2 = (x-y)(x+y)$ that $c = a + b$ is of the form $2^n d$ for some integer $d$. Taking $n$ sufficiently large, we can easily derive the claimed inequality. 



## Relation to other statements

The abc conjecture implies the [[Mordell conjecture]] ([Elkies](#Elkies)).

It is equivalent to the general form of [[Szpiro's conjecture]].

* [[Vojta's conjecture]]

## References

The abc conjecture was stated in 

* Joseph Oesterl&#233;, David Masser (1985)
 {#Oesterl&#233;Masser}

[[Shinichi Mochizuki]] anounced the proof which the mathematical community perceives as a serious but unchecked claim. See the references at _[[inter-universal Teichmüller theory]]_.

Comments on the proof are at

*  _[[Mochizuki's proof of abc]]_.

* MathOverflow, _[Philosophy behind Mochizuki's work on the ABC conjecture](http://mathoverflow.net/questions/106560/philosophy-behind-mochizukis-work-on-the-abc-conjecture/106658#106658)_

An popular account of the problem of the math community checking the proof is in 

* Caroline Chen, _The Paradox of the Proof_ ([web](http://projectwordsworth.com/the-paradox-of-the-proof/))

Mason's theorem was presented in 

* R.C. Mason, Equations over function fields. In _Number Theory, Proceedings of the Noordwijkerhout_, Springer Lecture Notes 1068 (1984), 149-157. 
{#Mason} 

Material on Mason's theorem and its relation to the abc conjecture was taken from 

* Serge Lang, Algebra ($3^{rd}$ Edition), Addison-Wesley (1993), 194-196. 
{#Lang}

See also

* [[Barry Mazur]], _Questions about number_, [pdf](http://www.math.harvard.edu/~mazur/papers/scanQuest.pdf) scan
 {#Mazur}

* PolyMath, _[ABC conjecture](http://michaelnielsen.org/polymath1/index.php?title=ABC_conjecture)_

*  Abderrahmane Nitaj, _[The ABC Conjecture Homepage](http://www.math.unicaen.fr/~nitaj/abc.html)_

* Wikipedia, _[abc conjecture](http://en.wikipedia.org/wiki/Abc_conjecture)_


The relation to the [[Mordell conjecture]] is discussed in

* [[Noam Elkies]], _ABC conjecture implies Mordell_, Int. Math. Research Notices 7 (1991) 99-109
 {#Elkies}

The relation to [[Szpiro's conjecture]] is discussed in 

* Matt Baker (notes taken by William Stein), _Elliptic curves, the ABC conjecture, and points of small canonical height_ ([pdf](http://modular.math.washington.edu/mcs/archive/Fall2001/notes/12-10-01/12-10-01.pdf))
