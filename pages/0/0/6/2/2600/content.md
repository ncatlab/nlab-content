
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
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


The **fivebrane 6-group** $Fivebrane(n)$ is a smooth version of the [[topological space]] that appears in the second step of the [[Whitehead tower]] of the [[orthogonal group]].

It is a lift of this through the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#GeometricRealization">geometric realization</a> functor $\Pi : $ [[∞LieGrpd]] $\to$ [[∞Grpd]].

One step below the fivebrane 6-group in the Whitehead tower is the [[string Lie 2-group]].

For the time being see the discussions at

<a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#SmoothWhitehead">smooth Whitehead tower</a>

and the Motivation section at

[[infinity-Chern-Weil theory]]

for more background.

## Definition

In the [[(∞,1)-topos]] $\mathbf{H} = $ [[∞LieGrpd]] we have a smooth refinement of the second fractional [[Pontryagin class]]

$$
  \frac{1}{6}
  \mathbf{p}_2
  :
  \mathbf{B} String(n) 
  \to 
  \mathbf{B}^7 \mathbb{R}/\mathbb{Z}
$$

defined on the [[delooping]] of the [[string Lie 2-group]]. Strictly speaking, we need $n\gt 6$, since for low $n$, $String(n)$ is not 6-connected. See [[orthogonal group#HomotopyGroups|orthogonal group]] for a table of the relevant homotopy groups.

The [[delooping]] $\mathbf{B}Fivebrane(n)$ of the **fivebrane 6-group** is the [[principal ∞-bundle]] classified by this in $\mathbf{H}$, that is the [[homotopy fiber]] 

$$
  \array{
    \mathbf{B} Fivebrane(n) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}String(n) &\stackrel{\frac{1}{6}\mathbf{p}_2}{\to}& \mathbf{B}^7 \mathbb{R}/\mathbb{Z}
  }
  \,.
$$


## Construction

Along the lines of the description at [[Lie integration]] and [[string 2-group]], in a canonical [[models for infinity-stack (infinity,1)-toposes|model]] for $\mathbf{H}$ the morphism $\frac{1}{6}\mathbf{p}_2$ is given by a morphism out of a [[resolution]] $\mathbf{B}Q$ of $\mathbf{B}String(n)$ that is built in degree $k \leq 7$ from smooth $k$-[[simplices]] in the [[Lie group]] $Spin(n)$. This morphism assigns to a 7-simplex $\phi : \Delta^7_{Diff} \to Spin(n)$  the integral 

$$
  \int_{\Delta^7_{Diff}} \phi^* \mu_7 \;\;\in
  \mathbb{R}/\mathbb{Z}
$$

of the degree 7 [[Lie algebra cohomology|Lie algebra cocycle]] $\mu_7$ of the [[special orthogonal Lie algebra]] $\mathfrak{so}(n)$ which is normalized such that its pullback to $String(n)$ (..explain...) is the deRham image of the generator in [[integral cohomology]] there.


More in detail, a resolution of $\mathbf{B}String(n)$ is given by the [[coskeleton]]

$$
  \mathbf{cosk}_7
  \left(
  \array{
    Q_7 \subset hom(\Delta^7_{Diff}, G) \times (U(1))^{8 \cdot 7 \cdot 6 \cdot 5 \cdot 4}
    \\
    \downarrow \downarrow 
    \downarrow\downarrow 
    \downarrow \downarrow    
    \downarrow \downarrow    
    \\
    \vdots
    \\
    \downarrow \downarrow \downarrow\downarrow \downarrow \downarrow    
    \\
    Q_4 \subset hom(\Delta^4_{Diff}, G) \times (U(1))^{20}
   \\    
    \downarrow \downarrow \downarrow\downarrow \downarrow
    \\     
    Q_3 \subset hom(\Delta^3_{Diff}, G) \times (U(1))^4
   \\    
    \downarrow \downarrow \downarrow\downarrow
    \\     
    hom(\Delta^2_{Diff}, G) \times U(1)
   \\    
    \downarrow \downarrow \downarrow
    \\     
    hom(\Delta^1_{Diff}, G)
    \\
    \downarrow \downarrow
    \\
    *
  }
  \right)
$$

where the subobjects are those consisting of 3-simplices in $G$ with 2-faces labeled in $U(1)$ such that the integral of $\mu_3$ over the 3-simplex in $\mathbb{R}/\mathbb{Z}$ is the signed product of these labels.

(...)

## Related concepts

[[!include image of J -- table]]

## References

The topological [[fivebrane group]] with its interpretation in [[dual heterotic string theory]] was discussed in 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _Fivebrane structures_ Reviews in mathematical physics, 10 (2009) 1197 (<a href="http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSII">web</a>)

and the smooth fivebrane 6-group was indicated. The latter is discussed in more detail in section 4.1 of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

* [[Jesse Wolfson]] says he has shown the existence of a presentation of the $Fivebrane$ [[smooth infinity-group|smooth 6-group]] by a locally Kan and degreewise finite-dimensional simplicial smooth manifold.

[[!redirects Fivebrane 6-group]]

[[!redirects fivebrane Lie 6-group]]
[[!redirects Fivebrane Lie 6-group]]

[[!redirects smooth fivebrane 6-group]]

