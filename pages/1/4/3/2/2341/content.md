+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--



# Icons
* table of contents
{: toc}

## Definition

### For 2-categories

Let $C,D$ be [[2-categories]] and $F,G:C\to D$ be [[functors]].  An **icon** $\alpha:F\to G$ consists of the following:

* the assertion that $F$ and $G$ agree on objects.
* for each morphism $u:x\to y$ in $C$, a 2-cell $\alpha_u:F(u) \to G(u)$ in $D$ (note that this only makes sense because $F$ and $G$ agree on objects, so that $F(u)$ and $G(u)$ are [[parallel morphism|parallel]].
* for each 2-cell $\mu:u\to v$ in $C$, we have $\alpha_v . F(\mu) = G(\mu).\alpha_u$.
* for each object $x$ of $C$, $\alpha_{1_x}$ is an identity (modulo the unit constraints of $F$ and $G$, if they are not strict functors).
* for each [[composable pair]] $x\overset{u}{\to} y \overset{v}{\to} z$ in $C$, we have $\alpha_v {*} \alpha_u = \alpha_{v u}$ (modulo the composition constraints of $F$ and $G$, if they are not strict functors).

If $D$ is a [[strict 2-category]] (or at least strictly unital), then an icon is identical to an [[oplax natural transformation]] whose 1-cell components are identities.  In general, there is a bijection between icons and such oplax natural transformations, obtained by pre- and post-composing with the unit constraints of $D$.  The name "icon" derives from this correspondence: it is an Identity Component Oplax Natural-transformation.



## Applications

Icons have technical importance in the theory of 2-categories.  For instance, there is no 2-category (or even 3-category) of 2-categories, functors, and lax or oplax transformations (even with modifications), but there is a 2-category of 2-categories, functors, and icons.  (In fact, this 2-category is the 2-category of algebras for a certain [[2-monad]].)

Additionally, if [[monoidal categories]] are regarded as one-object 2-categories, then monoidal functors can be identified with 2-functors, and monoidal transformations can be identified with icons.

Icons are also used to construct [[distributors]] in the context of enriched bicategories.

## Relation to pseudo double categories

A bicategory can be viewed as a [[pseudo double category]] whose tight-cells are trivial. An icon is then precisely a transformation of oplax functors of pseudo double categories. See [Paré](#Pare13) for details.

## References

* {#Lack10} [[Stephen Lack]], _Icons_. Appl. Categ. Structures. Volume 18, Issue 3,(2010), pp 289&#8211;307. [arxiv:0711.4657](http://arxiv.org/abs/0711.4657)

* {#GarnerShulman16} [[Richard Garner]], [[Mike Shulman]], Section 3.8 of _Enriched categories as a free cocompletion_, Adv. Math. 289 (2016), 1--94

* {#Pare13} [[Robert Paré]]. _Composition of modules for lax functors_. Theory and Applications of Categories 27.16 (2013): 393-444.


[[!redirects icon]]
[[!redirects icons]]
