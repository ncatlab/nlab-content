
> [[Urs Schreiber]]: this is not in the literature

#Idea#

The smooth $Fivebrane(n)$ 6-group is to the [[string 2-group]] as the [[topological group|topological]] [[fivebrane group]] is to the [[topological group|topological]] [[string group]].

The motivation and background described at [[string 2-group]] applies to the fivebrane 6-group with [[string structure]] everywhere replaced by [[fivebrane structure]].

#Definition#

In a [[schreiber:smooth (∞,1)-topos|smooth (∞,1)-topos]] $\mathbf{H}$ with $\mathbf{B}String(n)$ denoting the [[delooping]] of the [[string 2-group]], there is canonically (up to equivalence) a morphism

$$
  \frac{1}{6}
  p_2
  \mathbf{B} String(n) 
  \to 
  \mathbf{B}^7 R/Z
$$

being a smooth incarnation of the second fractional [[Pontryagin class]]. The [[delooping]] $\mathbf{B}Fivebrane(n)$ of the fivebrane 6-group is the [[homotopy fiber]] 

$$
  \array{
    \mathbf{B} Fivebrane(n) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}String(n) &\stackrel{\frac{1}{6}p_2}{\to}& \mathbf{B}^7 R/Z
  }
$$

of $\frac{1}{2}p_2$ in $\mathbf{H}$.

Along the lines of the description at [[string 2-group]], in a canonical [[models for infinity-stack (infinity,1)-toposes|model]] for $\mathbf{H}$ the morphism $\frac{1}{6}p_2$ is given by a morphism out of a resolution $\mathbf{B}Q$ of $\mathbf{B}String(n)$ that is built in degree $k \leq 7$ from smooth $k$-simplices in the [[Lie group]] $Spin(n)$. This morphism assigns to a 7-simplex $\phi : \Delta^7_{Diff} \to Spin(n)$  the integral 

$$
  \int_{\Delta^7_{Diff}} \phi^* \mu_7 \;\;\in
  R/Z
$$

of the degree 7 [[Lie algebra cohomology|Lie algebra cocycle]] $\mu_7$ of $\mathfrak{so}(n)$ which is normalized such that its pullback to $String(n)$ (..explain...) is the deRham image of the generator in [[integral cohomology]] there.

...

