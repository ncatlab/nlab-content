


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

The **compactness theorem** is a fundamental result of _[[model theory]]_ on the existence of [[models]] of [[first-order theories]].

Historically it goes back to work of [[Gödel]] and Mal'cev in the 1930s.

[[Lindström's theorem]] uses the compactness and the [[Löwenheim-Skolem theorem]] to characterize classical first-order logic. The validity or non-validity of the compactness theorem in logical systems other than first-order logic plays under the name of _compactness property_ an important role in [[abstract model theory]].

## Theorem

Briefly, the compactness theorem states that a set of first-order formulas $\Phi$ has a model precisely iff every finite subset of $\Phi$ has a model.

### Remark

There are different proofs for the compactness theorem e.g. an entirely 'semantic' one using [[ultraproduct|ultraproducts]]. A particularly transparent one relies on the completeness theorem for first-order logic and the essential finitude of the notion of formal proof[^end]: Suppose $\Phi$ has no model, due to completeness this implies that there is a contradiction $\varphi$ with $\Phi\vdash\varphi$ but such a deduction of $\varphi$ can involve only a finite subset $\Phi_0\subset \Phi$ hence $\Phi_0\vdash\varphi$ and $\Phi_0$ would have no model as well. 

Despite the intuitive appeal, this approach obliges one to establish the completeness theorem, which depends on fiddly details of formal proofs and deductive systems to make rigorous. 

### Compactness for propositional logic 

[^end]: In the German literature the compactness theorem is therefore also called 'Endlichkeitssatz'.

The motivation for the terminology stems from the observation that the compactness theorem literally expresses the compactness of a suitable topology on first-order structures.

## Illustrations 

As the compactness theorem is arguably the most fundamental result of model theory, there are too many examples of its use for us to do it much justice here. But perhaps a few examples here will help illustrate some typical uses. 

### Total orders {#totalorder}

+-- {: .num_prop #total} 
###### Proposition 
Every set $X$ can be totally ordered. 
=-- 

Of course this trivially follows from the stronger result that every set can be [[well-ordered set|well-ordered]], if we permit the [[axiom of choice]]. But part of our point here is that we don't need the full strength of the axiom of choice: the result can be derived from the weaker "choice principle" called the [[ultrafilter theorem]], on which the compactness theorem depends. 

+-- {: .proof} 
###### Proof 
Introduce a [[language]] (i.e., [[signature (in logic)|signature]]) with a constant symbol $c_p$ for each $p \in X$ and a binary relation symbol $L$, and for a [[theory]] take axioms $\neg (c_p = c_q)$ whenever $p \neq q$ in $X$ and the usual axioms to make $L$ a [[total order]] (reflexivity, transitivity, antisymmetry, and connectedness). This theory is finitely satisfiable: any finite subset $\Sigma$ of the axioms has a model, by interpreting each $c_x$ occurring in an inequality axiom belonging to $\Sigma$ simply as $x$, and totally ordering those finitely many $x$ in some way to interpret $L$; the remaining $c_x$ can be interpreted as the bottom element of that total order without any harm. By the compactness theorem, this theory has a model $Y$, and the restriction of the total order on $Y$ to the set of all constants $c_x$ in $Y$ is used to totally order all the $x \in X$. 
=-- 

With slightly more effort, a similar argument can be given to show that every [[partial order]] can be extended to a total order. We just proved the case where the partial order is discrete. 

#### Choice-like consequences 

Again, we assume the ultrafilter principle but do not assume the [[axiom of choice]]. 

+-- {: .num_cor} 
###### Corollary 
If $p: F \to X$ is [[surjection|surjective]] and every [[fiber]] is finite, then $p$ has a section $s$. 
=-- 

+-- {: .proof} 
###### Proof 
Using Proposition \ref{total} to totally order $F$, each fiber inherits a total order that is a [[well-ordered set|well-order]] by finiteness, and we can choose $s(x)$ for $x \in X$ to be the least element in the fiber $F_x$ by nonemptiness. 
=-- 

+-- {: .num_prop #countable} 
###### Proposition 
A countable disjoint union of finite sets is again countable. 
=-- 

+--{: .proof} 
###### Proof 
Let $F_n$ be the countable family and let $F$ be the union; again we have a fibering $F \to \mathbb{N}$ with fiber $F_n$ over $n$. Using Proposition \ref{total}, totally order $F$; each $F_n$ inherits an order from $F$, and since total orders on finite sets are well-orders, we have chosen a countable family of well-orders. Now put the [[lexicographic order]] on the set of pairs $F' = \{(n, x): n \in \mathbb{N}, x \in F_n\}$. This is a well-ordering, and clearly the projection $F' \to F$ is a bijection, so we obtain a well-ordering of $F$ by transport of structure (differing, probably, from the original total ordering of $F$ which has done its job but is of no further use). Then we can define a partial map $\phi: \mathbb{N} \to F$ by induction: $\phi(0)$ is the bottom of $F$, and $\phi(n+1)$ is (if it exists) the bottom of the complement of $\phi([0, n])$. This defines a bijection from an initial segment of $\mathbb{N}$ onto $F$, which is what we wanted. 
=-- 

+-- {: .num_cor #wkl} 
###### Corollary 
**(Weak K&#246;nig's lemma)** 
Every infinite [[tree]] for which there is finite branching at each node has an infinite branch. 
=-- 

+-- {: .proof} 
###### Proof 
A tree is by definition the [[category of elements]] $e = (n, x \in F(n))$ of a [[presheaf]] $F: \mathbb{N}^{op} \to Set$ where $\mathbb{N}$ has its usual order and $F(0)$ is terminal. A *descendant* of an element $e = (n, x \in F(n))$ is an element that maps to $e$, i.e., an element $(m, y \in F(m))$ with $m \geq n$ and $F(m \geq n)(y) = x$. A *child* of $e$ is such a descendant with $m = n+1$. 

By the branching hypothesis, the set $E_n$ of elements $e = (n, x)$ is finite. 
By Proposition \ref{countable}, the set of nodes or elements $E = \sum_n E_n$ is countable, i.e., is enumerated by some bijection $\mathbb{N} \to E$. Then an infinite branch (a [[global section]] $s$ of $F$) is given by recursion as follows: $s(0)$ is the root (the unique element of $E_0$). The root has infinitely many descendants since the tree is infinite. Given that $s(n) \in F(n)$ has infinitely many descendants, let $s(n+1)$ be the first of its children in the enumeration that also has infinitely many descendants (such children exist since $s(n)$ has only finitely many children by the branching hypothesis). 
=-- 

Weak K&#246;nig's lemma lends its name to one the so-called Big Five systems of [[reverse mathematics]], namely $WKL_0$, and (over a certain weak fragment of second-order arithmetic) is equivalent to many results in classical elementary analysis.

## Related concepts

* [[Löwenheim-Skolem theorem]]

* [[Skolem's paradox]]

* [[Lindström's theorem]]

* [[Deligne completeness theorem]]

* [[Stone duality]]

## References

* Wikipedia, _[compactness theorem](https://en.wikipedia.org/wiki/Compactness_theorem)_


