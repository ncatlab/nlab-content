#Idea#

* A functor is what goes between [[category|categories]].

* A functor from $C$ to $D$ is an _image of $C$ in $D$_.

* A functor between (small) categories is a morphism of the underlying graphs that respects the composition of edges.

More precisely, a _functor_ $F$ from a category $C$ to a category $D$ is a map sending each object $x \in C$ to an object $F(x) \in D$ and each morphisms $f : x \to y$ in $C$ to morphism $F(f) : F(x) \to F(y)$ in $D$.  We demand that:

* $F$ preserves [[composition]]: $F(f g) = F(f) F(g)$ whenever either side is well-defined.

* $F$ preserves identity morphisms: for each object $x \in X$, $F(1_x) = 1_{F(x)}$.

Functors are morphisms in the category [[Cat]].

#Internal definition#

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

