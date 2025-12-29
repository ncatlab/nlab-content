
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
#### Relations
+-- {: .hide}
[[!include relations - contents]]
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

A *preorder* or a *quasi-order* is like a [[partial order]], but without the "antisymmetry" requirement that $x \leq y$ and $y \leq x$ implies $x = y$.

By interpreting the relation $\leq$ as the existence of a unique [[morphism]], preorders may be regarded as certain [[categories]] (namely, [[thin categories]]).  This category is sometimes called the _preorder category_ associated to a preorder; see below for details.

## Definition

### As a set with a relation ###

A **preorder** or **quasiorder** on a set $S$ is a [[reflexive relation|reflexive]] and [[transitive relation|transitive]] relation, generally written $\leq$.  A **preordered set**, or **proset**, is a set equipped with a preorder. (This should not be confused with a [[pro-set]], i.e. a [[pro-object]] in [[Set]].)

### As a graph ###

A **preordered set** is a [[loop digraph object|loop]] [[digraph]] $(V, E, s:E \to V, t:E \to V)$, with functions $refl:V \to E$ and  
$$tr:\{(f,g) \in E \times E \vert t(f) =_V s(g)\} \to E$$ 
such that 

* for every $a \in V$, $s(refl(a)) =_V a$
* for every $a \in V$, $t(refl(a)) =_V a$
* for every $f \in E$, $s(tr(g,f)) =_V s(f)$ 
* for every $f \in E$, $t(tr(g,f)) =_V t(g)$
* for every $f \in E$, $tr(f, refl(s(f))) =_E f$ 
* for every $f \in E$, $tr(refl(t(f)), f) =_E f$ 
* for every $f \in E$, $g \in E$, and $h \in E$ such that $t(f) =_V s(g)$ and $t(g) =_V s(h)$, $tr(h,tr(g,f)) =_E tr(tr(h,g),f)$

### As a category ###
 {#AsACategory}

[[relation between preorders and (0,1)-categories|Equivalently, a preordered set is]] a ([[strict category|strict]]) [[thin category]]: a [[strict category]] such that for any [[pair]] of [[objects]] $x, y$, there is at most one [[morphism]] from $x$ to $y$.  The existence of such a morphism corresponds to the truth of the relation $x \leq y$.  [[relation between preorders and (0,1)-categories|In other words, it's]] a (strict) [[category enriched]] over the [[cartesian monoidal category]] of [[truth values]] (a [[(0,1)-category]]).


### In homotopy type theory

In [[homotopy type theory]], we must be careful to distinguish _preorders_ (on a homotopy type of arbitrary [[h-level]]) and _preordered sets_ (which apply to an [[h-set]]). When translating ordinary, set-level mathematics to HoTT, preordered sets are almost always what is wanted. A preorder on a type $A$ consists of:

* For each pair of elements $a, b : A$, a [[mere proposition | proposition]] $a \le b$;

* For every $a : A$, a witness of _reflexivity_ $\operatorname{refl}_a : a \le a$

* For every $a, b, c : A$, $p : a \le b$ and $q : b \le c$, a witness of _transitivity_ $\operatorname{trans}_{a,b,c}(p, q) : a \le c$.

Note that, as usual, the quantifiers "for each" and "for every" should be interpreted as applications of the corresponding [[dependent function types]]. Every homotopy type $A$ has an [[h-set]] of possible preordered structures, but the [[dependent sum type|sum]] of all possible structures has h-level bounded by $A$'s.

## Properties

### Relation to partial orders

Any preordered set is [[equivalence of categories|equivalent]] to a [[partial order|poset]].  This is a special case of the theorem that every category has a [[skeleton]], but (if you define 'equivalence' weakly enough) this case does _not_ require the [[axiom of choice]].

If the [[foundations]] have [[quotient sets]], then every preorder has a quotient set equivalent to a poset. Let $(P, \leq)$ be a preorder. Define the [[equivalence relation]] $\sim$ on $P$ for all elements $a, b \in P$ as $a \sim b := (a \leq b) \wedge (b \leq a)$. Then the quotient set $P / \sim$ is a poset. This is the 0-truncated version of the fact that because every [[category object in an (infinity,1)-category|precategory]] has a [[core]] [[groupoid object in an (infinity,1)-category|pregroupoid]] and every pregroupoid has a Rezk completion into a [[groupoid]], every precategory has a Rezk completion into a [[category]].

Note that while in [[homotopy type theory]], preorders can be applied to general types (thus the need for differentiating between preorders and preordered _sets_), partial orders necessarily apply to sets: Any map $p : (a \le b) \wedge (b \le a) \to (a = b)$ is necessarily a fibrewise equivalence (fixing $a$ and quantifying over $b$), since it induces an equivalence of total spaces. Thus, the codomain type $(a = b)$ is a proposition, since the domain $(a \le b) \wedge (b \le a)$, being a product of propositions, is a proposition.

### Relation to thin categories

In [[set theory|set-theoretic]] [[foundations]], a preordered set is the same as a [[thin category]] (a category in which any two parallel [[morphisms]] are equal), and it is partially ordered just when it is [[skeletal category|skeletal]].  Thus, asking for a preordered set to be partially ordered may seem to break the [[principle of equivalence]] of [[category theory]].  However, as remarked above, a thin category always has a [[skeleton]] which is a poset; so working with posets up to isomorphism is the same as working with preordered sets up to equivalence.  In other words, if $x \le y$ and $y \le x$, so that $x$ and $y$ are [[isomorphism|isomorphic]], we may as well say that they are equal (since they are isomorphic in only one way).

Another way to say this is that the [[nerve]] [[simplicial set]] of a preorder, which is necessarily a _[[Segal space]]_ or _[[category object in an (infinity,1)-category]]_ in $Set \hookrightarrow \infty Grpd$, is in addition a _[[complete Segal space]]_ or _genuine category object_ in $Set$ if the preorder is in fact a partial order. For more on this perspective see at _[Segal space -- Examples -- In Set](Segal+space#InSetByNervesOfCategories)_.

If we distinguish between isomorphism and [[equality]] of elements in a preordered set (hence considering preordered sets up to isomorphism, rather than up to equivalence), then this is equivalent to considering the corresponding thin category to also be a [[strict category]].  When treated in this sense, preordered sets are not equivalent to posets.

On the other hand, in non-set-theoretic [[foundations]] where not every category need have an underlying set (i.e. need not be a [[strict category]] in any canonical way) --- such as [[homotopy type theory]] or [[preset]] theories --- a preordered set defined as "a set with a relation $\leq$ ..." is automatically a strict category, with a notion of equality of objects coming from the given set.  By contrast, in this case a thin category (as opposed to a more general category) does have a canonical structure of strict category in which equality of objects *means* isomorphism, but not every strict thin category is canonical in this sense.  In this case, partially ordered sets correspond to thin categories (with canonical strict-category structures), while preordered sets correspond to thin categories with arbitrary strict-category structures.

### Construction of preorders from any binary relation

(See also [[codensity monad]], [[quantification#Guarded|guarded quantification]].) 

\begin{theorem}
Given [[sets]] $A$ and $B$ and a [[binary relation]] $R(x, y)$ between $A$ and $B$, then the relation 
$$T(x, y) \coloneqq \forall w:B.R(x, w) \implies R(y, w)$$
is a [[preorder]] on $A$. 
\end{theorem}

\begin{proof}
We work in [[dependent type theory]], where implication is denoted by the [[function type]] $P \to Q$ and universal quantification is denoted by the [[dependent product type]] $\prod_{x:A} P(x)$. Thus, the type family $T(x, y)$ is represented as

$$T(x, y) \coloneqq \prod_{w:B} R(x, w) \to R(y, w)$$

A [[binary relation]] in dependent type theory is a type family $x:A, y:B \vdash R(x, y)$ such that each $R(x, y)$ is an [[h-proposition]]. Since $R(x, w)$ and $R(y, w)$ are both [[h-propositions]], and h-propositions are closed under [[function types]] and [[dependent product types]], $T(x, y)$ is also valued in [[h-propositions]], and is a binary relation. 

In addition, for all elements $x:A$, there is an element

$$\mathrm{refl}_{T}(x):\prod_{w:B} R(x, w) \to R(x, w)$$

defined by the [[identity function]] on $R(x, w)$

$$\mathrm{refl}_{T}(x)(w) \coloneqq \mathrm{id}_{R(x, w)}$$

and for all elements $x:A$, $y:A$, and $z:A$, there is a function 

$$\mathrm{trans}_{T}(x, y, z):\left(\prod_{w:B} R(x, w) \to R(y, w)\right) \times \left(\prod_{w:B} R(y, w) \to R(z, w)\right) \to \left(\prod_{w:B} R(x, w) \to R(z, w)\right)$$

defined by [[composition]] of the functions $f(w):R(x, w) \to R(y, w)$ and $g(w):R(y, w) \to R(z, w)$ dependent upon element $w:B$:

$$\mathrm{trans}_{T}(x, y, z)(f, g)(w) \coloneqq g(w) \circ f(w)$$

Since the type 

$$\prod_{w:B} R(x, w) \to R(y, w)$$

is a [[binary relation]] valued in [[h-propositions]] which satisfies [[reflexivity]] and [[transitivity]], it is a [[preorder]]. 
\end{proof}

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

* [[relation between preorders and (0,1)-categories]]

* **preorder**

  * [[upper bound]], [[lower bound]]

* [[directed set]]

* [[partial order]]

* [[thin category]]

* [[specialization topology]]

* [[specialization order]]

* [[PreOrd]] 

* [[graph]], [[digraph]]

* [[symmetric preorder]]

* [[preordered object]]

## References

[[Cauchy completion]] for preorders is discussed in 

* {#Rosolini} G. Rosolini, _A note on Cauchy completeness for preorders_ ([pdf](http://rivista.math.unipr.it/fulltext/1999-2s/06.pdf))

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

[[!redirects quasiorder]]
[[!redirects quasiorders]]
[[!redirects quasi-order]]
[[!redirects quasi-orders]]
[[!redirects quasiordering]]
[[!redirects quasiorderings]]
[[!redirects quasi-ordering]]
[[!redirects quasi-orderings]]

[[!redirects quasiordered set]]
[[!redirects quasiordered sets]]
[[!redirects quasi-ordered set]]
[[!redirects quasi-ordered sets]]
[[!redirects quoset]]
[[!redirects quosets]]
