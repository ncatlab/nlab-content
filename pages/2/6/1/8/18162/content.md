+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
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
 {#Idea}

In [[topology]], some of the [[separation axioms]] that may be considered on [[topological spaces]] may equivalently be reformulated in terms of [[lifting properties]] ([Gavrilovich 2014](#\rightthreetimes)) with respect to simple counterexamples represented by finite preorders, and closely following standard definitions. 

To see this, first notice/recall  the following two simple examples of [[lifting properties]] in [[diagrams]] in [[TopSp]].

The property

* *$X \xrightarrow{f} Y$ is a [[surjective function]]*.

means equivalently that $f$ has the [[right lifting property]]
against the unique map from the [[empty space]] to the [[point space]], 
the simplest map which is not surjective:

\begin{tikzcd}
[
  column sep={between origins, 40pt}, 
  row sep={between origins, 40pt}
]
  \varnothing 
  \ar[rr]
  \ar[dd]
  &&
  X
  \ar[
    dd,
    "{ f }"
  ]
  \\
  \\
  \ast
  \ar[
    rr,
    "{ \forall }"
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  Y
\end{tikzcd}

Namely, a [[commuting diagram]] of the outer form is equivalently just the choice of a single point in $Y$ (this being the [[image]] of the bottom map), and the existence of the dashed lift means that any such point has a [[preimage]] through $f$. This is the very definition of [[surjective function|surjectivity]].

Note that we have defined surjectivity with help of a simplest counterexample: the map on the left is perhaps the simplest example 
of a non-surjective map. We shall see that this pattern holds 
in other examples as well. Part of the reason that a map never has the left lifting property with respect to itself unless it is an isomorphism,
and thus taking the lifting prperty is a simplest way to define a class of morphism not containing a given counterexample or without a given property 
in a matter useful in a diagram chasing computation. 

\linebreak



Similarly, the property

* *$X \xrightarrow{f} Y$ is an [[injective function]]*.

means equivalently that $f$ has the [[right lifting property]]
against the unique map from the [[discrete space]] with two elements $Dsc(\{0,1\})$

$$
  Opens
  \Big(
    Dsc
    \big( 
      \{0,1\}
    \big)
  \Big)
  \;\;
  \coloneqq
  \;\;
  \Big\{
    \varnothing 
    ,\,
    \{0\}
    ,\,
    \{1\}
    ,\,
    \{0,1\}
  \Big\}
$$

to the [[point space]], one of the simplest non-injective maps:

\begin{tikzcd}
[
  column sep={between origins, 40pt}, 
  row sep={between origins, 40pt}
]
  \mathrm{Dsc}
  \big( 
    \boxed{\{\boxed{0},\boxed{1}\}} 
  \big)
  \ar[
    rr,
    "{ \forall }"
  ]
  \ar[dd]
  &&
  X
  \ar[
    dd,
    "{ f }"
  ]
  \\
  \\
  \ast
  \ar[
    rr,
    "{ \forall }"
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  Y
\end{tikzcd}

Namely, that such a lift exists means that the two points in the [[image]] of the top map -- which may be any two points $x_1, x_2 \,\in\, X$ (by the nature of the [[discrete topology]]) such that (by [[commuting diagram|commutativity of the diagram]]) their images are equal, $f(x_1) \,=\, f(x_1) \;\in\; Y$ -- must already have been equal themselves. This is the very definition of [[injective function|injectivity]].


\linebreak


Now consider the variant of the previous example where the 2-element set is equipped instead with the [[codiscrete topology]], whose only [[open subsets]] are the [[empty set]] and the set containing both elements

\[
  \label{OpenSubsetsOfTheCodiscreteSpaceOnTwoElements}
  Opens
  \Big(
    CoDsc
   \big(    
      \{0,1\} 
   \big)
  \Big)
  \;\coloneqq\;
  \big\{
    \begin{array}{l}
      \varnothing, \{0,1\}
    \end{array}
  \big\}
  \,.
\]

In terms of this, the property

* *$X$ is a [[T0-space|$T_0$-space]].

means equivalently that its unique map $X \to \ast$ to the [[point space]] has the [[right lifting property]]
against the unique map from the [[codiscrete space]] with two [[elements]] 
to the [[point space]]:

\begin{tikzcd}
[
  column sep={between origins, 40pt}, 
  row sep={between origins, 40pt}
]
  \mathrm{CoDsc}
  \big( 
    \boxed{\{0\leftrightarrow 1\}} 
  \big)
  \ar[
    rr,
    "{ \forall }"
  ]
  \ar[dd]
  &&
  X
  \ar[dd]
  \\
  \\
  \ast
  \ar[
    rr
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  \ast
\end{tikzcd}

Namely, now [[continuous function|continuity]] restricts the top map to be such that neither $x_i \in\; X$ is contained in an [[open subset]] that does not contain the other (this is the usual way to state the axiom): For if it were, then the [[pre-image]] of that open subset would be $\{x_i\} \,\subset\, CoDsc\big( \{0,1\} \big)$, which however is *not* open (eq:OpenSubsetsOfTheCodiscreteSpaceOnTwoElements). This means that if $X_1$ is a [[T0-space|$T_0$-space]] then any such top map must be the [[constant function]], and this is equivalent to the existence of a lift in the diagram.

Note that [[codiscrete space]] with two points is a simple example of not a $T_0$-space.

\linebreak


Proceeding in this manner, one sees that the property

* *$X$ is a [[T1-space|$T_1$-space]].

means equivalently that its unique map $X \to \ast$ to the [[point space]] has the [[right lifting property]]
against the unique map from the [[Sierpinski space]] $Sierp$,
again the simplest not a $T_1$-space.  

$$
  Set
  \big(
    Sierp
  \big)
  \;\coloneqq\;
  \{0,1\}
  \,,
  \;\;\;\;\;\; 
  Opens
  \big(
    Sierp
  \big)
  \;\coloneqq\;
  \big\{  
    \varnothing 
    ,\,
    \{1\}
    ,\,
    \{0,1\}
  \big\}
$$

to the [[point space]]:

\begin{tikzcd}
[
  column sep={between origins, 40pt}, 
  row sep={between origins, 40pt}
]
  \mathrm{\boxed{\{\boxed{0}\rightarrow 1\}}}
  \ar[
    rr,
    "{ \forall }"
  ]
  \ar[dd]
  &&
  X
  \ar[dd]
  \\
  \\
  \ast
  \ar[
    rr
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  \ast
\end{tikzcd}

Namely, the previous argument applies, but only to the point $0 \in Sierp$, while now $\{1\} \,\subset\, Sierp$ *is* [[open subset|open]]. Therefore the existence of lifts now means that any two points must *both* have an [[open neighbourhood]] not containing the other, which is the definition of a [[T1-space|$T_1$-space]].




Next, a space is [[Hausdorff space|Hausdorff]] (axiom $T_2$) iff every two distinct points have disjoint open neighbourhoods. To give two disjoint open subsets is to give a map to the space with two open points and one closed point. To give two distinct points is to give an injective map. Hence, every two
distinct points have disjoint open neighbourhoods iff any such injective map extends to a map to that space with three points.

* *$X$ is a [[Hausdorff space|$T_2$-space]].

{#IllustrationOfLiftingForT2} This is represented by the following lifting property diagram. 

\begin{tikzcd}
[
  column sep={between origins, 50pt}, 
  row sep={between origins, 40pt}
]
  \boxed{\{0\leftrightarrow 1\}} 
  \ar[
    rr,
    "{ }"
  ]
  \ar[dd, hook, "{ \forall  }"{left} ]
  &&
  \boxed{
    \overset{
      \boxed{
        \boxed{u}
        \;\;
        \,
        \;\;
        \boxed{v}}
      }{
        \underset{
           c
        }
        {
          \searrow \;\, \swarrow
        }
      }
  }  
  \ar[dd]
  \\
  \\
  X
  \ar[
    rr
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  \ast
\end{tikzcd}

\linebreak

Axioms $T_3-T_5$ and others require finite topological spaces with 4 to 7 points, and we need to introduce appropriate notation. 



We give one more reformulation which does not require special notation.
A space is [[extremally disconnected]] iff the closure of an open subset is open, or, equivalently, the closures of disjoint open subsets are disjoint.

* *$X$ is [[extremally disconnected]].

{#IllustrationOfLiftingForExtremallyDisconnected} This is represented by the following lifting property diagram. 

\begin{tikzcd}
[
  column sep={between origins, 50pt}, 
  row sep={between origins, 40pt}
]
 \emptyset
  \ar[
    rr,
    "{ }"
  ]
  \ar[dd]
  && \boxed{
\boxed{{}^{\boxed{u}}\!\! \searrow_{\,c_1}} \,\,\, \boxed{{}_{c_2}\swarrow^{\boxed{v}}}
}
   \ar[dd]
  \\
  \\
  X
  \ar[
    rr
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  \boxed{
    \overset{
      \boxed{
        \boxed{u}
        \;\;
        \,
        \;\;
        \boxed{v}}
      }{
        \underset{
           c
        }
        {
          \searrow \;\, \swarrow
        }
      }
  }
\end{tikzcd}

\linebreak



## Background and notation
 {#BackgroundAndNotation}

In order to economically define and denote the [[finite topological spaces]] which will appear in the [[lifting problems]] discussed below, we may encode them through their *[[specialization order]]*.

Recall that the [[specialisation preorder]] on the [[underlying]] [[set]] of points of a [[topological space]] $X$ is the [[preorder]] whose [[order relation]], for any $x, y \in X$, is

$$
  x \,\leq\, y 
  \;\;\;\;\;\;\text{iff}\;\;\;\;\;\;  
  y \,\in\, cl(x)
  \,,
$$ 

where the right hand side means that the following two equivalent conditions hold:

1. $y$ is in the [[topological closure]] of $x$;

1. every [[open subset]] which contains $x$ also contains $y$.


We may regard these [[preordered sets]] equivalently as ([[thin category|thin]] and [[strict category|strict]]) [[categories]], whose

* [[objects]] are the points of $X$,

* [[morphisms]] reflect the order relation: 

  for $x, y \,\in\, X$ there exists a unique morphism $;\x \,\leftarrow\, y\;$ iff $\;y \,\leq\, x\;$ in the [[specialization order]].

For a [[finite topological space]] $X$, this [[specialisation preorder]] $Spec(X)$ -- or equivalently the corresponding category, which we shall conceptually conflate with the pre-ordering -- uniquely determines the topology:

A [[subset]] $C \,\subset X\,$ is [[closed subset|closed]] iff the following equivalent conditions hold:

1. $C$ [[downward closed subset|downward closed]] in the specialization order;

1. there are no morphisms going out of $C$ in the corresponding category.

Accordingly, we may and will denote [[finite topological spaces]] by showing the [[graph]] containing their points with a system of arrows indicating the generating [[morphisms]] in their corresponding [[specialization preorder]]-[[thin category|category]]. 

In doing so, often it will be convenient to show multiple copies of the *same* object, i.e. the same point. Noticing that in the [[strict category]] corresponding to a [[preorder]], an [[isomorphism]] between two objects does *not imply* their [[equality]], we have and distinguish the following two notations:

* '$=$' denotes an [[identity morphism]],

* '$\leftrightarrow$' denotes an [[isomorphism]]

  (hence, because the [[category]] is [[thin category|thin]], the existence of arrows back and forth $\leftrightarrows$).


For example:

|[[finite topological space]] |[[open subsets]] |[[specialization order]]|as picture | 
|--|--|--|--|
| [[discrete space]] <br/>  $Dsc\big(\{ 0,1 \}\big)$ | $\Big\{\; \varnothing,\, \{0\},\, \{1\},\, \{0,1\} \;\Big\}$ | $\Big\{\; 0 \phantom{\leftarrow} 1 \;\Big\}$| $\boxed{\{\boxed{0},\boxed{1}\}}$ |
| [[Sierpinski space]] <br/> $Sierp$ | $\Big\{\; \varnothing,\, \{1\},\, \{0,1\} \;\Big\}$ | $\Big\{\; 0 \leftarrow 1 \;\Big\}$ | $\boxed{\{\boxed{0}\rightarrow 1\}}$|
| [[codiscrete space]] <br/> $CoDsc\big( \{0,1\} \big)$ | $\Big\{\; \varnothing,\, \{0,1\}  \;\Big\}$ | $\Big\{\; 0 \leftrightarrows 1 \;\Big\}$ |  $\boxed{\{0\leftrightarrow 1\}}$ |
| [[point space]] <br/> $\ast$ | $\Big\{ \varnothing,\, \{0\} = \{1\}  \;\Big\}$ |  $\Big\{\; 0 = 1 \;\Big\}$  | $\boxed{*}$ |


Notice here how in $\big\{\; 0 \leftarrow 1 \;\}$ the point $1$ is [[open point|open]] (as there do emanate arrows form it) while the point ${0}$ is [[closed point|closed]] (as no arrows emanate from it).


Under this identitification of [[finite topological spaces]] $X$ with  [[preordered sets]] regarded as [[thin categories]] $Spec(X)$, the [[continuous maps]] between topological spaces correspond to [[functors]] between their specialization preorders:

$$
  \overset{
    \color{blue}
    {
      \text{continuous function betw.}
      \atop
      \text{finite topological spaces}
    }
    \mathclap{\phantom{\vert_{\vert_{\vert_{\vert_{\vert_{\vert}}}}}}}
  }{
    X \xrightarrow{f} Y
  }
  \;\;\;\;\;\;\;\;\;
  \text{corresponds to}
  \;\;\;\;\;\;\;\;\;
  \overset{
    \color{blue}
    {
      \text{functor between}
      \atop
      \text{ specialization orders }
    }
    \mathclap{\phantom{\vert_{\vert_{\vert_{\vert_{\vert_{\vert}}}}}}}
  }{
    Spec(X) \xrightarrow{Spec(f)} Spec(Y)
  }
  \mathrlap{\,.}
$$

With specialization orders denoted by their generating graphs as before, and using that there is at most one morphism for every ordered pair of objects, we may specify such functors $Spec(f)$ simply by labeling each object in their [[codomain]] by the same symbol as its [[preimage]].

For example

$$
  \big\{\, 0 \,\big\}
  \;\;\;
  \xrightarrow{\phantom{---}}
  \;\;\;
  \big\{\, 0,\, 1  \,\big\}
$$

is to denote the [[functor]] between [[specialization orders]] of [[discrete spaces]] with a single and with two elements, respectively, which takes the point denoted "$0$" on the left to the point denoted by the same symbol "$0$" on the right.

In this notation, the following shows the canonical functors between the four examples of specialization orders from the above list:

$$
  \overset{
    \color{blue}
    {
      \text{discrete space}
      \atop
      \phantom{-}
    }
  }{
    \Big\{\;
      0 
      \phantom{\leftarrow}
      1
    \;\Big\}
  }
  \;\;\xrightarrow{\phantom{---}}\;\;
  \overset{
    \color{blue}
    {
      \text{Sierpinski space}
      \atop
      \phantom{-}
    }
  }{
    \Big\{\;
      0 
      \leftarrow
      1
    \;\Big\}
  }
  \;\;\xrightarrow{\phantom{---}}\;\;
  \overset{
    \color{blue}
    {
      \text{codiscrete space}
      \atop
      \phantom{-}
    }
  }{
    \Big\{\;
      0 
      \leftrightarrows
      1
    \;\Big\}
  }
  \;\;\xrightarrow{\phantom{---}}\;\;
  \overset{
    \color{blue}
    {
      \text{point space}
      \atop
      \phantom{-}
    }
  }{
    \Big\{\;
      0 
      =
      1
    \;\Big\}
  }
  \mathrlap{\,.}
$$


{#ExampleMapIdentifyingThreePoints} Notice here the role of the equality sign: In the denotation of a  functor as above, arrows may be sent to equality signs (but not the other way around): This corresponds to the corresponding [[continuous function]] "gluing" these points, in that it is (at least locally) the [[coprojection]] onto the [[quotient space|quotient]] by the subset of points that are being identified. 

For example, the following denotes the functor corresponding to a map that "glues" three points to each other:

$$
  \left\{
    \;\;
    \array{   
      & & U && && V
      \\
      & \swarrow && \searrow && \swarrow && \searrow
      \\
      a && && x && && b
    }
    \;\;
  \right\}
  \;\;\;\;\;\;\;\;
  \xrightarrow{\phantom{------}}
  \;\;\;\;\;\;\;\;
  \left\{
    \;\;
     \array{
       && U  &\color{red}=& x &\color{red}=& V
       \\
       & \swarrow & && && & \searrow
       \\
       a & & &&  &&  &&   b
     }
    \;\;
  \right\}
$$
In this notation, the open subsets of the domain are 
$$\{\{U\}, \{V\}, \{a,U\}, \{V,b\}, \{U,x,V\}\},\{a,U,x,V,b\}\}
$$
In codomain, points $a$ and $b$ are closed, and the only point left is open.




## Separation of subsets
 {#SeparationOfSubsets}

Here we describe how topological separation of *[[subsets]]* of a [[topological space]] may be expressed in terms of factorizations of their joint [[characteristic function]].

In all of the following, $S$ denotes a [[topological space]] and 

$$
  F,\,G \;\subset\; S
$$

a [[pair]] of [[subsets]].


### Disjoint

We say that a pair of subsets is [[disjoint subset|disjoint]] if their [[intersection]] is [[empty set|empty]]:

\[
  \label{APairOfDisjointSubsets}
  F,\, G \,\subset\, S
  \,,
  \;\;\;\;
  F \cap G \,=\, \varnothing
\] 


This situation (eq:APairOfDisjointSubsets) may equivalently be expressed by a *[[characteristic function|characteristic]]* [[continuous function]] from $S$ to the [[codiscrete topological space]] of 3 elements. We will suggestively denote these three elements by $e_F$, $e_G$ and $e_\varnothing$,

> just a suggestion, please feel free to re-adjust notation

respectively, so that in the [above](#BackgroundAndNotation) notation the codiscrete topology on them reads like this:

$$
  CoDisc
  \big( 
    \{ e_F ,\, e_F ,\, e_{\varnothing} \}  
  \big)
  \;\;
  =
  \;\;
  \big\{
    e_F \leftrightarrows e_G \leftrightarrows e_\varnothing
  \big\}
  \,.
$$

Namely, any function to such a [[codiscrete space]] is continuous, and any function to the set with 3 elements partitions its [[domain]] into the [[disjoint]] [[preimages]] of these three elements, which we may regard as a pair $F, G$ of [[disjoint subsets]] and their [[complement]] $S \setminus \{F \cup G\}$:

\[
  \label{CharacteristicFunctionForPairOfDIsjointSubsets}
  \array{
    S_{F,G}
    &\colon&
    S 
    &\longrightarrow&  
    \big\{
       e_F \leftrightarrow e_G \leftrightarrow e_{\varnothing}
    \big\}
    \\
    &&
    x
    &\mapsto&
    \left\{
    \array{
      e_F &\vert& x \in F
      \\
      e_G &\vert& x \in G
      \\   
      e_\varnothing &\vert& otherwise 
    }
    \right.
  }
\]

We may now encode topological separation properties of the two subsets in terms of factorizations (hence liftings) of this their [[characteristic function]]:




### Topologically disjoint

We say that a disjoint pair of subsets (eq:APairOfDisjointSubsets) is __topologically disjoint__ if there exists a [[neighbourhood]] of one set that is [[disjoint subset|disjoint]] from the other set:  

\[
  \label{PairOfTopologicallyDisjointSubsets}
     F, G \;\text{are topologically disjoint}
     \;\;\;\;\;\;\;\;\;
     \Leftrightarrow
     \;\;\;\;\;\;\;\;\;
     \Big(
       \underset
         {
           U \underset{\mathclap{nbhd}}{\supseteq} F      
         }
         {\exists}
       ,\; 
       U \cap G = \varnothing
     \Big) 
     \;\;or\;\; 
     \Big(
       \underset
         {
           V \underset{\mathclap{nbhd}}{\supseteq} G      
         }
         {\exists}
       ,\; 
       F \cap V = \varnothing
     \Big) 
     \,.
\]

(Notice that topologically disjoint sets must be disjoint.)


The topological separation condition (eq:PairOfTopologicallyDisjointSubsets) on a pair of disjoint subsets means equivalently that their [[characteristic function]] (eq:CharacteristicFunctionForPairOfDIsjointSubsets) factors as

\begin{tikzcd}
[
  column sep={between origins, 60pt}, 
  row sep={between origins, 40pt}
]
  \varnothing
  \ar[dd]
  \ar[rr]
  &&
  \big\{
    e_F 
      \leftrightarrows 
    e_U 
      \to
    e_{\varnothing}
      \leftrightarrows
    e_G 
  \big\}
  \ar[dd]
  \\
  \\
  S
  \ar[
    rr,
    "{ S_{F,G} }"{below}
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  \big\{
    e_F 
      \leftrightarrows 
    e_U 
      =
    e_{\varnothing}
      \leftrightarrows
    e_G 
  \big\}  
\end{tikzcd}


or as


\begin{tikzcd}
[
  column sep={between origins, 60pt}, 
  row sep={between origins, 40pt}
]
  \varnothing
  \ar[dd]
  \ar[rr]
  &&
  \big\{
    e_F 
      \leftrightarrows 
    e_{\varnothing}
      \leftarrow
    e_V
      \leftrightarrows
    e_G 
  \big\}
  \ar[dd]
  \\
  \\
  S
  \ar[
    rr,
    "{ S_{F,G} }"{below}
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  \big\{
    e_F 
      \leftrightarrows 
    e_{\varnothing}
      =
    e_U 
      \leftrightarrows
    e_G 
  \big\}  
\end{tikzcd}







### Topologically separated

  They are __separated__ if each set has a neighbourhood that is disjoint from the other set:
 
   $$ 
     (\exists\; U \stackrel{\circ}\supseteq F,\; U \cap G = \empty)    
        \;\wedge\; 
     (\exists\; V \stackrel{\circ}\supseteq G,\; F \cap V = \empty)
         \;\;\equiv\;\;
     \exists\; U \stackrel{\circ}\supseteq F,\; \exists\; V \stackrel{\circ}\supseteq G,\; U \cap G = \empty \;\wedge\; F \cap V = \empty 
     \,.
   $$
   
   In terms of arrows,   $S_{F,G}: S \longrightarrow  \{F\leftrightarrow \bullet \leftrightarrow G \}$ factors both as 

   $$ 
     S_{F,G}
       \colon 
     S \longrightarrow  \{F \leftrightarrow U \searrow \bullet \leftrightarrow G\} \longrightarrow  \{F\leftrightarrow  U \stackrel{\circ}=\bullet \leftrightarrow G \}
   $$

   and as 
  
   $$ 
     S_{F,G}
       \colon 
     S \longrightarrow  \{F \leftrightarrow \bullet \swarrow V  \leftrightarrow G \} \longrightarrow \{F \leftrightarrow \bullet = V  \leftrightarrow G \} 
   $$ 

   where $ U $, $V $ maps to $\bullet$.
   Notice that separated sets must be topologically disjoint.



### Separated by neighbourhoods

{#SeparatedByNeighbourhoods} They are __separated by neighbourhoods__ if they have disjoint neighbourhoods:
   $$ \exists\; U \stackrel{\circ}\supseteq F,\; \exists\; V \stackrel{\circ}\supseteq G,\; U \cap V = \empty .$$
   The arrow  $S_{F,G}: S \longrightarrow  \{F\leftrightarrow \bullet \leftrightarrow G \}$ factors as 
   $S \longrightarrow \{F \leftrightarrow  U  \searrow \bullet \swarrow  V \leftrightarrow G\}\longrightarrow \{F \leftrightarrow  U  = \bullet =  V \leftrightarrow G\}$
   Notice that sets separated by neighbourhoods must be separated.



### Separated by closed neighbourhoods


They are __separated by closed neighbourhoods__ if they have disjoint closed neighbourhoods:
   $$ \exists\; U \stackrel{\circ}\supseteq F,\; \exists\; V \stackrel{\circ}\supseteq G,\; Cl(U) \cap Cl(V) = \empty .$$
   The arrow  $S_{F,G}: S \longrightarrow  \{F\leftrightarrow \bullet \leftrightarrow G \}$ factors as
   $$ S \longrightarrow \{ F \leftrightarrow U \searrow U' \swarrow \bullet \searrow V' \searrow V \leftrightarrow G \}
   \longrightarrow \{ F \leftrightarrow U = U' = \bullet = V' = V \leftrightarrow G \} $$
   Notice that sets separated by closed neighbourhoods must be separated by neighbourhoods.



### Separated by a function


They are __separated by a function__ if there exists a continuous [[real number|real]]-valued [[function]] on the space that maps $F$ to $0$ and $G$ to $1$:

$$ \exists\; f: S \to \mathbf{R},\; F \subseteq f^*(\{0\}) \;\wedge\; G \subseteq f^*(\{1\}) .$$

The arrow  $S_{F,G}: S \longrightarrow  \{F\leftrightarrow \bullet \leftrightarrow G \}$ factors as    

$$ S \longrightarrow   \{0'\} \cup [0,1] \cup \{1'\}  \longrightarrow  \{ 0'=F \leftrightarrow \bullet \leftrightarrow  1'=G\} $$

where points $0',0$ and $1,1'$ are topologically indistinguishable,
and $0'$ maps to $F$, and $1'$ maps to $G$, and $[0,1]$ maps to $\bullet$.
Notice that sets separated by a function must be separated by closed neighbourhoods (the preimages of $[-\epsilon, \epsilon]$ and $[1-\epsilon, 1+\epsilon]$).



### Precisely separated by a function

Finally, they are __precisely separated by a function__ if there exists a continuous real-valued function on the space that maps precisely $F$ to $0$ and $G$ to $1$:

$$ \exists\; f: S \to \mathbf{R},\; F = f^*(\{0\}) \;\wedge\; G = f^*(\{1\}) .$$
    
The arrow  
$S_{F,G}: S \longrightarrow  \{F\leftrightarrow \bullet \leftrightarrow G \}$ factors as    
    

$$ S \longrightarrow   [0,1]  \longrightarrow  \{ 0=F \leftrightarrow \bullet\leftrightarrow  1=G\}$$

where
  $0'$ maps to $F$, and $1'$ maps to $G$, and $(0,1)$ maps to $\bullet$.
  Notice that sets separated by a function must be separated by closed neighbourhoods (the preimages of $[-\epsilon, \epsilon]$ and $[1-\epsilon, 1+\epsilon]$).
   Notice that sets precisely separated by a function must be separated by a function.

Often $F$ and $G$ will be points (identified with their [[singleton]] subsets); in that case, one usually says _distinct_ in place of _disjoint_.

Often $F$ or $G$ will be closed sets; notice that disjoint closed sets are automatically separated, while a closed set and a point, if disjoint, are automatically topologically disjoint.


\linebreak


## Separation axioms as lifting properties 
 {#SeparationAxiomsAsLiftingProperties}

In all of the following definitions, ${X}$ is  a topological space.

We shall use the symbol "$\rightthreetimes$" to denote the [[lifting property]] of one map against another (compare *[[Joyal-Tierney calculus]]*):

So for $S \xrightarrow{\phi} T $ and $X \xrightarrow{f} Y$ a [[pair]] of [[continuous functions]] between topological spaces, we write

$$
  \phi \;\rightthreetimes\; f
  \;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;
  \phi \;\text{has the left lifting property against}\; f
$$ 

\begin{tikzcd}
[
  column sep={between origins, 40pt}, 
  row sep={between origins, 40pt}
]
  S
  \ar[
    rr,
    "{ \forall }"
  ]
  \ar[
    dd,
    "{ \phi }"
  ]
  &&
  X
  \ar[
    dd,
    "{ f }"
  ]
  \\
  \\
  T
  \ar[
    rr,
   "{ \forall }"
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  Y
\end{tikzcd}


With this notation, we have the following dictionary between [[lifting properties]] and [[separation axioms]]:

*  $ {X}$  is [[T0-space|$T_0$]], (or [[Kolmogorov topological space|Kolmogorov]]), if any two distinct points in ${X}$ are topologically
distinguishable. (It will be a common theme among the separation axioms to have
one version of an axiom that requires T0 and one version that doesn't.)
As a formula, this is expressed as
   $$ 
     \{x\leftrightarrow y\} \longrightarrow  \{x=y\} 
     \;\;\,\rightthreetimes\,\;\;  
     {X} \longrightarrow  \{*\}
   $$

*  ${X}$ is R0, or symmetric, if any two topologically distinguishable points in $X$
are separated, i.e.
   $$ 
     \{x{\searrow}y\} \longrightarrow  \{x\leftrightarrow y\}     
     \;\;\;\,\rightthreetimes\,\;\;\;  
     {X} \longrightarrow  \{*\} 
   $$

*  $X$ is T1, or accessible or Frechet, if any two distinct points in $X$ are separated, i.e.
   $$     
     \{x{\searrow}y\} \longrightarrow  \{x=y\} 
     \;\;\;\,\rightthreetimes\,\;\;\;  
     {X} \longrightarrow  \{*\}  
   $$
   
   Thus, $X$ is T1 if and only if it is both T0 and R0. (Although you may
say such things as "T1 space", "Frechet topology", and "Suppose that the
topological space $X$ is Frechet", avoid saying "Frechet space" in this
context, since there is another entirely different notion of Frechet space in
functional analysis.)

*  $X$ is R1, or preregular, if any two topologically distinguishable points in X are separated by neighbourhoods. Every R1 space is also R0.

*  $X$ is [[weakly Hausdorff topological space|weakly Hausdorff]], if the image of every continuous map from a [[compact Hausdorff space]] into $X$ is closed. All weak Hausdorff spaces are T1, and all Hausdorff spaces are weak Hausdorff.

*  $X$ is [[Hausdorff space|Hausdorff]], or T2 or separated, if any two distinct points in $X$ are separated by neighbourhoods, i.e.

   $$    
     \{x,y\} \hookrightarrow  {X} 
     \;\;\;\,\rightthreetimes\,\;\;\;  
     \{x{\searrow}X{\swarrow}y\} \longrightarrow  \{x=X=y\} 
   $$


   Thus, $X$ is Hausdorff if and only if it is both T0 and R1. Every Hausdorff space is also T1.

*  $X$ is $T2\frac{1}{2}$, or Urysohn, if any two distinct points in $X$ are separated by closed neighbourhoods. As a lifting property this is
   $$
    \{x,y\} \hookrightarrow  {X} 
    \;\;\;\,\rightthreetimes\,\;\;\;
     \boxed{\{\overset{\boxed{x}}{}{\searrow}\underset{U}{}{\swarrow}\overset{\boxed{X}}{}
}\!\!\!\!\!\!\!
\boxed{
{\,\,\,\,\,\,\searrow}\underset{V}{}{\swarrow}\overset{\boxed{y}}{}
}
\}     \longrightarrow  \{\boxed{x=x'=X=y'=y}\}
   $$
Indeed, the closed neighbourhoods would be the preimages under the diagonal arrow of closed subsets
$\big\{\overset{\boxed{x}}{}{\searrow}\underset{U}{}\big\} $
and $\big\{\underset{V}{}{\swarrow}\overset{\boxed{y}}{}\big\}$.

   Every $T2\frac{1}{2}$ space is also Hausdorff.

*  $X$ is completely Hausdorff, or completely T2, if any two distinct points in X are separated by a continuous function, i.e. 

   $$ 
     \{x,y\} \hookrightarrow  {X} 
     \;\;\;\,\rightthreetimes\,\;\;\;   
     [0,1]\longrightarrow \{*\}
   $$
 
   where  $\{x,y\} \hookrightarrow  X$  runs through all injective maps from the discrete two point space $\{x,y\}$.

   Every completely Hausdorff space is also $ T2\frac{1}{2} $.

*  $X$ is [[regular topological space|regular]] if, given any point ${x}$ and closed subset $F$ in $X$ such that ${x}$ does not belong to $F$, they are separated by neighbourhoods, i.e.
   $$    
      \{x\} \longrightarrow  {X} 
      \;\;\;\,\rightthreetimes\,\;\;\;  
\{
\boxed{
 \boxed{
\overset{\boxed{x}}{}
\searrow
\underset{X}{} \swarrow
\overset{\boxed{U}}{}
}\!\!\!\!\!\!\!
{\,\,\,\,\,\,\searrow\underset{F}{} }
}
\}
        \longrightarrow  
      \{\overset{\boxed{x=X=U}}{}\searrow\underset{F}{}\}
   $$
Indeed, the separating neighbourhoods would be 
the preimage under the diagonal arrow of 
$\{\boxed{x}\}$ and $\{\overset{\boxed{U}}{}\searrow\underset{F}{}\}$.

   (In fact, in a regular space, any such ${x}$ and ${F}$ will also be separated by closed neighbourhoods.) Every
regular space is also R1.

*  $X$ is regular Hausdorff, or T3, if it is both T0 and regular.[1] Every
regular Hausdorff space is also $T2\frac{1}{2}$.

*  $X$ is completely regular if, given any point ${x}$ and closed set $F$ in $X$ such that ${x}$ does not belong to $F$, they are separated by a continuous function, i.e. 

   $$
     \{x\} \longrightarrow  {X} 
     \;\;\;\,\rightthreetimes\,\;\;\;  
     [0,1] \cup \{F\} \longrightarrow  \{x{\searrow}F\}
   $$ 

   where points $F$ and $1$ are topologically indistinguishable, $[0,1]$ goes to $x$, and $F$ goes to $F$.

   Every completely regular space is also regular.

*  $X$ is [[Tychonoff space|Tychonoff]], or T3$\frac{1}{2}$, completely T3, or completely regular Hausdorff, if it is both T0 and completely regular.[2] Every Tychonoff space is both regular Hausdorff and completely Hausdorff.

*  $X$ is [[normal topological space|normal]] if any two disjoint closed subsets of $X$ are separated by neighbourhoods, i.e.
   $$   
      \emptyset \longrightarrow {X} 
      \;\;\;\,\rightthreetimes\,\;\;\;      
      \{\underset{x}{}{\swarrow}
        \overset{U}{}{\searrow}
      \underset{X}{}{\swarrow}\overset{V}{}{\searrow}\underset{y}{}\} 
         \longrightarrow  
      \{\underset{x}{}{\swarrow}\overset{\boxed{U=X=V}}{}{\searrow}
       \underset{y}{}\}
   $$
Indeed, the separating neighbourhoods are the preimages of 
open subsets $\big\{\underset{x}{}{\swarrow}
        \overset{U}{}\big\}$ 
and $\big\{\overset{V}{}{\searrow}\underset{y}{}\big\}$.

   In fact, by [[Urysohn's lemma]] a space is normal if and only if any two disjoint closed sets can be separated by a continuous function, i.e.

   $$   
      \emptyset \longrightarrow  {X} 
      \;\;\;\,\rightthreetimes\,\;\;\;  
      \{0'\} \cup [0,1] \cup \{1'\} 
      \longrightarrow  \{0=0'{\searrow}x{\swarrow}1=1'\} 
   $$

   where points $0',0$ and $1,1'$ are topologically indistinguishable, $[0,1]$ goes to $x$, and both $0,0'$ map to point $0=0'$,  and both $1,1'$ map to point $1=1'$.


*  $X$ is normal Hausdorff, or T4, if it is both T1 and normal. Every normal
Hausdorff space is both Tychonoff and normal regular.

*  $X$ is _completely or heriditarily normal_ if any two separated sets $A$ and $B$ are separated by neighbourhoods $U\supset A$ and $V\supset B$ such that $U$ and $V$ do not intersect, i.e.
   $$
     \emptyset \longrightarrow  {X} 
     \;\;\;\,\rightthreetimes\,\;\;\;  
     \{
      \underset{X}{}{\swarrow}
     \overset{A\leftrightarrow U}{}
     {\searrow} \underset{U'}{}{\swarrow}
     \overset{W}{} {\searrow}
     \underset{V'}{}{\swarrow} 
     \overset{V\leftrightarrow B}{}{\searrow}
     \underset{X}{} \} \longrightarrow  \{U=U',V'=V\}
   $$
      
   Every completely normal space is also normal.


*  $X$ is [[perfectly normal topological space|perfectly normal]] if any two disjoint closed sets are precisely separated by a continuous function, i.e. 

   $$
    \emptyset\longrightarrow {X} 
      \;\;\;\,\rightthreetimes\,\;\;\;  
    [0,1]\longrightarrow \{0{\swarrow}X{\searrow}1\}
   $$   

   where $(0,1)$ goes to the open point $X$, and $0$ goes to $0$, and $1$ goes to $1$.

   Every perfectly normal space is also completely normal.


*  The [[Tietze extension theorem]] applies to [[normal spaces]].

   Accordingly, a (Hausdorff) space $X$ is normal if and only if every function $f \colon A \to \mathbb{R}$ from a [[closed subspace]] $A \subset X$ admits an [[extension]] $\tilde{f}: X \to \mathbb{R}$, 

   $$
     \array{
       A &\overset{f}{\longrightarrow}& \mathbb{R}
       \\
       \downarrow & \nearrow_{\mathrlap{\tilde f}}
       \\
       X
     }
   $$

   or what is the same, every [[regular monomorphism]] into $X$ in $Haus$ has the [[left lifting property]] with respect to the map $\mathbb{R} \to 1$. 



\begin{remark}
A standard proof of [[Urysohn's lemma]] may be represented as follows: 
iterate the lifting property to prove 

$$ 
  \emptyset \longrightarrow X
  \;\;\;\;\rightthreetimes\;\;\;\; 
  \{
\underset{x}{} \swarrow 
\overset{x_1}{} \searrow \cdots \swarrow 
\overset{x_n}{} \searrow 
\underset{y}{} \} 
  \longrightarrow  
  \{
\underset{x}{} \swarrow 
\overset{x_1 = \cdots = x_n}{} \searrow 
\underset{y}{} \}
$$

Then pass to the infinite limit to construct a map  $ X \longrightarrow  \mathbb{R}$.
\end{remark}


## Related concepts

* [Tychonoff theorem -- Proof via lifting properties](Tychonoff+theorem#ProofViaTaimanovTheoremAndLiftingProperties)

## References

* {#Gavrolovich14} [[Misha Gavrilovich]], *Point set topology as diagram chasing computations*,  The De Morgan Gazette. 2014. Vol. 5. No. 4. P. 23-32.  ([arXiv:1408.6710](https://arxiv.org/abs/1408.6710), [pdf](http://mishap.sdf.org/mints-lifting-property-as-negation-DMG_5_no_4_2014.pdf))

* [[Misha Gavrilovich]], *The unreasonable power of the lifting property in elementary mathematics*, 2017 ([arXiv:1707.06615](https://arxiv.org/abs/1707.06615),  [pdf](http://mishap.sdf.org/by:gavrilovich/expressive_power_of_the_lifting_property.pdf))

* [[Misha Gavrilovich]], Konstantin Pimenov. *A naive diagram chasing approach to formalisation of tame topology.*, 2018 ([pdf](http://mishap.sdf.org/mintsGE.pdf))

* [[Misha Gavrilovich]], *Extremally disconnected spaces as $\{\{u\to a,b\leftarrow v\}\to\{u\to a=b\leftarrow v\}\}^{lr}$, and being proper as $(\{\{o\}\to\{o\to c\}\}^r_{\le 4})^{lr}$*, 2021 ([pdf](http://mishap.sdf.org/yetanothernotanobfuscatedsyntax.pdf))
