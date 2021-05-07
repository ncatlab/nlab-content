
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Homotopy type theory
+--{: .hide}
[[!include homotopy type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

A preorder (also sometimes called a _[[quasi-order]]_, especially if one works with $\lt$ instead of $\leq$) is like a [[partial order]], but without the "antisymmetry" requirement that $x \leq y$ and $y \leq x$ implies $x = y$.

By interpreting the relation $\leq$ as the existence of a unique [[morphism]], preorders may be regarded as certain [[categories]] (namely, [[thin categories]]).  This category is sometimes called the _preorder category_ associated to a preorder; see below for details.


## Definition

A **preorder** on a set $S$ is a [[reflexive relation|reflexive]] and [[transitive relation|transitive]] relation, generally written $\leq$.  A **preordered set**, or **proset**, is a set equipped with a preorder.  (This should not be confused with a [[pro-set]], i.e. a [[pro-object]] in [[Set]].)

Equivalently, a proset is a (strict) [[thin category]]: a [[strict category]] such that for any pair of objects $x, y$, there is at most one morphism from $x$ to $y$.  The existence of such a morphism corresponds to the truth of the relation $x\leq y$.  In other words, it's a (strict) [[category enriched]] over the [[cartesian monoidal category]] of [[truth values]].

### In homotopy type theory

A __preorder__ $A$ in homotopy type theory consists of the following: 

* A homotopy type $A_0$, whose terms $a:A_0$ we write as $a:A$.  
* For every $a, b:A$, a proposition $p: a \leq_A b$ 
* For every $a:A$, a proposition $refl_a: a \leq_A a$ called reflexivity
* For every $a, b, c:A$, a function 
$$(a \leq_A b) \rightarrow (b \leq_A c) \rightarrow (a \leq_A c)$$
called transitivity, and denoted infix as an implication by $p \implies q \implies p \wedge q$
* For every $a,b:A$, and $p: a \leq b$ we have $p \iff refl_a \wedge p$ and $p \iff p \wedge refl_b$
* For every $a,b,c,d:A$ and $p:a\leq b$, $q:b\leq c$, $r:c\leq d$, we have $p \wedge (q \wedge r) \iff (p \wedge q) \wedge r$. 

A proposition $p:a \leq b$ is an __equivalence relation__ if there is a proposition $q:b \leq a$ such that $p \wedge q \iff refl_a$ and $q \wedge p \iff refl_b$. We write $a ~_A b$ for the type of such equivalence relation, which is also a proposition. 

The only relationship between the equivalence relation $a ~_A b$ as defined and the [[identity type]] $Id_A(a, b)$ for $a,b:A$ is that there exists a function 
$$idtoeq_{a,b}: Id_A(a,b) \rightarrow a ~_A b$$

A __preordered set__ or __proset__ is a preorder such that the type $A_0$ is [[0-truncated]], and a __partial order__ is a preorder such that for every $a,b:A$, the function $idtoeq_{a,b}$ is a homotopy equivalence. A __partially ordered set__ or __poset__ is a preordered set and a partial order. Every set is the [[core]] of a proset. 

## Properties

### Relation to partial orders

Any preordered set is [[equivalence of categories|equivalent]] to a [[partial order|poset]].  This is a special case of the theorem that every category has a [[skeleton]], but (if you define 'equivalence' weakly enough) this case does _not_ require the [[axiom of choice]].

If the [[foundations]] have [[quotient sets]], then every preorder has a quotient set equivalent to a poset. Let $(P, \leq)$ be a preorder. Define the [[equivalence relation]] $\sim$ on $P$ for all elements $a, b \in P$ as $a \sim b := (a \leq b) \wedge (b \leq a)$. Then the quotient set $P / \sim$ is a poset. This is the 0-truncated version of the fact that because every [[category object in an (infinity,1)-category|precategory]] has a [[core]] [[groupoid object in an (infinity,1)-category|pregroupoid]] and every pregroupoid has a Rezk completion into a [[groupoid]], every precategory has a Rezk completion into a [[category]]. 

### Relation to thin categories

In [[set theory|set-theoretic]] [[foundations]], a preordered set is the same as a [[thin category]] (a category in which any two parallel [[morphisms]] are equal), and it is partially ordered just when it is [[skeletal category|skeletal]].  Thus, asking for a preordered set to be partially ordered may seem to break the [[principle of equivalence]] of [[category theory]].  However, as remarked above, a thin category always has a [[skeleton]] which is a poset; so working with posets up to isomorphism is the same as working with preordered sets up to equivalence.  In other words, if $x \le y$ and $y \le x$, so that $x$ and $y$ are [[isomorphism|isomorphic]], we may as well say that they are equal (since they are isomorphic in only one way).

Another way to say this is that the [[nerve]] [[simplicial set]] of a preorder, which is necessarily a _[[Segal space]]_ or _[[category object in an (infinity,1)-category]]_ in $Set \hookrightarrow \infty Grpd$, is in addition a _[[complete Segal space]]_ or _genuine category object_ in $Set$ if the preorder is in fact a partial order. For more on this perspective see at _[Segal space -- Examples -- In Set](Segal+space#InSetByNervesOfCategories)_.

If we distinguish between isomorphism and [[equality]] of elements in a preordered set (hence considering preordered sets up to isomorphism, rather than up to equivalence), then this is equivalent to considering the corresponding thin category to also be a [[strict category]].  When treated in this sense, preordered sets are not equivalent to posets.

On the other hand, in non-set-theoretic [[foundations]] where not every category need have an underlying set (i.e. need not be a [[strict category]] in any canonical way) --- such as [[homotopy type theory]] or [[preset]] theories --- a preordered set defined as "a set with a relation $\leq$ ..." is automatically a strict category, with a notion of equality of objects coming from the given set.  By contrast, in this case a thin category (as opposed to a more general category) does have a canonical structure of strict category in which equality of objects *means* isomorphism, but not every strict thin category is canonical in this sense.  In this case, partially ordered sets correspond to thin categories (with canonical strict-category structures), while preordered sets correspond to thin categories with arbitrary strict-category structures.

### Preorder reflection

The 2-category of preorders (more precisely, that of [[thin categories]]) is [[reflective subcategory|reflective]] in [[Cat]].  The reflector preserves the objects and declares $x \leq y$ if there exists an arrow from $x$ to $y$.


### Cauchy completion

+-- {: .num_prop}
###### Proposition

[[internalization|Internal]] to any [[regular category]] every [[poset]] is a [[Cauchy complete category]].

=--

This appears as ([Rosolini, prop. 2.1](#Rosolini)).

+-- {: .num_prop}
###### Proposition

[[internalization|Internal to]] any [[exact category]] the Cauchy completion of any [[preorder]] exists and is its [[poset reflection]].

=--

This appears as ([Rosolini, corollary. 2.3](#Rosolini)).


## Related concepts

* **preorder**

  * [[upper bound]], [[lower bound]]

* [[directed set]]

* [[partial order]]

* [[thin category]]

* [[specialization topology]]

* [[PreOrd]] 

## References

[[Cauchy completion]] for preorders is discussed in 

* {#Rosolini} G. Rosolini, _A note on Cauchy completeness for preorders_ ([pdf](http://www.disi.unige.it/person/RosoliniG/notccp.pdf))
 


[[!redirects preorder]]
[[!redirects preorders]]
[[!redirects pre-order]]
[[!redirects pre-orders]]
[[!redirects proset]]
[[!redirects prosets]]
[[!redirects preordered set]]
[[!redirects preordered sets]]
[[!redirects pre-ordered set]]
[[!redirects pre-ordered sets]]

[[!redirects preordering]]
[[!redirects preorderings]]

[[!redirects preorder category]]
[[!redirects preorder categories]]
