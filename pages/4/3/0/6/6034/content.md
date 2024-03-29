
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In the philosophy of the [[Grothendieck]] school, one starts with some [[category]] $C$ of "local models" of [[spaces]], equips it with a [[subcanonical topology|subcanonical]] [[Grothendieck topology]], $\tau$, and enlarges $C$ to some category of [[sheaf|sheaves of sets]] on the [[site]] $(C,\tau)$ playing the role of *spaces*. There are further generalizations to [[stacks]] and so on.

When doing this, we often find that properties of "local model spaces" $X\in C$ have to be extended to properties of arbitrary spaces (i.e. sheaves on $(C,\tau)$).  In fact it is most natural to do this in a *relative* situation, i.e. to talk about properties of _morphisms_ rather than properties of _objects_, with an object $X$ regarded as the morphism $X\to 1$.  Thus, one of the main steps in the construction of the theory is to extend good classes of morphisms of local models to the category of spaces. Grothendieck axiomatizes the situation, actually for general presheaves.

Representable morphisms are also important in [[algebraic set theory]] and appear implicitly in the notion of [[category with families]].


## Definition

Let $\mathcal{P}$ be a class of [[morphisms]] in a [[category]] $C$ which is closed under isomorphisms, i.e. it is [[replete subcategory|replete]] when regarded as a [[full subcategory]] of the [[arrow category]] of $C$.

+-- {: .un_defn}
###### Definition
A morphism $\alpha : F\to G$ of [[presheaves]] of sets on $C$ is said to be __representable by a morphism in__ $\mathcal{P}$ if for every morphism from a representable presheaf $h_X\to G$, the projection from the pullback $F\times_G h_X\to h_X$ is (the image under the [[Yoneda embedding]] of) a morphism in $\mathcal{P}$.

When $\mathcal{P}$ is the class of all morphisms in $C$, we simply say that $\alpha$ is __representable__.
=--

In geometrical contexts, we usually assume that $\mathcal{P}$ is itself closed under pullbacks in $C$, i.e. if $f: X\to Y$ is in $\mathcal{P}$ and $g : V\to Y$ a morphism in $C$, then the [[pullback]] $X\times_Y V$ exists and the projection $X\times_Y V\to V$ is in $\mathcal{P}$.  If $C$ has all pullbacks, then the class of *all* morphisms in $C$ satisfies this property.

If $\mathcal{P}$ is closed under pullback, then a morphism $h_X\to h_Y$ between representable presheaves is representable by a morphism in $\mathcal{P}$ if and only if it is itself (the image under the Yoneda embedding of) a morphism in $\mathcal{P}$.  In this way, the class $\mathcal{P}$ of morphisms in $C$ is extended to a class $\hat{\mathcal{P}}$ of morphisms in the category of presheaves of sets $\hat{C} = Set^{C^{op}}$.


## Examples

* [[representable morphism of stacks]] (extends this notion from presheaves to stacks)

[[!redirects representable morphisms]]
[[!redirects representable morphism of presheaves]]
[[!redirects representable morphisms of presheaves]]
[[!redirects representable natural transformation]]

