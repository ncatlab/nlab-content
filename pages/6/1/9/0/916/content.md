
# Partial functions
* table of contents
{: toc}

## Idea

A _partial function_ $f: A \to B$ is like a [[function]] from $A$ to $B$ except that $f(x)$ may not be defined for every element $x$ of $A$.  (Compare a [[multi-valued function]], where $f(x)$ may have several possible values.)

In some fields (including secondary-school mathematics even today), functions are often considered to be partial by default, requiring one to specify a _total_ function otherwise.  As category-theoretic and type-theoretic formalisation spreads, this is difficult to treat as the basic concept, and the most modern idea is that a function must be total.  If you want partial functions, then you can get them in terms of total functions as below.


## Definitions

### In type theory

#### As functions

In [[dependent type theory]], given [[h-sets]] $A$ and $B$, a **partial function** $f$ from $A$ to $B$ is an [[h-proposition]]-valued type family $P_f$ on $A$ which states whether $f$ is defined for element $a:A$, and a section

$$x:A, p:P_f \vdash f:B$$

If the dependent type theory has [[function types]] and [[dependent sum types]], then one could define the partial function directly as:

$$f:\left(\sum_{a:A} P_f(a)\right) \to B$$

#### As partial anafunctions

In [[dependent type theory]], given types $A$ and $B$, a **partial anafunction** is a [[type family]] $x\colon A, y \colon B \vdash R(x, y) \; \mathrm{type}$ which comes with a family of witnesses 
$$x \colon A \vdash p(x) \colon \mathrm{isProp}\left(\sum_{y:B} R(x, y) \right)$$
that for each [[term|element]] $x\colon A$, the [[dependent sum type]] $\sum_{y \colon B} R(x, y)$ is a [[mere proposition]].

Historically, partial anafunctions are called *[[functional relations]]*, but nowadays in type theory one tends to use the term *[[relation]]* only for those [[type families]] which are valued in [[mere propositions]]. 

For any partial anafunction, there is a partial function 
$$x:A, p:\mathrm{isContr}\left(\sum_{y:B} R(x, y) \right) \vdash f(x, p):B$$

which could be written as the function
$$f:\sum_{x:A} \mathrm{isContr}\left(\sum_{y:B} R(x, y) \right) \to B$$

since $\sum_{y:B} R(x, y)$ is already a proposition, one could simply use
$$x:A, p:\sum_{y:B} R(x, y) \vdash f(x, p):B$$
instead, and by the rules of dependent sum types, it becomes 
$$x:A, y:B, p:R(x, y) \vdash f(x, y, p):B$$

on the other side, the function can be written as
$$f:\left(\sum_{x:A} \sum_{y:B} R(x, y) \right) \to B$$

#### Examples

There are multiple examples of partial functions in mathematics. 

The [[reciprocal function]] on the [[real numbers]] is only defined on the real numbers apart from zero, and so is given by the following rules:

$$\frac{\Gamma \vdash \mathbb{R} \; \mathrm{type}}{\Gamma, x:\mathbb{R}, p:\vert x \vert \gt 0 \vdash {(-)}^{-1}:\mathbb{R}}$$

$$\frac{\Gamma \vdash \mathbb{R} \; \mathrm{type}}{\Gamma, x:\mathbb{R}, p:\vert x \vert \gt 0 \vdash \mathrm{recipax}:x \cdot {(x, p)}^{-1} =_\mathbb{R} 1}$$

The reciprocal function is given by the partial anafunction $x \cdot y =_\mathbb{R} 1$. 

Another example is the [[metric square root]] on the [[real numbers]], which is only defined on the non-negative real numbers, and is given by the following rules:

$$\frac{\Gamma \vdash \mathbb{R} \; \mathrm{type}}{\Gamma, x:\mathbb{R}, p:x \geq 0 \vdash \sqrt{-}:\mathbb{R}}$$

$$\frac{\Gamma \vdash \mathbb{R} \; \mathrm{type}}{\Gamma, x:\mathbb{R}, p:x \geq 0 \vdash \mathrm{sqrtax}:\sqrt{x, p}^2 =_\mathbb{R} x}$$

In both cases, the witness $p$ is usually left implicit in informal notation, and the partial function is written as ${x}^{-1}$ or $\sqrt{x}$. 

### In category theory

#### In the category of sets
 {#DefinitionInSets}

Given [[set]]s $A$ and $B$, a __partial function__ $f$ from $A$ to $B$ consists a [[subset]] $D$ of $A$ and a (total) function from $D$ to $B$.  In more detail, this is a [[span]]
$$ \array {
  &                & D \\
  & \swarrow_\iota &   & \searrow^f \\
A &                &   &            & B \\
} $$
of total functions, where $\iota: D \to A$ is an [[injection]].  (This condition can be dropped to define a partial [[multi-valued function]], which is simply a span.)

$A$ and $B$ are called the _[[source]]_ and _[[target]]_ of $f$ as usual; then $D$ is the __domain__ of $f$ and $\iota: D \to A $ is the __inclusion__ of the domain into the source.  By abuse of notation, the partial function $f$ is conflated with the (total) function $f: D \to B$.

Notice that the induced function $D \to A \times B$ is an [[injection]], so a partial function is the same as a [[functional relation]] seen from a different point of view.

We consider two partial functions (with the same given source and target) to be __equal__ if there is a [[bijection]] between their domains that makes the obvious diagrams commute.  You can get this automatically in a traditional set theory by requiring $D$ to be literally a [[subset]] of $A$ (with $\iota$ the inclusion map).


#### General abstract
 {#DefinitionGeneralAbstract}

##### In terms of spans

If $C$ is a [[category]] with [[pullbacks]], then a **partial map** from $a$ to $b$ may be defined to be a [[span]] 

$$\array{
 & & D & & \\
 & ^\mathllap{i} \swarrow & & \searrow^\mathrlap{f} & \\
A & & & & B
}$$ 
 
where $i$ is [[monomorphism|monic]]. Such spans are closed under span composition, and as a [[locally full sub-2-category]] of $Span(C)$, the bicategory of partial maps in $C$ is locally preordered. In more down-to-earth terms, if $(i, f)$ and $(i', f')$ are partial maps from $a$ to $b$, we have $(i, f) \leq (i', f')$ if there exists (necessarily monic) $j$ such that $i = i' \circ j$ and $f = f' \circ j$. 

Abstract bicategories of partial maps, parallel to [[bicategory of relations|bicategories of relations]], were introduced by ([Carboni 87](#Carb87)). 


##### In terms of the maybe monad

Notice that a partial function $f$ from $A$ to $B$ as [above](#DefinitionInSets) is (in [[classical mathematics]]) equivalently a genuine function from $A$ to the [[disjoint union]] ([[coproduct]]) of $B$ with the point (the singleton)

$$
  \phi \;\colon\; A \longrightarrow B \coprod \ast
  \,.
$$

The [[subset]] $D \hookrightarrow A$ in the [above](#DefinitionInSets) is the [[preimage]] $\phi^*(B)$; for $x$ in this preimage, $f(x) = \phi(x)$.  Conversely, an element $x \in A$ is sent to $\ast$ by $\phi$ if and only if $f$ is undefined at $x$.

This in turn is equivalently a morphism in the [[Kleisli category]] of the [[maybe monad]]. Phrased this way, the concept of partial function makes sense in any [[category]] with [[coproducts]] and with a [[terminal object]]. It comes out as intended when the category is an [[extensive category]] (partial functions with complemented domain).


## Examples

In secondary-school mathematics, one often makes functions partial by fiat, just to see if students can calculate the domains of composite functions and the like.  This is not (only) busywork, as in applications one often has a function given by a formula that is really valid only on a certain domain.  However, in more sophisticated analyses (such as those that Lawvere and his followers propose for physics and synthetic geometry), these domains and the total functions on them become the primary objects of study, with the partial functions being secondary (as $\iota$ is seen as merely a way to place _coordinates_ on $D$).

In analysis, one often considers partial functions whose domains are required to be intervals in the real line, regions of the complex plane, or dense subsets of a [[Banach space]].

In a [[field]], the multiplicative [[inverse]] is a partial function whose domain is the set of non-zero elements of the field.


## The category of sets and partial functions

The [[category]] $Set_part$ of sets and partial functions between them is important for understanding computation.  However, one often replaces this with an [[equivalence of categories|equivalent]] category of sets and total functions.

Specifically, replace each set $S$ with the set $S_\bot$ of all [[subset]]s of $S$ with at most one element, otherwise known as the [[partial map classifier]] of [[Set]].  In this context, we identify an element $x$ of $S$ with the subset $\{x\}$ and write the [[empty set|empty]] subset as $\bot$.  Then a partial function $S \to T$ becomes a total function $S_\bot \to T_\bot$ such that [[inhabited set|inhabited]] subsets of $T$ are assigned only to inhabited subsets of $S$.  Then $Set_part$ is equivalent to the category $Set_\bot$ of such sets and functions.

In [[classical mathematics]] $S_\bot \cong S \amalg \{\bot\}$, although this is not true [[constructive mathematics|constructively]].  In this case, $S\mapsto S \amalg \{\bot\}$ is the [[maybe monad]] and $Set_\bot$ is its [[Kleisli category]].  Moreover, since every algebra for this monad is [[free algebra|free]] this category is also equivalent to its [[Eilenberg-Moore category]], which is the category $Set_*$ of [[pointed set]]s and total point-preserving functions.  Traditionally, one uses the notation of $Set_\bot$ but (unless one is a constructivist) thinks of this as simply different notation for $Set_*$.  It is still true constructively that $S\mapsto S_\bot$ is a monad (the [[partial map classifier]]) and $Set_\bot$ is its Kleisli category, but it is (probably) no longer true that every algebra is free.

For a more sophisticated analysis of computation, $Set_\bot$ can be replaced with a suitable category of domains, such as [[direction|directed]] [[complete lattice|complete]] [[partial order|partially ordered]] sets (DCPOs).  The requirement that $\bot$ be preserved can then be removed to model lazy computation, but now we are hardly talking about partial functions anymore.


## Algebras of partial functions

The functions of high-school mathematics, consisting of real (or complex)-valued functions of one (or two or three) real (or complex) variables, are by default partial functions.  As they take values in a [[field]], one may consider adding or multiplying them.  The usual rule is that $\dom(f + g) = \dom f \cap \dom g$, etc, but this leads to an unusual algebra: a commutative [[semiring]] in which addition has an identity element (the always-defined constant [[zero function]]) and multiplication has an absorbing element (the never-defined [[empty function]]), but it fails to be a [[rig]] because these two elements are not the same.  It has many other interesting properties, such as simultaneous additive and multiplicative [[idempotent element|idempotents]] (the zero functions with arbitrary domains).

An axiomatic treatment of such semirings may be found at the end of [Richman 2012](#Richman12), as well as in the article [[category of partial endofunctions]].

## Related concepts

* [[total function]]
* [[restriction category]]
* [[category of partial endofunctions]]
* [[partial function type]]
* [[multivalued partial function]]

## References 
 {#References}

* {#Carb87} [[Aurelio Carboni]], Bicategories of partial maps, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 28 no. 2 (1987), p. 111-126 ([web](http://www.numdam.org/item?id=CTGDC_1987__28_2_111_0))

* [[Robin Cockett]], [[Steve Lack]], _Restriction categories I: categories of partial maps_ ([pdf](http://pages.cpsc.ucalgary.ca/~robin/FMCS/FMCS_06/RestrictionsI.pdf))

* [[Robin Cockett]], [[Steve Lack]], _Restriction categories II: partial map classification_ ([web](http://maths.mq.edu.au/~slack/papers/restii.html))

* [[Robin Cockett]], [[Steve Lack]], _Restriction categories III: colimits, partial limits, and extensivity_ ([arXiv:math/0610500](http://arxiv.org/abs/math/0610500))

* {#Richman12} [[Fred Richman]], *Algebraic functions, calculus style*. Communications in Algebra, Volume 40, Issue 7, July 2012, Pages 2671-2683 &lbrack;[doi:10.1080/00927872.2011.584337](https://doi.org/10.1080/00927872.2011.584337)&rbrack;

For an alternative to [[restriction categories]] as a category-theoretic framework for partial maps:

* Marcello Lanfranchi, [[Jean-Simon Pacaud Lemay]], *Local categories: a new framework for partiality* &lbrack;[arXiv:2512.03371](https://arxiv.org/abs/2512.03371)&rbrack;



[[!redirects partial function]]
[[!redirects partial functions]]
[[!redirects partially defined function]]
[[!redirects partially defined functions]]
[[!redirects partially-defined function]]
[[!redirects partially-defined functions]]

[[!redirects partial map]]
[[!redirects partial maps]]

[[!redirects partial morphism]]
[[!redirects partial morphisms]]

[[!redirects partial anafunction]]
[[!redirects partial anafunctions]]
