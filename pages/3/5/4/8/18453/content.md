
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contentsrepre
* table of contents
{:toc}

## Idea

A _groupoid representation_ is a [[representation]] of a [[groupoid]].

## Definition

+-- {: .num_defn #GroupoidRepresentation}
###### Definition
**([[groupoid representation]])

Let $\mathcal{G}$ be a [[groupoid]]. Then:

A [[linear representation]] of $\mathcal{G}$ is a groupoid homomorphism ([[functor]])

$$
  \rho \;\colon\; \mathcal{G} \longrightarrow Core(Vect)
$$
   
to the groupoid [[core]] of the category [[Vect]] of [[vector spaces]] ([this example](groupoid#CoreGroupoid)). Hence this is
   
1. For each object $x$ of $\mathcal{G}$ a [[vector space]] $V_x$;

1. for each morphism $x \overset{f}{\longrightarrow} y$ of $\mathcal{G}$ a
   [[linear map]] $\rho(f) \;\colon\; V_x \to V_y$
   
such that

1. (respect for composition) for all composable morphisms $x \overset{f}{\to}y \overset{g}{\to} z$ in the groupoid we have an [[equality]]
   
   $$
     \rho(g) \circ \rho(f) = \rho(g \circ f)
   $$

1. (respect for identities) for each object $x$ of the groupoid we have an equality

   $$
     \rho(id_x) = id_{V_x}
     \,.
   $$

Similarly a _[[permutation representation]]_ of $\mathcal{G}$ is a groupoid homomorphism ([[functor]]) 

$$
  \rho \;\colon\; \mathcal{G} \longrightarrow Core(Set)
$$   

to the groupoid core of [[Set]]. Hence this is

1. For each object $x$ of $\mathcal{G}$ a [[set]] $S_x$;

1. for each morphism $x \overset{f}{\longrightarrow} y$ of $\mathcal{G}$ a
   [[function]] $\rho(f) \;\colon\; S_x \to S_y$
   
such that composition and identities are respected, as above.   

For $\rho_1$ and $\rho_2$ two such representations, then a homomorphism of representations

$$
  \phi \;\colon\; \rho_1 \longrightarrow \rho_2
$$

is a [[natural transformation]] between these functors, hence is

* for each object $x$ of the groupoid a (linear) function
 
  $$
    (V_1)_x \overset{\phi(x)}{\longrightarrow} (V_2)_x
  $$

* such that for all morphisms $x \overset{f}{\longrightarrow} y$
  we have
  
  $$
    \phi(y) \circ \rho_1(f) = \rho_2(x) \circ \phi(x)
    \phantom{AAAAAA}
    \array{
      (V_1)_x &\overset{\phi(x)}{\longrightarrow}& (V_2)_x
      \\
      {}^{\mathllap{\rho_1(f)}}\downarrow && \downarrow^{\mathrlap{\phi_2(f)}}
      \\
      (V_1)_y &\underset{\phi(y)}{\longrightarrow}& (V_2)_y
    }
  $$

A permutation representation of $\mathcal{G}$ is often called a "$\mathcal{G}$-set" (see at _[[G-set]]_) and the category of permutation representations is also often denoted

$$
  \mathcal{G}Set
  \phantom{AAAAA}
  \text{or}
  \phantom{AAAAA}
  Set^{\mathcal{G}}
$$



=--

## Properties

+-- {: .num_cor #GroupoidRepresentationsAreProductsOfGroupRepresentations}
###### Corollary
**([[groupoid representations]] are [[product category|products]] of [[group representations]])

Assuming the [[axiom of choice]] then the following holds:

Let $\mathcal{G}$ be a [[groupoid]]. Then its [[category of representations|category of]] groupoid representations is [[equivalence of categories|equivalent]] to the [[product category]] indexed by the set of [[connected components]] $\pi_0(\mathcal{G})$ ([this def.](groupoid#GroupoidConnectedComponents)) of [[group representations]]  of the [[automorphism group]] $G_i \coloneqq Aut_{\mathcal{G}}(x_i)$ ([this def.](groupoid#InGrupoidAutomorphismGroup)) for $x_i$ any object in the $i$th connected component:

$$
  Rep_{Grpd}(\mathcal{G})
   \;\simeq\;
  \underset{i \in \pi_0(\mathcal{G})}{\prod} Rep(G_i)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Let $\mathcal{C}$ be the category that the representation is on. Then by definition

$$
  Rep_{Grpd}(\mathcal{G}) = Hom( \mathcal{G} , \mathcal{C}  )
  \,.
$$

Consider the injection functor of the [[skeleton]] (from [this lemma](groupoid#DeloopingGroupoidEquivalence))

$$
  inc
  \;\colon\;
  \underset{i \in \pi_0(\mathcal{G})}{\sqcup} B G_i
  \overset{}{\longrightarrow}
  \mathcal{G}
  \,.
$$


By [this lemma](groupoid#HmotopiesWithMorphismsHorizontaComposition) the pre-composition with this constitutes a functor

$$
  inc^\ast \;\colon\; Hom( \mathcal{G}, \mathcal{C} ) \longrightarrow Hom( \underset{i \in \pi_0(\mathcal{G})}{\sqcup} B G_i, \mathcal{C} )
$$

and by combining [this lemma](groupoid#DeloopingGroupoidEquivalence) with [this lemma](groupoid#HorizontalCompositionWithHomotopyIsNaturalTransformation)
this is an [[equivalence of categories]]. Finally, by [this example](groupoid#GroupoidRepresentationOfDeloopingGroupoid) the 
category on the right is the product of group representation categories as claimed.



=--



## Examples


+-- {: .num_example #GroupoidRepresentationOfDeloopingGroupoid}
###### Example
**([[groupoid representation]] of [[delooping]] groupoid is [[group representation]])

If $B G$ is the [[delooping]] groupoid of a [[group]] $G$ ([this example](groupoid#GroupoidFromDelooping)),
then a [[groupoid representation]] of $B G$ according to def. \ref{GroupoidRepresentation} is
equivalently a [[group representation]] of the group $G$:

$$
  Rep_{Grpd}(B G) \simeq Rep(G)
  \,.
$$

=--

+-- {: .num_example }
###### Example
**([[fundamental theorem of covering spaces]])**

For $X$ a [[topological space]] then forming [[monodromy]] is a [[functor]] from the [[category of covering spaces]] over $X$ to that of [[permutation representations]] of the [[fundamental groupoid]] of $X$:

$$
  Fib \;\colon\; Cov(C)  \longrightarrow Set^{\Pi_1(X)}
  \,.
$$

If $X$ is [[locally path-connected topological space|locally path connected]] and [[semi-locally simply connected topological space|semi-locally simply connected]], then this is an [[equivalence of categories]]. See at _[[fundamental theorem of covering spaces]]_ for details.

=--

## References

* [[Alberto Ibort]], [[Miguel A. Rodriguez]]: *An Introduction to Groups, Groupoids and Their Representations*, CRC Press (2021) &lbrack;[ISBN:9781032086767](https://www.routledge.com/An-Introduction-to-Groups-Groupoids-and-Their-Representations/Ibort-Rodriguez/p/book/9781032086767?srsltid=AfmBOoqc0EH7Qjc1_0C-TYQtUbhTWpdb3Juy61vwE9TfRC5oaJwjlYfN), [doi:10.1201/b22019](https://doi.org/10.1201/b22019)&rbrack;




[[!redirects groupoid representations]]

[[!redirects representation of groupoids]]
[[!redirects representations of groupoids]]
