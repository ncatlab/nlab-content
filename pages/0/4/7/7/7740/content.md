
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition
 {#Definition}

We define general non-linear differential operators.

### In differential geometry
 {#DefinitionInDifferentialGeometry}

Depending on which definition of differential operators one regards as fundamental, the following are either definitions or are propositions.

+-- {: .num_defn #DifferentialOperatorViaJetBundles}
###### Definition/Proposition

For $X$ a [[smooth manifold]] and $(E\to X)$ a smooth [[bundle]] over $X$, write $(Jet(E)\to X)$ for its [[jet bundle]].

For $(E_1 \to X)$, $(E_2 \to X)$
two [[bundles]] over $X$, then a _differential operator_ 

$$
  D \colon \Gamma_X(E_1) \to \Gamma_X(E_2)
$$ 

between their [[spaces of sections]] is equivalently a map of the form

$$
  \phi \mapsto \tilde D \circ j_\infty(\phi)
$$

where $j_\infty(\phi) \in \Gamma_X(Jet(E_1))$ is the jet prolongation of the section $\phi \in \Gamma_X(E_1)$, and where

$$
  \tilde D \colon Jet(E_1) \to E_2
$$

is a bundle morphism from the [[jet bundle]] of $E_1$ to the bundle $E_2$.

=--

In this form this appears for instance as ([Saunders 89, def. 6.2.22](#Saunders89)).  Discussion showing the equivalence of this definition with the maybe more traditional definition is in ([Krasil'shchikVerbovetsky 98, def. 1.1, prop. 1.1, prop. 1.9](#KrasilshchikVerbovetsky98), [Krasilshchik 99, theorem 10](#Krasilshchik99)).

+-- {: .num_remark }
###### Remark

The [[jet bundle]] construction $Jet \colon \mathbf{H}_{/X} \to \mathbf{H}_{/X}$ is (by the discussion there) a [[comonad]] on the category of bundles over $X$. In terms of this def. \ref{DifferentialOperatorViaJetBundles} says that a differential operators from a bundle $E_1$ to a bundle $E_2$ is a morphism from $E_1$ to $E_2$ in the [[co-Kleisli category]] of the jet comonad.

=--

Indeed, also the composition of differential operators is the composition in this [[co-Kleisli category]] (e.g. [Marvan 93, section 1.1](#Marvan93)):

+-- {: .num_prop #CompositionOfDifferentialOperatorsViaCoKleisli}
###### Proposition

The [[composition]] $D_2 \circ D_1 \colon \Gamma_X(E_1) \to \Gamma_X(E_3)$ of two differential operators $D_1 \colon \Gamma_X(E_1) \to \Gamma_X(E_2)$ and $D_2 \colon \Gamma_X(E_2)\to \Gamma_X(E_3)$ , def. \ref{DifferentialOperatorViaJetBundles}, is given,under the identification of def. \ref{DifferentialOperatorViaJetBundles}, by the composite

$$
  \widetilde{D_2 \circ D_1}
  \;\colon\;
  Jet(E_1)
  \longrightarrow
  Jet(Jet(E_1))
  \stackrel{Jet(\tilde D_1)}{\longrightarrow}
  Jet(E_2)
  \stackrel{\tilde D_2}{\longrightarrow}
  E_3
  \,,
$$

where the first morphism is the [[counit of a comonad|counit]] of the [[jet bundle]] [[comonad]].

=--

+-- {: .proof}
###### Proof

Abbreviating $P_i \coloneqq \Gamma_X(E_i)$ and $J^\infty(P_i) = \Gamma_X(Jet(E_i))$, consider the following pasting diagram:


$$
  \array{
    P_1 &\stackrel{id}{\longrightarrow}& P_1 &\stackrel{D_1}{\longrightarrow}& P_2 &\stackrel{D_2}{\longrightarrow}& P_3
    \\
    \downarrow^{\mathrlap{id}} 
      && 
    \downarrow^{\mathrlap{j_\infty}} 
      && 
    \downarrow^{\mathrlap{j_\infty}} 
      && 
    \downarrow^{\mathrlap{id}}
    \\
    P_1 
     &\stackrel{j_\infty}{\longrightarrow}& 
    J^\infty(P_1)
    &\stackrel{J^\infty(D_1)}{\longrightarrow}&
    J^\infty(P_2)
    \\
    \downarrow^{\mathrlap{j_\infty}} 
      && 
    \downarrow^{\mathrlap{j_\infty}}
      &&
    \downarrow^{\mathrlap{id}}
      &&
    \downarrow^{\mathrlap{id}}
    \\
    J^\infty (P_1) 
      &\stackrel{c^{\infty,\infty}}{\longrightarrow}& 
    J^\infty(J^\infty(P_1))
     &\stackrel{J^\infty (\tilde D_1)}{\longrightarrow}&
    J^\infty(P_2)
     &\stackrel{\tilde D_2}{\longrightarrow}&
    P_3
  }
  \,.
$$

Here all the nontrivial squares are as in ([Krasil'shchik-Verbovetsky 98, p. 12-13](#KrasilshchikVerbovetsky98)), with the bottom middle square being the image under $J^\infty$ of the square defining $\tilde D_1$. The bottom horizontal fillers of these squares are unique by ([Krasil'shchik 99, theorem 10](#Krasilshchik99)) (which is just our def/prop. \ref{DifferentialOperatorViaJetBundles}), hence the identification of the middle bottom morphism as displayed in the diagram.

With this, the morphism that our proposition claims is the correct composite is the total bottom morphism, and the differential operator that this defines by def. \ref{DifferentialOperatorViaJetBundles} is the further composite with the left vertical morphism. Therefore the commutativity of the total diagram gives that this is equal to the total top morphisms, which is the composite of the two differential operators as claimed.

=--

The co-Kleisli-like composition for finite order differential operators also appears in ([Kock 10, section 7.3](#Kock10)), from a perspective of [[synthetic differential geometry]].

### In differential cohesion
 {#DefinitionInDifferentialCohesion}

In view of the [above](#DefinitionInDifferentialGeometry) one may axiomatize the category of differential operators in any context $\mathbf{H}$ of [[differential cohesion]] with [[infinitesimal shape modality]] $\Im$ as being the [[co-Kleisli category]] of the [[jet comonad]] 

$$
  Jet_X \coloneqq i^\ast i_\ast
$$

induced by [[base change]] along the [[unit of a monad|unit]] $i \colon X \to \Im X$, for any choice of base space $X \in \mathbf{H}$.

### In algebraic geometry / D-geometry

For the case of [[algebraic geometry]], where $\Im X$ is known as the [[de Rham stack]] of a [[scheme]] $X$, and the [[quasicoherent sheaves]] on $i^\ast i_\ast X$ are the [[D-modules]] over $X$ (see at _[[jet bundle]]_ for more on this), this statement is implicit in ([Saito 89, def. 1.3](#Saito89)).

## Properties

+-- {: .num_prop #RetainsOrShrinksWaveFrontSetDifferentialOperator}
###### Proposition
**([[differential operator]] preserves or shrinks [[wave front set]])**

Let $P$ be a [[differential operator]] (with [[smooth function|smooth]] [[coefficients]]). Then for $u \in \mathcal{D}'$ a [[distribution]], the [[wave front set]] of the [[derivative of distributions]] $P u$ is contained in the original wave front set of $u$:

$$
  WF(P u) \subset WF(u)
  \,.
$$

=--

([Hörmander 90, (8.1.11)](#Hoermander90))


## Types of differential operators

* [[elliptic differential operator]]

* [[regular differential operator]], [[regular differential operator in noncommutative geometry]]

* [[pseudodifferential operator]]

* [[chiral differential operator]]

* [[crystalline differential operator]]


## Related concepts

* [[formally adjoint differential operator]]

* [[symbol of a differential operator]]

* [[index of a differential operator]]

* [[formal adjoint differential operator]]

* [[D-module]]

* [[Spencer cohomology]]

## References

A coordinate-free definition of a linear differential operator suitable for [[algebraic geometry]] was introduced by [[Grothendieck]] in Proposition IV.16.8.8(b) of

* [[A. Grothendieck]], [[J. Dieudonné]]. _[[Éléments de géométrie algébrique]] IV. Étude locale des schémas et des morphismes des schémas, Quatrième partie_, Publications Mathematiques de l’IHÉS 32, 5–361, 1967.


* {#Marvan86} [[Michal Marvan]], _A note on the category of partial differential equations_, in _Differential geometry and its applications_, Proceedings of the Conference August 24-30, 1986, Brno ([[MarvanJetComonad.pdf:file]])

  (notice that prop. 1.3 there holds only when the equalizer exists in the first place)

* {#Saunders89} [[David Saunders]], _The geometry of jet bundles_, London Mathematical Society Lecture Note Series __142__, Cambridge Univ. Press 1989.

* {#Saito89} [[Morihiko Saito]], _Induced D-modules and differential complexes_, Bull. Soc. Math. France 117 (1989), 361&#8211;387, [pdf](http://smf4.emath.fr/Publications/Bulletin/117/pdf/smf_bull_117_361-387.pdf)

* {#Hoermander90} [[Lars Hörmander]], _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990


* {#Marvan93} [[Michal Marvan]], _On Zero-Curvature Representations of Partial Differential Equations_,  (1993) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.45.5631))


* {#KrasilshchikVerbovetsky98} [[Joseph Krasil'shchik]], [[Alexander Verbovetsky]], _Homological Methods in Equations of Mathematical Physics_,  Lectures given in August 1998 at the International Summer School in Levoca, Slovakia ([arXiv:math/9808130](http://arxiv.org/abs/math/9808130))

* {#Krasilshchik99} [[Joseph Krasil'shchik]] in collaboration with Barbara Prinari, _Lectures on Linear Differential Operators over Commutative Algebras_ ([pdf](https://diffiety.mccme.ru/preprint/99/01_99.pdf))

Discussion from a point of view of [[synthetic differential geometry]] is in 

* {#Kock10} [[Anders Kock]], _Synthetic geometry of manfiolds_, Cambridge Tracts in Mathematics 180 (2010). ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))

[[!redirects differential operators]]

[[!redirects linear differential operator]]
[[!redirects linear differential operators]]

