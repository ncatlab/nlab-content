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

In [[topology]], some of the [[separation axioms]] that may be considered on [[topological spaces]] may equivalently be reformulated in terms of [[lifting properties]] ([Gavrilovich 2014](#\rightthreetimes)). 

To see this, first notice/recall  the following two simple examples of [[lifting properties]] in [[diagrams]] in [[TopSp]].

The property

* *$X \xrightarrow{f} Y$ is a [[surjective function]]*.

means equivalently that $f$ has the [[right lifting property]]
against the unique map from the [[empty space]] to the [[point space]]:

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

to the [[point space]]:

\begin{tikzcd}
[
  column sep={between origins, 40pt}, 
  row sep={between origins, 40pt}
]
  \mathrm{Dsc}
  \big( 
    \{0,1\} 
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
    \{0,1\} 
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

Namely, now [[continuous function|continuity]] restricts the top map to be such that neither $x_i \in\; X$ is contained in an [[open subset]] that does not contain the other: For if it were, then the [[pre-image]] of that open subset would be $\{x_i\} \,\subset\, CoDsc\big( \{0,1\} \big)$, which however is *not* open (eq:OpenSubsetsOfTheCodiscreteSpaceOnTwoElements). This means that if $X_1$ is a [[T0-space|$T_0$-space]] then any such top map must be the [[constant function]], and this is equivalent to the existence of a lift in the diagram.

\linebreak


Proceeding in this manner, one sees that the property

* *$X$ is a [[T1-space|$T_1$-space]].

means equivalently that its unique map $X \to \ast$ to the [[point space]] has the [[right lifting property]]
against the unique map from the [[Sierpinski space]] $Sierp$ 

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
  \mathrm{Sierp}
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




## Background and notation


A [[topological space]] comes with a _[[specialisation preorder]]_ on its points: for
points $x,y \in X$,  $x \leq y$ iff $y \in cl x$ ($y$ is in the [[topological closure]] of $x$), or equivalently. The resulting [[preordered set]] may be regarded as a [[category]] whose
[[objects]] are the points of ${X}$ and where there is a unique [[morphism]] $x{\searrow}y$ iff $y \in cl x$.

For a [[finite topological space]] $X$, the [[specialisation preorder]] or equivalently the corresponding category uniquely determines the space: a [[subset]] of ${X}$ is [[closed subset|closed]] iff it is
[[downward closed subset|downward closed]], or equivalently, there are no morphisms going outside the subset.


The monotone maps (i.e. [[functors]]) are the [[continuous maps]] for this topology.

We denote a [[finite topological space]] by a list of the arrows (morphisms) in the corresponding [[specialization preorder]]; 

* '$\leftrightarrow $' denotes an [[isomorphism]] 

* '$=$' denotes the [[identity morphism]].  

An arrow between two such lists denotes a [[functor]] between these [[preorders]] (corresponding to a [[continuous map]] between the corresponding [[finite topological spaces]]) which sends each point to the correspondingly labelled point, but possibly turning some morphisms into identity morphisms, thus gluing some points. 

With this notation, we may display continuous functions for instance between the [[discrete space]] on two points, the [[Sierpinski space]], the [[antidiscrete space]] and the [[point space]] as follows (where each point is understood to be mapped to the point of the same name in the next space):

$$
  \array{
  \{a,b\}
     &\longrightarrow& 
  \{a{\searrow}b\}
     &\longrightarrow& 
  \{a\leftrightarrow b\}
    &\longrightarrow& 
  \{a=b\}
  \\
  \text{(discrete space)}
     &\longrightarrow& 
  \text{(Sierpinski space)}
    &\longrightarrow& 
  \text{(antidiscrete space)}
    &\longrightarrow& 
  \text{(single point)}
  }
$$

Here, in $\{a{\searrow}b\}$ the point $a$ is [[open point|open]] and point ${b}$ is [[closed point|closed]].


In $A \longrightarrow  B$, each object and each morphism in $A$ necessarily appears in {B} as well; we avoid listing 
the same object or morphism twice. Thus 
both 
$$
\{a\} \longrightarrow  \{a,b\}
  \phantom{AAA} \text{ and } \phantom{AAA} 
\{a\} \longrightarrow  \{b\}
$$ 
denote the same map from a single point to the [[discrete space]] with two points.



{#ExampleMapIdentifyingThreePoints} Similarly, both

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
       && U  &=& x &=& V
       \\
       & \swarrow & && && & \searrow
       \\
       a & & &&  &&  &&   b
     }
    \;\;
  \right\}
$$

and

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
       U  &=& x &=& V
     }
    \;\;
  \right\}
$$

denote the morphism gluing points $U$, $x$, and $V$.




## Separation conditions in terms of arrows


Fix two [[subsets]] $F, G \;\subset\; S$.

*  The sets $F$ and $G$ are __[[disjoint sets|disjoint]]__ if their [[intersection]] is [[empty set|empty]]:

   $$ 
     F \cap G = \empty 
     \,.
   $$
 
   In terms of arrows,  the following map is well-defined: 

   $$ 
     \array{
       S_{F,G}
       &\colon&
       S 
       &\longrightarrow&  
       \big\{
          F \leftrightarrow G \leftrightarrow \bullet 
       \big\}
     }
   $$ 

   such that

   $$
     S_{F,G}(x)
     \;=\;
     \left\{
     \array{
       F &\vert& x \in F
       \\
       G &\vert& x \in G
       \\   
       \bullet &\vert& otherwise 
     }
     \right.
   $$

*  They are __topologically disjoint__ if there exists a [[neighbourhood]] of one set that is disjoint from the other set:  

   $$ 
     (\exists\; U \stackrel{\circ}\supseteq F,\; U \cap G = \empty) 
     \;\vee\; 
     (\exists\; V \stackrel{\circ}\supseteq G,\; F \cap V = \empty) 
     \,.
   $$

   In terms of arrows,   $S_{F,G}: S \longrightarrow  \{F\leftrightarrow \bullet \leftrightarrow G \}$ factors either as 

   $$ S_{F,G}: S \longrightarrow   \{F \leftrightarrow U  \searrow \bullet \leftrightarrow G\} \longrightarrow  \{F\leftrightarrow  U =\bullet \leftrightarrow G \}$$ 

   or 

   $$ 
     S_{F,G}
      \colon 
     S \longrightarrow  \{F \leftrightarrow \bullet \swarrow V  \leftrightarrow G \} 
       \longrightarrow
     \{F \leftrightarrow \bullet = V  \leftrightarrow G \}   
   $$ 

   where $U$, $V$ maps to $\bullet$.
   Notice that topologically disjoint sets must be disjoint.

*  They are __separated__ if each set has a neighbourhood that is disjoint from the other set:
 
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

*  {#SeparatedByNeighbourhoods} They are __separated by neighbourhoods__ if they have disjoint neighbourhoods:
   $$ \exists\; U \stackrel{\circ}\supseteq F,\; \exists\; V \stackrel{\circ}\supseteq G,\; U \cap V = \empty .$$
   The arrow  $S_{F,G}: S \longrightarrow  \{F\leftrightarrow \bullet \leftrightarrow G \}$ factors as 
   $S \longrightarrow \{F \leftrightarrow  U  \searrow \bullet \swarrow  V \leftrightarrow G\}\longrightarrow \{F \leftrightarrow  U  = \bullet =  V \leftrightarrow G\}$
   Notice that sets separated by neighbourhoods must be separated.
*  They are __separated by closed neighbourhoods__ if they have disjoint closed neighbourhoods:
   $$ \exists\; U \stackrel{\circ}\supseteq F,\; \exists\; V \stackrel{\circ}\supseteq G,\; Cl(U) \cap Cl(V) = \empty .$$
   The arrow  $S_{F,G}: S \longrightarrow  \{F\leftrightarrow \bullet \leftrightarrow G \}$ factors as
   $$ S \longrightarrow \{ F \leftrightarrow U \searrow U' \swarrow \bullet \searrow V' \searrow V \leftrightarrow G \}
   \longrightarrow \{ F \leftrightarrow U = U' = \bullet = V' = V \leftrightarrow G \} $$
   Notice that sets separated by closed neighbourhoods must be separated by neighbourhoods.
*  They are __separated by a function__ if there exists a continuous [[real number|real]]-valued [[function]] on the space that maps $F$ to $0$ and $G$ to $1$:
   $$ \exists\; f: S \to \mathbf{R},\; F \subseteq f^*(\{0\}) \;\wedge\; G \subseteq f^*(\{1\}) .$$
    The arrow  $S_{F,G}: S \longrightarrow  \{F\leftrightarrow \bullet \leftrightarrow G \}$ factors as    
    $$ S \longrightarrow   \{0'\} \cup [0,1] \cup \{1'\}  \longrightarrow  \{ 0'=F \leftrightarrow \bullet \leftrightarrow  1'=G\}
  $$
  where points $0',0$ and $1,1'$ are topologically indistinguishable,
  and $0'$ maps to $F$, and $1'$ maps to $G$, and $[0,1]$ maps to $\bullet$.
  Notice that sets separated by a function must be separated by closed neighbourhoods (the preimages of $[-\epsilon, \epsilon]$ and $[1-\epsilon, 1+\epsilon]$).
*  Finally, they are __precisely separated by a function__ if there exists a continuous real-valued function on the space that maps precisely $F$ to $0$ and $G$ to $1$:
   $$ \exists\; f: S \to \mathbf{R},\; F = f^*(\{0\}) \;\wedge\; G = f^*(\{1\}) .$$
    The arrow  $S_{F,G}: S \longrightarrow  \{F\leftrightarrow \bullet \leftrightarrow G \}$ factors as    
    $$ S \longrightarrow   [0,1]  \longrightarrow  \{ 0=F \leftrightarrow \bullet\leftrightarrow  1=G\}
  $$
  where
  $0'$ maps to $F$, and $1'$ maps to $G$, and $(0,1)$ maps to $\bullet$.
  Notice that sets separated by a function must be separated by closed neighbourhoods (the preimages of $[-\epsilon, \epsilon]$ and $[1-\epsilon, 1+\epsilon]$).
   Notice that sets precisely separated by a function must be separated by a function.

Often $F$ and $G$ will be points (identified with their [[singleton]] subsets); in that case, one usually says _distinct_ in place of _disjoint_.

Often $F$ or $G$ will be closed sets; notice that disjoint closed sets are automatically separated, while a closed set and a point, if disjoint, are automatically topologically disjoint.



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

*  $X$ is $T2\frac{1}{2}$, or Urysohn, if any two distinct points in $X$ are separated by closed neighbourhoods, i.e.

   $$
    \{x,y\} \hookrightarrow  {X} 
    \;\;\;\,\rightthreetimes\,\;\;\;
     \{x{\searrow}x'{\swarrow}X{\searrow}y'{\swarrow}y\} 
    \longrightarrow  \{x=x'=X=y'=y\}
   $$

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
      \{x{\searrow}X{\swarrow}U{\searrow}F\} 
        \longrightarrow  
      \{x=X=U{\searrow}F\}
   $$

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
      \{x{\swarrow}x'{\searrow}X{\swarrow}y'{\searrow}y\} 
      \longrightarrow  \{x{\swarrow}x'=X=y'{\searrow}y\}
   $$

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

*  $X$ is completely normal if any two separated sets $A$ and $B$ are separated by neighbourhoods $U\supset A$ and $V\supset B$ such that $U$ and $V$ do not intersect, i.e.

   $$
     \emptyset \longrightarrow  {X} 
     \;\;\;\,\rightthreetimes\,\;\;\;  
     \{X{\swarrow}A\leftrightarrow 
     U{\searrow}U'{\swarrow}W{\searrow}V'{\swarrow} 
     V\leftrightarrow B{\searrow}X\} \longrightarrow  \{U=U',V'=V\}
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
  \{x \swarrow x_1 \searrow \cdots \swarrow x_n \searrow y \} 
  \longrightarrow  
  \{x \swarrow x_1 = \cdots = x_n \searrow y \}
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
