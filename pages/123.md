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

$$F_L^{-1}\circ F = 1_U,$$

then we can construct a functor 

$$F:\mathbf{B} End(U)\to\mathbf{B} End(V)$$

by defining its action on objects by

$$F(U) = F U$$

and its action on endomorphisms by

$$F(f) = F f F_L^{-1}.$$

Composition follows immediately

$$F(f g) = F f g F_L^{-1} = F f F_L^{-1} F g F_L^{-1} = F(f) F(g).$$

Identity morphisms are preserved since for any vector $y$ in $F(U)\subset V$, then 

$$y = F x$$

for some vector $x$ in $U$ and we have

$$F(1_U)y = F\circ F_L^{-1}y = F\circ F_L^{-1}\circ F x = F x = y$$

so that

$$F(1_U) = 1_{F(U)}$$

as required. Hence, $F$ is a functor.

###Right Inverses###

If the linear map $F:U\to V$ has a right inverse, i.e.

$$F\circ F_R^{-1} = 1_V,$$

then we can construct a functor 

$$F^*:\mathbf{B} End(V)\to\mathbf{B} End(U)$$

by defining its action on objects by

$$F^*(V) = F_R^{-1}(V)$$

and its action on endomorphisms by

$$F^*(f) = F_R^{-1} f F.$$

Composition follows immediately

$$F^*(f g) = F_R^{-1} f g F = F_R^{-1} f F F_R^{-1} g F = F^*(f) F^*(g).$$

Identity morphisms are preserved since for any vector $x$ in $F_R^{-1}(V)\subset U$, then 

$$x = F_R^{-1}y$$

for some vector $y$ in $V$ and we have

$$F^*(1_V)x = F_R^{-1}\circ F x = F_R^{-1}\circ F \circ F_R^{-1} y = F_R^{-1} y = x$$

so that

$$F^*(1_V) = 1_{F^*(V)}$$

as required. Hence, $F^*$ is a functor.