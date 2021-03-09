



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

Unifying these two cases, there is the bivariant Boardman homomorphism ([Adams 74, p. 58](#Adams74))

$$
  [X, Y]_\bullet 
    \;\simeq\; 
  [X, Y \wedge \mathbb{S}]_\bullet 
    \longrightarrow 
  [X,Y \wedge E]_\bullet
  \,.
$$

Since [[generalized homology]]/[[generalized cohomology]] is typically more tractable than [[homotopy groups]]/[[cohomotopy]] (in particular when [[homology spectra split]]), the Boardman homomorphism is often used to partially reduce computations of the latter in terms of computations of the former. 

One example is the computation of the homotopy groups of [[MU]] via the [[homology of MU]] ([[Quillen's theorem on MU]]), see [below](#ForComplexOrientedCohomologyTheories).

## Examples

### In ordinary cohomology

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

Similarly, if instead the manifold has dimension $d = 7$ but sticking to degree $n = 4$, then the estimate is that the cokernel is [[torsion subgroup|4-torsion]], 

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



+-- {: .num_prop #BoardmanIsoOn7SphereMod2I}
###### Proposition
**([[Boardman homomorphism|Boardman]] [[isomorphism]] on [[2-sphere]] mod [[binary icosahedral group]])

Consider the  [[binary icosahedral group]] $2 I$ and its [[action]] on the [[7-sphere]] induced via the identification $S^7 \simeq S(\mathbb{H} \times \mathbb{H})$ from the [[diagonal action|diagonal]] of the canonical action of $2I$ on the [[quaternions]] $\mathbb{H}$ induced via it being a [[finite subgroup of SU(2)]].  

On the [[quotient space]] $S^7/2 I$ the [[Boardman homomorphism]] in degree 4 is an [[isomorphism]]

$$
  \mathbb{S}^4\left(
     S^7/2I
  \right)
  \underoverset{\simeq}{\beta}{\longrightarrow}
  H^4\left( S^7/2I , \mathbb{Z} \right)
$$

from [[stable cohomotopy]] in degree 4 to [[integral cohomology]] in degree 4.

=--

+-- {: .proof}
###### Proof

In terms of the [[Atiyah-Hirzebruch spectral sequence]] for [[stable cohomotopy]] it is sufficient to see that the two differentials 

$$
  H^4\left(
    S^7/2I, \pi^0_s = \pi^s_0 =\mathbb{Z}
  \right)
  \overset{d_3}{\longrightarrow}
  H^6\left(
    S^7/2I, \pi^{-1}_s = \pi^s_{1} =\mathbb{Z}/2
  \right)
$$

and

$$
  H^4\left(
    S^7/2I, \pi^0_s = \pi^s_0 =\mathbb{Z}
  \right)
  \overset{d_3}{\longrightarrow}
  H^7\left(
    S^7/2I, \pi^{-2}_s = \pi^s_{2} =\mathbb{Z}/2
  \right)
$$

both vanish (all higher differentials on $H^4(-,\pi^0_s)$ vanish simply for dimensional reasons as $S^7$ is of [[dimension]] 7, while there are no differentials into $H^4(-,\pi^0_s)$ simply because the [[sphere spectrum]] is [[connective spectrum|connective]], so that the [[stable homotopy groups of spheres]] vanish in [[negative number|negative]] degree).

For $d_2$ to vanish, it is sufficient that 

$$
  H^6\left(
    S^7/2I, \pi^{-1}_s = \pi^s_{1} =\mathbb{Z}/2
  \right)
  \;\simeq\;
  0
$$

We now first show that this is the case:

First, by the [[Gysin sequence]] for the [[spherical fibration]]

$$
  \array{
    S^7 &\longrightarrow& S^7/SI
    \\
    && \downarrow
    \\
    && B (2 I)
  }
$$

we have

$$
  H^6\left(
    S^7/2I, \, \mathbb{Z}/2
  \right)
  \;\simeq\;
  H^6\left(
    B(2I),\, \mathbb{Z}/2
  \right)
  \,,
$$

where $B (2 I) \simeq \ast \sslash (2I)$ is the [[classifying space]] of $2I$ (see e.g. at [[infinity-action]]).

Moreover, by the [[universal coefficient theorem]] ([this Prop.](universal+coefficient+theorem#OrdinaryStatementInTopology)) we have a [[short exact sequence]]

$$
  0 
    \to 
  Ext^1(H_{5}\big(B(2I), \mathbb{Z}), \mathbb{Z}/2\big) 
    \longrightarrow 
  H^6\big(B(2I), \mathbb{Z}/2\big)
    \longrightarrow 
  Hom_{Ab}\big( H_6( B(2I), \mathbb{Z}) , \mathbb{Z}/2 \big) 
    \to 
  0
  \,.
$$

This means that it is sufficient to see that

$$
  H_{5}\big(B(2I), \mathbb{Z}) \simeq 0
  \phantom{AAA}
  H_{6}\big(B(2I), \mathbb{Z}) \simeq 0
$$

But for every [[finite subgroup of SU(2)]] $G_{ADE} \subset SU(2)$ we have (by [this Prop.](https://ncatlab.org/nlab/show/finite+rotation+group#GroupCohomologyOfFiniteSubgroupsOfSU2))

$$
  H_{5}\big(B(2I), \mathbb{Z}) \simeq G^{ab}_{ADE}
  \phantom{AAA}
  H_{6}\big(B(2I), \mathbb{Z}) \simeq 0
$$

where $G^{ab}_{ADE}$ is the [[abelianization]] of $G_{ADE}$. Specifically for $G_{ADE} = 2I$ this does vanish: the [[binary icosahedral group]] is a [[perfect group]] ([this Prop.](icosahedral+group#2IIsPerfect)).

This shows that $d_2$ vanishes on $H^4(-, \pi^0)$.

Now by a standard argument, the AHSS-differentials between ordinary cohomology groups are stable [[cohomology operations]], and thus, if non-trivial, must be the  [[Steenrod operations]] $Sq^n$ (e.g. [here](https://mathgroove.wordpress.com/2016/11/30/filling-the-details-5-two-words-about-the-atiyah-hirzebruch-spectral-sequence/), but let's add a more canonical reference).

This means first of all that if $d_2$ is not trivial then $d_2 = Sq^2$. But since that vanishes on $H^4(-,\pi^0)$ by the above argument, and on $H^7(-,\pi^2)$ for dimension reasons, so that the relevant entries pass as ordinary cohomology groups to the third page of the [[spectral sequence]], it follows similarly that  $d_3 = Sq^3$.

But by the [[Adem relation]] $Sq^3 = Sq^1 \circ Sq^2$, the vanishing of $Sq_2$ on $H^4(-,\pi^0)$ then also implies the vanishing of $d_3$ on this entry.

=--




### In complex oriented cohomology 
 {#ForComplexOrientedCohomologyTheories}

Used for [[complex oriented cohomology theories]] and proof of [[Quillen's theorem on MU]] via the [[homology of MU]] (...)

([Adams 74, pages 60-62](#Adams74), [Lurie 10, lecture 7](#Lurie10))


### In topological modular forms

See _[[Boardman homomorphism in tmf]]_








## Related concepts

* [[Hopf degree theorem]]


## References

According to [Hunton 95](#Hunton95), the concept was introduced, in print, in:

* [[John Michael Boardman]], _The eightfold way to BP-operations_, in: _Current trends in algebraic topology_, pp. 187–226, Canadian Mathematical Society Proceedings, 2, Part 1.  Providence 1982 ([ISBN:978-0-8218-6003-8](https://bookstore.ams.org/cmsams-2))

Further discussion:


* {#Adams74} [[John Frank Adams]], part II, section 6 of: _[[Stable homotopy and generalised homology]]_ (1974)


* {#Hunton95} John Hunton, _The Boardman homomorphism_, Contemporary Mathematics 181, 251-251, 1995 ([GoogleBooks](https://books.google.ae/books?hl=en&lr=&id=hcYaCAAAQBAJ&oi=fnd&pg=PA251&dq=John+Hunton,+The+Boardman+homomorphism&ots=_ZI5SEcU28&sig=cK1Xd7AZwZP7WeTiy4dGv5v9BJk&redir_esc=y#v=onepage&q=John%20Hunton%2C%20The%20Boardman%20homomorphism&f=false))


* {#Kochmann96} [[Stanley Kochmann]], section 4.3 of: _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Arlettaz04} [[Dominique Arlettaz]], _The generalized Boardman homomorphisms_, Central European Journal of Mathematics March 2004, Volume 2, Issue 1, pp 50-56 ([doi:10.2478/BF02475949](https://doi.org/10.2478/BF02475949))



* {#Lurie10} [[Jacob Lurie]], lecture 7 of _[[Chromatic Homotopy Theory]]_, 2010, ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture7.pdf))

* [[Akhil Mathew]], _Torsion exponents in stable homotopy and the Hurewicz homomorphism_, Algebr. Geom. Topol. 16 (2016) 1025-1041 ([arXiv:1501.07561](https://arxiv.org/abs/1501.07561))


* Hadi Zare, _On the image of the unstable Boardman map_ ([arXiv:1806.07079](https://arxiv.org/abs/1806.07079))



On the [[Boardman homomorphism]] (generalized [[Hurewicz homomorphism]]) to [[tmf]]:

* [[Mark Behrens]], [[Mark Mahowald]], J.D. Quigley, _The 2-primary Hurewicz image of $tmf$_ ([arXiv:2011.08956](https://arxiv.org/abs/2011.08956))


[[!redirects Boardman homomorphisms]]