

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A _[[partial differential equation]]_ (PDE) is _Green hyperbolic_ ([Khavkine 14, def. 2.2](#Khavkine14)) if it behaves like a [[normally hyperbolic differential equation]] on a [[globally hyperbolic spacetime]] in that it has unique [[advanced and retarded Green functions]].

_Duhamel&#8217;s principle_ essentially establishes the equivalence between [[hyperbolic  differential equations]] with a well-posed [[Cauchy problem]] and Green hyperbolic systems. ([Khavkine 14, p. 12](#Khavkine14))

## Definition

Let $\Sigma$ be a [[time orientation|time-oriented]] [[Lorentzian manifold]] of [[dimension]] $p+1$, or more generally a [[conal manifold]] with [[conal causal structure]].
 
$$
  \array{
    E 
    \\
    \downarrow^{\mathrlap{fb}}
    \\
    \Sigma
  }
$$ 

be a [[smooth vector bundle]]. Write

$$
  \tilde E^\ast
     \;\coloneqq\; 
   E^\ast \otimes_\Sigma \wedge_\Sigma^{p+1} T^\ast \Sigma
$$

for the _[[density|densitized]] [[dual vector bundle]]_, hence the [[tensor product of vector bundles]] of the [[dual vector bundle]] with the [[differential n-form]]-bundle.

+-- {: .num_defn #CompactlySourceCausalSupport}
###### Definition
**(compactly sourced causal support)

Given a [[vector bundle]] $E \overset{}{\to} \Sigma$ over a manifold $\Sigma$ with [[conal causal structure|causal structure]]


Write $\Gamma_{\Sigma}(-)$ for [[space of sections|spaces of smooth sections]], and write

$$
  \array{
    \Gamma_{cp}(-) & \text{compact support}
    \\
    \Gamma_{\Sigma,\pm cp}(-) & \text{compactly sourced future/past support}
    \\
    \Gamma_{\Sigma,scp}(-) & \text{compactly source causal support}
  }
$$ 

for the [[linear subspaces]] on those smooth sections whose [[support]] is 
1) inside a [[compact subset]], 2) inside the [[closed future cone]]/[[closed past cone]], respectively of a [[compact subset]], 3) inside the [[closed causal cone]] of a [[compact subset]] (spacelike compact support).

=--

([B&#228;r 14, def. 3.2](#Baer14}), [Khavkine 14, def. 2.1](#Khavkine14))


+-- {: .num_defn #GreenHyperbolicDifferentialOperator}
###### Definition
**([[Green hyperbolic differential operator]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[smooth vector bundle]] over a [[smooth manifold]] $\Sigma$ with [[causal structure]].

A linear [[hyperbolic differential operator]].

$$
  P 
    \;\colon\;
  \Gamma_\Sigma(E)
    \longrightarrow
  \Gamma_{\Sigma}(\tilde E^\ast)
$$

is called _Green hyperbolic_ with respect to the given [[causal structure]] if for every 

$$  
  \tilde \alpha^\ast \in \Gamma_{\pm}(\tilde E^\ast)
$$

the inhomogeneous [[differential equation]]

$$
  P \Phi_{\pm} = \tilde \alpha^\ast
$$

has a unique solution  $\Phi_{\pm}$; and such that this unique solution has [[support]] inside the [[closed future cone]]/[[closed past cone]] of the support of $\tilde \alpha^\ast$, respectively.

=--

([B&#228;r 14, def. 3.1](#Baer14}), [Khavkine 14, def. 2.2](#Khavkine14))


+-- {: .num_defn #AdvancedAndRetardedGreenFuntions}
###### Definition
**([[advanced and retarded Green functions]] and [[causal Green function]])**

Given a Green-hyperbolic differential operator $P$ (def. \ref{GreenHyperbolicDifferentialOperator}) there are [[linear maps]]

$$
  \mathrm{G}_\pm
    \;\colon\;
  \Gamma_{\Sigma,\pm cp}(\tilde E^\ast)
    \longrightarrow
  \Gamma_{\Sigma, \pm cp}(E)
$$

between spaces of causally source future/past support (def. \ref{CompactlySourceCausalSupport})
such that the unique solution to $P \Phi_\pm = \tilde \alpha^\ast$ is given by 

$$
  \Phi_\pm = \mathrm{G}_\pm(\tilde \alpha^\ast)
  \,.
$$

These $\mathrm{G}_{\pm}$ are called the _[[advanced and retarded Green functions]]_ for $P$.

The difference

$$
  \mathrm{G} \coloneqq \mathrm{G}_+ - \mathrm{G}_-
$$

is called the _[[causal Green function]]_ for $P$.

=--

## Properties
 {#Properties}


### Formally adjoint Green hyperbolic operators

+-- {: .num_defn #FormallyAdjointDifferentialOperators}
###### Definition
**([[formally adjoint differential operators]])**

Two [[differential operators]]

$$
  P, P^\ast
   \;\colon\;
  \Gamma_\Sigma(E)
    \longrightarrow
  \Gamma_\Sigma(\tilde E^\ast)
$$

are called _[[formally adjoint differential operators]]_ via a [[bilinear map|bilinear]] [[differential operator]]

$$
  \label{FormallyAdjointDifferentialOperatorWitness}
  K \;\colon\;
  \Gamma_\Sigma(E) \otimes \Gamma_\Sigma(E)
    \longrightarrow
   \Gamma_\Sigma(\wedge^{p} T^\ast \Sigma)
$$

such that for all $\Phi_1, \Phi_2 \in \Gamma_\Sigma(E)$ we have

$$
  P(\Phi_1) \cdot \Phi_2
  -
  \Phi_1 \cdot P^\ast(\Phi_2)
   \;=\;
  d K(\Phi_1, \Phi_2)
$$

=--

([Khavkine 14, def. 2.4](#Khavkine14))

+-- {: .num_prop}
###### Proposition
**([[causal Green functions]] of [[formally adjoint differential operator|formally adjoint]] [[Green hyperbolic differential operators]] are [[formally adjoint differential operator|formally adjoint]])**

Let

$$
  P, P^\ast \;\colon\;\Gamma_\Sigma(E) \overset{}{\longrightarrow} \Gamma_\Sigma(\tilde E^\ast)
$$ 

be a pair of Green hyperbolic differential operators (def. \ref{GreenHyperbolicDifferentialOperator}) which are [[formally adjoint differential operator|formally adjoint]] (def. \ref{FormallyAdjointDifferentialOperators}).  Then also their [[causal Green functions]] $\mathrm{G}_P$ and $G_{P^\ast}$ (def. \ref{AdvancedAndRetardedGreenFuntions}) are [[formally adjoint differential operators]], up to a sign:

$$
  \left( 
    \mathrm{G}_P
  \right)^\ast
  \;=\;
  - \mathrm{G}_{P^\ast}
  \,.
$$

=--

([Khavkine 14, (24), (25)](#Khavkine14))


### Linear functionals on the solution space

+-- {: .num_prop #ExactSequenceOfGreenHyperbolicSystem}
###### Proposition
**([[exact sequence]] of Green hyperbolic system)**


Let $\Gamma_\Sigma(E) \overset{P}{\longrightarrow} \Gamma_\Sigma(\tilde E^\ast)$ be a Green hyperbolic differential operator (def. \ref{GreenHyperbolicDifferentialOperator}) with [[causal Green function]] $\mathrm{G}$ (def. \ref{GreenHyperbolicDifferentialOperator}). Then the sequence 

$$
  0 
    \to  
  \Gamma_{\Sigma,cp}(E)
   \overset{P}{\longrightarrow}
  \Gamma_{\Sigma,cp}(\tilde E^\ast)
    \overset{\mathrm{G}}{\longrightarrow}
  \Gamma_{\Sigma,scp}(E)
    \overset{P}{\longrightarrow}
  \Gamma_{\Sigma,scp}(\tilde E^\ast)
     \to
  0
$$

of these operators restricted to compact or spatially compact support as indicated (def. \ref{CompactlySourceCausalSupport})
is an [[exact sequence]] of continuous operators.

In particular this means that there is a [[linear isomorphism]] betwen the space $ker_{scp}(P)$ of spatially compact solutions to the differential equation and the [[quotient space]] of the [[compact support|compactly supported]] dual sections by the [[image]] of $P$:

$$
  \label{SolutionSpaceIsomorphicToQuotientByImP}
  \Gamma_{\Sigma,cp}(\tilde E^\ast)/im(P)
    \underoverset{\simeq}{\phantom{A}\mathrm{G}\phantom{A}}{\longrightarrow}
  ker_{scp}(P)
  \,.
$$

=--

The following proof is a slight refinement of ([Khavkine 14, prop. 2.1](#Khavkine14)).

+-- {: .proof}
###### Proof

Let $\Sigma_p^-, \Sigma_p^+ \subset \Sigma$ be two Cauchy surfaces, with $\Sigma_p^-$ in the past of $\Sigma_p^+$. Let also $\{\chi_+,\chi_-\}$ be a [[partition of unity]] subordinate to the cover $\{J^+(\Sigma_p^-), J^-(\Sigma_p^+)\}$ of $\Sigma$, that is, smooth functions such $\chi_+ + \chi_- = 1$, while $\chi_+ = 0$ on the past of $\Sigma_p^-$ and $\chi_- = 0$ on the future of $\Sigma_p^+$.

We can use these functions to define the following [[contracting homotopy]] of our complex into itself:
$$
  \begin{array}{ccccccccccc}
  0 &
    \to & 
  \Gamma_{\Sigma,cp}(E) &
   \overset{P}{\longrightarrow} &
  \Gamma_{\Sigma,cp}(\tilde E^\ast) &
    \overset{\mathrm{G}}{\longrightarrow} &
  \Gamma_{\Sigma,scp}(E) &
    \overset{P}{\longrightarrow} &
  \Gamma_{\Sigma,scp}(\tilde E^\ast) &
     \to &
  0
  \\
  & &
  {\downarrow} id & {\swarrow} {}_\chi\mathrm{G} &
  {\downarrow} id & {\swarrow} P_\chi &
  {\downarrow} id & {\swarrow} \mathrm{G}_\chi &
  {\downarrow} id
  \\
  0 &
    \to & 
  \Gamma_{\Sigma,cp}(E) &
   \overset{P}{\longrightarrow} &
  \Gamma_{\Sigma,cp}(\tilde E^\ast) &
    \overset{\mathrm{G}}{\longrightarrow} &
  \Gamma_{\Sigma,scp}(E) &
    \overset{P}{\longrightarrow} &
  \Gamma_{\Sigma,scp}(\tilde E^\ast) &
     \to &
  0
  \end{array}
$$
The homotopy maps are defined as follows:
$$
\begin{aligned}
  {}_\chi\mathrm{G}[\tilde{\alpha}^*]
  &= \chi_+ \mathrm{G}_-[\tilde{\alpha}^*]
    + \chi_- \mathrm{G}_+[\tilde{\alpha}^*] , \\
  P_\chi[\psi]
  &= P[\chi_+\psi] - \chi_+ P[\psi] = -P[\chi_-\psi] + \chi_- P[\psi] , \\
  \mathrm{G}_\chi[\tilde{\alpha}^*]
  &= \mathrm{G}_+[\chi_+\tilde{\alpha}^*] + \mathrm{G}_-[\chi_-\tilde{\alpha}^*] .
\end{aligned}
$$
The contracting identities
$$
\begin{aligned}
  {}_\chi\mathrm{G} \circ P &= id , \\
  P\circ {}_\chi\mathrm{G} + P_\chi \circ \mathrm{G} &= id , \\
  \mathrm{G}\circ P_\chi + \mathrm{G}_\chi \circ P &= id , \\
  P \circ \mathrm{G}_\chi &= id ,
\end{aligned}
$$
are simply a matter of direct calculation.

The identity morphism of our complex to itself induces an isomorphism on its cohomology. On the other hand, since this morphism itself is induced by a homotopy, it must be in fact be the zero map on cohomology. This is only possible when all cohomologies vanish and our complex is exact. (...remains to check continuity...)
=--

Equip all [[spaces of sections]] here with suitable [[topological vector space]] structure. As topological vector spaces, these spaces were considered in ([Sanders 13](#Sanders12)) and ([Baer 14](#Baer14)), where their topological duals were also determined. Keep in mind the following notation: $\Gamma'_{\Sigma}(\tilde{E}^*) := (\Gamma_{\Sigma,cp}(E))^*$ denotes the topological dual, which is interpreted as the space of _distributional sections_ of the bundle $\tilde{E}^*$. With this notations, smooth compactly supported sections of the same bundle are a dense subset $\Gamma_{\Sigma,cp}(\tilde{E}^*) \subset \Gamma'_{\Sigma}(\tilde{E}^*)$. Applying the same restrictions to the supports of distributions as of smooth functions, we have the following subspaces of distributional sections
$$
  \Gamma'_{\Sigma,cp}(\tilde E^\ast) ,
  \Gamma'_{\Sigma,scp}(\tilde E^\ast) ,  
  \Gamma'_{\Sigma,tcp}(\tilde E^\ast)
  \subset
  \Gamma'_{\Sigma}(\tilde E^\ast) .
$$



+-- {: .num_prop #DistributionsWithCausalSupports}
###### Proposition
**(topological duality with causally restricted supports)**
We have the following isomorphisms:
$$
\begin{aligned}
  \Gamma_{\Sigma,cp}(E)^* &\simeq \Gamma'_{\Sigma}(\tilde E^\ast) , \\
  \Gamma_{\Sigma,scp}(E)^* &\simeq \Gamma'_{\Sigma,tcp}(\tilde E^\ast) , \\
  \Gamma_{\Sigma,tcp}(E)^* &\simeq \Gamma'_{\Sigma,scp}(\tilde E^\ast) , \\
  \Gamma_{\Sigma}(E)^* &\simeq \Gamma'_{\Sigma,cp}(\tilde E^\ast) .
\end{aligned}
$$
=--
([Sanders 13, thm. 4.3](#Sanders12), [Baer 14, lem. 2.14](#Baer14))

Next, by dualizing the exact sequence from prop. \ref{ExactSequenceOfGreenHyperbolicSystem}, we have
+-- {: .num_prop #DualExactSequenceOfGreenHyperbolicSystem}
###### Proposition
**(distributional [[exact sequence]] of Green hyperbolic system)**

The following is an exact sequence of continuous maps:
$$
  0 
    \to  
  \Gamma'_{\Sigma,tcp}(E)
   \overset{P^*}{\longrightarrow}
  \Gamma'_{\Sigma,tcp}(\tilde E^\ast)
    \overset{\mathrm{-G}_{P^*}}{\longrightarrow}
  \Gamma'_{\Sigma}(E)
    \overset{P^*}{\longrightarrow}
  \Gamma'_{\Sigma}(\tilde E^\ast)
     \to
  0
$$
=--
Differential operators extend continuously to distributions in a standard way. The only nontrivial check is on the Green functions. Their continuity is discussed in ([Sanders 13, sec. 5](#Sanders12)) and ([Baer 14, lem. 4.1](#Baer14)). The exactness follows from the same argument as in the proof of prop. \ref{ExactSequenceOfGreenHyperbolicSystem} (a contracting homotopy dualizes to a contracting homotopy). The exactness of a sequence similar to the one above also appears as ([Baer 14, thm. 4.3](#Baer14)). 

Putting the above results together, it follows:

+-- {: .num_cor #DistributionsOnSolutionSpaceAreTheGeneralizedPDESolutions}
###### Corollary
**([[distributions]] on solution space are the [[generalized PDE solutions]])**

Let $P, P^\ast \;\colon\; \Gamma_\Sigma(E) \overset{}{\longrightarrow} \Gamma_\Sigma(\tilde E^\ast)$ be a pair of  Green hyperbolic differential operators (def. \ref{GreenHyperbolicDifferentialOperator}) which are [[formally adjoint differential operator|formally adjoint]] (def. \ref{FormallyAdjointDifferentialOperators}).

A [[continuous linear functional]] on the solution space

$$
  u_{sol} \in \left(ker_{scp}(P)\right)^\ast
$$

is equivalently a [[distribution]]

$$
  u \in \Gamma'_{\Sigma}(E)
$$

which is a [[generalized solution]] to the differential equation

$$
  P^\ast u = 0
  \,,
$$

and this [[linear isomorphism]] is given by pullback along the [[causal Green function]] $\mathrm{G}$ (def. \ref{AdvancedAndRetardedGreenFuntions}):

$$
  \left(ker_{scp}(P)\right)^\ast
     \underoverset{\simeq}{(-)\circ \mathrm{G}}{\longrightarrow}
   \left\{
     u \in \Gamma'_{\Sigma}(E)
     \,\vert\,
     P^* u = 0
   \right\}
  \,.
$$

=--


+-- {: .proof}
###### Proof

Keeping in mind that both $\ker_{scp}(P) \subset \Gamma_{\Sigma,scp}(E)$ and $im_{tcp}(P^*) \subset \Gamma'_{\Sigma,tcp}(\tilde{E}^*)$ are [[closed subspaces]] (the first by continuity of $P$ and the second by exactness of the sequence in prop. \ref{DualExactSequenceOfGreenHyperbolicSystem}), on the level of [[locally convex vector spaces]] ([Treves 67, props. 35.5, 35.6](#Treves67)), there is a linear bijection
$$
  (\ker_{scp}(P))^* \simeq \Gamma'_{\Sigma,tcp}(\tilde{E}^*) / im_{tcp}(P^*) ,
$$
which is also a topological isomorphism in the weak topology. Then, once again exploiting the exactness of the sequence in prop. \ref{DualExactSequenceOfGreenHyperbolicSystem}, we also have the chain of isomorphisms
$$
  \Gamma'_{\Sigma,tcp}(\tilde{E}^*) / im_{tcp}(P^*)
  \simeq \Gamma'_{\Sigma,tcp}(\tilde{E}^*) / \ker_{tcp}(G_{P^*})
  \simeq \ker(P^*) \subset \Gamma'_{\Sigma}(\tilde{E}) .
$$

=--



### The $P$-Poisson and $P$-Peierls brackets
 {#PPoissonAndPPeierlsBracket}


+-- {: .num_defn #BracketPPoissonAndPPeierls}
###### Definition
**($P$-Poisson and $P$-Peierls bracket)**

Let

$$
  P, P^\ast \;\colon\;\Gamma_\Sigma(E) \overset{}{\longrightarrow} \Gamma_\Sigma(\tilde E^\ast)
$$ 

be a pair of [[Green hyperbolic differential operators]] (def. \ref{GreenHyperbolicDifferentialOperator}) which are [[formally adjoint differential operator|formally adjoint]] (def. \ref{FormallyAdjointDifferentialOperators}) via a differential operator $K$ (eq:FormallyAdjointDifferentialOperatorWitness).

Then:

1. For any [[Cauchy surface]] $\Sigma_p \overset{\iota_{\Sigma_p}}{\hookrightarrow} \Sigma$ the _$P$-Poisson bracket_ is the [[bilinear map]]

   $$
     \array{
       \Gamma_{\Sigma,scp}(E) \otimes \Gamma_{\Sigma,scp}(E)
         &\overset{ \left\{-,- \right\}_{\Sigma_p,K} }{\longrightarrow}&
       \mathbb{R}
       \\
       (\mathbf{\Phi}_1, \mathbf{\Phi}_2)
       &\mapsto&
       \underset{\Sigma_p}{\int} (\iota_{\Sigma_p})^\ast K(\mathbf{\Phi}_1, \mathbf{\Phi}_2)
     }
   $$

1. The _$P$-Peierls bracket_ is the [[bilinear map]]
   
   $$
     \array{
       \Gamma_{\Sigma,cp}(\tilde E^\ast) \otimes \Gamma_{\Sigma,cp}(\tilde E^\ast)
         &
           \overset{
              \left\{ -,- \right\}_{\Sigma, \mathrm{G}}   
           }{
             \longrightarrow
           }
         &  
       \mathbb{R}
       \\
       (\tilde \alpha^\ast_1, \tilde \alpha^\ast_2)
         &\mapsto&  
       \underset{\Sigma}{\int} \tilde \alpha^\ast_1 \cdot \mathrm{G}_P(\tilde \alpha^\ast_2)
     }
   $$

=--


+-- {: .num_prop #PoissonToPPeierls}
###### Proposition
**([[causal Green function]] transforms $P$-Poisson bracket to $P$-Peierls bracket)**

Let

$$
  P, P^\ast \;\colon\;\Gamma_\Sigma(E) \overset{}{\longrightarrow} \Gamma_\Sigma(\tilde E^\ast)
$$ 

be a pair of [[Green hyperbolic differential operators]] (def. \ref{GreenHyperbolicDifferentialOperator}) which are [[formally adjoint differential operator|formally adjoint]] (def. \ref{FormallyAdjointDifferentialOperators}) via a differential operator $K$ (eq:FormallyAdjointDifferentialOperatorWitness).



Then the [[causal Green function]] intertwines the $P$-Poisson bracket with the $P$-Peierls bracket (def. \ref{BracketPPoissonAndPPeierls}) in that for every [[Cauchy surface]] $\Sigma_p \hookrightarrow \Sigma$ and all 

$$
  \tilde \alpha_1^\ast, \tilde \alpha_2
  \;\in\;
  \Gamma_{\Sigma,scp}(\tilde E^\ast)
$$

we have

$$
  \left\{
     \tilde \alpha^\ast_1, \tilde \alpha^\ast_2
  \right\}_{\Sigma,\mathrm{G}}
  \;=\;
  \left\{
     \mathrm{G}(\tilde \alpha^\ast_1),
     \mathrm{G}(\tilde \alpha^\ast_2)
  \right\}_{\Sigma_p,K}
  \,.
$$


=--

([Khavkine 14, lemma 2.5](#Khavkine14))

## Examples


+-- {: .num_example}
###### Example
**([[Klein-Gordon operator]])**

For $\Sigma$ a [[globally hyperbolic spacetimes]] then the [[Klein-Gordon operator]] $P = \Box - m^2$ (i.e. the [[wave operator]] for $m = 0$) is [[Green hyperbolic differential operator|Green hyperbolic]] according to  def. \ref{GreenHyperbolicDifferentialOperator} (e. g. [B&#228;r-Ginoux-Pfaeffle 07](#Klein-Gordon+equation#BaerGinouxPfaeffle07)) and formally self-adjoint ([this example](formal+adjoint+differential+operator#FormallySelfAdjointKleinGordonOperator)). The corresponding $P$-Peierls bracket (def. \ref{BracketPPoissonAndPPeierls}) is the original [[Peierls bracket]].

=--

## References

* {#Treves67} [[François Treves]], _Topological Vector Spaces, Distributions and Kernels_ (Academic Press, New York, 1967)

* {#Sanders12} [[Ko Sanders]], _A note on spacelike and timelike compactness_, Classical and Quantum Gravity 30, 115014 (2012) ([doi](http://dx.doi.org/10.1088/0264-9381/30/11/115014), [arXiv:1211.2469](https://arxiv.org/abs/1211.2469))

* {#Baer14} [[Christian Bär]], _Green-hyperbolic operators on globally hyperbolic spacetimes_, Communications in Mathematical Physics 333, 1585-1615 (2014)
([doi](http://dx.doi.org/10.1007/s00220-014-2097-7), [arXiv:1310.0738](https://arxiv.org/abs/1310.0738))

* {#Khavkine14} [[Igor Khavkine]], _Covariant phase space, constraints, gauge and the Peierls formula_, Int. J. Mod. Phys. A, 29, 1430009 (2014) ([arXiv:1402.1282](https://arxiv.org/abs/1402.1282))

[[!redirects Green hyperbolic partial differential equations]]

[[!redirects Green hyperbolic differential equation]]
[[!redirects Green hyperbolic partial differential equation]]

[[!redirects Duhamel's principle]]
[[!redirects Duhamel principle]]

[[!redirects Green hyperbolic PDE]]
[[!redirects Green hyperbolic PDEs]]

[[!redirects Green hyperbolic differential operator]]
[[!redirects Green hyperbolic differential operators]]


