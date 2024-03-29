
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

## Examples

* The __[[fundamental theorem of algebra]]__ is, classically, the statement that the [[complex number]]s form an algebraically closed field $\mathbb{C}$.  

  Arguably, this theorem is not entirely algebraic; the algebraic portion is that $R[\mathrm{i}]$ is algebraically closed whenever $R$ is a [[real-closed field]].  Unusually, this algebraic portion is *not* (as stated) valid in [[constructive mathematics]], while the analytic result (that the [[real numbers]] form a real closed field $\mathbb{R}$) is constructively valid with the usual definitions.
 
* The algebraic closure $\overline{\mathbb{Q}}$ of the [[rational numbers]] $\mathbb{Q}$ is the [[algebraic numbers]].

## Related concepts

* [[Galois group]]

* [[separable closure]]

* [[geometric point]] 

The algebraic closure of a field $F$ is the splitting field of the set of all [[monic polynomials]] over $F$. Thus for relevant material, see 

* [[splitting field]] 

## References

* {#Leinster21} [[Tom Leinster]], _[Algebraic closure](https://golem.ph.utexas.edu/category/2021/04/algebraic_closure.html)_, [[n-Category Café]]

*  {#Chow06} _[Algebraic closure of Q](http://cs.nyu.edu/pipermail/fom/2006-May/010531.html)_, a thread on FOM started by [[Timothy Chow]]; 

be sure to check for improperly replied posts with the same subject in that and the next two months

* {#Banaschewski92} [[Bernhard Banaschewski]], *Algebraic closure without choice*, Mathematical Logic Quarterly, Volume 38, Issue 1, 1992, Pages 383-385, &lbrack;[doi:10.1002/malq.19920380136](https://doi.org/10.1002/malq.19920380136)&rbrack;

* {#Richman00} [[Fred Richman]], *The fundamental theorem of algebra: a constructive development without choice*, Pacific Journal of Mathematics **196** 1 (2000) 213–230 &lbrack;[doi:10.2140/pjm.2000.196.213](http://dx.doi.org/10.2140/pjm.2000.196.213), [pdf](https://msp.org/pjm/2000/196-1/pjm-v196-n1-p10-p.pdf)&rbrack;

* {#Ruitenberg91} Wim Ruitenberg, Constructing Roots of Polynomials over the Complex Numbers, Computational Aspects of Lie Group Representations and Related Topics, CWI Tract, Vol. 84, Centre for Mathematics and Computer Science, Amsterdam, 1991, pp. 107–128. ([pdf](https://www.mscsnet.mu.edu/~wim/publica/roots_new.pdf))

[[!redirects algebraically closed field]]
[[!redirects algebraically closed fields]]

[[!redirects algebraic closure]]
[[!redirects algebraic closures]]
