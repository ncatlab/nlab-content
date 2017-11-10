

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

Let 

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

Write $\Gamma_{\Sigma}(-)$ for [[space of sections|spaces of smooth sections]], and write

$$
  \Gamma_{\Sigma,scp}(-)
  ,
  \Gamma_\pm(-)
$$ 

for the [[linear subspaces]] in those smooth sections whose [[support]] is inside the [[closed causal cone]] or [[closed future cone]]/[[closed past cone]], respectively, of a [[compact subset]] of $\Sigma$.

([Khavkine 14, def. 2.1](#Khavkine14))


+-- {: .num_defn #GreenHyperbolicDifferentialOperator}
###### Definition
**(Green hyperbolic differential operator)**

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

([Khavkine 14, def. 2.2](#Khavkine14))


+-- {: .num_defn #AdvancedAndRetardedGreenFuntioons}
###### Definition
**([[advanced and retarded Green functions]] and [[causal Green function]])**

Given a Green-hyperbolic differential operator $P$ (def. \ref{GreenHyperbolicDifferentialOperator}) there are [[linear maps]]

$$
  \mathrm{G}_\pm
    \;\colon\;
  \Gamma_\pm(\tilde E^\ast)
    \longrightarrow
  \Gamma_\pm(E)
$$

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


+-- {: .num_prop}
###### Proposition


Let $\Gamma_\Sigma(E) \overset{P}{\longrightarrow} \Gamma_\Sigma(\tilde E^\ast)$ be a Green hyperbolic differential operator (def. \ref{GreenHyperbolicDifferentialOperator}) with [[causal Green function]] $\mathrm{G}$ (def. \ref{GreenHyperbolicDifferentialOperator}). Then the sequence 

$$
  0 
    \to  
  \Gamma_{\Sigma,cp}(E)
   \overset{P}{\longrightarrow}
  \Gamma_{cp}(\tilde E^\ast)
    \overset{G}{\longrightarrow}
  \Gamma_{scp}(E)
    \overset{P}{\longrightarrow}
  \Gamma_{scp}(\tilde E^\ast)
     \to
  0
$$

is an [[exact sequence]].

In particular this means that there is a [[linear isomorphism]] betwen the space $ker_{scp}(P)$ of spatially compact solutions to the differential equation and the [[quotient space]] of the [[compact support|compactly supported]] dual sections by the [[image]] of $P$:

$$
  \Gamma_{\Sigma,cp}(\tilde E^\ast)/im(P)
    \underoverset{\simeq}{\phantom{A}\mathrm{G}\phantom{A}}{\longrightarrow}
  ker_{scp}(P)
  \,.
$$

=--

([Khavkine 14, prop. 2.1](#Khavkine14))


## References

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


