<div class="rightHandSide toc">
[[!include category theory - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}


##Idea##

* A functor is what goes between [[category|categories]].

* A functor from $C$ to $D$ is an _image of $C$ in $D$_.

* A functor between (small) categories is a morphism of the underlying graphs that respects the composition of edges.


##Definition##

A _functor_ $F$ from a [[category]] $C$ to a category $D$ is a map sending each [[object]] $x \in C$ to an object $F(x) \in D$ and each [[morphism]] $f : x \to y$ in $C$ to morphism $F(f) : F(x) \to F(y)$ in $D$, such that

* $F$ preserves [[composition]]: $F(f g) = F(f) F(g)$ whenever the left-hand side is well-defined,

* $F$ preserves [[identity morphisms]]: for each object $x \in X$, $F(1_x) = 1_{F(x)}$.

The functors between two categories $C$ and $D$ form themselves a category, the [[functor category]] $[C,D]$, whose morphisms are [[natural transformations]]. Equipped with these functor categories as [[hom-object]]s, we have a $2$-[[2-category|category]] [[Cat]] of categories, functors and natural transformations.  In other words, functors are [[morphisms]] in $Cat$.


## Special properties ##

Functors with special properties are important in applications. See for instance

* [[essentially surjective functor]]

* [[full functor]]

* [[faithful functor]]

* [[full and faithful functor]]

And for more background on this see [[stuff, structure, property]].


##Internal definition##

Suppose now that $C$ and $D$ are [[internal categories]] in some ambient category $A$.  Then an __internal functor__ $F : C \to D$ is 

* a morphism of objects $F_0 : C_0 \to D_0$ in $A$;

* a morphisms of morphisms $F_1 : C_1 \to D_1$ in $A$;

* such that the following diagrams commute

  * respect for the source map: 
  $
 \array{
  C_1 &\stackrel{f_1}{\to}& D_1
  \\
  \downarrow^s && \downarrow^s
  \\
  C_0 
  &\stackrel{f_0}{\to}&
  D_0
 }
$;

   * respect for the target map: 
  $
 \array{
  C_1 &\stackrel{f_1}{\to}& D_1
  \\
  \downarrow^t && \downarrow^t
  \\
  C_0 
  &\stackrel{f_0}{\to}&
  D_0
 }
$;

   * respect for identities 
  $
 \array{
   C_0 &\stackrel{f_0}{\to}&
   D_0
   \\
   \downarrow^i && \downarrow^i
   \\
   C_1 &\stackrel{f_1}{\to}& D_1
 }
$;

   * respect for composition 
  $
  \array{
    C_1 \times_{t,s} 
   C_1 &\stackrel{f_1\times_{t,s} f_1}{\to}&
   D_1 \times_{t,s} D_1
  \\
   \downarrow^{\circ} && \downarrow^{\circ}
  \\
  C_1 &\stackrel{f_1}{\to}& D_1
  }  
$.

In many cases, this notion is too restrictive, and we should use internal [[anafunctors]] instead.


##Examples ## 


### morphisms of monoids and groups ###

For $A,B$ [[monoid]]s or $G, H$ [[group]]s, let $\mathbf{B}A, \mathbf{B}B$, $\mathbf{B}G$, $\mathbf{B}H$ be the corresponding obe-object [[category|categories]] (as described at [[delooping]]). Then functors

$$
  \mathbf{B}A \to \mathbf{B}B
$$

are canonically in bijection with monoid homomorphisms $A \to B$ and accordingly functors

$$
  \mathbf{B}G \to \mathbf{B}H
$$

are canonically in bijection with group homomorphisms $G \to H$.


### Representations ###

With $\mathbf{B}G$ as above, functors on $\mathbf{B}G$ with values in [[Vect]] are the same as linear [[representation]]s of the [[group]] $G$. In fact, we have a canonical isomorphism of categories

$$
  Funct(\mathbf{B}G, Vect) \simeq Rep(G)
$$

of the [[functor category]] with the representation category.


###Linear Maps###

Let $\mathbf{B} End(U)$ and $\mathbf{B} End(V)$ be one-object categories whose objects are each finite-dimensional vector space and whose morphisms are all of the linear [[endomorphism]]s on that space, i.e. one-object [[full subcategory|full subcategories]] of $Fin Vect$.


####Left Inverses####

If the linear map $F:U\to V$ has a left inverse, i.e.

$$F^*\circ F = 1_U,$$

where $F^*$ is the [[preimage]], then we can construct a functor 

$$F_*:\mathbf{B} End(U)\to\mathbf{B} End(V)$$

by defining its action on objects by

$$F_*(U) = F_* U$$

where $F_*$ on the right-hand side is the [[image]] and its action on endomorphisms by

$$F_*(f) = F f F^*.$$

Composition follows immediately

$$F_*(f g) = F f g F^* = F f F^* F g F^* = F_*(f) F_*(g).$$

Identity morphisms are preserved since for any vector $y$ in $F_*U\subset V$, then 

$$y = F x$$

for some vector $x$ in $U$ and we have

$$F_*(1_U)y = F\circ F^* y = F\circ F^*\circ F x = F x = y$$

so that

$$F_*(1_U) = 1_{F_*(U)}$$

as required. Hence, $F_*$ is a functor.


####Right Inverses####

If the linear map $F:U\to V$ has a right inverse, i.e.

$$F\circ F^* = 1_V,$$

where $F^*$ is the preimage, then we can construct a functor 

$$F^*:\mathbf{B} End(V)\to\mathbf{B} End(U)$$

by defining its action on objects by

$$F^*(V) = F^*V$$

where $F^*$ on the right-hand side is preimage, and its action on endomorphisms by

$$F^*(f) = F^* f F.$$

Composition follows immediately

$$F^*(f g) = F^* f g F = F^* f F F^* g F = F^*(f) F^*(g).$$

Identity morphisms are preserved since for any vector $x$ in $F^*V\subset U$, then 

$$x = F^*y$$

for some vector $y$ in $V$ and we have

$$F^*(1_V)x = F^*\circ F x = F^*\circ F \circ F^* y = F^* y = x$$

so that

$$F^*(1_V) = 1_{F^*(V)}$$

as required. Hence, $F^*$ is a functor.


### Presheaves ###

Functors $F : C \to Set$ with values in [[Set]] are also called [[presheaf|presheaves]]. As such one calls them presheaves on the [[opposite category]] $C^{op}$ of $C$. See [[presheaf]] for more on this.



## Generalizations ##

A generalization of the notion of functor within ordinary [[category theory]] and then naturally further within [[enriched category theory]] is the notion of [[profunctor]].

In [[higher category theory]] there are corresponding higher notions of functor, such as

* [[2-functor]]

  * [[strict 2-functor]]

  * [[pseudofunctor]]

  * [[lax functor]]

* [[(∞,1)-functor]]


* See also [[Eric Forgy]]\'s [[experimental alternative definition of functor]].


[[!redirects functors]]