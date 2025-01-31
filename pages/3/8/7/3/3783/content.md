
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea ##

The **Kerr spacetime** is the unique stationary axially symmetric [[asymptotically flat]] vacuum (family of) solution(s) to the [[Einstein field equations]]. Informally, it describes an eternal, rotating [[black hole]] inside an otherwise empty universe. It is thought to closely approximate the gravitational field outside of compact rotating objects, to the point that astrophysical black holes are often described as "Kerr".

These black holes are characterized by their [[mass]] and their [[angular momentum]].


## Abstract ##
The definition states the components of the metric tensor in a specific coordinate system, the Boyer-Lindquist coordinates, and compares those to the Minkowski and Schwartzschild metrics. Some properties can be read off directly from the metric tensor, which is done in the properties paragraph.

## Boyer-Lindquist Description ##

Spacetimes in the Kerr family are distinguished by two (real) parameters, $m$ and $a$, respectively interpreted as the hole's [[mass]] and [[angular momentum]] per unit mass. Indeed as $a \to 0$ the geometry approaches that of a mass $m$ "nonrotating" [[Schwartzchild spacetime]].

As in the Schwartzchild spacetime, the observations of distant observers can be described using spherical coordinates $r, \phi, \theta$ on the "space" $\mathbb{R}^3$ and a time coordinate $t \in \mathbb{R}$. These coordinates are called **Boyer-Lindquist coordinates** in the context of the Kerr geometry. They limit to Schwartzchild coordinates with $a \to 0$.

We define two functions mainly as an abbreviation:
$$
\rho^2 = r^2 + a^2 \cos^2(\theta )
$$ 

$$
\triangle = r^2 - 2 m r + a^2
$$ 

The following table lists the components of the metric of Minkowski, Schwartzschild and Kerr spacetimes respectivly using the canonical coordinates and the Boyer-Lindquist coordinates for the Kerr spacetime:

| metric | Minkowski | Schwartzschild | Kerr |
|--------|-----------|----------------|------|
| $g_{tt}$ | -1 | $-1 + 2 \frac{m}{r}$ | $-1 + 2 \frac{mr}{\rho^2}$ |
| $g_{rr}$ | +1 | $\frac{r}{r - 2m}$ | $\frac{\rho^2}{\triangle}$ |
| $g_{\theta\theta}$ | $r^2$ | $r^2$ | $\rho^2$ |
| $g_{\phi\phi}$ | $r^2 \sin^2(\theta)$ | $r^2 \sin^2(\theta)$ | $(r^2 + a^2 + \frac{2 m r a^2 \sin^2(\theta)}{\rho^2}) \sin^2{\theta}$ |
| $g_{ij}$ $i \neq j$ | all zero | all zero | all zero except $g_{t \phi} = g_{\phi t} = - \frac{2 m r a \sin^2(\theta)}{\rho^2}$ |


One gets the [[Kerr-Newman metric]] for an electrically charged source with charge $e$ by replacing the definition of $\triangle$ with 

$$
\triangle = r^2 - 2 m r + a^2 + e^2
$$ 

The family of Kerr spacetimes is classified by the relation of the parameters $a$ and $m$:

* $0 = a$ gives Schwartzschild spacetime

* $0 \lt a^2 \lt m^2$ gives slowly rotating Kerr spacetime (**slow Kerr**)

* $a^2 = m^2$ gives **extreme Kerr spacetime** and

* $m^2 \lt a^2$ gives rapidly rotating Kerr spacetime (**fast Kerr**) 
 
## Properties ##
### Direct Consequences from the Definition ###
There are several coordinate singularities, inlcuding the z-axis (where $\sin(\theta) = 0$) and where $\rho = 0$ and $\triangle = 0$. Points where $\triangle = 0$ define the horizons of Kerr spacetime.

Both $\partial_t$ and $\partial_{\phi}$ are [[Killing vector field]]s, expressing the time invariance and the axial symmetry of the model respectively. Combining the sign changes $t \to -t, \phi \to -\phi$ gives an isometry: Letting time running backwards reverses the rotation.

Kerr spacetime is **asymptotically flat**, that is the Kerr metric approximates the Minkowski metric for large $r$.

### Boyer-Lindquist Blocks ###
The Boyer-Lindquist coordinates are defined on a subset of $\mathbb{R}^2 \times \mathcal{S}^2$ with $t, r$ defined on a copy of $\mathbb{R}$ respectively (actually $r$ is not supposed to take negative values, this definition is for convenience only). There are three subsets where the coordinates fail:

1. The **horizon H** where $\triangle = 0$.

2. The **ring singularity $\Sigma$** where $\rho^2 = 0$

3. The **axis A** where $\sin(\theta) = 0$.



+-- {: .un_def}
###### Definition
The **Boyer-Lindquist blocks I, II, III** are the following open subsets of $\mathbb{R}^2 \times \mathcal{S}^2 - \Sigma$:

1. For slow Kerr, there are two horizons at $r_{\pm}$,
$$
I: r \gt r_+ 
$$

$$
II: r_- \lt r \lt r_+ 
$$

$$
III: r \lt r_- 
$$

2. For extreme Kerr, there is a single horizon at $r = m$,
$$
I: r \gt m
$$

$$
III: r \lt m
$$
3. For fast Kerr, there is no horizon and $\mathbb{R}^2 \times \mathcal{S}^2 - \Sigma$ can be considered as one block I = III.
=--

Block I is also called the **Kerr exterior** and can be visualized as close to the Newtonian concept of space and time with a central force field.

+-- {: .un_theorem}
###### Theorem
**Causality of I and II**
The Boyer-Lindquist blocks I and II are causal.
=--

For a definition of causality see [[spacetime]].

+-- {: .un_theorem}
###### Theorem
**Noncausality of III**
The Boyer-Lindquist block III is vicious, that is for any two events $p, q$ in III there is a timelike future-pointing curve in III from p to q.
=--

### Extremal spinning black holes

The maximum [[angular momentum]] $J$ of a black hole with [[mass]] $M$ is $J = M^2$.

([[naked singularity]])

One considers the quotient $q \coloneqq J/M^2$. Spinning black holes exist for $q \lt 1$.

### Formation

> the following uses material taken from [this PhysicsSE comment](http://physics.stackexchange.com/a/91284/5603)

High angular momentum presents a barrier preventing collapse to a black hole (at least until this angular momentum is radiated away). 

The parameter on which the formation of black hole depends is the ratio $q$ of angular momentum ($J$) to the square of mass ($M$). If $q=J/M^2 \lt 1$ (in relativistic units with $G=1$, $c=1$), then the black hole (non-extremal Kerr black hole, to be precise) can be formed. If $q\gt 1$ then the black hole cannot be formed from all the matter without some mechanism for losing angular momentum (this means of course that some of the mass also has to be lost in the process).

For example, currently for the Sun this parameter is slightly more than 1. (*Of course solar mass is too small to ever form a black hole, angular momentum or not*).

If we are talking stellar collapse (see for instance [HFWLH 02](#HFWLH02)), during the late time evolution of the star it loses considerable portion of its outer shell. Since the outer layers carry most of angular momentum, it is quite possible than as the result of this process the rotation of the actual collapsing object would be slow enough to form the black hole outright.

Alternatively, if the rotation speed of the collapsing star is high enough, during the collapse the part of an angular momentum is retained in the [accretion disk](http://en.wikipedia.org/wiki/Accretion_disk) which is formed around the newly created black hole. The matter from such disk could then fall inside, potentially increasing the ratio $q$, but still it will never reach the limiting value of 1.

Note, that accretion disk (depending on the actual configuration) also can produce the opposite effect [Blandford&#8211;Znajek process](http://en.wikipedia.org/wiki/Blandford%E2%80%93Znajek_process) can slow the rotation of a black hole by extracting rotational energy.

Another possibility is that if the rotation is fast enough the black hole is never formed: for instance numerical simulations in ([DSY 04](#DSY04)) found that for $q\gt 1$ the collapsing neutron star forms a torus which then fragments into nonaxisymmetric clumps (without ever producing horizon).



### Higher symmetries

The Kerr spactime admits an extra [[Killing tensor]] and [[Killing-Yano tensor]] (...) See for instance ([JL](#JL)).


## Related concepts

[[!include charged and rotating black holes -- table]]

## References 

### General

The original article:

* [[Roy Kerr]], _Gravitational Field of a Spinning Mass as an Example of Algebraically Special Metrics_, Phys. Rev. Lett. 11, 237 (1963) ([doi:10.1103/PhysRevLett.11.237](https://doi.org/10.1103/PhysRevLett.11.237))

Global structure:

* Brandon Carter, *Global Structure of the Kerr Family of Gravitational Fields*, Phys. Rev. **174** (1968) 1559 &lbrack;[doi:10.1103/PhysRev.174.1559](https://doi.org/10.1103/PhysRev.174.1559)&rbrack;


and sources (cf. at *[[black brane]]*):

* Werner Israel, *Source of the Kerr Metric*, Phys. Rev. D **2** 641 (1970) &lbrack;[doi:10.1103/PhysRevD.2.641](https://doi.org/10.1103/PhysRevD.2.641)&rbrack;


Most textbooks on [[general relativity]] have chapter about the Kerr spacetime. 

Monograph:

* [[Barrett O'Neill]], *The geometry of Kerr black holes*, Dover (2014) &lbrack;[ISBN:9780486493428](https://store.doverpublications.com/products/9780486493428), [zmath:0828.53078](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0828.53078&format=complete)&rbrack;

Further survey:

* Project F, _The spinning black hole_ ([pdf](http://www.eftaylor.com/pub/SpinNEW.pdf))

See also:

* Wikipedia, _[Kerr spacetime](http://en.wikipedia.org/wiki/Kerr_spacetime)_


The [[Killing-Yano tensors]] of the Kerr spacetime are discussed in

* {#JL} Jacek Jezierski, Maciej &#321;ukasik, _Conformal Yano-Killing tensor for the Kerr metric and conserved quantities_ ([arXiv:gr-qc/0510058](http://arxiv.org/abs/gr-qc/0510058))
 


Formation of spinning black holes is discussed in 

* {#HFWLH02} Heger, A., Fryer, C. L., Woosley, S. E., Langer, N., & Hartmann, D. H. (2003). *How massive single stars end their life*. The Astrophysical Journal, 591(1), 288. [arXiv:astro-ph/0212469](http://arxiv.org/abs/astro-ph/0212469).
 

* {#DSY04} Duez, M. D., Shapiro, S. L., & Yo, H. J. (2004). *Relativistic hydrodynamic evolutions with black hole excision*. Physical Review D, 69(10), 104016. [arXiv:gr-qc/040107](http://arxiv.org/abs/gr-qc/0401076).
 

Kerr-type solutions in dimension $\gt 4$ were first given in 

* R. C. Myers and M. J. Perry, Annals Phys. 172, 304 (1986).

In higher dimensions the uniqueness theorem of 4d breaks down, and there are solutions with non-spherical topology, such as [[black rings]]. This plays a role notably in the discussion of [[black holes in string theory]].

On Kerr black holes in the context of the [[holographic principle]] and the [[AdS-CFT correspondence]]:

* [[Monica Guica]], [[Thomas Hartman]], Wei Song, [[Andrew Strominger]], _The Kerr/CFT Correspondence_, Phys. Rev. D **80** (2009) 124008 &lbrack;[arXiv:0809.4266](http://arxiv.org/abs/0809.4266), [doi:10.1103/PhysRevD.80.124008](https://doi.org/10.1103/PhysRevD.80.124008)&rbrack;


### Phenomenology
 {#ReferencesObservation}

Observational signature:

* Minyong Guo, Niels A. Obers, Haopeng Yan, _Observational signature of near-extremal Kerr-like black holes in a modified gravity theory at the Event Horizon Telescope_, Phys. Rev. D 98, 084063 (2018) ([arXiv:1806.05249](https://arxiv.org/abs/1806.05249))


Near-extremal spinning black holes are being observed:

* Xinyu Dai, Shaun Steele, Eduardo Guerras, Christopher W. Morgan, Bin Chen, _Constraining Quasar Relativistic Reflection Regions and Spins with Microlensing_ ([arXiv:1901.06007](https://arxiv.org/abs/1901.06007))

  exposition in:

  [[Chandra Observatory]], _[Chandra Views Spinning Black Holes Across Cosmic Sea](https://scitechdaily.com/chandra-views-spinning-black-holes-across-cosmic-sea/)_, July 5 2019


[[!redirects Kerr spacetimes]]

[[!redirects Kerr black hole spacetime]]
[[!redirects Kerr black hole spacetimes]]

[[!redirects Kerr black hole]]
[[!redirects Kerr black holes]]

[[!redirects spinning black hole]]
[[!redirects spinning black holes]]


[[!redirects Kerr solution]]
[[!redirects Kerr metric]]
[[!redirects Kerr black hole]]
[[!redirects Kerr-Newman black hole]]
[[!redirects Boyer-Lindquist coordinates]]
[[!redirects Boyer-Lindquist]]




