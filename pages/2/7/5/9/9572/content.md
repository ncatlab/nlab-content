
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


\tableofcontents



## Idea

The notion of the _center of a monoidal category_ or the _Drinfeld center_ is a [[categorification]] of the notion of the [[center]] of a [[monoid]]([[associative algebra]], [[group]], etc.) from monoids to [[monoidal categories]].

Where the [[center]] of a monoid is just a sub-monoid with the [[property]] that it commutes with everything else, under categorification this becomes a [[stuff, structure, property|structure]], since we have to specify _how_ the objects in the Drinfeld center commute ([[braided monoidal category|braid]]) with everything else.

## Definition

We first give the general-abstract definition

* [Abstract definition](#AbstractDefinition)

of Drinfeld centers. Then we spell out what this means in components in 

* [Definition in components](#DefinitionInComponents).


### Abstractly
 {#AbstractDefinition}


+-- {: .num_defn}
###### Definition

For $(\mathcal{C}, \otimes)$ a [[monoidal category]], write $\mathbf{B}_\otimes \mathcal{C}$ for its [[delooping]], the pointed [[2-category]] with a single [[object]] $*$ such that $Hom_{\mathbf{B}_\otimes \mathcal{C}}(*, *) \simeq \mathcal{C}$.

The **Drinfeld center** $Z(\mathcal{C}, \otimes)$ of $(\mathcal{C}, \otimes)$ is the [[monoidal category]] of [[endofunctor|endo]]-[[pseudonatural transformations]] of the [[identity]]-[[2-functor]] on $\mathbf{B}_\otimes \mathcal{C}$:

$$
  Z(\mathcal{C}, \otimes)
  \coloneqq
  End_{\mathbf{B}_\otimes \mathcal{C}}(id_{\mathbf{B}_\otimes \mathcal{C}})
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Unwinding the definitions, we find that an [[object]] of $Z(\mathcal{C}, \otimes)$, $\Phi \colon id_{\mathbf{B}_\otimes \mathcal{C}} \to id_{\mathbf{B}_\otimes \mathcal{C}}$, has for components  pseudonaturality squares

$$
  \array{
    \ast &\stackrel{X \coloneqq \Phi(\ast)}{\to}& \ast
    \\
    {}^{\mathllap{Y}}\downarrow &\swArrow_{\Phi_Y}& \downarrow^{\mathrlap{Y}}
    \\
    \ast
    &\underset{X = \Phi(\ast)}{\to}&
    \ast
  }
$$

for each $Y \in Obj(\mathcal{C})$. As shown, these consist of a choice of an object $X \in \mathcal{C}$ together with a [[natural isomorphism]]

$$
  \Phi_{(-)} \colon X \otimes (-) \to (-) \otimes X
$$

in $\mathcal{C}$.

The [[transfor]]-property of $\Phi$ says that 

$$
  \array{
    \ast &\stackrel{X \coloneqq \Phi(\ast)}{\to}& \ast
    \\
    {}^{\mathllap{Y}}\downarrow &\swArrow_{\Phi_Y}& \downarrow^{\mathrlap{Y}}
    \\
    \ast
    &\underset{X = \Phi(\ast)}{\to}&
    \ast
    \\
    {}^{\mathllap{Z}}\downarrow &\swArrow_{\Phi_Z}& \downarrow^{\mathrlap{Z}}
    \\
    \ast
    &\underset{X = \Phi(\ast)}{\to}&
    \ast
  }
  \;\;\;\;
  \simeq
  \;\;\;\;
  \;\;\;\;
  \array{
    \ast &\stackrel{X \coloneqq \Phi(\ast)}{\to}& \ast
    \\
    {}^{\mathllap{Y \otimes Z}}\downarrow &\swArrow_{\Phi_{Y \otimes Z}}& \downarrow^{\mathrlap{Y \otimes Z}}
    \\
    \ast
    &\underset{X = \Phi(\ast)}{\to}&
    \ast
  }
  \,.
$$

And so forth. Writing this out in terms of $(\mathcal{C}, \otimes)$ yields the following component characterization of Drinfeld centers, def. \ref{CompDef}.

=--



### In components
 {#DefinitionInComponents}

+-- {: .num_defn #CompDef}
###### Definition

Let $(\mathcal{C}, \otimes)$ be a [[monoidal category]]. Its **Drinfeld center** is a [[monoidal category]] $Z(\mathcal{C})$ whose

* [[objects]] are pairs $(X, \Phi)$ of an object $X \in \mathcal{C}$ and a [[natural isomorphism]] (the *half-braiding*)

  $$
    \Phi_{(-)}
      \;\colon\; 
    X \otimes (-) \longrightarrow (-) \otimes X
  $$

  such that for all $Y \in \mathcal{C}$ we have 

  $$
    \Phi_{Y \otimes Z}
    =
    \big(id_Y \otimes \Phi_Z\big) 
      \circ   
    \big(\Phi_Y \otimes id_Z \big) 
  $$

* [[morphisms]] are given by

  $$
    Hom\big((X, \Phi), (Y,\Psi)\big)
    =
   \Big\{
     f \in Hom_{\mathcal{C}}(X,Y)
     \;\big|\;
     (id \otimes f) \circ \Phi_Z
     = 
     \Psi_Z \circ (f \otimes id), \; \forall Z \in \mathcal{C}
   \Big\}
   \,.
  $$

* the [[tensor product]] is given by 
 
  $$
    (X, \Phi) \otimes (Y, \Psi) 
      \;=\; 
    \big(
       X \otimes Y, 
      (\Phi \otimes id_Y) \circ (id_X \otimes \Psi)
    \big)
    \,.
  $$

=--

## Properties

### Extra structure on the Drinfeld center

+-- {: .num_prop}
###### Proposition

The Drinfeld center $Z(\mathcal{C})$ is naturally a [[braided monoidal category]]. 

=--


\begin{proposition}
\label{DrinfeldCenterOfFusionCategory}
If $\mathcal{C}$ is a [[fusion category]] 
over an [[algebraically closed field]] of [[characteristic zero]],
then the Drinfeld center $Z(\mathcal{C})$ is also naturally a fusion category.
\end{proposition}

([Etingof, Nikshych & Ostrik 2005, Thm. 2.15](#EtingofNikshychOstrik05), review in [Davydov, Mueger, Nikshych & Ostrik 2003, Sec. 2.3](#DavydovMuegerNikshychOstrik03), see also [Drinfeld, Gelaki, Nikshych & Ostrik 2010, Cor. 3.9](#DrinfeldGelakiNikshychOstrik10), [Mueger 2003](#Mueger03), [EGNO 2015, Thm. 9.3.2](#EGNO15)).


### Relation to Drinfeld double
 {#RelationToDrinfeldDouble}

Under [[Tannaka duality]], forming the Drinfeld center of a [[category of modules]] of some [[Hopf algebra]] corresponds to forming the category of modules over the corresponding [[Drinfeld double]] algebra (cf. [EGNO15, §7.14](#EGNO15)).


[[!include structure on algebras and their module categories - table]]


## Examples
 {#Examples}

### Of $G$-graded vector spaces
 {#DrinfeldCenterOfGGradedVectorSpaces}

The archetypical example of Drinfeld centers is that of the of the category of [[finite-dimensional vector space|finite-dimensional]] $G$-[[graded vector spaces]] for a group $G$.

This is also known as the representation category of the *[[Drinfeld double]]* of $G$. 

We spell out the characterization of the [[simple objects]] (Prop. \ref{SimpleObjectsInDrinfeldCenterOfGGradedVectorSpaces}, which is classical, cf. [EGNO 2015 Example 8.5.4. in](#EGNO15)) and also the fusion coefficients (Prop. \ref{FusionCoefficientInDrinfeldCenterOfGVectorSpaces}, which may not be in the literature, but cf. [Li 2026](Drinfeld+double#Li2026)).


#### The fusion category

We start by recalling definitions and establishing notation:

By $\mathrm{Vec} \coloneqq \big({\mathrm{FD}\mathbb{C}\mathrm{Vec}, \otimes, \mathbb{C}}\big)$ we denote the [[monoidal category]] of [[finite-dimensional vector space|finite-dimensional]] [[complex vector spaces]] with the usual [[tensor product of vector spaces]]. For $G$ a [[group]], the monoidal category $\mathrm{Vec}_G$ of *$G$-[[graded vector spaces]]* has:

1. as [[objects]] [[vector spaces]] $V \in \mathrm{Vec}$ equipped with $G$-[[indexed set|indexed]] [[direct sum]] decomposition

   $$  
     V
     \equiv
     \bigoplus_{g \in G}
     V_g
     \mathrlap{\,,}
   $$

1. as [[morphisms]] [[linear maps]] that respect the $G$-grading,

1.  as [[monoidal category|monoidal]] [[structure]] $\widetilde \otimes$ the  [[tensor product of vector spaces|ordinary tensor product]] but equipped with the [[convolution]] grading:
   \[\label{TensorProductOnGradedVectorSpaces}
     \big(V \widetilde\otimes W\big)_g
     \coloneqq
     \bigoplus_{k \in G}
     \big({
       V_{k} \otimes W_{k^{-1} g}
     }\big)
     \mathrlap{\,.}
   \]

   We will be referring to $\widetilde\otimes$, and its incarnation (eq:TensorProductInDrinfeldCenterOfVecG) in the Drinfeld center, as the *fusion product*, to be distinguished from the degreewise tensor product (cf. also Rem. \ref{DrinfeldCenterNotMonoidallyEquivalent} below).

Equivalently, with 

$$
  C(G) \in HopfAlg
$$

denoting the [[Hopf algebra|Hopf]] [[algebra of functions]] $G \to \mathbb{C}$ (with product the pointwise product of functions and with [[coproduct]] induced by [[precomposition]] of functions with the [[binary operation|group multiplication]]), we have that $Vec_G$ is [[equivalence of categories|equivalent]] (as a [[monoidal category]]) to the [[category of modules]] of $C(G)$:

$$
  Vec_G \simeq Mod\big(C(G))
  \mathrlap{\,.}
$$

(The pointwise product in $C(G)$ induces the $G$-grading and the coproduct induces the [[convolution product|convolution]] in (eq:TensorProductOnGradedVectorSpaces).)

For example, with $X \in \mathrm{Vec}$ an ungraded vector space and $g_0 \in G$ a group element, we write
\[
  \label{GradedVectorSpaceConcentratedInSingleDegree}
  X \delta_{g_0}
  \in 
  \mathrm{Vec}_G
  \,,
  \;\;\;
  ({X \delta_{g_0}})_g
  \coloneqq
  \left\{
  \begin{array}{ll}
    X & \text{if}\;g = g_0
    \\
    0 & \text{otherwise}
  \end{array}
  \right.
\]
for the $G$-graded vector space which is concentrated on $X$ in degree $g_0$.

Now, the *Drinfeld center* $\mathcal{Z}({\mathrm{Vec}_G})$ is, by its general definition (Def. \ref{CompDef}, but we now change the conventuion for the handedness of the half-braiding in order to end up with *left* group actions), the [[monoidal category]] which has:

1. as [[objects]] [[pairs]], $(V,\beta)$, consisting of a $V \in \mathrm{Vec}_G$ and a [[natural isomorphism]] (the \emph{half-braiding})

   \[
     \label{TheHalfBraiding}
     \beta_{(-)}
     \,\colon\,
     (-) \widetilde\otimes V
     \xrightarrow{ \sim }
     V \widetilde\otimes (-)
     \mathrlap{\,,}
   \]

   satisfying for all $W, W' \in \mathrm{Vec}_G$ the relation
   \[
     \label{CoherenceOfHalfBraiding}
     \beta_{W \widetilde\otimes W'}
     =
     \big({
       \beta_{W} \widetilde\otimes \mathrm{id}_{W'}
     }\big)
       \circ
     \big({
       \mathrm{id}_{W} \widetilde\otimes \beta_{W'}
     }\big)
     \mathrlap{\,,}
   \]

1. as [[morphisms]] $(V,\beta) \to (V',\beta')$ [[linear maps]] $f \colon V \to V'$ such that for all $W \in \mathrm{Vec}_G$ we have
  \[
    \label{ConditionOnMorphismsInDrinfeldCenter}
    \beta'_W
    \circ
    \big(
      id_W \widetilde\otimes f
    \big)
    =
    \big(
      f \widetilde\otimes id_{W}
    \big)
    \circ
    \beta_W
    \mathrlap{\,,}
  \]

1. as [[tensor product]] $\widetilde\otimes$ the operation which on the graded vector spaces is the convolution product $\widetilde\otimes$ from (eq:TensorProductOnGradedVectorSpaces), extended to the half-braiding as follows:
   \[\label{TensorProductInDrinfeldCenterOfVecG}
     (V,\beta)
     \widetilde\otimes
     (V',\beta')
     =
     \big({
       V \widetilde\otimes V',
       (\mathrm{id}_{V} \widetilde\otimes \beta')
       \circ
       (\beta \widetilde\otimes \mathrm{id}_{V'})
     }\big)
     \mathrlap{\,.}
   \]



#### Simple objects as inertia irreps

The above general definition of Drinfeld center applied to the case of $Vec_G$ may be further simplified:

Since every [[vector space]] is [[isomorphism|isomorphic]] to a [[direct sum]] of copies of [[complex numbers|$\mathbb{C}$]], the linear maps $\beta_{(-)}$ (eq:TheHalfBraiding) are determined already by their values on $\mathbb{C} \delta_{g_0}$ (eq:GradedVectorSpaceConcentratedInSingleDegree); and if we understand that $\mathbb{C} \otimes V = V$, then, by degree reasons, their $g_0 g$-components must be [[linear isomorphisms]] $g_0 \cdot (-)$ of this form:

\begin{tikzcd}
    \big({
      \mathbb{C} \delta_{g_0}
        \widetilde\otimes 
      V 
    }\big)_{g_0 g}
    \ar[
      r,
      "{ 
        ({
          \beta_{\mathbb{C}\delta_{g_0}} 
        })_{g_0 g}
      }"
    ]
    \ar[d, equals]
    &
    \big({
      V
        \widetilde\otimes 
      \mathbb{C}\delta_{g_0} 
    }\big)_{g_0 g}
    \ar[d, equals]
    \\
    V_{g} 
    \ar[r, "{ g_0\cdot(-) }"]
      &
    V_{g_0 g g_0^{-1}}
    \mathrlap{\,.}
\end{tikzcd}

For these, the coherence condition (eq:CoherenceOfHalfBraiding) reduces to the *[action property](action#ActionPropertyOfGroupActions)*
\[
  g_2 \cdot \big({g_1 \cdot (-)}\big)
  =
  (g_2 g_1) \cdot (-)
  \mathrlap{\,.}
\]
This way, the objects of $\mathcal{Z}({\mathrm{Vec}_G})$ are [[bijection|bijectively]] identified with (complex, finite-dimensional) *[[groupoid representations]]* of the [[action groupoid]]
$$
  \Lambda G
  \coloneqq
  G\sslash_{\!\mathrm{Ad}} G
$$
of the [[adjoint action]] of $G$ (its *[[inertia groupoid]]*):

\begin{tikzcd}[sep=0pt]
    \Lambda G
    \ar[
      rr
    ]
    &&
    \mathrm{Vec}
    \\
    g
    \ar[
      d,
      "{ g_1 }"
    ]
    &\mapsto&
    V_g
    \ar[
      d,
      "{ g_1 \cdot }"
    ]
    \\[20pt]
    g_1
    g 
    g_1^{-1}
    &\mapsto&
    V_{g_1 g g_1^{-1}}
    \mathrlap{\,.}
\end{tikzcd}

In this representation-theoretic description, the morphisms (eq:ConditionOnMorphismsInDrinfeldCenter) of $\mathcal{Z}(\mathrm{Vec}_G)$ are equivalently the [[homomorphisms]] of [[groupoid representations]] (the *[[intertwiners]]*). This shows that:

\begin{proposition}
For $G$ a [[group]], the [[Drinfeld center]] of [[graded vector spaces|$\mathrm{Vec}_G$]] is [[equivalence of categories|equivalently]] the [[representation category]] of the [[inertia groupoid]] of $G$:
  \[
    \label{DrinfeldCenterAsAdjointActionGroupoidRepresentations}
    \mathcal{Z}({\mathrm{Vec}_G})
    \simeq
    \mathrm{Rep}({
      \Lambda G
    })
    \mathrlap{\,.}
  \]
\end{proposition}


The [[equivalence of categories|equivalence]] (eq:DrinfeldCenterAsAdjointActionGroupoidRepresentations) implies at once that the *[[simple objects]]* in $\mathcal{Z}({\mathrm{Vec}_G})$ (those admitting no nontrivial [[direct sum]] decomposition) are [[support|supported]] on [[conjugacy classes]] of group elements
\[
  [g]
  \coloneqq
  \big\{
    g^k
     \coloneqq
    k g k^{-1}
  \big\vert
    k \in G
  \big\}
  \mathrlap{\,,}
\]
where they form an ([[irreducible representation|irreducible]]) [[groupoid representation]] of the [[connected component]] $[g] \sslash_{\!\mathrm{Ad}} G \subset G\sslash_{\!\mathrm{Ad}} G$. 
Since these connected groupoids are [[equivalence of categories|equivalent]] to the [[delooping groupoid|delooping]] of their [[isotropy group]], $[g] \sslash_{\!\mathrm{Ad}} G \simeq \mathbf{B}Z_G(g)$ (cf. [this prop.](groupoid#EveryGroupoidIsEquivalentToDisjointUnionOfGroupDeloopings)), these [[groupoid representations]] are [[equivalence of categories|equivalently]] [[irreducible representation|irreducible]] [[linear representations]] of the [[centralizer group]] $Z_G(g)$:

\begin{proposition}
\label{SimpleObjectsInDrinfeldCenterOfGGradedVectorSpaces}
The [[simple objects]] of $\mathcal{Z}({\mathrm{Vec}_G})$ are [[pairs]] $([g],\rho)$ consisting of a [[conjugacy class]] $[g]$ and an [[irrep]] of [[centralizer subgroup|$Z_G(g)$]]:

\[
  \Big\{
    \text{simple objects}
  \Big\}
  \;\simeq\;
  \bigsqcup_{\mathclap{
    \substack{
      [g] \in
      \\
      \mathrm{Conj}(g)
    }
  }}
  \mathrm{Irr}\big({
    [g]\sslash_{\!\mathrm{Ad}}
    G
  }\big)
  \;\simeq\;
  \bigsqcup_{\mathclap{
    \substack{
      [g] \in
      \\
      \mathrm{Conj}(g)
    }
  }}
  \mathrm{Irr}\big({
    Z_G(g)
  }\big)
  \mathrlap{\,.}
\]
\end{proposition}



#### The fusion product

\begin{remark}\label{DrinfeldCenterNotMonoidallyEquivalent}
Beware that the above equivalence (eq:DrinfeldCenterAsAdjointActionGroupoidRepresentations) is *not* a [[strong monoidal functor|monoidal]] equivalence, as the standard tensor product on groupoid representations is degree-wise, not convolutive as in (eq:TensorProductOnGradedVectorSpaces).
\end{remark}

Instead, the fusion product in the Drinfeld center is category-theoretically given as follows:
\begin{lemma}\label{FusionViaPullPush}
  For a pair of objects $F_1,F_2 \in \mathrm{Rep}(\Lambda G) \simeq \mathcal{Z}({\mathrm{Vec}_G})$ (eq:DrinfeldCenterEquivalentToInertiaGroupoidReps), their fusion tensor product $\widetilde\otimes$ (eq:TensorProductInDrinfeldCenter) is equivalently given by the following pull-tensor-push operation:
  $$
    \begin{array}{ccc}
      ({
        G\sslash_{\!\mathrm{Ad}}G
      })
      \times
      ({
        G\sslash_{\!\mathrm{Ad}}G
      })
      &
      \xleftarrow{
          (\mathrm{pr}_1,\mathrm{pr}_2)
        }
      &
      ({G \times G})
      \sslash_{\!\mathrm{Ad}}G
      &
      \xrightarrow{ 
          m \coloneqq
          (-)\cdot(-) 
        }
      &
      G\sslash_{\!\mathrm{Ad}}G
      \\
      ({F,F'})
      &\mapsto&
      &\mapsto&
      m_!\big({
        ({\mathrm{pr}_1^\ast F})
        \otimes
        ({\mathrm{pr}_2^\ast F})
      }\big)
    \end{array}
  $$
  in that there is a [[natural isomorphism]]
  \[
    F_1 \widetilde\otimes F_2
    \simeq
      m_!\big({
        ({\mathrm{pr}_1^\ast F})
        \otimes
        ({\mathrm{pr}_2^\ast F})
      }\big)    
    \mathrlap{\,.}
  \]
\end{lemma}
\begin{proof}
  Since the functor $m$ is a Kan fibration, the left base change $m_!$ is given by forming the direct sum over fibers. (It is immediate to check the universal property of the left adjoint explicitly.) This reproduces the definition (eq:TensorProductOnGradedVectorSpaces). The induced $G$-action on these direct sums is the diagonal one, which under the equivalence (eq:DrinfeldCenterAsAdjointActionGroupoidRepresentations) reproduces the definition (eq:TensorProductInDrinfeldCenterOfVecG). 
\end{proof}


To determine concretely the convolution tensor product $\widetilde{\otimes}$ of a pair of such simple objects, we first need:
\begin{lemma}
  \label{OnTheDecompositionOfProductOrbits}
  For $g,g' \in G$, with $[g] \times [g'] \subset G^2$ denoting the [[Cartesian product]] of their [[conjugacy classes]] (eq:ConjugacyClass), the [[action groupoid]] of the [[diagonal action|diagonal]] [[adjoint action]] is [[equivalence of categories|equivalent]] to the following [[disjoint union]] of [[delooping groupoids]]:
\[
  \label{DecompositionProductOrbits}
  \big({
    [g]
      \times
    [g']
  }\big)
  \sslash_{\!\mathrm{Ad}} G
  \;\;\simeq\;\;
  \bigsqcup_{\mathclap{
    \substack{
      [c] \in
      \\
      \mathrm{Conj}(G)
    }
  }}
  \;\;\;
  \bigsqcup_{
    \substack{
      [k,k'] \in R
      \\
      g^k g'^{k'} = c
    }
  }
  \mathbf{B}\big({
    Z_G(g^k,g'^{l'}) 
  }\big)
  \mathrlap{\,,}
\]
where $R$ denotes the following [[double coset]]:
\[
  \label{DoubleCosetInProductOrbitDecomposition}
  R
  \coloneqq
  Z_G(c) 
    \backslash  
  G^2 
    / 
  \big( Z_G(g) \times Z_G(g') \big)
  \mathrlap{\,.}
\]
\end{lemma}
\begin{proof}
Consider the [[binary operation|group multiplication]] map
$
  {[g]} \times {[g']}
  \xrightarrow{ (-) \cdot (-) }
  G
$. Since this is $G$-[[equivariant map|equivariant]] for the ([[diagonal action|diagonal]]) [[adjoint action]], the [[set]] of $G$-[[orbits]] in $[g] \times [g']$ is partitioned into [[subsets]] labeled by [[conjugacy classes]] $[c] \in \mathrm{Conj}(G)$. An [[orbit]] in $[g] \times [g']$ is in the subset labeled by $[c]$ iff it contains an element $(g^k, g'^{k'})$ such that $g^k g'^{k'} = c$, for some $(k,k') \in G^2$. With the representative $c$ of $[c]$ held fixed, the latter pair has a unique class $[k,k'] \in G^2/\big({ Z_G(g) \times Z_G(g') }\big)$, and hence the set of orbits labeled by $[c]$ is in bijection to $R$ (eq:DoubleCosetInProductOrbitDecomposition). 

This shows that the disjoint union on the right of (eq:DecompositionProductOrbits) is indexed by the set of orbits of the groupoid on the left. Since the disjoint union is over the [[delooping groupoids]] of the [[isotropy groups]] of these orbits, the claim follows.
\end{proof}

It follows that:

\begin{proposition}
\label{FusionCoefficientInDrinfeldCenterOfGVectorSpaces}
The fusion product of a pair of simple objects $\big({([g_1],\rho_1), ([g_2],\rho_2)}\big)$ contains any simple object $\big({[g],\rho}\big)$ with the following multiplicity:
\[\label{TheFusionCoefficientsInDrinfeldCenterOfGVectorSpaces}
  N_{ ([g_1],\rho_1), ([g_2],\rho_2)}^{([g],\rho)}
  \;=\;
  \sum_{\mathclap{
    \substack{
      [k_1,k_2] \in R
      \\
      g_1^{k_1} g_2^{k_2} = g
    }
  }}
  \;
  \mathrm{dim}\,
  \mathrm{Hom}_{
    Z_G(g_1)^{k_1}
      \cap
    Z_G(g_2)^{k_2}
  }
  \big({
    \rho_1^{k_1}
    \otimes
    \rho_2^{k_2},
    \rho
  }\big)
  \mathrlap{\,.}
\]
\end{proposition}
\begin{proof}
  By Lem. \ref{FusionViaPullPush} we have that the fusion product is given by pull-push through
  $$
      \big([g]\sslash_{\!\mathrm{Ad}} G\big)
      \times
      \big([g']\sslash_{\!\mathrm{Ad}} G\big)
      \longleftarrow
      \big({
        [g]\times [g']
      }\big)\sslash_{\!\mathrm{Ad}} G
      \longrightarrow
      G \sslash_{\!\mathrm{Ad}} G
      \mathrlap{\,.}
  $$
  
By Lemma \ref{OnTheDecompositionOfProductOrbits}, this yields on the orbit $[g]$ the isotropy representation
\begin{equation}
  \bigoplus_{\mathclap{
    \substack{
      [k_1, k_2] \in R
      \\
      g_1^{k_1} g_2^{k_2} = g
    }
  }}
  \,
  \mathrm{Ind}
    _{Z_G(g_1^{k_1}, g_2^{k_2})}
    ^{Z_G(g)}
  \left({
    \mathrm{Res}
      ^{Z_G(g_1^{k_1}, g_2^{k_2})}
      _{Z_G(g)}
    \big({
      \rho_1^{k_1}
    }\big)
    \otimes
    \mathrm{Res}
      ^{Z_G(g_1^{k_1}, g_2^{k_2})}
      _{Z_G(g)}
    \big({
      \rho_2^{k_2}
    }\big)
  }\right)
  \mathrlap{\,,}
\end{equation}
where we are using that on group representations the left base change $m_!$ is given by forming [[induced representations]].

This yields the claim: By [[Schur's lemma]], the multiplicity of the irrep $\rho$ in this expression is the dimension of the hom-space from the latter to the former. Finally, by Frobenius reciprocity the induction is left adjoint to restriction, whence we have (eq:TheFusionCoefficientsInDrinfeldCenterOfGVectorSpaces).
\end{proof}

\linebreak


## Related concepts

* [[center of a category]], [[center of an additive category]]

* [[Drinfeld double]]



## References

Original articles:

* {#Mueger03} [[Michael Mueger]], *From Subfactors to Categories and Topology II. The quantum double of tensor categories and subfactors*, J. Pure Appl. Alg. 180, 159-219 (2003) ([arXiv:math/0111205](https://arxiv.org/abs/math/0111205))

* {#EtingofNikshychOstrik05} [[Pavel Etingof]], [[Dmitri Nikshych]], [[Victor Ostrik]], *On fusion categories*, Annals of Mathematics Second Series, Vol. 162, No. 2 (Sep., 2005), pp. 581-642 ([arXiv:math/0203060](http://arxiv.org/abs/math/0203060), [jstor:20159926](https://www.jstor.org/stable/20159926))

* {#DrinfeldGelakiNikshychOstrik10} [[Vladimir Drinfeld]], [[Shlomo Gelaki]], [[Dmitri Nikshych]], [[Victor Ostrik]], *On braided fusion categories I*, Selecta Mathematica. New Series 16 (2010), no. 1, 1–119 ([doi:10.1007/s00029-010-0017-z](https://doi.org/10.1007/s00029-010-0017-z))

Review:

* {#DavydovMuegerNikshychOstrik03} [[Alexei Davydov]], [[Michael Mueger]], [[Dmitri Nikshych]], [[Victor Ostrik]], Sec. 2.3 of: *The Witt group of non-degenerate braided fusion categories*, Journal fuer reine und angewandte Mathematik, **677** (2013. 135-177), de Gruyter 2003  ([arXiv:1009.2117](https://arxiv.org/abs/1009.2117), [doi:10.1515/crelle.2012.014](https://doi.org/10.1515/crelle.2012.014))


Textbook accounts:

* [[Shahn Majid]]: *Foundations of quantum group theory*, Cambridge University Press (1995, 2000) &lbrack;[doi:10.1017/CBO9780511613104](https://doi.org/10.1017/CBO9780511613104)&rbrack;

* [[Christian Kassel]]: _Quantum groups_, Graduate Texts in Mathematics __155__, Springer (1995) &lbrack;[doi:10.1007/978-1-4612-0783-2](https://link.springer.com/book/10.1007/978-1-4612-0783-2), [webpage](http://www-irma.u-strasbg.fr/~kassel/QGbk.html), [errata pdf](http://www-irma.u-strasbg.fr/~kassel/QGerrata030399.pdf)&rbrack;

* {#BakalovKirillov2001} [[Bojko Bakalov]], [[Alexandre Kirillov]]; section 3.2 in: *Lectures on tensor categories and modular functors*, University Lecture Series **21**, Amer. Math. Soc. (2001) &lbrack;[webpage](http://www.math.stonybrook.edu/~kirillov/tensor/tensor.html), [ams:ulect/21](https://bookstore.ams.org/view?ProductCode=ULECT/21), [[BakalovKirillov2000.pdf:file]]&rbrack;

* {#EGNO15} [[Pavel Etingof]], [[Shlomo Gelaki]], [[Dmitri Nikshych]], [[Victor Ostrik]]: *Tensor Categories*, Mathematical Surveys and Monographs **205**, AMS (2015) &lbrack;[ISBN:978-1-4704-3441-0](https://bookstore.ams.org/surv-205), [pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf)&rbrack;

A general discussion of centers of [[monoid objects]] in [[braided monoidal 2-categories]] (which reduces to the above for the 2-category [[Cat]] with its [[cartesian product]]) is in 

* [[Ross Street]], _The monoidal center as a limit_, [pdf](http://maths.mq.edu.au/~street/centre.pdf)

An application to character sheaves is in 

* [[George Lusztig]], _Non-unipotent character sheaves as a categorical centre_, [arxiv/1506.04598](http://arxiv.org/abs/1506.04598)

In relation to [[spectra of tensor triangulated categories]]:

* Kent B. Vashaw, _Balmer spectra and Drinfeld centers_ ([arXiv:2010.11287](https://arxiv.org/abs/2010.11287))

Relation to [[Frobenius monoidal functors]]:

* Johannes Flake, Robert Laugwitz, Sebastian Posur: *Frobenius monoidal functors from ambiadjunctions and their lifts to Drinfeld centers* &lbrack;[arXiv:2410.08702](https://arxiv.org/abs/2410.08702)&rbrack;



[[!redirects Drinfeld centers]]

[[!redirects Drinfel'd center]]
[[!redirects Drinfel'd centers]]
  
[[!redirects center of a monoidal category]]

