
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _classical model structure on topological spaces_ or _Quillen-Serre model structure_ $Top_{Quillen}$ ([Quillen 67, II.3](#Quillen67)) is a [[model category]] structure on the [[category]] [[Top]] of [[topological spaces]] (also on many [[convenient categories of topological spaces]]) which represents the standard [[homotopy theory]] of [[CW-complexes]], in that its [[homotopy category of a model category]] is the [[classical homotopy category]] on [[cell complexes]]/[[CW-complexes]].

Its [[weak equivalences]] are the [[weak homotopy equivalences]], its [[fibrations]] are the [[Serre fibrations]] and its [[cofibrations]] are the [[retracts]] of [[relative cell complexes]].

The [[singular simplicial complex]]/[[geometric realization]] [[nerve and realization|adjunction]] constitutes a [[Quillen equivalence]] between 
$Top_{Quillen}$ and $sSet_{Quillen}$, the [[classical model structure on simplicial sets]]. This is sometimes called part of the statement of the _[[homotopy hypothesis]]_ [for Kan complexes](homotopy+hypothesis#ForKanComplexes). In the language of [[(∞,1)-category theory]] this means that $Top_{Quillen}$ and $sSet_{Quillen}$ both are [[presentable (∞,1)-category|presentations]] of the [[(∞,1)-category]] [[∞Grpd]] of [[∞-groupoids]].

There are also other model structures on [[Top]] itself, see at _[[model structure on topological spaces]]_ for more. This entry here focuses on just the classical model structure on topological spaces.


## Background from algebraic topology

This section recalls basic relevant concepts from [[algebraic topology]] and highlights some basic facts that may serve to motivate the Quillen model structure.

### Homotopy

The fundamental concept of [[homotopy theory]] is that of _[[homotopy]]_. In the context of [[topological spaces]] this is about [[continuous function|contiunous]] deformations of [[continuous functions]] parameterized by the standard interval:

+-- {: .num_defn #TopologicalInterval}
###### Definition

Write 

$$
  I \coloneqq [0,1] \hookrightarrow \mathbb{R}
$$

for the standard topological [[interval]], a [[compact topological space|compact]] [[connected topological space|connected]] [[topological subspace]] of the [[real line]].

Equipped with the canonical inclusion of its two endpoints

$$
  \ast \sqcup \ast \stackrel{(\delta_0,\delta_1)}{\longrightarrow} I \stackrel{\exists !}{\longrightarrow} \ast
$$

this is the standard [[interval object]] in [[Top]].

For $X \in Top$, the [[product topological space]] $X\times I$
is called the standard _[[cylinder object]]_ over $X$.
The endpoint inclusions of the interval make it factor the [[codiagonal]] on $X$

$$
  \nabla_X 
    \;\colon\; 
  X \sqcup X
  \stackrel{((id,\delta_0),(id,\delta_1))}{\longrightarrow}
  X \times I
  \longrightarrow
  X
  \,.
$$

=--



+-- {: .num_defn #LeftHomotopy}
###### Definition

For $f,g\colon X \longrightarrow Y$ two [[continuous functions]] between [[topological spaces]] $X,Y$, then a **[[left homotopy]]** $f \Rightarrow_L g$ is a [[continuous function]]

$$
  \eta \;\colon\; X \times I \longrightarrow Y
$$

out of the [[product topological space]] of $X$ with the standard interval of def. \ref{TopologicalInterval}, such that this fits into a [[commuting diagram]] of the form

$$
  \array{
     X 
     \\
     {}^{\mathllap{(id,\delta_0)}}\downarrow & \searrow^{\mathrlap{f}}
     \\
     X \times I &\stackrel{\eta}{\longrightarrow}& Y
     \\
     {}^{\mathllap{(id,\delta_1)}}\uparrow & \nearrow_{\mathrlap{g}}
     \\
     && X
  }
  \,.
$$

=--

+-- {: .num_defn #HomotopyEquivalence}
###### Definition

A [[continuous function]] $f \;\colon\; X \longrightarrow Y$
is called a **[[homotopy equivalence]]** if there exists a 
continuous function $X \longleftarrow Y \;\colon\; g$
and [[left homotopies]], def. \ref{LeftHomotopy}

$$
  \eta_1 \;\colon\; f\circ g \Rightarrow_L id_Y
$$

and

$$
  \eta_2 \;\colon\; g\circ f \Rightarrow_L id_X
  \,.
$$

If here $\eta_2$ is constant along $I$, $f$ is is said to exhibit $X$ as a **[[deformation retract]]** of $Y$.

=--



Another key application of the concept of left homotopy is to the definition of [[homotopy groups]].

+-- {: .num_defn #HomotopyGroupsOftopologicalSpaces}
###### Definition

For $X$ a [[topological space]], then its set $\pi_0(X)$
of _[[connected components]]_, also called the **0-th homotopy set**, 
is the set of 
[[left homotopy]]-[[equivalence classes]] of points $\ast \to X$,
def.\ref{LeftHomotopy}. By [[composition]] this extends to a [[functor]]

$$
  \pi_0 \colon Top \longrightarrow Set
  \,.
$$

For $n \in \mathb{N}$, $n \geq 1$ and for $x \colon \ast \to X$
any point, then the $n$th **[[homotopy group]]** $\pi_n(X)$ of $X$ at $x$
is the [[group]] 

* whose underlying [[set]] is the set of [[left homotopy]]-[[equivalence classes]] of maps $I^n \longrightarrow X$ that take the [[boundary]] of $I^n$ to $x$ and where the left homotopies $\eta$ are constrained to be constant on the boundary;

* whose [[group]] product operation takes $[\alpha \colon I^n \to X]$ and $[\beta \colon I^n \to X]$ to $[\alpha \cdot \beta]$ with

$$
  \alpha \cdot \beta
  \;\colon\;
  I^n 
  \stackrel{\simeq}{\longrightarrow}
  I^n \underset{I^{n-1}}{\sqcup} I^n
  \stackrel{(\alpha,\beta)}{\longrightarrow}
  X
  \,,
$$

where the first morphism is any [[homeomorphism]] from the unit $n$-[[cube]] to the $n$-cube with one side twice the unit length (see also at _[[positive dimension spheres are H-cogroup objects]]_).

By [[composition]], this construction extends to a [[functor]] 

$$
  \pi_{\bullet \geq 1}
    \;\colon\; 
  Top^{\ast/}
   \longrightarrow 
  Grp^{\mathbb{N}_{\geq 1}}
$$

from [[pointed topological spaces]] to [[graded object|graded]] [[group]].

=--

+-- {: .num_defn #WeakHomotopyEquivalenceOfTopologicalSpaces}
###### Definition

A [[continuous function]] $f \colon X \longrightarrow Y$
is called  a **[[weak homotopy equivalence]]** if its image
under all the [[homotopy group]] functors of def. \ref{HomotopyGroupsOftopologicalSpaces}
is an [[isomorphism]], hence if 

$$
  \pi_0(f) \;\colon\; \pi_0(X) \stackrel{\simeq}{\longrightarrow} \pi_0(X)
$$

and for all $x \in X$ and all $n \geq 1$

$$
  \pi_n(f) \;\colon\; \pi_n(X,x) \stackrel{\simeq}{\longrightarrow} \pi_n(Y,f(y))
  \,.
$$


=--

+-- {: .num_example #TopologicalHomotopyEquivalencesAreWeakHomotopyEquivalences}
###### Example

Every [[homotopy equivalence]], def. \ref{HomotopyEquivalence}, is a weak homotopy equivalence, def. \ref{WeakHomotopyEquivalenceOfTopologicalSpaces}.

In particular a [[deformation retraction]], def. \ref{HomotopyEquivalence}, is a weak homotopy equivalence.

=--


+-- {: .num_example #FactoringTopologicalCodiagonalThroughCylinder}
###### Example

For $X\in Top$, the projection $X\times I \longrightarrow X$
from the [[cylinder object]] of $X$, def. \ref{TopologicalInterval},
is a [[weak homotopy equivalence]], def. \ref{WeakHomotopyEquivalenceOfTopologicalSpaces}. 

This means that the factorization 

$$
  \nabla_X 
  \;\colon\;
  X \sqcup X
  \stackrel{}{\longrightarrow}
  X\times I
  \stackrel{\simeq}{\longrightarrow}
$$

of the [[codiagonal]] $\nabla_X$ in def. \ref{TopologicalInterval}, which in general is far from being a [[monomorphism]], may be thought of as factoring it through a monomorphism after replacing $X$, up to weak homotopy equivalence, by $X\times I$.

In fact $X \sqcup X \to X \times I$ has better properties than the generic monomorphism has, in particular better homotopy invariant properties:
it has the [[left lifting property]] against all [[Serre fibrations]] $ E \stackrel{p}{\longrightarrow} B$ (def. \ref{SerreFibration}) that are also [[weak homotopy equivalences]].

=--


For $Y$ a [[topological space]], the set $Hom_{Top}(I,Y)$ of continuous functions from the standard interval $I$, def. \ref{TopologicalInterval}, to $Y$ is the set of continuous paths in $X$. Every such path may be though of as a [[left homotopy]] between its endpoints. Hence a function $X \longrightarrow Hom_{Top}(I,Y)$ is an $X$-parameterized collection of such paths. In order for that to also give a concept of homotopy, we need to impose a continuity condition on how the paths may vary, hence we need to put a suitable [[topological space|topology]] on $Hom_{Top}(I,X)$. This is the [[compact-open topology]]:

+-- {: .num_defn #CompactOpenTopology}
###### Definition

For $X$ a [[topological space]] and $Y$ a [[locally compact topological space|locally compact]] [[Hausdorff topological space]], the **[[mapping space]]**

$$
  X^Y \in Top
$$

is the [[topological space]] 

* whose underlying set is the set $Hom_{Top}(Y,X)$ of [[continuous 
functions]] $Y \to X$, 

* whose [[open subsets]] are [[finitary intersections]] of [[unions]] of the following [[topological base|subbase]] of standard open subsets:

  the standard open subset $U_{K,U} \subset Hom_{Top}(Y,X)$ for 

  * $K \hookrightarrow Y$ a [[compact topological space]] subset

  * $U \hookrightarrow X$ an [[open subset]]

  is the subset of [[continuous functions]] $f$ of all those  that fit into a [[commuting diagram]] of the form

  $$
    \array{
       K &\hookrightarrow& Y
       \\
       \downarrow && \downarrow^{\mathrlap{f}}
       \\
       U &\hookrightarrow& X
    }
    \,.
  $$

Accordingly this is called the _[[compact-open topology]]_ on the set of functions.

The construction extends to a [[functor]] 

$$
  (-)^{(-)} \;\colon\; Top_{lcH}^{op} \times Top \longrightarrow Top
  \,.
$$

=--
 
+-- {: .num_prop #MappingTopologicalSpaceIsExponentialObject}
###### Proposition

For $X$ a [[topological space]] and $Y$ a [[locally compact topological space|locally compact]] [[Hausdorff topological space]], the **topological [[mapping space]]** $X^Y$ from def. \ref{CompactOpenTopology} is an [[exponential object]]: there is a [[natural isomorphism|natural]] [[bijection]]

$$
  Hom_{Top}(Z \times Y, X) \simeq Hom_{Top}(Z, X^Y)
$$ 

between continuous functions out of any [[product topological space]] of $Y$ with any $Z \in Top$ and continuous functions from $Z$ into the mapping space.

=--

+-- {: .num_remark}
###### Remark

Proposition \ref{MappingTopologicalSpaceIsExponentialObject} fails if $Y$ is not locally compact and Hausdorff. Therefore the plain category [[Top]] of all topological spaces is not a [[Cartesian closed category]]. 

This is no problem for the construction of the homotopy theory of topological spaces as such, but it becomes a technical nuisance when comparing it for instance to the [[simplicial homotopy theory]] via the singular [[nerve and realization]] adjunction, since it implies that [[geometric realization]] of [[simplicial sets]] does not necessarily preserve [[finite limits]].

On the other hand, without changing any of the following discussion one may just pass to a more [[convenient category of topological spaces]] such as notably the [[full subcategory]] of [[compactly generated topological spaces]] $Top_{ck} \hookrightarrow Top$ which is [[Cartesian closed category|Cartesian closed]].

=--

+-- {: .num_defn #TopologicalPathSpace}
###### Definition

For $X$ a [[topological space]], its **[[path space object]]** is the topological [[mapping space]] $X^I$, def. \ref{MappingTopologicalSpaceIsExponentialObject}, out of the standard interval $I$ of def. \ref{TopologicalInterval}.


=--

+-- {: .num_example}
###### Example

The endpoint inclusion into the standard interval, def. \ref{TopologicalInterval}, makes the path space $X^I$ of def. \ref{TopologicalPathSpace} factor the [[diagonal]] on $X$ through the inclusion of constant paths and the endpoint evaluation of paths:


$$
  \Delta_X
  \;\colon\; 
  X \stackrel{X^{I \to \ast}}{\longrightarrow} X^I \stackrel{X^{\ast \sqcup \ast \to I}}{\longrightarrow} X \times X
  \,.
$$

Here

1. $X^{I \to \ast}$ is a [[weak homotopy equivalence]];

1. $X^{\ast \sqcup \ast \to I}$ is a [[Serre fibration]].

So while in general the [[diagonal]] $\Delta_X$ is far from being an [[epimorphism]] or even just a [[Serre fibration]], the factorization through the [[path space object]] may be thought of as replacing $X$, up to weak homotopy equivalence, by its path space, such as to turn its diagonal into a Serre fibration after all.

=--

+-- {: .num_defn }
###### Definition

For $f,g\colon X \longrightarrow Y$ two [[continuous functions]] between [[topological spaces]] $X,Y$, then a **[[right homotopy]]** $f \Rightarrow_R g$ is a [[continuous function]]

$$
  \eta \;\colon\; X \longrightarrow Y^I
$$

into the [[path space object]] of $X$, def. \ref{TopologicalPathSpace}, such that this fits into a [[commuting diagram]] of the form

$$
  \array{
    && Y
    \\
    & {}^{\mathllap{f}}\nearrow & \uparrow^{\mathrlap{X^{\delta_0}}}
    \\
    X &\stackrel{\eta}{\longrightarrow}& Y^I
    \\
    & {}_{\mathllap{g}}\searrow & \downarrow^{\mathrlap{Y^{\delta_1}}}
    \\
    && Y
  }
  \,.
$$


=--


### Cell complexes

+-- {: .num_defn #TopologicalGeneratingCofibrations}
###### Definition

For $n \in \mathbb{N}$ write

* $D^n \coloneqq \{ \vec x\in \mathbb{R}^n | {\vert \vec x \vert \leq 1}\} \hookrightarrow \mathbb{R}^n$ for the standard topological [[n-disk]];

* $S^{n-1} = \partial D^n \coloneqq \{ \vec x\in \mathbb{R}^n | {\vert \vec x \vert = 1}\} \hookrightarrow \mathbb{R}^n$ for the standard topological [[n-sphere]];

Write

$$
  I_{Top}
    \coloneqq
  \{S^{n-1} \stackrel{\iota_n}{\hookrightarrow} D^{n}\}_{n \in \mathbb{N}}
    \subset 
  Mor(Top)
$$

for the set of canonical [[boundary]] inclusion maps. This going to be called the set of standard **topological [[generating cofibrations]]**.

Notice that $S^{-1} = \emptyset$ and that $S^0 = \ast \sqcup \ast$.

=--

+-- {: .num_defn #TopologicalCellComplex}
###### Definition

For $X \in Top$ and for $n \in \mathbb{N}$, an **$n$-cell attachment** to $X$ is the [[pushout]] of a generatic cofibration, def. \ref{TopologicalGeneratingCofibrations}

$$
  \array{
    S^{n-1} &\stackrel{\phi}{\longrightarrow}& X
    \\
    {}^{\mathllap{\iota_n}}\downarrow && \downarrow
    \\
    D^n &\longrightarrow& X {}_\phi\underset{S^{n-1}}{\sqcup} D^n
  }
$$

along some [[continuous function]] $\phi$.

A continuous function $f \colon X \longrightarrow Y$ is called a **topological [[relative cell complex]]** if it is exhibited by a (possibly infinite) sequence of cell attachments to $X$, hence if it is a [[transfinite composition]] of [[pushouts]]

$$
  \array{
    \underset{i}{\coprod} S^{n_i - 1} &\longrightarrow& X_{k-1}
    \\
    {}^{\mathllap{\underset{i}{\coprod}\iota_{n_i}}}\downarrow 
     &(pb)& \downarrow  
    \\
    \underset{i}{\coprod} D^{n_i} &\longrightarrow& X_{k}
  }
$$

of [[coproducts]] of [[generating cofibrations]].

A topological space is a **[[cell complex]]** if $\emptyset \longrightarrow X$ is a relative cell complex.

A relative cell complex is called a **finite relative cell complex** if it is obtained from a [[finite number]] of cell attachments.

A (relative) cell complex is called a (relative) **[[CW-complex]]** if in the above transfinite composition is countable 

$$
  \array{
    X = X_0 &\longrightarrow& X_1 &\longrightarrow& X_2 &\longrightarrow& \cdots
    \\
    & {}_{\mathllap{f}}\searrow & \downarrow & \swarrow && \cdots
    \\
    && Y = \underset{\longrightarrow}{\lim} X_\bullet
  }
$$

and if $X_k$ is obtained from $X_{k-1}$ by attaching cells precisely only of [[dimension]] $k$.

=--

+-- {: .num_remark}
###### Remark

Strictly speaking a relative cell complex, def. \ref{TopologicalCellComplex}, is a function $f\colon X \to Y$, _together_ with its cell structure, hence together with the information of the pushout diagrams and the transfinite composition of the pushout maps that exhibit it.

In many applications, however,  all that matters is that there is _some_ (relative) cell decomosition, and then one tends to speak loosely and mean by a (relative) cell complex only a (relative) topological space that admits some cell decomposition.

=--

+-- {: .num_defn #TopologicalCCellComplex}
###### Definition

For $C \subset Mor(\mathcal{C})$ any [[class]] of morphisms, the concept of  **relative $C$-cell complexes** is defined as in def. \ref{TopologicalCellComplex}, with the boundary inclusions $\iota_n \in I_{Top}$ replaced by the maps in $C$: 

a **relative $C$-cell complex** is a [[transfinite composition]] of [[pushouts]] of [[coproducts]] of the maps in $C \hookrightarrow Mor(Top)$.

=--

Given a relative $C$-cell complex $\iota \colon  X \to Y$, def. \ref{TopologicalCCellComplex}, it is typically interesting to study the [[extension]] problem along $f$, i.e. to ask which topological spaces $E$ are such that every [[continuous function]] $f\colon X \longrightarrow E$ has an extension $\tilde $ along $\iota$ 

$$
  \array{
    X &\stackrel{f}{\longrightarrow}& E
    \\
    {}^{\mathllap{\iota}}\downarrow & \nearrow_{\mathrlap{\exists \tilde f}}
    \\
    Y
  }
  \,.
$$

If so, then this means that $E$ is sufficiently "spead out" with respect to the maps in $C$. More generally one considers this extension problem fiberwise, i.e. with both $E$ and $Y$ (hence also $X$) equipped with a map to some base space $B$.


+-- {: .num_defn #RightLiftingProperty}
###### Definition

Given a [[category]] $\mathcal{C}$ and a sub-[[class]] $C \subset Mor(\mathcal{C})$ of its [[morphisms]], then a morphism $p \colon E \longrightarrow B$ in $\mathcal{C}$ is said to have the [[right lifting property]] against the morphisms in $C$ if every [[commuting diagram]] in $\mathcal{C}$ of the form

$$
  \array{
    X &\longrightarrow& E
    \\
    {}^{\mathllap{c}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    Y &\longrightarrow& B
  }
  \,,
$$

with $c \in C$, has a [[lift]] $w$, in that it may be completed to a [[commuting diagram]] of the form

$$
  \array{
    X &\longrightarrow& E
    \\
    {}^{\mathllap{c}}\downarrow &{}^{\mathllap{w}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    Y &\longrightarrow& B
  }
  \,.
$$

We will also say that $f$ is a **$C$-[[injective morphism]]** if it satisfies the [[right lifting property]] against $C$.

=--


### Fibrations

+-- {: .num_defn #TopologicalGeneratingAcyclicCofibrations}
###### Definition

Write

$$
  J_{Top}
    \coloneqq
  \{D^n \stackrel{(id,\delta_0)}{\hookrightarrow} D^n \times I\}_{n \in \mathbb{N}}
  \subset Mor(Top)
$$

for the [[set]] of inclusions of the topological [[n-disks]], def. \ref{TopologicalGeneratingCofibrations}, into their [[cylinder objects]], def. \ref{TopologicalInterval}, along (for definiteness) the left endpoint inclusion.

These inclusions are similar to the standard topological [[generating cofibrations]] of def. \ref{TopologicalGeneratingCofibrations}, but in contrast to these they are "acyclic" (meaning: trivial on homotopy classes of maps from "cycles" given by [[n-spheres]]) in that they are [[weak homotopy equivalences]] (example \ref{FactoringTopologicalCodiagonalThroughCylinder}).

Accordingly, $J$ is to be called the set of standard **topological [[generating acyclic cofibrations]]**.

=--

+-- {: .num_lemma #TopologicalGeneratingAcyclicCofibrationsAreRelativeCellComplexes}
###### Lemma

The maps $D^n \hookrightarrow D^n \times I$ in def. \ref{TopologicalGeneratingAcyclicCofibrations} are finite [[relative cell complexes]], def. \ref{TopologicalCellComplex}.

=--


+-- {: .num_defn #SerreFibration}
###### Definition

A [[continuous function]] $p \colon E \longrightarrow B$
is called a **[[Serre fibration]]** if it is a $J_{Top}$-[[injective morphisms]]; i.e. if it has the [[right lifting property]], def. \ref{RightLiftingProperty}, against all topological generating acylic cofibrations, def. \ref{TopologicalGeneratingAcyclicCofibrations};
hence if for every [[commuting diagram]] of [[continuous functions]] of the form

$$
  \array{
    D^n &\longrightarrow& E
    \\
    {}^{\mathllap{(id,\delta_0)}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    D^n\times I &\longrightarrow& B
  }
  \,,
$$

has a [[lift]] $w$, in that it may be completed to a [[commuting diagram]] of the form

$$
  \array{
    D^n &\longrightarrow& E
    \\
    {}^{\mathllap{(id,\delta_0)}}\downarrow 
     &{}^{\mathllap{w}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    D^n\times I &\longrightarrow& B
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Def. \ref{SerreFibration} says, in view of the definition of [[left homotopy]], that a [[Serre fibration]] $p$ is a map with the property that given a [[left homotopy]], def. \ref{LeftHomotopy}, between two functions into its [[codomain]], and given a lift of one the two functions through $p$, then also the homotopy between the two lifts, in particular the second function lifts, too, and both lifts are related by left homotopy.

Therefore the condition on a [[Serre fibration]] is also called the _[[homotopy lifting property]]_ for maps whose domain is an [[n-disk]].

More generally one may ask functions $p$ to have such [[homotopy lifting property]] for functions with arbitrary domain. These are called _[[Hurewicz fibrations]]_. 

=--


## Background from model category theory

This section recalls some standard arguments in [[model category]] theory.

+-- {: .num_remark #RetractsOfMorphisms}
###### Remark

As usual, by a [[retract]] of a [[morphism]] $X \stackrel{f}{\longrightarrow} Y$ in some [[category]] $\mathcal{C}$ we mean a retract in the [[arrow category]] $\mathcal{C}^{\Delta[1]}$, hence a morphism $A \stackrel{g}{\longrightarrow} B$ such that in $\mathcal{C}^{\Delta[1]}$ there is a factorization of the identity on $g$ through $f$

$$
  id_g \;\colon\;
  g \longrightarrow f \longrightarrow g
  \,.
$$

This means equivalently that in $\mathcal{C}$ there is a [[commuting diagram]] of the form

$$
  \array{
    id_A \colon & A &\longrightarrow& X &\longrightarrow& A
    \\
    & \downarrow^{\mathrlap{g}} && \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{g}}
    \\
    id_A \colon & A &\longrightarrow& Y &\longrightarrow& A
  }
  \,.
$$

=--


### Lifting

+-- {: .num_defn #LiftingAndExtension}
###### Definition

Let $\mathcal{C}$ be any [[category]]. 
Given a [[diagram]] in $\mathcal{C}$ of the form

$$
  \array{
     X &\stackrel{f}{\longrightarrow}& Y
     \\
     {}^{\mathllap{p}}\downarrow
     \\
     B
  }
$$

then an *[[extension]]* of the [[morphism]] $f$ along the [[morphism]] $p$ is a completion to a [[commuting diagram]] of the form

$$
  \array{
     X &\stackrel{f}{\longrightarrow}& Y
     \\
     {}^{\mathllap{p}}\downarrow & \nearrow_{\mathrlap{\tilde f}}
     \\
     B
  }
  \,.
$$

Dually, given a [[diagram]] of the form

$$
  \array{
    && A
    \\
    && \downarrow^{\mathrlap{p}}
    \\
    X &\stackrel{f}{\longrightarrow}& Y
  }
$$

then a **[[lift]]** of $f$ through $p$ is a completion to a [[commuting diagram]] of the form

$$
  \array{
    && A
    \\
    &{}^{\mathllap{\tilde f}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    X &\stackrel{f}{\longrightarrow}& Y
  }
  \,.
$$

Combining these cases: given a square [[commuting diagram]] 

$$
  \array{
     X_1 &\stackrel{f_1}{\longrightarrow}& Y_1
     \\
     {}^{\mathllap{p_l}}\downarrow && \downarrow^{\mathrlap{p_r}}
     \\
     X_2 &\stackrel{f_1}{\longrightarrow}& Y_2     
  }
$$

then a **[[lifting]]** in the diagram is a completion to a [[commuting diagram]] of the form

$$
  \array{
     X_1 &\stackrel{f_1}{\longrightarrow}& Y_1
     \\
     {}^{\mathllap{p_l}}\downarrow &\nearrow& \downarrow^{\mathrlap{p_r}}
     \\
     X_2 &\stackrel{f_1}{\longrightarrow}& Y_2     
  }
  \,.
$$

Given a sub-[[class]] of morphhisms $C \subset Mor(\mathcal{C})$, then a morphism $p_r$ as above is said to have the **[[right lifting property]]** against $C$ if in all square diagrams with $p_r$ on the right and any $p_l \in C$ on the left a lift exists. Dually, a fixed $p_l$ is said to have the **[[left lifting property]]** against $C$ if in all square diagrams with $p_l$ on the left and any $p_r \in C$ on the left a lift exists.


=--


+-- {: .num_lemma #SaturationOfGeneratingCofibrations}
###### Lemma

Let $\mathcal{C}$ be a [[category]] with all small [[colimits]],
and let $C\subset Mor(\mathcal{C})$ be a sub-[[class]] of its morphisms.

Then every $C$-[[injective morphism]], def. \ref{RightLiftingProperty}, has the [[right lifting property]], def. \ref{LiftingAndExtension}, against all $C$-[[relative cell complexes]], def. \ref{TopologicalCCellComplex} and their [[retracts]], remark \ref{RetractsOfMorphisms}.

=--

+-- {: .num_lemma #RetractArgument}
###### Lemma
**(retract argument)**

If in a composite morphism

$$
  g \;\colon\; \stackrel{i}{\longrightarrow} \stackrel{p}{\longrightarrow}
$$

the factor $p$ has the [[right lifting property]], def. \ref{RightLiftingProperty}, against the total morphism $g$, then $g$ is a [[retract]] (rem. \ref{RetractsOfMorphisms}) of $i$.

=--


### The small object argument

Given a class $C \subset Mor(\mathcal{C})$ of morphisms in some [[category]] $\mathcal{C}$, a natural question is how to factor any given morphism $f\colon X \longrightarrow Y$ through a relative $C$-cell complex, def. \ref{TopologicalCCellComplex}, followed by a $C$-[[injective morphism]], def. \ref{RightLiftingProperty}

$$
  f 
    \;\colon\; 
  X 
    \stackrel{\in C cell}{\longrightarrow} 
  \hat X
    \stackrel{\in C fib}{\longrightarrow} 
  Y
  \,.
$$

A first approximation to such a factorization turns out to be given simply by forming $\hat X = X_1$ by attaching **all** possible $C$-cells to $X$. Namely let

$$
  (C/f) 
   \coloneqq
  \left\{
    \array{
       dom(c) &\stackrel{}{\longrightarrow}& X
       \\
       {}^{\mathllap{c\in C}}\downarrow && \downarrow^{\mathrlap{f}}
       \\
       cod(c) &\longrightarrow& Y
    }
  \right\}
$$

be the set of **all** ways to find a $C$-cell attachment in $f$, and consider the [[pushout]] $\hat X$ of the [[coproduct]] of morphisms in $C$ over all these:

$$
  \array{
    \underset{c\in(C/f)}{\coprod} dom(c) &\longrightarrow& X
    \\
    {}^{\mathllap{\underset{c\in(C/f)}{\coprod} c}}\downarrow
    &(po)& 
    \downarrow^{\mathrlap{}}
    \\
    \underset{c\in(C/f)}{\coprod} cod(c)
    &\longrightarrow&
    X_1
  }
  \,.
$$

This gets already close to producing the intended factorization: 

First of all the resulting map $X \to X_1$ is a $C$-relative cell complex, by construction. 

Second, by the fact that the coproduct is over all commuting squres to $f$, the morphism $f$ itself makes a [[commuting diagram]] 

$$
  \array{
    \underset{c\in(C/f)}{\coprod} dom(c) &\longrightarrow& X
    \\
    {}^{\mathllap{\underset{c\in(C/f)}{\coprod} c}}\downarrow
    && 
    \downarrow^{\mathrlap{f}}
    \\
    \underset{c\in(C/f)}{\coprod} cod(c)
    &\longrightarrow&
    Y
  }
$$

and hence the [[universal property]] of the [[colimit]] means that $f$ is indeed factored through that $C$-cell complex $X_1$; we may suggestively arrange that factorizing diagram like so:

$$
  \array{
    \underset{c\in(C/f)}{\coprod} dom(c) 
      &\longrightarrow& 
    X
    \\
    {}^{\mathllap{id}}\downarrow
    && 
    \downarrow^{\mathrlap{}}
    \\
    \underset{c\in(C/f)}{\coprod} dom(c)
     &&
    X_1
    \\
    {}^{\mathllap{\underset{c\in(C/f)}{\coprod} c}}\downarrow 
    &\nearrow& \downarrow
    \\
    \underset{c\in(C/f)}{\coprod} cod(c)
    &\longrightarrow&
    Y
  }
  \,.
$$

This shows that, finally, the colimiting [[co-cone]] map -- the one that now appears diagonally -- **almost** exhibits the desired right lifting of $X_1 \to X$ against the $c\in C$. The failure of that to hold on the nose is only the fact that a horizontal map in the middle of the above diagram is missing: the diagonal map obtained above lifts not all commuting diagrams of $c\in C$ into $f$, but only those where the top morphism $dom(c) \to X_1$ factors through $X \to X_1$.

The idea of the [[small object argument]] now is to fix this only problem by iterating the construction: next factor $X_1 \to X$ in the same way into 

$$
  X_1 \longrightarrow X_2 \longrightarrow X
$$

and so forth. Since relative $C$-cell complexes are closed under composition, at stage $n$ the resulting $X \longrightarrow X_n$ is still a $C$-cell complex, getting bigger and bigger. But accordingly, the failure of the accompanying $X_n \longrightarrow Y$ to be a $C$-[[injective morphism]] becomes smaller and smaller, for it now lifts against all diagrams where $dom(c) \longrightarrow X_n$ factors through $X_{n-1}\longrightarrow X_n$, which intuitively is less and less of a condition as the $X_{n-1}$ grow larger and larger.

The concept of _[[small object]]_ is just what makes this intuition precise and finishes the small object argument. For the present purpose we just need the following simple version:

+-- {: .num_defn #ClassOfMorphismsWithSmallDomains}
###### Definition

For $\mathcal{C}$ a [[category]] and $C \subset Mor(\mathcal{C})$
a sub-[[class]] of its morphisms, say that these have _small [[domains]]_
if for every $c\in C$ and for every $C$-[[relative cell complex]] 
$f\colon X \longrightarrow \hat X$ every morphism 
$dom(c)\longrightarrow \hat X$ factors through a finite relative subcomplex.

=--

+-- {: .num_prop #SmallObjectArgument}
###### Proposition
**(small object argument)**

Let $\mathcal{C}$ be a [[locally small category]] with all small [[colimits]]. If a [[class]] $C\subset Mor(\mathcal{C})$ of morphisms has all small domains in the sense of def. \ref{ClassOfMorphismsWithSmallDomains}, then every morphism $f\colon X\longrightarrow $ in $\mathcal{C}$ factors through a $C$-[[relative cell complex]], def. \ref{TopologicalCCellComplex}, followed by a $C$-[[injective morphism]], def. \ref{RightLiftingProperty}

$$
  f \;\colon\;
  X \stackrel{\in C cell}{\longrightarrow} \hat X \stackrel{\in C fib}{\longrightarrow}
  Y
  \,.
$$
 
=--

## The classical model structure $Top_{Quillen}$

+-- {: .num_defn #ClassesOfMorhismsInTopQuillen}
###### Definition

Say that a [[continuous function]], hence a [[morphism]] in [[Top]] is

* a (classical) **weak equivalence** if it is a [[weak homotopy equivalence]], def. \ref{WeakHomotopyEquivalenceOfTopologicalSpaces};

* a (classical) **fibration** if it is a [[Serre fibration]], def. \ref{SerreFibration};

* a (classical) **cofibration** if it is a [[retract]], rem \ref{RetractsOfMorphisms}, of a [[relative cell complex]], def. \ref{TopologicalCellComplex}.

=--

and as usual:

* an **acyclic cofibration** if it is a cofibration and a weak equivalence;

* an **acyclic fibration** if it is a fibration and a weak equivalence.



### Technical lemmas

The [[proof]] ([below](#VerificationOfTopQuillen)) that def. \ref{ClassesOfMorhismsInTopQuillen} defines a [[model category]] structure involves two technical lemmas which concern the special nature of [[topological spaces]].  With these two lemmas in hand, the rest of the proof is a routine argument in model category theory.

+-- {: .num_lemma #CompactSubsetsAreSmallInCellComplexes}
###### Lemma

Every [[compact topological space|compact]] [[topological subspace|subspace]] of a topological [[cell complex]], def. \ref{TopologicalCellComplex}, is contained in the [[union]] of a [[finite number]] of cells.

=--

A proof is spelled out for instance in ([Hirschhorn 15, section 3.1](#Hirschhorn15)).

+-- {: .num_lemma #AcyclicSerreFibrationsAreTheJTopFibrations}
###### Lemma

The continuous functions with the [[right lifting property]], def. \ref{RightLiftingProperty} against the set $I_{Top} = \{S^{n-1}\hookrightarrow D^n\}$ of topological [[generating cofibrations]], def. \ref{TopologicalGeneratingCofibrations}, are precisely those which are both [[weak homotopy equivalences]], def. \ref{WeakHomotopyEquivalenceOfTopologicalSpaces} as well as [[Serre fibrations]], def. \ref{SerreFibration}.

=--


+-- {: .proof}
###### Proof

We break this up into three sub-statements:

**A) $I_{Top}$-[[injective morphisms]] are in particular weak homotopy equivalences**

Let $p \colon \hat X \to X$ have the [[right lifting property]] against $I_{Top}$

$$
  \array{
    S^{n-1}  &\longrightarrow & \hat X
    \\
    {}^{\mathllap{\iota_n}}\downarrow &{}^{\mathllap{\exists}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    D^n &\longrightarrow& X
  }
$$

We check that the lifts in these diagrams exhibit $\pi_\bullet(f)$ as being an [[isomorphism]] on all [[homotopy groups]], def. \ref{HomotopyGroupsOftopologicalSpaces}:


For $n = 0$ the existence of these lifts says that every point of $X$ is in the image of $p$, hence that $\pi_0(\hat X) \to \pi_0(X)$ is [[surjection|surjective]]. Let then $S^0 = \ast \coprod \ast \longrightarrow \hat X$ be a map that hits two connected components, then the existence of the lift says that if they have the same image in $\pi_0(X)$ then they were already the same connected component in $\hat X$. Hence $\pi_0(\hat X)\to \pi_0(X)$ is also [[injection|injective]] and hence is a [[bijection]].

Similarly, for $n \geq 1$, if $S^n \to \hat X$ represents an element in $\pi_n(\hat X)$ that becomes trivial in $\pi_n(X)$, then the existence of the lift says that it already represented the trivial element itself. Hence $\pi_n(\hat X) \to \pi_n(X)$ has trivial [[kernel]] and so is injective. 

Finally, to see that $\pi_n(\hat X) \to \pi_n(X)$ is also surjective, hence bijective, observe that every elements in $\pi_n(X)$ is equivalently represented by a commuting diagram of the form

$$
  \array{
    S^{n-1} &\longrightarrow& \ast &\longrightarrow& \hat X
    \\
    \downarrow && \downarrow && \downarrow
    \\
    D^n &\longrightarrow& X &=& X
  }  
$$

and so here the lift gives a representative of a preimage in $\pi_{n}(\hat X)$.

**B) $I_{Top}$-[[injective morphisms]] are in particular Serre fibrations**

By lemma \ref{SaturationOfGeneratingCofibrations} an $I_{Top}$-[[injective morphisms]] has also the [[right lifting property]] against all [[relative cell complexes]], and hence by lemma \ref{TopologicalGeneratingAcyclicCofibrationsAreRelativeCellComplexes} it is also a $J_{Top}$-[[injective morphism]], hence a Serre fibration.

**C) Acyclic Serre fibrations are in particular $I_{Top}$-[[injective morphisms]]**

A proof of this is spelled out in ([Hirschhorn 15, section 6](#Hirschhorn15)).


=--

### Verification of the axioms
 {#VerificationOfTopQuillen}

We use the above to prove that the classes of morphisms in def. \ref{ClassesOfMorhismsInTopQuillen} satifies the conditions for a [[model category]] structure on the category [[Top]].

+-- {: .num_prop #QuillenWeakEquivalencesSatisfyTwoOutOfThree}
###### Proposition

The classical weak equivalences, def. \ref{ClassesOfMorhismsInTopQuillen}, satify [[two-out-of-three]].

=--

+-- {: .proof}
###### Proof

Since [[isomorphisms]] (of [[homotopy groups]]) satisfy 2-out-of-3, this property is directly inherited via the very definition of [[weak homotopy equivalence]], def. \ref{WeakHomotopyEquivalenceOfTopologicalSpaces}.

=--

+-- {: .num_prop}
###### Proposition

Every morphism $f\colon X \longrightarrow Y$ in [[Top]] factors as a classical cofibration followed by an acyclic fibration, def. \ref{ClassesOfMorhismsInTopQuillen}:

$$
  f
  \;\colon\;
  X 
    \stackrel{cofib}{\longrightarrow}
  \hat X
    \stackrel{fib_{we}}{\longrightarrow}
  Y
  \,.
$$

=--

+-- {: .proof}
###### Proof

By lemma \ref{CompactSubsetsAreSmallInCellComplexes}
the set $I_{Top} = \{S^{n-1}\hookrightarrow D^n\}$ of 
topological [[generating cofibrations]], def. \ref{TopologicalGeneratingCofibrations}, has small domains, in the sense of def. \ref{ClassOfMorphismsWithSmallDomains} (the [[n-spheres]] are [[compact topological space|compact]]). Hence by the [[small object argument]], prop. \ref{SmallObjectArgument}, $f$ factors as an $I_{Top}$-relative cell complex, hence just a plain relative cell complex, followed by an $I_{Top}$-[[injective morphisms]], def. \ref{RightLiftingProperty}.

$$
  f 
  \;\colon\;
  X 
   \stackrel{\in cofib}{\longrightarrow}
  \hat X
   \stackrel{\in I_{top} fib}{\longrightarrow}
  Y
  \,.
$$

By lemma \ref{AcyclicSerreFibrationsAreTheJTopFibrations} the map $\hat X \to X$ is both a weak equivalence as well as a Serre fibration.

=--

+-- {: .num_prop #ContinuousFunctionsFactorAsQuillenAcyclicCofibrationFollowedBySerreFibration}
###### Proposition

Every morphism $f\colon X \longrightarrow Y$ in [[Top]] factors as an acyclic classical cofibration followed by a fibration, def. \ref{ClassesOfMorhismsInTopQuillen}:

$$
  f
  \;\colon\;
  X 
    \stackrel{cofib_{we}}{\longrightarrow}
  \hat X
    \stackrel{fib}{\longrightarrow}
  Y
  \,.
$$

=--

+-- {: .proof}
###### Proof

By lemma \ref{TopologicalGeneratingAcyclicCofibrationsAreRelativeCellComplexes} a relative $J_{Top}$-cell complex is in particular a relative $I_{Top}$-cell complex. 

By lemma \ref{CompactSubsetsAreSmallInCellComplexes}
the set $J_{Top} = \{D^n \hookrightarrow D^n\times I\}$ of 
topological [[generating acyclic cofibrations]], def. \ref{TopologicalGeneratingAcyclicCofibrations}, has small domains, in the sense of def. \ref{ClassOfMorphismsWithSmallDomains} (the [[n-disks]] are [[compact topological space|compact]]). Hence by the [[small object argument]], prop. \ref{SmallObjectArgument}, $f$ factors as an $J_{Top}$-relative cell complex, followed by an $J_{top}$-[[injective morphisms]], def. \ref{RightLiftingProperty}:

$$
  f
  \;\colon\;
  X 
   \stackrel{J_{Top} cell}{\longrightarrow}
  \hat X
    \stackrel{J_{Top} fib}{\longrightarrow}
  X
  \,.
$$

By definition this makes $\hat X \to X$ a [[Serre fibration]], hence a fibration.

By lemma \ref{TopologicalGeneratingAcyclicCofibrationsAreRelativeCellComplexes} a relative $J_{Top}$-cell complex is in particular a relative $I_{Top}$-cell complex and hence $X \to \hat X$ is a cofibration.

Finally, to see that relative $J_{Top}$-cell complexes are weak homotopy equivalences, first notice that with the elements $D^n \hookrightarrow D^n \times I$ of $J_{Top}$ themselves, also each stage $X_{k} \to X_{k+1}$ in the construction of $\hat X$ via the [[small object argument]] is a [[strong deformation retract]], hence, by example \ref{TopologicalHomotopyEquivalencesAreWeakHomotopyEquivalences}, a weak homotopy equivalence. Now the [[small object argument]] with lemma \ref{CompactSubsetsAreSmallInCellComplexes} applies once more to give that every representative and every null homotopy of elements in $\pi_n(\hat X)$ already exist at some stage $X_n$, hence that also $\underset{\longrightarrow}{\lim}_{k} \pi_\bullet(X_k)\to \pi_\bullet(\hat X)$ is an isomorphism. (...)


=--

+-- {: .num_prop}
###### Proposition

Every [[commuting diagram|commuting square]] in [[Top]] with the left morphism a classical cofibration and the right morphism a fibration, def. \ref{ClassesOfMorhismsInTopQuillen}

$$
  \array{
    &\longrightarrow&
    \\
    {}^{\mathllap{{g \in} \atop { cof}}}\downarrow && \downarrow^{\mathrlap{{f \in }\atop fib}}
    \\
    &\longrightarrow&
  }
$$

admits a [[lift]] as soon as one of the two is also a weak equivalence.


=--

+-- {: .proof}
###### Proof

**A)** If the fibration $f$ is also a weak equivalence, then lemma \ref{AcyclicSerreFibrationsAreTheJTopFibrations} says that it has the right lifting property against the generating cofibrations $I_{Top}$, and lemma \ref{SaturationOfGeneratingCofibrations} implies the claim.

**B)** If the cofibration $g$ on the left is also a weak equivalence, consider any factorization into a relative $J_{Top}$-cell complex, def. \ref{TopologicalGeneratingAcyclicCofibrations}, def. \ref{TopologicalCCellComplex}, followed by a fibration,

$$
  g \;\colon\; \stackrel{J_{Top} cell}{\longrightarrow} \stackrel{fib}{\longrightarrow}
  \,,
$$

as in the proof of prop. \ref{ContinuousFunctionsFactorAsQuillenAcyclicCofibrationFollowedBySerreFibration}. Now by [[two-out-of-three]], prop. \ref{QuillenWeakEquivalencesSatisfyTwoOutOfThree}, the factorizing fibration is actually an acyclic fibration. By case A), this acyclic fibration has the [[right lifting property]] against the cofibration $g$ itself, and so the [[retract argument]], lemma \ref{RetractArgument} gives that $g$  is a [[retract]] of a relative $J_{Top}$-cell complex. With this, finally lemma \ref{SaturationOfGeneratingCofibrations} implies that $f$ has the [[right lifting property]] against $g$.

=--


In conclusion:

+-- {: .num_theorem #TopQuillenModelStructure} 
###### Theorem

The classes of morphisms in $Mor(Top)$ of def.  \ref{ClassesOfMorhismsInTopQuillen},

* $W = $ [[weak homotopy equivalences]],

* $F = $ [[Serre fibrations]] 

* $C = $ [[retracts]] of [[relative cell complexes]]

define a [[model category]] structure, $Top_{Quillen}$.

=--


### The homotopy theory

(...)

+-- {: .num_remark} 
###### Remark

Theorem \ref{TopQuillenModelStructure} in itself implies only that every topological space is weakly equivalent to a [[cell complex]], def. \ref{TopologicalCellComplex}. But by the [[Quillen equivalence]] to the [[Quillen model structure on simplicial sets]] every topological space is weakly homotopy equivalent to the [[geometric realization]] of its [[singular simplicial complex]] and every geometric realization of a [[simplicial set]] is (by [this proposition](geometric+realization#mono)) even a [[CW-complex]], def. \ref{TopologicalCellComplex}.

=--

(...)

## Related concepts

* [[classical model structure on simplicial sets]]

* [[classical model structure on pointed topological spaces]]

## References

The original article is

* {#Quillen67} [[Dan Quillen]], chapter II, section 3 of _Homotopical algebra_, Lecture Notes in Mathematics __43__, Springer-Verlag 1967, iv+156 pp.

An expository, concise and comprehensive writeup of the proof of the model category axioms is in 

* {#Hirschhorn15} [[Philip Hirschhorn]], _The Quillen model category of topological spaces_, 2015 ([arXiv:1508.01942](http://arxiv.org/abs/1508.01942))

[[!redirects Quillen model structure on topological spaces]]
[[!redirects Quillen model structure on Top]]

[[!redirects Quillen-Serre model structure on topological spaces]]
[[!redirects Quillen-Serre model structure on Top]]

[[!redirects standard model structure on topological spaces]]
[[!redirects standard model structure on Top]]