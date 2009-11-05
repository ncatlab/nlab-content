<div class="rightHandSide toc">
[[!include category theory - contents]]
</div>


##Idea##

* A functor is what goes between [[category|categories]].

* A functor from $C$ to $D$ is an _image of $C$ in $D$_.

* A functor between (small) categories is a morphism of the underlying graphs that respects the composition of edges.

More precisely, a _functor_ $F$ from a category $C$ to a category $D$ is a map sending each object $x \in C$ to an object $F(x) \in D$ and each morphisms $f : x \to y$ in $C$ to morphism $F(f) : F(x) \to F(y)$ in $D$.  We demand that:

* $F$ preserves [[composition]]: $F(f g) = F(f) F(g)$ whenever either side is well-defined.

* $F$ preserves identity morphisms: for each object $x \in X$, $F(1_x) = 1_{F(x)}$.

Functors are morphisms in the category [[Cat]].

##Internal definition##

[[internalization|Internal to]] an ambient category $A$, a functor $F : C \to D$ is 

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

However, see [[anafunctor]] for a different approach.

##Example: Linear Maps##

Let $\mathbf{B} End(U)$ and $\mathbf{B} End(V)$ be one-object categories whose objects are each finite-dimensional vector space and whose morphisms are all of the linear [[endomorphism]]s on that space, i.e. one-object [[full subcategory|full subcategories]] of $Fin Vect$.

###Left Inverses###

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

###Right Inverses###

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

##Discussion##

[[Eric]]: Motivated by some discussion over at [[natural transformation]], I was wondering if the following alternative definition of functor holds water:

>##Definition##
>Given categories $A$, $B$, a **functor** is a map $F:A\to B$ that assigns maps $\alpha_x:x\to F(x)$ and $\alpha_y:y\to F(y)$ for any morphism $f:x\to y$ in $A$ such that the following diagram commutes:
$$ 
  \array{ 
    x
    & 
    \stackrel{f}{\to} 
    & 
    y 
    \\ 
    \mathllap{\scriptsize{\alpha_x}}\downarrow 
    && 
    \downarrow\mathrlap{\scriptsize{\alpha_y}} 
    \\ F(x) 
    & 
    \stackrel{F(f)}{\to} & F(y) 
  }
$$

If so, it has a certain beauty that appeals to me. Thanks!

Urs: that diagram seems to be meaningful only if $A = B$, right? In that case, this is a functor $F : A \to A$ together with a natural transformation from the identity functor on $A$ into $F$.

[[!redirects functors]]