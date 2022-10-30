
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

The _Quillen model structure on topological spaces_ $Top_{Quillen}$ is a [[model category]] structure on the [[category]] [[Top]] of [[topological spaces]] (also on many [[convenient categories of topological spaces]]) which represents the standard classical [[homotopy theory]]. 

Its [[weak equivalences]] are the [[weak homotopy equivalences]], its [[fibrations]] are the [[Serre fibrations]] and its [[cofibrations]] are the [[retracts]] of [[relative cell complexes]].

The [[singular simplicial complex]]/[[geometric realization]] [[nerve and realization|adjunction]] constitutes a [[Quillen equivalence]] between 
$Top_{Quillen}$ and $sSet_{Quillen}$, the [[Quillen model structure on simplicial sets]]. This is sometimes called part of the statement of the _[[homotopy hypothesis]]_ [for Kan complexes](homotopy+hypothesis#ForKanComplexes). In the language of [[(∞,1)-category theory]] this means that $Top_{Quillen}$ and $sSet_{Quillen}$ both are [[presentable (∞,1)-category|presentations]] of the [[(∞,1)-category]] [[∞Grpd]] of [[∞-groupoids]].

There are also other model structures on [[Top]] itself, see at _[[model structure on topological spaces]]_ for more. This entry here focuses on just the standard Quillen model structure.

## Background and motivation -- Topological homotopy theory

This section recalls basic relevant background concepts from [[topology]] and highlights some basic facts that may serve to motivate the Quillen model structure.

The fundamental concept of [[homotopy theory]] is that of _[[homotopy]]_. This is about contiunous deformations of [[continuous functions]] parameterized by the standard interval:

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
     {}^{\mathllap{(id,\delta_0)}}\downarrow
     \\
     X \times I &\stackrel{\eta}{\longrightarrow}& Y
     \\
     {}^{\mathllap{(id,\delta_1)}}\uparrow
     \\
     X
  }
  \,.
$$

=--

The key application of the concept of left homotopy is to the definition of [[homotopy groups]].

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
  I^n \underset{I^{n-1}}{\coprod} I^n
  \stackrel{(\alpha,\beta)}{\longrightarrow}
  \,,
$$

where the first morphism is any [[homeomorphism]] from the unit $n$-[[cube]] to the $n$-cube with one side twice the unit length.

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
it has the [[left lifting property]] against all [[Serre fibrations]] $ E \stackrel{p}{\longrightarrow} B$ that are also [[weak homotopy equivalences]].


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

So while in general the [[diagonal]] $\Delta_X$ is far from being an [[epimoprhism]] or even just a [[Serre fibration]], the factorization through the [[path space object]] may be thought of as replacing $X$, up to weak homotopy equivalence, by its path space, such as to turn its diagonal into a Serre fibration after all.

=--

+-- {: .num_defn }
###### Definition

spring

=--


## References

The original article is

* {#Quillen67} [[Dan Quillen]], chapter II, section 3 of _Homotopical algebra_, Lecture Notes in Mathematics __43__, Springer-Verlag 1967, iv+156 pp.

An expository, concise and comprehensive writeup of the proof of the model category axioms is in 

* [[Philip Hirschhorn]], _The Quillen model category of topological spaces_, 2015 ([arXiv:1508.01942](http://arxiv.org/abs/1508.01942))

[[!redirects Quillen model structure on topological spaces]]
[[!redirects Quillen model structure on Top]]