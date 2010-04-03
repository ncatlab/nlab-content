
#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A **diagram** in a [[category]] $C$ is simply a [[functor]] $F: J \to C$. 

The category $J$ is called the **shape** or **index category** of the diagram, and is typically understood to be a [[small category]]. 

One speaks of such functors as diagrams for instance 

* when the [[limit]] or [[colimit]] over the functor is considered. This is then  often called the limit or colimit of the corresponding diagram. 

* when _commuting diagrams_ are considered: a **[[commuting diagram]]** in $C$ is a diagram for which $J$ is a [[poset]]. 

  So a commuting diagram is a diagram where every two morphisms in $C$ that are assigned to any pair of _parallel morphisms in $J$_ (i.e. with same source and target in $J$) are equal. 

## Examples

* The shape of the **empty diagram** is the [[initial object|initial category]] with no object and no morphism. 

  Every category $C$ admits a unique diagram whose shape is the empty ([[initial object|initial]]) category, which is called the **empty diagram** in $C$.

* The shape of the **terminal diagram** is the [[terminal category]] $J = \{*\}$ consisting of a single object and a single morphism (the identity morphism on that object). 

  Specifying a diagram in $C$ whose shape is $\{*\}$ is the same as specifying a single [[object]] of $C$, the image of the unique object of $1$. (See [[global element]])


* A diagram of the shape $\{a \to b\}$ in $C$ is the choice of any one [[morphism]] $F_{a b} : X_a \to X_b$ in $C$.

  Notice that strictly speaking this counts as a _commuting diagram_ , but is a degenrate case of a commuting diagram, since there is only a single morphism involved, which is necessarily equal to itself.

* A diagram of shape the [[poset]] indicated by

  $$
    \left\{
      \array{
         a &\to& b
         \\
         \downarrow && \downarrow
         \\
         b' &\to& c
      }
    \right\}
  $$

  is a **commuting square** in $C$: this is a choice of four (not necessarily distinct!) objects $X_a, X_b, X_{b'}, X_c$ in C, together with a choice of (not necessarily distinct) four morphisms $F_{a b} : X_a \to X_b$, $F_{b c} : X_b \to X_c$ and $F_{a b'} : X_a \to X_{b'}$, $F_{b' c} : X_{b'} \to X_c$ in $C$, such that the composite morphism $F_{b c}\circ F_{a b}$ equals the composite $F_{b' c}\circ F_{a b'}$.

  One typically "draws the diagram" as

  $$
      \array{
         X_a &\stackrel{F_{a b}}{\to}& X_b
         \\
         {}^{\mathllap{F_{a b'}}}\downarrow && 
        \downarrow^{\mathrlap{F_{b c}}}
         \\
         X_{b'} &\stackrel{F_{b' c}}{\to}& X_{c}
      }    
  $$

  in $C$ and says that _the diagram commutes_ if the above equality of composite morphisms holds.

  Notice that the original poset had, necessarily, a morphism $a \to c$ and could have equivalently be depicted as

  $$
    \left\{
      \array{
         a &\to& b
         \\
         \downarrow &\searrow& \downarrow
         \\
         b' &\to& c
      }
    \right\}
  $$

  in which case we could more explicitly draw its image in $C$ as

  $$
      \array{
         X_a &\stackrel{F_{a b}}{\to}& X_b
         \\
         {}^{\mathllap{F_{a b'}}}\downarrow &\searrow^{\stackrel{F_{b c}\circ F_{a b}}{= F_{b' c}\circ F_{a b'}}}& 
        \downarrow^{\mathrlap{F_{b c}}}
         \\
         X_{b'} &\stackrel{F_{b' c}}{\to}& X_{c}
      }    
  $$


* A pair of objects is a diagram whose shape is a [[discrete category]] with two objects.


* A pair of [[parallel morphisms]] is a diagram whose shape is a category 
  $J = \{a \stackrel{\to}{\to} b\}$
  with two objects and two morphisms from one to the other. 

  Notice that if we required  $\{a \stackrel{\to}{\to} b\}$ to be a [[poset]] this would necessarily make these two morphisms equal, and hence reduce this example to the one where $J = \{a \to b\}$. 

* A [[span]] is a diagram whose shape is a category with just three objects and single morphisms from one of the objects to the other two; 

  $$
    J = \left\{
      \array{
        && a
        \\
        & \swarrow && \searrow
        \\
        b &&&& c
      }
    \right\}
  $$

  dually, a [[cospan]] is a diagram whose shape is [[opposite category|opposite]] to the shape of a span.

  $$
    J = \left\{
      \array{
        b &&&& c
        \\
        & \searrow && \swarrow
        \\
        && a
      }
    \right\}
  $$

* A [[transfinite composition]] diagram is one of the shape the [[poset]] indicated by

  $$
    J = 
    \left\{
     \array{
      a_0 &\to& a_1 &\to& \cdots 
      \\
      & \searrow & \downarrow & \swarrow & \cdots 
      \\
      && b
     }
    \right\}
    \,,
  $$

  where the indices may range over the [[natural number]]s or even some more general [[ordinal number]].

  This is non-finite commuting diagram.


[[!redirects diagram]]
[[!redirects diagrams]]
