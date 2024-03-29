

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

At the moment, this is a "place holder" page.  I ([[Andrew Stacey]]) want to learn about the appearance of [[algebraic theories]] in [[functional analysis]] and shall record what I learn here.  A preliminary outline is to find out about the following statements:

1. The category of [[Banach spaces]] with linear [[short maps]] is not [[monadic category|monadic]] over Set.  The "nearest" algebraic theory is that of [[totally convex spaces]].
2. The category of [[Banach algebras]] is also not algebraic.
3. The category of $C^*$-[[C-star-algebra|algebras]] is algebraic.

### Banach Spaces ###

We consider the category of [[Banach spaces]] with linear [[short maps]].  That is, this is the category $\operatorname{Ban}$ with:

* Objects: Banach spaces over $\mathbb{R}$
* Morphisms $E \to F$: Linear short maps.  That is, bounded linear transformations $T \colon E \to F$ such that $\|T\| \le 1$

We define a functor $B \colon \operatorname{Ban} \to \operatorname{Set}$ sending a Banach space to its unit ball.  Since linear short maps $E \to F$ take the unit ball of $E$ into the unit ball of $F$, this is well-defined.

There is a functor in the opposite direction which assigns to a set the "free" Banach space on that set.  That is, it assigns to a set $X$ the Banach space $\ell^1(X)$ of all absolutely summable sequences indexed by elements of $X$.  It is a standard result that such a sequence must have countable support, no matter how large $X$ is.

+-- {: .num_lemma #bspadj}
###### Lemma
$\ell^1$ is left adjoint to $B$.
=--

+-- {: .proof}
###### Proof
We need to define the adjunction natural transformations: $\eta_X \colon X \to B \ell^1(X)$ and $\epsilon_E \colon \ell^1(B E) \to E$.  The first is the map which assigns to $x$ the sequence $(\delta_{x y})$ which is $1$ at $x$ and $0$ elsewhere.  The second is the summation map which assigns to an absolutely summable sequence $(a_e)$ indexed by $e \in B E$ its sum, $\sum a_e e$.
=--

This adjunction defines a [[monad]] over $\operatorname{Set}$.  Let us spell out the details.  The functor $T \colon \operatorname{Set} \to \operatorname{Set}$ sends a set $X$ to the unit ball of $\ell^1(X)$.  That is, an element of $T(X)$ is a weighted (formal) sum of elements of $X$, $\sum a_x$, such that $\sum |a_x| \le 1$.  The unit for the monad sends an element $x \in X$ to the delta sequences in $T(X)$.  The product, $\mu$, takes a "sum of sums" and evaluates them.  That is, given a formal sum $\sum a_s$ where each $s$ is of the form $\sum s_x$, $\mu(\sum a_s) = \sum b_x$ where $b_x = \sum_s s_x$.

+-- {: .query}
AS: I think!  I need to check exactly how the product works in this example but I'm just getting the basic sketch down first.
=--

The key question is whether or not $\operatorname{Ban}$ is (equivalent to) the category of algebras for this monad.  That is, is $B \colon \operatorname{Ban} \to \operatorname{Set}$ _tripleable_?  If not (as it will turn out), how close is it?

[[Beck's tripleability theorem]] gives three conditions for a functor to be tripleable.  We already have one (the adjunction), let us show that the second also holds.

+-- {: .num_lemma #bsprefiso}
###### Lemma
$B \colon \operatorname{Ban} \to \operatorname{Set}$ reflects isomorphisms.
=--

+-- {: .proof}
###### Proof
Let $T \colon E \to F$ be a linear short map which induces an isomorphism on the unit balls of $E$ and $F$.  It is evident that it is therefore a bijection from the underlying set of $E$ to that of $F$.  Hence, by the open mapping theorem, it is a linear homeomorphism.  It remains to show that $\|T(x)\| = \|x\|$ (so that its inverse is a short map as well).  This is simple to show: if we had some $x \in E$ with $\|x\| = 1$ but $\|T(x)\| \lt 1$ (if it fails, it must fail that way as $T$ is short) then there would be some $\lambda \gt 1$ such that $\|T(\lambda x)\| \le 1$.  As $B(T) \colon B E \to B F$ is surjective, there is some $y \in B E$ such that $T(y) = T(\lambda x)$.  But as $\lambda \gt 1$, $\lambda x \notin B E$ so $\lambda x \ne y$, contradicting the injectivity of $T$. (Incidentally, this argument is valid [[constructive mathematics|constructively]]; it is a property of located [[real numbers]] that any number that is neither greater nor smaller than $1$ must equal $1$.)
=--


+-- {: .query}
AS: To be continued ...
=--


#### References: ####

The above is essentially [[Andrew Stacey|my]] "notes" on reading the following (and whatever necessary to understand the following):

Section 4.4 of _Toposes, Triples, and Theories_ by Barr and Wells ([TAC reprint](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html))


## References

* _On the equational theory of $C^*$-algebras_, Pelletier, J. Wick and Rosick&#253;, J., [MR1223636](http://www.ams.org/mathscinet-getitem?mr=1223636)
* Any more suggested by [this question on mathoverflow](http://mathoverflow.net/questions/9169/request-for-reference-banach-type-spaces-as-algebraic-theories)