
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Span rewriting

* table of contents
{: toc}

## Idea

Span rewriting is a collection of abstract [[category theory|category-theoretic]] methods of using [[spans]] to "rewrite" [[objects]] in a [[category]] by "deleting" part of them and replacing it with a substitute part that retains some of the same "connections" between the deleted part and the rest of the object.

The most common application is to the category of [[quivers]] (called [[directed graphs|(directed) graphs]] in the relevant literature) or related categories; thus span rewriting is often called "graph rewriting".

There is probably not much connection to algebraic [[rewriting]].

## Definitions

All the definitions below have the following context in common.  A **production** or **rule** in a category (often the category [[Quiv]] of [[quivers]]) is a [[span]]

$$ L \xleftarrow{l} K \xrightarrow{r} R. $$

A **match** for this production is a morphism $f:L\to C$ for some object $C$.  A **derivation** of a match along a production is supposed to be a new object obtained by "deleting the image of $L$ and replacing it with $R$".

A production is **left-linear** if $l$ is a [[monomorphism]], and **linear** if in addition $r$ is a monomorphism.

### Double pushout rewriting

For this definition, we work in an [[adhesive category]] (which includes all [[toposes]], hence in particular $Quiv$).  Given a left-linear production $ L \xleftarrow{l} K \xrightarrow{r} R$, a match $f:L\to C$ satisfies the **gluing condition** if the pair $(l,f)$ has a [[pushout complement]] consisting of $g:K\to E$ and $v:E\to C$.  In this case the **(double-pushout) derivation** associated to the match is the pushout of $g$ along $r$, yielding a pair of pushout squares

$$\array{ L & \xleftarrow{l} & K & \xrightarrow{r} & R \\
^f\downarrow && \downarrow^{\mathrlap{g}} && \downarrow \\
C & \xleftarrow{v}  & E & \to & D.}$$

The restriction of $l$ to be monic is necessary to ensure that pushout complements are essentially unique when they exist.  Often we further restrict $r$ to be monic to ensure overall good behavior, obtaining the notion of **linear production**.

[Lack and Sobocinski](#LS) describe the intuition in this way:

> in order to perform the rewrite, we need to match $L$ as a substructure of a redex $C$. The structure $K$, thought of as a substructure of $L$, is exactly the part of $L$ which is to remain invariant as we apply the rule to $C$. Finally, parts of $R$ which are not in $K$ should be added to produce the final result of the rewrite.

> Thus, an application of a rewrite rule consists of three steps. First we must match $L$ as a substructure of the redex C; secondly, we delete all of parts of the redex matched by $L$ which are not included in $K$. Thirdly, we add all of $R$ which is not contained in $K$, thereby producing a new structure $D$.  The deletion and addition of structure is handled, respectively, by finding a pushout complement and constructing a pushout.


### Sesqui-pushout rewriting

In an adhesive category, the pushout of a monomorphism is also a pullback.  Thus, the pushout complements involved in double-pushout rewriting are also "pullback complements".  Pullback complements are not in general unique, even in an adhesive category, but those arising as pushout complements do satisfy a [[universal property]]: they are [[final pullback complements]].

This suggests the following generalization.  In an arbitrary category, given an arbitrary production $ L \xleftarrow{l} K \xrightarrow{r} R $, the **(sesqui-pushout) derivation** associated to a match $f:L\to C$ is a diagram

$$\array{ L & \xleftarrow{l} & K & \xrightarrow{r} & R \\
^f\downarrow && \downarrow^{\mathrlap{g}} && \downarrow \\
C & \xleftarrow{v}  & E & \to & D.}$$

in which the left square is a final pullback complement and the right square is a pushout.  Such a derivation may or may not exist, but if it does then it is essentially unique.  Moreover, if we are in an adhesive category and $l$ is monic, then any double-pushout derivation is also a sesqui-pushout derivation.  

More generally, given the construction of final pullback complements using [[exponential objects]], if the exponential $\Pi_f l$ exists and the [[counit]] $f^* \Pi_f l \to l$ is an isomorphism, then such a derivation exists with $E = \Pi_f l$.  In particular, this happens in any [[locally cartesian closed category]] if $f$ and $l$ are both monomorphisms.


### Single pushout rewriting

We can also regard a left-linear production as a [[partial morphism]], in which case the universal property of a final pullback complement suggests the following different viewpoint.  Given a left-linear production $ L \xleftarrow{l} K \xrightarrow{r} R $, the **(single-pushout) derivation** associated to a match $f:L\to C$ is the [[pushout]] of $(l,r)$ and $f$ in the category of partial morphisms (if it exists).

It can be shown (see [CHHK](#CHHK)) that in a certain abstract context, any sesqui-pushout derivation of a left-linear production is also a single-pushout derivation; and that the converse holds if and only if the match is "conflict-free", and if and only if the induced partial morphism from $R$ to the target object $D$ is total.


### General gluing constructions

In [Lowe10](#Lowe10) and [Lowe12](#Lowe12) a yet more general construction is considered for span rewriting, involving $3\times 3$ diagrams consisting of a pullback, two final pullback complements, and a pushout.


## References

* H. Ehrig, M. Pfender, and H.J. Schneider, _Graph-grammars: an algebraic approach_, In IEEE Conf. on Automata and Switching Theory, pages 167&#8211;180, 1973.

* [[Steve Lack]] and [[Pawel Sobocinski]], *Adhesive categories*, [PDF](http://users.ecs.soton.ac.uk/ps/papers/adhesive.pdf)
 {#LS}

* Andrea Corradini, Tobias Heindel, Frank Hermann, and Barbara K&#246;nig, *Sesqui-pushout rewriting*, 2006, [springerlink](https://link.springer.com/chapter/10.1007/11841883_4), [pdf](http://www.ti.inf.uni-due.de/publications/koenig/icgt06b.pdf).
 {#CHHK}

* Michael L&#246;we, *Graph rewriting in Span-categories*, 2010, [springerlink](https://link.springer.com/chapter/10.1007/978-3-642-15928-2_15)
 {#Lowe10}

* Michael L&#246;we, *Refined graph rewriting in Span-categories*, 2012, [springerlink](https://link.springer.com/chapter/10.1007/978-3-642-33654-6_8)
 {#Lowe12}

* Nicolas Behr, Pawel Sobocinski, *Rule Algebras for Adhesive Categories*, [arXiv:1807.00785](https://arxiv.org/abs/1807.00785)



[[!redirects graph rewriting]]
[[!redirects double pushout graph rewriting]]
[[!redirects double pushout rewriting]]
[[!redirects single pushout graph rewriting]]
[[!redirects single pushout rewriting]]
[[!redirects sesqui-pushout graph rewriting]]
[[!redirects sesqui-pushout rewriting]]
[[!redirects double-pushout rewriting]]