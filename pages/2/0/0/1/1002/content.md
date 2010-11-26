# Ultrafilters
* table of contents
{: toc}


## Definitions

An __ultrafilter__ on a set $S$ is a collection $F$ of [[subset]]s of $S$ satisfying the axiom
$$ A \in F \;\Leftrightarrow\; \forall (B_1, \ldots, B_n \in F),\; \exists (x \in A \cap B_1 \cap \cdots \cap B_n) .$$
This is the only axiom necessary; from this, you can prove that $F$ is a [[filter]].

Using [[excluded middle]], it is equivalent to say that a filter $F$ is an ultrafilter if, given any subset $A$ of $S$, either $A$ or its complement belongs to $F$.  This version generalises to any [[Boolean algebra]].  Another way to define an ultrafilter _in_ a Boolean algebra $L$ is as a Boolean-algebra homomorphism from $L$ to the set $\{\bot,\top\}$ of Boolean [[truth value]]s. In particular, an ultrafilter _on_ a set $X$ is the same as an ultrafilter _in_ the Boolean algebra $P X$ (the power set). 

More generally, we can define an __ultrafilter__ in any [[partial order|poset]] to be a proper [[filter]] that is maximal among proper filters.  In a distributive [[lattice]], every ultrafilter is prime; the converse holds in a Boolean lattice.

Given an element $x$ of $S$, the __principal__ (or __fixed__) __ultrafilter__ (on $S$) at $x$ consists of every subset of $S$ to which $x$ belongs.  In contrast, if $F$ is an ultrafilter on $S$ such that the intersection of the elements of $F$ is [[empty set|empty]], then we call $F$ a __free ultrafilter__.  It is possible, if one denies the [[axiom of choice]], that every ultrafilter of subsets is principal.  In contrast, the [[ultrafilter theorem]] (a weak consequence of the axiom of choice) states that any proper filter (in a Boolean lattice) may be extended to a maximal filter.

Free ultrafilters are important in [[nonstandard analysis]] and [[model theory]], where the ultrafilter theorem seems to be a necessity.


## Category-theoretic idea

(This is [[Todd Trimble]]'s [description](http://dialinf.wordpress.com/2009/01/21/ultraproducts-the-category-theoretic-way/) of [[Lawvere]]'s idea.)

Let $3$ denote a $3$-element set, say $\{0, 1, 2\}$. Let $M = hom(3, 3)$ be the $27$-element monoid consisting of functions from $3$ to $3$, with composition of functions playing the role of monoid multiplication. Then for any set $X$, $M$ acts naturally on $hom(X, 3)$, abbreviated here to $3^X$. Thus $3^X$ lives in the category $M$-Set. The set $3 = 3^1$ in particular carries a structure of $M$-set.

So, the map $X \mapsto 3^X$ defines a functor $Set \to (M-Set)^{op}$. This functor is left adjoint to a functor $(M-Set)^{op} \to Set$ which sends an $M$-set $Y$ to $hom_M(Y, 3)$, the set of functions $Y \to 3$ which respect the $M$-actions. Then, it turns out that the set of ultrafilters on $X$ can be naturally identified with the set $hom_M(3^X, 3)$, and the principal ultrafilter map

$$
X \to hom_M(3^X, 3)
$$

is again the unit of the adjunction. [The object $3$ plays a dual role, both as set and as $M$-set, and the adjunction we speak of here is based on this ambimorphicity of $3$. This is parallel to the ambimorphic nature of $2$ seen as set or as Boolean algebra.]

One can play a similar game, replacing $3$ by any set $A$, replacing $hom(3, 3)$, by $hom(A, A)$, etc. The monad of the adjunction would then be $hom_{A^A} (A^X, A)$. If $A$ is finite and greater than $2$, this monad is again the ultrafilter monad.

Lawvere seemed to be interested in formulating "large cardinal hypotheses" in terms of obstructions to nice duality statements for these and similar monads, where "nice" would mean here that the unit

$$
X \to hom_{A^A} (A^X, A)
$$

is an isomorphism. Again, if $A \gt 2$ is finite, and assuming the axiom of choice, this niceness is obstructed by the existence of infinite sets $X$. But if we take $A$ to be larger, let us say the set of natural numbers $\mathbb{N}$, the existence of obstructions to this niceness then becomes tantamount to the existence of measurable cardinals. Lawvere cites one or two more examples of this phenomenon, of a more topological nature. 


## The ultrafilter monad

For any set $X$, let $U X$ be the set of ultrafilters on $X$.  Principal ultrafilters provide an inclusion $\eta\colon X\to U X$, which turns out to be the unit of a [[monad]] on $Set$.  The multiplication can be described fairly explicitly.  First of all, if $A\subseteq X$, define $[A]\subseteq U X$ to be the set of all ultrafilters containing $A$.  Then $\mathcal{F} \in U U X$, i.e. an ultrafilter of ultrafilters, we let $\mu(\mathcal{F}) = \{ A | [A] \in \mathcal{F} \}$; one can verify that this is an ultrafilter and makes $U$ into a monad. This monad is traditionally denoted $\beta$. 

A theorem due to Ernest Manes is that the [[Eilenberg-Moore category]] of this monad is the category of [[compact Hausdorff spaces]] with its obvious forgetful functor to $Set$. In one direction, if $X$ is a compact Hausdorff space, then the corresponding algebra structure 

$$\xi: \beta X \to X$$ 

sends an ultrafilter $F$ on $X$ to the unique point in $X$ to which $F$ converges. 

(To be continued.) 

In particular, $\beta X$ can be equipped with a compact Hausdorff topology which is the free compact Hausdorff space generated by $X$, or equivalently the [[Stone-∞ech compactification]] of the [[discrete topology]] on $X$.

The monad $\beta$ also extends to the [[bicategory]] $Rel$ of sets and binary [[relations]].  It was observed by Barr that the [[generalized multicategories]] defined relative to this extension can be identified with arbitrary [[topological spaces]].  Thus, compact Hausdorff spaces are to topological spaces as monoidal categories are to multicategories. 

By exploiting the connection between monads and [[algebraic theory|algebraic theories]], it is possible to define a **compact Hausdorff object** in any category $C$ with small products, as a product-preserving functor 

$$Kl(\beta)^{op} \to C$$ 

where $Kl(\beta)$ is the Kleisli category (or the full category of compact Hausdorff spaces whose objects are of the form $\beta S$). 


[[!redirects principal ultrafilter]]
[[!redirects fixed ultrafilter]]
[[!redirects free ultrafilter]]
[[!redirects ultrafilters]]
[[!redirects principal ultrafilters]]
[[!redirects fixed ultrafilters]]
[[!redirects free ultrafilters]]
[[!redirects ultrafilter monad]]
