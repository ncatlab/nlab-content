
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition


+-- {: .num_defn #SubspaceTopology}
###### Definition
**([[topological subspace|subspace topology]])**

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/OpenSubsetsOfSquareInsidePlane.png" width="200">
</div>

Let $(X, \tau_X)$ be a [[topological space]], and let $S \subset X$ be a [[subset]] of its underlying [[set]]. Then the corresponding _[[topological subspace]]_ has $S$ as its underlying set, and its [[open subsets]] are those subsets of $S$ which arise as restrictions of open subsets of $X$ (i.e. [[intersections]] of open subsets of $X$ with $S$):

$$
  \left(
    U_S \subset S\,\,\text{open}
  \right)
    \,\Leftrightarrow\,
  \left(
     \underset{U_X \in \tau_X}{\exists} \left( U_S = U_X \cap S \right)
  \right)
  \,.
$$


In other words, $\tau_Y$ is the [[finer topology|smallest topology]] on $Y$ such that the inclusion $Y \hookrightarrow X$ is [[continuous map|continuous]] (the [[initial topology]] on that map). 

The picture on the right shows two open subsets inside the [[square]], regarded as a [[topological subspace]] of the [[plane]] $\mathbb{R}^2$:

> graphics grabbed from [Munkres 75](#Munkres75)


=--

The pair $(Y,\tau_Y)$ is then said to be a *topological [[subspace]]* of $(X,\tau_X)$. The induced topology is for that reason sometimes called the **subspace topology** on $Y$. 

A continuous function that factors as a [[homeomorphism]] onto its [[image]] equipped with the subspace topology is called an _[[embedding of topological spaces]]_.

A property of topological spaces is said to be **hereditary** if its satisfaction for a topological space $X$ implies its satisfaction for all topological subspaces of $X$. 

## Examples

* The [[open subsets]] of a [[closed interval]] $[0,1] \subset \mathbb{R}$ regarded as a topological subspace of the [[real line]] equipped with its [[Euclidean space|Euclidean]] [[metric topology]] is generated from the [[sub-base of a topology|sub-base]] $\beta = \{ [0, a) ,(a,1]\}_{a \in [0,1]}$.

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/OpenSubsetsOfSquareInsidePlane.png" width="200">
</div>

The image on the right shows open subsets in the closed square $[0,1]^2$, regarded as a topological subspace of the Euclidean plane

* A subset of a [[metric space]] equipped with its [[induced metric]] is a subspace with respect to the corresponding [[metric topologies]].

## Properties 

### Universal property
 {#UniversalProperty}

+-- {: .num_prop #UniversalPropertyOfSupspaceInclusion}
###### Proposition
**([[universal property]] of [[subspace topology]])**


Let $U \overset{i}{\longrightarrow} X$ be an [[injective function|injective]] [[continuous function]] between [[topological spaces]]. Then this is a [[topological subspace|subspace inclusion]] (Def. \ref{SubspaceTopology}) precisely if it satisfies the following [[universal property]]: 

* For $Z$ any topological space, a [[function]] $Z \overset{f}{\longrightarrow} U$ is [[continuous function|continuous]] precisely of $i \circ f$ is continuous

  $$
    \array{
       Z &\overset{f}{\longrightarrow}& U
       \\
       &{}_{\mathllap{i \circ f}}\searrow& \Big\downarrow{}^{\mathrlap{i}}
       \\
       && X
    }
  $$

=--

The elementary **proof** is spelled out, for instance, in [Terilla 14, theorem 1](#Terilla14). Of course this is just another way to speak of the [[initial topology]].

The universal characterization of Prop. \ref{UniversalPropertyOfSupspaceInclusion} lends itself to formalization via axioms for [[cohesion]]:

+-- {: .num_defn}
###### Definition
**([[sharp modality]] on [[topological spaces]])**

Let 

$$
  Set
    \underoverset 
      {\underset{coDisc}{\longrightarrow}}
      {\overset{\Gamma}{\longleftarrow}}
      {\bot}
  Top
$$

be the pair of [[adjoint functors]] given by sending a [[topological space]] $X$ to its underlying [[set]] $\Gamma(X)$, and by equipping a [[set]] $S$ with the [[codiscrete topology]] making it a [[codiscrete space]] $coDisc(X)$.

Write

$$
  \sharp \;\coloneqq\; coDisc \circ \Gamma
  \;\colon\;
  Top
    \longrightarrow
  Top
$$

for the induced [[modal operator]] on [[Top]] ([[sharp modality]]). We write

$$
  id \overset{\eta^{\sharp}}{\longrightarrow} \sharp 
$$

for the [[unit of an adjunction|unit]] morphism of this [[adjunction]].

=--

+-- {: .num_prop #UniversalPropertyViaSharpModality}
###### Proposition

Let $U \overset{i}{\longrightarrow} X$ be an [[injective function|injective]] [[continuous function]] between [[topological spaces]]. Then this is a [[topological subspace|subspace inclusion]] (Def. \ref{SubspaceTopology}) precisely if its [[naturality square]] of the $\sharp$-[[unit of an adjunction|unit]] 

$$
  \array{
    U &\overset{ \eta^\sharp_U }{\longrightarrow}& \sharp U
    \\
    {}^{\mathllap{i}}\Big\downarrow && \Big\downarrow{}^{\mathrlap{\sharp i}}
    \\
    X &\underset{\eta^\sharp_X}{\longrightarrow}& \sharp X
  }
$$

is a [[pullback]] square.

=--

+-- {: .proof}
###### Proof

By the [[universal property]] of a [[pullback]]/[[fiber product]] and the nature of $\sharp$, we have $U \simeq X \times_{\sharp X} \sharp U$ precisely if continuous functions out of some topological space $Z$ into $U$ are in [[natural bijection]] with continuous functions  $Z \to X$ whose underlying function $Z \to X \to \sharp X$ factors through the underlying function of $i$. This implies the statement by Prop. \ref{UniversalPropertyOfSupspaceInclusion}.

=--

### General

A subspace $i: Y \hookrightarrow X$ is **closed** if $Y$ is [[closed subset|closed]] as a subset of $X$ (or if $i$ is a [[closed map]]), and is **open** if $Y$ is open as a subset of $X$ (or if $i$ is an [[open map]]). 


+-- {: .num_prop #TopologicalEmbeddingsAreTheRegularMonos} 
###### Proposition 

Topological subspace inclusions ([[topological embedding]]) are precisely the [[regular monomorphisms]] in the [[category]] [[Top]] of all [[topological spaces]]. 

=-- 

For example, the [[equalizer]] of two maps $f, g \colon X \stackrel{\to}{\to} Y$ in [[Top]] is computed as the equalizer at the underlying-set level, equipped with the subspace topology. 

+-- {: .num_lemma #pushout} 
###### Lemma 
The [[pushout]] in [[Top]] of any (closed/open) subspace $i \colon A \hookrightarrow B$ along any [[continuous function]] $f \colon A \to C$, 

$$\array{
A & \stackrel{i}{\hookrightarrow} & B \\ 
\mathllap{f} \downarrow & po & \downarrow \mathrlap{g} \\ 
C & \underset{j}{\hookrightarrow} & D,
}$$ 

is a (closed/open) subspace $j: C \hookrightarrow D$. 
=-- 

+-- {: .proof} 
###### Proof 
Since $U = \hom(1, -): Top \to Set$ is [[faithful functor|faithful]], we have that monos are reflected by $U$; also monos and pushouts are preserved by $U$ since $U$ has both a [[left adjoint]] and a [[right adjoint]]. In $Set$, the pushout of a mono along any map is a mono, so we conclude $j$ is monic in $Top$. Furthermore, such a pushout diagram in $Set$ is also a pullback, so that we have the [[Beck-Chevalley condition|Beck-Chevalley equality]] $\exists_i \circ f^\ast = g^\ast \exists_j \colon P(C) \to P(B)$ (where $\exists_i \colon P(A) \to P(B)$ is the [[direct image]] map between [[power sets]], and $f^\ast: P(C) \to P(A)$ is the [[inverse image]] map). 

To prove that $j$ is a subspace, let $U \subseteq C$ be any open set. Then there exists open $V \subseteq B$ such that $i^\ast(V) = f^\ast(U)$ because $i$ is a subspace inclusion. If $\chi_U \colon C \to \mathbf{2}$ and $\chi_V \colon B \to \mathbf{2}$ are the maps to [[Sierpinski space]] that classify these open sets, then by the universal property of the pushout, there exists a unique continuous map $\chi_W \colon D \to \mathbf{2}$ which extends the pair of maps $\chi_U, \chi_V$. It follows that $j^{-1}(W) = U$, so that $j$ is a subspace inclusion. 

If moreover $i$ is an open inclusion, then for any open $U \subseteq C$ we have that $j^\ast(\exists_j(U)) = U$ (since $j$ is monic) and (by Beck-Chevalley) $g^\ast(\exists_j(U)) = \exists_i(f^\ast(U))$ is open in $B$. By the definition of the topology on $D$, it follows that $\exists_j(U)$ is open, so that $j$ is an open inclusion. The same proof, replacing the word "open" with the word "closed" throughout, shows that the pushout of a closed inclusion $i$ is a closed inclusion $j$. 
=-- 
 
A similar (but even simpler) line of argument establishes the following result. 

+-- {: .num_lemma #transfinite} 
###### Lemma 
Let $\kappa$ be an [[ordinal]], viewed as a [[preorder]] category, and let $F: \kappa \to Top$ be a functor that preserves [[directed colimits]]. Then if $F(i \leq j)$ is a (closed/open) subspace inclusion for each morphism $i \leq j$ of $\kappa$, then the canonical map $F(0) \to colim_{i \in \kappa} F(i)$ is also a (closed/open) inclusion. 
=-- 

## Variations

There is also a notion of a [[Grothendieck topology]] induced along a [[functor]] from a Grothendieck topology on another category (actually the input can be a somewhat more general [[coverage]], then the topology induced along the [[identity functor]] will serve as a sort of a completion). (this will be explained later).

A topology may be induced by more than a [[function]] other than a subset inclusion, or indeed by a family of functions out of $Y$ (not necessarily all with the same [[target]]). However, the term 'induced topology' is often (usually?) restricted to subspaces; the general concept is called a [[weak topology]].  (This construction can be done in any [[topological concrete category]]; in this generality it is often called an [[initial structure]] for a [[sink|source]].)  The dual construction (involving functions to $Y$) is a [[strong topology]] (or [[final structure]] for a [[sink]]); an example is the [[quotient topology]] on a [[quotient space]].

## Related concepts

* [[embedding]]

* [[embedding of topological spaces]]

* [[embedding of smooth manifolds]]

[[!include universal constructions of topological spaces -- table]]


## References

* {#Bourbaki71} [[Nicolas Bourbaki]], _Elements of Mathematics -- General topology_, 1971, 1990

* {#Munkres75} [[James Munkres]], _Topology_, Prentice Hall (1975, 2000)

* {#Terilla14} [[John Terilla]],  _Notes on categories, the subspace topology and the product topology_ 2014 ([pdf](https://math.mit.edu/~jhirsh/terilla_subspace_quotient.pdf))

[[!redirects subspace topology]]
[[!redirects subspace topologies]]

[[!redirects topological subspace]]
[[!redirects topological subspaces]]

[[!redirects subspace of a topological space]]
[[!redirects subspaces of a topological space]]

