
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

* table of contents
{: toc}

## Idea 

In [[logic]], an incompleteness theorem expresses limitations on provability within a (consistent) formal [[theory]]. Most famously it refers to a pair of theorems due to [[Kurt Gödel]]; the first incompleteness theorem says roughly that for any [[consistent theory]] $T$ containing [[Peano arithmetic|arithmetic]] and whose [[axioms]] form a [[recursive set]], there is an arithmetic sentence which is true for the [[natural numbers]] $\mathbb{N}$ that cannot be proven in $T$. The second incompleteness theorem shows that for such theories $T$, the sentence can be taken to be a suitable arithmetization of the statement of consistency of $T$ itself, i.e., that no such theory "can demonstrate its own consistency" -- can prove an arithmetic statement that encodes the assertion of its consistency. 

An incompleteness theorem can be read as an [[undecidable proposition|undecidability result]]: there are formal propositions $p$ in the theory such that neither $p$ nor its [[negation]] $\neg{p}$ have [[proofs]] in the theory. As such, it is part of a long history; for example, axiom systems for [[Euclidean geometry]] not including the [[parallel postulate]] might not decide the parallel postulate, as shown by models for both Euclidean and non-Euclidean geometry. What was novel about G&#246;del's results is that they worked directly at the level of syntax and applied to any (effectively generated) extension of arithmetic, producing sentences which in effect imply their unprovability. 

To some extent, G&#246;del's incompleteness theorems have always had an air of mystery about them, or at least a reputation of being exceedingly difficult or subtle. The major insight of G&#246;del, that items in formal logic can be encoded within the recursive structures afforded by arithmetic ([[Gödel numbering]]), is of course a signal achievement not to be underestimated, and the detailed working out of the result that the provability predicate can be encoded as a [[recursive set]] can be said to form the technical core of this work. But the punchline, in the form of his [[diagonalization argument]] that produces a true[^fine1] but unprovable sentence, should be seen for what it is: one of many [[diagonalization arguments]] (including for example [[Cantor's theorem]]) that are essentially alike in structure, and familiar to all mathematicians. 

In an interview ([Lawvere 07](William+Lawvere#Interview07)) not long after G&#246;del's 100th birthday, [[William Lawvere]] answered the question

> We have recently celebrated Kurt G&#246;del's 100th birthday. What do you think about the extra-mathematical publicity around his incompleteness theorem?

by saying (reproduced in [Lawvere 69 reprint, p. 2](#Lawvere69)):

> "In 'Diagonal arguments and Cartesian closed categories' ([Lawvere 69](#Lawvere69)) we demystified the incompleteness theorem of G&#246;del and the truth-definition theory of Tarski by showing that both are consequences of some very simple algebra in the Cartesian-closed setting. It was always hard for many to comprehend how Cantor's mathematical theorem could be re-christened as a "paradox" by Russell and how G&#246;del's theorem could be so often declared to be the most significant result of the 20th century. There was always the suspicion among scientists that such extra-mathematical publicity movements concealed an agenda for re-establishing belief as a substitute for science. Now, one hundred years after G&#246;del's birth, the organized attempts to harness his great mathematical work to such an agenda have become explicit.


[[Yuri Manin]] writes in [Manin02, p. 7](#Manin02):

> Baffling discoveries such as G&#246;del's incompleteness of arithmetic lose some of their mystery once one comes to understand their content as a statement that a certain algebraic structure simply is not finitely generated with respect to the allowed composition laws.

This diagonalization result, so often obscured, should be laid bare as the simple piece of algebra that it is. We give one approach here, based on the algebra of [[hyperdoctrines]].


## G&#246;del\'s incompleteness theorems 


### Categorical preliminaries 

We define the [[equational theory]] $\mathbf{PRA}$ ([[primitive recursive arithmetic]]) to be [[initial object|initial]] among [[Lawvere theories]] whose generator $1$ is a parametrized [[natural numbers object]]. The [[hom-set]] of morphisms $0 \to 1$ in $\mathbf{PRA}$ is the set of equivalence classes of closed [[terms]], and is identified with the set $\mathbb{N}$ of [[numerals]]. (This $\mathbb{N}$ will serve double duty in a moment, as being also the set of objects of the Lawvere theory.) 

The [[first-order theory]] of [[Peano arithmetic]], PA for short, can be presented as a [[Boolean hyperdoctrine]]

$$T: \mathbf{PRA}^{op} \to BooleanAlgebra$$ 

taking $j \in Ob(\mathbf{PRA}) = \mathbb{N}$ to the set $T(j)$ consisting of $j$-ary [[predicates]] in the language of PA, modulo provable equivalence in PA. If $f: j \to k$ is a morphism of $\mathbf{PRA}$ and $R \in T(k)$, we let $f^\ast (R)$ denote $T(f)(R) \in T(j)$; it can be described as the result of substituting or pulling back $R$ along $f$. There is a corresponding "action" of $\mathbf{PRA}$ on $T$, 

$$\mathbf{PRA}(j, k) \times T(k) \stackrel{action}{\to} T(j)$$ 

$$\,$$ 

$$(f, R) \mapsto f^\ast(R),$$ 

which allows us to regard $T$ as a $\mathbf{PRA}$-module. 


### Syntactic terminology and notation 

Let $Form(PA)$ be the set of all formulas of PA, with $\Phi(j)$ the set of formulas with $j$ [[free variables]]. There is an equivalence relation on $\Phi(j)$, where two formulas $F, F'$ belong to the same equivalence class $[F]$ if they are provably equivalent in PA. Thus $[-]: \Phi(j) \to T(j)$ is the corresponding quotient map. Let $Term(0)$ denote the set of closed terms in the logical theory $PRA$; morphisms $0 \to 1$ in the Lawvere theory $\mathbf{PRA}$ are equivalence classes of terms, and we let $ev: Term(0) \to \mathbf{PRA}(0, 1)$ be the corresponding quotient map. The map $ev$ has a section $num: \mathbf{PRA}(0, 1) \to Term(0)$ which sends each morphism $0 \stackrel{'n'}{\to} 1$ to the corresponding numeral term (the $n$-fold successor of the zero term). Finally, we have a substitution map 

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

The following result is routine from general recursive-arithmetic properties of G&#246;del coding; it applies to any extension of PA (or just [[Robinson arithmetic]]) whose formulas can be recursively (computably) enumerated.  

+-- {: .num_lemma} 
###### Lemma 
There is a primitive recursive function (i.e., a morphism $d: 1 \to 1$ in $\mathbf{PRA}$) such that for all $t \in \Phi(1)$, we have $d \circ code(t) = code (t \cdot t)$.[^fine2] 
=-- 

+-- {: .num_theorem #fix} 
###### Theorem 
For every $R \in \Phi(1)$ there is a fixed point in $\Phi(0)$, i.e., a closed formula $s \in \Phi(0)$ such that $s \Leftrightarrow s \cdot R$ ($s$ is provably equivalent to $s \cdot R$). 
=-- 

+-- {: .proof} 
###### Proof 
Pick a formula $t \in \Phi(1)$ such that $[t] = d^\ast [R]$, and then put $s = t \cdot t$. We want to show $[s] = [s \cdot R]$. We have 

$$\array{
[t \cdot t] & = & code(t)^\ast ([t]) & equation\; (1) \\ 
 & \coloneqq & code(t)^\ast (d^\ast [R]) & \\ 
 & = & (d \circ code(t))^\ast ([R]) & (functoriality) \\ 
 & = & (code (t \cdot t))^\ast ([R]) & (by\; the\; lemma)\\ 
 & = & [(t \cdot t) \cdot R] & equation\; (1) 
}$$ 

as required. 
=-- 

+-- {: .num_remark} 
###### Remark 
The proof of theorem \ref{fix} was written to lay bare its provenance as a special case of [[Lawvere's fixed point theorem]], and its essential kinship with the structure of the standard fixpoint combinator in [[combinatory algebra]]. See [Yanofsky 03](#Yanofsky03). 
=-- 


### Incompleteness 

Recall there is also a G&#246;del coding of PA proofs (certain sequences of PA formulas), $code: Proof(PA) \to \mathbf{PRA}(0, 1)$. The following result applies in fact to any theory like PA that extends basic Robinson arithmetic and whose axioms form a recursive set. 

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
Indeed, let $R$ be a formula that represents the unary predicate $\neg Prov$, and let $s$ be a fixed point in the sense $[s] = [s \cdot R]$, which is guaranteed to exist by theorem \ref{fix}. The equality here is logical equivalence, and $[s \cdot R] = code(s)^\ast (\neg Prov)$ by equation (eq:eqn1). 
=-- 


## Related concepts

* [[Löb's theorem]]

* [[Lawvere's fixed point theorem]]

* [[Chaitin's incompleteness theorem]]

* [[Deligne completeness theorem]]

* [[foundations of mathematics]]

* [[platonism]]

* [[arithmetic universe]]

* [[introspective theory]]

## References 
 {#References}

* {#Lawvere69} [[William Lawvere]], _Diagonal Arguments and Cartesian Closed Categories_, Lecture Notes in Mathematics, 92 (1969), 134-145 ([TAC](http://tac.mta.ca/tac/reprints/articles/15/tr15abs.html))

* {#Manin02} [[Yuri Manin]], _Georg Cantor and his heritage_, [arXiv:math/0209244](http://arxiv.org/abs/math/0209244)

* {#Yanofsky03} Noson S. Yanofsky, _A Universal Approach to Self-Referential Paradoxes, Incompleteness and Fixed Points_, arXiv:math/0305282 ([web](http://arxiv.org/abs/math/0305282)) 

A brief review discussion explicitly in the context of [[type theory]]/[[topos theory]] is in 

* Erik Gregersen, _[Internal lanuage](http://www.britannica.com/EBchecked/topic/369221/foundations-of-mathematics/35468/Internal-language)_, Encyclopedia Britannica

A [[formal proof]] of the G&#246;del-Rosser incompleteness theorem in [[Coq]] is given in

* [[Russell O'Connor]], *Essential Incompleteness of Arithmetic Verified by Coq*, in: *Theorem Proving in Higher Order Logics. TPHOLs 2005*, Lecture Notes in Computer Science **3603**, Springer (2005) 245-260 &lbrack;[web](http://r6.ca/Goedel/goedel1.html), [arXiv:cs/0505034](https://arxiv.org/abs/cs/0505034), [doi:10.1007/11541868_16](https://doi.org/10.1007/11541868_16)&rbrack;

Formal proof of the second incompleteness theorem:

* Lawrence Paulson, _A Mechanised Proof of G&#246;del's Incompleteness Theorems using Nominal Isabelle_ &lbrack;[pdf](https://www.cl.cam.ac.uk/~lp15/papers/Isabelle/Goedel-ar.pdf)&rbrack;


Unified account of [[Löb's theorem]]/[[Gödel's second incompleteness theorem]], [[Kripke semantics]] for [[provability logic]], and [[guarded recursion]], via [[essentially algebraic theories]] which "self-internalize"::

* [[Sridhar Ramesh]], *Introspective Theories and Geminal Categories*, PhD thesis, Berkeley (2023) &lbrack;[escholarship:3mn0c475](https://escholarship.org/uc/item/3mn0c475), [[Ramesh-IntrospectiveTheories.pdf:file]]&rbrack;

The following contains a careful discussion of the incompleteness theorem in the context of categorical foundations using the [[free topos]]:

* [[Jim Lambek]], [[Phil Scott]], _Reflections on Categorical Foundations of Mathematics_ , pp.171-185 in  Sommaruga (ed.), _Foundational Theories of Classical and Constructive Mathematics_,  Springer New York 2011. ([draft](https://www.site.uottawa.ca/~phil/papers/LS11.final.pdf)) {#LS11}

A _bref survol technique_ of G&#246;del's theorem within the landscape of [[Hilbert's program]] can be found in the first chapters of

* [[Jean-Yves Girard]], _Le point aveugle I_ , Hermann Paris 2006. ([chapters 1-2](http://iml.univ-mrs.fr/~girard/cours/hermann.pdf.gz))

See also the discussion in [[list-arithmetic pretoposes]]

* [[Maria Maietti]], _Joyal's arithmetic universe as list-arithmetic pretopos_, Theory and Applications of Categories, Vol. 24, 2010, No. 3, pp 39-83. ([TAC](http://www.tac.mta.ca/tac/volumes/24/3/24-03abs.html))

* {#vanDijkOldenziel20} Joost van Dijk, Alexander Gietelink Oldenziel, _Gödel's Incompleteness after Joyal_ , arXiv:2004.10482 (2020). ([abstract](https://arxiv.org/abs/2004.10482))


[^fine1]: Assuming that the theory is consistent. If the theory is inconsistent, then it can prove falsity and thence anything, including any internal statements of consistency. 

[^fine2]: This and the next lemma demonstrate the essential truth of Paul Taylor's quip (Practical Foundations of Mathematics, p. 192): "Lemmas do the work in mathematics: Theorems, like management, just take the credit. A good lemma also survives a philosophical or technological revolution." 


[[!redirects incompleteness theorem]]
[[!redirects incompleteness theorems]]
[[!redirects Gödel incompleteness theorem]]
[[!redirects Gödel incompleteness theorems]]
[[!redirects Goedel incompleteness theorem]]
[[!redirects Goddel incompleteness theorems]]


[[!redirects Gödel's incompleteness theorem]]
[[!redirects Gödel's incompleteness theorems]]
[[!redirects Goedel's incompleteness theorem]]
[[!redirects Goedel's incompleteness theorems]]

[[!redirects Gödel\'s incompleteness theorem]]
[[!redirects Gödel\'s incompleteness theorems]]
[[!redirects Goedel\'s incompleteness theorem]]
[[!redirects Goedel\'s incompleteness theorems]]

[[!redirects Gödel's incompleteness theorem]]
[[!redirects Gödel's incompleteness theorems]]
[[!redirects Goedel's incompleteness theorem]]
[[!redirects Goedel's incompleteness theorems]]

[[!redirects Gödel's theorem]]
[[!redirects Gödel's theorems]]
[[!redirects Goedel's theorem]]
[[!redirects Goedel's theorems]]

[[!redirects Gödel\'s theorem]]
[[!redirects Gödel\'s theorems]]
[[!redirects Goedel\'s theorem]]
[[!redirects Goedel\'s theorems]]


[[!redirects Gödel's theorem]]
[[!redirects Gödel's theorems]]
[[!redirects Goedel's theorem]]
[[!redirects Goedel's theorems]]

[[!redirects Gödel's second incompleteness theorem]]
[[!redirects Gödel's second incompleteness theorems]]
[[!redirects Goedel's second incompleteness theorem]]
[[!redirects Goedel's second incompleteness theorems]]



