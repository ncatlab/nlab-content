<div class="rightHandSide toc">
[[!include 2-category theory - contents]]
</div>

# Icons
* table of contents
{: toc}

## Definition

Let $C,D$ be [[2-categories]] and $F,G:C\to D$ be [[functors]].  An **icon** $\alpha:F\to G$ consists of the following:

* the assertion that $F$ and $G$ agree on objects.
* for each morphism $u:x\to y$ in $C$, a 2-cell $\alpha_u:F(u) \to G(u)$ in $D$ (note that this only makes sense because $F$ and $G$ agree on objects, so that $F(u)$ and $G(u)$ are [[parallel morphism|parallel]].
* for each 2-cell $\mu:u\to v$ in $C$, we have $\alpha_v . F(\mu) = G(\mu).\alpha_u$.
* for each object $x$ of $C$, $\alpha_{1_x}$ is an identity (modulo the unit constraints of $F$ and $G$, if they are not strict functors).
* for each [[composable pair]] $x\overset{u}{\to} y \overset{v}{\to} z$ in $C$, we have $\alpha_v {*} \alpha_u = \alpha_{v u}$ (modulo the composition constraints of $F$ and $G$, if they are not strict functors).

If $D$ is a [[strict 2-category]] (or at least strictly unital), then an icon is identical to an [[oplax natural transformation]] whose 1-cell components are identities.  In general, there is a bijection between icons and such oplax natural transformations, obtained by pre- and post-composing with the unit constraints of $D$.  The name "icon" derives from this correspondence: it is an Identity Component Oplax Natural-transformation.


### More general definition for enriched bicategories

Icons have recently been used (cf. ([Sections 3 and 4](#GarnerShulman16)) for constructions in the context of general $\mathcal{V}$-enriched bicategories. (We recall that this is more general than the definition given above in that, roughly speaking, the categories can be enriched in an arbitrary monoidal category, and that moreover the composition-axioms need not hold strictly, but only up to coherent specified 2-isomorphisms).

Even though part of this is already documented on the nLab, to make this article self-contained (within reason), and to fix some notation for later use, we first recall the notion of $\mathcal{V}$-functors, more or less consistently with the notation above.  

Definition ($\mathcal{V}$-functor). 

Let $\mathcal{V}$ be any monoidal category.
Let $C,D$ be $\mathcal{V}$-[[enriched bicategories]]. 
Then a $\mathcal{V}$-functor $F:C\rightarrow D$ consists of the following data:

* a class-function $Ob(C)\rightarrow Ob(D)$

* for each pair $o_0,o_1$ of objects of $C$, a morphism $C(o,o')\overset{F_{o_0,o_1}}{\rightarrow}D(F(o_0),F({o_1}))$ of the category $\mathcal{V}$

* for each object $o$ of $C$ and for each triple $o,o',o''$ of objects of $C$, the following 2-morphisms (ensuring that the functoriality-morphisms are compatible with the unit- and composition morphisms).

(... to be continued)

## Applications

Icons have technical importance in the theory of 2-categories.  For instance, there is no 2-category (or even 3-category) of 2-categories, functors, and lax or oplax transformations (even with modifications), but there is a 2-category of 2-categories, functors, and icons.  (In fact, this 2-category is the 2-category of algebras for a certain [[2-monad]].)

Additionally, if [[monoidal categories]] are regarded as one-object 2-categories, then monoidal functors can be identified with 2-functors, and monoidal transformations can be identified with icons.

Icons are also used to construct [[distributors]] in the context of enriched bicategories.



## References

* {#Lack10} Stephen Lack, _Icons_. Appl. Categ. Structures. Volume 18, Issue 3,(2010), pp 289&#8211;307. [arxiv:0711.4657](http://arxiv.org/abs/0711.4657)

* {#GarnerShulman16} R. Garner, M. Shulman. Enriched categories as a free cocompletion. Adv. Math. 289 (2016), 1--94. especially Section 3.8


[[!redirects icon]]
[[!redirects icons]]
