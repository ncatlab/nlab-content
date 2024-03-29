
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

A _free diagram_ in a [[category]] $\mathcal{C}$ is a particularly simple special case of the general concept of a _[[diagram]]_ $X_\bullet \;\colon\; \mathcal{I} \to \mathcal{C}$, namely the case where the shape $\mathcal{I}$ of the diagram is a [[free category]].

Many important types of [[limits]] and [[colimits]] are over free diagrams, for instance [[products]]/[[coproducts]], [[equalizers]]/[[coequalizers]], [[pullbacks]]/[[pushouts]], [[sequential limits]]/[[sequential colimits]].

Due to the simplicity of the concept of free diagrams, these types of [[limits]] and [[colimits]] may be discussed in a very low-brow way, without even making the concept of _[[category]]_ and _[[functor]]_ explicit. For this see the _[Exposition](#Exposition)_ below.


## Definition

Recall that 

+-- {: .num_defn #Diagram}
###### Definition
**([[diagram]])**

For $\mathcal{C}$ a [[category]], then a _[[diagram]] in $\mathcal{C}$_ is 

1. a [[small category]] $\mathcal{I}$ , the _shape_ of the diagram;

1. a [[functor]] $X_\bullet \;\colon\; \mathcal{I} \to \mathcal{C}$.

=--

+-- {: .num_defn #FreeCategory}
###### Definition
**([[free category]])**

There is a [[free-forgetful adjunction]]

$$
  Cat
    \underoverset
      {\underset{Underlying}{\longrightarrow}}
      {\overset{Free}{\longleftarrow}}
      {\bot}
  DirGraph
$$

between the [[1-categories]] of [[categories]] and that of [[directed graphs]]. 

A _[[free category]]_ is one in the [[image]] of this [[left adjoint]] functor $Free \colon DirGraph \to Cat$ (sometimes called a "[[path category]]").

=--


+-- {: .num_defn #FreeDiagram}
###### Definition
**(free diagram)**

A _[[free diagram]]_ in a [[category]] $\mathcal{C}$ is a [[diagram]] in $\mathcal{C}$ (def. \ref{Diagram}) whose shape is a [[free category]] (def. \ref{FreeCategory}). 

In other words, a free diagram in $\mathcal{C}$ is

1. a [[directed graph]] $I$;

1. a [[functor]] of the form $X_\bullet \;\colon\; Free(I) \to \mathcal{C}$.

=--

## Examples

+-- {: .num_example}
###### Example

Types of free diagrams that are commonly encountered in practice, as well as the names of the [[limits]]/[[colimits]] over them are shown in the following table

[[!include free diagrams -- table]]

=--



## Exposition 
 {#Exposition}

We give an exposition of free diagrams, and their [[cones]] and [[limits]], intentionally avoiding abstract category-theoretic language, expressing everything just in components. See also at _[[limits and colimits by example]]_.

For concreteness, we speak only of diagrams of [[sets]] and of [[topological spaces]] in the following:






+-- {: .num_defn #Diagram}
###### Definition
**([[free diagram]] of [[sets]]/[[topological spaces]])**

A _[[free diagram]]_ $X_\bullet$ of [[sets]] or of [[topological spaces]] is

1. a [[set]] $\{ X_i \}_{i \in I}$ of [[sets]] or of [[topological spaces]], respectively;

1. for every [[pair]] $(i,j) \in I \times I$ of labels, a [[set]]
   $\{ X_i \overset{ f_\alpha }{\longrightarrow} X_j\}_{\alpha \in I_{i,j}}$ of [[functions]] of of [[continuous functions]], respectively, between these.

=--


+-- {: .num_example #DiscreteDiagram}
###### Example
**([[discrete category|discrete]] [[diagram]] and [[empty diagram]])**

Let $I$ be any [[set]], and for each $(i,j) \in I \times I$ let $I_{i,j} = \emptyset$
be the [[empty set]].

The corresponding [[free diagrams]] (def. \ref{Diagram})
are simply a set of sets/topological spaces with no specified (continuous) functions between them.
This is called a _[[discrete category|discrete]] [[diagram]]_.

For example for $I = \{1,2,3\}$ the set with 3-elements, then such a diagram looks like this:

$$
  X_1 \phantom{AAA} X_2 \phantom{AAA} X_3
  \,.
$$

Notice that here the index set may be [[empty set]], $I = \emptyset$, in which case the
corresponding diagram consists of no data. This is also called the _[[empty diagram]]_.

=--

+-- {: .num_defn #ParallelMorphisms}
###### Definition
**([[parallel morphisms]] [[diagram]])**

Let $I = \{a, b\}$ be the [[set]] with two elements, and consider the sets


$$
  I_{i,j}
    \;\coloneqq\;
  \left\{
    \array{
      \{ 1,2 \} & \vert & (i = a) \,\text{and}\, (j = b)
      \\
      \emptyset & \vert & \text{otherwise}
    }
  \right\}
  \,.
$$

The corresponding [[free diagrams]] (def. \ref{Diagram}) are called _[[pairs of  parallel morphisms]]_.
They may be depicted like so:

$$
  X_a
    \underoverset
      {\underset{f_2}{\longrightarrow}}
      {\overset{f_1}{\longrightarrow}}
      {\phantom{AAAAA}}
  X_b
  \,.
$$

=--


+-- {: .num_example #SpanDiagram}
###### Example
**([[span]] and [[cospan]] [[diagram]])**

Let $I = \{a,b,c\}$ the set with three elements, and set

$$
  I_{i ,j}
   =
  \left\{
    \array{
      \{f_1\} & \vert \, (i = c) \,\text{and}\, (j = a)
      \\
      \{f_2\} & \vert \, (i = c) \,\text{and}\, (j = b)
      \\
      \emptyset & \vert \, \text{otherwise}
    }
  \right.
$$

The corresponding [[free diagrams]] (def. \ref{Diagram}) look like so:

$$
  \array{
    && X_c
    \\
    & {}^{\mathllap{f_1}}\swarrow && \searrow^{\mathrlap{f_2}}
    \\
    X_a && && X_b
  }
  \,.
$$

These are called _[[span]] [[diagrams]]_.

Similary, there is the _[[cospan]]_ diagram of the form

$$
  \array{
    && X_c
    \\
    & {}^{\mathllap{f_1}}\nearrow && \nwarrow^{\mathrlap{f_2}}
    \\
    X_a && && X_b
  }
  \,.
$$

=--

+-- {: .num_example}
###### Example
**([[tower]] [[diagram]])**

Let $I = \mathbb{N}$ be the set of [[natural numbers]] and consider

$$
  I_{i,j}
   \;\coloneqq\;
  \left\{
    \array{
      \{f_{i,j}\} & \vert & i \leq j
      \\
      \emptyset & \vert & \text{otherwise}
    }
  \right.
$$

The corresponding [[free diagrams]] (def. \ref{Diagram}) are called _[[tower]] [[diagrams]]_.
They look as follows:


$$
   X_0
     \overset{\phantom{A}f_{0,1} \phantom{A} }{\longrightarrow}
   X_1
     \overset{\phantom{A} f_{1,2} \phantom{A} }{\longrightarrow}
   X_2
     \overset{\phantom{A} f_{2,3} \phantom{A} }{\longrightarrow}
   X_3
     \overset{}{\longrightarrow}
   \cdots
   \,.
$$


Similarly there are co-tower diagram

$$
   X_0
     \overset{\phantom{A} f_{0,1} \phantom{A} }{\longleftarrow}
   X_1
     \overset{\phantom{A} f_{1,2} \phantom{A}}{\longleftarrow}
   X_2
     \overset{\phantom{A} f_{2,3} \phantom{A}}{\longleftarrow}
   X_3
     \overset{}{\longleftarrow}
   \cdots
   \,.
$$


=--


$\,$

+-- {: .num_defn #Cone}
###### Definition
**([[cone]] over a [[free diagram]])**

Consider a [[free diagram]] of sets or of topological spaces (def. \ref{Diagram})

$$
  X_\bullet
    \,=\,
  \left\{
    X_i \overset{f_\alpha}{\longrightarrow} X_j
  \right\}_{i,j \in I, \alpha \in I_{i,j}}
  \,.
$$

Then

1. a _[[cone]]_ over this diagram is

   1. a [[set]] or [[topological space]] $\tilde X$ (called the _tip_ of the cone);

   1. for each $i \in I$ a [[function]] or [[continuous function]] $\tilde X \overset{p_i}{\longrightarrow} X_i$

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
         & {}^{\mathllap{p_i}}\swarrow && \searrow^{\mathrlap{p_j}}
         \\
         X_i
           && \underset{f_\alpha}{\longrightarrow} &&
         X_j
       }
     $$

1. a _[[co-cone]]_ over this diagram is

   1. a set or topological space $\tilde X$ (called the _tip_ of the co-cone);

   1. for each $i \in I$ a function or continuous function $q_i \colon X_i \longrightarrow \tilde X$;

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


+-- {: .num_example #ConeIncarnationOfSolutionsToEquations}
###### Example
**([[solutions]] to [[equations]] are [[cones]])**

Let $f,g \colon \mathbb{R} \to \mathbb{R}$ be two [[functions]] from the [[real numbers]] to themselves, and consider the
corresponding [[parallel morphism]] [[diagram]] of sets (example \ref{ParallelMorphisms}):

$$
  \mathbb{R}
    \underoverset
      {\underset{f_2}{\longrightarrow}}
      {\overset{f_1}{\longrightarrow}}
      {\phantom{AAAAA}}
  \mathbb{R}
  \,.
$$

Then a [[cone]] (def. \ref{Cone}) over this free diagram with tip the [[singleton]] set $\ast$ is a _[[solution]]_ to
the [[equation]] $f(x) = g(x)$

$$
  \array{
    && \ast
    \\
    & {}^{\mathllap{const_x}}\swarrow && \searrow^{\mathrlap{const_y}}
    \\
    \mathbb{R}
      &&
      \underoverset
        {\underset{f_2}{\longrightarrow}}
        {\overset{f_1}{\longrightarrow}}
        {\phantom{AAAAA}}
      &&
    \mathbb{R}
  }
  \,.
$$

Namely the components of the cone are two functions of the form

$$
  cont_x, const_y \;\colon\; \ast \to \mathbb{R}
$$

hence equivalently two [[real numbers]], and the conditions on these are

$$
  f_1 \circ const_x = const_y
  \phantom{AAAA}
  f_2 \circ const_x = const_y
  \,.
$$

=--


+-- {: .num_defn #LimitingCone}
###### Definition
**([[limit|limiting cone]] over a [[diagram]])**

Consider a [[free diagram]] of sets or of topological spaces (def. \ref{Diagram}):

$$
  \left\{
    X_i \overset{f_\alpha}{\longrightarrow} X_j
  \right\}_{i,j \in I, \alpha \in I_{i,j}}
  \,.
$$

Then

1. its _[[limit|limiting cone]]_ (or just _[[limit]]_ for short, also "[[inverse limit]]", for historical reasons) is
   [[generalized the|the]] [[cone]]

   $$
     \left\{
     \array{
       && \underset{\longleftarrow}{\lim}_k X_k
       \\
       & {}^{\mathllap{p_i}}\swarrow && \searrow^{\mathrlap{p_j}}
       \\
       X_i
         && \underset{f_\alpha}{\longrightarrow} &&
       X_j
     }
     \right\}
   $$

   over this diagram (def. \ref{Cone}) which is _[[universal property|universal]]_ among all possible cones,
   in that for

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

   any other [[cone]], then there is a unique function or continuous function, respectively

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
       {}^{\mathllap{ \exists !\, \phi}}\downarrow & \searrow^{\mathrlap{p'_i}}
       \\
       \underset{\longrightarrow}{\lim}_i X_i
       &\underset{p_i}{\longrightarrow}&
       X_i
     }
   $$

1. its _[[colimit|colimiting cocone]]_ (or just _[[colimit]]_ for short, also "[[direct limit]]", for historical reasons) is
   [[generalized the|the]] [[cocone]]

   $$
     \left\{
     \array{
       X_i
         && \overset{f_\alpha}{\longrightarrow} &&
       X_j
       \\
       & {}^{\mathllap{q_i}}\searrow && \swarrow^{\mathrlap{q_j}}
       \\
       \\
       && \underset{\longrightarrow}{\lim}_i X_i
     }
     \right\}
   $$

   under this diagram (def. \ref{Cone}) which is _[[universal property|universal]]_ among all possible co-cones,
   in that it has the property that for

   $$
     \left\{
     \array{
       X_i
         && \overset{f_\alpha}{\longrightarrow} &&
       X_j
       \\
       & {}^{\mathllap{q'_i}}\searrow && \swarrow_{\mathrlap{q'_j}}
       \\
       && \tilde X
     }
     \right\}
   $$

   any other [[cocone]], then there is a unique function or continuous function, respectively

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
       & {}_{q'_i}\searrow & \downarrow^{\mathrlap{\exists ! \phi}}
       \\
       && \tilde X
     }
   $$

=--

$\,$

All the limits and colimits over the free diagram in the above list of examples have special names:



[[!include free diagrams -- table]]

+-- {: .num_example #TerminalInitialObject}
###### Example
**([[initial object]] and [[terminal object]])**

Consider the [[empty diagram]] (def. \ref{DiscreteDiagram}).

1. A [[cone]] over the empty diagram is just an object $X$, with no further structure or condition.
The [[universal property]] of the [[limit]] ``$\ast$'' over the empty diagram is hence that
for every object $X$, there is a unique map of the form $X \to \ast$. Such an object $\ast$ is called a _[[terminal object]]_.

1. A [[co.cone]] over the empty diagram is just an object $X$, with no further structure or condition.
The [[universal property]] of the [[colimit]] ``$0$'' over the empty diagram is hence that
for every object $X$, there is a unique map of the form $0 \to X$. Such an object $\ast$ is called a _[[initial object]]_.

=--


+-- {: .num_example #CoProduct}
###### Example
**([[Cartesian product]] and [[coproduct]])**

Let $\{X_i\}_{i \in I}$ be a [[discrete category|discrete]] [[diagram]] (example \ref{DiscreteDiagram}),
i.e. just a set of objects.

1. The [[limit]] over this diagram is called the _[[Cartesian product]]_, denoted $\underset{i \in I}{\prod} X_i$;

1. The [[colimit]] over this diagram is called the _[[coproducts]]_, denoted $\underset{i \in I}{\coprod} X_i$.


=--

+-- {: .num_example #Equalizer}
###### Example
**([[equalizer]])**

Let

$$
  X_1
    \underoverset
      {\underset{\phantom{AA}f_2\phantom{AA}}{\longrightarrow}}
      {\overset{\phantom{AA}f_1\phantom{AA}}{\longrightarrow}}
      {}
  X_2
$$

be a [[free diagram]] of the shape "[[pair of parallel morphisms]]" (example \ref{ParallelMorphisms}).

A [[limit]] over this diagram according to def. \ref{LimitingCone} is also called the _[[equalizer]]_ of the maps $f_1$ and $f_2$.
This is a set or topological space $eq(f_1,f_2)$ equipped with a map $eq(f_1,f_2) \overset{p_1}{\longrightarrow} X_1$,
so that $f_1 \circ p_1 = f_2 \circ p_1$ and such that if $Y \to X_1$ is any other map with this property

$$
  \array{
    && Y
    \\
    && \downarrow & \searrow
    \\
    eq(f_1,f_2)
      &\overset{p_1}{\longrightarrow}&
    X_1
      &
        \underoverset
          {\underset{\phantom{AA}f_2\phantom{AA}}{\longrightarrow}}
          {\overset{\phantom{AA}f_1\phantom{AA}}{\longrightarrow}}
          {}
      &
    X_2
  }
$$

then there is a unique factorization through the equalizer:

$$
  \array{
    && Y
    \\
    &{}^{\mathllap{\exists !}}\swarrow& \downarrow & \searrow
    \\
    eq(f_1,f_2)
      &\overset{p_1}{\longrightarrow}&
    X_1
      &
        \underoverset
          {\underset{f_2}{\longrightarrow}}
          {\overset{f_1}{\longrightarrow}}
          {}
      &
    X_2
  }
  \,.
$$

In example \ref{ConeIncarnationOfSolutionsToEquations} we have seen that a cone over
such a pair of parallel morphisms is a _[[solution]]_ to the equation $f_1(x) = f_2(x)$.

The equalizer above is the _space of all solutions_ of this equation.

=--

+-- {: .num_example #Pushout}
###### Example
**([[pullback]]/[[fiber product]] and [[coproduct]])**

Consider a [[cospan]] [[diagram]] (example \ref{SpanDiagram})

$$
  \array{
     && Y
     \\
     && \downarrow^{\mathrlap{f}}
     \\
     X
       &\underset{g}{\longrightarrow}&
     Z
  }
  \,.
$$

The [[limit]] over this diagram is also called the _[[fiber product]]_ of $X$ with $Y$ over $Z$, and denoted
$X \underset{Z}{\times}Y$. Thought of as equipped with the projection map to $X$, this is also called the
_[[pullback]]_ of $f$ along $g$

$$
  \array{
     X \underset{X}{\times} Z
       &\longrightarrow&
     Y
     \\
     \downarrow &(pb)& \downarrow^{\mathrlap{f}}
     \\
     X
       &\underset{g}{\longrightarrow}&
     Z
  }
  \,.
$$

[[formal duality|Dually]], consider a [[span]] [[diagram]] (example \ref{SpanDiagram})

$$
  \array{
    Z
      &\overset{g}{\longrightarrow}&
    Y
    \\
    {}^{\mathllap{f}}\downarrow
    \\
    X
  }
$$

The [[colimit]] over this diagram is also called the [[pushout]] of $f$ along $g$, denoted $X \underset{Z}{\sqcup}Y$:

$$
  \array{
    Z
      &\overset{g}{\longrightarrow}&
    Y
    \\
    {}^{\mathllap{f}}\downarrow &(po)& \downarrow
    \\
    X &\longrightarrow& X \underset{Z}{\sqcup} Y
  }
$$


=--




$\,$


Here is a more explicit description of the limiting cone over a diagram of sets:


+-- {: .num_prop #SetLimits}
###### Proposition
**([limits and colimits of sets](limits+and+colimits+by+example#limcoliminset))**

Let $\left\{ X_i \overset{f_\alpha}{\longrightarrow} X_j \right\}_{i,j \in I, \alpha \in I_{i,j}}$
be a [[free diagram]] of sets  (def. \ref{Diagram}). Then

1. its [[limit|limit cone]] (def. \ref{LimitingCone}) is given by
   the following [[subset]] of the [[Cartesian product]]
   $\underset{i \in I}{\prod} X_i$
   of all the [[sets]] $X_i$ appearing in the diagram

   $$
     \underset{\longleftarrow}{\lim}_i X_i
     \,\overset{\phantom{AAA}}{\hookrightarrow}\,
     \underset{i \in I}{\prod} X_i
   $$

   on those [[tuples]] of elements which match the [[graphs]] of the functions appearing in the diagram:

   $$
     \underset{\longleftarrow}{\lim}_{i} X_i
     \;\simeq\;
     \left\{
       (x_i)_{i \in I}
       \,\vert\,
       \underset{ {i,j \in I} \atop { \alpha \in I_{i,j} } }{\forall}
       \left(
         f_{\alpha}(x_i) = x_j
       \right)
     \right\}
   $$

   and the projection functions are $p_i \colon (x_j)_{j \in I} \mapsto x_i$.

1. its [[colimit|colimiting co-cone]] (def. \ref{LimitingCone}) is given by the [[quotient set]] of the [[disjoint union]] $\underset{i \in I}{\sqcup} X_i$ of all the [[sets]] $X_i$ appearing in the diagram

   $$
     \underset{i \in I}{\sqcup} X_i
       \,\overset{\phantom{AAA}}{\longrightarrow}\,
     \underset{\longrightarrow}{\lim}_{i \in I} X_i
   $$

   with respect to the [[equivalence relation]] which is generated from the [[graphs]] of the functions in the diagram:

   $$
     \underset{\longrightarrow}{\lim}_i X_i
     \;\simeq\;
     \left(
       \underset{i \in I}{\sqcup} X_i
     \right)/
     \left(
       (x \sim x')
         \Leftrightarrow
       \left(
         \underset{ {i,j \in I} \atop { \alpha \in I_{i,j} } }{\exists}
         \left(
           f_\alpha(x) = x'
         \right)
       \right)
     \right)
   $$

   and the injection functions are the evident maps to [[equivalence classes]]:

   $$
     q_i \;\colon\; x_i \mapsto [x_i]
     \,.
   $$

=--

+-- {: .proof}
###### Proof

We dicuss the proof of the first case. The second is directly analogous.

First observe that indeed, by consturction, the projection maps $p_i$ as given do make a cone over the free diagram,
by the very nature of the relation that is imposed on the tuples:

$$
  \array{
     &&
     \left\{
       (x_k)_{k \in I}
       \,\vert\,
       \underset{ {i,j \in I} \atop { \alpha \in I_{i,j} } }{\forall}
       \left(
         f_{\alpha}(x_i) = x_j
       \right)
     \right\}
    \\
    & {}^{\mathllap{p_i}}\swarrow && \searrow^{\mathrlap{p_j}}
    \\
    X_i && \underset{f_\alpha}{\longrightarrow} && X_j
  }
  \,.
$$

We need to show that this is universal, in that any other cone over the free diagram factors universally
through it. First consider the case that the tip of a give cone is a singleton:

$$
  \array{
    && \ast
    \\
    & {}^{\mathllap{p'_i}}\swarrow && \searrow^{\mathrlap{p'_j}}
    \\
    X_i
      && \underset{f_\alpha}{\longrightarrow} &&
    X_j
  }
  \,.
$$

This is hence equivalently for each $i \in I$ an element $x'_i \in X_i$, such that for all $i, j \in I$ and $\alpha \in I_{i,j}$
then $f_\alpha(x'_i) = x'_j$. But this is precisely the relation used in the construction of the limit above and hence there
is a unique map

$$
  \ast
    \longrightarrow
     \left\{
       (x_k)_{k \in I}
       \,\vert\,
       \underset{ {i,j \in I} \atop { \alpha \in I_{i,j} } }{\forall}
       \left(
         f_{\alpha}(x_i) = x_j
       \right)
     \right\}
$$

such that for all $i \in I $ we have

$$
  \array{
    \ast
    \\
    \downarrow & \searrow^{\mathrlap{p'_i}}
    \\
     \left\{
       (x_k)_{k \in I}
       \,\vert\,
       \underset{ {i,j \in I} \atop { \alpha \in I_{i,j} } }{\forall}
       \left(
         f_{\alpha}(x_i) = x_j
       \right)
     \right\}
     &\underset{p_i}{\longrightarrow}&
     X_i
  }
$$

namely that map is the one that picks the element $(x'_i)_{i \in I}$.

This shows that every cone with tip a singleton factors uniquely through the claimed limiting cone. But
then for a cone with tip an arbitrary set $Y$, this same argument applies to all the single elements of $Y$.

=--














## Related concepts

* [[diagram]]

* [[commuting diagram]]

* [[internal diagram]]


[[!redirects free diagrams]]

