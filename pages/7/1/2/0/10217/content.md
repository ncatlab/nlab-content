
## Idea 

In logic, an incompleteness theorem says (about some formal theory) that for some statements expressed in the language of the theory, neither it nor its negation are provable in the theory: that certain statements are formally undecidable in the theory. Particularly for many theories, it is possible to internalize within the theory the external statement that the theory is consistent, but the theory, if consistent, is incapable of establishing its internal consistency. 

The most famous example is probably the pair of incompleteness theorems, due to G&#246;del, that bear on _any_ theory in which Peano arithmetic can be internalized, but in some sense the phenomenon had been known long before. For example, axiom systems for Euclidean geometry which do not include the parallel postulate might not decide the parallel postulate, as shown by models for both Euclidean and non-Euclidean geometry. But the sweeping and ubiquitous nature of incompleteness phenomena only became fully appreciated after G&#246;del's work. 

## G&#246;del incompleteness theorems 

To some extent, G&#246;del's incompleteness theorems have always had an air of mystery about them, or at least a reputation of being exceedingly difficult or subtle. The major insight of G&#246;del, that items in formal logic can be encoded within the recursive structures afforded by arithmetic, is of course a signal achievement not to be underestimated, and the detailed working out of the result that the provability predicate can be encoded as a recursive set can be said to form the technical core of this work. But the punchline, in the form of his diagonalization argument that produces a true[^fine] but unprovable sentence, should be seen for what it is: one of many diagonalization arguments (including for example Cantor's theorem) that are essentially alike in structure, and familiar to all mathematicians. 

This diagonalization result, so often obscured, should be laid bare as the simple piece of algebra that it is. We give one approach here, based on the algebra of hyperdoctrines. 

### Categorical preliminaries 

We define the equational theory $\mathbf{PRA}$ (Primitive Recursive Arithmetic) to be initial among Lawvere theories whose generator $1$ is a parametrized natural numbers object. The set of morphisms $0 \to 1$ in $\mathbf{PRA}$ is the set of equivalence classes of closed terms, and is identified with the set of numerals $\mathbb{N}$. (This $\mathbb{N}$ will serve double duty in a moment, as being also the set of objects of the Lawvere theory.) 

The first-order theory of Peano Arithmetic, PA for short, can be presented as a Boolean hyperdoctrine 

$$T: \mathbf{PRA}^{op} \to Bool$$ 

taking $j \in Ob(\mathbf{PRA}) = \mathbb{N}$ to the set $T(j)$ consisting of $j$-ary predicates in the language of PA, modulo provable equivalence in PA. If $f: j \to k$ is a morphism of $\mathbf{PRA}$ and $R \in T(k)$, we let $f^\ast (R)$ denote $T(f)(R) \in T(j)$; it can be described as the result of substituting or pulling back $R$ along $f$. There is a corresponding "action" of $\mathbf{PRA}$ on $T$, 

$$\mathbf{PRA}(j, k) \times T(k) \stackrel{action}{\to} T(j)$$ 

$$\,$$ 

$$(f, R) \mapsto f^\ast(R),$$ 

which allows us to regard $T$ as a $\mathbf{PRA}$-module. 

### Syntactic terminology and notation 

Let $Form(PA)$ be the set of all formulas of PA, with $\Phi(j)$ the set of formulas with $j$ free variables. There is an equivalence relation on $\Phi(j)$, where two formulas $F, F'$ belong to the same equivalence class $[F]$ if they are provably equivalent in PA. Thus $[-]: \Phi(j) \to T(j)$ is the corresponding quotient map. Let $Term(0)$ denote the set of closed terms in the logical theory $PRA$; morphisms $0 \to 1$ in the Lawvere theory $\mathbf{PRA}$ are equivalence classes of terms, and we let $ev: Term(0) \to \mathbf{PRA}(0, 1)$ be the corresponding quotient map. The map $ev$ has a section $num: \mathbf{PRA}(0, 1) \to Term(0)$ which sends each morphism $0 \stackrel{'n'}{\to} 1$ to the corresponding numeral term (the $n$-fold successor of the zero term). Finally, we have a substitution map 

$$sub: Term(0) \times \Phi(1) \to \Phi(0)$$ 

that substitutes a closed term $\tau$ in for the free variable of $F \in \Phi(1)$, giving a closed formula $sub(\tau, F) \in \Phi(0)$.  

There is a standard G&#246;del coding taking formulas to numerals,  

$$code: Form(PA) \to \mathbf{PRA}(0, 1),$$ 

and we define an application pairing $\cdot$ to be the composite along the top of the following commutative diagram: 

$$\array{
Form(PA) \times \Phi(1) & \stackrel{code \times 1}{\to} & \mathbf{PRA}(0, 1) \times \Phi(1) & \stackrel{num \times 1}{\to} & Term(0) \times \Phi(1) &  \stackrel{sub}{\to} & \Phi(0) \\ 
 & & & _\mathllap{1 \times [-]} \searrow & \downarrow _\mathrlap{ev \times [-]} & & \downarrow _\mathrlap{[-]} \\ 
 & & & & \mathbf{PRA}(0, 1) \times T(1) & \underset{action}{\to} & T(0).
}$$ 

In other words, for all formulas $F \in Form(PA)$ and $R \in \Phi(1)$, we define the pairing $F \cdot R \coloneqq sub(num (code(F)), R)$, and according to the commutative diagram, we have the equation 

$$\label{eqn1} [F \cdot R] = code(F)^\ast ([R])$$ 

which will be used in our diagonalization result. 

### Diagonalization 

The following result is routine from general recursive-arithmetic properties of G&#246;del coding: 

+-- {: .num_lemma} 
###### Lemma 
There is a primitive recursive function (i.e., a morphism $d: 1 \to 1$ in $\mathbf{PRA}$) such that for all $t \in \Phi(1)$, we have $d \circ code(t) = code (t \cdot t)$.[^fine] 
=-- 

+-- {: .num_theorem #fix} 
###### Theorem 
For every $R \in \Phi(1)$ there is a fixed point in \Phi(0), i.e., a closed formula $s \in \Phi(0)$ such that $[s] = [s \cdot R]$ ($s$ is provably equivalent to $s \cdot R$). 
=-- 

+-- {: .proof} 
###### Proof 
Pick a formula $t \in \Phi(1)$ such that $[t] = d^\ast [R]$, and then put $s = t \cdot t$. We have 

$$\array{
[t \cdot t] & = & code(t)^\ast ([t]) & equation\; (1) \\ 
 & \coloneqq & code(t)^\ast (d^\ast [R]) & \\ 
 & = & (d \circ code(t))^\ast ([R]) & (functoriality) \\ 
 & = & (code (t \cdot t))^\ast ([R]) & (by\; the\; lemma)\\ 
 & = & [(t \cdot t) \cdot R] & equation\; (1) 
}$$ 

as required. 
=-- 


### Incompleteness 

Recall there is also a G&#246;del coding of PA proofs (certain sequences of PA formulas), $code: Proof(PA) \to \mathbf{PRA}(0, 1)$. 

+-- {: .num_lemma} 
###### Lemma 
There is a binary primitive recursive predicate $Pf$ such that $Pf(p, x)$ is true in $\mathbb{N}$ if $p$ is the code of a proof of a sentence (a closed formula) with code $x$. Thus there is an unary recursive predicate $Prov \coloneqq \exists_p Pf(p, x) \in T(1)$. Similarly, there is an unary recursive predicate $R = \neg Prov \in T(1)$. 
=-- 

+-- {: .num_theorem} 
###### Theorem 
**(G&#246;del's First Incompleteness Theorem)** 
There exists a sentence $s$ in the language of PA such that $s$ is logically equivalent to the PA-sentence $code(s)^\ast (\neg Prov)$ (whose interpretation in the model $\mathbb{N}$ is that $s$ has no PA proof). 
=-- 

Thus, if $s$ is false in $\mathbb{N}$, then $s$ has a PA proof (so that PA proves a false statement in a model: is inconsistent). In classical logic, the only other alternative is that $s$ is true in $\mathbb{N}$, but then this true sentence (in the language of PA) has no PA proof. 

+-- {: .proof} 
###### Proof 
Indeed, let $R$ be a formula that represents the unary predicate $\neg Prov$, and let $s$ be a fixed point in the sense $[s] = [s \cdot R]$. The equality here is logical equivalence, and $[s \cdot R] = code(s)^\ast (\neg Prov)$ by equation (eq:eqn1). 
=-- 

+-- {: .num_remark} 
###### Remark 
The proof of theorem \ref{fix} was written to lay bare its provenance as a special case of Lawvere's fixed point theorem, and its essential kinship with the structure of the standard fixpoint combinator in combinatory algebra. See Yanofsky's article below. 
=-- 

## References 

* Noson S. Yanofsky, _A Universal Approach to Self-Referential Paradoxes, Incompleteness and Fixed Points_, arXiv:math/0305282 ([web](http://arxiv.org/abs/math/0305282)) 

[^fine]: Assuming that the theory is consistent. If the theory is inconsistent, then it can prove falsity and thence anything, including any internal statements of consistency. 

[^fine]: This and the next lemma demonstrate the essential truth of Paul Taylor's quip (Practical Foundations of Mathematics, p. 192): "Lemmas do the work in mathematics: Theorems, like management, just take the credit. A good lemma also survives a philosophical or technological revolution." 
