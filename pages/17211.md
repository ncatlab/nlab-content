



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Given any [[homotopy commutative ring spectrum]] $(E, \mu, e)$, then the _Boardman homomorphism_ is the [[homomorphism]] from [[stable homotopy groups]] (hence from [[stable homotopy homology theory]]) to $E$-[[generalized homology]] groups that is induced by [[smash product]] with the unit map $e \colon \mathbb{S} \longrightarrow E$ from the [[sphere spectrum]]:

$$
  \pi_\bullet(-)
  \simeq
  \pi_\bullet(\mathbb{S} \wedge (-))
  \longrightarrow
  \pi_\bullet(E \wedge (-))
  =
  E_\bullet(-)
  \,.
$$


For $E = H \mathbb{Z}$ the [[Eilenberg-MacLane spectrum]] for [[ordinary homology]], then this reduces to the [[Hurewicz homomorphism]] $\pi_\bullet(-) \to H_\bullet(-)$.

Dually, there is the Boardman homomorphism from [[stable cohomotopy]] to [[generalized cohomology]] induced under forming [[mapping spectra]] into the unit map of $E$:

$$
  \pi^\bullet(-)
  \simeq
  \pi_\bullet([(-),\mathbb{S}])
   \longrightarrow
  \pi_\bullet([(-),E])
   =
  E^\bullet(-)
  \,.
$$ 

Unifying these two cases, there is the bivariant Boardman homomorphism


$$
  [X, Y]_\bullet \simeq [X, Y \wedge \mathbb{S}]_\bullet \longrightarrow [X,Y \wedge E]_\bullet
  \,.
$$

Since [[generalized homology]]/[[generalized cohomology]] is typically more tractable than [[homotopy groups]]/[[cohomotopy]] (in particular when [[homology spectra split]]), the Boardman homomorphism is often used to partially reduce computations of the latter in terms of computations of the former. 

One example is the computation of the homotopy grous of [[MU]] via the [[homology of MU]] ([[Quillen's theorem on MU]]), see [below](#ForComplexOrientedCohomologyTheories).

## Examples

### From stable cohomotopy to ordinary cohomology

Consider the [[unit]] morphism

$$
  \mathbb{S} \longrightarrow H \mathbb{Z}
$$

from the [[sphere spectrum]] to the [[Eilenberg-MacLane spectrum]] of the [[integers]]. For any [[topological space]]/[[spectrum]] postcomposition with this morphism induces [[Boardman homomorphisms]] of [[cohomology groups]] (in fact of [[commutative rings]])

\[
  \label{BoardmandCohomotopyToOrdinaryCohomology}
  b^n
  \;\colon\;
  \pi^n(X)
  \longrightarrow
  H^n(X, \mathbb{Z})
\]

from the [[stable cohomotopy]] of $X$ in degree $n$ to its [[ordinary cohomology]] in degree $n$.

+-- {: .num_prop #BoundsOnCoKernelOfBoardmandFromStableCohomotopyToOrdinaryCohomology}
###### Proposition
**(bounds on ([[cokernel|co-]])[[kernel]] of [[Boardman homomorphism]] from [[stable cohomotopy]] to [[integral cohomology]])**

If $X$ is a [[CW-spectrum]] which

1. is [[n-connected object of an (infinity,1)-topos|(m-1)-connected]]

1. of dimension $d \in \mathbb{N}$

then 

1. the [[kernel]] of the [[Boardman homomorphism]] $b^n$ (eq:BoardmandCohomotopyToOrdinaryCohomology) for   
   
   $$
     m \leq n\leq d -1
   $$

   is a $\overline{\rho}_{d-n}$-[[torsion subgroup|torsion group]]:

   $$
     \overline{\rho}_{d-n} ker(b^n) \;\simeq\; 0
   $$


1. the [[cokernel]] of the [[Boardman homomorphism]] $b^n$ (eq:BoardmandCohomotopyToOrdinaryCohomology) for 

   $$
     m \leq n  \leq d - 2
   $$

   is a $\overline{\rho}_{d-n-1}$-[[torsion subgroup|torsion group]]:

   \[
     \label{TorsionEstimateCokernel}
     \overline{\rho}_{d-n-1} coker(b^n) \;\simeq\; 0
   \]

where

$$
  \overline{\rho}_{i}
   \;\coloneqq\;
   \left\{
   \array{
     1 &\vert& i\leq 1
     \\
     \underoverset{j = 1}{i}{\prod}  
       exp\left( 
         \pi_j\left( \mathbb{S}\right)
       \right)
     &\vert&
     \text{otherwise}
   }
   \right.
$$

is the [[multiplication|product]] of the [[exponent of a group|exponents]] of the [[stable homotopy groups of spheres]] in [[positive number|positive]] degree $\leq i$.
  
=--

([Arlettaz 04, theorem 1.2](#Arlettaz04))

+-- {: .num_example #ExampleForEstimatesOfTorsionOfCokernelOfBeta}
###### Example
**(estimates for torsion of cokernel of Boardman homomorphism)**

Let $X$ be a [[manifold]] 

* of [[dimension]] $d = 6$

* [[simply connected topological space|simply connected]] with $\pi_2(X) \neq 0$

then Prop. \ref{BoundsOnCoKernelOfBoardmandFromStableCohomotopyToOrdinaryCohomology} asserts that the [[cokernel]] of the [[Boardman homomorphism]] 

$$
  \beta^4
  \;\colon\;
  \mathbb{S}^4(X)
  \longrightarrow
  H^4( X, \mathbb{Z} )
$$

in 

* degree $n = 4$

is [[torsion subgroup|2-torsion]]:

$$
  2 coker(\beta^4) \;=\; 0
  \,.
$$

This is because in this case (eq:TorsionEstimateCokernel) gives that the relevant torsion degree is

$$
  \begin{aligned}
    \overline{\rho}_{d-n-1}
    & =
    \overline{\rho}_{1}
    \\
    & = \exp( \pi_1(\mathbb{S}) )
    \\
    & = \exp( \mathbb{Z}/2 )     
    \\  
    & = 2
  \end{aligned}
  \,.
$$

Similarly, if instead the manifold has dimension $d = 7$ but sticking to degree $n = 4$, then the estimate is that the cokernel is [[torsion subgroup}4-torsion]], 

$$
  4 coker(\beta^4) \;=\; 0
  \,.
$$

since then

$$
  \begin{aligned}
    \overline{\rho}_{d-n-1}
    & =
    \overline{\rho}_{2}
    \\
    & = \exp( \pi_1(\mathbb{S}) ) \cdot \exp( \pi_2(\mathbb{S}) )
    \\
    & = \exp( \mathbb{Z}/2 ) \cdot \exp( \mathbb{Z}/2 ) 
    \\  
    & = 2 \cdot 2
    \\
    & = 4
  \end{aligned}
  \,.
$$

Next for $d = 8$ we

$$
  \begin{aligned}
    \overline{\rho}_{d-n-1}
    & =
    \overline{\rho}_{3}
    \\
    & = 
      \exp( \pi_1(\mathbb{S}) ) 
      \cdot \exp( \pi_2(\mathbb{S}) )
      \cdot \exp( \pi_3(\mathbb{S}) )
    \\
    & = \exp( \mathbb{Z}/2 ) 
      \cdot \exp( \mathbb{Z}/2 ) 
      \cdot \exp( \mathbb{Z}/{24} ) 
    \\  
    & = 2 \cdot 2 \cdot 6
    \\
    & = 24
  \end{aligned}
  \,.
$$



=--

### For complex oriented cohomology theories
 {#ForComplexOrientedCohomologyTheories}

Used for [[complex oriented cohomology theories]] and proof of [[Quillen's theorem on MU]] via the [[homology of MU]] (...)

([Adams 74, pages 60-62](#Adams74), [Lurie 10, lecture 7](#Lurie10))


## References

Named after [[Michael Boardman]].

* {#Adams74} [[John Frank Adams]], part II, section 6 of _[[Stable homotopy and generalised homology]]_ (1974)

* {#Kochmann96} [[Stanley Kochmann]], section 4.3 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Arlettaz04} Dominique Arlettaz, _The generalized Boardman homomorphisms_, Central European Journal of Mathematics March 2004, Volume 2, Issue 1, pp 50-56

* {#Lurie10} [[Jacob Lurie]], lecture 7 of _[[Chromatic Homotopy Theory]]_, 2010, ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture7.pdf))

* [[Akhil Mathew]], _Torsion exponents in stable homotopy and the Hurewicz homomorphism_, Algebr. Geom. Topol. 16 (2016) 1025-1041 ([arXiv:1501.07561](https://arxiv.org/abs/1501.07561))


[[!redirects Boardman homomorphisms]]