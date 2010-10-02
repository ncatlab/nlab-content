
# Premonoidal categories
* table of contents
{: toc}

## Idea

A premonoidal category is a generalisation of a [[monoidal category]], applied by [[John Power]] and his collaborators to [[denotational semantics]] in [[computer science]].

Recall that a [[bifunctor]] to $C$ from $D$ and $E$ (for $C,D,E$ [[categories]]) is simply a [[functor]] to $E$ from the [[product category]] $C \times D$.  We can think of this as an operation which is 'jointly functorial'.  But just as a [[function]] to $X$ from $Y$ and $Z$ (for $X,Y,Z$ [[topological spaces]]) may be [[continuous map|continuous]] in each variable yet not [[jointly continuous function|jointly continuous]] (continuous from the [[Tychonoff product]] $Y \times Z$), so an operation between categories can be functorial in each variable separately yet not jointly functorial.

Recall that a [[monoidal category]] is a [[category]] $C$ equipped with a bifunctor $C \times C \to C$ (equipped with [[extra structure]] such as the [[associator]]).  Similarly, a premonoidal category is a category equipped with an operation $C \times C \to C$, which is (at least) a [[function]] on [[objects]] as shown, but one which is functorial only in each variable separately.


## Definition

A __binoidal category__ is a [[category]] $C$ equipped with

*  for each pair $x,y$ of [[objects]] of $C$, an object $x \otimes y$;
*  for each object $x$ a [[functor]] $x \rtimes -$ whose action on objects sends $y$ to $x \otimes y$
*  for each object $x$ a [[functor]] $- \ltimes x$ whose action on objects sends $y$ to $y \otimes x$

A [[morphism]] $f\colon x \to y$ in a binoidal category is __central__ if, for every morphism $f'\colon x' \to y'$, the diagrams
$$ \array {
   x \otimes x'                      & \overset{x \rtimes f'}\to  & x \otimes y' \\
   \mathllap{f \ltimes x'}\downarrow &                            & \downarrow\mathrlap{f \ltimes y'} \\
   y \otimes x'                      & \underset{y \rtimes f'}\to & y \otimes y' \\
   } $$
and
$$ \array {
   x' \otimes x                      & \overset{x' \rtimes f}\to  & x' \otimes y \\
   \mathllap{f' \ltimes x}\downarrow &                            & \downarrow\mathrlap{f' \ltimes y} \\
   y' \otimes x                      & \underset{y' \rtimes f}\to & y' \otimes y \\
   } $$
commute.  In this case, we denote the common composites $f \otimes f'\colon x \otimes x' \to y \otimes y'$ and $f' \otimes f\colon x' \otimes x \to y' \otimes y$.

A __premonoidal category__ is a binoidal category equipped with:

*  an object $I$;
*  for each triple $x,y,z$ of objects, a central [[isomorphism]] $\alpha_{x,y,z}\colon (x \otimes y) \otimes z \to x \otimes (y \otimes z)$; and
*  for each object $x$, central isomorphisms $\lambda_x\colon x \otimes I \to x$ and $\rho_x\colon I \otimes x \to x$;

such that:

*  the [[naturality square]]s for $\alpha$, $\lambda$, and $\rho$ (which make sense since we have central morphisms) commute;
*  the [[pentagon identity]] holds for $\alpha$; and
*  the [[triangle identity]] holds for $\lambda$ and $\rho$.

A __strict premonoidal category__ is a monoidal category in which $(x \otimes y) \otimes z = x \otimes (y \otimes z)$, $x \otimes I = x$, and $I \otimes x = x$, and in which $\alpha_{x,y,z}$, $\lambda_x$, and $\rho_x$ are all [[identity morphisms]].  (We need the underlying category $C$ to be a [[strict category]] for this to make sense.)


## Slick version

As a [[strict monoidal category]] is a [[monoid]] in the [[cartesian monoidal category]] [[Cat]], so a premonoidal category is a monoid in another [[symmetric monoidal category]] whose underlying category is also $Cat$.

Given [[categories]] $C,D$ and [[functors]] $F,G\colon C \to D$, a (*not* necessarily natural) __transformation__ from $F$ to $G$ consists of, for each object $x$ of $C$, a morphism from $F(x)$ to $G(x)$ in $D$.  (So a [[natural transformation]] is a transformation that satisfies an [[extra property]].)  We can compose transformations using [[vertical composition]] (but *not* [[horizontal composition]]).

Given categories $C,D$, let $C \Rightarrow D$ be the category whose objects are functors from $C$ to $D$ and whose morphisms are transformations between these functors.  This makes $Cat$ into a [[closed category]].  We can then define a [[tensor product]] by a [[universal property]] and make $Cat$ into a [[monoidal category]] $(Cat,\otimes)$ which is in fact symmetric.

Then a strict premonoidal category is precisely a [[monoid object]] in $(Cat,\otimes)$.

It should be possible to weaken the above make $(Cat,\otimes)$ a [[symmetric monoidal 2-category]], in which a monoid object is precisely a premonoidal category, but if so, nobody seems to have written this up yet.


## Properties

Every [[monoidal category]] is a premonoidal category.

The central morphisms of a premonoidal category $C$ form a [[subcategory]] $Z(C)$, called the __centre__ of $C$, which is a [[monoidal category]].

The above properties combine to form an [[adjunction]] $Pre Mon Cat \leftrightarrows Mon Cat$.  (I haven\'t actually checked this.)


## References

*  [[John Power]] and [[Edmund Robinson]]; 1993; _Premonoidal categories and notions of computation_; [PostScript](http://www.eecs.qmul.ac.uk/~edmundr/pubs/mscs97/premoncat.ps)

## Discussion

There's been a lot of discussion of this on the $n$-Category Caf&#233; --- someone find it and cite it!


+-- {: .query}
[[Adam]]: I believe that the "naturality square" for $\alpha$ above actually requires three distinct natural isomorphisms for three different ways of composing the binoidality functors (LL=L, RR=R, LR=RL):

* $(a \rtimes -)\circ(b \rtimes -) \simeq ((a \otimes b) \rtimes -)$
* $(- \ltimes c)\circ(- \ltimes b) \simeq (- \ltimes (b \otimes c))$
* $(a \rtimes -)\circ(- \ltimes c) \simeq (- \ltimes c)\circ(a \rtimes -)$

I have a Coq formalization of binoidal/premonoidal categories and I wasn't able to make things work without all three.  Perhaps there's a way to capture them all with a single natural iso, but I couldn't find it.  In a monoidal category these all collapse into a single natural iso because we're dealing with a single bifunctor rather than two separate functors.

I also suspect that all useful binoidal categories have the first two natural isos.  I'm having a hard time finding an example which doesn't.
=--

[[!redirects premonoidal category]]
[[!redirects premonoidal categories]]

[[!redirects binoidal category]]
[[!redirects binoidal categories]]
