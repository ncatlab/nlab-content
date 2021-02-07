
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Definition

An [[elementary topos]] $E$ is **well-pointed** if

1. the [[terminal object]] 1 is a [[separator|generator]];

   equivalently: the [[global section]] functor $\Gamma : E \to Set = E(1, -)$
   is a [[faithful functor]];

   equivalently: if $f, g: a \rightarrow b$ are morphisms such that $f x = g x$ for all [[global element]]s $x: 1 \to a$, then $f = g$;

   equivalently: every global element $x: 1 \to a$ is an [[epimorphism]]. 

2. and $E$ is nondegenerate, i.e., 1 is not an [[initial object]].


## Examples

* The category [[Set]].  Here the [[global section]] functor is even (isomorphic to) the identity functor.

* Any model of [[ETCS]].


## Properties

### Boolean properties

Assuming that one accepts [[excluded middle]] in one\'s metalogic, a well-pointed topos is also [[Boolean topos|Boolean]].  Similarly, a well-pointed topos is [[two-valued topos|two-valued]]; that is, the only [[global element|global elements]] of the [[subobject classifier]] are $\top$ and $\bot$ (and these are distinct, by nondegeneracy).


### Logical properties

The main point of a well-pointed topos in logic is the equivalence of *external* and *internal* properties. In particular, a statement in the [[internal logic]] of the topos will be satisfied if and only if it holds for all global terms. (For the 'only if' part, it is necessary that the topos be nondegenerate.)


## Generalizations
{#general}

### In constructive mathematics

To maintain this logical result in [[constructive mathematics]] (that is, without excluded middle in the metalogic), one must add  the following requirements:

3. the terminal object is [[indecomposable object|indecomposable]], and
4. the terminal object is [[projective object|projective]].

These are analogues, for [[disjunction]] and [[existential quantification]], of the nondegeneracy requirement (which is about [[falsehood]]).  Classically, they follow from the two conditions given above.

Incidentally, a well-pointed topos in a constructive metalogic is still "two-valued" in the sense that a global element of the subobject classifier is false if and only if it is not true.  However, it is not two-valued in the (classically equivalent) sense that every global element of the subobject classifier is either true or false.


### In a pretopos

If $E$ is only a [[pretopos]], we have to strengthen the condition that 1 is a generator to the condition that 1 is a [[separator|extremal generator]], i.e. for any monomorphism $m:A\to B$, if every global element $1\to B$ factors through $m$, then $m$ is an isomorphism.  In a category with a subobject classifier (such as a topos), any generator is a strong generator.

This strengthening is important in [[predicative mathematics]], where the category of sets (and in general, a [[Grothendieck topos|category of sheaves]]) is a pretopos but need not be a topos. But of course, the same applies whenever one is studying an arbitrary pretopos, not just a predicative version of $Set$.


### In more general categories

Do we know what these should be in any more general situations?

[[Mike Shulman]]: Well, the pretopos version makes sense in any [[coherent category]], and I would bet that it's the right notion in that generality.  In a [[regular category]] one might just want to assert that $1$ is a (regular-)projective extremal generator, which would probably be enough for regular logic.  And in a category with mere finite limits, being a extremal generator is all one could ask for, and that'd probably be enough for finite-limit logic.


### Well-pointed $(\infty,1)$-toposes {#Infty1Version}

> [[Urs Schreiber|Urs]]: an attempt

One might like to say that "[[∞Grpd]] is essentially the unique [[(∞,1)-topos]] with all small limits and colimits that is well-pointed ."

Possibly one should say: an $(\infty,1)$-topos $\mathbf{H}$ is _well-pointed_ if the terminal object is not the initial one and the  [[global section]] [[(∞,1)-functor]] $\Gamma : \mathbf{H} \to \infty Grpd$ is faithful...

...which should mean that on hom-$\infty$-groupoids it is a [[monomorphism in an (∞,1)-category]]...

...which should mean that for all $X,Y \in \mathbf{H}$ the image of the morphism $\Gamma_{X,Y} : \mathbf{H}(X,Y) \to Func(\Gamma(X),\Gamma(Y))$ in the [[homotopy category]] identifies $\mathbf{H}(X,Y)$ as a [[direct sum]]mand of $Func(\Gamma(X),\Gamma(Y))$.

## Related entries

* [[ETCS]]


[[!redirects well-pointed topos]]
[[!redirects well-pointed toposes]]
[[!redirects well-pointed topoi]]
[[!redirects well pointed topos]]
[[!redirects well pointed toposes]]
[[!redirects well pointed topoi]]

[[!redirects well-pointed pretopos]]
[[!redirects well-pointed pretoposes]]
[[!redirects well-pointed pretopoi]]
[[!redirects well pointed pretopos]]
[[!redirects well pointed pretoposes]]
[[!redirects well pointed pretopoi]]

[[!redirects well-pointed category]]
[[!redirects well-pointed categories]]
[[!redirects well pointed category]]
[[!redirects well pointed categories]]
