
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory#
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Informally, a **diagram** in a [[category]] $C$ consists of some [[objects]] of $C$ connected by some [[morphisms]] of $C$.  Frequently when doing category theory, we "draw diagrams" such as
$$\array{A & \overset{f}{\to} & B\\
  ^h\downarrow && \downarrow^k\\
  C& \underset{g}{\to} & D}$$
by drawing some objects (or dots labeled by objects) connected by arrows labeled by morphisms.

This terminology is often used when speaking about [[limits]] and [[colimits]]; that is, we speak about "the limit or colimit of a diagram." 

There are two natural ways to give the notion of "diagram" a formal definition.  One is to say that a diagram is a [[functor]], usually one whose domain is a (very) [[small category]].  This level of generality is sometimes convenient.

On the other hand, a more direct representation of what we draw on the page, when we "draw a diagram," only involves labeling the vertices and edges of a [[directed graph]] (or [[quiver]]) by objects and morphisms of the category.  This sort of diagram can be identified with a functor whose domain is a [[free category]], and this is the most common context when we talk about diagrams "commuting."


## Definitions


### Diagrams shaped like categories
 {#CategoryShapedDiagrams}

We discuss here diagrams of the "shape of a small catgeory", as well as the concept of [[cones]]/[[cocones]] over these and [[limit|limiting]]/[[colimit|colimiting]] (co-)cones. There is a quick abstract functorial definition

* _[functorial definition](#CategoryShapedDiagramFunctorially)_

and there is a more long-winded but more explicit definition in terms of components 

* _[component definition](#CategoryShapedDiagramInComponents)_.

#### Functorial definition
 {#CategoryShapedDiagramFunctorially}

We state the concise functorial definition of diagrams of the shape of categories.

+-- {: .num_defn #AbstractDefinition}
###### Definition
**(functorial definition)**

Let $\mathcal{C}$ be a [[category]] and let  $\mathcal{I}$  [[small category]],

Then 

1. a _diagram $X$ of shape $\mathcal{I}$ in $\mathcal{C}$_ is a [[functor]] of the form

   $$
     X \;\colon\; \mathcal{I} \longrightarrow \mathcal{C}
     \,,
   $$

1. the _category of $\mathcal{I}$-shaped diagrams in $\mathcal{C}$_ is the [[functor category]] $Funct(\mathcal{I}, \mathcal{C})$;

1. a diagram $X \colon \mathcal{I} \to \mathcal{C}$ is _constant_ if it is a [[constant functor]]

   $$
     const_{\tilde X}
       \;\colon\;  
     \mathcal{I} 
       \overset{\exists!}{\longrightarrow} 
     \ast
       \overset{\tilde X}{\longrightarrow}
     \mathcal{C}
   $$

   in which case it is given by the data of a single object $\tilde X$;

1. a _[[cone]]_ $C$ over a diagram $X \colon \mathcal{I} \to \mathcal{C}$ with _tip_ an object $\tilde X \in \mathcal{C}$ is a [[natural transformation]] from the constant diagram $const_{\tilde X} \colon \mathcal{I} \to \ast \to \mathcal{C}$ to $X$:

   $$
     C \;\colon\; const_{\tilde X} \Rightarrow X
   $$

1. a _[[cocone]]_ $C$ under a diagram $X \colon \mathcal{I} \to \mathcal{C}$ is a [[natural transformation]] to a constant diagram $const_{\tilde X} \colon \mathcal{I} \to \ast \to \mathcal{C}$ from $X$:

   $$
     C \;\colon\; X \Rightarrow const_{\tilde X}
   $$

1. the _limiting cone_ (or  _[[limit]]_, for short) over a diagram $X$ is, if it exists, the [[terminal object]] in the [[category]] of [[cones]] over $X$, which means that it is a cone $C_{lim}$ with tip denoted $\underset{\longleftarrow}{\lim}_i X_i$ such that for every other cone $C$ with tip $\tilde X$ there is a unique [[natural transformation]] $\phi \colon const_{\tilde X} \Rightarrow const_{\underset{\longrightarrow}{\lim}_i X_i}$ such that

   $$
     C = C_{lim} \circ \phi
   $$ 

1. the _colimiting cone_ (or _[[colimit]]_, for short) under a diagram $X$ is, if it exists, the [[initial object]] in the [[category]] of [[cocones]] under $X$, which means that it is a co-cone $C_{lim}$ with tip denoted $\underset{\longrightarrow}{\lim}_i X_i$ such that for every other cocone $C$ with tip $\tilde X$ there is a unique [[natural transformation]] $\phi \colon  const_{\underset{\longrightarrow}{\lim}_i X_i} \Rightarrow const_{\tilde X}$ such that

   $$
     C = \phi \circ C_{lim}
     \,.
   $$ 

=--


#### Component definition
 {#CategoryShapedDiagramInComponents}

We state an explicit component-based definition of diagrams of the shape of categories.

+-- {: .num_defn #Diagram}
###### Definition
**([[diagram]] in a [[category]])**

A [[diagram]] $X_\bullet$ in a [[category]] is

1. a [[set]] $\{ X_i \}_{i \in I}$ of [[objects]] in the category;

1. for every [[pair]] $(i,j) \in I \times I$ of labels of objects a [[set]]
   $\{ X_i \overset{ f_\alpha }{\longrightarrow} X_j\}_{\alpha \in I_{i,j}}$ of [[morphisms]] between these objects;

1. for every label $i \in I$ a choice of element $\epsilon_i \in I_{i,i}$;
  
1. for each [[triple]] $i,j,k \in I$ a [[function]]

   $$
     comp_{i,j,k} \;\colon\; I_{i,j} \times I_{j,k} \longrightarrow I_{i,k}
   $$
 
such that 

1. the pairing $comp$ is [[associativity|associative]] and [[unital]] with the $f_{\epsilon_i}$-s the [[neutral elements]];

1. for every $i \in I$ then $f_{\epsilon_i} = id_{X_i}$ is the [[identity morphism]] on the $i$-th obect;

1. for every composable pair of morphisms 

  $$
    X_i 
      \overset{f_{\alpha} }{\longrightarrow} 
    X_j
      \overset{ f_{\beta} }{\longrightarrow}
    X_k
  $$
  
  then the [[composition|composite]] of these two morphisms equals the morphism of the diagram that is 
  labeled by the value of $comp_{i,j,k}$ on their labels:
  
  $$
    f_{\beta} \circ f_\alpha 
    \,=\,
    f_{comp_{i,j,k}( \alpha, \beta )}
    \,.
  $$
  
The last condition we depict as follows:

$$
  \array{ 
    && X_j
    \\
    & {}^{\mathllap{f_{\alpha}}}\nearrow && \searrow^{\mathrlap{f_{\beta}}}
    \\
    X_i && \underset{ comp_{i,j,k}(\alpha,\beta) }{\longrightarrow} && X_k
  }
  \,.
$$


=--

+-- {: .num_defn #Cone}
###### Definition
**([[cone]] over a [[diagram]])**

Consider a [[diagram]] 

$$
  X_\bullet
    \,=\,
  \left(
     \left\{
       X_i \overset{f_\alpha}{\longrightarrow} X_j
     \right\}_{i,j \in I, \alpha \in I_{i,j}}
     \,,\,
     \mathrm{comp}
  \right)
$$

in some [[category]] (def. \ref{Diagram}). Then 

1. a _[[cone]]_ over this diagram is

   1. an [[object]] $\tilde X$ in the category;
   
   1. for each $i \in I$ a morphism $\tilde X \overset{p_i}{\longrightarrow} X_i$ in the category
   
   such that

   * for all $(i,j) \in I \times I$ and all $\alpha \in I_{i,j}$ then the condition
   
     $$
       f_{\alpha} \circ p_i = p_j
     $$
     
     holds, which we depict as follows:  

     $$
       \array{
         && \tilde X
         \\
         & {}^{\mathllap{p_i}}\swarrow && \searrow^{\mathrlap{p'_j}}
         \\
         X_i 
           && \underset{f_\alpha}{\longrightarrow} &&
         X_j
       }
     $$
     
1. a _[[co-cone]]_ over this diagram is

   1. an [[object]] $\tilde X$ in the category;

   1. for each $i \in I$ a morphism $q_i \colon X_i \longrightarrow \tilde X$ in the category

   such that

   * for all $(i,j) \in I \times I$ and all $\alpha \in I_{i,j}$ then the condition

     $$
       q_j \circ f_{\alpha} = q_i
     $$

     holds, which we depict as follows:

     $$
       \array{
         X_i && \overset{f_\alpha}{\longrightarrow} && X_j
         \\
         & {}_{\mathllap{q_i}}\searrow && \swarrow_{\mathrlap{q_j}}
         \\
         && \tilde X
       }
       \,.
     $$

=--



+-- {: .num_defn #LimitingCone}
###### Definition

Consider a [[diagram]]

$$
  X_\bullet
    \,=\,
  \left(
     \left\{
       X_i \overset{f_\alpha}{\longrightarrow} X_j
     \right\}_{i,j \in I, \alpha \in I_{i,j}}
     \,,\,
     \mathrm{comp}
  \right)
$$

in some [[category]] (def. \ref{Diagram}). Then

1. its _[[limit|limiting cone]]_ (or just _[[limit]]_ for short) is, if it exists,
   [[generalized the|the]] [[cone]] 
   
   $$
     \left\{
     \array{
       && \underset{\longleftarrow}{\lim}_i X_i
       \\
       & {}^{\mathllap{p_i}}\swarrow && \searrow^{\mathrlap{p_j}}
       \\
       X_i
         && \underset{f_\alpha}{\longrightarrow} &&
       X_j
     }
     \right\}
   $$

   over this diagram (def. \ref{Cone}) which is _universal_ or _initial_ among all 
   possible cones,
   in that it has the property that for

   $$
     \left\{
     \array{
       && \tilde X
       \\
       & {}^{\mathllap{p'_i}}\swarrow && \searrow^{\mathrlap{p'_j}}
       \\
       X_i
         && \underset{f_\alpha}{\longrightarrow} &&
       X_j
     }
     \right\}
   $$
   
   any other [[cone]], then there is a unique morphism
   
   $$
     \phi \;\colon\; \tilde X \overset{}{\longrightarrow} \underset{\longrightarrow}{\lim}_i X_i
   $$
   
   that factors the given cone through the limiting cone, in that for all $i \in I$ then
   
   $$
     p'_i = p_i \circ \phi
   $$
   
   which we depict as follows:

   $$
     \array{
       \tilde X
       \\
       {}^{\mathllap{\phi}}\downarrow & \searrow^{\mathrlap{p_i}}
       \\
       \underset{\longrightarrow}{\lim}_i X_i
       &\underset{p_i}{\longrightarrow}& 
       X_i
     }
   $$

1. its _[[colimit|colimiting cocone]]_ (or just _[[colimit]]_ for short) is, if it exists,
   [[generalized the|the]] [[cocone]]

   $$
     \left\{
     \array{
       X_i
         && \underset{f_\alpha}{\longrightarrow} &&
       X_j
       \\
       & {}^{\mathllap{q_i}}\searrow && \swarrow^{\mathrlap{q_j}}
       \\
       \\
       && \underset{\longrightarrow}{\lim}_i X_i
     }
     \right\}
   $$

   under this diagram (def. \ref{Cone}) which is _universal_ or _terminal_ among all
   possible co-cones,
   in that it has the property that for

   $$
     \left\{
     \array{
       X_i
         && \underset{f_\alpha}{\longrightarrow} &&
       X_j
       \\
       & {}^{\mathllap{q'_i}}\searrow && \swarrow_{\mathrlap{q'_j}}
       \\
       && \tilde X
     }
     \right\}
   $$

   any other [[cocone]], then there is a unique morphism

   $$
     \phi \;\colon\;  \underset{\longrightarrow}{\lim}_i X_i \overset{}{\longrightarrow} \tilde X
   $$

   that factors the given co-cone through the co-limiting cocone, in that for all $i \in I$ then

   $$
     q'_i = \phi \circ q_i
   $$

   which we depict as follows:

   $$
     \array{
       X_i
       &\overset{q_i}{\longrightarrow}&
       \underset{\longrightarrow}{\lim}_i X_i
       \\
       {}^{\mathllap{\phi}}\downarrow & \swarrow^{\mathrlap{q'_i}}
       \\
       \tilde X
     }
   $$

=--



### Diagrams shaped like directed graphs
 {#ShapeOfDirectedGraph}

+-- {: .num_defn}
###### Definition
**([[free diagram]])**

If $J$ is a [[directed graph]] with [[free category]] $F(J)$, then a __diagram__ in $C$ of shape $J$ is a functor $D\colon F(J) \to C$, or equivalently a graph morphism $\bar{D}\colon J \to U(C)$.
=--

Here $F\colon Quiv \to Cat$ denotes the [[free category]] on a quiver and $U\colon Cat \to Quiv$ the underlying quiver of a category, which form a pair of [[adjoint functors]].  These are the sorts of diagrams which we "draw on a page" --- we draw a quiver, and then label its vertices with objects of $C$ and its edges with morphisms in $C$, thereby forming a graph morphism $J\to U(C)$.


## Remarks

* For either sort of diagram, $J$ may be called the __shape__, __scheme__, or __index__ category or graph.

* Note that given a diagram $D:J\to C$, the image of the shape $J$ is not necessarily a [[subcategory]] of $C$, even if $J$ is itself taken to be a category.  This is because the functor $D$ could identify objects of $J$, thereby producing new potential composites which do not exist in $J$.  (Sometimes one talks about the "image" of a functor as a subcategory, but this really means the subcategory *generated* by the image in the literal objects-and-morphisms sense.)

* $C$ must be a [[strict category]] to make sense of $U(C)$; however, $F(J)$ always makes sense.


## Commutative diagrams

If $J$ is a category, then a diagram $J\to C$ is __[[commutative diagram|commutative]]__ if it factors through a [[thin category]].  Equivalently, a diagram of shape $J$ commutes iff any two morphisms in $C$ that are assigned to any pair of [[parallel morphisms]] in $J$ (i.e., with same source and target in $J$) are equal.

If $J$ is a quiver, as is more common when we speak about "commutative" diagrams, then a diagram of shape $J$ commutes if the functor $F(J) \to C$ factors through a thin category.  Equivalently, this means that given any two parallel *paths* of arbitrary finite length (including zero) in $J$, their images in $C$ have equal composites.


## Examples

* The shape of the **empty diagram** is the [[initial object|initial category]] with no object and no morphism. 

  Every category $C$ admits a unique diagram whose shape is the empty ([[initial object|initial]]) category, which is called the **empty diagram** in $C$.

* The shape of the **terminal diagram** is the [[terminal category]] $J = \{*\}$ consisting of a single object and a single morphism (the identity morphism on that object). 

  Specifying a diagram in $C$ whose shape is $\{*\}$ is the same as specifying a single [[object]] of $C$, the image of the unique object of $1$. (See [[global element]])


* A diagram of the shape $\{a \to b\}$ in $C$ is the choice of any one [[morphism]] $D_{a b} : X_a \to X_b$ in $C$.

  Notice that strictly speaking this counts as a _commuting diagram_ , but is a degenerate case of a commuting diagram, since there is only a single morphism involved, which is necessarily equal to itself.

* If $J$ is the quiver with one object $a$ and one endo-edge $a\to a$, then a diagram of shape $J$ in $C$ consists of a single [[endomorphism]] in $C$.  Since $a\to a$ and the zero-length path are parallel in $J$, such a diagram only commutes if the endomorphism is an identity.  Note, in particular, that a single endomorphism can be considered as a diagram with more than one shape (this one and the previous one), and that whether this diagram "commutes" depends on the chosen shape.

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

  is a **commuting square** in $C$: this is a choice of four (not necessarily distinct!) objects $X_a, X_b, X_{b'}, X_c$ in C, together with a choice of (not necessarily distinct) four morphisms $D_{a b} : X_a \to X_b$, $D_{b c} : X_b \to X_c$ and $D_{a b'} : X_a \to X_{b'}$, $D_{b' c} : X_{b'} \to X_c$ in $C$, such that the composite morphism $D_{b c}\circ D_{a b}$ equals the composite $D_{b' c}\circ D_{a b'}$.

  One typically "draws the diagram" as

  $$
      \array{
         X_a &\stackrel{D_{a b}}{\to}& X_b
         \\
         {}^{\mathllap{D_{a b'}}}\downarrow && 
        \downarrow^{\mathrlap{D_{b c}}}
         \\
         X_{b'} &\stackrel{D_{b' c}}{\to}& X_{c}
      }    
  $$

  in $C$ and says that _the diagram commutes_ if the above equality of composite morphisms holds.

  Notice that the original poset had, necessarily, a morphism $a \to c$ and could have equivalently  been depicted as

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
         X_a &\stackrel{D_{a b}}{\to}& X_b
         \\
         {}^{\mathllap{D_{a b'}}}\downarrow &\searrow^{\stackrel{D_{b c}\circ D_{a b}}{= D_{b' c}\circ D_{a b'}}}& 
        \downarrow^{\mathrlap{D_{b c}}}
         \\
         X_{b'} &\stackrel{D_{b' c}}{\to}& X_{c}
      }    
  $$

* By contrast, a diagram whose shape is the *quiver*
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
  is a not-necessarily-commuting square.  The free category on this quiver differs from the poset in the previous example by having *two* morphisms $a\to c$, one given by the composite $a\to b\to c$ and the other by the composite $a \to b'\to c$.  But the poset in the previous category is the poset reflection of this $F(J)$, so a diagram of this shape commutes, in the sense defined above, iff it is a commuting square in the usual sense.


* A pair of objects is a diagram whose shape is a [[discrete category]] with two objects.


* A pair of [[parallel morphisms]] is a diagram whose shape is a category 
  $J = \{a \stackrel{\to}{\to} b\}$
  with two objects and two morphisms from one to the other. 

  Notice that if we required  $\{a \stackrel{\to}{\to} b\}$ to be a [[poset]] this would necessarily make these two morphisms equal, and hence reduce this example to the one where $J = \{a \to b\}$.  In other words, a diagram of this shape only *commutes* if the two morphisms are equal.

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

  This is a non-finite commuting diagram.

* [[tower diagram]]


## Related concepts

* [[commuting diagram]]

* [[internal diagram]]

* [[free diagram]]

[[!redirects diagram]]
[[!redirects diagrams]]

[[!redirects small diagram]]
[[!redirects small diagrams]]
