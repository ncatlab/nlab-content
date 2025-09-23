+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

{:toc}

An **anabicategory** is a particular notion of _weak [[2-category]]_ appropriate in the absence of the [[axiom of choice]] (including in many [[internal category|internal]] contexts).  It is derived from the notion of [[bicategory]] by replacing the composition functors $\circ: B(y,z) \times B(x,y) \to B(x,z)$ with [[anafunctor]]s (and therefore the [[associator]]s and [[unitor]]s with [[ananatural transformation|ananatural transformations]]).

If [[Cat]] is defined as consisting of ([[small category|small]]) [[category|categories]], anafunctors, and [[ananatural transformation|ananatural transformations]] (as is most appropriate in the absence of choice), then $Cat$ is more naturally an anabicategory rather than any stricter notion.

Under the equivalence between [[anafunctors]] and [[representable profunctors]], anabicategories are equivalent to [[representable multicategory|representable]] [[probicategories]].

# Explicit definition

An anabicategory $\mathcal{C}$ consists of a set $\mathcal{C}_0$ of objects, a set $\mathcal{C}_1$ of 1-cells, which are relations $\mathcal{C}_0 \times \mathcal{C}_0$, and a set $\mathcal{C}_2$ of 2-cells, which are relations $\mathcal{C}_1 \times \mathcal{C}_1$. (Note that only $\mathcal{C}_2$ needs a defined equality relation, so the other two sets only need to be [[preset]]s.) On these sets are defined several relations; for each relation $R$ if we have $R(x, y)$ $y$ is said to be a _value_ of $R$ at $x$. Some pairs $x, y$ with $R(x, y)$ are also said to be _specified values_; generally if $R$ has some value at $x$, at least one such value will be specified. We omit the word "value" when it is clear from context.

1. There are _source_ and _target_ relations $\mathcal{C}_1 \times \mathcal{C}_0$ and $\mathcal{C}_2 \times \mathcal{C}_1$, and every 1- or 2- cell $f$ has some specified value for its source and target.
1. There are _2-source_ and _2-target_ relations $\mathcal{C}_2 \times \mathcal{C}_0$, and every 2- cell $f$ has some specified value for its 2-source and 2-target.
1. There are _identity_ relations $Id:\mathcal{C}_0 \times \mathcal{C}_1$ and $\mathcal{C}_1 \times \mathcal{C}_2$, and every object or 1-cell has some specified value for its identity.
1. There is a _composition_ relation $\circ:(\mathcal{C}_1 \times \mathcal{C}_1) \times \mathcal{C}_1$; whenever $f_1$ and $f_2$ are such that some specified target of $f_1$ is also a specified source of $f_2$, there is some specified value of the composite of $f_1$ and $f_2$.
1. There is a _1-composition_ relation $\circ_1:(\mathcal{C}_2 \times \mathcal{C}_2) \times \mathcal{C}_2$; whenever $f_1$ and $f_2$ are such that some specified 2-target at $f_1$ is also a specified 2-source at $f_2$, there is some specified value of the 1-composite of $f_1$ and $f_2$.
1. There is a _2-composition_ relation $\circ_2:(\mathcal{C}_2 \times \mathcal{C}_2) \times \mathcal{C}_2$; whenever $f_1$ and $f_2$ are such that some specified target at $f_1$ is also a specified source at $f_2$, there is some specified value of the 2-composite of $f_1$ and $f_2$.

The relations satisfy the following conditions:

1. For any 2-cell $f$, and any values $x$ and $y$ of its source and target (respectively), the set of targets of $x$, of targets of $y$, and of 2-targets of $f$ are all equal (as subsets of $\mathcal{C}_1$), and likewise for sources/2-sources. If $x$ or $y$ is a specified value of either relation, each specified value of its source is a specified value of the 2-source, and likewise for targets/2-targets.
1. Any source of an identity $x$ is also a target of $x$, and vice versa. (However, we do not require the sets of specified values to match.) For any specified identity $y$ of $x$, $x$ should be a specified source and target of $y$.
1. If $h$ is composition of $f \circ g$, the set of targets of $f$ is equal to the set of targets of $h$, and the set of sources of $g$ is equal to the set of sources of $h$. If $h$ is a specified composition, any specified target of $f$ is a specified target of $h$, and any specified source of $g$ is a specified source of $h$. (In general the converses may fail.) Moreover, if the composition $f \circ g$ has any value, the set of targets of $g$ is equal to the set of sources of $f$.
1. If $h$ is a value of the 2-composition $f \circ_2 g$, the set of targets of $f$ is equal to the set of targets of $h$, and the set of sources of $g$ is equal to the set of sources of $h$. If $h$ is a specified value of the 2-composition, any specified target of $f$ is a specified target of $h$, and any specified source of $g$ is a specified source of $h$. Moreover, if the 2-composition $f \circ_2 g$ has any value, the set of targets of $g$ is equal to the set of sources of $f$.
1. If $h$ is a value of the 1-composition $f \circ_1 g$, each source of $h$ is a composition of some source of $f$ and some source of $g$, and each such composition is a source of $h$. For any specified sources of $f$ and $g$, each specified value of their composition is a specified source of $h$. The same results hold with source replaced by target. Moreover, if the 1-composition $f \circ_1 g$ has any value, the set of 2-targets of $g$ is equal to the set of 2-sources of $f$.

There are also conditions defining equivalence relations on $\mathcal{C}_0$ and $\mathcal{C}_1$. (The equivalence relation for $\mathcal{C}_2$ is simply equality.) All the relations defined above are required to be invariant under the appropriate equivalence relations (note, however, that their specified values do not need to be invariant). So in particular, the identity relation $\mathcal{C}_1\times \mathcal{C}_2$ and the 1- and 2- composition relations $(\mathcal{C}_2 \times \mathcal{C}_2) \times \mathcal{C}_2$ are functional: any two values of the identity on some 1-cell $x$, or any two values of one of the compositions on some 2-cells $f$ and $g$, must be equal (as elements of $\mathcal{C}_2$.)

* A 2-cell $f$ is said to be an _isomorphism_ (between any of its sources and any of its targets) if there are some 2-cell $g$ and 1-cell $x$ such that the 2-composition of $f$ and $g$ is the identity on $x$. We say that $g$ is an _inverse_ of $f$.
* Two 1-cells $f$ and $g$ are _isomorphic_ if there is a 2-cell isomorphism $h$ with $f$ as a source and $g$ as a target (or equivalently, vice versa). This is the chosen equivalence relation for $\mathcal{C}_1$.
* A 1-cell $f$ is said to be an _equivalence_ (between any of its sources and any of its targets) if there are some 1-cell $g$ and object $x$ such that some composition of $f$ and $g$ in either direction is isomorphic to an identity on $x$.
* Two objects $x$ and $y$ are _equivalent_ if there is a 1-cell equivalence $g$ with $x$ as a source and $y$ as a target (or equivalently, vice versa). This is the chosen equivalence relation for $\mathcal{C}_0$.


Finally there are coherence relations:

1. Let $f$ be an identity 2-cell (in other words, a value of the identity relation for some 1-cell), and $g$ be any 2-cell. Then, if there is a 2-composition $f \circ_2 g$ or $g \circ_2 f$, any such value is equal to $g$. It follows (by considering their 2-composition) that identities on isomorphic 1-cells are equal, and that when two 1-cells are isomorphic, this fact will be witnessed by the identity on either object.
1. Let $f$ and $g$ be identity 2-cells on, say, $x$ and $y$ respectively, and suppose that $f \circ_1 g$ exists. Then it is an identity 2-cell on any value of $x \circ y$. Equivalently: the 1-composition of isomorphisms is an isomorphism.
1. Let $f$ be an identity 1-cell, and let $g$ be any 1-cell. Then, if there is a composition $f \circ g$ or $g \circ f$, any such value is isomorphic to $g$. It follows (by considering their composition) that identities on equivalent objects are isomorphic, and that when two objects are equivalent, this fact will be witnessed by the identity on either object. 
1. Let $f$, $g$, and $h$ be 2-cells. If $F = f \circ_2 g$, and $G = g \circ_2 h$, then $F \circ_2 h = f \circ_2 G$. (The latter values exist because the set of targets of $G$ and $g$ are equal, as are the set of sources of $g$ and $F$.)
1. Let $f$, $g$, and $h$ be 2-cells. If $F = f \circ_1 g$, and $G = g \circ_1 h$, then $F \circ_1 h = f \circ_1 G$. (The latter values exist because the set of 2-targets of $G$ and $g$ are equal, as are the set of 2-sources of $g$ and $F$.) It follows that composition of 1-cells is also associative, up to isomorphism.
1. Let $f_1$, $f_2$, $g_1$, and $g_2$ be 2-cells. If $F = f_1 \circ_1 f_2$, $G = g_1 \circ_1 g_2$, $H_1 = f_1 \circ_2 g_1$, and $H_2 = f_2 \circ_2 g_2$, then $F \circ_1 G = H_1 \circ_2 H_2$. (It follows from the preceding relations that these compositions exist.)

So every anabicategory is "ana[[skeletal]]" (every equivalence is an identity), and "[[strict category|anastrict]]:" its associators and unitors are also identities.

Every [[bicategory]] can be made into an anabicategory; we simply make the source, target, identity, and composition maps into relations with the original functions as specified values, then define the full values by isomorphism and equivalence. This will satisfy the coherence relations because the original bicategory satisfied the bicategory coherence relations.

On the other hand, we can also assume that every value of the defining relations is specified; then the anabicategory is said to be _saturated_. Any such anabicategory is clearly [[anafunctors|anaequivalent]] to a strict 2-category (just map each object or 1-cell to its equivalence class, and vice versa). For there to be a weak equivalence between the anabicategory and the 2-category, however, we would need the [[Axiom of Choice]] (to pick out a single element of each equivalence class to serve as its image).

# Related pages

* [[probicategory]]

# Reference

*  [[Michael Makkai]]; Avoiding the axiom of choice in general category theory; section 3 (which is part 4 [here](http://www.math.mcgill.ca/makkai/anafun/)).