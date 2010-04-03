
# Contents
* tic
{:toc}

## Idea

A **double profunctor** is an appropriate notion of [[profunctor]] between [[double categories]].

## Definition

A double profunctor can be defined in several equivalent ways.  In each case, however, we must choose whether to regard the "vertical" or the "horizontal" direction as primary; applying transposes results in a different notion of double profunctor.


### As internal profunctors in Cat

Since a (strict) double category is an [[internal category]] in [[Cat]], it makes sense to define a **double profunctor** to be an internal profunctor in $Cat$.  Thus, if $C$ and $D$ are double categories, a double profunctor $C &#8696; D$ consists of a span $C_0 \leftarrow H \to D_0$ in $Cat$, together with actions $C_1 \times_{C_0} H \to H$ and $H\times_{D_0} D \to H$ which are associative and commute with each other.


### As collages in DblCat

Another natural way to define a double profunctor is in terms of its [[collage]].  From this perspective, a double profunctor $C &#8696; D$ consists of a double category $H$, together with double functors $C\to H$ and $D\to H$ such that:

1. The images of $C$ and $D$ in $H$ are disjoint.
1. The induced functor $C\sqcup D\to H$ is bijective on objects and vertical arrows.
1. Each functor $C\to H$ and $D\to H$ is fully faithful on horizontal arrows and squares.
1. There are no horizontal arrows in $H$ from an object of $C$ to an object of $D$, and therefore also no squares whose horizontal source is a vertical arrow in $C$ and whose horizontal target is a vertical arrow in $D$.

In order to identify this with the previous definition as written, for a double category $C = C_1 \;\rightrightarrows\; C_0$ written as an internal category in $Cat$, we have to write the arrows of $C_0$ vertically and the objects of $C_1$ horizontally.

Defined in this way, double profunctors can be seen to be precisely the two-sided [[codiscrete cofibration|codiscrete cofibrations]] in the 2-category $DblCat$ of double categories, double functors, and horizontal transformations.


### As Span-valued double functors

A third natural way to define double profunctors is as functors defined on $D^{op}\times C$.  In order to make this agree with the previous two definitions, we have to consider *lax* double functors from $D^{op}\times C$ to $Span$, where $D^{op}$ denotes horizontal reversal, and $Span$ denotes the (pseudo) double category whose objects are sets, whose horizontal arrows are functions, and whose vertical arrows are spans.


### Explicit definition

Each of these definitions can be unraveled to give a more explicit definition, and thereby shown to be the same.  Explicitly, a double profunctor $H\colon C &#8696; D$ consists of the following.

* An ordinary [[profunctor]] $H^0\colon C^0 &#8696; D^0$, where now $C^0$ denotes the *horizontal* category of $C$.

* An ordinary profunctor $H^1 \colon C^1  &#8696; D^1$.

* Each $r \in H^1(q,p)$ is assigned a vertical source $s(r) \in H^0(s(q),s(p))$ and target $t(r) \in H^0(t(q),t(p))$.

* Each $h \in H^0(d,c)$ is assigned an identity $1_h \in H^1(1_d,1_c)$.

* If $r_1 \in H^1(q_1,p_1)$ and $r_2 \in H^1(q_2,p_2)$ and $t(r_1) = s(r_2)$ (hence $t(q_1)=s(q_2)$ and $t(p_1)=s(p_2)$), then there is a vertical composite $r_2 \boxminus r_1 \in H^1(q_2 q_1,p_2 p_1)$ with $s(r_2\boxminus r_1) = s(r_1)$ and $t(r_2\boxminus r_1) = t(r_2)$.

* The composition $\boxminus$ is associative and unital (with $1_h$ as identities), and interchanges with the action of the profunctor $H^1$ and the vertical composition of squares in $C$ and $D$.


## Examples

* If $C$ and $D$ are [[strict 2-categories]] regarded as vertically-discrete double categories, then a double profunctor $C &#8696; D$ is the same as a $Cat$-[[enriched category|enriched]] [[profunctor]], i.e. a strict 2-functor $D^{op}\times C \to Cat$.  There is a corresponding statement in the pseudo case (see below).

* On the other hand, if $C$ and $D$ are 2-categories regarded as *horizontally*-discrete double categories, then a double profunctor $C &#8696; D$ is the same as a lax 2-functor $D^{co}\times C \to Span$, or equivalently a normal lax 2-functor $D^{co}\times C \to Prof$.


## Weakenings

The definition can be weakened to the case when the composition of $C$ and $D$ is weak in one direction or the other, or both (modulo a suitable definition of the latter situation, see [[double category]] for several possibilities).

* The internal definition can easily be weakened in the case when $C$ and $D$ are *horizontally* pseudo, since then they are simply pseudo internal categories in $Cat$.

* The collage definition, on the other hand, can easily be weakened to the case when $C$ and $D$ are *vertically* pseudo, by looking at codiscrete cofibrations in the 2-category of vertically-pseudo double categories, pseudo double functors, and horizontal transformations.  The explicit description of the collages could also be given for horizontally or doubly pseudo double categories, although in those cases it would be harder to identify them with codiscrete cofibrations, since horizontal transformations would no longer be the 2-cells in a 2-category (only a [[tricategory]] of some sort).

* The Span-valued double functor definition makes perfect sense as written if $C$ and $D$ are vertically pseudo, and also if they are horizontally or doubly pseudo, modulo a suitable definition of "vertically lax functor" in the latter two cases.

* The explicit definition can also easily be weakened, with an insertion of coherence isomorphisms for $C$ and $D$ in appropriate places.


## Composites

Composition of double profunctors is, unfortunately, hard to define and not well-behaved.  Several of the above definitions suggests a possible way to compose them, but not all of these definitions work.  In particular, there is not a double category of double categories, double functors, and double profunctors.


### Using internal profunctors

For instance, internal profunctors can be composed, using a coequalizer, in any category which has coequalizers preserved by pullback---but while $Cat$ has coequalizers, they are not preserved by pullback, so this does not work.  (This failure has nothing to do with strictness or weakness; [[2-colimits]] in $Cat$ are also not preserved by [[2-pullbacks]].)

This definition does, however, suggest a replacement for the nonexistent double category of double profunctors.  Namely, internal categories, functors, and profunctors in *any* category with pullbacks always form a [[virtual double category]], and in fact a [[virtual equipment]].   Thus, in particular, there is a virtual equipment $DblProf$ of double categories, double functors, and double profunctors.  In terms of the explicit definition, a cell in $DblProf$ with some given boundary consists of:

* An ordinary cell in $Prof$, whose boundary is obtained by applying $(-)^0$, and

* Another ordinary cell in $Prof$, whose boundary is obtained by applying $(-)^1$, such that

* Vertical sources, targets, identities, and composites are respected.

For many purposes, having a virtual equipment of double profunctors is sufficient.  For instance, this is all we need in order to talk about [[weighted limits]], and in order to define [[generalized multicategories]].  We can also use this as a setting in which to ask whether some particular pair (or string) of double profunctors might have a composite, or a "weak composite," as described at [[tensor product]].


### Using collages

The standard way to compose codiscrete cofibrations $C\to H \leftarrow D$ and $D\to K\leftarrow E$ is to take the pushout (or 2-pushout) $H\sqcup_D K$ and then factor $C\sqcup E \to H\sqcup_D K$ as $C\sqcup E \to H\circ K \to H\sqcup_D K$ in some way such as to make $C\sqcup E \to H\circ K$ codiscrete.  We can do this for codiscrete cofibrations in $DblCat$, but the resulting composition operation is not associative, since pushouts in $DblCat$ do not preserve the requisite factorizations.

I believe that the binary composite of double profunctors defined in this way is a "weak composite" in the virtual double category $DblProf$, i.e. it has a universal property relative to cells with source of length 2 only.  We can likewise define basic $n$-ary composites of codiscrete cofibrations by taking an $n$-ary pushout and then a factorization, but for $n\gt 2$, as far as I can tell, there is little relation between these composites and $DblProf$.  In particular, these composites form a "lax double category", whereas a virtual double category with all weak composites can be identified with an "oplax double category."  I also don't know whether the cells in $DblProf$ with source of length $\gt 2$ can be seen from the perspective of collages.

[[!redirects double profunctors]]
