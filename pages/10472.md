
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _pointed topological space_ (often _[[pointed space]]_, for short) is a [[topological space]] equipped with a choice of one of its [[points]] ([[elements]]).

Although  this concept may seem simple, pointed topological spaces play a central role for instance in [[algebraic topology]] as domains for  [[reduced cohomology|reduced]] [[generalized (Eilenberg-Steenrod) cohomology theories]] and as an ingredient for the definition of [[spectra]].

One reason why pointed topological spaces are important is that the [[category]] which they form is an intermediate stage in the [[stabilization]] of [[homotopy theory]] (the [[classical model structure on topological spaces|classical homotopy theory of topological spaces]]) to [[stable homotopy theory]]:

The category of pointed topological spaces has a [[zero object]] (the [[point space]] itself) and the canonical [[tensor product]] on pointed spaces is the _[[smash product]]_, which is non-[[cartesian monoidal category]], in contrast to the plain [[product space|product of topological space]].

## Definition

A _pointed topological space_ is a [[topological space]] $(X,\tau)$ equipped with a choice of point $x \in X$.
A [[homomorphism]] between pointed topological space $(X,x)$ $(Y,y)$ is a [[continuous function]] $f \colon X \to Y$ which preserves the chosen basepoints in that $f(x) = y$.

### The category of pointed topological spaces

Stated in the language of [[category theory]], this means that pointed topological spaces are the _[[pointed objects]]_ in the [[category]] [[Top]] of topological spaces. This is the [[coslice category]] $Top^{\ast/}$ of topological spaces "under" the [[point space]] $\ast$:

an [[object]] in $Top^{\ast/}$ is equivalently a [[continuous function]] $x \colon \ast  \to (X,\tau)$, which is equivalently just a choice of point in $X$, and a [[morphism]] in $Top^{\ast/}$ is a morphism $f \colon X \to Y$ in [[Top]] (hence a continuous function), such that this triangle [[diagram]] [[commuting diagram|commutes]]

$$
  \array{
    && \ast
    \\
    & {}^{\mathllap{x}}\swarrow && \searrow^{\mathrlap{y}}
    &&
    \\
    X && \underset{f}{\longrightarrow} && Y
  }
$$

which equivalently means that $f(x) = y$.

### Forgetting and adjoining basepoints
 {#ForgettingAndAdjoiningBasepoints}

+-- {: .num_defn #BasePointAdjoined}
###### Definition

The [[forgetful functor]] $Top^{\ast/} \to Top$ has a [[left adjoint]] given by forming the [[disjoint union space]] ([[coproduct]] in [[Top]]) with a [[point space]] ("adjoining a base point"), this is denoted by

$$
  (-)_+ \coloneqq (-) \sqcup \ast \;\colon \; Top \longrightarrow Top^{\ast/}
  \,.
$$

=--


### Wedge sum and Smash product

+-- {: .num_example #WedgeSumAsCoproduct}
###### Example

Given two pointed topological spaces $(X,x)$ and $(Y,y)$, then:

1. their [[Cartesian product]] in $Top^{\ast/}$ is simply their [[product topological space]] $X \times Y$ equipped with the [[pair]] of basepoints $(X\times Y, (x,y))$;

1. their [[coproduct]] in $Top^{\ast/}$ has to be computed using the second clause in [this prop.](pointed+object#LimitsAndColimitsOfPointedObjects): since the point $\ast$ has to be adjoined to the diagram, it is given not by the coproduct in $Top$ (which is the [[disjoint union space]]), but by the [[pushout]] in $Top$ of the form:

   $$
     \array{
       \ast &\overset{x}{\longrightarrow}& X
       \\
       {}^{\mathllap{y}}\downarrow &(po)& \downarrow
       \\
       Y &\longrightarrow& X \vee Y
     }
     \,.
   $$

   This is called the _[[wedge sum]]_ operation on pointed objects.

   This is the [[quotient topological space]] of the [[disjoint union space]] under the [[equivalence relation]] which identifies the two basepoints:

   $$
     X \vee Y \;\simeq\; (X \sqcup Y)/(x \sim y)
   $$ 

Generally for a set $\{(X_i,x_i)\}_{i \in I}$ of pointed topological spaces

1. their [[product]] is formed in [[Top]], as the [[product topological space]] with the [[Tychonoff topology]], with the [[tuple]] $(x_i)_{i \in I} \in \underset{i \in I}{\prod} X_i$ of basepoints being the new basepoint;

1. their [[coproduct]] is formed by the [[colimit]] in $Top$ over the [[diagram]] with a basepoint adjoined, and is called the [[wedge sum]] $\vee_{i \in I} X_i$, which is the [[quotient topological space]] of the [[disjoint union space]] with all the basepoints identified:

   $$
     \underset{i \in I}{\vee} X_i
     \;\simeq\;
     \left(\underset{i \in I}{\sqcup} X_i\right)/(x_i \sim x_j)_{i,j \in I}
    \,.
   $$

=--


+-- {: .num_example}
###### Example

For $X$ a [[CW-complex]],  then for every $n \in \mathbb{N}$ the [[quotient]] of its $n$-skeleton by its $(n-1)$-skeleton is the [[wedge sum]], def. \ref{WedgeSumAsCoproduct}, of $n$-spheres, one for each $n$-cell of $X$:

$$
  X^n / X^{n-1} \simeq \underset{i \in I_n}{\vee} S^n
  \,.
$$

=--


+-- {: .num_defn #SmashProductOfPointedObjects}
###### Definition

The _[[smash product]]_ of pointed topological spaces is the [[functor]]

$$
  (-)\wedge(-)
    \;\colon\;
  Top^{\ast/}
    \times 
  Top^{\ast/}
    \longrightarrow
  Top^{\ast/}
$$

given by

$$
  X \wedge Y
  \;\coloneqq\;
  \ast
  \underset{X\sqcup Y}{\sqcup} (X \times Y)
  \,,
$$

hence by the [[pushout]] in $Top$ of he frm

$$
  \array{
    X \sqcup Y &\overset{(id_X,y),(x,id_Y) }{\longrightarrow}& X \times Y
    \\
    \downarrow &(po)& \downarrow
    \\
    \ast &\longrightarrow& X \wedge Y
  }
  \,.
$$

In terms of the [[wedge sum]] from def. \ref{WedgeSumAsCoproduct}, this may be written concisely as the [[quotient space]] ([this def](quotient+space#QuotientBySubspace)) of the [[product topological space]] by the [[subspace]] constituted by the  [[wedge sum]]

$$
  X \wedge Y \simeq \frac{X\times Y}{X \vee Y}
  \,.
$$
 
=--
t
$\,$

| symbol | name | category theory |
|--------|------|-----------------|
| $X \times Y$ | [[product space]] | [[product]] in $Top^{\ast/}$ |
| $X \vee Y$ | [[wedge sum]] | [[coproduct]] in $Top^{\ast/}$ |
| $X \wedge Y = \frac{X \times Y}{X \vee Y}$ | [[smash product]] | [[tensor product]] in $Top^{\ast/}$ |

+-- {: .num_example #WedgeAndSmashOfBasePointAdjoinedTopologicalSpaces}
###### Example

For $X, Y \in Top$, with $X_+,Y_+ \in Top^{\ast/}$, def. \ref{BasePointAdjoined}, then

* $X_+ \vee Y_+ \simeq (X \sqcup Y)_+$;

* $X_+ \wedge Y_+ \simeq (X \times Y)_+$. 

=--

+-- {: .proof}
###### Proof

By example \ref{WedgeSumAsCoproduct}, $X_+ \vee Y_+$ is given by the colimit in $Top$ over the diagram

$$
  \array{
    && && \ast
    \\
    && & \swarrow && \searrow
    \\
    X &\,\,& \ast && && \ast &\,\,& Y
  }  
  \,.
$$

This is clearly $A \sqcup \ast \sqcup B$. Then, by definition \ref{SmashProductOfPointedObjects}

$$
  \begin{aligned}
    X_+ \wedge Y_+
    & \simeq
    \frac{(X \sqcup \ast) \times (X \sqcup \ast)}{(X\sqcup \ast) \vee (Y \sqcup \ast)}
    \\
    & \simeq 
    \frac{X \times Y \sqcup X \sqcup Y \sqcup \ast}{X \sqcup Y \sqcup \ast}
    \\
    & \simeq
    X \times Y \sqcup \ast
    \,.
  \end{aligned} 
$$

=--


+-- {: .num_example #StandardReducedCyclinderInTop}
###### Example

Let $I \coloneqq [0,1] \subset \mathbb{R}$ be the [[closed interval]] with its [[Euclidean space|Euclidean]] [[metric topology]].

Hence

$$
  I_+ \in Top^{\ast/}
$$

is the interval with a disjoint basepoint adjoined, def. \ref{BasePointAdjoined}. 

Now for $X$ any [[pointed topological space]], then the [[smash product]] (def. \ref{SmashProductOfPointedObjects})

$$
  X \wedge (I_+) = (X \times I)/(\{x_0\} \times I)
$$

is the **[[reduced cylinder]]** over $X$: the result of forming the ordinary [[cylinder]] over $X$, and then identifying the interval over the basepoint of $X$ with the point.

(Generally, any construction in $Top$ properly adapted to pointed spaces is called the "reduced" version of the unpointed construction. Notably so for "[[reduced suspension]]" which we come to [below](#MappingCones).)


Just like the ordinary cylinder $X\times I$ receives a canonical injection from the [[coproduct]] $X \sqcup X$ formed in $Top$, so the reduced cyclinder receives a canonical injection from the coproduct $X \sqcup X$ formed in $Top^{\ast/}$, which is the [[wedge sum]] from example \ref{WedgeSumAsCoproduct}:

$$
  X \vee X \longrightarrow X \wedge (I_+)
  \,.
$$

=--


### Mapping (co-)cones


Recall that the _[[cone]]_ on a [[topological space]] $X$ is the [[quotient space]] of the [[product space]] with the closed interval

$$
  Cone(X)
   = 
  (X \times [0,1])/( X \times \{0\} )
  \,.
$$

If $X$ is pointed with basepoint $x \in X$, then the  _reduced cone_ is the further quotient by the copy of the interval over the basepoint

$$
  Cone(X,x) = Cone(X) / ( \{x\} \times [0,1] )
  \,.
$$

For $f \colon X \to Y$ a [[continuous function]], then 

1. the _[[mapping cylinder]]_ of $f$ is the [[attachment space]]

   $$
     Cyl(f) \coloneqq Y \cup_f Cyl(X)
   $$

1. the _[[mapping cone]]_ of $f$ is the [[attachment space]]

   $$
     Cone(f) \coloneqq Y \cup_f Cone(X)
   $$

accordingly if $f \colon X \to Y$ is a continuous function between pointed spaces which preserves the basepoint, then the analogous construction with the [[reduced cylinder]] and the reduce cone, respectively, yield the _reduced mapping cyclinder_ and the _reduced mapping cone_. 

We now say this again in terms of [[pushouts]]:


+-- {: .num_defn #MappingConeAndMappingCocone}
###### Definition

For $f \colon X \longrightarrow Y$ a [[continuous function]] between pointed spces, its **reduced [[mapping cone]]** is the space

$$
  Cone(f)
    \coloneqq
  \ast \underset{X}{\sqcup} Cyl(X) \underset{X}{\sqcup} Y
$$

in the [[colimit|colimiting]] [[diagram]]

$$
  \array{
    && X &\stackrel{f}{\longrightarrow}& Y
    \\
    && \downarrow^{\mathrlap{i_1}} && \downarrow^{\mathrlap{i}}
    \\
    X &\stackrel{i_0}{\longrightarrow}& Cyl(X)
    \\
    \downarrow && & \searrow^{\mathrlap{\eta}} & \downarrow
    \\
    {*} &\longrightarrow& &\longrightarrow& Cone(f)
  }
  \,,
$$

where $Cyl(X)$ is the  [[reduced cylinder]] from def. \ref{StandardReducedCyclinderInTop}.

=--


+-- {: .num_prop #ConeAndMappingCylinder}
###### Proposition

The colimit appearing in the definition of the reduced [[mapping cone]] in def. \ref{MappingConeAndMappingCocone} is equivalent to three consecutive [[pushouts]]:

$$
  \array{
    && X &\stackrel{f}{\longrightarrow}& Y
    \\
    && \downarrow^{\mathrlap{i_1}} &(po)& \downarrow^{\mathrlap{i}}
    \\
    X &\stackrel{i_0}{\longrightarrow}& Cyl(X) &\longrightarrow& Cyl(f)
    \\
    \downarrow &(po)& \downarrow & (po) & \downarrow
    \\
    {*} &\longrightarrow& Cone(X) &\longrightarrow& Cone(f)
  }
  \,.
$$

The two intermediate objects appearing here are called

* the plain **reduced [[cone]]**  $Cone(X) \coloneqq \ast \underset{X}{\sqcup} Cyl(X)$;

* the **reduced [[mapping cylinder]]** $Cyl(f) \coloneqq Cyl(X) \underset{X}{\sqcup} Y$.

=--


+-- {: .num_defn #SuspensionAndLoopSpaceObject}
###### Definition

Let $X \in Top^{\ast/}$ be any pointed topological space.

The [[mapping cone]], def. \ref{ConeAndMappingCylinder}, of $X \to \ast$ is called the  **[[reduced suspension|reduced]] [[suspension]]** of $X$, denoted

   $$
     \Sigma X = Cone(X\to\ast)\,.
   $$

   Via prop. \ref{ConeAndMappingCylinder} this is equivalently the coproduct of two copies of the cone on $X$ over their base:

   $$
     \array{
       && X &\stackrel{}{\longrightarrow}& \ast
       \\
       && \downarrow^{\mathrlap{i_1}} &(po)& \downarrow^{\mathrlap{}}
       \\
       X &\stackrel{i_0}{\longrightarrow}& Cyl(X) &\longrightarrow& Cone(X)
       \\
       \downarrow &(po)& \downarrow & (po) & \downarrow
       \\
       {*} &\longrightarrow& Cone(X) &\longrightarrow& \Sigma X
     }
     \,.
   $$

   This is also equivalently the [[cofiber]]f of $(i_0,i_1)$, hence (example \ref{WedgeSumAsCoproduct}) of the [[wedge sum]] inclusion:

   $$
     X \vee X
      =
     X \sqcup X
      \overset{(i_0,i_1)}{\longrightarrow}
     Cyl(X)
       \overset{cofib(i_0,i_1)}{\longrightarrow}
     \Sigma X
     \,.
   $$


=--

+-- {: .num_prop #ReducedSuspensionBySmashProductWithCircle}
###### Proposition


The [[reduced suspension]] objects (def. \ref{SuspensionAndLoopSpaceObject}) induced from the standard [[reduced cylinder]] $(-)\wedge (I_+)$ of example \ref{StandardReducedCyclinderInTop} are isomorphic to the [[smash product]] (def. \ref{SmashProductOfPointedObjects}) with the [[circle] (the [[1-sphere]]) 

  $$
    cofib(X \vee X \to X \wedge (I_+)) \simeq S^1 \wedge X
    \,,
  $$

=--




+-- {: .num_prop #UnreducedMappingConeAsReducedConeOfBasedPointAdjoined}
###### Proposition

For $f \colon X \longrightarrow Y$ a morphism in [[Top]], then its unreduced mapping cone with respect to the standard cylinder object $X \times I$ def. \ref{TopologicalInterval}, is isomorphic to the reduced mapping cone, of the morphism $f_+ \colon X_+ \to Y_+$ (with a basepoint adjoined) with respect to the standard [[reduced cylinder]]:

$$
  Cone'(f) \simeq Cone(f_+)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By example \ref{WedgeAndSmashOfBasePointAdjoinedTopologicalSpaces}, $Cone(f_+)$ is given by the colimit in $Top$ over the following diagram:

$$
  \array{
    \ast &\longrightarrow& X \sqcup \ast &\overset{(f,id)}{\longrightarrow}& Y \sqcup \ast
    \\
    \downarrow && \downarrow && \downarrow
    \\
    X \sqcup\ast &\longrightarrow& (X \times I) \sqcup \ast
    \\
    \downarrow && && \downarrow
    \\
    \ast &\longrightarrow& &\longrightarrow& Cone(f_+)
  }
  \,.
$$

We may factor the vertical maps to give

$$
  \array{
    \ast &\longrightarrow& X \sqcup \ast &\overset{(f,id)}{\longrightarrow}& Y \sqcup \ast
    \\
    \downarrow && \downarrow && \downarrow
    \\
    X \sqcup\ast &\longrightarrow& (X \times I) \sqcup \ast
    \\
    \downarrow && && \downarrow
    \\
    \ast \sqcup \ast &\longrightarrow& &\longrightarrow& Cone'(f)_+
    \\
    \downarrow && && \downarrow
    \\
    \ast &\longrightarrow& &\longrightarrow& Cone'(f)
  }
  \,.
$$



This way the top part of the diagram (using the [[pasting law]] to compute the colimit in two stages) is manifestly a cocone under the result of applying $(-)_+$ to the diagram for the unreduced cone. Since $(-)_+$ is itself given by a colimit, it preserves colimits, and hence gives the partial colimit $Cone'(f)_+$ as shown. The remaining pushout then contracts the remaining copy of the point away.

=--



## Properties

### General

Most of the relevant constructions on pointed topological spaces are immediate specializations of the general construction discussed at _[[pointed object]]_. 

### Relation to one-point compactification

+-- {: .num_prop #OnePointCompactificationAndSmashProduct}
###### Proposition
**([[one-point compactification intertwines Cartesian product with smash product]])

On the [[subcategory]] $Top_{LCHaus}$ of [[Top]] on the [[locally compact Hausdorff spaces]] with [[proper maps]] between them, the [[functor]] of [[one-point compactification]] (Prop. \ref{OnePointCompactificationFunctor})

$$
  (-)^{cpt}
  \;\colon\;
  Top_{LCHaus}
  \longrightarrow 
  Top^{\ast/}
$$

sends [[Cartesian products]] ([[product topological spaces]]) to [[smash products]] of [[pointed topological spaces]], hence constitutes a [[strong monoidal functor]], in that there is a [[natural transformation|natural]] [[homeomorphism]]:

$$
  \big(
    X \times Y 
  \big)^{cpt}
  \;\simeq\;
  X^{cpt} \wedge Y^{cpt}
  \,.
$$

=--

This is briefly mentioned in, for instance, [Bredon 93, p. 199](#Bredon93).
The argument may be found spelled out in: [MO:a/1645794/](https://math.stackexchange.com/a/1645794/58526), [Cutler 20, Prop. 1.6](#Cutler20).





[[!include smash-monoidal diagonals -- section]]





## Related concepts

* [[pointed simplicial set]]

* [[loop space]], [[reduced suspension]]

* [[smash product]], [[wedge sum]]

* [[pointed homotopy type]]

* [[spectrum]]

* [[classical model structure on pointed topological spaces]]

## References

Textbook accounts:

* {#GabrielZisman67} [[Pierre Gabriel]], [[Michel Zisman]], Chapters IV.4 and V.7 of _[[Calculus of fractions and homotopy theory]]_, Ergebnisse der Mathematik und ihrer Grenzgebiete, Band 35, Springer (1967)  ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/GZ.pdf))


* {#Bredon93} [[Glen Bredon]], _Topology and Geometry_, Graduate Texts in Mathematics 139, Springer 1993 ([doi:10.1007/978-1-4757-6848-0](https://link.springer.com/book/10.1007/978-1-4757-6848-0), [pdf](http://virtualmath1.stanford.edu/~ralph/math215b/Bredon.pdf))

Review:

* {#Cutler20} Tyrone Cutler, _The category of pointed topological spaces_, 2020 ([pdf](https://www.math.uni-bielefeld.de/~tcutler/pdf/Elementary%20Homotopy%20Theory%20II%20-%20The%20Pointed%20Category.pdf), [[CutlerPointedTopologicalSpaces.pdf:file]])



[[!redirects pointed topological spaces]]

[[!redirects based topological space]]
[[!redirects based topological spaces]]