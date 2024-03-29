
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Generators and relations
* table of contents
{: toc}

## Idea

A mathematical structure is said to be _presented by generators and relations_ if it is obtained from a structure _[[free construction|freely]] generated_ by a [[set]] of _generators_ by imposing _relations_ among these generators. 

For instance an [[associative algebra]] $A$ may be obtained by imposing on the [[tensor algebra]] of the underlying vector space (which is the [[free monoid|free algebra]] on that vector space) the product relations, which identify the formal juxtaposition of two elements with their intended product. This is for instance how _[[Clifford algebras]]_ or _[[universal enveloping algebras]]_ are traditionally defined.

Similarly a [[group presentation]] specifies a group in terms of a set of generators and relations.  The study of group presentations form and important part of [[combinatorial group theory]].

But the concept of _generators and relations_ is very general and applies to all kinds of structures. Below we discuss a general formalization using concepts from [[category theory]] and [[universal algebra]].

## Definition

Let $C$ be a [[category]], $T$ a [[monad]] on $C$, and $A$ a $T$-[[algebra for a monad|algebra]].  A **presentation of $A$ by generators and relations** is a [[coequalizer]] diagram

$$ T R \; \rightrightarrows \; T G \to A $$

in the category $C^T$ of $T$-algebras.  Here $G\in C$ is the *object of generators* and $R\in C$ is the *object of relations*.

The $T$-algebra map $T G \to A$ corresponds to a unique morphism $G\to A$ in $C$, which we think of as the "inclusion" of the generators into $A$ (though in general it need not be any kind of [[monomorphism]]).  Similarly, the $T$-algebra maps $T R \;\rightrightarrows\; T G $ correspond to unique morphisms $R \;\rightrightarrows\; T G$ in $C$, which we think of as a [[binary relation]] on $T G$ (though in general, the maps need not be jointly monic either).

This definition can be generalised to any [[concrete category]] with [[free objects]], not necessarily monadic.


## Examples

### Monads on Set

The classical case is when $C=$[[Set]].  Then $G$ and $R$ are sets, and a presentation of a $T$-algebra by generators and relations amounts to first constructing the free $T$-algebra $T G$ on the generators, then specifying (via the maps $R \;\rightrightarrows\; T G$) a set of pairs of elements of $T G$ to be identified (the relations).  The presented $T$-algebra $A$ is the [[quotient set]] by these relations.

Probably the *most* classical case is when $T$ is the free [[group]] monad on $Set$.


### Categories

[[Cat]] (to be precise, [[Str Cat]]) is the category of algebras for a monad on the category of [[quivers]].  Therefore, we have a notion of a [[presentation of a category by generators and relations]].


### Theories and Monads

[[Lawvere theories]], [[operads]], and even ([[accessible functor|accessible]]) [[monads]] can be realized as the algebras for monads on some categories.  Thus, we can talk about presentations of these sorts of objects by generators and relations.  In this context, each "generator" is an *operation*, and each "relation" is an *axiom* that the operations must satisfy.  For instance, the usual definition of a group in terms of binary, nullary, and unary operations satisfying associativity, unitality, and inversion axioms can be regarded as a presentation of the Lawvere theory (or monad) of groups by generators and relations.


## Existence

+-- {: .num_theorem}
###### Theorem
Every $T$-algebra has a presentation by generators and relations.
=--
+-- {: .proof}
###### Proof
For any $T$-algebra $A$, the following diagram is a coequalizer (also called the [[Beck coequalizer]]):
$$ T^2 A \; \underoverset{\mu}{\T a}{\rightrightarrows}\; T A \xrightarrow{a} A$$
where $a\colon T A \to A$ is the structure map of the $T$-algebra $A$ and $\mu$ is the multiplication of the monad $T$.
=--

This particular presentation is of importance in the [[monadicity theorem]].

However, in practice one is usually interested in more "economical" presentations where $G$ and $R$ are smaller than $A$.  For example, for monads over [[Set]], when $G$ and $R$ are [[finite sets]], then we say that $A$ is __[[finitely presented object|finitely presented]]__.


## Remarks

Note that knowing only the category of $T$-algebras does not suffice to determine the notion of "presentation by generators and relations"; we also have to exhibit it as the category of algebras for a monad $T$ on some other category $C$.  Often the choice of $C$ is obvious, but there are cases in which the same category can be realized as the category of algebras for multiple monads on multiple different categories, yielding different notions of "generators and relations".  For example, the category of finitary monads on $Set$ (= Lawvere theories) can be realized as monadic over the category of finitary endofunctors of Set, or over the category of $\mathbb{N}$-indexed sets.


## Categorifications

If $C$ is an [[n-category]] and $T$ a suitable sort of monad, then we have a similar notion except that coequalizers must be replaced by ($n$-truncated) [[codescent object|codescent objects]], i.e. [[geometric realization]].

## Related concepts

* [[finitely generated object]]



[[!redirects generators and relations]]
[[!redirects presentation by generators and relations]]
[[!redirects presentations by generators and relations]]

[[!redirects presentation]]
[[!redirects presentations]]
