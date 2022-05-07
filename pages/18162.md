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

In [[topology]], some of the [[separation axioms]] that may be considered on [[topological spaces]] may equivalently be reformulated in terms of [[lifting properties]] ([Gavrilovich 2014](#\rightthreetimes)). 


## Background and notation


A [[topological space]] comes with a _[[specialisation preorder]]_ on its points: for
points $x,y \in X$,  $x \leq y$ iff $y \in cl x$ ($y$ is in the [[topological closure]] of $x$), or equivalently. The resulting [[preordered set]] may be regarded as a [[category]] whose
[[objects]] are the points of ${X}$ and where there is a unique [[morphism]] $x{\searrow}y$ iff $y \in cl x$.

For a [[finite topological space]] $X$, the specialisation preorder or equivalently the corresponding category uniquely determines the space: a [[subset]] of ${X}$ is [[closed subset|closed]] iff it is
[[downward closed subset|downward closed]], or equivalently, there are no morphisms going outside the subset.


The monotone maps (i.e. [[functors]]) are the [[continuous maps]] for this topology.

We denote a finite topological space by a list of the arrows (morphisms) in
the corresponding category; '$\leftrightarrow $' denotes an [[isomorphism]] and '$=$' denotes the [[identity morphism]].  An arrow between two such lists denotes a [[continuous map]] (a functor) which sends each point to the correspondingly labelled point, but possibly turning some morphisms into identity morphisms, thus gluing some points. 

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

In $A \longrightarrow  B$, each object and each morphism in $A$ necessarily appears in {B} as well; we avoid listing 
the same object or morphism twice. Thus 
both 
$$
\{a\} \longrightarrow  \{a,b\}
  \phantom{AAA} \text{ and } \phantom{AAA} 
\{a\} \longrightarrow  \{b\}
$$ 
denote the same map from a single point to the discrete space with two points.
Both
 $$\{a{\swarrow}U{\searrow}x{\swarrow}V{\searrow}b\}\longrightarrow \{a{\swarrow}U=x=V{\searrow}b\}\text{ and }\{a{\swarrow}U{\searrow}x{\swarrow}V{\searrow}b\}\longrightarrow \{U=x=V\}$$
denote the morphism gluing points $U,x,V$.

In $\{a{\searrow}b\}$, the point $a$ is open and point ${b}$ is closed.



## Separation conditions in terms of arrows


Fix two sets ([[subsets]]) $F$ and $G$ of $S$.

*  The sets $F$ and $G$ are __[[disjoint sets|disjoint]]__ if their [[intersection]] is [[empty set|empty]]:

   $$ 
     F \cap G = \empty 
     \,.
   $$
 
  In terms of arrows,  the following map is well-defined: $S_{F,G}: S \longrightarrow  \{F\leftrightarrow G \leftrightarrow \bullet \}$ such that $S_{F,G}(x)=F$ for $x \in F$, $S_{F,G}(x)=G$ for $x \in G$, and $S_{F,G}(x)=\bullet$ for $x \notin F\cup G$.

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

In all of the following definitions, ${X}$ is  a topological space.


*  $ {X}$  is T0, or Kolmogorov, if any two distinct points in ${X}$ are topologically
distinguishable. (It will be a common theme among the separation axioms to have
one version of an axiom that requires T0 and one version that doesn't.)
As a formula, this is expressed as
   $$ \{x\leftrightarrow y\} \longrightarrow  \{x=y\} \,\rightthreetimes\,  {X} \longrightarrow  \{*\}$$

*    ${X}$ is R0, or symmetric, if any two topologically distinguishable points in $X$
are separated, i.e.
   $$ \{x{\searrow}y\} \longrightarrow  \{x\leftrightarrow y\} \,\rightthreetimes\,  {X} \longrightarrow  \{*\} $$

*  $X$ is T1, or accessible or Frechet, if any two distinct points in $X$ are
separated, i.e.
$$     \{x{\searrow}y\} \longrightarrow  \{x=y\} \,\rightthreetimes\,  {X} \longrightarrow  \{*\}  $$
 Thus, $X$ is T1 if and only if it is both T0 and R0. (Although you may
say such things as "T1 space", "Frechet topology", and "Suppose that the
topological space $X$ is Frechet", avoid saying "Frechet space" in this
context, since there is another entirely different notion of Frechet space in
functional analysis.)

*  $X$ is R1, or preregular, if any two topologically distinguishable points in
X are separated by neighbourhoods. Every R1 space is also R0.

*  $X$ is weak Hausdorff, if the image of every continuous map from a compact
Hausdorff space into $X$ is closed. All weak Hausdorff spaces are T1, and all
Hausdorff spaces are weak Hausdorff.

*  $X$ is Hausdorff, or T2 or separated, if any two distinct points in $X$ are
separated by neighbourhoods, i.e.
$$    \{x,y\} \hookrightarrow  {X} \,\rightthreetimes\,  \{x{\searrow}X{\swarrow}y\} \longrightarrow  \{x=X=y\} $$
Thus, $X$ is Hausdorff if and only if it is both T0
and R1. Every Hausdorff space is also T1.

*  $X$ is $T2\frac{1}{2}$, or Urysohn, if any two distinct points in $X$ are separated by
closed neighbourhoods, i.e.
$$
 \{x,y\} \hookrightarrow  {X} \,\rightthreetimes\,  \{x{\searrow}x'{\swarrow}X{\searrow}y'{\swarrow}y\} \longrightarrow  \{x=x'=X=y'=y\}
$$
Every $T2\frac{1}{2}$ space is also Hausdorff.

*  $X$ is completely Hausdorff, or completely T2, if any two distinct points in
X are separated by a continuous function, i.e. 
$$ \{x,y\} \hookrightarrow  {X} \,\rightthreetimes\,   [0,1]\longrightarrow \{*\}
$$
 where  $\{x,y\} \hookrightarrow  X$  runs through all injective maps from the discrete two
point space $\{x,y\}$.

Every completely Hausdorff space is
also $ T2\frac{1}{2} $.

*  $X$ is regular if, given any point ${x}$ and closed subset $F$ in $X$ such that ${x}$ does
not belong to $F$, they are separated by neighbourhoods, i.e.
$$    \{x\} \longrightarrow  {X} \,\rightthreetimes\,  \{x{\searrow}X{\swarrow}U{\searrow}F\} \longrightarrow  \{x=X=U{\searrow}F\}
$$
(In fact, in a regular
space, any such ${x}$ and ${F}$ will also be separated by closed neighbourhoods.) Every
regular space is also R1.

*  $X$ is regular Hausdorff, or T3, if it is both T0 and regular.[1] Every
regular Hausdorff space is also $T2\frac{1}{2}$.

*  $X$ is completely regular if, given any point ${x}$ and closed set $F$ in $X$ such
that ${x}$ does not belong to $F$, they are separated by a continuous function, i.e. 
$$
 \{x\} \longrightarrow  {X} \,\rightthreetimes\,  [0,1] \cup \{F\} \longrightarrow  \{x{\searrow}F\}
$$ 
where points $F$ and $1$ are topologically indistinguishable, $[0,1]$ goes to $x$, and $F$ goes to $F$.

Every
completely regular space is also regular.

*  $X$ is Tychonoff, or T3$\frac{1}{2}$, completely T3, or completely regular Hausdorff, if
it is both T0 and completely regular.[2] Every Tychonoff space is both regular
Hausdorff and completely Hausdorff.

*  $X$ is normal if any two disjoint closed subsets of $X$ are separated by
neighbourhoods, i.e.
$$   \emptyset \longrightarrow {X} \,\rightthreetimes\,  \{x{\swarrow}x'{\searrow}X{\swarrow}y'{\searrow}y\} \longrightarrow  \{x{\swarrow}x'=X=y'{\searrow}y\}
$$
 In fact, by Urysohn lemma a space is normal if and only if any two disjoint
closed sets can be separated by a continuous function, i.e.
 $$   \emptyset \longrightarrow  {X} \,\rightthreetimes\,  \{0'\} \cup [0,1] \cup \{1'\} \longrightarrow  \{0=0'{\searrow}x{\swarrow}1=1'\} $$
where points
$0',0$ and $1,1'$ are topologically indistinguishable,
            $[0,1]$ goes to $x$, and both $0,0'$ map to point $0=0'$,  and both $1,1'$ map to point
$1=1'$.



*  $X$ is normal Hausdorff, or T4, if it is both T1 and normal. Every normal
Hausdorff space is both Tychonoff and normal regular.

*  $X$ is completely normal if any two separated sets $A$ and $B$ are separated by
neighbourhoods $U\supset A$ and $V\supset B$
      such that $U$ and $V$ do not intersect, i.e.
 $$\emptyset \longrightarrow  {X} \,\rightthreetimes\,  \{X{\swarrow}A\leftrightarrow U{\searrow}U'{\swarrow}W{\searrow}V'{\swarrow}V\leftrightarrow B{\searrow}X\} \longrightarrow  \{U=U',V'=V\}$$
      Every completely normal space is also normal.


*  $X$ is perfectly normal if any two disjoint closed sets are precisely
separated by a continuous function, i.e. 
$$
 \emptyset\longrightarrow {X} \,\rightthreetimes\,  [0,1]\longrightarrow \{0{\swarrow}X{\searrow}1\}
$$   
where $(0,1)$ goes to the open point $X$, and $0$ goes to $0$, and $1$ goes to $1$.

Every perfectly normal space is also
completely normal.

+--
#### Remark. 
Note that a standard proof of Uryhson lemma may be represented as follows: iterate the lifting property to prove 
$$ \emptyset \longrightarrow X\rightthreetimes \{x \swarrow x_1 \searrow ... \swarrow x_n \searrow y \} \longrightarrow  \{x \swarrow x_1 = ... = x_n \searrow y \}$$
 Then pass to the infinite limit to construct a map 
$ X \longrightarrow  \mathbb{R}$.
=--

## Merge or discard




### $T_4$/Normality

The [[Tietze extension theorem]] applies to [[normal spaces]].

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

## Related concepts

* [Tychonoff theorem -- Proof via lifting properties](Tychonoff+theorem#ProofViaTaimanovTheoremAndLiftingProperties)

## References

* [[Misha Gavrilovich]], _The unreasonable power of the lifting property in
elementary mathematics_ ([pdf](http://mishap.sdf.org/by:gavrilovich/expressive_power_of_the_lifting_property.pdf))

* {#Gavrolovich14} [[Misha Gavrilovich]], *Point set topology as diagram chasing computations* ([arXiv:1408.6710](https://arxiv.org/abs/1408.6710), [pdf](http://mishap.sdf.org/mints-lifting-property-as-negation-DMG_5_no_4_2014.pdf))


