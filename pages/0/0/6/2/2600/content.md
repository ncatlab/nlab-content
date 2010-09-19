
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

> [[Urs Schreiber]]: this is not in the literature

#Contents#
* automatic table of contents goes here
{:toc}

## Idea


The **fivebrane 6-group** $Fivebrane(n)$ is a smooth version of the [[topological space]] that appears in the second step of the [[Whitehead tower]] of the [[orthogonal group]].

It is a lift of this through the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#GeometricRealization">geometric realization</a> functor $\Pi : $ [[?LieGrpd]] $\to$ [[∞Grpd]].

One step below the fivebrane 6-group in the Whitehead tower is the [[string Lie 2-group]].

For the time being see the discussions at

<a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#SmoothWhitehead">smooth Whitehead tower</a>

and the Motivation section at

[[infinity-Chern-Weil theory]]

for more background.

## Definition

In the [[(∞,1)-topos]] $\mathbf{H} = $ [[?LieGrpd]] we have a smooh refinement of the second fractional [[Pontryagin class]]

$$
  \frac{1}{6}
  \mathbf{p}_2
  :
  \mathbf{B} String(n) 
  \to 
  \mathbf{B}^7 \mathbb{R}/\mathbb{Z}
$$

defined on the [[delooping]] of the [[string Lie 2-group]].

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

Along the lines of the description at [[Lie integration]] and [[string 2-group]], in a canonical [[models for infinity-stack (infinity,1)-toposes|model]] for $\mathbf{H}$ the morphism $\frac{1}{6}\mathbf{p]_2$ is given by a morphism out of a [[resolution]] $\mathbf{B}Q$ of $\mathbf{B}String(n)$ that is built in degree $k \leq 7$ from smooth $k$-[[simplices]] in the [[Lie group]] $Spin(n)$. This morphism assigns to a 7-simplex $\phi : \Delta^7_{Diff} \to Spin(n)$  the integral 

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

[[!redirects Fivebrane 6-group]]