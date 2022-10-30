
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The definition of [[differential cohomology]], is a special case of the definition of [[twisted cohomology]] (see [[cohesive (infinity,1)-topos -- structures]] for more on this).
It is natural to iterate these constructions and consider twists by differential cohomology classes. Following ([SSSIII](#SSSIII)) one can speak of _twisted differential $\mathbf{c}$-structures_ .

These appear in various guises in the [[background gauge field]]s of  [[string theory]] application. Below we discuss the following
special cases and applications.

* Higher differential spin structures 

  * [[differential string structure]]

  * [[supergravity C-field]]

  * [[differential fivebrane structure]]

* [[differential T-duality]]

## Definition

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]], usually $\mathbf{H} = $ [[Smooth∞Grpd]] or [[SynthDiff∞Grpd]] or the like.

+-- {: .num_defn}
###### Definition

For $\mathbf{c} : \mathbf{B}G \to \mathbf{B}^n U(1)$ a [[characteristic class|characteristic map]]
in $\mathbf{H}$ and $\hat {\mathbf{c}} : \mathbf{B}G_{\mathrm{conn}}
  \to \mathbf{B}^n U(1)_{\mathrm{conn}}$ its differential refinement,
sending [[connections on ∞-bundles]] to [[circle n-bundles with connection]] (see [[∞-Chern-Weil homomorphism]]).

We write $\hat {\mathbf{c}}\mathrm{Struc}_{\mathrm{tw}}(X)$ for the 
  corresponding [[twisted cohomology]], 

$$
  \array{
    \hat {\mathbf{c}}Struc_{tw}(X) &\stackrel{tw}{\to}& 
    H^{n+1}_{diff}(X)
    \\
    {}^{\mathllap{\chi}}\downarrow && \downarrow
    \\
    \mathbf{H}(X, \mathbf{B}G_{conn})
     &
     \stackrel{\hat \mathbf{c}}{\to}
     &
    \mathbf{H}(X, \mathbf{B}^n U(1)_{conn})
  }
  \,.
$$  

=--

## References

The notion was conceived of in 

* H. Sati, U. Schreiber, J. Stasheff, _Twisted differential string- and fivebrane structures_
  {#SSSIII}

in terms of [[L-∞ algebra]]ic data. The full formalization in cohesive $\infty$-toposes is due to

* D. Fiorenza, U. Schreiber, J. Stasheff, _[[schreiber:Cech cocycles for differential characteristic classes]]_
 {#FSS}

A general account is in section 4.2 of 

* U. Schreiber, _[[schreiber:differential cohomology in a cohesive topos]]_

[[!redirects twisted differential c-structures]]

[[!redirects twisted differential structure]]
[[!redirects twisted differential structures]]