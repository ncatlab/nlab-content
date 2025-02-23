
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents 
* table of contents 
{: toc} 

## Idea 

A _fixed point_ (or _fixpoint_) of an [[endofunction]] $f \colon X \to X$ is an [[element]] $x \in X$ such that $f(x) = x$. 

More generally, if $C$ is a [[category]] with a [[terminal object]] $1$ and an [[endomorphism]] $f \colon X \to X$, then a fixed point of $f$ is an element $x \colon 1 \to X$ such that $f \circ x = x$. More generally still, we can speak of the same notion but replacing global elements $x \colon 1 \to X$ by [[generalized elements]] $x \colon U \to X$, where again $x$ is a fixed point of $f \colon X \to X$ if $f \circ x = x$. 

Fixed points are also called _[[invariants]]_, in particular if they are joint fixed points of all the operations in a given [[monoid]] or [[group]].

Such fixed points we discuss below in

* _[Examples in analysis and topology](#ExamplesInAnalysisAndTopology)_

* _[Examples for ordered sets](#ExamplesForOrderedSets)_

* _[Examples in Set theory](#ExamplesInSetTheory)_

The importance of fixed points all throughout mathematics is difficult to overstate. They are particularly important in [[analysis]], [[topology]], [[lattice]] theory, set theory, and category theory. Fixed points of endofunctors frequently arise as solutions to "recursive equations", especially in the form of [[initial algebra of an endofunctor|initial algebras and terminal coalgebras]]. 


In [[category theory]] the concept of fixed points admits [[categorification]]: For example, if $F \colon C \to C$ is an [[endofunctor]], then an object $c$ of $C$ is called a "fixed point of the endofunctor" $F$ is there is an [[isomorphism]] $F(c) \cong c$ (although usually, a fixed point of a functor is an object together with a specified such isomorphism). These fixed points for endofunctors we discuss below in 

* _[Fixed points of an endofunctor](#ExamplesInCategoryTheory)_

See also at

* _[[fixed point of an adjunction]]_ (which in particular restricts to a concept of fixed points of a [[Galois correspondence]])

In [[homotopy theory]] the concept of fixed point becomes that of

* _[[homotopy fixed point]]_

In [[stable homotopy theory]] it becomes the concept of

* _[[fixed point spectrum]]_

For further occurences in [[logic]] see also

* _[[fixed-point combinator]]_

* _[[Lawvere's fixed point theorem]]_



## Examples in analysis and topology 
 {#ExamplesInAnalysisAndTopology}

A typical application of fixed points in analysis is through the following general theorem: 

+-- {: .num_theorem} 
###### Theorem 
Suppose $X$ is an (inhabited) [[complete metric space]] with distance function $d$ and $f \colon X \to X$ is a function with Lipschitz constant $r$ strictly less than $1$, i.e., $d(f(x), f(y)) \leq r \cdot d(x, y)$ for all $x, y \in X$. Then $f$ has a unique fixed point. 
=-- 

The proof is very easy: starting with an initial point $x_0$, the [[sequence]] defined by $x_{n+1} = f(x_n)$ is readily seen to be a [[Cauchy sequence]] which converges to some point $x$. The sequence $x_{n+1} = f(x_n)$ converges to both $x$ and $f(x)$, so $x = f(x)$. If $x$ and $y$ are fixed points, then $0 \leq d(x, y) = d(f(x), f(y)) \leq r \cdot d(x, y)$, so 

$$(1-r)d(x, y) \leq 0$$ 

whence $0 \leq d(x, y) \leq 0$ and therefore $x = y$.  

By a suitable choice of space $X$ and endomorphism $f$, this theorem can be used to establish existence and uniqueness of solutions of differential equations (this should be expanded upon). 

In the case where $X$ is compact, we may weaken the condition $d(f(x), f(y)) \leq r d(x, y)$ for some uniform $r \lt 1$, to merely $d(f(x), f(y)) \lt d(x, y)$ whenever $x \neq y$. To see this, use compactness to show that $d(x, f(x))$ attains a minimum value at some $x_0$. Then $f(x_0) = x_0$, else $d(f(x_0), f(f(x_0))) \lt d(x_0, f(x_0))$. Hence there exists at least one fixed point, and only one since if $x_0, y_0$ are different fixed points, then $d(x_0, y_0) = d(f(x_0), f(y_0)) \lt d(x_0, y_0)$. 

* [[Banach fixed point theorem]]

* [[Brouwer's fixed point theorem]]

* Schauder 

* Kakutani 

* Tychonoff 

* Lefschetz 

* Atiyah-Singer; Wood's Hole 

## Examples for ordered sets 
 {#ExamplesForOrderedSets}

### Knaster-Tarski theorem 

+-- {: .num_theorem} 
###### Theorem 

If $L$ is a [[complete lattice]], then every monotone (i.e., order-preserving) map $f \colon L \to L$ has a fixed point (in fact, the fixed points of $f$ form a complete lattice). 

=-- 

+-- {: .proof} 
###### Proof 
The [[algebra of an endofunctor|algebras]] for the functor $f \colon L \to L$ are elements $x$ such that $f(x) \leq x$. Limits in $Alg(L)$ are preserved and reflected by the forgetful functor or inclusion $Alg(L) \to L$, hence $Alg(L)$ is complete if $L$ is. In particular, $Alg(L)$ has an initial object, and initial algebras are fixed points. 

(In more down-to-earth terms, let $t$ be the infimum of $A = \{x: f(x) \leq x\}$. Then for every $x \in A$, we have $f(t) \leq f(x) \leq x$, hence $f(t) \leq t$. We therefore also have $f(f(t)) \leq f(t)$, so that $f(t) \in A$. But then it follows that $t \leq f(t)$, whence $t = f(t)$. Clearly this $t$ is a least fixed point of $f$.) 

To show completeness of $fix(f)$, suppose given $S \subseteq fix(f)$, and let $s$ be the supremum of $S$ in $L$. Then the principal upward-closed set $s \uparrow$ generated by $s$ is a complete lattice. Also, $f$ restricts to a map $s \uparrow \to s \uparrow$ (for if $s \leq x$, then $p \leq x$ for all $p \in S$, whence $p = f(p) \leq f(x)$ for all $p \in S$, so that $s \leq f(x)$). The least fixed point of $f: s \uparrow \to s \uparrow$ is the supremum of $S$ in $fix(f)$. 
=-- 

A virtual corollary of this theorem is the [[Cantor-Schroeder-Bernstein theorem]]. 


### Pataraia's theorem 

The following significantly strengthens the [[Knaster-Tarski theorem]], and is based on the notion of an **ipo** (inductive partial order; see Paul Taylor's book), i.e., a poset with a bottom element and admitting joins of [[direction|directed subsets]]. 

\begin{theorem}
**(Pataraia)**
\linebreak
If $L$ is an ipo, then every monotone map $f \colon L \to L$ has a (least) fixed point. 
\end{theorem}

+-- {: .proof}
###### Proof 
Consider the smallest $S$ among subsets of $L$ which contain $\bot$, are closed under $f$, and closed under directed joins in $L$. Then the restriction $f \colon S \to S$ satisfies $1_S \leq f$, i.e., $f$ is _inflationary_. (For the set of all elements $x \in L$ such that $x \leq f(x)$ is another such subset, so $S$ is contained in it.) Thus it suffices to show that every inflationary map on a poset $S$ with a bottom element and directed joins has a fixed point. 

The collection $I$ of inflationary monotone maps on $S$ is an ipo: its bottom element is $1_S$, and directed joins are computed pointwise. Moreover, $I$ is itself directed: if $g, h \in I$, then $g \circ h \in I$ dominates them both. Thus the directed join $t$ of the collection exists; it is the maximal element $t$ of $I$. It follows that $f \circ t \leq t$, but also $t \leq f \circ t$ since $f$ is inflationary. So $f \circ t = t$, and in particular $t(\bot) \in S$ is a fixed point of $f$. 

This $t(\bot)$ is a least fixed point of $f: L \to L$. For if $x$ is any fixed point, the downward-closed set $L \downarrow x$ contains $\bot$, is closed under $f$, and is closed under [[direction|directed unions]], and therefore $S \subseteq L \downarrow x$. Hence $t(\bot) \in S$ satisfies $t(\bot) \leq x$. 
=-- 

One may mimic the last part of the proof of the Knaster-Tarski theorem to show that if $L$ is an ipo and $f$ is monotone, then $fix(f)$ (with the order inherited from $L$) is also an ipo. Indeed, we have just seen $fix(f)$ has a bottom element, and if $A \subseteq fix(f)$ is any directed subset, and $s = sup(A)$ is its sup in $L$, then we may argue as we did for the Knaster-Tarski theorem that $f$ restricts to a monotone map on the ipo $s \uparrow L$, whence by Pataraia's theorem it has a least fixed point, and this will be the sup of $A$ in $fix(f)$. 

### Galois connections 

## Examples in set theory 
 {#ExamplesInSetTheory}

* The [[identity function]] on a [[set]] $S$ is [[generalized the|the]] [[uniqueness quantifier|unique]] [[function]] on $S$ such that every element in $S$ is a [[fixed point]] of said function. 

* In at least some of the "lower" levels of the hierarchy of countable ordinals, leading up to the Feferman-Sch&#252;tte ordinal, fixed points of continuous operators on the first uncountable ordinal play a central role. More information may be found at [[countable ordinal]].  

* Critical points of elementary embeddings (non-fixed points) 

## Examples in category theory 
 {#ExamplesInCategoryTheory}

### Initial algebras and final coalgebras 

Various classical fixed-point theorems for monotone functions on posets can be "[[categorification|categorified]]" to give appropriate fixed-point theorems for [[endofunctors]] on categories. An example is that [[Kleene's fixed-point theorem]] generalizes to [[Adámek's fixed point theorem]]: 

+-- {: .num_theorem} 
###### Theorem 

Let $C$ be a [[category]] with an [[initial object]] $0$ and [[colimits]] of $\kappa$-[[directed diagrams]] for some [[regular cardinal]] $\kappa$, and suppose $F \colon C \to C$ [[preserved colimit|preserves]] $\kappa$-[[directed colimits]]. Then $F$ has an [[initial algebra]] (which by [[Lambek's theorem]] is a fixed point of $F$). 

=-- 

+-- {: .proof} 
###### Proof 

Regarding $\kappa$ as an ordinal $\{\alpha \lt \kappa\}$ (hence a poset, hence a category), define a functor $G \colon \kappa \to C$ recursively: on objects, put $G(\emptyset) = 0$, $G(\alpha + 1) = F(G(\alpha))$, and $G(\beta) = colim_{\alpha \lt \beta} G(\alpha)$ for $\beta$ a limit ordinal. On morphisms $\alpha \lt \beta$, 

* $G(\emptyset \lt \beta)$ is the unique map $0 \to G(\beta)$; 

* For $\beta$ a limit ordinal, $G(\alpha \lt \beta)$ is a component of the cocone diagram that defines $G(\beta)$ as a colimit; 

* $G(\alpha + 1 \lt \beta + 1) = F(G(\alpha \lt \beta))$; 

* For $\alpha$ a limit ordinal, $G(\alpha \lt \beta + 1)$ is the unique map $colim_{\gamma \lt \alpha} G(\gamma) \to G(\beta +1)$ corresponding to the cocone from the diagram $G| \colon \alpha \to C$ to $G(\beta+1)$. 

By assumption, $colim G$ exists in $C$, and this colimit is preserved by $F$. Thus we have an isomorphism $F(colim G) \cong colim G$, affording an $F$-algebra structure on $colim G$. If $(x, \theta: F(x) \to x)$ is any algebra, then we define a cocone from $G$ to $x$ whose component at successor stages $\alpha + 1$ is defined recursively as an evident composite 

$$G(\alpha + 1) = F(G(\alpha)) \to F(x) \stackrel{\theta}{\to} x,$$ 

and whose component at limit stages $\alpha$ is the unique map $G(\alpha) \to x$ out of the colimit that is compatible with previous components $G(\beta) \to x$, for $\beta \lt \alpha$. It is readily seen that the map $colim G \to x$, uniquely determined from the cocone $G \to x$, is the only possible algebra map. 
=-- 

A typical application is where $C$ is a $\kappa$-accessible category and $F \colon C \to C$ is a $\kappa$-accessible functor. A concise statement is that accessible endofunctors on accessible categories with an initial object possess categorical fixed points (in fact, the fixed points form another accessible category with an initial object). 

An arguably more elegant viewpoint on this is given in the following theorem and proof. 

+-- {: .num_theorem} 
###### Theorem 
Suppose $C$ is [[locally presentable category|locally presentable]], i.e., [[accessible category|accessible]] and [[complete category|complete]]/[[cocomplete category|cocomplete]], and suppose $F \colon C \to C$ is an [[accessible functor]]. Then the category of $F$-[[algebra of an endofunctor|algebras]] is also locally presentable. In particular, there exists an initial $F$-algebra. Moreover, the category of fixed points, i.e., the category of $F$-algebras $X$ for which the structure $F X \to X$ is an isomorphism is also locally presentable (in particular, cocomplete and complete). 
=-- 

+-- {: .proof}
###### Proof 
$Alg_F$ is an [[inserter]] construction, i.e., the data consisting of the evident 1-cell $U \colon Alg_F \to C$ and 2-cell $F \circ U \to U$ is universal among all such data in the 2-category $Cat$. Since $Acc$ is closed under 2-limits in $Cat$ such as inserters (see [Makkai-Par&#233;](#MakkaiPare), theorem 5.1.6), the category $Alg_F$ is accessible. It is also complete since $C$ is complete (being locally presentable) and the underlying functor $U \colon Alg_F \to F$ reflects limits. Since $Alg_F$ is accessible and complete, it is also cocomplete, hence contains an initial object. 

Similarly, the category of fixed points $i \colon Fix(F) \to C$ is formed as an iso-inserter construction and is therefore accessible. If $D \colon J \to Fix(F)$ is a diagram of fixed points and $c \in Ob(C)$ is the colimit of $i \circ D$, then $F$ induces a functor (which we give the same name) $F\colon c \downarrow C \to c \downarrow C$, because for any object $c \to d$ in $c \downarrow C$, we have a [[cocone]] $i \circ D \cong F \circ i \circ D \to F(d)$, factoring uniquely through an arrow $c \to F(d)$. Since $c \downarrow C$ is a locally presentable category, the accessible functor $F$ acting on it has an initial algebra $(c \to c', (c \to F(c')) \to (c \to c'))$, as we argued before. This is the colimit of $D$ in $Fix(F)$, as is easily checked. Therefore $Fix(F)$ is cocomplete and accessible. 
=-- 

Boundedness conditions, such as those given as hypotheses in the previous two theorems, are generally required to establish existence of categorical fixed points. The example of the covariant power-set functor on $Set$ shows that a naive generalization of the Knaster-Tarski theorem from complete lattices to complete/cocomplete categories is hopelessly false. 

Paul Taylor has built an elegant theory of locating certain initial algebras inside final coalgebras, via his notion of well-founded coalgebras. This too can be "categorified" (to be continued). 

### Fixed points of left exact idempotent endofunctors 

+-- {: .num_theorem} 
###### Theorem (Par&#233;, Rosebrugh, Wood) 
Let $E$ be a topos, and let $F \colon E \to E$ be a left-exact idempotent _functor_. Then the category of $F$-coalgebras $X$ whose structure maps $\theta \colon X \to F(X)$ are isomorphisms is a topos. 
=--

Here "idempotent" involves a coassociativity condition.

This theorem is a special case of a general theorem about categories of dialgebras for a [[diad]].

+-- {: .query} 
Todd: To be related to structures over a modal operator, as at my web, or to diads a la Toby Kenney. 
=-- 


## Related concepts

* [[fixed point of an adjunction]], 

  including fixed points of [[Galois correspondences]]

* [[fixed point space]]

* [[fixed point group]]

**Theorems**

* [[Lawvere's fixed point theorem]]

* [[Lefschetz fixed point theorem]]

* [[Kleene's fixed point theorem]]

* [[Adámek's fixed point theorem]]

* [[Brouwer's fixed point theorem]]

* [[Atiyah-Bott fixed point theorem]]



## References 

* {#Hermida97} [[Claudio Hermida]], [[Bart Jacobs]], _Structural induction and coinduction in a fibrational setting_, Information and Computation 145 (1997), 107-152. ([citeseer](http://citeseer.ist.psu.edu/viewdoc/summary?doi=10.1.1.36.7400)) 

* {#MakkaiPare} [[Michael Makkai]], [[Robert Paré]], _Accessible Categories: The Foundations of Categorical Model Theory_, Contemporary Mathematics 104, AMS (1989). 

* Wikipedia, _[Fixed point (mathematics)](https://en.wikipedia.org/wiki/Fixed_point_(mathematics%29)_

A version of the Knaster-Tarski fixed-point theorem is proved in constructive (and even predicative) set theory in

* Giovanni Curi, _On Tarski's fixed point theorem_, Proc. Amer. Math. Soc. **143** (2015), 4439-4455  doi:[10.1090/proc/12569](http://dx.doi.org/10.1090/proc/12569)

as well as in [[dependent type theory]] in

* Ian Ray, *Tarski's Least Fixed Point Theorem: A Type Theoretic Formulation* ([arXiv:2401.00841](https://arxiv.org/abs/2401.00841))

A relation to [[framed manifold|framed]] [[cobordism classes]] and fixed points:

* {#Prieto03} [[Carlos Prieto]], _Fixed point theory and framed cobordism_, Topol. Methods Nonlinear Anal. Volume 21, Number 1 (2003), 155-169. ([Euclid](https://projecteuclid.org/euclid.tmna/1475266278))

* [[Robert Paré]], [[R. Rosebrugh]] and [[R. J. Wood]], _Idempotents in bicategories_, Bulletin of the Australian Mathematical Society, Vol. 39, No. 3, 1989, pp. 421-434. &lbrack;[doi:10.1017/S0004972700003336](https://doi.org/10.1017/S0004972700003336)&rbrack;

* Toby Kenney, _Diads and their Application to Topoi_, Applied Categorical Structures 17 (2009): 567-590.


[[!redirects fixed points]]


[[!redirects fixed point of the endofunctor]]
[[!redirects fixed points of the endofunctor]]



[[!redirects Knaster-Tarski theorem]]
[[!redirects Knaster-Tarski's fixed point theorem]]

