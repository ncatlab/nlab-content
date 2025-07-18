
> This entry is about the notion of universe of [[sets]] in [[mathematics]]. For other notions of universe, see at [[universe]]. 

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc} 

## Idea

A **universe of [[sets]]** is a realm within which (some conceived part, naively and virtually all, of) the [[mathematics]] of [[sets]] may be thought of as taking place. Universes can be purely metamathematical, but we can also reflect upon them and bring them into mathematics. 

## Categories as universes

Much of [[ordinary mathematics]] can be thought of as taking place [[internalization|inside]] "the archetypical [[category]] [[Set|SET]] of sets".  Typically, the properties of $SET$ are formulated in [[first-order logic]] using a [[set theory]] such as [[ZFC]] or (more directly) [[ETCS]].

We can generalise this from $SET$ to any other [[category]] $C$.  Without further assumptions on the category, there is in general very little mathematics that can be formulated inside it, but a few extra properties and structures are usually sufficient to provide something interesting.  This is the general topic of _[[internalisation]]_.  The attitude to take is that any *specific* category is merely one [[model]], while a general *class* of categories is a [[theory]] (really a [[doctrine]], or [[2-theory]]).

We can also use [[higher category theory|higher categories]] instead of mere categories here.  Even for ordinary mathematics, this means starting with $\infty$-[[infinity-Grpd|GRPD]] instead of $SET$.

## Universes as classes

The idea of the [[large category]] $SET$ as the universe of mathematics has an analogue in [[class theory]]. In a [[material class theory]], the __von Neumann universe__ $V$ is the [[class]] of all [[axiom of foundation|well-founded]] [[pure sets]].

More explicitly: for every [[ordinal number]] $\alpha$, we have a [[set]] $V_\alpha$ (the von Neumann universe of __rank__ $\alpha$), defined [[recursion|recursively]] using the operations of [[power set]] and (material) [[union]] as
$$ V_\alpha \coloneqq \bigcup_{\beta \lt \alpha} \mathcal{P}V_\beta .$$
Then $V$ itself is the union of all of the $V_\alpha$.

A similar but more complicated definition allows us to define the universe $L$ of [[constructible set]]s, called the [[constructible universe]].

See also a [Wikipedia article](https://secure.wikimedia.org/wikipedia/en/wiki/Universe_%28mathematics%29) written largely by [[Toby Bartels]] in another lifetime.

In a [[structural class theory]], such as the [[category with class structure]] found in [[algebraic set theory]], a **universe** is a class $U$ with a [[monic]] class [[map]] $\mathcal{P}(U) \hookrightarrow U$ from the [[power object|powerclass]] of $U$ to $U$. In particular, every [[universal class]] is a universe. 

## Grothendieck universes 

A [[Grothendieck universe]] is a set $U$ such that the following properties hold for $U$: 

1. if $x \in a \in U$, then $x \in U$;  
1. if $a, b \in U$, then $\{a, b\}$ and $a\times b$ are elements of $U$;
1. if $a \in U$, then $\cup a$ and $P(a)$ are elements of $U$; 
1. the set $\omega$ of all natural numbers is an element of $U$; 
1. if $f:a \to b$ is surjective with $a \in U$ and $b \subseteq U$, then $b \in U$.

## Universes inside $SET$

If set theory is the [[foundation of mathematics]], then the universes above are part of metamathematics rather than mathematics itself.  However, we can also look for [[small categories]] or sets that exist within set theory and have the properties of a universe.

There is already a hint of this in the hierarchy $V_\alpha$ out of which the von Neumann universe is built.  For some values of $\alpha$, $V_\alpha$ might be a sufficiently large and complete collection of [[sets]] in which to do ordinary mathematics.  From the [[nPOV]], we can instead look at the category $Set_\alpha$ of these sets and the [[functions]] between them, although it\'s more common to think about $Set_\kappa$ for some [[cardinal number]] $\kappa$.

An [[infinite set]] is a simple example, as [[finite mathematics]] can be done inside it.  Going beyond this, a [[Grothendieck universe]] is a set within which other infinite sets exist but which is complete under the operations of [[material set theory]] that are needed for ordinary mathematics.  The [[structural set theory|structural]] analogue is a [[universe in the topos]] $SET$.

In general, we need some axioms to state the existence of such universes; we can think of these as [[large cardinal]] axioms.  (The existence of an infinite set is the [[axiom of infinity]]; the existence of a Grothendieck universe is the existence of an [[inaccessible cardinal]].)

The use of such universes is convenient when we want to work with [[large categories]] "as if they were small."  That is, if we redefine "small" to mean "element of some fixed universe," then the categories of all small structures of some sort will still be sets (rather than [[proper classes]]) in the bigger ambient universe, and thus we can for instance form [[functor categories]] between them freely.  We do sometimes then need a way to "move a category" from one universe to another; see [[universe enlargement]].


## Reflection

In [[logic]], we use [[reflection principle]]s (see [Wikipedia](https://secure.wikimedia.org/wikipedia/en/wiki/Reflection_principle)) to systematically identify features of our meta-universe and see what is needed to prove the existence of an internal universe with these features.

This follows the following outline:

1.  We assume that we understand _a priori_ what it means to use [[first-order logic]] (or some other finitary base logic).

2.  Using this base logic, we can formulate a foundational [[set theory]] that describes a meta-universe such as $SET$.

3.  Of course, $SET$ cannot be described from inside itself.  But there may be objects in $SET$ ([[internal categories]]) that _look like_ $SET$ itself.

4.  We add an additional axiom to our set theory stating that such objects, the _internal universes_, exist.  These are then [[models]] of our original set theory.

5.  Now we are using a new, stronger set theory; repeat.

## Universe of sets in type theory

Set theory is not the only [[foundation of mathematics]].  For example, there are also various foundational [[type theories]], closely related to [[structural set theory]].  Then we have a meta-universe of all types, and we can isolate the types which are [[sets]] to get a meta-universe of sets. 

We can also add axioms for the existence of internal [[type universes]] $U$, and in [[dependent type theory]] similarly isolate the types which are [[h-sets]] $\mathrm{Set}_U \coloneqq \sum_{A:U} \mathrm{isSet}(A)$, resulting in the notion of an internal **universe of sets**. 

See [[type universe]] for the more general concept of a universe of types. 

## Related concepts

* [[constructible universe]]

* [[universe enlargement]]

* [[universe polymorphism]]

* [[type of types]]

  * [[subobject classifier]], [[object classifier]], [[partial map classifier]]

* [[reflective subuniverse]]

* [[G-universe]]

## References

### General

For universes in [[class theory]] and [[algebraic set theory]], see

* [[Steve Awodey]]. *Notes on algebraic set theory*, Notes for lectures given at the Summer School on Topos Theory, Haute-Bodeux, Belgium. May 29 to June 5, 2005. Carnegie Mellon University Technical Report No. CMU-PHIL-170. June 2005. ([pdf](https://www.phil.cmu.edu/projects/ast/Papers/bnotes.pdf))

For Grothendieck's early use of the term

* [[Alexander Grothendieck]]. *Sur la formalisation des catégories et foncteurs*, Rédaction Bourbaki [No. 307] Fonds Pierre Cartier (Archives Henri Poincaré) ([pdf](https://csg.igrothendieck.org/wp-content/uploads/2024/06/U2u.pdf))

### In type theory

* [[Martin Hofmann]], section 2.1.6 of _Syntax and semantics of dependent types_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.36.8985))

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

[[!redirects universe > history]]

[[!redirects von Neumann universe]]
[[!redirects von Neumann universes]]

[[!redirects universe of sets]]
[[!redirects universes of sets]]

[[!redirects set universe]]
[[!redirects set universes]]

[[!redirects set of all sets]]
