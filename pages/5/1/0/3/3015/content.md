# Structured sets
* tic
{: toc}


## Idea

A structured set is, of course, a [[set]] equipped with extra [[structure]].  It is not the individual structured set that matters so much as the [[category]] of sets with a particular sort of structure.


## Definitions

### Abstract

Very abstractly, we may define a __structured set__ as an [[object]] of any [[concrete category]], that is an object of any category $C$ equipped with a [[faithful functor]] $U\: C \to Set$ to the [[category of sets]].  Given two structured sets $X$ and $Y$ (in the same category $C$), a [[function]] $f\colon U(X) \to U(Y)$ between their underlying sets __preserves__ the structure if it lies in the image of $U$, that is if there exists a (necessarily unique since $U$ is faithful) [[morphism]] $\tilde{f}\colon X \to Y$ in $C$ such that $U(\tilde{f}) = f$.


### Concrete

More concretely, we may define a __type of structure on sets__ as an operation $T$ that, to any set $A$, assigns a set $T(A)$ of __$T$-structures__ on $A$.  At minimum, we should have $T(A) \cong T(B)$ whenever $A \cong B$ (where $\cong$ is [[isomorphism]] in $Set$), so that the concept is [[structural set theory|structural]].  But for good behaviour, we actually want something more coherent; we want an additional operation that, to any [[bijection]] $f\colon A \to B$, assigns a bijection $T(f)\colon T(A) \to T(B)$, such that:

*  $T(\id_A) = \id_{T(A)}$,
*  $T(f g) = T(f) T(g)$.

In other words, $T\colon Set_\cong \to Set_\cong$ (or equivalently $T\colon Set_\cong \to Set$) is a [[functor]] from the [[underlying groupoid]] of $Set$ to itself (or equivalently to all of $Set$).  In particular, any [[automorphism]] of a single set $A$ defines an automorphism of the $T$-structures on $A$, giving an [[action]] of the [[symmetric group]] $S_A$ on $T(A)$.

(Compare the notion of [[structure type]] from [[combinatorics]], which is a set-valued functor on the groupoid of [[finite sets]].  Every combinatorial structure type can be interpreted as a type of structure, where only finite sets are capable of supporting the structure.)

Given a type $T$ of structure on sets, we define a __$T$-structure set__ to be a set $A$ equipped with an [[element]] of $T(A)$.  Given $T$-structured sets $X = (A,\sigma)$ and $Y = (B,\tau)$, a bijection $f\colon A \to B$ __preserves__ the $T$-structure on $X$ and $Y$ if $T(f)(\sigma) = \tau$.  In general, there is no notion of whether an arbitrary function $f\colon A \to B$ preserves $T$-structure, although such a notion may be defined in many cases.

It is often convenient to restrict the form that $T$ may take.  [[Bourbaki]]\'s theory of structure, while not described in category-theoretic terms, is essentially the above where $T$ is required to be constructed from constant finite sets, [[cartesian products]], [[power sets]] and the like.  (I need to check Bourbaki for a complete list, particularly what kinds of [[subsets]] we may take in constructing $T$.)  This is particularly convenient for deciding when a non-invertible function preserves $T$-structure, although it does not always give the most useful answer.


## Conversions

Morally, either of the abstract and concrete versions can be converted into the other.  Technically, there are some restrictions.


### Abstract to concrete

Given a category $C$ and a faithful functor $U\colon C \to Set$, we may define a type $T$ of structure on sets as follows:

For each set $A$, consider the [[essential fiber|essential fibre]] of $U$ over $A$, the collection of pairs $(X,f)$ where $X$ is an object of $C$ and $f\colon U(X) \to A$ is a bijection.  We consider two such pairs $(X,\sigma)$ and $(Y,\tau)$ to be [[equivalent]] if there is an [[isomorphism]] $h\colon X \to Y$ in $C$ such that $U(h) ; \tau = \sigma$.  (Because $U$ is faithful, any such $h$ must be unique.)  Define $T(A)$ to be the [[quotient set]] of the essential fibre modulo this [[equivalence relation]].  That is, a $T$-structure on $A$ is an equivalence class $[(X,\sigma)]$.

Given a bijection $f\colon A \to B$, we must define $T(f)\colon T(A) \to T(B)$.  So given $(X,\sigma)$ as above, let $T(f)$ map $[(X,\sigma)]$ to $[(X,\sigma;f)]$ in $T(B)$.  It\'s easy to check that this is well defined as a function from $T(A)$ to $T(B)$; we can also check that this makes $T$ into a functor and that the abstract and concrete definitions of whether a bijection preserves $T$-structure agree.

Technicality:  If $C$ is a [[large category]], then $T(A)$ might be a [[proper class]] instead of a set.  In this case, we can pass to a larger [[universe]]; it is not essential for $T\colon Set_\cong \to Set$ that both copies of $Set$ be the same size.  But for the above description to make sense as it is, we must require that $U$ have essentially small fibres.


### Concrete to abstract

Given a type $T$ of structure on sets, we cannot quite reconstruct the category $C$, but we can reconstruct its [[core]] $C_\cong$.  That is, we can say what the [[objects]] and [[isomorphisms]] of $C$ are, if not the [[morphisms]] of $C$ in general.

An object of $C$ is simply a pair $(A,\sigma)$ consisting of a set $A$ and an element $\sigma$ of $T(A)$.  Given two such objects, an isomorphism from $(A,\sigma)$ to $(B,\tau)$ is simply a structure-preserving map from $A$ to $B$, that is a bijection $f\colon A \to B$ such that $T(f)(\sigma) = \tau$.  Then it is straightforward to check that this defines a [[groupoid]] $C_\cong$.  This groupoid is naturally equipped with a faithful [[forgetful functor]] $U\colon C_\cong \to Set$, given by $U(A,\sigma) \coloneqq A$.

For $T$ restricted to certain functors, such as is done by Bourbaki, we may also define a notion of non-invertible morphism in $C$.  However, this does not always give the most useful notion of morphism in $C$; while defining isomorphisms of structured sets is an exact science, choosing more general morphisms of structured sets is still something of an art.  (More details ...)


### Back and forth

If we start with a type $T$ of structures on sets, construct from this a groupoid $C_\cong$ and a faithful functor $U\colon C_\cong \to Set$ and then construct from this another type $T'$ of structures, then $T'$ will be equivalent to $T$ in the sense that there is a [[natural isomorphism]] between them as functors from $Set_\cong$ to $Set$.

If we start with a category $C$ and a faithful functor $U\colon C \to Set$, construct from this a type of structures $T\colon Set_\cong \to Set$, and then construct from this a groupoid $C_\cong$ with a faithful functor $U\colon C_\cong \to Set$, then $C_\cong$ will in fact be the [[core]] of $C$, with $U\colon C_\cong \to Set$ to restriction of $U\colon C \to Set$ to this core, up to [[equivalence of categories]].

(Do we need proofs?)

Thus the abstract and concrete approaches to structured sets are equivalent, except that the concrete approach does not include a specification of what are the noninvertible morphisms between structured sets.


## Examples

Almost everything in contemporary [[mathematics]] is an example of a structured set; here we list only a few representative ones (and perhaps also some exceptions).

+-- {: .query}
I want to check Bourbaki first, so that I can say clearly how they get morphisms between structured sets in the concrete approach, given restrictions on $T$.  That way, the examples can also discuss when this gives the right notion (as with [[varieties of algebras]] and preimage categories like [[Top]] and [[measurable space|Meas Sp]]) and when it does not (such as [[linear order|Lin Ord]] or [[metric space|Met]], although these are probably all arguable too!).
=--


## Structured objects

Given any category $S$ whatsoever, we may define a __type of structure__ on objects of $S$ as a functor $T\colon S_\cong \to Set$ to $Set$ from the underyling groupoid of $S$.  Then any [[faithful functor]] $U\colon C \to S$ whatsoever defines a type of structure on objects of $S$ (at least if its fibres are essentially small), in the same way as a concrete category defines a type of structure on sets.  Indeed, we say that $U$ presents the objects of $C$ as objects of $S$ with __[[extra structure]]__.


## See also

*  [[category of elements]]
*  [[Grothendieck construction]]


[[!redirects structured sets]]