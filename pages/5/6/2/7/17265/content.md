
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

The _classical model structure on topological spaces_ or _Quillen-Serre model structure_ $Top_{Quillen}$ ([Quillen 67, II.3](#Quillen67)) is a [[model category]] structure on the [[category]] [[Top]] of [[topological spaces]] (also on many [[convenient categories of topological spaces]]) which represents the standard [[homotopy theory]] of [[CW-complexes]] ([[topological homotopy theory]]), in that its [[homotopy category of a model category]] is the [[classical homotopy category]] on [[cell complexes]]/[[CW-complexes]].

Its [[weak equivalences]] are the [[weak homotopy equivalences]], its [[fibrations]] are the [[Serre fibrations]] and its [[cofibrations]] are the [[retracts]] of [[relative cell complexes]].

The [[singular simplicial complex]]/[[geometric realization]] [[nerve and realization|adjunction]] constitutes a [[Quillen equivalence]] between 
$Top_{Quillen}$ and $sSet_{Quillen}$, the [[classical model structure on simplicial sets]]. This is sometimes called part of the statement of the _[[homotopy hypothesis]]_ [for Kan complexes](homotopy+hypothesis#ForKanComplexes). In the language of [[(∞,1)-category theory]] this means that $Top_{Quillen}$ and $sSet_{Quillen}$ both are [[presentable (∞,1)-category|presentations]] of the [[(∞,1)-category]] [[∞Grpd]] of [[∞-groupoids]].

There are also other model structures on [[Top]] itself, see at _[[model structure on topological spaces]]_ for more. This entry here focuses on just the classical model structure on topological spaces.


## Background from point-set topology

This section recalls basic relevant concepts from [[topology]] ("point-set topology") and highlights some basic facts that may serve to motivate the Quillen model structure below.

### Homotopy

The fundamental concept of [[homotopy theory]] is that of _[[homotopy]]_. In the context of [[topological spaces]] this is about [[continuous function|contiunous]] deformations of [[continuous functions]] parameterized by the standard [[topological interval]]:

+-- {: .num_defn #TopologicalInterval}
###### Definition

Write 

$$
  I \coloneqq [0,1] \hookrightarrow \mathbb{R}
$$

for the standard [[topological interval]], a [[compact topological space|compact]] [[connected topological space|connected]] [[topological subspace]] of the [[real line]].

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
     X
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

For $n \in \mathbb{N}$, $n \geq 1$ and for $x \colon \ast \to X$
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


+-- {: .num_prop #TopologicalHomotopyEquivalencesAreWeakHomotopyEquivalences}
###### Proposition

Every [[homotopy equivalence]], def. \ref{HomotopyEquivalence}, is a weak homotopy equivalence, def. \ref{WeakHomotopyEquivalenceOfTopologicalSpaces}.

In particular a [[deformation retraction]], def. \ref{HomotopyEquivalence}, is a weak homotopy equivalence.

=--

+-- {: .proof}
###### Proof

First observe that for all $X\in$ [[Top]] the inclusion maps 

$$
  X \overset{(id,\delta_0)}{\longrightarrow} X \times I
$$

into the standard [[cylinder object]], def. \ref{TopologicalInterval}, are weak homotopy equivalences: by postcomposition with the contracting homotopy of the interval from example \ref{StandardContractionOfStandardInterval} all homotopy groups of $X \times I$ have representatives that factor through this inclusion.

Then given a general [[homotopy equivalence]], apply the homotopy groups functor to the corresponding homotopy diagrams (where for the moment we notationally suppress the choice of basepoint for readability) to get two commuting diagrams

$$
  \array{
     \pi_\bullet(X) 
     \\
     {}^{\mathllap{\pi_\bullet(id,\delta_0)}}\downarrow & \searrow^{\mathrlap{\pi_\bullet(f)\circ \pi_\bullet(g)}}
     \\
     \pi_\bullet(X \times I) &\stackrel{\pi_\bullet(\eta)}{\longrightarrow}& \pi_\bullet(Y)
     \\
     {}^{\mathllap{\pi_\bullet(id,\delta_1)}}\uparrow & \nearrow_{\mathrlap{\pi_\bullet(id)}}
     \\
     \pi_\bullet(X)
  }
  \;\;\;\;\;\;\;
  \,,
  \;\;\;\;\;\;\;
  \array{
     \pi_\bullet(Y) 
     \\
     {}^{\mathllap{\pi_\bullet(id,\delta_0)}}\downarrow & \searrow^{\mathrlap{\pi_\bullet(g)\circ \pi_\bullet(f)}}
     \\
     \pi_\bullet(Y \times I) &\stackrel{\pi_\bullet(\eta)}{\longrightarrow}& \pi_\bullet(X)
     \\
     {}^{\mathllap{\pi_\bullet(id,\delta_1)}}\uparrow & \nearrow_{\mathrlap{\pi_\bullet(id)}}
     \\
     \pi_\bullet(Y)
  }
  \,.
$$

By the previous observation, the vertical morphisms here are isomorphisms, and hence these diagrams exhibit $\pi_\bullet(f)$ as the inverse of $\pi_\bullet(g)$, hence both as isomorphisms.

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

On the other hand, without changing any of the following discussion one may just pass to a more [[convenient category of topological spaces]] such as notably the [[full subcategory]] of [[compactly generated topological spaces]] $Top_{cg} \hookrightarrow Top$ which is [[Cartesian closed category|Cartesian closed]].

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
     &(po)& \downarrow  
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

For $C \subset Mor(Top)$ any [[class]] of morphisms, the concept of  **relative $C$-cell complexes** is defined as in def. \ref{TopologicalCellComplex}, with the boundary inclusions $\iota_n \in I_{Top}$ replaced by the maps in $C$: 

a **relative $C$-cell complex** is a [[transfinite composition]] of [[pushouts]] of [[coproducts]] of the maps in $C \hookrightarrow Mor(Top)$.

=--

Given a relative $C$-cell complex $\iota \colon  X \to Y$, def. \ref{TopologicalCCellComplex}, it is typically interesting to study the [[extension]] problem along $f$, i.e. to ask which topological spaces $E$ are such that every [[continuous function]] $f\colon X \longrightarrow E$ has an extension $\tilde f$ along $\iota$ 

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

If so, then this means that $E$ is sufficiently "spread out" with respect to the maps in $C$. More generally one considers this extension problem fiberwise, i.e. with both $E$ and $Y$ (hence also $X$) equipped with a map to some base space $B$.


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

+-- {: .proof}
###### Proof

There is a [[homeomorphism]]

$$
  \array{
     D^n & = & D^n 
     \\
     {}^{\mathllap{(id,\delta_0)}}\downarrow  && \downarrow
     \\
     D^n \times I &\simeq& D^{n+1}
  }
$$

such that the map on the right is the inclusion of one hemisphere into the [[boundary]] [[n-sphere]] of $D^{n+1}$. This inclusion is the result of attaching two cells:

$$
  \array{
    S^{n-1} &\overset{\iota_n}{\longrightarrow}& D^n 
    \\
    {}^{\mathllap{\iota_n}}\downarrow &(po)& \downarrow
    \\
    D^n &\longrightarrow& S^{n}
    \\
    && \downarrow^{=}
    \\
    S^n &\overset{id}{\longrightarrow}& S^n
    \\
    {}^{\mathllap{\iota_{n+1}}}\downarrow &(po)& \downarrow
    \\
    D^{n+1} &\underset{id}{\longrightarrow}& D^{n+1}
  }
  \,.
$$

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

+-- {: .num_remark #SerreFibrationsByLiftingAgainstMapsHomeomorphicToDiskInclusions}
###### Remark

The precise shape of $D^n$ and $D^n \times I$ in def. \ref{SerreFibration} turns out not to actually matter much for the nature of Serre fibrations. We will eventually find below (prop. \ref{LiftingPropertyInTheClassicalModelStructureOnTopologicalSpaces}) that what actually matters here is only that the inclusions $D^n \hookrightarrow D^n \times I$ are [[relative cell complexes]] and [[weak homotopy equivalences]] and that all of these may be generated from them in a suitable way.

But for simple special cases this is readily seen directly, too. Notably it is trivial, but nevertheless important in applications, that we could replace the [[n-disks]] in def. \ref{SerreFibration} with any [[homeomorphism|homeomorphic]] topological space. A choice that becomes important in the comparison to the [[classical model structure on simplicial sets]] is to instead take the topological [[n-simplices]] $\Delta^n$. Hence a Serre fibration is equivalently characterized as having lifts in all diagrams of the form

$$
  \array{
    \Delta^n &\longrightarrow& E
    \\
    {}^{\mathllap{(id,\delta_0)}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    \Delta^n\times I &\longrightarrow& B
  }
  \,.
$$

Other deformations of the $n$-disks are useful in computations, too. For instance there is a homeomorphism from the $n$-disk to its "cylinder with interior and end removed", formally:

$$
  \array{
    (D^n \times \{0\})\cup (\partial D^n \times I) &\simeq& D^n
    \\
    \downarrow && \downarrow
    \\
    D^n \times I \times I &\simeq& D^n\times I
  }
$$

and hence $f$ is a Serre fibration equivalently also if it admits lifts in all diagrams of the form

$$
  \array{
    (D^n \times \{0\})\cup (\partial D^n \times I) &\longrightarrow& E
    \\
    {}^{\mathllap{(id,\delta_0)}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    \Delta^n\times I &\longrightarrow& B
  }
  \,.
$$

=--

+-- {: .num_prop #SerreFibrationGivesExactSequenceOfHomotopyGroups}
###### Proposition

Let $f\colon X \longrightarrow Y$ be a [[Serre fibration]], def. \ref{SerreFibration}, let $y \colon \ast \to Y$ be any point and write 

$$
  F_y \overset{\iota}{\hookrightarrow} X \overset{f}{\longrightarrow} Y
$$

for the [[fiber]] inclusion over that point. Then for every choice $x \colon \ast \to X$ of lift of the point $y$ through $f$, the induced sequence of [[homotopy groups]]

$$

  \pi_{\bullet}(F_y, x)
    \overset{\iota_\ast}{\longrightarrow}
  \pi_\bullet(X, x)
    \overset{f_\ast}{\longrightarrow}
  \pi_\bullet(Y)
$$

is [[exact sequence|exact]], in that the [[kernel]] of $f_\ast$ is canonically identified with the [[image]] of $\iota_\ast$: 

$$
  ker(f_\ast) \simeq im(\iota_\ast)
  \,.
$$

=--

+-- {: .proof}
###### Proof

It is clear that the image of $\iota_\ast$ is in the kernel of $f_\ast$ (every sphere in $F_y\hookrightarrow X$ becomes constant on $y$, hence contractible, when sent forward to $Y$).

For the converse, let $[\alpha]\in \pi_{\bullet}(X,x)$ be represented by some $\alpha \colon S^{n-1} \to X$. Assume that $[\alpha]$ is in the kernel of $f_\ast$. This means equivalently that $\alpha$ fits into a [[commuting diagram]] of the form

$$
  \array{
    S^{n-1} &\overset{\alpha}{\longrightarrow}& X
    \\
    \downarrow && \downarrow^{\mathrlap{f}}
    \\
    D^n &\overset{\kappa}{\longrightarrow}& Y
  }
  \,,
$$

where $\kappa$ is the contracting homotopy witnessing that $f_\ast[\alpha] = 0$.

Now since $x$ is a lift of $y$, there exists a [[left homotopy]] 

$$
  \eta  \;\colon\; \kappa \Rightarrow const_y
$$ 

as follows:

$$
  \array{
    && S^{n-1} &\overset{\alpha}{\longrightarrow}& X
    \\
    && {}^{\mathllap{\iota_n}}\downarrow && \downarrow^{\mathrlap{f}}
    \\
    && D^n &\overset{\kappa}{\longrightarrow}& Y
    \\
    && \downarrow^{\mathrlap{(id,1)}} && \downarrow^{\mathrlap{id}}
    \\
    D^n &\overset{(id,0)}{\longrightarrow}& D^n \times I &\overset{\eta}{\longrightarrow}& Y
    \\
    \downarrow && &&  \downarrow
    \\
    \ast && \overset{y}{\longrightarrow} && Y
  }
$$

(for instance: regard $D^n$ as embedded in $\mathbb{R}^n$ such that $0 \in \mathbb{R}^n$ is identified with the basepoint on the boundary of $D^n$ and set $\eta(\vec v,t) \coloneqq \kappa(t \vec v)$).

The [[pasting]] of the top two squares that have appeared this way is equivalent to the following commuting square

$$
  \array{
    S^{n-1} &\longrightarrow& &\overset{\alpha}{\longrightarrow}& X
    \\
    {}^{\mathllap{(id,1)}}\downarrow 
    &&
    && \downarrow^{\mathrlap{f}}
    \\
    S^{n-1} \times I 
      &\overset{(\iota_n, id)}{\longrightarrow}& 
    D^n \times I 
      &\overset{\eta}{\longrightarrow}& 
    Y
  }
  \,.
$$

Because $S^{n-1} \to S^{n-1}\times I$ is a $J_{Top}$-[[relative cell complex]] and $f$ is a [[Serre fibration]] (see there), this has a [[lift]] 

$$
  \tilde \eta \;\colon\; S^{n-1} \times I \longrightarrow X
  \,.
$$

Notice that $\tilde \eta$ is a basepoint preserving [[left homotopy]] from $\alpha = \tilde \eta|_1$ to some $\alpha' \coloneqq \tilde \eta|_0$. Being homotopic, they represent the same element of $\pi_{n-1}(X,x)$:

$$
  [\alpha'] = [\alpha]
  \,.
$$

But the new representative $\alpha'$ has the special property that its image in $Y$ is not just trivializable, but trivialized:
combining $\tilde \eta$ with the previous diagram shows that it sits in the following commuting diagram

$$
  \array{
    \alpha' \colon & S^{n-1} &\overset{(id,0)}{\longrightarrow}& S^{n-1}\times I &\overset{\tilde \eta}{\longrightarrow}& X
    \\
    & \downarrow^{\iota_n} && \downarrow^{\mathrlap{(\iota_n,id)}} && \downarrow^{\mathrlap{f}}
    \\
    & D^n &\overset{(id,0)}{\longrightarrow}& D^n \times I &\overset{\eta}{\longrightarrow}& Y
    \\
    & \downarrow && &&  \downarrow
    \\
    & \ast && \overset{y}{\longrightarrow} && Y
  }
  \,.
$$

The commutativity of the outer square says that $f_\ast \alpha'$ is constant, hence that $\alpha'$ is entirely contained in the fiber $F_y$. Said more abstractly, the [[universal property]] of [[fibers]] gives that $\alpha'$ factors through $F_y\overset{\iota}{\hookrightarrow} X$, hence that $[\alpha'] = [\alpha]$ is in the image of $\iota_\ast$.

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
    id_B \colon & B &\longrightarrow& Y &\longrightarrow& B
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

+-- {: .proof}
###### Proof

This is an immediate consequence of the general fact ([here](injective+or+projective+morphism#ClosurePropertiesOfInjectiveAndProjectiveMorphisms)) that classes of morphisms characterized by a [[left lifting property]] are closed under the operations of [[coproducts]], [[pushouts]], [[retracts]] and [[transfinite composition]].

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

Given a [[set]] $C \subset Mor(\mathcal{C})$ of morphisms in some [[category]] $\mathcal{C}$, a natural question is how to factor any given morphism $f\colon X \longrightarrow Y$ through a relative $C$-cell complex, def. \ref{TopologicalCCellComplex}, followed by a $C$-[[injective morphism]], def. \ref{RightLiftingProperty}

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

This shows that, finally, the colimiting [[co-cone]] map -- the one that now appears diagonally -- **almost** exhibits the desired right lifting of $X_1 \to Y$ against the $c\in C$. The failure of that to hold on the nose is only the fact that a horizontal map in the middle of the above diagram is missing: the diagonal map obtained above lifts not all commuting diagrams of $c\in C$ into $f$, but only those where the top morphism $dom(c) \to X_1$ factors through $X \to X_1$.

The idea of the [[small object argument]] now is to fix this only remaining problem by iterating the construction: next factor $X_1 \to Y$ in the same way into 

$$
  X_1 \longrightarrow X_2 \longrightarrow Y
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

Let $\mathcal{C}$ be a [[locally small category]] with all small [[colimits]]. If a [[set]] $C\subset Mor(\mathcal{C})$ of morphisms has all small domains in the sense of def. \ref{ClassOfMorphismsWithSmallDomains}, then every morphism $f\colon X\longrightarrow $ in $\mathcal{C}$ factors through a $C$-[[relative cell complex]], def. \ref{TopologicalCCellComplex}, followed by a $C$-[[injective morphism]], def. \ref{RightLiftingProperty}

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
 {#TechnicalLemmas}

The [[proof]] ([below](#VerificationOfTopQuillen)) that def. \ref{ClassesOfMorhismsInTopQuillen} defines a [[model category]] structure involves two technical lemmas which concern the special nature of [[topological spaces]] ("point-set topology").  With these two lemmas in hand, the rest of the proof is a routine argument in model category theory.

+-- {: .num_lemma #CompactSubsetsAreSmallInCellComplexes}
###### Lemma

Assuming the [[axiom of choice]] and the [[law of excluded middle]],
every [[compact topological space|compact]] [[topological subspace|subspace]] of a topological [[cell complex]], def. \ref{TopologicalCellComplex}, intersects the [[interior]] of a [[finite number]] of cells.

=--

(e.g. [Hirschhorn 15, section 3.1](#Hirschhorn15))

+-- {: .proof}
###### Proof

So let $Y$ be a topological cell complex and $C \hookrightarrow Y$ a [[compact topological space|compact]] [[topological subspace|subspace]]. Define a subset 

$$
  P \subset Y
$$ 

by _choosing_ one point in the [[interior]] of the intersection with $C$ of each cell of $Y$ that intersects $C$.

It is now sufficient to show that $P$ has no [[accumulation point]]. Because, by the [[compact topological space|compactness]] of $X$, every non-finite subset of $C$ does have an accumulation point, and hence the lack of such shows that $P$ is a [[finite set]] and hence that $C$ intersects the interior of finitely many cells of $Y$.

To that end, let $c\in C$ be any point. If $c$ is a 0-cell in $Y$, write $U_c \coloneqq \{c\}$. Otherwise, write $e_c$ for the unique cell of $Y$ that contains $c$ in its [[interior]]. By construction, there is exactly one point of $P$ in the interior of $e_c$. Hence there is an [[open neighbourhood]] $c \in U_c \subset e_c$ containing no further points of $P$ beyond possibly $c$ itself, if $c$ happens to be that single point of $P$ in $e_c$.

It is now sufficient to show that $U_c$ may be enlarged to an open subset $\tilde U_c$ of $Y$ containing no point of $P$, except for possibly $c$ itself, for that means that $c$ is not an accumulation point of $P$.

To that end, let $\alpha_c$ be the [[ordinal]] that labels the stage $Y_{\alpha_c}$ of the [[transfinite composition]] in the [[cell complex]]-presentation of $Y$ at which the cell $e_c$ above appears. Let $\gamma$ be the ordinal of the full cell complex. Then define the set

$$
  T 
  \coloneqq
  \left\{
    \;
    (\beta, U)
    \;|\;
    \alpha_c \leq \beta \leq \gamma
    \;\,,\;
    U \underset{open}{\subset} Y_\beta
    \;\,,\;
    U \cap Y_\alpha = U_c
    \;\,,\;
    U \cap P \in \{ \emptyset, \{c\} \}
    \;
  \right\}
  \,,
$$

and regard this as a [[partially ordered set]] by declaring a partial ordering via

$$
  (\beta_1, U_1) \lt (\beta_2, U_2)
  \;\;\;\;
  \Leftrightarrow
  \;\;\;\;
  \beta_1 \lt \beta_2
  \;\,,\;
  U_2 \cap Y_{\beta_1} = U_1
  \,.
$$

This is set up such that every element $(\beta, U)$ of $T$ with $\beta$ the maximum value $\beta = \gamma$ is an extension $\tilde U_c$ that we are after. 

Observe then that for $(\beta_s, U_s)_{s\in S}$ a chain in $(T,\lt)$ (a subset on which the relation $\lt$ restricts to a [[total order]]), it has an upper bound in $T$ given by the [[union]] $({\cup}_s \beta_s ,\cup_s U_s)$. Therefore [[Zorn's lemma]] applies, saying that $(T,\lt)$ contains a [[maximal element]] $(\beta_{max}, U_{max})$.

Hence it is now sufficient to show that $\beta_{max} = \gamma$. We argue this by showing that assuming $\beta_{\max}\lt \gamma$ leads to a contradiction.

So assume $\beta_{max}\lt \gamma$. Then to construct an  element of $T$ that is larger than $(\beta_{max},U_{max})$, consider for each cell $d$ at stage $Y_{\beta_{max}+1}$ its attaching map $h_d \colon S^{n-1} \to Y_{\beta_{max}}$ and the corresponding preimage open set $h_d^{-1}(U_{max})\subset S^{n-1}$. Enlarging all these  preimages to open subsets of $D^n$ (such that their image back in $X_{\beta_{max}+1}$ does not contain $c$), then $(\beta_{max}, U_{max}) \lt (\beta_{max}+1, \cup_d U_d )$. This is a contradiction. Hence $\beta_{max} = \gamma$, and we are done.

=--

+-- {: .num_lemma #JTopRelativeCellComplexesAreWeakHomotopyEquivalences}
###### Lemma

Every $J_{Top}$-[[relative cell complex]] (def. \ref{TopologicalGeneratingAcyclicCofibrations}, def. \ref{TopologicalCCellComplex}) is a [[weak homotopy equivalence]], def. \ref{WeakHomotopyEquivalenceOfTopologicalSpaces}.

=--

+-- {: .proof}
###### Proof

Let $X \longrightarrow \hat X$ be a $J_{Top}$-relative cell complex. 

Notice that with the elements $D^n \hookrightarrow D^n \times I$ of $J_{Top}$ themselves, also each stage $X_{\alpha} \to X_{\alpha+1}$ in the [[transfinite composition]] defining $\hat X$ is a [[homotopy equivalence]], hence, by prop.  \ref{TopologicalHomotopyEquivalencesAreWeakHomotopyEquivalences}, a weak homotopy equivalence. 

This means that all morphisms in the following diagram (notationally suppressing basepoints and showing only the finite stages)

$$
  \array{
    \pi_n(X)
      &\overset{\simeq}{\longrightarrow}&
    \pi_n(X_1)
      &\overset{\simeq}{\longrightarrow}&
    \pi_n(X_2)
      &\overset{\simeq}{\longrightarrow}&
    \pi_n(X_3)
      &\overset{\simeq}{\longrightarrow}&
    \cdots
    \\
    & {}_{\mathllap{\simeq}}\searrow & 
      \downarrow^{\mathrlap{\simeq}}
    & \swarrow_{\mathrlap{\simeq}} & \cdots
    \\
    && \underset{\longleftarrow}{\lim}_\alpha \pi_n(X_\alpha)
  }
$$

are isomorphisms.

Moreover, lemma \ref{CompactSubsetsAreSmallInCellComplexes} gives that every representative and every null homotopy of elements in $\pi_n(\hat X)$ already exists at some finite stage $X_k$. This means that also the universally induced morphism

$$
  \underset{\longleftarrow}{\lim}_\alpha \pi_n(X_\alpha)
  \overset{\simeq}{\longrightarrow}
  \pi_n(\hat X)
$$

is an isomorphism. Hence the composite $\pi_n(X) \overset{\simeq}{\longrightarrow} \pi_n(\hat X)$ is an isomorphism.

=--



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

Finally, to see that $\pi_n(\hat X) \to \pi_n(X)$ is also surjective, hence bijective, observe that every element in $\pi_n(X)$ is equivalently represented by a commuting diagram of the form

$$
  \array{
    S^{n-1} &\longrightarrow& \ast &\longrightarrow& \hat X
    \\
    \downarrow && \downarrow && \downarrow
    \\
    D^n &\longrightarrow& X &=& X
  }  
  \,,
$$

and so here the lift gives a representative of a preimage in $\pi_{n}(\hat X)$.

**B) $I_{Top}$-[[injective morphisms]] are in particular Serre fibrations**

By lemma \ref{SaturationOfGeneratingCofibrations} an $I_{Top}$-[[injective morphisms]] has also the [[right lifting property]] against all [[relative cell complexes]], and hence by lemma \ref{TopologicalGeneratingAcyclicCofibrationsAreRelativeCellComplexes} it is also a $J_{Top}$-[[injective morphism]], hence a Serre fibration.

**C) Acyclic Serre fibrations are in particular $I_{Top}$-[[injective morphisms]]**


Let $f\colon X \to Y$ be a Serre fibration that induces isomorphisms
on homotopy groups. In degree 0 this means that $f$ is an isomorphism on [[connected components]], and this means that there is a lift in every [[commuting square]] of the form

$$
  \array{
    S^{-1} = \emptyset &\longrightarrow& X 
    \\
    \downarrow && \downarrow^{\mathrlap{f}}
    \\
    D^0 = \ast &\longrightarrow& Y
  }
$$

(this is $\pi_0(f)$ being surjective) and in every commuting square of the form

$$
  \array{
    S^0  &\longrightarrow& X 
    \\
    {}^{\mathllap{\iota_0}}\downarrow && \downarrow^{\mathrlap{f}}
    \\
    D^1 = \ast &\longrightarrow& Y
  }
$$

(this is $\pi_0(f)$ being injective). Hence we are reduced to showing that for $n \geq 2$ every diagram of the form

$$
  \array{
    S^{n-1}  &\overset{\alpha}{\longrightarrow}& X 
    \\
    {}^{\mathllap{\iota_n}}\downarrow && \downarrow^{\mathrlap{f}}
    \\
    D^n  &\overset{\kappa}{\longrightarrow}& Y
  }
$$

has a lift.  


To that end, pick a basepoint on $S^{n-1}$ and write $x$ and $y$ for its images in $X$ and $Y$, respectively 

Then the diagram above expresses that $f_\ast[\alpha] = 0 \in \pi_{n-1}(Y,y)$ and hence by assumption on $f$ it follows that $[\alpha] = 0 \in \pi_{n-1}(X,x)$, which in turn mean that there is $\kappa'$ making the upper triangle of our lifting problem commute:

$$
  \array{
    S^{n-1} &\overset{\alpha}{\longrightarrow}& X
    \\
    {}^{\mathllap{\iota_n}}\downarrow & \nearrow_{\mathrlap{\kappa'}}
    \\
    D^n
  }
  \,.
$$

It is now sufficient to show that any such $\kappa'$ may be deformed to a $\rho'$ which keeps making this upper triangle commute but also makes the remaining lower triangle commute.

To that end, notice that by the commutativity of the original square, we already have at least this commuting square:

$$
  \array{
    S^{n-1} &\overset{\iota_n}{\longrightarrow}& D^n
    \\
    {}^{\mathllap{\iota_n}}\downarrow && \downarrow^{\mathrlap{f \circ \kappa'}}
    \\
    D^n &\underset{\kappa}{\longrightarrow}& Y
  }
  \,.
$$

This induces the universal map $(\kappa,f \circ \kappa')$ from the [[pushout]] of its [[cospan]] in the top left, which is the [[n-sphere]] (see [this](Top#TopologicalnSphereIsPushoutOfBoundaryOfnBallInclusionAlongItself) example):

$$
  \array{
    S^{n-1} &\overset{\iota_n}{\longrightarrow}& D^n
    \\
    {}^{\mathllap{\iota_n}}\downarrow 
    &(po)& 
    \downarrow^{\mathrlap{f \circ \kappa'}}
    \\
    D^n &\underset{\kappa}{\longrightarrow}& S^n
    \\
    && & \searrow^{(\kappa,f \circ \kappa')}
    \\
    && && Y
  }
  \,.
$$

This universal morphism represents an element of the $n$th homotopy group:

$$
  [(\kappa,f \circ \kappa')]
   \in
  \pi_n(Y,y)
  \,.
$$

By assumption that $f$ is a weak homotopy equivalence, there is a $[\rho] \in \pi_{n}(X,x)$ with 

$$
  f_\ast [\rho] = [(\kappa,f \circ \kappa')]
$$ 

hence on representatives there is a lift up to homotopy

$$
  \array{
    && X
    \\
    &{}^{\mathllap{\rho}}\nearrow_{\mathrlap{\Downarrow}} & \downarrow^{\mathrlap{f}}
    \\
    S^n
    &\underset{(\kappa,f\circ \kappa')}{\longrightarrow}&
    Y
  }
  \,.
$$

Morever, we may always find $\rho$ of the form $(\rho', \kappa')$ for some $\rho' \colon D^n \to X$. ("Paste $\kappa'$ to the reverse of $\rho$.")

Consider then the map

$$
  S^n \overset{(f\circ \rho', \kappa)}{\longrightarrow} Y
$$

and observe that this represents the trivial class:

$$
  \begin{aligned}
    [(f \circ \rho', \kappa)]
    & =
    [(f\circ \rho', f\circ \kappa')]
     +
      [(f\circ \kappa', \kappa)]
    \\
    & = f_\ast \underset{= [\rho]}{\underbrace{[(\rho',\kappa')]}}
      +
        [(f\circ \kappa', \kappa)]
    \\
    & = [(\kappa,f \circ \kappa')]
      +
        [(f\circ \kappa', \kappa)]
    \\
    & = 0     
  \end{aligned}
  \,.
$$

This means equivalently that there is a homotopy

$$
  \phi \; \colon \; f\circ \rho' \Rightarrow \kappa
$$

fixing the boundary of the $n$-disk.

Hence if we denote homotopy by double arrows, then we have now achieved the following situation

$$
  \array{
    S^{n-1} &\overset{\alpha}{\longrightarrow}& X
    \\
    {}^{\mathllap{\iota_n}}\downarrow 
    & 
      {}^{\rho'}\nearrow_{\Downarrow^{\phi}}
    &
    \downarrow^{\mathrlap{f}}
    \\
    D^n &\longrightarrow& Y
  }
$$

and it now suffices to show that $\phi$ may be lifted to a homotopy of just $\rho'$, fixing the boundary, for then the resulting homotopic $\rho''$ is the desired lift.

To that end, notice that the condition that $\phi \colon D^n \times I \to Y$ fixes the boundary of the $n$-disk means equivalently that it extends to a morphism

$$
  S^{n-1} \underset{S^{n-1}\times I}{\sqcup} D^n \times I
  \overset{(f\circ \alpha,\phi)}{\longrightarrow}
  Y
$$

out of the [[pushout]] that identifies in the cylinder over $D^n$ all points lying over the boundary. Hence we are reduced to finding a lift in 

$$
  \array{
    D^n &\overset{\rho'}{\longrightarrow}& X 
    \\
    \downarrow && \downarrow^{\mathrlap{f}}
    \\
    S^{n-1}\underset{S^{n-1}\times I}{\sqcup} D^n \times I
    &\overset{(f\circ \alpha,\phi)}{\longrightarrow}&
    Y
  }
  \,.
$$

But inspection of the left map reveals that it is homeomorphic again to $D^n \to D^n \times I$, and hence the lift does indeed exist.


=--

### Verification of the axioms
 {#VerificationOfTopQuillen}

We use the lemmas [above](#TechnicalLemmas) to prove that the classes of morphisms in def. \ref{ClassesOfMorhismsInTopQuillen} satify the conditions for a [[model category]] structure on the category [[Top]].

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
    \stackrel{\in Cof}{\longrightarrow}
  \hat X
    \stackrel{\in W \cap Fib}{\longrightarrow}
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
   \stackrel{\in Cof}{\longrightarrow}
  \hat X
   \stackrel{\in I_{top} Inj}{\longrightarrow}
  Y
  \,.
$$

By lemma \ref{AcyclicSerreFibrationsAreTheJTopFibrations} the map $\hat X \to Y$ is both a weak equivalence as well as a Serre fibration.

=--


+-- {: .num_prop #ContinuousFunctionsFactorAsQuillenAcyclicCofibrationFollowedBySerreFibration}
###### Proposition

Every morphism $f\colon X \longrightarrow Y$ in [[Top]] factors as an acyclic classical cofibration followed by a classical fibration, def. \ref{ClassesOfMorhismsInTopQuillen}:

$$
  f
  \;\colon\;
  X 
    \stackrel{\in W \cap Cof}{\longrightarrow}
  \hat X
    \stackrel{\in Fib}{\longrightarrow}
  Y
  \,.
$$

=--

+-- {: .proof}
###### Proof

By lemma \ref{CompactSubsetsAreSmallInCellComplexes}
the set $J_{Top} = \{D^n \hookrightarrow D^n\times I\}$ of 
topological [[generating acyclic cofibrations]], def. \ref{TopologicalGeneratingAcyclicCofibrations}, has small domains, in the sense of def. \ref{ClassOfMorphismsWithSmallDomains} (the [[n-disks]] are [[compact topological space|compact]]). Hence by the [[small object argument]], prop. \ref{SmallObjectArgument}, $f$ factors as an $J_{Top}$-relative cell complex, followed by an $J_{top}$-[[injective morphisms]], def. \ref{RightLiftingProperty}:

$$
  f
  \;\colon\;
  X 
   \stackrel{\in J_{Top} Cell}{\longrightarrow}
  \hat X
    \stackrel{\in J_{Top} Inj}{\longrightarrow}
  Y
  \,.
$$

By definition this makes $\hat X \to Y$ a [[Serre fibration]], hence a fibration.

By lemma \ref{TopologicalGeneratingAcyclicCofibrationsAreRelativeCellComplexes} a relative $J_{Top}$-cell complex is in particular a relative $I_{Top}$-cell complex. Hence $X \to \hat X$ is a cofibration. By lemma \ref{JTopRelativeCellComplexesAreWeakHomotopyEquivalences} it is also a weak equivalence.

=--

+-- {: .num_prop #LiftingPropertyInTheClassicalModelStructureOnTopologicalSpaces}
###### Proposition

Every [[commuting diagram|commuting square]] in [[Top]] with the left morphism a classical cofibration and the right morphism a fibration, def. \ref{ClassesOfMorhismsInTopQuillen}

$$
  \array{
    &\longrightarrow&
    \\
    {}^{\mathllap{{g \in} \atop { Cof}}}\downarrow && \downarrow^{\mathrlap{{f \in }\atop Fib}}
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
  g \;\colon\; \stackrel{\in J_{Top} Cell}{\longrightarrow} \stackrel{\in Fib}{\longrightarrow}
  \,,
$$

as in the proof of prop. \ref{ContinuousFunctionsFactorAsQuillenAcyclicCofibrationFollowedBySerreFibration}. Now by [[two-out-of-three]], prop. \ref{QuillenWeakEquivalencesSatisfyTwoOutOfThree}, the factorizing fibration is actually an acyclic fibration. By case A), this acyclic fibration has the [[right lifting property]] against the cofibration $g$ itself, and so the [[retract argument]], lemma \ref{RetractArgument} gives that $g$  is a [[retract]] of a relative $J_{Top}$-cell complex. With this, finally lemma \ref{SaturationOfGeneratingCofibrations} implies that $f$ has the [[right lifting property]] against $g$.

=--

Finally:

+-- {: .num_prop #LiftingExhausted}
###### Proposition

The systems $(Cof , W \cap Fib)$ and $(\W \cap Cof, Fib)$ are [[weak factorization systems]].

=--

+-- {: .proof}
###### Proof

We have already seen the factorization and the lifting property, it remains to see that the given left/right classes exhaust the class of morphisms with the given lifting property. 

For the fibrations this is by definition, for the the acyclic fibrations this is by lemma \ref{AcyclicSerreFibrationsAreTheJTopFibrations}.

The remaining statement for $Cof$ and $W\cap Cof$ follows from a general argument ([here](cofibrantly+generated+model+category#RetractsOfCellComplexesExchaustLLPOfRLP)) for [[cofibrantly generated model categories]]:

So let $f \colon X \longrightarrow Y$ be in $(I_{Top} Inj) Proj$, we need to show that then $f$ is a retract of a relative cell complex. To that end, apply the [[small object]] argument to factor $f$ as 

$$
  f \;\colon \; X \overset{}{\longrightarrow} \hat Y \overset{\in I Inj}{\longrightarrow} Y
  \,.
$$

It follows that $f$ has the left lefting property again $\hat Y \to Y$, and hence by the [[retract argument]] it is a retract of $X \to \hat Y$, which proves the claim for $Cof$.

The argument for $W \cap Cof$ is analogous, using the [[small object argument]] now for $J_{Top}$.


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


### The homotopy category

We may now pass to the [[homotopy category of a model category]] and find [[Ho(Top)]] the "[[classical homotopy category]]" (or maybe "Quillen-Serre homotopy category"). For discussion of the [[Quillen equivalence]] to the [[classical model structure on simplicial sets]] (the "[[homotopy hypothesis]]"), see there.

+-- {: .num_remark} 
###### Remark

Theorem \ref{TopQuillenModelStructure} in itself implies only that every topological space is weakly equivalent to a [[retract]] of a [[cell complex]], def. \ref{TopologicalCellComplex}. But by the existence of [[CW approximations]], every topological space is weakly homotopy equivalent even to a [[CW complex]]. In particular, by the [[Quillen equivalence]] to the [[Quillen model structure on simplicial sets]], every topological space is weakly homotopy equivalent to the [[geometric realization]] of its [[singular simplicial complex]] (and every geometric realization of a [[simplicial set]] is (by [this proposition](geometric+realization#mono)) a [[CW-complex]], def. \ref{TopologicalCellComplex}.

=--

## Properties

+-- {: .num_prop #Properness}
###### Proposition

The model categories $Top_{Quillen}$ and $(Top^{\ast/})_{Quillen}$ are [[proper model categories]].

=--

([Hirschhorn 02,theorem 13.1.10](model+category#Hirschhorn02))

Right properness is immediate from the fact that all objects are fibrant. Left properness needs an argument. First check that weak equivalences are preserved under pushout of inclusion maps along cell attachments. Then use that a general cofibration is a retract a relative cell complex inclusion. Observe that if weak equivalences are preserved under pushout along some class of morphisms, then also under pushout along retracts of these. Hence reduce to pushout along relative cell complexes. By the first statement these are a transfinite pasting composite along pushouts that preserve weak equivalences.


## Related model structures
 {#RelatedModelStructures}

We discuss various further [[model category]] structures whose existence follows by immediate variation of the above proof of theorem \ref{TopQuillenModelStructure}:

* [The model structure on pointed topological spaces](#ModelstructureOnPointedTopologicalSpaces);

* [The model structure on compactly generated topological spaces](#ModelStructureOnCompactlyGeneratedTopologicalSpaces);

* [The model structure on topologically enriched functors](#ModelStructureOnTopEnrichedFunctors).


### Classical model structure on pointed topological spaces
 {#ModelstructureOnPointedTopologicalSpaces}

Every [[coslice category]] $\mathcal{C}^{X/}$ of a [[model category]] $\mathcal{C}$ inherits the [[coslice model structure]], whose classes of morphisms are those of $\mathcal{C}$ as seen by the [[forgetful functor]] $U \colon \mathcal{C}^{X/}\longrightarrow \mathcal{C}$.

Accordingly there is the induced [[classical model structure on pointed topological spaces]] $Top^{\ast/}_{Quillen}$.

+-- {: .num_defn #BasePointAdjoined}
###### Definition

Let $\mathcal{C}$ be a [[category]] with [[terminal object]] and [[finite colimits]]. Then the [[forgetful functor]] $U \colon \mathcal{C}^{\ast/} \to \mathcal{C}$ from its [[category of pointed objects]], def. \ref{CategoryOfPointedObjects}, has a [[left adjoint]] 

$$
  \mathcal{C}^{\ast/}
     \underoverset
       {\underset{U}{\longrightarrow}}
       {\overset{(-)_+}{\longleftarrow}}
       {\bot}
  \mathcal{C}
$$

given by forming the [[disjoint union]] ([[coproduct]]) with a base point ("adjoining a base point").

=--

+-- {: .num_prop #LimitsAndColimitsOfPointedObjects}
###### Proposition

Let $\mathcal{C}$ be a [[category]] with all [[limits]] and [[colimits]]. Then also the [[category of pointed objects]] $\mathcal{C}^{\ast/}$, def. \ref{CategoryOfPointedObjects}, has all limits and colimits.

Moreover:

1. the limits are the limits of the underlying diagrams in $\mathcal{C}$, with the base point of the limit induced by its universal property in $\mathcal{C}$;

1. the colimits are the limits in $\mathcal{C}$ of the diagrams _with the basepoint adjoined_.

=--

+-- {: .proof}
###### Proof

It is immediate to check the relevant [[universal property]]. For details see at _[slice category -- limits and colimits](overcategory#LimitsAndColimits)_.

=--

+-- {: .num_example #WedgeSumAsCoproduct}
###### Example

Given two pointed objects $(X,x)$ and $(Y,y)$, then:

1. their [[product]] in $\mathcal{C}^{\ast/}$ is simply $(X\times Y, (x,y))$;

1. their [[coproduct]] in $\mathcal{C}^{\ast/}$ has to be computed using the second clause in prop. \ref{LimitsAndColimitsOfPointedObjects}: since the point $\ast$ has to be adjoined to the diagram, it is given not by the coproduct in $\mathcal{C}$, but by the [[pushout]] in $\mathcal{C}$ of the form:

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

Generally for a set $\{X_i\}_{i \in I}$ in $Top^{\ast/}$

1. their [[product]] is formed in $Top$ as in example \ref{ProductTopologicalSpace}, with the new basepoint canonically induced;

1. their [[coproduct]] is formed by the [[colimit]] in $Top$ over the diagram with a basepoint adjoined, and is called the [[wedge sum]] $\vee_{i \in I} X_i$.

=--

+-- {: .num_example}
###### Example

For $X$ a [[CW-complex]], def. \ref{TopologicalCellComplex} then for every $n \in \mathbb{N}$ the [[quotient]] (example \ref{QuotientSpaceAsPushout}) of its $n$-skeleton by its $(n-1)$-skeleton is the [[wedge sum]], def. \ref{WedgeSumAsCoproduct}, of $n$-spheres, one for each $n$-cell of $X$:

$$
  X^n / X^{n-1} \simeq \underset{i \in I_n}{\vee} S^n
  \,.
$$

=--


+-- {: .num_defn #SmashProductOfPointedObjects}
###### Definition

For $\mathcal{C}^{\ast/}$ a [[category of pointed objects]] with [[finite limits]] and [[finite colimits]], the _[[smash product]]_ is the [[functor]]

$$
  (-)\wedge(-)
  \;\colon\;
  \mathcal{C}^{\ast/}
  \times 
  \mathcal{C}^{\ast/}
  \longrightarrow
  \mathcal{C}^{\ast/}
$$

given by

$$
  X \wedge Y
  \;\coloneqq\;
  \ast
  \underset{X\sqcup Y}{\sqcup} (X \times Y)
  \,,
$$

hence by the [[pushout]] in $\mathcal{C}$

$$
  \array{
    X \sqcup Y &\overset{(id_X,y),(x,id_Y) }{\longrightarrow}& X \times Y
    \\
    \downarrow && \downarrow
    \\
    \ast &\longrightarrow& X \wedge Y
  }
  \,.
$$

In terms of the [[wedge sum]] from def. \ref{WedgeSumAsCoproduct}, this may be written concisely as

$$
  X \wedge Y = \frac{X\times Y}{X \vee Y}
  \,.
$$
 
=--

+-- {: .num_remark #SmashProductOnTopNotAssociative}
###### Remark

For a general category $\mathcal{C}$ in def. \ref{SmashProductOfPointedObjects}, the [[smash product]] need not be [[associativity|associative]], namely it fails to be associative if the functor $(-)\times Z$ does not preserve the [[quotients]] involved in the definition. 

In particular this may happen for $\mathcal{C} = $ [[Top]].

A sufficient condition for $(-) \times Z$ to preserve quotients is that it is a [[left adjoint]] functor. This is the case in the smaller subcategory of [[compactly generated topological spaces]], we come to this in prop. \ref{SmashProductInTopcgIsAssociative} below. 



=--

These two operations are going to be ubiquituous in [[stable homotopy theory]]:

| symbol | name | category theory |
|--------|------|-----------------|
| $X \vee Y$ | [[wedge sum]] | [[coproduct]] in $\mathcal{C}^{\ast/}$ |
| $X \wedge Y$ | [[smash product]] | [[tensor product]] in $\mathcal{C}^{\ast/}$|


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

Let $\mathcal{C}^{\ast/} = Top^{\ast/}$ be [[pointed topological spaces]]. Then 

$$
  I_+ \in Top^{\ast/}
$$

denotes the standard interval object $I = [0,1]$ from def. \ref{TopologicalInterval}, with a djoint basepoint adjoined, def. \ref{BasePointAdjoined}. Now for $X$ any [[pointed topological space]], then 

$$
  X \wedge (I_+) = (X \times I)/(\{x_0\} \times I)
$$

is the **[[reduced cylinder]]** over $X$: the result of forming the ordinary cyclinder over $X$ as in def. \ref{TopologicalInterval}, and then identifying the interval over the basepoint of $X$ with the point.

(Generally, any construction in $\mathcal{C}$ properly adapted to pointed objects $\mathcal{C}^{\ast/}$ is called the "reduced" version of the unpointed construction. Notably so for "[[reduced suspension]]" which we come to [below](#MappingCones).)


Just like the ordinary cylinder $X\times I$ receives a canonical injection from the [[coproduct]] $X \sqcup X$ formed in $Top$, so the reduced cyclinder receives a canonical injection from the coproduct $X \sqcup X$ formed in $Top^{\ast/}$, which is the [[wedge sum]] from example \ref{WedgeSumAsCoproduct}:

$$
  X \vee X \longrightarrow X \wedge (I_+)
  \,.
$$

=--

+-- {: .num_example #PointedMappingSpace}
###### Example

For $(X,x),(Y,y)$ [[pointed topological spaces]] with $Y$ a [[locally compact topological space]], then the **[[pointed mapping space]]** is the [[topological subspace]] of the [[mapping space]] of def. \ref{CompactOpenTopology}

$$
  Maps((Y,y),(X,x))_\ast
    \hookrightarrow
  (X^Y, const_x)
$$

on those maps which preserve the basepoints, and pointed by the map constant on the basepoint of $X$.

In particular, the **standard topological pointed path space object** on some pointed $X$ (the pointed variant of def. \ref{TopologicalPathSpace}) is the pointed mapping space $Maps(I_+,X)_\ast$.

The pointed consequence of prop. \ref{MappingTopologicalSpaceIsExponentialObject} then gives that there is a [[natural bijection]]

$$
  Hom_{Top^{\ast/}}((Z,z) \wedge (Y,y), (X,x))
  \simeq
  Hom_{Top^{\ast/}}((Z,z), Maps((Y,y),(X,x))_\ast)
$$

between basepoint-preserving continuous functions out of a [[smash product]], def. \ref{SmashProductOfPointedObjects}, with pointed continuous functions of one variable into the pointed mapping space.

=--



+-- {: .num_defn #GeneratingCofibrationsForPointedTopologicalSpaces}
###### Definition

Write

$$
  I_{Top^{\ast/}}
  = 
 \left\{
    S^{n-1}_+ \overset{(\iota_n)_+}{\longrightarrow} D^n_+
 \right\}
  \;\;
  \subset Mor(Top^{\ast/})
$$

and

$$
  J_{Top^{\ast/}}
  = 
 \left\{
    D^n_+ \overset{(id, \delta_0)_+}{\longrightarrow} (D^n \times I)_+
 \right\}
  \;\;\;
  \subset Mor(Top^{\ast/})
 \,,
$$

respectively, for the classes of morphisms obtained from the classical generating cofibrations, def. \ref{TopologicalGeneratingCofibrations}, and the classical generating acyclic cofibrations, def. \ref{TopologicalGeneratingAcyclicCofibrations}, under adjoining of basepoints.

=--

+-- {: .num_theorem #CofibrantGenerationOfPointedTopologicalSpaces}
###### Theorem

The classes in def. \ref{GeneratingCofibrationsForPointedTopologicalSpaces} exhibit the [[classical model structure on pointed topological spaces]], $Top^{\ast/}_{Quillen}$ as a [[cofibrantly generated model category]].

=--

This is a special case of a general statement about cofibrant generation of [[coslice model structures]], see [this proposition](model+structure+on+an+over+category#ModelStructureInheritsGoodProperties). But it also follows by a proof directly analogous to that of theorem \ref{TopQuillenModelStructure}:

+-- {: .proof}
###### Proof

Due to the fact that in $J_{Top^{\ast/}}$ a basepoint is freely adjoined, lemma \ref{AcyclicSerreFibrationsAreTheJTopFibrations} goes through verbatim for the pointed case, with $J_{Top}$ replaced by $J_{Top^{\ast/}}$, as do the other two lemmas above that depend on point-set topology, lemma \ref{CompactSubsetsAreSmallInCellComplexes} and lemma \ref{JTopRelativeCellComplexesAreWeakHomotopyEquivalences}. With this, the rest of the proof follows by the same general abstract reasoning as [above](#VerificationOfTopQuillen) in the proof of theorem \ref{TopQuillenModelStructure}.

=--

### Model structure on compactly generated topological spaces
 {#ModelStructureOnCompactlyGeneratedTopologicalSpaces}

The category [[Top]] has the technical inconvenience that [[mapping spaces]] $X^Y$ (def. \ref{CompactOpenTopology}) exist only for $Y$ a [[locally compact topological space]] but fail to exist more generally. In other words: [[Top]] is not [[cartesian closed category|cartesian closed]]. But cartesian closure is necessary for some purposes of homotopy theory, for instance it ensures that

1. the [[smash product]] on [[pointed topological spaces]] is [[associative]];

1. there is a concept of [[topologically enriched functors]] with values in topological spaces, to which we turn [below](#ModelStructureOnTopEnrichedFunctors).

1. [[geometric realization]] of [[simplicial sets]] preserves [[products]].

Now, since, by the above, the [[homotopy theory]] of topological spaces only cares about the [[CW approximation]] to any topological space, it is plausible to ask for a [[full subcategory]] of [[Top]] which still contains all [[CW-complexes]], still has all [[limits]] and [[colimits]], still supports a model category structure constructed in the same way as above, but which in addition is [[cartesian closed category|cartesian closed]], and preferably such that the model structure interacts well with the cartesian closure.

Such a full subcategory exists, the category of [[compactly generated topological spaces]]. This we briefly describe now.

+-- {: .num_defn #kTop}
###### Definition

Let $X$ be a [[topological space]].

A subset $A \subset X$ is called **$k$-closed** if for every [[continuous function]] $\phi \colon K \longrightarrow X$ out of a [[compact topological space|compact]] [[Hausdorff topological space|Hausdorff]] $K$, then the [[preimage]] $\phi^{-1}(A)$ is a [[closed subset]] of $K$.

$X$ is called **[[compactly generated topological space|compactly generated]]** if its closed subsets exhaust (hence coincide with) the $k$-closed subsets.

Write

$$
  Top_{cg} \hookrightarrow Top
$$

for the [[full subcategory]] of [[Top]] on the compactly generated topological spaces.

=--

+-- {: .num_defn #kfication}
###### Definition

Write

$$
  Top \overset{k}{\longrightarrow} Top_{cg} \hookrightarrow Top
$$

for the [[functor]] which sends any [[topological space]] $X = (S,\tau)$ to the  topological space with the same underlying set $S$, but with open subsets $k \tau$ the collection of all $k$-open subsets.

=--


+-- {: .num_lemma #ContinuousFunctionsOutOfCompactlyGeneratedFactorThroughCompactlyGeneratedClosureOfCodomain}
###### Lemma

Let $X \in Top_{cg} \hookrightarrow Top$ (def. \ref{kTop}) and let $Y\in Top$. Then [[continuous functions]]

$$
  X \longrightarrow Y
$$

are also continuous when regarded as a function

$$
  X \longrightarrow k(Y)
$$

with $k$ from def. \ref{kfication}.

=--

+-- {: .proof}
###### Proof

We need to show that for $A \subset Y$ a $k$-closed subset, then $f^{-1}(A) \subset X$ is closed subset. 

Let $\phi \colon K \longrightarrow X$ be any continuous function out of a compact Hausdorff space $K$. Since $A$ is $k$-closed by assumption, we have that $(f \circ \phi)^{-1}(A) = \phi^{-1}(f^{-1}(A))\subset K$ is closed in $K$. This means that $f^{-1}(A)$ is $k$-closed in $X$. But by the assumption that $X$ is compactly generated, it follows that $f^{-1}(A)$ is already closed.

=--

+-- {: .num_cor #kTopIsCoreflectiveSubcategory}
###### Corollary

For $X \in Top_{cg}$ there is a [[natural bijection]]

$$
  Hom_{Top}(X,Y) \simeq Hom_{Top_{cg}}(X, k(Y))
  \,,
$$

which means equivalently that the functor $k$ (def. \ref{kfication}) together with the inclusion from def. \ref{kTop} forms an pair of [[adjoint functors]]

$$
  Top_{cg}
    \stackrel{\hookrightarrow}{\underoverset{k}{\bot}{\longleftarrow}}
  Top
  \,.
$$

This in turn means equivalently that $Top_{cg} \hookrightarrow Top$ is a [[coreflective subcategory]] with coreflector $k$. In particular $k$ is [[idempotent monad|idemotent]] in that there are [[natural isomorphisms|natural]] [[homeomorphisms]]

$$
  k(k(X))\simeq k(X)
  \,.
$$

Hence [[colimits]] in $Top_{cg}$ exists and are computed as in [[Top]]. Also [[limits]] in $Top_{cg}$ exists, these are obtained by computing the limit in [[Top]] and then applying the functor $k$ to the result.

=--

+-- {: .num_defn #CompactlyGeneratedMappingSpaces}
###### Definition

For $X, Y \in Top_{cg}$ (def. \ref{kTop}) the **compactly generated mapping space** $X^Y \in Top_{cg}$ is the [[compactly generated topological space]] whose underlying set is the set $C(X,Y)$ of [[continuous functions]] $f \colon X \to Y$, and for which a [[topological base|subbase]] for its topology has elements $U^\kappa$, for $U \subset Y$ any [[open subset]] and $\kappa \colon K \to X$ a [[continuous function]] out of a [[compact topological space|compact]] [[Hausdorff space]] $K$ given by

$$
  U^\kappa \coloneqq \left\{ f\in C(X,Y) | f(\kappa(K)) \subset U \right\}
  \,.
$$

=--


+-- {: .num_prop #CartesianClosureOfTopcg}
###### Proposition

The category $Top_{cg}$ (def. \ref{kTop}) is [[cartesian closed category|cartesian closed]]: 

for every $X \in Top_{cg}$ then the operation $X\times (-) \times (-)\times X$ of forming the Cartesian product in $Top_{cg}$ (which by cor. \ref{kTopIsCoreflectiveSubcategory} is $k$ applied to the usual [[product topological space]]) together with the operation $(-)^X$ of forming the compactly generated [[mapping space]] (def. \ref{CompactlyGeneratedMappingSpaces}) forms a pair of [[adjoint functors]]

$$
  Top_{cg}
  \underoverset
    {\underset{(-)^X}{\longrightarrow}}
    {\overset{X \times (-)}{\longleftarrow}}
    {\;\;\;\; \bot \;\;\;\;}
  Top_{cg}
  \,.
$$

=--

e.g. ([Strickland 09, prop. 2.12](#Strickland09))

Due to the [[idempotent monad|idempotency]] $k \circ k \simeq k$ (cor. \ref{kTopIsCoreflectiveSubcategory}) it is useful to know plenty of conditions under which a given topological space is already compactly generated, for then applying $k$ to it does not change it.

+-- {: .num_example #CWComplexIsCompactlyGenerated}
###### Example

Every [[CW-complex]] is [[compactly generated topological space|compactly generated]]. 

=--

+-- {: .proof}
###### Proof

Since [[a CW-complex is a Hausdorff space]], by prop. \ref{HausdorffImpliessWeaklyHausdorff} and  prop. \ref{CharacterizationOfCompactClosedSetsInWeaklyHausdorffSpace} its $k$-closed subsets are precisely those whose intersection with every [[compact subspace]] is closed. 

Since a CW-complex $X$ is a [[colimit]] in [[Top]] over attachments of standard [[n-disks]] $D^{n_i}$ (its cells), by the characterization of colimits in $Top$ ([prop.](Top#DescriptionOfLimitsAndColimitsInTop)) a subset of $X$ is open or closed precisely if its restriction to each cell is open or closed, respectively. Since the $n$-disks are compact, this implies one direction: if a subset $A$ of $X$ intersected with all compact subsets is closed, then $A$ is closed. 

For the converse direction, since [[a CW-complex is a Hausdorff space]] and since [[compact subspaces of Hausdorff spaces are closed]], the intersection of a closed subset with a compact subset is closed.

=--

+-- {: .num_example}
###### Example

The category $Top_{cg}$ of [[compactly generated topological spaces]] includes

1. all [[locally compact topological spaces]]

1. all [[first-countable topological spaces]]

   hence in particular

   1. all [[metrizable topological spaces]]

   1. all [[discrete topological spaces]]

   1. all [[codiscrete topological spaces]]

=--

([Lewis 78, p. 148](#Lewis78))

Recall that by corollary \ref{kTopIsCoreflectiveSubcategory}, all [[colimits]] of compactly generated spaces are again compactly generated.

+-- {: .num_example #ProductOfCWWithLocallyCompactCWIsCompactlyGenerated}
###### Example

The [[product topological space]] of a [[CW-complex]] with a [[compact topological space|compact]] CW-complex is [[compactly generated topological space|compactly generated]].

=--

([Hatcher "Topology of cell complexes", theorem A.6](CW+complex#HatcherTopologyOfCellComplexes))

More generally:

+-- {: .num_prop }
###### Proposition

The [[product topological space]] of a [[compactly generated topological space]] with a [[locally compact topological space|locally compact]] [[Hausdorff topological space]] is itself compactly generated.

=--

([Strickland 09, prop. 2.6](#Strickland09))

+-- {: .num_prop #kificationComparisonIsWeakHomotopyEquivalence}
###### Proposition

For every topological space $X$, the canonical function $k(X) \longrightarrow X$ is a [[weak homotopy equivalence]].

=--

+-- {: .proof}
###### Proof

By example \ref{CWComplexIsCompactlyGenerated}, example \ref{ProductOfCWWithLocallyCompactCWIsCompactlyGenerated} and lemma \ref{ContinuousFunctionsOutOfCompactlyGeneratedFactorThroughCompactlyGeneratedClosureOfCodomain}, continuous functions $S^n \to k(X)$ and their left homotopies $S^n \times I \to k(X)$ are in bijection with functions $S^n \to X$ and their homotopies $S^n \times I \to X$.

=--


+-- {: .num_theorem #ModelStructureOnTopcg} 
###### Theorem
**([[model structure on compactly generated topological spaces]])**

The restriction of the [[model category]] structure on $Top_{Quillen}$ from theorem \ref{TopQuillenModelStructure} along the inclusion $Top_{cg} \hookrightarrow Top$ of def. \ref{kTop} is still a [[model category]] structure, which is [[cofibrantly generated model category|cofibrantly generated]] by the same sets $I_{Top}$ (def. \ref{TopologicalGeneratingCofibrations}) and $J_{Top}$ (def. \ref{TopologicalGeneratingAcyclicCofibrations}). The [[k-ification]] coreflection of cor. \ref{kTopIsCoreflectiveSubcategory} is a  [[Quillen equivalence]]

$$
  Top_{cg, Quillen}
    \stackrel{\hookrightarrow}{\underoverset{k}{\bot}{\longleftarrow}}
  Top_{Quillen}
  \,.
$$

=--

+-- {: .proof}
###### Proof

By example \ref{CWComplexIsCompactlyGenerated}, the sets $I_{Top}$ and $J_{Top}$ are indeed in $Mor(Top_{cg})$. By example \ref{ProductOfCWWithLocallyCompactCWIsCompactlyGenerated} all arguments above about left homotopies between maps out of these basic cells go through verbatim in $Top_{cg}$. Hence the three technical lemmas above depending on actual point-set topology,  topology, lemma \ref{CompactSubsetsAreSmallInCellComplexes}, lemma \ref{JTopRelativeCellComplexesAreWeakHomotopyEquivalences} and lemma \ref{AcyclicSerreFibrationsAreTheJTopFibrations}, go through verbatim as before. Accordingly, since the remainder of the proof of theorem \ref{TopQuillenModelStructure} of $Top_{Quillen}$ follows by general abstract arguments from these, it also still goes through verbatim for $(Top_{cg})_{Quillen}$.

Hence the (acyclic) cofibrations in $(Top_{cg})_{Quillen}$ are identified with those in $Top_{Quillen}$, and so the inclusion is a part of a [[Quillen adjunction]]. To see that this is a [[Quillen equivalence]], it is sufficient to check that for $X$ a compactly generated space then a continuous function $f \colon X \longrightarrow Y$ is a [[weak homotopy equivalence]] (def. \ref{WeakHomotopyEquivalenceOfTopologicalSpaces}) precisely if the [[adjunct]] $\tilde f \colon X \to k(Y)$ is a weak homotopy equivalence. But, by lemma \ref{ContinuousFunctionsOutOfCompactlyGeneratedFactorThroughCompactlyGeneratedClosureOfCodomain}, $\tilde f$ is the same function as $f$, just considered with different codomain. Hence the result follows with prop. \ref{kificationComparisonIsWeakHomotopyEquivalence}.

=--


#### Pointed compactly generated topological spaces

Moreover:

+-- {: .num_prop}
###### Proposition

Write $Top_{cg}^{\ast/}$ for the category of [[pointed topological space|pointed]] [[compactly generated topological spaces]] (def. \ref{kTop}). Then the [[smash product]]

$$
  (-)\wedge (-)
  \;\colon\;
  Top_{cg}^{\ast/}
    \times
  Top_{cg}^{\ast/}
    \longrightarrow
  Top_{cg}^{\ast/}
$$

is [[associativity|associative]] and the [[0-sphere]] is a [[tensor unit]] for it, hence $(Top_{cg}^{\ast/}, \wedge, S^0)$ is a [[symmetric monoidal category]].

Moreover together with the [[pointed mapping space]] version $(-)_\ast^X$ of the compactly generated mapping space of def. \ref{CompactlyGeneratedMappingSpaces}, $Top_{cg}^{\ast/}$ becomes a [[closed monoidal category]]: 

for every $X \in Top_{cg}^{\ast/}$ then the operations of forming the [[smash product]] $X\wedge (-)$ and of forming the [[pointed mapping space]] $(-)_\ast^X$ constitute a pair of [[adjoint functors]]

$$
  Top_{cg}^{\ast/}
    \stackrel{\overset{X \wedge (-)}{\longleftarrow}}{\underset{(-)_\ast^X}{\longrightarrow}}
  Top_{cg}^{\ast/}
 \,.
$$
 
=--

+-- {: .proof}
###### Proof

For the first statement, since $(-)\times X$ is a [[left adjoint]] by prop. \ref{CartesianClosureOfTopcg}, it presevers [[colimits]] and in particular [[quotient space]] projections. Therefore with $X, Y, Z \in Top_{cg}^{\ast/}$ then

$$
  \begin{aligned}
    (X \wedge Y) \wedge Z
    & =
    \frac{
      \frac{X\times Y}{X \times\{y\} \sqcup \{x\}\times Y}
      \times Z
    }{ (X \wedge Y)\times \{z\} \sqcup \{[x] = [y]\} \times Z}
    \\
    & \simeq
    \frac{\frac{X \times Y \times Z}{X \times \{y\}\times Z \sqcup \{x\}\times Y \times Z}}{
      X \times Y \times \{z\}
    }
   \\
   &\simeq
    \frac{X\times Y \times Z}{ X \vee Y \vee Z}
  \end{aligned}
  \,.
$$

The analogous reasoning applies to yield also $X \wedge (Y\wedge Z) \simeq \frac{X\times Y \times Z}{ X \vee Y \vee Z}$.

=--



#### Compactly generated weakly Hausdorff spaces

While the inclusion $Top_{cg} \hookrightarrow Top$ [above](#ModelStructureOnCompactlyGeneratedTopologicalSpaces) does satisfy the requirement that it gives a [[cartesian closed category]] with all [[limits]] and [[colimits]] and containing all [[CW-complexes]], one may ask for yet smaller subcategories that still share all these properties but potentially exhibit further convenient properties still.

One may in addition demand all compactly generated spaces to be [[Hausdorff topological spaces]] (e. g. [Hirschhorn 15, top of p. 2](#Hirschhorn15)) and use Hausdorff reflection (in addition to reflection onto compactly generated spaces) to make [[colimits]] land again in Hausdorff space.

A morre popular choice introduced in ([McCord 69](weakly+Hausdorff+topological+space#McCord69)) is _weak Hausdorffness_, i.e. to add the further restriction to topopological spaces which are not only compactly generated but also [[weakly Hausdorff topological space|weakly Hausdorff]]. This was motivated from ([Steenrod 67](compactly+generated+topological+space#Steenrod67)) where compactly generated Hausdorff spaces were used by the observation ([McCord 69, section 2](weakly+Hausdorff+topological+space#McCord69)) that Hausdorffness is not preserved my many colimit operations, notably not by forming [[quotient spaces]]. 

On the other hand, in the above we wouldn't have imposed Hausdorffness in the first place. Possibly more intrinsic advantages of $Top_{cgwH}$ over $Top_{cg}$ are the following:

* every [[pushout]] of a morphism in $Top_{cgwH} \hookrightarrow Top$ along a [[closed subspace]] inclusion in $Top$ is again in $Top_{cgwH}$ ([MO comment by Peter May](http://mathoverflow.net/a/204221/381))

* in $Top_{cgwH}$ quotient spaces are not only preserved by [[cartesian products]] (as is the case for all compactly generated spaces due to $X\times (-)$ being a left adjoint, according to cor. \ref{kTopIsCoreflectiveSubcategory}) but by all [[pullbacks]] ([MO comment by Charles Rezk](http://mathoverflow.net/a/47724/381))


* in $Top_{cgwH}$ the [[regular monomorphisms]] are the [[closed subspace]] inclusions ([MO comment by Charles Rezk](http://mathoverflow.net/a/47724/381))


+-- {: .num_defn #WeaklyHausdorff}
###### Definition

A [[topological space]] $X$ is called **[[weakly Hausdorff topological space|weakly Hausdorff]]** if for every [[continuous function]]

$$
  f \;\colon\; K \longrightarrow X
$$

out of a [[compact topological space|compact]] [[Hausdorff space]] $K$, its [[image]] $f(K) \subset X$  is a [[closed subset]] of $X$.

=--

+-- {: .num_prop #HausdorffImpliessWeaklyHausdorff}
###### Proposition

Every [[Hausdorff space]] is a [[weakly Hausdorff space]], def. \ref{WeaklyHausdorff}.

=--

+-- {: .proof}
###### Proof

Since [[compact subspaces of Hausdorff spaces are closed]].

=--



+-- {: .num_prop #CharacterizationOfCompactClosedSetsInWeaklyHausdorffSpace}
###### Proposition

For $X$ a [[weakly Hausdorff topological space]], def. \ref{WeaklyHausdorff}, then a subset $A \subset X$ is $k$-closed, def. \ref{kTop}, precisely if for every subset $K \subset X$ that is [[compact subspace|compact]] [[Hausdorff space|Hausdorff]] with respect to the [[subspace topology]], then the [[intersection]] $K \cap A$ is a [[closed subset]] of $X$.

=--

e.g. ([Strickland 09, lemma 1.4 (c)](#Strickland09))


### Monoidal and topologically enriched model structure
 {#TopologicalEnrichment}

We discuss that $(Top_{cg})_{Quillen}$ and $(Top^{\ast/}_{cg})_{Quillen}$ are [[monoidal model categories]] and [[enriched model categories]] over themselves, the former with respect to [[Cartesian product]] and the latter with respect to the induced [[smash product]].

+-- {: .num_defn #PushoutProduct}
###### Definition

Let $i_1 \colon X_1 \to Y_1$ and $i_2 \colon X_2 \to Y_2$ be morphisms in $Top_{cg}$, def. \ref{kTop}. Their **[[pushout product]]** 

$$
  i_1\Box i_2
   \coloneqq
  \big(
    (id, i_2), (i_1,id)
  \big)
$$ 

is the universal morphism in the following diagram

$$
  \array{
    && X_1 \times X_2
    \\
    & {}^{\mathllap{(i_1,id)}}\swarrow && \searrow^{\mathrlap{(id,i_2)}}
    \\
    Y_1 \times X_2 && (po) && X_1 \times Y_2
    \\
    & {}_{\mathllap{}}\searrow && \swarrow
    \\
    && (Y_1 \times X_2) \underset{X_1 \times X_2}{\sqcup} (X_1 \times Y_2)
    \\
    && \downarrow^{\mathrlap{((id, i_2), (i_1,id))}}
    \\
    && Y_1 \times Y_2
  }
$$

=--

+-- {: .num_example #PushoutProductOfTwoInclusions}
###### Example

If $i_1 \colon X_1 \hookrightarrow Y_1$ and $i_2 \colon X_2 \hookrightarrow Y_2$ are inclusions, then their pushout product $i_1 \Box i_2$ from def. \ref{PushoutProduct} is the inclusion

$$
  \left(
     X_1 \times Y_2 \;\cup\; Y_1 \times X_2
  \right)
    \hookrightarrow
  Y_1 \times Y_2
  \,.
$$

For instance 

$$
  \left(
    \{0\} \hookrightarrow I
  \right)
   \Box
  \left(
    \{0\} \hookrightarrow I
  \right)
$$

is the inclusion of two adjacent edges of a square into the square.

=--

+-- {: .num_example #PushoutProductWithInitialMorphism}
###### Example

The pushout product with an [[initial object|initial]] morphism
is just the ordinary [[Cartesian product]] functor

$$
  (\emptyset \to X) \Box (-)
    \simeq
  X \times (-)
  \,,
$$

i.e.

$$
  (\emptyset \to X) \Box (A \overset{f}{\to} B)
  \simeq
  (X\times A \overset{X \times f}{\longrightarrow} X \times B ) 
  \,.
$$

=--

+-- {: .proof}
###### Proof

The [[product topological space]] with the [[empty set|empty]] space is the empty space, hence the map $\emptyset \times A \overset{(id,f)}{\longrightarrow} \emptyset \times B$ is an isomorphism, and so the pushout in the pushout product is $X \times A$. From this one reads off the universal map in question to be $X \times  f$:

$$
  \array{
    && \emptyset \times A
    \\
    & {}^{\mathllap{}}\swarrow && \searrow^{\mathrlap{\simeq}}
    \\
    X \times A && (po) && \emptyset \times B
    \\
    & {}_{\mathllap{}}\searrow && \swarrow
    \\
    && X \times A
    \\
    && \downarrow^{\mathrlap{((id, f), \exists !)}}
    \\
    && X \times B
  }
  \,.
$$

=--

+-- {: .num_example #PushoutProductOfITopwithITopAndJTop}
###### Example

With 

$$
  I_{Top} \colon \{ S^{n-1} \overset{i_n}{\hookrightarrow} D^n\}
  \;\;\;
  and
  \;\;\;
  J_{Top} \colon \{ D^n \overset{j_n}{\hookrightarrow} D^n \times I\}
$$

the generating cofibrations (def. \ref{TopologicalGeneratingCofibrations}) and generating acyclic cofibrations (def. \ref{TopologicalGeneratingAcyclicCofibrations}) of $(Top_{cg})_{Quillen}$ (theorem \ref{ModelStructureOnTopcg}), then
their [[pushout-products]] (def. \ref{PushoutProduct}) are

$$
  \begin{aligned}
  i_{n_1} \Box i_{n_2} & \simeq i_{n_1 + n_2}
  \\
  i_{n_1} \Box j_{n_2} & \simeq j_{n_1 + n_2}
  \end{aligned}
  \,.
$$

=--

+-- {: .proof}
###### Proof

To see this, it is profitable to model [[n-disks]] and [[n-spheres]], up to [[homeomorphism]], as $n$-cubes $D^\n \simeq [0,1]^n \subset \mathbb{R}^n$ and their boundaries $S^{n-1} \simeq \partial [0,1]^n$ . For the idea of the proof, consider the situation in low dimensions, where one readily sees pictorially that

$$
  i_1 \Box i_1
  \;\colon\;
    \left(\;\; = \;\;\cup\;\; \vert\vert\;\;\right) 
    \hookrightarrow
    \Box
$$

and

$$
  i_1 \Box j_0
  \;\colon\;
    \left(\;\; = \;\;\cup\;\; \vert \;\; \right) 
    \hookrightarrow
    \Box
  \,.
$$

Generally, $D^n$ may be represented as the space of $n$-tuples of elements in $[0,1]$, and $S^n$ as the suspace of tuples for which at least one of the coordinates is equal to 0 or to 1. 

Accordingly, $S^{n_1} \times D^{n_2} \hookrightarrow D^{n_1 + n_2}$ is the subspace of $(n_1+n_2)$-tuples, such that at least one of the first $n_1$ coordinates is equal to 0 or 1, while $D^{n_1} \times S^{n_2} \hookrightarrow D^{n_1+ n_2}$ is the subspace of $(n_1 + n_2)$-tuples such that east least one of the last $n_2$ coordinates is equal to 0 or to 1. Therefore

$$
  S^{n_1} \times D^{n_2} \cup D^{n_1} \times S^{n_2} \simeq S^{n_1 + n_2}
  \,.
$$

And of course it is clear that $D^{n_1} \times D^{n_2} \simeq D^{n_1 + n_2}$. This shows the first case.

For the second, use that $S^{n_1} \times D^{n_2} \times I$ is contractible to $S^{n_1} \times D^{n_2}$ in $D^{n_1} \times D^{n_2} \times I$, and that $S^{n_1} \times D^{n_2}$ is a subspace of $D^{n_1} \times D^{n_2}$.

=--


+-- {: .num_defn #PullbackPowering}
###### Definition

Let $i \colon A \to B$ and $p \colon X \to Y$ be two morphisms in $Top_{cg}$, def. \ref{kTop}. Their **pullback powering** is

$$
  p^{\Box i}
    \coloneqq
  (p^B, X^i)
$$ 

being the universal morphism in 

$$
  \array{
    && X^B
    \\
    && \downarrow^{\mathrlap{(p^B, X^i)}}
    \\
    && Y^B \underset{Y^A}{\times} X^A
    \\
    & \swarrow && \searrow
    \\
    Y^B && (pb) && X^A
    \\
    & {}_{\mathllap{Y^i}}\searrow && \swarrow_{\mathrlap{p^A}}
    \\
    && Y^A   
  }
$$

=--

+-- {: .num_prop #JoyalTierneyCalculus}
###### Proposition

Let $i_1, i_2 , p$ be three morphisms in $Top_{cg}$, def. \ref{kTop}. Then for their [[pushout-products]] (def. \ref{PushoutProduct}) and pullback-powerings (def. \ref{PullbackPowering}) the following [[lifting properties]] are equivalent ("[[Joyal-Tierney calculus]]"):

$$
  \array{
    &  i_1 \Box i_2 & \text{has LLP against} & p 
    \\
    \Leftrightarrow & i_1 &  \text{has LLP against} & p^{\Box i_2}
    \\
    \Leftrightarrow & i_2 &  \text{has LLP against} & p^{\Box i_1}
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

We claim that by the [[cartesian closed category|cartesian closure]] of $Top_{cg}$, and carefully collecting terms, one finds a natural bijection between [[commuting squares]] and their [[lifts]] as follows:

$$
  \array{
    Q &\overset{f}{\longrightarrow}& X^B
    \\
    {}^{\mathllap{i_1}}\downarrow && \downarrow^{\mathrlap{p^{\Box i_2}}}
    \\
    P &\underset{(g_1,g_2)}{\longrightarrow}& Y^B \underset{Y^A}{\times} X^A
  }
  \;\;\;\;\;\;\;
  \leftrightarrow
  \;\;\;\;\;\;\;
  \array{
    Q \times B \underset{Q \times A}{\sqcup} P \times A
    &\overset{(\tilde f, \tilde g_2)}{\longrightarrow}&
    X
    \\
    {}^{\mathllap{i_1 \Box i_2}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    P \times B & \underset{\tilde g_1}{\longrightarrow} & Y
  }
  \,,
$$

where the tilde denotes product/hom-[[adjuncts]], for instance

$$
  \frac{
    P \overset{g_1}{\longrightarrow} Y^B
  }{
    P \times B \overset{\tilde g_1}{\longrightarrow} Y
  }
$$

etc. 

To see this in more detail, observe that both squares above each represent two squares from the two components into the fiber product and out of the pushout, respectively, as well as one more square exhibiting the compatibility condition on these components:

$$
 \begin{aligned}
   &
   \;\;\;\; 
  \array{
    Q &\overset{f}{\longrightarrow}& X^B
    \\
    {}^{\mathllap{i_1}}\downarrow && \downarrow^{\mathrlap{p^{\Box i_2}}}
    \\
    P &\underset{(g_1,g_2)}{\longrightarrow}& Y^B \underset{Y^A}{\times} X^A
  }
   \\
  \simeq &
   \;\;\;\;
   \left\{
    \;\;\;\;
    \array{
      Q &\overset{f}{\longrightarrow}& X^B
      \\
      {}^{\mathllap{i_1}}\downarrow && \downarrow^{\mathrlap{p^B}}
      \\
      P &\underset{g_1}{\longrightarrow}& Y^B
    }
  \;\;\;\;\;
  \,,
  \;\;\;\;\;
    \array{
      Q &\overset{f}{\longrightarrow}& X^B
      \\
      {}^{\mathllap{i_1}}\downarrow && \downarrow^{\mathrlap{X^{i_2}}}
      \\
      P &\underset{g_1}{\longrightarrow}& X^A
    }
  \;\;\;\;\;
  \,,
  \;\;\;\;\;
  \array{
    P &\overset{g_2}{\longrightarrow}& X^A
    \\
    {}^{\mathllap{g_1}}\downarrow && \downarrow^{\mathrlap{p^A}}
    \\
    Y^B &\underset{Y^{i_2}}{\longrightarrow}& Y^A
  }
  \;\;\;\;\;
  \right\}
  \\
  \leftrightarrow
  &
  \;\;\;\;
  \left\{
    \;\;\;\;\;
    \array{
      Q \times B &\overset{\tilde f}{\longrightarrow}& X
      \\
      {}^{\mathllap{(i_1,id)}}\downarrow && \downarrow^{\mathrlap{p}}
      \\
      P \times B &\underset{\tilde g_2}{\longrightarrow}& Y
    }
    \;\;\;\;\;
    \,,
    \;\;\;\;\;
    \array{
      Q \times A &\overset{(id,i_2)}{\longrightarrow}& Q \times B
      \\
      {}^{\mathllap{(i_1,id)}}\downarrow && \downarrow^{\mathrlap{\tilde f}}
      \\
      P \times A &\underset{\tilde g_2}{\longrightarrow}& X
    }
    \;\;\;\;\;
    \,,
    \;\;\;\;\;
    \array{
      P \times A &\overset{\tilde g_2}{\longrightarrow}& X
      \\
      {}^{\mathllap{(id,i_2)}}\downarrow && \downarrow^{\mathrlap{p}}
      \\
      P \times B &\underset{\tilde g_1}{\longrightarrow}& Y
    }
    \;\;\;\;\;
  \right\}
  \\
  \simeq
  &
  \;\;\;\;
  \array{
    Q \times B \underset{Q \times A}{\sqcup} P \times A
    &\overset{(\tilde f, \tilde g_2)}{\longrightarrow}&
    X
    \\
    {}^{\mathllap{i_1 \Box i_2}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    P \times B & \underset{\tilde g_1}{\longrightarrow} & Y
  }
  \end{aligned}
  \,.
$$


=--


+-- {: .num_prop #PushoutProductInTopCGSendsCofCofToCof}
###### Proposition

The [[pushout-product]] in $Top_{cg}$ (def. \ref{kTop}) of two classical cofibrations is a classical cofibration:

$$
  Cof_{cl} \Box Cof_{cl} \subset Cof_{cl}
  \,.
$$

If one of them is acyclic, then so is the pushout-product:

$$
  Cof_{cl} \Box (W_{cl} \cap Cof_{cl}) \subset W_{cl}\cap Cof_{cl}
  \,.
$$


=--

+-- {: .proof}
###### Proof

Regarding the first point:

By example \ref{PushoutProductOfITopwithITopAndJTop} we have

$$
  I_{Top} \Box I_{Top} \subset I_{Top}
$$

Hence

$$
  \array{
    & I_{Top} \Box I_{Top} & \text{has LLP against} & W_{cl} \cap Fib_{cl}
    \\
    \Leftrightarrow
    & I_{Top} & \text{has LLP against} & (W_{cl} \cap Fib_{cl})^{\Box I_{Top}}
    \\
    \Rightarrow
    & Cof_{cl} & \text{has LLP against} & (W_{cl} \cap Fib_{cl})^{\Box I_{Top}}
    \\
    \Leftrightarrow
    & 
    I_{Top} \Box Cof_{cl} & \text{has LLP against} & W_{cl} \cap Fib_{cl}
    \\
    \Leftrightarrow
    &
    I_{Top} & \text{has LLP against} & (W_{cl} \cap Fib_{cl})^{Cof_{cl}}
    \\
    \Rightarrow
    & Cof_{cl} & \text{has LLP against} & (W_{cl} \cap Fib_{cl})^{Cof_{cl}}
    \\
    \Leftrightarrow
    & Cof_{cl} \Box \Cof_{cl}  & \text{has LLP against} & W_{cl} \cap Fib_{cl}
  }
  \,,
$$

where all logical equivalences used are those of prop. \ref{JoyalTierneyCalculus} and where all implications appearing are by the closure property of lifting problems ([prop.](injective+or+projective+morphism#ClosurePropertiesOfInjectiveAndProjectiveMorphisms)).

Regarding the second point: By example \ref{PushoutProductOfITopwithITopAndJTop} we moreover have

$$
  I_{Top} \Box J_{Top} \subset J_{Top}
$$

and the conclusion follows by the same kind of reasoning.

=--

+-- {: .num_remark}
###### Remark

In [[model category]] theory the property in proposition \ref{PushoutProductInTopCGSendsCofCofToCof} is referred to as saying that the model category $(Top_{cg})_{Quillen}$ from theorem \ref{ModelStructureOnTopcg}

1. is a [[monoidal model category]] with respect to the [[Cartesian product]] on $Top_{cg}$;

1. is an [[enriched model category]], over itself.


=--

A key point of what this entails is the following:

+-- {: .num_prop #HomProductAdjunctionForCofibrantObjectInTopCGIsQuillen}
###### Proposition

For $X \in (Top_{cg})_{Quillen}$ cofibrant (a [[retract]] of a [[cell complex]], e.g. a [[CW complex]]) then the product-hom-adjunction for $Y$ (prop. \ref{CartesianClosureOfTopcg}) is a [[Quillen adjunction]]

$$
  (Top_{cg})_{Quillen}
   \underoverset
     \underset{(-)^X}{\longrightarrow}
     \overset{X \times (-)}{\longleftarrow}
     {\bot}
  (Top_{cg})_{Quillen}
  \,.
$$

=--

+-- {: .proof}
###### Proof

By example \ref{PushoutProductWithInitialMorphism} we have that the [[left adjoint]] functor is equivalently the [[pushout product]] functor with the initial morphism of $X$: 

$$
  X \times (-)
  \simeq
  (\emptyset \to X) \Box (-)
  \,.
$$

By assumption $(\emptyset \to X)$ is a cofibration, and hence prop. \ref{PushoutProductInTopCGSendsCofCofToCof} says that this is a left Quillen functor.

=--

The statement and proof of prop. \ref{HomProductAdjunctionForCofibrantObjectInTopCGIsQuillen} has a direct analogue in [[pointed topological spaces]]

+-- {: .num_prop #HomProductAdjunctionForCofibrantObjectInPointedTopCGIsQuillen}
###### Proposition

For $X \in (Top^{\ast/}_{cg})_{Quillen}$ cofibrant with respect to the [[classical model structure on pointed topological spaces|classical model structure on pointed]] [[compactly generated topological spaces]] (theorem \ref{ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces}, prop. \ref{ModelStructureOnSliceCategory}) (hence a [[retract]] of a [[cell complex]] with non-degenerate basepoint, remark \ref{NonDegenerateBasepointAsCofibrantObjects}) then the pointed product-hom-adjunction from corollary \ref{SmashHomAdjunctionOnPointedCompactlyGeneratedTopologicalSpaces}  is a [[Quillen adjunction]] (def. \ref{QuillenAdjunction}):

$$
  (Top^{\ast/}_{cg})_{Quillen}
   \underoverset
     \underset{(-)^X}{\longrightarrow}
     \overset{X \times (-)}{\longleftarrow}
     {\bot}
  (Top^{\ast/}_{cg})_{Quillen}
  \,.
$$

=--

+-- {: .proof}
###### Proof

Let now $\Box_\wedge$ denote the **smash pushout product** and $(-)^{\Box(-)}$ the **smash pullback powering** defined as in def. \ref{PushoutProduct} and def. \ref{PullbackPowering}, but with [[Cartesian product]] replaced by [[smash product]] (def. \ref{SmashProductOfPointedObjects}) and compactly generated [[mapping space]] replaced by pointed mapping spaces (def. \ref{PointedMappingSpace}).

By theorem \ref{CofibrantGenerationOfPointedTopologicalSpaces} $(Top_{cg}^{\ast/})_{Quillen}$ is [[cofibrantly generated model category|cofibrantly generated]] by $I_{Top^{\ast/}} = (I_{Top})_+$ and $J_{Top^{\ast/}}= (J_{Top})_+$. Example \ref{WedgeAndSmashOfBasePointAdjoinedTopologicalSpaces} gives that for $i_n \in I_{Top}$ and $j_n \in J_{Top}$ then

$$
  (i_{n_1})_+ \Box_\wedge (i_{n_2})_+ \simeq (i_{n_1 + n_2})_+
$$

and

$$
  (i_{n_1})_+ \wedge_\wedge (i_{n_2})_+ \simeq (i_{n_1 + n_2})_+
  \,.
$$

Hence the pointed analog of prop. \ref{PushoutProductInTopCGSendsCofCofToCof} holds and therefore so does the pointed analog of the conclusion in prop. \ref{HomProductAdjunctionForCofibrantObjectInTopCGIsQuillen}.


=--




### The model structure on topologically enriched functors
 {#ModelStructureOnTopEnrichedFunctors}

The [[projective model structure on enriched functors]], enriched over the classical model structure on topological spaces above, is an immediate corollary of the above proof ([Piacenza 91](#Piacenza91)). 

In the following we say _[[Top]]-[[enriched category]]_ and _[[Top]]-[[enriched functor]]_ etc. for what often is referred to as "[[topological category]]" and "[[topological functor]]" etc. As discussed there, these latter terms are ambiguous.


+-- {: .num_defn #TopEnrichedCategory}
###### Definition

A **[[topologically enriched category]]** $\mathcal{C}$ is a [[Top]]-[[enriched category]], hence:

1. a [[class]] $Obj(\mathcal{C})$, called the **class of [[objects]]**;

1. for each $a,b\in Obj(\mathcal{C})$ a topological space 

   $$
     \mathcal{C}(a,b)\in Top
     \,,
   $$

   called the **space of [[morphisms]]** or the **[[hom-space]]** between $a$ and $b$;

1. for each $a,b,c\in Obj(\mathcal{C})$ a [[continuous function]]

   $$
     \circ_{a,b,c} \;\colon\; \mathcal{C}(a,b)\times \mathcal{C}(b,c) \longrightarrow \mathcal{C}(a,c)
   $$

   out of the [[product topological space]], called the _[[composition]]_ operation

1. for each $a \in Obj(\mathcal{C})$ a point $Id_a\in \mathcal{C}(a,a)$, called the _[[identity]]_ morphism on $a$

such that the composition is [[associativity|associative]] and [[unitality|unital]].

Similarly a **pointed topologically enriched category** is such a structire with $Top_k$ replaced by [[pointed topological spaces]] and with the [[Cartesian product]] replaced by the [[smash product]] of pointed topological spaces.

=--

+-- {: .num_remark #UnderlyingCategoryOfTopEnrichedCategory}
###### Remark

Given a (pointed) [[topologically enriched category]] as in def. \ref{TopEnrichedCategory}, then forgetting the topology on the [[hom-spaces]] (along the [[forgetful functor]] $U \colon Top_k \to Set$) yields an ordinary [[locally small category]] with

$$
  Hom_{\mathcal{C}}(a,b) = U(\mathcal{C}(a,b))
  \,.
$$

It is in this sense that $\mathcal{C}$ is a category with [[extra structure]], and hence "[[enriched category|enriched]]".
 
=--

The archetypical example is the following:

+-- {: .num_example #TopkAsATopologicallyEnrichedCategory}
###### Example

Write 

$$
  Top_k \hookrightarrow Top
$$ 

for the [[full subcategory]] of [[Top]] on the [[compactly generated topological spaces]]. Under forming [[Cartesian product]] 

$$
  (-)\times (-)
  \;\colon\;
  Top_k \times Top_k \longrightarrow Top_k
$$


and [[mapping spaces]] 

$$
  (-)^{(-)}
  \;\colon\;
  Top_k^{op}\times Top_k
  \longrightarrow
  Top_k
$$

this is a [[cartesian closed category]] (see at _[[convenient category of topological spaces]]_). As such it canonically obtains the structure of a [[topologically enriched category]], def. \ref{TopEnrichedCategory}, with [[hom-spaces]] given by [[mapping spaces]]

$$
  Top_k(X,Y)
  \coloneqq
  Y^X
$$

and with [[composition]] 

$$
  Y^X \times Z^Y
  \longrightarrow
  Z^X
$$

given by the (product$\dashv$ mapping-space)-[[adjunct]] of the [[evaluation morphism]]

$$
  X \times Y^X \times Z^Y
  \overset{(ev, id)}{\longrightarrow}
  Y \times Z^Y
  \overset{ev}{\longrightarrow}
  Z
  \,.
$$

Similarly, [[pointed topological spaces|pointed]] [[compactly generated topological spaces]] $Top_k^{\ast/}$ form a pointed topologically enriched category.

=--

+-- {: .num_defn #TopologicallyEnrichedFunctor}
###### Definition

A [[topologically enriched functor]] between two [[topologically enriched categories]] 

$$
  F \;\colon\;  \mathcal{C}  \longrightarrow \mathcal{D}
$$

is a [[Top]]-[[enriched functor]], hence:

1. a [[function]]

   $$
     F_0 \colon Obj(\mathcal{C}) \longrightarrow Obj(\mathcal{D})
   $$

   of [[objects]];

1. for each $a,b \in Obj(\mathcal{C})$ a [[continuous function]]

   $$
     F_{a,b} \;\colon\; \mathcal{C}(a,b) \longrightarrow \mathcal{D}(F_0(a), F_0(b))
   $$

   of [[hom-spaces]]

such that this preserves [[composition]] and [[identity]] morphisms in the evident sense.

A [[homomorphism]] of topologically enriched functors 

$$
  \eta \;\colon\; F \Rightarrow G
$$ 

is a [[Top]]-[[enriched natural transformation]]: for each $c \in Obj(\mathcal{C})$ a choice of morphism $\eta_c \in \mathcal{D}(F(c),G(c))$ such that for each pair of objects $c,d \in \mathcal{C}$ the two continuous functions 

$$
  \eta_d \circ F(-) \;\colon\; \mathcal{C}(c,d) \longrightarrow \mathcal{D}(F(c), G(d))
$$

and

$$
  G(-) \circ \eta_c \;\colon\; \mathcal{C}(c,d) \longrightarrow \mathcal{D}(F(c), G(d))
$$

agree.

We write $[\mathcal{C}, \mathcal{D}]$ for the resulting category of topologically enriched functors. This itself naturally obtains the structure of [[topologically enriched category]], see at _[[enriched functor category]]_.

=--


+-- {: .num_example #TopologicallyEnrichedFunctorsToTopk}
###### Example

For $\mathcal{C}$ any topologically enriched category, def. \ref{TopEnrichedCategory} then a topologically enriched functor

$$
  F \;\colon\; \mathcal{C} \longrightarrow Top_k
$$

to the archetical topologically enriched category from example \ref{TopkAsATopologicallyEnrichedCategory} may be thought of as a topologically enriched [[copresheaf]], at least if $\mathcal{C}$ is [[small category|small]] (in that its [[class]] of objects is a proper [[set]]).

Hence the category of topologically enriched functors

$$
  [\mathcal{C}, Top_k] 
$$

according to def. \ref{TopologicallyEnrichedFunctor} may be thought of as the ([[copresheaf|co-]])[[presheaf category]] over $\mathcal{C}$ in the realm of topological enriched categories.

A funcotor $F \in [\mathcal{C}, Top_k]$ is equivalently 

* a [[compactly generated topological space]] $F_a\in Top_k$ for each object $a \in Obj(\mathcal{C})$;

* a [[continuous function]]

  $$
     F_a \times \mathcal{C}(a,b) \longrightarrow F_b
  $$

  for all pairs of objects $a,b \in Obj(\mathcal{C})$

such that composition is respected, in the evident sense.

For every object $c \in \mathcal{C}$, there is a topologically enriched [[representable functor]], denoted $y(c) or \mathcal{C}(c,-)$ which sends objects to 

$$
  y(c)(d) = \mathcal{C}(c,d) \in Top
$$

and whose action on morphisms is, under the above identification, just the [[composition]] operation in $\mathcal{C}$.

=--

There is a full blown [[Top]]-[[enriched Yoneda lemma]]. The following records a slightly simplified version which is all that is needed here:

+-- {: .num_prop #TopologicallyEnrichedYonedaLemma}
###### Proposition
**(topologically enriched Yoneda-lemma)**

Let $\mathcal{C}$ be a [[topologically enriched category]], def. \ref{TopEnrichedCategory}, write $[\mathcal{C}, Top_k]$ for its category of topologically enriched (co-)presheaves, and for $c\in Obj(\mathcal{C})$ write $y(c) = \mathcal{C}(c,-) \in [\mathcal{C}, Top_k]$ for the topologically enriched functor that it represents, all according to example \ref{TopologicallyEnrichedFunctorsToTopk}. Recall also the Top-tensored functors $F \cdot X$ from that example.

For $c\in Obj(\mathcal{C})$, $X \in Top$ and $F \in [\mathcal{C}, Top_k]$, there is a [[natural bijection]] between 

1. morphisms $y(c) \cdot X \longrightarrow F$ in $[\mathcal{C}, Top_k]$;

1. morphisms $X \longrightarrow F(c)$ in [[Top]].

=--

+-- {: .proof}
###### Proof

Given a morphism $\eta \colon y(c) \cdot X \longrightarrow F$ consider its component

$$
  \eta_c \;\colon\; \mathcal{C}(c,c)\times X \longrightarrow F(c)
$$

and restrict that to the identity morphism $id_c \in \mathcal{C}(c,c)$ in the first argument

$$
  \eta_c(id_c,-) \;\colon\; X \longrightarrow F(c)
  \,.
$$

We claim that just this $\eta_c(id_c,-)$ already uniquely determines all components 

$$
  \eta_d \;\colon\; \mathcal{C}(c,d)\times X \longrightarrow F(d)
$$

of $\eta$, for all $d \in Obj(\mathcal{C})$: By definition of the transformation $\eta$ (def. \ref{TopologicallyEnrichedFunctor}), the two functions

$$
   F(-) \circ \eta_c
  \;\colon\;
  \mathcal{C}(c,d)
  \longrightarrow
  F(d)^{\mathcal{C}(c,c) \times X}
$$

and

$$
  \eta_d  \circ \mathcal{C}(c,-) \times X
  \;\colon\;
  \mathcal{C}(c,d)
  \longrightarrow
  F(d)^{\mathcal{C}(c,c) \times X}
$$

agree. This means that they may be thought of jointly as a function with values in commuting squares in $Top$ of this form:

$$
  f
  \;\;\;\;
  \mapsto
  \;\;\;\;
  \array{
    \mathcal{C}(c,c) \times X &\overset{\eta_c}{\longrightarrow}& F(c)
    \\
    {}^{\mathllap{\mathcal{C}(c,f)}}\downarrow && \downarrow^{\mathrlap{F(f)}}
    \\
    \mathcal{C}(c,d) \times X &\underset{\eta_d}{\longrightarrow}& F(d)
  }
$$

For any $f \in \mathcal{C}(c,d)$, consider the restriction of

$$
  \eta_d \circ \mathcal{C}(c,f) \in F(d)^{\mathcal{C}(c,c) \times X}
$$

to $id_c \in \mathcal{C}(c,c)$, hence restricting the above commuting squares to

$$
  f
  \;\;\;\;
  \mapsto
  \;\;\;\;
  \array{
    \{id_c\} \times X &\overset{\eta_c}{\longrightarrow}& F(c)
    \\
    {}^{\mathllap{\mathcal{C}(c,f)}}\downarrow && \downarrow^{\mathrlap{F}(f)}
    \\
    \{f\} \times X &\underset{\eta_d}{\longrightarrow}& F(d)
  }
$$

This shows that $\eta_d$ is fixed to be the function

$$
  \eta_d(f,x) = F(f)\circ \eta_c(id_c,x)
$$

and this is a continuous function since all the operations it is built from are continuous.

Conversely, given a continuous function $\alpha \colon X \longrightarrow F(c)$, define for each $d$ the function

$$
  \eta_d \colon (f,x) \mapsto F(f) \circ \alpha
  \,.
$$

Running the above analysis backwards shows that this determines a transformation $\eta \colon y(c)\times X \to F$.


=--



+-- {: .num_defn #GeneratingCofibrationsForProjectiveStructureOnFunctors}
###### Definition

For $\mathcal{C}$ a [[small category|small]] topologically enriched category, def. \ref{TopEnrichedCategory}, write

$$
  I_{Top}^{\mathcal{C}}
  \;\coloneqq\;
  \left\{
    y(c)\cdot (S^{n-1} \overset{\iota_n}{\longrightarrow} D^n)
  \right\}_{{n \in \mathbb{N}} \atop {c \in Obj(\mathcal{C})}}
$$

and 

$$
  J_{Top}^{\mathcal{C}}
  \;\coloneqq\;
  \left\{
    y(c)\cdot (D^n \overset{(id, \delta_0)}{\longrightarrow} D^n \times I)
  \right\}_{{n \in \mathbb{N}} \atop {c \in Obj(\mathcal{C})}}
$$

for the classes (here: sets) of morphisms given by [[tensoring]] the representable functors, example \ref{TopologicallyEnrichedFunctorsToTopk} with the generating cofibrations (def.\ref{TopologicalGeneratingCofibrations}) and acyclic generating cofibrations (def. \ref{TopologicalGeneratingAcyclicCofibrations}) of $Top_k$, respectively.

These are going to be called the **[[generating cofibrations]]** and **acyclic generating cofibrations** for the projective model structure on topologically enriched functors on $\mathcal{C}$.

Similarly, for $\mathcal{C}$ a pointed topologically enriched category, write 

$$
  I_{Top^{\ast/}}^{\mathcal{C}}
  \;\coloneqq\;
  \left\{
    y(c)\cdot (S^{n-1}_+ \overset{(\iota_n)_+}{\longrightarrow} D^n_+)
  \right\}_{{n \in \mathbb{N}} \atop {c \in Obj(\mathcal{C})}}
$$

and 

$$
  J_{Top^{\ast/}}^{\mathcal{C}}
  \;\coloneqq\;
  \left\{
    y(c)\cdot (D^n_+ \overset{(id, \delta_0)_+}{\longrightarrow} (D^n \times I)_+)
  \right\}_{{n \in \mathbb{N}} \atop {c \in Obj(\mathcal{C})}}
$$

for the same construction applied to the pointed generating (acyclic) cofibrations of def. \ref{GeneratingCofibrationsForPointedTopologicalSpaces}.

=--

+-- {: .num_remark #MorphismsFromTensoredRepresentableToTopologicallyEnrichedFunctor}
###### Remark

By the [[Top]]-[[enriched Yoneda lemma]], prop. \ref{TopologicallyEnrichedYonedaLemma}, and the defining property of [[tensoring]] over $Top_k$, there are [[natural bijections]]

$$
  \frac{
    y(c)\cdot X \longrightarrow F
  }{
    X \longrightarrow F(c)
  }
$$

between 

1. [[natural transformations]] from $y(c)\cdot X$  (the [[tensoring]] with $X \in Top_k$ of the [[representable functor]] of $c\in Obj(\mathcal{C})$) to some topologically enriched functor $F$ , 

1. [[continuous functions]] from $X$ to the value of that topological functor on the object $c$.

=--

+-- {: .num_defn #ClassesOfMorphismsInTheProjectiveModelStructureOnTopEnrichedFunctors}
###### Definition

Given a [[small category|small]] (pointed) [[topologically enriched category]] $\mathcal{C}$, def. \ref{TopEnrichedCategory}, say that a morphism in the category of (pointed) topologically enriched copresheaves $[\mathcal{C}, Top_k]$ ($[\mathcal{C},Top_k^{\ast/}]$), example \ref{TopologicallyEnrichedFunctorsToTopk}, hence a [[natural transformation]] between topologically enriched functors, $\eta \colon F \to G$ is

* a **projective weak equivalence**, if for all $c\in Obj(\mathcal{C})$ the component $\eta_c \colon F(c) \to G(c)$ is a [[weak homotopy equivalence]] (def. \ref{WeakHomotopyEquivalenceOfTopologicalSpaces});

* a **projective fibration** if for all $c\in Obj(\mathcal{C})$ the component $\eta_c \colon F(c) \to G(c)$ is a [[Serre fibration]] (def. \ref{SerreFibration});

* a **projective cofibration** if it is a [[retract]] (rmk. \ref{RetractsOfMorphisms}) of an $I_{Top}^{\mathcal{C}}$-[[relative cell complex]] (def. \ref{TopologicalCCellComplex}, def. \ref{GeneratingCofibrationsForProjectiveStructureOnFunctors}).

Write 

$$ 
  [\mathcal{C}, Top_{Quillen}]_{proj}
$$

for the category of topologically enriched functors equipped with these classes of morphisms.

=--

+-- {: .num_theorem #ProjectiveModelStructureOnTopEnrichedFunctors}
###### Theorem

The classes of morphisms in def. \ref{ClassesOfMorphismsInTheProjectiveModelStructureOnTopEnrichedFunctors} constitute a [[model category]] structure on $[\mathcal{C}, Top]$, called the **[[projective model structure on enriched functors]]** $[\mathcal{C}, Top_{Quillen}]_{proj}$.

=--

([Piacenza 91, theorem 5.4](#Piacenza91))

+-- {: .proof}
###### Proof

Via remark \ref{MorphismsFromTensoredRepresentableToTopologicallyEnrichedFunctor}, the statement essentially reduces objectwise to the proof of theorem \ref{TopQuillenModelStructure}:

In particular, the technical lemmas \ref{CompactSubsetsAreSmallInCellComplexes}, \ref{JTopRelativeCellComplexesAreWeakHomotopyEquivalences} and \ref{AcyclicSerreFibrationsAreTheJTopFibrations} generalize immediately to the present situation, with the evident small change of wording. 

For instance the fact that a morphism of topologically enriched functors $\eta \colon F \to G$ that has the right lifting property against the elements of $I_{Top}^{\mathcal{C}}$ is a projective weak equivalence, follows by noticing that remark \ref{MorphismsFromTensoredRepresentableToTopologicallyEnrichedFunctor} gives a [[natural bijection]] of commuting diagrams (and their fillers) of the form

$$
  \left(
  \array{
    y(c) \cdot S^{n-1} &\longrightarrow& F
    \\
    {}^{\mathllap{(id\cdot \iota_n)}}\downarrow && \downarrow^{\mathrlap{\eta}}
    \\ 
    y(c) \cdot D^n &\longrightarrow& G
  }
  \right)
  \;\;\;\leftrightarrow\;\;\;
  \left(
  \array{
     S^{n-1} &\longrightarrow& F(c)
     \\
     \downarrow && \downarrow^{\mathrlap{\eta_c}}
     \\
     D^n &\longrightarrow& G(c)
  }
  \right)
  \,,
$$

and hence the statement follows with part A) of the proof of lemma \ref{AcyclicSerreFibrationsAreTheJTopFibrations}.

With these three lemmas in hand, the remaining formal part of the proof goes through verbatim as [above](#VerificationOfTopQuillen): repeatedly use the [[small object argument]] and the [[retract argument]] to establish the two weak factorization systems. (While again the structure of a [[category with weak equivalences]] is evident.)

=--

+-- {: .num_remark}
###### Remark

The same argument applies to functors with values in the [[classical model structure on pointed topological spaces]]

$$
  [\mathcal{C}, Top_{Quillen}^{\ast/}]
  \,.
$$

=--


+-- {: .num_example}
###### Example

The _strict_ [[Bousfield-Friedlander model structure]] on [[sequential spectra]] is equivalently the projective model structure on functors on the non-full subcategory of $Top^{\ast/}$ on the "standard spheres" (see at _[sequential spectrum -- As diagram spectra](sequential+spectrum#AsDiagramSpectra)_)

The actual stable [[Bousfield-Friedlander model structure]] is then the [[Bousfield localization of model categories|left Bousfield localization]] of that at the [[stable weak homotopy equivalences]].


$$
  SeqSpec(Top)_{stable}
   \stackrel{\longleftarrow}{\overset{Bousf.\; loc.}{\longrightarrow}}
  SeqSpec(Top)_{strict}
  \simeq
  [StdSpheres, Top^{\ast/}_{Quillen}]_{proj}
  \,.
$$

=--






## Related concepts

* [[classical model structure on simplicial sets]]

* [[model structure on topological spaces]]

  * [[classical model structure on pointed topological spaces]]

  * [[Strøm model structure]]

  * [[model structure on Delta-generated topological spaces]]

For [[topological G-spaces]] in [[equivariant homotopy theory]]:

* [[fine model structure on topological G-spaces]]

* [[coarse model structure on topological G-spaces]] ([[Borel model structure]])


## References

The original article is

* {#Quillen67} [[Dan Quillen]], chapter II, section 3 of _[[Homotopical Algebra]]_, Lecture Notes in Mathematics __43__, Springer-Verlag 1967, iv+156 pp.

An expository, concise and comprehensive writeup of the proof of the model category axioms is in 

* {#Hirschhorn15} [[Philip Hirschhorn]], _The Quillen model category of topological spaces_, Expositiones Mathematicae Volume 37, Issue 1, March 2019, Pages 2-24 ([arXiv:1508.01942](http://arxiv.org/abs/1508.01942), [doi:10.1016/j.exmath.2017.10.004](https://doi.org/10.1016/j.exmath.2017.10.004))


Useful discussion of the issue of [[compactly generated topological spaces]] in the context of homotopy theory is in 

* {#Lewis78} [[L. Gaunce Lewis]], _Compactly generated spaces_ ([pdf](http://www.math.uchicago.edu/~may/MISC/GaunceApp.pdf)), appendix A of _The Stable Category and Generalized Thom Spectra_ PhD thesis Chicago, 1978

* {#Strickland09} [[Neil Strickland]], _The category of CGWH spaces_, 2009 ([pdf](http://neil-strickland.staff.shef.ac.uk/courses/homotopy/cgwh.pdf))

See also

* {#JoyalTierney08} [[André Joyal]], [[Myles Tierney]], _Notes on simplicial homotopy theory_, Lecture at _[Advanced Course on Simplicial Methods in Higher Categories](https://lists.lehigh.edu/pipermail/algtop-l/2007q4/000017.html)_, CRM 2008  ([[JoyalTierneyNotesOnSimplicialHomotopyTheory.pdf:file]])

The observation that the proof directly extends to give the [[projective model structures on enriched functors]], enriched over $Top_{Quillen}$, is due to 

* {#Piacenza91} [[Robert Piacenza]]  section 5 of _Homotopy theory of diagrams and CW-complexes over a category_, Can. J. Math. Vol 43 (4), 1991 ([[Piazenza91.pdf:file]])

  also chapter VI of [[Peter May]] et al., _Equivariant homotopy and cohomology theory_, 1996 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/alaska.pdf))

The quick way to see the topological enrichment is indicated for instance in

* [[Stefan Schwede]], pages 5-6 of _Orbispaces, orthogonal spaces, and the universal compact Lie group_ ([pdf](http://www.math.uni-bonn.de/people/schwede/orbispaces.pdf))

[[!redirects Quillen model structure on topological spaces]]
[[!redirects Quillen model structure on Top]]

[[!redirects Quillen-Serre model structure on topological spaces]]
[[!redirects Quillen-Serre model structure on Top]]

[[!redirects Serre-Quillen model structure on topological spaces]]
[[!redirects Serre-Quillen model structure on Top]]


[[!redirects Serre model structure on topological spaces]]
[[!redirects Serre model structure on Top]]
[[!redirects Serre model structure]]

[[!redirects standard model structure on topological spaces]]
[[!redirects standard model structure on Top]]

[[!redirects cofibration of topological spaces]]
[[!redirects cofibrations of topological spaces]]
[[!redirects Serre cofibration of topological spaces]]
[[!redirects Serre cofibrations of topological spaces]]
[[!redirects Serre cofibration]]
[[!redirects Serre cofibrations]]

[[!redirects classical homotopy theory]]