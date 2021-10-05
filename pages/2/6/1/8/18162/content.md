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

In [[topology]], some of the [[separation axioms]] that may be considered on [[topological spaces]] may equivalently be reformulated in terms of [[lifting properties]] ([Gavrilovich 2014](#&solb;)) with respect to simple or archetypal counterexamples represented by finite preorders, and closely following standard definitions. It is convenient to refer
as _the left/right [[Quillen negation]] of a morphism_
to the class of morphism having the left/right lifting property
with respect to the morphism, and say that the separation axioms
are defined by the Quillen negation of archetypal counterexamples.

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
    \{0\}
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

Namely, the previous argument applies, but only to the point $1 \in Sierp$, while now $\{0\} \,\subset\, Sierp$ *is* [[open subset|open]]. Therefore the existence of lifts now means that any two points must *both* have an [[open neighbourhood]] not containing the other, which is the definition of a [[T1-space|$T_1$-space]].




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
| [[Sierpinski space]] <br/> $Sierp$ | $\Big\{\; \varnothing,\, \{0\},\, \{0,1\} \;\Big\}$ | $\Big\{\; 0 \rightarrow 1 \;\Big\}$ | $\boxed{\{\boxed{0}\rightarrow 1\}}$|
| [[codiscrete space]] <br/> $CoDsc\big( \{0,1\} \big)$ | $\Big\{\; \varnothing,\, \{0,1\}  \;\Big\}$ | $\Big\{\; 0 \leftrightarrow 1 \;\Big\}$ |  $\boxed{\{0\leftrightarrow 1\}}$ |
| [[point space]] <br/> $\ast$ | $\Big\{ \varnothing,\, \{0\} = \{1\}  \;\Big\}$ |  $\Big\{\; 0 = 1 \;\Big\}$  | $\boxed{*}$ |


Notice here how in $\big\{\; 0 \rightarrow 1 \;\}$ the point $0$ is [[open point|open]] (as there do emanate arrows form it) while the point ${1}$ is [[closed point|closed]] (as no arrows emanate from it).


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
      \rightarrow
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
      \leftrightarrow
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
In the codomain, points $a$ and $b$ are closed, and the only point left is open.




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
    e_F \leftrightarrow e_G \leftrightarrow e_\varnothing
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


Often $F$ and $G$ will be points (identified with their [[singleton]] subsets); in that case, one usually says _distinct_ in place of _disjoint_.

Often $F$ or $G$ will be closed sets; notice that disjoint closed sets are automatically separated, while a closed set and a point, if disjoint, are automatically topologically disjoint.

To express the assumption that $F$ or $G$ is closed, we may modify the topology on $\{e_F,e_{\varnothing}, e_G$ and make the points $e_F$ and/or $e_G$ closed as appropriate.




### Topologically disjoint
 {#TopologicallyDisjoint}

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
         \;\;
       U \cap G = \varnothing
     \Big)
     \;\;or\;\;
     \Big(
       \underset
         {
           V \underset{\mathclap{nbhd}}{\supseteq} G
         }
         {\exists}
       \;\;
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
      \leftrightarrow
    e_U
      \to
    e_{\varnothing}
      \leftrightarrow
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
      \leftrightarrow
    e_U
      =
    e_{\varnothing}
      \leftrightarrow
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
      \leftrightarrow
    e_{\varnothing}
      \leftarrow
    e_V
      \leftrightarrow
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
      \leftrightarrow
    e_{\varnothing}
      =
    e_U
      \leftrightarrow
    e_G
  \big\}
\end{tikzcd}

The required neighbourhoods $U\supset F$ or $V\supset B$ are
the preimages under the diagonal arrow of the open neighbourhoods
$ \big\{
    e_F
      \leftrightarrow
        e_{\varnothing}
  \big\}$ of point $e_F$, or
$ \big\{
        e_{\varnothing}
      \leftrightarrow
    e_G
  \big\}
$ of point $e_G$, respectively.







### Topologically separated
 {#TopologicallySeparated}


We say that a disjoint pair of subsets (eq:APairOfDisjointSubsets) is
__separated__ if each set has a [[neighbourhood]] that is [[disjoint subset|disjoint]] from the other set:

\[
  \label{PairOfSeparatedSubsets}
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
     \;\;and\;\;
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

(Notice that separated sets must be topologically disjoint and disjoint.)


The separation condition (eq:PairOfSeparatedSubsets) on a pair of disjoint subsets means equivalently that
their characteristic function
(eq:CharacteristicFunctionForPairOfDIsjointSubsets)
factors as


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
      \leftrightarrow
    e_U
      \to
    e_{\varnothing}
      \leftrightarrow
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
      \leftrightarrow
    e_U
      =
    e_{\varnothing}
      \leftrightarrow
    e_G
  \big\}
\end{tikzcd}


and as


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
      \leftrightarrow
    e_{\varnothing}
      \leftarrow
    e_V
      \leftrightarrow
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
      \leftrightarrow
    e_{\varnothing}
      =
    e_V
      \leftrightarrow
    e_G
  \big\}
\end{tikzcd}

The two diagrams above can equivalently be combined into a single diagram;
the separating neighbourhoods $U\supset F$ and $V\supset B$ are
the preimages under the diagonal arrow of the open subsets
$ \big\{
    e_F
      \leftrightarrow
    e_U \leftarrow
        e_{\varnothing}
  \big\}$ and
$ \big\{
        e_{\varnothing}
      \rightarrow
    e_V
      \leftrightarrow
    e_G
  \big\}
$.




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
      \leftrightarrow
    e_U \leftarrow
        e_{\varnothing}
      \rightarrow
    e_V
      \leftrightarrow
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
      \leftrightarrow
    e_U=
    e_{\varnothing}
      =
    e_V
      \leftrightarrow
    e_G
  \big\}
\end{tikzcd}



### Separated by neighbourhoods
 {#SeparatedByNeighbourhoods}

We say that a disjoint pair of subsets (eq:APairOfDisjointSubsets) is
__separated by neighbourhoods__ if the sets have [[disjoint subset|disjoint]] [[neighbourhoods]]

\[
  \label{PairOfSeparatedNeighbourhoods}
  U \subseteq V
  \;\text{and}\;
  V \subseteq G
  \;\;\;\text{such that}\;\;\;
  U \cap V = \varnothing
  \,.
\]

The separation condition (eq:PairOfSeparatedNeighbourhoods) on a pair of disjoint subsets means equivalently that
their characteristic function
(eq:CharacteristicFunctionForPairOfDIsjointSubsets)
factors as

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
      \leftrightarrow
    e_U \rightarrow
        e_{\varnothing}
      \leftarrow
    e_V
      \leftrightarrow
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
      \leftrightarrow
    e_U=
    e_{\varnothing}
      =
    e_U
      \leftrightarrow
    e_G
  \big\}
\end{tikzcd}
The separating neighbourhoods $U\supset F$ and $V\supset B$ are
the preimages under the diagonal arrow of the open subsets
$ \big\{
    e_F
      \leftrightarrow
    e_U
  \big\}$ and
$ \big\{e_V
      \leftrightarrow
    e_G
  \big\}
$.


### Separated by closed neighbourhoods


{#eq:PairOfSeparatedClosedNeighbourhoods}
We say that a disjoint pair of subsets (eq:APairOfDisjointSubsets) is
__separated by neighbourhoods__ if the sets have [[disjoint subset|disjoint]] closed [[neighbourhoods]], i.e. there exist
$U\subseteq V$ and $V\subseteq G$ such that their closures
$\bar U$ and $ \bar V$ do not intersect


\[
  \label{PairOfSeparatedClosedNeighbourhoods}
  U \subseteq V
  \;\text{and}\;
  V \subseteq G
  \;\;\;\;\;\;
  \text{such that}
  \;\;\;\;\;\;
  \bar U \cap \bar V
  \;=\;
  \varnothing
\]

The separation condition (eq:PairOfSeparatedClosedNeighbourhoods) on a pair of disjoint subsets means equivalently that
their characteristic function
(eq:CharacteristicFunctionForPairOfDIsjointSubsets)
factors as

\begin{tikzcd}
[
  column sep={between origins, 75pt},
  row sep={between origins, 40pt}
]
  \varnothing
  \ar[dd]
  \ar[rr]
  &&
  \big\{
    e_F
      \leftrightarrow
    e_U \rightarrow
    e_{\bar U} \leftarrow
        e_{\varnothing} \rightarrow
    e_{\bar V}
      \leftarrow
    e_V
      \leftrightarrow
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
      \leftrightarrow
    e_U=e_{\bar U}=
    e_{\varnothing}
      =
    e_{\bar V}=e_V
      \leftrightarrow
    e_G
  \big\}
\end{tikzcd}

The separating closed neighbourhoods $\bar U\supset F$ and $\bar V\supset B$ are
the preimages under the diagonal arrow of the closed neighbourhoods
$ \big\{
    e_F
      \leftrightarrow
   e_U \rightarrow
   e_{\bar U} \big\}$ of point $e_F$, and
$ \big\{
  e_{\bar V}
      \leftarrow
  e_V
      \leftrightarrow
    e_G
  \big\}
$ of point $e_G$.



### Separated by a function


We say that two disjoint subsets $F$ and $G$ are __separated by a function__ if there exists a continuous [[real number|real]]-valued [[function]] on the space that maps $F$ to $0$ and $G$ to $1$:

\[
  \label{ConditionForSeparationByAFunction}
  \underset
    {f \,\colon\, S \to \mathbb{R}}
    {\exists}
  \left(
    F \subseteq f^{-1}(\{0\})
    \;\wedge\;
    G \subseteq f^{-1}(\{1\})
  \right)
\]

Equivalently, we may assume that $f$ takes values in $[0,1]\subseteq \mathbb{R}$.


This separation condition (eq:ConditionForSeparationByAFunction) on a pair of disjoint subsets means equivalently that
their characteristic function
(eq:CharacteristicFunctionForPairOfDIsjointSubsets)
factors as

\begin{tikzcd}
[
  column sep={between origins, 60pt},
  row sep={between origins, 40pt}
]
  \varnothing
  \ar[dd]
  \ar[rr]
  &&
  {[0,1]}\vee_{\{0,1\}} \{e_F\leftrightarrow 0, 1\leftrightarrow e_G\}
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
      \leftrightarrow
    e_{[0,1]}
      \leftrightarrow
    e_G
  \big\}
\end{tikzcd}
If $f:S\to [0,1]$ in a separating function as above, we may take the diagonal arrow defined as
\[
  \label{CharacteristicFunctiontoR01ForPairOfDIsjointSubsets}
  \array{
    f'
    &\colon&
    S
    &\longrightarrow& [0,1]\vee_{\{0,1\}} \{0'\leftrightarrow 0, 1\leftrightarrow 1\}
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
      f(x) &\vert& otherwise
    }
    \right.
  }
\]


### Precisely separated by a function

Finally, we say that two disjoint subsets $F$ and $G$ are __separated by a function__ if there exists a continuous [[real number|real]]-valued [[function]] on the space that maps precisely $F$ to $0$ and $G$ to $1$:

\[
  \label{ConditionForPreciseSeparationByAFunction}
  \underset
    {f \,\colon\, S \to \mathbf{R}}
    {\exists}
  \left(
    F \,=\, f^{-1}(\{0\})
    \;\;\wedge\;\;
    G \,=\, f^{-1}(\{1\})
  \right)
\]

Equivalently, we may assume that $f$ takes values in $[0,1]\subseteq \mathbb{R}$.


This separation condition (eq:ConditionForPreciseSeparationByAFunction) on a pair of disjoint subsets means equivalently that
their characteristic function
(eq:CharacteristicFunctionForPairOfDIsjointSubsets)
factors as

\begin{tikzcd}
[
  column sep={between origins, 60pt},
  row sep={between origins, 40pt}
]
  \varnothing
  \ar[dd]
  \ar[rr]
  && [0,1]
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
    0
      \leftrightarrow
    e_{(0,1)}
      \leftrightarrow
    1
  \big\}
\end{tikzcd}
If $f:S\to [0,1]$ in a separating function as above, we may take the diagonal arrow defined as
\[
  \label{CharacteristicFunctiontoRForPairOfDIsjointSubsets}
  \array{
    f'
    &\colon&
    S
    &\longrightarrow&
  {[0,1]}
    \\
    &&
    x
    &\mapsto&
    \left\{
    \array{
      0 &\vert& x \in F
      \\
      1 &\vert& x \in G
      \\
      f(x) &\vert& otherwise
    }
    \right.
  }
\]


  Notice that sets separated by a function must be separated by closed neighbourhoods (the preimages of $[-\epsilon, \epsilon]$ and $[1-\epsilon, 1+\epsilon]$).
   Notice that sets precisely separated by a function must be separated by a function.


\linebreak


## Separation axioms as lifting properties
 {#SeparationAxiomsAsLiftingProperties}

In all of the following definitions, ${X}$ is  a topological space.

We shall use the symbol "$&solb;$" to denote the [[lifting property]] of one map against another (compare *[[Joyal-Tierney calculus]]*):

So for $S \xrightarrow{\phi} T $ and $X \xrightarrow{f} Y$ a [[pair]] of [[continuous functions]] between topological spaces, we write

$$
  \phi \;&solb;\; f
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


With this notation, we have the following dictionary between [[lifting properties]] and [[separation axioms]].


### Kolmogorov spaces ($T_0$)
 {#KolmogorovSpaces}

A topological space ${X}$  is [[T0-space|$T_0$]] (or [[Kolmogorov topological space|Kolmogorov]]) if any two distinct points in ${X}$ are [topologically disjoint](#TopologicallyDisjoint).

(It will be a common theme among the following separation axioms to have
one version of an axiom that requires $T_0$ and one version that doesn't.)

This condition is equivalent to the [[lifting property]]

$$
  \big(
    \{x\leftrightarrow y\} \longrightarrow  \{x=y\}
  \big)
  \;\;\,&solb;\,\;\;
  \big(
    {X} \longrightarrow  \{*\}
  \big)
$$

hence:

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


### Symmetric spaces ($R_0$)
 {#SymmetricSpaces}

A topological space ${X}$ is an [[R0-space|$R_0$-space]] (also: *symmetric space*), if any two [topologically distinguishable](#TopologicallyDisjoint) points in $X$ are [topologically separated](#TopologicallySeparated).

This condition is equivalent to the following [[lifting property]]:

$$
  \big(
    \{x{\searrow}y\} \longrightarrow  \{x\leftrightarrow y\}
  \big)
  \;\;\;\,&solb;\,\;\;\;
  \big(
    {X} \longrightarrow  \{*\}
  \big)
  \,.
$$


### Accessible spaces ($T_1$)

$X$ is [[T1-space|$T_1$]] (or *accessible* or *Fréchet*) if any two distinct points in $X$ are separated, i.e.

   $$
     \{x{\searrow}y\} \longrightarrow  \{x=y\}
     \;\;\;\,&solb;\,\;\;\;
     {X} \longrightarrow  \{*\}
   $$

 Thus, $X$ is T1 if and only if it is both T0 and R0: indeed, a morphism lifts wrt the composition 
$ \{x{\searrow}y\} \longrightarrow  \{x\leftrightarrow y\} \longrightarrow  \{x=y\}$
iff it lifts wrt either one of the two morphisms. (Although you may
say such things as "T1 space", "Frechet topology", and "Suppose that the
topological space $X$ is Frechet", avoid saying "Frechet space" in this
context, since there is another entirely different notion of Frechet space in
functional analysis.)


### Reregular spaces ($R_1$)

$X$ is R1, or preregular, if any two topologically distinguishable points in X are separated by neighbourhoods. Every R1 space is also R0.



### Weakly Hausdorff spaces


$X$ is [[weakly Hausdorff topological space|weakly Hausdorff]], if the image of every continuous map from a [[compact Hausdorff space]] into $X$ is closed. All weak Hausdorff spaces are T1, and all Hausdorff spaces are weak Hausdorff.


### Hausdorff spaces ($T_2$)

$X$ is [[Hausdorff space|Hausdorff]], or T2 or separated, if any two distinct points in $X$ are separated by neighbourhoods, i.e.

   $$
     \{x,y\} \hookrightarrow  \underset{X}{}
     \;\;\;\,&solb;\,\;\;\;
       \{x{\searrow}\underset{X}{}{\swarrow}y\} \longrightarrow  \{x=X=y\}
   $$
As a lifting diagram this is 
\begin{tikzcd}
[
  column sep={between origins, 80pt},
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
        \boxed{x}
        \;\;
        \,
        \;\;
        \boxed{y}}
      }{
        \underset{
           X
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
   \{x=X=y\}
\end{tikzcd}
The interesting case is when the top horizontal arrow 
$     \{x,y\} \to
       \{x{\searrow}\underset{X}{}{\swarrow}y\} $
maps $x$ and $y$ to the open points $x$ and $y$;
in that case the separating neighbourhoods are the preimages of the open points $x$ and $y$ under the diagonal arrow. 
In the other cases both points map to a copy of $\{0\to 1\}$,
and the lifting property reduces to $T_1$. In particular, 
we see that every  Hausdorff space is also T1.

   Also, $X$ is Hausdorff if and only if it is both T0 and R1. 



### Urysohn spaces ($T_{2 \tfrac{1}{2}}$)

$X$ is $T2\frac{1}{2}$, or Urysohn, if any two distinct points in $X$ are separated by closed neighbourhoods. As a lifting property this is
   $$
    \{x,y\} \hookrightarrow  {X}
    \;\;\;\,&solb;\,\;\;\;
     \boxed{\{\overset{\boxed{x}}{}{\searrow}\underset{U}{}{\swarrow}\overset{\boxed{X}}{}
}\!\!\!\!\!\!\!
\boxed{
{\,\,\,\,\,\,\searrow}\underset{V}{}{\swarrow}\overset{\boxed{y}}{}
}
\}     \longrightarrow  \{\boxed{x=x'=X=y'=y}\}
   $$

As a lifting diagram this is 
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
 \{\boxed{\overset{\boxed{x}}{}{\searrow}\underset{U}{}{\swarrow}\overset{\boxed{X}}{}
}\!\!\!\!\!\!\!
\boxed{
{\,\,\,\,\,\,\searrow}\underset{V}{}{\swarrow}\overset{\boxed{y}}{}
}
\}     
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
\{\boxed{x=x'=X=y'=y}\}
\end{tikzcd}
The interesting case is when the top horizontal arrow 
maps $x$ and $y$ to the open points $x$ and $y$;
in that case the separating closed neighbourhoods are 
of closed subsets
$\big\{\overset{\boxed{x}}{}{\searrow}\underset{U}{}\big\} $
and $\big\{\underset{V}{}{\swarrow}\overset{\boxed{y}}{}\big\}$
under the diagonal arrow. The other cases are similar but easier. 

Note the 5-point space here contains a copy of the 3-point space used in $T_2$. Hence,    every $T2\frac{1}{2}$ space is also Hausdorff.



### Completely Hausdorff spaces

$X$ is completely Hausdorff, or completely T2, if any two distinct points in X are separated by a continuous function, i.e.

   $$
     \{x,y\} \hookrightarrow  {X}
     \;\;\;\,&solb;\,\;\;\;
     [0,1]\longrightarrow \{*\}
   $$

   where  $\{x,y\} \hookrightarrow  X$  runs through all injective maps from the discrete two point space $\{x,y\}$.
As a lifting diagram this is 

\begin{tikzcd}
[
  column sep={between origins, 60pt},
  row sep={between origins, 40pt}
]
  \{x,y\}
  \ar[dd]
  \ar[rr]
  &&
  {[0,1]}\vee_{\{0,1\}} \{x\leftrightarrow 0, 1\leftrightarrow x\}
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
  \big\{
    x
      \leftrightarrow
    e_{[0,1]}
      \leftrightarrow
    y
  \big\}
\end{tikzcd}

Every completely Hausdorff space is also $ T2\frac{1}{2} $
because there is a surjection 
${[0,1]}\vee_{\{0,1\}} \{x\leftrightarrow 0, 1\leftrightarrow y\}
  \to
 \{\boxed{\overset{\boxed{x}}{}{\searrow}\underset{U}{}{\swarrow}\overset{\boxed{X}}{}
}\!\!\!\!\!\!\!
\boxed{
{\,\,\,\,\,\,\searrow}\underset{V}{}{\swarrow}\overset{\boxed{y}}{}
}
\}     
$.


### Regular spaces

$X$ is [[regular topological space|regular]] if, given any point ${x}$ and closed subset $F$ in $X$ such that ${x}$ does not belong to $F$, they are separated by neighbourhoods, i.e.
   $$
      \{x\} \longrightarrow  {X}
      \;\;\;\,&solb;\,\;\;\;
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
Indeed, in the interesting  case that $x$ maps to $x$
by the top horizontal arrow, 
the separating neighbourhoods would be
the preimage under the diagonal arrow of
$\{\boxed{x}\}$ and $\{\overset{\boxed{U}}{}\searrow\underset{F}{}\}$.

   (In fact, in a regular space, any such ${x}$ and ${F}$ will also be separated by closed neighbourhoods.) Every
regular space is also R1.


### Regular Hausdorff space ($T_3$)

$X$ is a [[regular Hausdorff space]], or T3, if it is both T0 and regular.[1] Every
regular Hausdorff space is also $T2\frac{1}{2}$.



### Completely regular spaces

$X$ is completely regular if, given any point ${x}$ and closed set $F$ in $X$ such that ${x}$ does not belong to $F$, they are separated by a continuous function, i.e.

   $$
     \{x\} \longrightarrow  {X}
     \;\;\;\,&solb;\,\;\;\;
     [0,1] \vee_{\{1\}} {\{1\leftrightarrow F\}}
        \longrightarrow  \{ \overset{e_{[0,1]}}{}  \searrow F\}
   $$
Here in $[0,1] \vee_{\{1\}} {\{1\leftrightarrow F\}}$
the points $F$ and $1$ are topologically indistinguishable, $[0,1]$ goes to $x$, and $F$ goes to $F$.

   Every completely regular space is also regular.



### Tychonoff spaces ($T_{3 \tfrac{1}{2}}$)


$X$ is [[Tychonoff space|Tychonoff]], or T3$\frac{1}{2}$, completely T3, or completely regular Hausdorff, if it is both T0 and completely regular.[2] Every Tychonoff space is both regular Hausdorff and completely Hausdorff.



### Normal spaces

$X$ is [[normal topological space|normal]] if any two disjoint closed subsets of $X$ are separated by neighbourhoods, i.e.
   $$
      \emptyset \longrightarrow {X}
      \;\;\;\,&solb;\,\;\;\;
      \{\underset{x}{}{\swarrow}
        \overset{U}{}{\searrow}
      \underset{X}{}{\swarrow}\overset{V}{}{\searrow}\underset{y}{}\}
         \longrightarrow
      \{\underset{x}{}{\swarrow}\overset{\boxed{U=X=V}}{}{\searrow}
       \underset{y}{}\}
   $$
Indeed, the disjoint closed subsets are the preimges of the closed points 
$x$ and $y$ under the bottom horizontl arrow, and 
their separating neighbourhoods are the preimages of
open subsets $\big\{\underset{x}{}{\swarrow}
        \overset{U}{}\big\}$
and $\big\{\overset{V}{}{\searrow}\underset{y}{}\big\}$.

   In fact, by [[Urysohn's lemma]] a space is normal if and only if any two disjoint closed sets can be separated by a continuous function, i.e.

   $$
      \emptyset \longrightarrow  {X}
      \;\;\;\,&solb;\,\;\;\;
       [0,1]\vee_{\{0,1\}} \{0'\leftrightarrow 0, 1\leftrightarrow 1'\}
      \longrightarrow  \{0=0'{\searrow}e_{[0,1]}{\swarrow}1=1'\}
   $$
Here in $[0,1]\vee_{\{0,1\}} \{0'\leftrightarrow 0, 1\leftrightarrow 1'\}$
   the points $0',0$ and $1,1'$ are topologically indistinguishable, $[0,1]$ goes to $e_{[0,1]}$, and both $0,0'$ map to point $0=0'$,  and both $1,1'$ map to point $1=1'$.


### Normal Hausdorff spaces ($T_4$)

$X$ is normal Hausdorff, or T4, if it is both T1 and normal. Every normal
Hausdorff space is both Tychonoff and normal regular.



### Completely normal spaces

$X$ is _completely or heriditarily normal_ if any two separated sets $A$ and $B$ are separated by neighbourhoods $U\supset A$ and $V\supset B$ such that $U$ and $V$ do not intersect, i.e.
   $$
     \emptyset \longrightarrow  {X}
     \;\;\;\,&solb;\,\;\;\;
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



### Perfectly normal spaces


$X$ is [[perfectly normal topological space|perfectly normal]] if any two disjoint closed sets are precisely separated by a continuous function, i.e.

   $$
    \emptyset\longrightarrow {X}
      \;\;\;\,&solb;\,\;\;\;
    [0,1]\longrightarrow \{0{\swarrow}X{\searrow}1\}
   $$

   where $(0,1)$ goes to the open point $X$, and $0$ goes to $0$, and $1$ goes to $1$.

   Every perfectly normal space is also completely normal.




## Applications.

The following notation and terminology helps to discuss applications. 

### Quillen negation 

For a class $P$ of morphisms in a category, its _left Quillen negation_ $P^{&solb; l}$ with respect to the lifting property, respectively its _right Quillen negation_ $P^{&solb; r}$, 
is the class of all morphisms which have the left, respectively right, lifting property with respect to each morphism in the class $P$. In notation,
$$
P^{&solb; l} := \{ i \,\,:\,\, \forall p\in P\,\, i\;\;\;\,&solb;\,\;\;\; p\},
P^{&solb;r} := \{ p \,\,:\,\, \forall i\in P\,\, i\;\;\;\,&solb;\,\;\;\; p\}, P^\lr:=(P^\lrl)^\rlr,..$$

As the terminology might suggest, 
taking the Quillen negation of a class/property $P$ is a simple way to define a class of morphisms excluding non-isomorphisms 
from $P$, in a way which is useful in a diagram chasing computation, and is often used to
define properties of morphisms starting from an explicitly given class of (counter)examples. 
A number of elementary notions may also be expressed using the lifting property starting from a list of (counter)examples. 



### Urysohn lemma and Tietze extension theorem. 

We now explain how to view the standard proof of the [[Urysohn lemma]] in terms of lifting properties.

Let $\Lambda_n=\big\{
\underset{c_0}{} \swarrow 
\overset{o_1}{} \searrow \cdots \swarrow 
\overset{o_n}{} \searrow 
\underset{c_n}{} \big\} $ for $n\geq 1$. Pick a sequence of  "subdivision" maps, e.g. 
$$\Lambda_{2({n+1})}\to \Lambda_{2n}$$
$$c_{2i}\mapsto c_i,\,\,\, o_{2i+1},c_{2i+1},o_{2i+2}\mapsto o_i,\,\,\, 0\leq i\leq n-1,\,\,\,c_{2n}\mapsto c_n,$$ 
and let $\Lambda_\infty=\lim_{n\to\infty} \Lambda_{2^n},$ be the limit in the category of topological spaces.

In this notation normality (T4) is defined by $\varnothing \to X \;\;\;\,&solb;\,\;\;\; \Lambda_2\to \Lambda_1$.
Iterating the lifting property shows that $f \;\;\;\,&solb;\,\;\;\; \Lambda_2\to \Lambda_1$ implies
that $f \;\;\;\,&solb;\,\;\;\; \Lambda_{2n}\to \Lambda_n$ and, passing to the limit, 
$f \;\;\;\,&solb;\,\;\;\; \Lambda_\infty\to \Lambda_1$. 

Iterating the lifting property $T_4$ implies that 
$$\Lambda_\infty\to  \Lambda_1 \in \{ \Lambda_2 \to \Lambda_1\}^{lr}.$$

The standard arguments from the proof of Urysohn lemma give the following
relation between $\Lambda_\infty$ and $\mathbf{R}$. 

1. $[0,1]$  and  ${[0,1]}\vee_{\{0,1\}} \{e_F\leftrightarrow 0, 1\leftrightarrow e_G\}$ are retracts of $\Lambda_\infty$. 



2. The map $\Lambda_\infty\to \Lambda_1$ factors as 
$$\Lambda_\infty\to   {[0,1]}\vee_{\{0,1\}} \{e_F\leftrightarrow 0, 1\leftrightarrow e_G\}\to \Lambda_2 \to \Lambda_1$$

Item (1) implies that 
$A \to X \;\;\;\,&solb;\,\;\;\; \Lambda_\infty\to \{o\}$ implies $A \to X \;\;\;\,&solb;\,\;\;\; [0,1]\to \{o\}$ 
(and  $A \to X \;\;\;\,&solb;\,\;\;\; [0,1]\vee_{\{0,1\}} \{e_F\leftrightarrow 0, 1\leftrightarrow e_G\}\to \{o\}$).

This reminds one of the [[Tietze extension theorem]] but is different: [it is not true that any closed inclusion
in a normal space lifts wrt to $\Lambda_2 \to \Lambda_1$](https://mathoverflow.net/questions/394187/extending-disjoint-open-subsets-of-a-normal-hausdorff-space/394193), although it is true for closed inclusions
into a heriditarily normal space.


\begin{tikzcd}
[
  column sep={between origins, 120pt},
  row sep={between origins, 40pt}
]
  A
  \ar[dd]
  \ar[rr]
  &[-60pt]
  & \Lambda_\infty \ar[rdd]\ar[dd]
  & { {[0,1]}\vee_{\{0,1\}} \{e_F\leftrightarrow 0, 1\leftrightarrow e_G\} }\ar[l]\ar[dd] \ar[r] 
  &  \Lambda_2 
  \ar[
    ddll,
    crossing over
  ]
  \\
  \\
  B
  \ar[
    rr
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&\Lambda_1 
  & { {[0,1]}\vee_{\{0,1\}} \{e_F\leftrightarrow 0, 1\leftrightarrow e_G\} }\ar[l] 
\end{tikzcd}


Item (2) (see the diagram above) shows that  $A\to B \;\;\;\,&solb;\,\;\;\; \Lambda_\infty\to \Lambda_1$ implies that 
$A\to B \;\;\;\,&solb;\,\;\;\; {[0,1]}\vee_{\{0,1\}} \{e_F\leftrightarrow 0, 1\leftrightarrow e_G\}\to \Lambda_1$.
Finally, for $A=\varnothing$ the latter implies that $\varnothing \to B \;\;\;\,&solb;\,\;\;\;   \Lambda_2 \to \Lambda_1$.
This implies the Urysohn lemma that 
$$\varnothing \to B \;\;\;\,&solb;\,\;\;\;   \Lambda_2 \to \Lambda_1\text{ iff }\varnothing \to B \;\;\;\,&solb;\,\;\;\;   {[0,1]}\vee_{\{0,1\}} \{e_F\leftrightarrow 0, 1\leftrightarrow e_G\} \to \Lambda_1$$

The following theorem is a summary of considerations above. 
\begin{theorem}

1. $ \{\Lambda_2\to \Lambda_1\} ^{&solb; l} \subset  \{\Lambda_\infty\to \Lambda_1\}^{&solb; l} \subset   \{{[0,1]}\vee_{\{0,1\}} \{e_F\leftrightarrow 0, 1\leftrightarrow e_G\} \to \Lambda_1\}^{&solb; l}  $

2. $ \{\Lambda_2\to \Lambda_1\} ^{&solb; l}  \subset  \{\Lambda_\infty\to \{o\}\}^{&solb; l} \subset   \{{[0,1]} \to \{o\}\}^{&solb; l} $

3. for arbitrary space $B$ it holds  
$$\varnothing \to B \;\;\;\,&solb;\,\;\;\;   \Lambda_2 \to \Lambda_1\,\,\,\text{ iff }\,\,\,\varnothing \to B \;\;\;\,&solb;\,\;\;\;   {[0,1]}\vee_{\{0,1\}} \{e_F\leftrightarrow 0, 1\leftrightarrow e_G\} \to \Lambda_1$$

\end{theorem}

A noted above, item (3) is the usual statement of Urysohn lemma, and item (2) is similar but not equivalent to the Tietze extension theorem. 




### Extremally disconnected spaces being projective
The morphism {#DiscussionOfLiftingForExtremallyDisconnected}
$f_{e.d.}:= \boxed{
\boxed{{}^{\boxed{u}}\!\! \searrow_{\,c_1}} \,\,\, \boxed{{}_{c_2}\swarrow^{\boxed{v}}}
}
\to
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
$
is surjective, proper, and has the right lifting property $T_1$. 

Both being surjective and [being proper](Tychonoff+theorem#ProofViaTaimanovTheoremAndLiftingProperties) are the right lifting properties. 
This means that each morphism  $S\xrightarrow { (f_{e.d.})^{lr} } X$ is surjective and proper, 
and if $X$ has $T_1$, so does $S$. In particular, if $X$ is compact Hausdorff, so is $S$. 

Each morphism $\varnothing \to X$ can be decomposed as 
$$
\varnothing \xrightarrow{ (f_{e.d.})^l } S \xrightarrow { (f_{e.d.})^{lr} } X
$$

This means there is a surjective proper map onto each space from an extremally disconnected space,
and that in this both spaces can be assumed compact Hausdorff. 
The Gleason theorem that extremally disconnected spaces are projective in the category 
of topological spaces and proper maps, can be expressed by saying that 
$\varnothing \to  S \in (proper)^{l}$ whenever $\varnothing \xrightarrow{ (f_{e.d.})^l } S$.

In fact there is a proper morphism $f_{proper}$ of finite spaces such that 
for compact Hausdorff spaces it holds
$S \xrightarrow { (f_{proper})^{lr} } X$, i.e. $(f_{proper})^{lr} $ 
is a class of proper maps containing (necessarily proper) maps of compact Hausdorff spaces. 











## Related concepts

* [Tychonoff theorem -- Proof via lifting properties](Tychonoff+theorem#ProofViaTaimanovTheoremAndLiftingProperties)

## References

* {#Gavrolovich14} [[Misha Gavrilovich]], *Point set topology as diagram chasing computations*,  The De Morgan Gazette. 2014. Vol. 5. No. 4. P. 23-32.  ([arXiv:1408.6710](https://arxiv.org/abs/1408.6710), [pdf](http://mishap.sdf.org/mints-lifting-property-as-negation-DMG_5_no_4_2014.pdf))

* [[Misha Gavrilovich]], *The unreasonable power of the lifting property in elementary mathematics*, 2017 ([arXiv:1707.06615](https://arxiv.org/abs/1707.06615),  [pdf](http://mishap.sdf.org/by:gavrilovich/expressive_power_of_the_lifting_property.pdf))

* [[Misha Gavrilovich]], Konstantin Pimenov. *A naive diagram chasing approach to formalisation of tame topology.*, 2018 ([pdf](http://mishap.sdf.org/mintsGE.pdf))

* [[Misha Gavrilovich]], *Extremally disconnected spaces as $\{\{u\to a,b\leftarrow v\}\to\{u\to a=b\leftarrow v\}\}^{lr}$, and being proper as $(\{\{o\}\to\{o\to c\}\}^r_{\le 4})^{lr}$*, 2021 ([pdf](http://mishap.sdf.org/yetanothernotanobfuscatedsyntax.pdf))
