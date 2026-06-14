
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[field]] $k$ is __algebraically closed__ if every non-constant [[polynomial]] (with one variable and coefficients from $k$) has a root in $k$.  It follows that every polynomial of degree $n$ can be factored uniquely (up to [[permutation]] of the factors) as
$$ p = c \prod_{i = 1}^n (\mathrm{x} - a_i) ,$$
where $c$ and the $a_i$ are elements of $k$.


An __algebraic closure__ of an arbitrary field $k$ is an algebraically closed field $\bar{k}$ equipped with a field homomorphism (necessarily an [[injection]]) $i: k \to \bar{k}$ such that $\bar{k}$ is an [[algebraic extension]] of $k$ (which means that every element of $\bar{k}$ is the root of some non-zero polynomial with coefficients only from $k$). For example, $\mathbb{C}$ is an algebraic closure of $\mathbb{R}$.   An algebraic closure of $k$ can also be described as a maximal algebraic extension of $k$.  The [[axiom of choice]] proves the existence of $\bar{k}$ for any field $k$, as well as its uniqueness up to [[isomorphism]] over $k$.  (See [[splitting field]] for a more refined result.) However, note that $\bar{k}$ need not be unique up to *unique* isomorphism, so it\'s not really appropriate to speak of [[the]] algebraic closure of $k$.  For example, complex conjugation is a nontrivial [[automorphism]] of $\mathbb{C}$ over $\mathbb{R}$.

Without choice, the existence and uniqueness of algebraic closures may fail; see [Chow06](#Chow06), [Banaschewski92](#Banaschewski92), [Richman00](#Richman00). 

Even with choice, algebraic closure is not [[functor|functorial]] in any reasonable sense. For example, it is very easy to demonstrate that there is no algebraic closure functor $F \mapsto \widebar{F}$ that renders the inclusion $i: F \to \widebar{F}$ natural: 

+-- {: .num_example} 
###### Example 
Supposing there were such an algebraic closure functor $F \mapsto \widebar{F}$, consider its application to the (equalizer) diagram 

$$\mathbb{R} \to \mathbb{C} \underoverset{conj}{id}{\rightrightarrows} \mathbb{C}.$$ 

We would have a commutative naturality diagram (meaning serially commutative on the right) 

$$\array{
\mathbb{R} & \stackrel{i}{\to} & \mathbb{C} & \underoverset{conj}{id}{\rightrightarrows} & \mathbb{C} \\ 
\mathllap{i} \downarrow & & \mathllap{id} \downarrow & & \downarrow \mathrlap{id} \\ 
\widebar{\mathbb{R}} & \stackrel{\widebar{i}}{\to} & \widebar{\mathbb{C}} & \underoverset{\widebar{conj}}{\widebar{id}}{\rightrightarrows} & \widebar{\mathbb{C}} 
}$$ 

where serial commutativity of the right square(s) forces $\widebar{id} \neq \widebar{conj}$, but functoriality applied to the equation $id \circ i = conj \circ i$ on the top forces $\widebar{id} = \widebar{conj}$ (no matter which isomorphism $\widebar{i}$ is taken to be, $id$ or $conj$). 
=-- 

Thus, any two algebraic closures are isomorphic, but [[unnatural isomorphism|not naturally]] so. 

## Classical invariants 

Putting aside the concerns of constructive mathematics, and freely adopting the principle of the [[excluded middle]] and the [[axiom of choice]], algebraically closed fields are characterized (up to non-unique isomorphism) by just two cardinal invariants: 

+-- {: .num_theorem} 
###### Theorem 
Two algebraically closed fields $K, K'$ are isomorphic iff they have the same characteristic $p$ (the nonnegative generator of the [[kernel]] of the unique [[ring]] map $\mathbb{Z} \to K$) and the same [[transcendence degree]] (the [[cardinality]] of any maximal set of algebraically independent elements). 
=-- 

In outline, the proof is simple in structure. The "only if" statement is clear, provided we allow that transcendence degree is _well-defined_. For the "if" statement, $K$ contains a subring isomorphic to $\mathbb{Z}/(p)[S]$ where $S$ is a transcendence basis, and similarly $K'$ contains a subring isomorphic to $\mathbb{Z}/(p)[S']$. By hypothesis, there is a bijection $f: S \to S'$, which extends uniquely to an isomorphism of [[integral domains]] $\mathbb{Z}/(p)[S] \to \mathbb{Z}/(p)[S']$, which extends uniquely to an isomorphism of their fields of fractions $\mathbb{F}(S) \to \mathbb{F}(S')$. Then $K, K'$ are algebraic closures of these fields, and one applies a theorem that an isomorphism of fields $\mathbb{F}(S) \to \mathbb{F}(S')$ can be extended to an isomorphism $K \to K'$ of their algebraic closures. 

The full details of such a proof carry some themes important in [[model theory]]: 

* There is a notion of algebraic closure of a subset, 

* There are prime models (algebraic closure of prime field $\mathbb{Z}/(p)$), 

* There are notions of independence and basis, and well-defined degree or dimension, 

* There are extensions of isomorphisms of independent sets to isomorphisms of their algebraic closures. 

Perhaps the most subtle in the list is the notion of independence and well-definedness of (transcendence) degree, which notably involves verification of the Steinitz exchange axiom: 

+-- {: .num_lemma} 
###### Lemma 
Let $K$ be an algebraically closed field, and let $cl: P(K) \to P(K)$ be the operator that takes a subset $S \subseteq K$ to the smallest algebraically closed subfield that contains $S$. Then $cl$ is a [[geometric stability theory|pregeometry]]. 
=-- 

+-- {: .proof} 
###### Proof 
For the moment, please consult Jacobson, Basic Algebra II, Theorem 8.34. This may be expanded upon a little later. 
=-- 

Well-definedness of transcendence degree then follows from abstract considerations of pregeometries; see [this result](/nlab/show/matroid#welldefined). 

## In constructive mathematics

In [[constructive mathematics]], for [[Heyting fields]], one has to use the [[tight apartness relation]] of the Heyting field to define a nonconstant polynomial to mean "apart from every constant polynomial function" in the definition of an algebraically closed field. 

Algebraic closure for Heyting fields is equivalent in strength to [[integral closure]] for Heyting fields: 

\begin{theorem}
Suppose that $F$ is integrally closed: every monic polynomial function is separable. Then $F$ is algebraically closed: every non-constant polynomial function is separable. 
\end{theorem}

\begin{proof}
One can adapt the proof of theorem 1 of [Geuvers, Wiedijk, & Zwanenburg 2000](#GWZ00) to the statement that every monic polynomial function of a Heyting field is separable, replacing every statement that "there exists a zero for a polynomial function" with the statement that "the polynomial function is separable". Lemma 6 and Corollary 1 of [Geuvers, Wiedijk, & Zwanenburg 2000](#GWZ00) hold for any [[Heyting field]] $F$ as their proofs only require the field structure of $F$, and the equivalent of Theorem 1 here is that "every non-constant polynomial function is separable" and depends on Lemma 6, Corollary 1, and the statement that "every monic polynomial function is separable" but otherwise only depends on the field structure of $F$. 
\end{proof}

The converse holds because every monic polynomial function is non-constant. 

## Examples

* The algebraic closure $\overline{\mathbb{Q}}$ of the [[rational numbers]] $\mathbb{Q}$ is the [[algebraic numbers]].

* The algebraic closure of a field $F$ is the [[splitting field]] of the set of all [[monic polynomials]] over $F$. 

### Algebraic closure of the complex numbers

The __[[fundamental theorem of algebra]]__ is, classically, the statement that the [[complex number]]s form an algebraically closed field $\mathbb{C}$. 

There are many proofs of the algebraic closure of the complex numbers, all of which are not algebraic in some sense or another; most of them use [[real analysis]] or [[complex analysis]] in one form or another. However, there is one proof of the fundamental theorem of algebra which is somewhat algebraic, that first proves the real numbers are a [[real closed field]], and then proves that $R[\mathrm{i}]$ is algebraically closed whenever $R$ is a [[real closed field]]; this second portion is algebraic classically. 

In [[constructive mathematics]], there are multiple different notions of a [[real closed field]]. In particular, one can consider the mere existence in the sense of [[first order logic]], that there exists a [[root]] of odd degree polynomials in $\mathbb{R}$, or one can consider constructive existence in the sense of the [[BHK interpretation]], that one can construct a specified root of odd degree polynomials in $R$. 

On one hand, the result that for every non-negative real number there exists a [[real square root]] and for every odd degree real polynomial there exists a root of the polynomial is constructively valid. On the other hand, the stronger statement that for every odd degree real polynomial one can construct a specified root of the polynomial is not provable in [[constructive mathematics]] without a weak form of choice: that every surjective polynomial function with odd degree and fixed point at zero has a [[section]]. This gap is analytic in nature as the weak form of choice implies the existence of [[discontinuous functions]] on the [[real numbers]], since any section of the polynomial function $x \mapsto x^3 - 3x$ is necessarily discontinuous somewhere in the [[closed interval]] $[-2, 2]$, which implies the constructive [[taboo]] [[analytic WLPO]] (see definition 7.3 and proposition 7.5 of [Bauer & Hanson 2026](#BauerHanson)). This stronger statement is needed for the algebraic result of being able to factor real polynomials of odd degree into a real polynomial of degree 1 and a monic polynomial of even degree with coefficients in the reals, which is needed to show that the complex numbers are [[algebraically closed]]. 

More generally, in constructive mathematics, there are many different versions of the [[fundamental theorem of algebra]] that are not provably equivalent to the statement that the complex numbers are algebraically closed. Some of these versions of the fundamental theorem of algebra, such as there merely existing a root of every non-constant polynomial function, are provable in [[constructive mathematics]]. However, the statement that the complex numbers are algebraically closed is only provable in [[constructive mathematics]] when using some constructive [[taboos]], since factorization of a monic polynomial in $\mathbb{C}$ requires being able to construct the $n$ [[roots]] of a monic [[polynomial function]] in $\mathbb{C}$. This in turn is equivalent to a weak form of choice that states that every [[surjective]] polynomial function in $\mathbb{C}$ has a [[section]]. This fails in some [[toposes]], such as the [[topos of sheaves]] on the [[real numbers]] $\mathbb{R}$, where all functions on $\mathbb{C}$ are [[continuous functions]], and any section of a monic polynomial function with [[degree of a polynomial|degree]] $n \geq 2$, if it exists, necessarily has to be discontinuous at a branch cut. 

## Related concepts

* [[Galois group]]

* [[separable closure]]

* [[geometric point]] 

* [[splitting field]] 

## References

* {#Leinster21} [[Tom Leinster]], _[Algebraic closure](https://golem.ph.utexas.edu/category/2021/04/algebraic_closure.html)_, [[n-Category Café]]

*  {#Chow06} _[Algebraic closure of Q](http://cs.nyu.edu/pipermail/fom/2006-May/010531.html)_, a thread on FOM started by [[Timothy Chow]]; 

be sure to check for improperly replied posts with the same subject in that and the next two months

* {#Banaschewski92} [[Bernhard Banaschewski]], *Algebraic closure without choice*, Mathematical Logic Quarterly, Volume 38, Issue 1, 1992, Pages 383-385, &lbrack;[doi:10.1002/malq.19920380136](https://doi.org/10.1002/malq.19920380136)&rbrack;

* {#Richman00} [[Fred Richman]], *The fundamental theorem of algebra: a constructive development without choice*, Pacific Journal of Mathematics **196** 1 (2000) 213–230 &lbrack;[doi:10.2140/pjm.2000.196.213](http://dx.doi.org/10.2140/pjm.2000.196.213), [pdf](https://msp.org/pjm/2000/196-1/pjm-v196-n1-p10-p.pdf)&rbrack;

* {#Ruitenberg91} [[Wim Ruitenburg]]: *Constructing Roots of Polynomials over the Complex Numbers*, Computational Aspects of Lie Group Representations and Related Topics, CWI Tract **84** Centre for Mathematics and Computer Science, Amsterdam (1991) 107–-128 &lbrack;[pdf](https://www.mscsnet.mu.edu/~wim/publica/roots_new.pdf), [[Ruitenburg-Roots.pdf:file]]&rbrack;

* {#GWZ00} Herman Geuvers, Freek Wiedijk, Jan Zwanenburg, *A Constructive Proof of the Fundamental Theorem of Algebra without using the Rationals*, TYPES '00: Selected papers from the International Workshop on Types for Proofs and Programs, Pages 96 - 111, 08 December 2000 &lbrack;[web](https://dl.acm.org/doi/10.5555/646540.696038), [pdf](https://www.cs.ru.nl/F.Wiedijk/pubs/kneser.pdf)&rbrack;

* {#LombardiQuitté2010} [[Henri Lombardi]], [[Claude Quitté]] (trans. by Tania K. Roblo): *Commutative algebra: Constructive methods --- Finite projective modules*, Springer (2015) &lbrack;[doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf)&rbrack;

* {#BauerHanson} [[Andrej Bauer]], [[James Hanson]], *The Countable Reals* ([arXiv:2404.01256](https://arxiv.org/abs/2404.01256))

[[!redirects algebraically closed field]]
[[!redirects algebraically closed fields]]

[[!redirects algebraic closure]]
[[!redirects algebraic closures]]

[[!redirects algebraically closed]]