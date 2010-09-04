+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}


## Idea

* A functor is what goes between [[category|categories]].

* A functor from $C$ to $D$ is an _image of $C$ in $D$_ (but the naive [[image]] need not be a [[subcategory]] of $D$).

* A functor between (small) categories is a morphism of the underlying [[directed graphs]] that respects the composition of edges.


So a functor $F : C \to D$ is a [[morphism]] between two [[category|categories]] that 

* constsis of a map $F_0 : Obj(C) \to Obj(D)$ of the objects of the categories

* and a map $F_1 : Mor(C) \to Mor(D)$ of the morphisms of the categories

such that

* it respect source and target: $F_1$ coincides with $F_0$ on source and target objects;

* it respects composition: the image of the composite of two morphisms under $F$ is the composite of their images.

This last property is the decicive one of a functor. It is called the **functoriality condition**. It is a direct generalization of the notion of [[homomorphism]] (of [[monoids]], [[groups]], [[algebras]], etc.) to the case that there are more objects. As a slogan we have

The notion of functor is a [[horizontal categorification]] of that of [[homomorphism]].

## Definition

### External definition

A **functor** $F$ from a [[category]] $C$ to a category $D$ is a map sending each [[object]] $x \in C$ to an object $F(x) \in D$ and each [[morphism]] $f : x \to y$ in $C$ to morphism $F(f) : F(x) \to F(y)$ in $D$, such that

* $F$ preserves [[composition]]: $F(g\circ f) = F(g)\circ F(f)$ whenever the left-hand side is well-defined,

* $F$ preserves [[identity morphisms]]: for each object $x \in X$, $F(1_x) = 1_{F(x)}$.

Or equivalently, since compositions $g f = g\circ f$ (commuting triangles) and identities $1_x$ (commuting loops) are both simple commuting diagrams, we can combine the above conditions to the single statement

* $F$ preserves commuting diagrams.

Given morphisms $f:X\to Y$, $g:Y\to Z$, and $h:X\to Z$, declaring the triangle commutes amounts to declaring 
$$h = g\circ f.$$ 
In this case, for $F:C\to D$ to preserve the commutative triangle means 
$$F(h) = F(g)\circ F(f)$$
as depicted below

<img src="http://ncatlab.org/nlab/files/functor.jpg" width = "300"/>

Preserving commuting triangles means $F$ preserves compositions. 

Given morphisms $f:X\to Y$, $g:Y\to Z$, and $h:Z\to X$, declaring the loop commutes amounts to declaring 
$$1_X = h\circ g\circ f.$$
In this case, for $F:C\to D$ to preserve the commutative loop means 
$$F(1_X) = F(h)\circ F(g)\circ F(f)$$
as depicted below

<img src="http://ncatlab.org/nlab/files/commuteloop.jpg" width = "300"/>

However, it means more than that. Since any commutative loop is equal to the identity morphism, we must also have
$$1_{F(X)} = F(h)\circ F(g)\circ F(f)$$
implying
$$F(1_X) = 1_{F(X)}.$$

Preserving commuting loops means $F$ preserves identity morphisms.

Another equivalent way to say this is that a functor $F : C \to D$ is precisely a morphism of [[simplicial sets]] $N(F) : N(C) \to N(D)$ between the [[nerves]] of these categories

* the [[objects]] of $C$ and $D$ are the 0-cells of $N(C)$ and $N(D)$, so $N(F)_0 : N(F)_0 \to N(F)_0$ maps objects of $C$ to objects of $D$;

* the [[morphisms]] of $C$ and $D$ are the 1-cells of $N(C)$ and $N(D)$, so $N(F)_1 : N(F)_1 \to N(F)_1$ maps morphisms of $C$ to objects of $D$;

* the identity morphisms of $C$ and $D$ are the degenerate 1-cellsof $N(C)$ and $N(D)$, so the fact that $N(F)$ respects degeneracy maps means that $F$ respects identities;

* the commuting triangles of $C$ and $D$ are the 2-cells of $N(C)$ and $N(D)$, so the fact that $N(F)$ maps 2-cells to 2-cells means that it respects commuting triangles, hence that it respects composition.

See [[nerve]] for more details on this.


The functors between two categories $C$ and $D$ form themselves a category, the [[functor category]] $[C,D]$, whose morphisms are [[natural transformations]]. Equipped with these functor categories as [[hom-objects]], we have a $2$-[[2-category|category]] [[Cat]] of categories, functors and natural transformations.  In other words, functors are [[morphisms]] in $Cat$.

### Internal definition {#InternalDefinition}

If $C$ and $D$ are [[internal categories]] in some ambient category $A$, then an __internal functor__ $F : C \to D$ is 

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

This reproducces the external definition of functors above for [[small categories]], which are categories [[internalization|internal to]] [[Set]]

In many cases, this notion is too restrictive, and we should use internal [[anafunctors]] instead.


### Enriched definition

In [[enriched category theory]] a functor maps not [[hom-sets]] but the given [[hom-objects]] to each other, in a way that respects their composition. This is described at

* [[enriched functor]].


### Profunctors

A generalization of the notion of [[enriched functor]] is the notion of [[profunctor]].

### Higher categorical functors

In [[higher category theory]] there are corresponding higher notions of functor, such as

* [[2-functor]]

  * [[strict 2-functor]]

  * [[pseudofunctor]]

  * [[lax functor]]

* [[(∞,1)-functor]]


* See also an informal discussion about an [[experimental alternative definition of functor]].


## Special properties of functors

Functors with special properties are important in applications. See for instance

* [[essentially surjective functor]]

* [[full functor]]

* [[faithful functor]]

* [[full and faithful functor]]

And for more background on this see [[stuff, structure, property]].


##Examples 

### Morphisms of monoids and groups 

For $A,B$ [[monoids]] or $G, H$ [[groups]], let $\mathbf{B}A, \mathbf{B}B$, $\mathbf{B}G$, $\mathbf{B}H$ be the corresponding obe-object [[category|categories]] (as described at [[delooping]]). Then functors

$$
  \mathbf{B}A \to \mathbf{B}B
$$

are canonically in bijection with monoid homomorphisms $A \to B$ and accordingly functors

$$
  \mathbf{B}G \to \mathbf{B}H
$$

are canonically in bijection with group homomorphisms $G \to H$.


### Representations 

With $\mathbf{B}G$ as above, functors on $\mathbf{B}G$ with values in [[Vect]] are the same as linear [[representations]] of the [[group]] $G$. In fact, we have a canonical isomorphism of categories

$$
  Funct(\mathbf{B}G, Vect) \simeq Rep(G)
$$

of the [[functor category]] with the representation category.


### Linear Maps

Let $\mathbf{B} End(U)$ and $\mathbf{B} End(V)$ be one-object categories whose objects are each finite-dimensional vector space and whose morphisms are all of the linear [[endomorphisms]] on that space, i.e. one-object [[full subcategory|full subcategories]] of $Fin Vect$.


#### Left Inverses

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


#### Right Inverses

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


### Presheaves 

Functors $F : C \to Set$ with values in [[Set]] are also called [[presheaf|presheaves]]. As such one calls them presheaves on the [[opposite category]] $C^{op}$ of $C$. See [[presheaf]] for more on this.


### Functors and generalized elements {#OnGeneralizedElements}

For $C$ a [[category]], and $X \in C$ an [[object]], and $U$ any other object, a [[morphism]] $x : U \to X$ may be regarded as a [[generalized element]] of $X$, written $x \in X$ (For this language applied to the category [[Set]] of sets see [[ETCS]]. For the general case see [[type theory]]).

The _[[set]]_ of generalized elements of an object $X \in C$ is thus the union of [[hom-sets]] $\coprod_{U \in C} Hom_C(U,X)$.

While a [[morphism]] $f : X \to Y$ in an  arbitrary category $C$ need not at all come to us as a function of sets, it always induces a function of sets of _generalized elements_ : it sends the generalized element $x : U \to X$ of $X$ to the generalized element 

$$
  f(x) : U \stackrel{x}{\to} X \stackrel{f}{\to} Y
$$ 

of $Y$, using the composition of the morphism $f$ with the morphism $x$ in $C$.

In terms of this notation, the functoriality condition on a functor $F : C \to D$, which is 

$$
  F(U \stackrel{x}{\to} X \stackrel{f}{\to} Y)
  =
  F(U) \stackrel{F(x)}{\to} F(X) \stackrel{F(f)}{\to} F(Y)
$$

appears as

$$
  F(f(x)) = F(f)(F(x))
  \,.
$$

This can be illustrated in the following diagram

<img src="http://ncatlab.org/nlab/files/altfunctor.jpg" width = "300"/>

which provides an alternative expression of the functoriality condition as simply a statement that commuting diagrams in $C$ map to commuting diagrams in $D$.

[[!redirects functors]]
[[!redirects covariant functor]]
[[!redirects covariant functors]]

[[!redirects internal functor]]
[[!redirects internal functors]]