
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

__Geometric stability theory__ is the principal part of the branch of [[model theory]] called __[[geometric model theory]]__. It was introduced in works of [[Boris Zilber]], Gregory Cherlin, [[Ehud Hrushovski]], Anand Pillay, and others.

Geometric stability theory has largely to do with the model-theoretic classification of [[structure in model theory|structures]] in terms of dimension-like quantities that can be axiomatized in terms of notions of [[combinatorial geometry]] such as [[matroid]]. Key guiding examples include [[vector spaces]] and [[algebraically closed fields]], and many of the guiding concepts have an [[algebraic geometry|algebro-geometric]] flavor (e.g., Morley rank as a generalization of Krull dimension). 

Such a structural geometric approach can make geometric stability theory an attractive key of entry into modern model theory for those mathematicians who are not already logicians. 


## Basic concepts 

Perhaps the key axiomatic notions of geometric stability theory (which at the outset don't seem particularly wedded to logic) are those of _pregeometry_ and _geometry_. 

+-- {: .num_defn} 
###### Definition 
Let $X$ be a set. A **pregeometry** on $X$ is a [[closure operator]] (i.e., a [[monad]] $cl \colon P X \to P X$ on the [[power set]]), satisfying the following two conditions: 

* The monad $cl$ is [[finitary functor|finitary]], i.e., $A \in P X$ and $a \in cl(A)$, then there is a finite $A_0 \subseteq A$ such that $a \in cl(A_0)$. 

* (Exchange condition) If $A \in P X$, $a,b \in X$, and $a \in cl(A\cup\{b\})$, then $a \in cl(A)$ or $b \in cl(A \cup \{\a\})$. (Cf. [[matroid]]) 

A **geometry** is a pregeometry such that $cl(\emptyset) = \emptyset$ and $cl(\{x\}) = \{x\}$ for all $x \in X$. 
=-- 

+-- {: .num_example} 
###### Examples 

* Let $X$ be a [[vector space]], and let $cl$ be the monad on $P X$ whose algebras are vector subspaces of $X$. Clearly $cl$ is finitary (any subspace is the set-theoretic union of finite-dimensional subspaces), and the exchange condition is a classical fact about vector spaces related to the notion of independence. Thus $cl$ is a pregeometry. 

* Similarly, let $X$ be a [[projective space]] $\mathbb{P}V$, and let $cl$ be the monad on $P X$ whose algebras are projective subspaces. Then $cl$ is a geometry (the closure of a point is a point). Any pregeometry $cl$ gives rise to a geometry in a similar way, in the sense that a pregeometry $cl$ induces a geometry on the image of the function $X \to P X$, $x \mapsto cl(\{x\})$, as explained in Remark \ref{project}. 

* Let $X$ be an algebraically closed field; let $cl$ be the monad on $P X$ whose algebras are algebraically closed subfields. Then $cl$ is a pregeometry. That the exchange condition is satisfied is a classical result credited to Steinitz[^fine]. 
=-- 

+-- {: .num_defn}
###### Definition 
Given a pregeometry $(X, cl)$, a subset $A \in P X$ is **independent** if for all $a \in A$, $a \notin cl(A - \{a\})$. An independent set $A$ said to be a **basis** for $Y \in P X$ if $Y \subseteq cl(A)$. All bases of $Y$ have the same cardinality, called the **dimension** of $Y$. 
=-- 

+-- {: .num_remark} 
###### Remark 
Given a pregeometry $(X, cl)$ and a subset $Y \subseteq X$, there is a restriction pregeometry $cl^Y: P(Y) \to P(Y)$ defined by the formula 

$$cl^Y(S) = cl(S) \cap Y.$$ 

It is immediate that $A \subseteq Y$ is independent in $(X, cl)$ iff it is independent in $(Y, cl^Y)$, and that it is a basis for $Y$ in $(X, cl)$ iff it is a basis for $Y$ in $(Y, cl^Y)$. By this observation, to prove that any $Y \in P(X)$ has a well-defined dimension, we may assume without loss of generality that $Y = X$. That a pregeometry $X$ has well-defined dimension was proven [here](nlab/show/matroid#welldefined). 
=-- 

+-- {: .num_remark #project} 
###### Remark 
There is a standard way of getting a geometry from a pregeometry $(X, cl)$. First, if $cl(\emptyset) \neq \emptyset$, then replace $X$ by $X' \coloneqq X - cl(\emptyset)$, equipped with the restriction pregeometry of the previous remark. Then define an equivalence relation on $X'$ by $x \sim y$ if $cl(\{x\}) = cl(\{y\})$, and define a pregeometry on the quotient set $X'/\sim$ by 

$$\widehat{cl}(A) \coloneqq \{[b]: b \in cl(A)\}$$ 

where $[b]$ denotes the equivalence class of $b$. This abstracts the process of taking a projectivization of a vector space. 
=-- 

### Minimal and strongly minimal sets 

We'll suppose for now that $\mathbf{L}$ is a countable [[signature (in logic)|signature]], so that the [[first-order language|language]] it generates consists of countably many formulas. Let $\mathbf{M}$ be an $\mathbf{L}$-structure, with underlying set $M$. 

+-- {: .num_defn} 
###### Definition 
For $A \subseteq M$, an element $b \in M$ is **algebraic** over $A$ if there is a formula $\phi(y, w_1, \ldots, w_n)$ and elements $a_1, \ldots, a_n \in A$ such that $\mathbf{M} \models \phi(b, a_1, \ldots, a_n)$ and 

$$\{c \in M: \mathbf{M} \models \phi(c, a_1, \ldots, a_n)\}$$ 

is finite. The **algebraic closure** of $A$, denoted $acl(A)$, is the set of elements of $M$ that are algebraic over $A$. 
=-- 

+-- {: .num_prop #finclos} 
###### Proposition 
The algebraic closure $A \mapsto acl(A)$ defines a finitary closure operator on $M$. 
=-- 

+-- {: .proof} 
###### Proof 
That $acl$ is monotone (preserves order) is obvious. Also the fact that $acl$ is finitary is easy: given that $b \in acl(A)$ satisfies $\mathbf{M} \models \phi(b, a_1, \ldots, a_n)$ for $a_1, \ldots, a_n \in A$, then similarly $b \in acl(A_0)$ for $A_0 = \{a_1, \ldots, a_n\}$. 

Taking $\phi(y, w)$ to be the equality predicate $y = w$, we see $A \subseteq acl(A)$. 

For idempotence of $acl$, suppose $b_1, \ldots, b_k \in acl(A)$ and $\mathbf{M} \models \psi(c, b_1, \ldots, b_k)$ where $\{y \in M: \mathbf{M} \models \psi(y, b_1, \ldots, b_k)\}$ has exactly $m$ elements. Write down a formula $F_{m, \psi}(x_1, \ldots, x_k)$ that says $\{y \in M: \mathbf{M} \models \psi(y, x_1, \ldots, x_k)\}$ has at most $m$ elements (by adding some extra inequalities, we can make this "exactly $m$ elements"): 

$$F_{m, \psi}(x_1, \ldots, x_k) \coloneqq \exists_{y_1, \ldots, y_m} \forall_y \psi(y, x_1, \ldots, x_k) \Leftrightarrow (y = y_1) \vee \ldots \vee (y = y_m).$$ 

Now for $i = 1, \ldots, k$, let $\phi_i$ be a formula witnessing $b_i \in acl(A)$, i.e., $\mathbf{M} \models \phi_i(b_i, a_{i, 1}, \ldots, a_{i, n_i})$ where $a_{i, k} \in A$ and $\{x \in M: \mathbf{M} \models \phi_i(x, a_{i, 1}, \ldots, a_{i, n_i})\}$ has finitely many elements. Then 

$$\exists_{x_1, \ldots, x_k} F_{m, \psi}(x_1, \ldots, x_k) \wedge \psi(y, x_1, \ldots, x_k) \wedge \bigwedge_{i=1}^k \phi_i(x_i, a_{i, 1}, \ldots, a_{i, n_i})$$ 

is a formula with parameters in $A$ that witnesses $c \in acl(A)$. This proves the idempotence of $acl$. 
=-- 

As before, this notion of algebraic closure $acl: P(M) \to P(M)$ can be restricted to a closure operator $acl^X: P(X) \to P(X)$ for a subset $X \subseteq M$, via the definition $acl^X(A) \coloneqq X \cap acl(A)$ for $A \subseteq X$. One often writes just $acl$ instead of $acl^X$, provided that $X$ is understood. 

+-- {: .num_defn} 
###### Definitions 
For an $\mathbf{L}$-structure $\mathbf{M}$, let $D \subseteq M^n$ be definable. $D$ is **minimal** if the only definable subsets of $D$ are finite or cofinite in $D$. Slightly abusing language, if $\phi(x_1, \ldots, x_n, a_1, \ldots, a_k)$ is a formula with parameters that defines $D$, we also say $\phi$ is minimal. We say $D$ (or $\phi$) is **strongly minimal** if it is minimal in any elementary extension of $\mathbf{M}$. 

A theory $\mathbf{T}$ is _strongly minimal_ if for any model $\mathbf{M}$ of $\mathbf{T}$, the underlying set $M$ (definable by the formula $x = x$) is strongly minimal. 
=-- 

+-- {: .num_example} 
###### Examples 
1. Let $K$ be an algebraically closed field. (Elimination of quantifiers, Chevalley's theorem, etc.) Conclusion: ACF is a strongly minimal theory. 

1. Divisible torsionfree abelian groups. 

1. Non-example of dense linear orders. 

=-- 

+-- {: .num_theorem} 
###### Theorem 
**(Baldwin, Lachlan)** 
The algebraic closure operator on a minimal set $X$ is a pregeometry. 
=-- 

+-- {: .proof}  
###### Proof 
Let $A \subseteq X$ and suppose $c \in acl(A \cup \{b\}) - acl(A)$ for $b, c \in X$; we want to show $b \in acl(A \cup \{c\})$. Thus, suppose $\phi(c, b)$ is a formula with parameters from $A$ such that $\mathbf{M} \models \phi(c, b)$ and $card(\{x \in X: \mathbf{M} \models \phi(x, b)\}) = n$, a finite number. As in the proof of Proposition \ref{finclos}, let $\psi(w)$ be a formula that says $card(\{x \in X: \mathbf{M} \models \phi(x, w)\}) = n$. This is a formula with parameters from $A$ and $\psi(b)$ is satisfied in $\mathbf{M}$. 

If $\{y \in X: \mathbf{M} \models \phi(c, y) \wedge \psi(y)\}$ is finite, then since $b$ belongs to this set, $\phi(c, y) \wedge \psi(y)$ would witness $b \in acl(A \cup \{c\})$ and we would be done. So suppose otherwise. Then this set is cofinite in $X$, so that 

$$card(X - \{y \in X: \mathbf{M} \models \phi(c, y) \wedge \psi(y)\}) = m$$ 

for some finite $m$, and we can again write down a formula $\chi(x)$ with parameters from $A$ that says 

$$card(X - \{y \in X: \mathbf{M} \models \phi(x, y) \wedge \psi(y)\}) = m.$$

If $\chi(x)$ defines a finite subset of $X$, then since $\chi(c)$ is satisfied, we would reach the conclusion that $c \in acl(A)$, a contradiction. Hence $\chi(x)$ defines a subset cofinite in $X$. We may therefore choose $n+1$ elements $a_1, \ldots, a_{n+1} \in X$ such that $\chi(a_i)$ is satisfied. By our supposition, 

$$B_i \coloneqq \{u \in X: \mathbf{M} \models \phi(a_i, u) \wedge \psi(u)\}$$ 

is cofinite for $i = 1, \ldots, n+1$. Hence $\bigcap_{i=1}^{n+1} B_i$ is inhabited, say by an element $b'$. We have at least $n+1$ elements $x \in X$ such that $\phi(x, b')$ is satisfied, namely $x = a_1, \ldots, a_{n+1}$. But now this contradicts the fact $\psi(b')$. 
=-- 

=-- 

## Related concepts

* [[stability in model theory]]

* [[Zariski geometry]] 

* [[matroid]] 


## References

* Anand Pillay, _Geometric stability theory_, Oxford Logic Guides __32__
* slides from conference "[Geometric model theory](http://www.maths.ox.ac.uk/events/borisfest)", Oxford 2010: directory [html](http://people.maths.ox.ac.uk/bays/misc/borisfest/notes)
* Misha Gavrilovich, _Model theory of universal covering space of complex algebraic varieties_, thesis, [pdf](http://people.maths.ox.ac.uk/bays/misha-thesis.pdf) 

* [[Boris Zilber]], _Elements of Geometric Stability Theory_, 2003 ([pdf](http://people.maths.ox.ac.uk/zilber/est.pdf))

[^fine]: Although oddly enough, as explained at the [MacTutor biography page](http://www-history.mcs.st-andrews.ac.uk/Biographies/Steinitz.html), what is called the Steinitz exchange condition was set out by Ernst Steinitz in a 1913 publication on convergent series and apparently not (?), as might be supposed, in his _Algebraische Theorie der K&#246;rper_ (Crelle's Journal, 1910). His 1913 lemma was for _vector spaces_. 