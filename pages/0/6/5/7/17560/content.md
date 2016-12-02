

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

What is called _$\kappa$-symmetry_ is a certain fermionic [[symmetry]] of [[Green-Schwarz action functionals]] for [[super p-branes]] whose effect is to [[gauge symmetry|gauge away]] half of the [[spinor|spinorial]] [[sigma-model]] [[field (physics)|fields]].

In a completely super-covariant formulation of the [[Green-Schwarz action functionals]], this $\kappa$-symmetry is simply the odd-graded part of the [[supermanifold|super]]-[[worldvolume]] [[super-diffeomorphism]] symmetry of the [[sigma-model]] ([Sorokin 99, section 4.3](#Sorokin99), [Howe-Sezgin 04, section 4.3](#HoweSezgin04)): If 

1. $X$ denotes a [[superspacetime]] locally modeled on [[super-Minkowski spacetime]] $\mathbb{R}^{d-1,1\vert \mathbf{N}}$

1. $\Sigma$ denotes a [[supermanifold|super]]-[[worldvolume]] of a [[super p-brane]] locally modeled on [[super-Minkowski spacetime]] $\mathbb{R}^{p,1\vert \mathbf{N}/2}$

1. so that a [[sigma-model]] [[field (physics)|field]] configuration for a [[super p-brane]] of shape $\Sigma$ to popagate in $X$ is a morphism of [[supermanifolds]] of the form

   $$
     \array{
        \Sigma && \text{super-worldvolume}
        \\
        \downarrow^{\mathrlap{\phi}} &&\text{sigma-model super-field}& 
        \\
        X && \text{super-spacetime}
     }
   $$

then:

1. the postcomposition [[action]] of [[spacetime]] [[super-isometries]] $X \stackrel{\simeq}{\longrightarrow} X$ is in even degree the action of [[spacetime]] [[isometries]] and in odd degree the action of **[[spacetime]] [[supersymmetry]]** on the sigma-model fields;

1. the precomposition action of [[worldvolume]] [[super-diffeomorphism]] $\Sigma \stackrel{\simeq}{\to} \Sigma$ is in even degree the action of bosonic worldvolume [[diffeomorphism]] and in odd degree the action of **$\kappa$-symmetry**:

$$
  \array{
      \Sigma  &\underoverset{\simeq}{\kappa\text{-symmetry}}{\longrightarrow}& \Sigma
      \\
      \downarrow^{\mathrlap{\phi}} && \downarrow^{\mathrlap{\phi'}}
      \\
      X &\underoverset{\simeq}{\text{spacetime supersymmetry}}{\longrightarrow}&
    X
  }
  \,.
$$

Notice here the assumption that the number of odd directions on the [[worldvolume]] is half that of the [[target spacetime]]. This is the default assumption for fundamental [[super p-branes]], and it directly reflects the statement that the corrresponding [[black brane]] solutions are $1/2$ [[supergravity]] [[BPS states]].

For example, consider the embedding 

$$
  \mathbb{R}^{2,1} \hookrightarrow \mathbb{R}^{10,1}
$$

of 2+1d [[Minkowski spacetime]], thought of as the [[worldvolume]] of a [[membrane]] into 11d Minkowski spacetime, linearly along the coordinate axis. Any such embedding breaks the [[isometry group]] of $\mathbb{R}^{10,1}$ from the [[Poincare group]] $Iso(10,1)$ to $Iso(2,1) \times O(8)$. Now consider instead [[super Minkowski spacetime]] $\mathbb{R}^{10,1\vert \mathbf{32}}$. We are to ask what subspace of the [[spin representation]] $\mathbf{32}$ preserves the embedding in that the spinor bilinear pairing $\overline{\psi}_1 \Gamma \psi$ lands in $Iso(2,1) \hookrightarrow Iso(10,1)$. This tunrs out to be the case precisely for a half-dimensional subspace, and hence we may lift the above to a super-embedding of the form


$$
  \mathbb{R}^{2,1\vert 8 \otimes \mathbf{2}} \hookrightarrow \mathbb{R}^{10,1\vert \mathbf{32}}
  \,.
$$

If one now thinks of this not as inclusions of global spacetimes, but of their super tangent spaces at the points where the membrane sits in spacetime, then this reflects the local structure of $\kappa$-symmetry. 




Historically $\kappa$-symmetry was originally observed and considered for [[Green-Schwarz sigma models]] whose [[worldvolume]] is regarded as an ordinary (bosonic) [[smooth manifold]]. Then $\kappa$-symmetry is a "hidden" symmetry, with no evident geometric interpretation. As such it was first observed for the [[super-particle]] ([Siegel 83](#Siegel83)) and then for the [[super 1-brane in 3d]] ([Siegel 84](#Siegel84)). 

Based on this the [[Green-Schwarz action functional]] for the [[superstring]] in 10d ([[heterotic string]], [[type II superstring]]) was found in ([Green-Schwarz 84](GreenSchwarz84)) by first observing that the plain [[Nambu-Goto action]] for a string on a [[supermanifold]] has twice as many fermionic [[shell|on-shell]] [[degrees of freedom]] as the [[NSR-string]] and then by adding a term to the action (the [[WZW-term]]) to correct this defect, by ensuring that the sum of the NG-action with the WZW term enjoys $\kappa$-symmetry.
By the same recipe later $\kappa$-symmetric Green-Schwarz-type [[sigma-model]] actions for all the other [[super p-branes]] were found.



## References

Originally, $\kappa$-symmetry was observed for the [[super-particle]] in

* {#Siegel83} Warren Siegel, _Hidden Local Supersymmetry In The Supersymmetric Particle Action_ Phys. Lett. B 128, 397 (1983)

and for the [[super 1-brane in 3d]] in

* {#Siegel84} Warren Siegel, _Light Cone Analysis Of Covariant Superstring_ , Nucl. Phys. B 236, 311 (1984).

Then it was used to define/construct the manifestly spacetime supersymmetric [[Green-Schwarz action functional]] for the [[superstring]] in 10d in

* {#GreenSchwarz84} [[Michael Green]], [[John Schwarz]], _Covariant description of superstrings_, Phys. Lett. B136 (1984), 367&#8211;370 ([web](http://adsabs.harvard.edu/abs/1984PhLB..136..367G))

The interpretation of $\kappa$-symmetry as the odd-graded part of the action of [[super-diffeomorphism]] on the [[super p-brane]] [[worldvolume]], regarded itself as a [[supermanifold]], is discussed in

* {#Sorokin99} [[Dmitri Sorokin]], _Superbranes and Superembeddings_, Phys.Rept.329:1-101,2000 ([arXiv:hep-th/9906142](http://arxiv.org/abs/hep-th/9906142))

* {#HoweSezgin04} [[Paul Howe]], [[Ergin Sezgin]], _The supermembrane revisited_, Class.Quant.Grav. 22 (2005) 2167-2200 ([arXiv:hep-th/0412245](http://arxiv.org/abs/hep-th/0412245))


[[!redirects kappa symmetry]]
