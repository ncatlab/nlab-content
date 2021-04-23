> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

When formulating a [[theory of physics]] in terms of [[mathematics]] one typically models the range of certain physical quantities by [[torsors]] over some [[group]] of transformations.  

For instance a [[wavelength]] would be identified as element in the [[real line]] minus its origin, $\mathbb{R}-\{0\}$ , being a torsor over the [[multiplicative group]] $\mathbb{R}^\times$ of [[real numbers]]. 

In order for the "[[coordination]]" of the mathematical theory with physical [[experiment]] to take place, one needs to choose an identification of this abstract torsor with the (idealized) one that it is supposed to model in nature. Such a choice is equivalent to a choice of [[unit]] (in the mathematical sense), hence a choice of element of the torsor. In this context this is then a _physical unit_. 

For instance picking an element in $\mathbb{R}-\{0\}$ and declaring this to be length of the path travelled by light in a vacuum in 
1/299 792 458 second means defining a _physical unit of length_ (in this example:  of the [[meter]]).

Physical units are often called _physical constants_. But by definition physical units are arbitrary choices made in the desciption of a physical system. Of course once made, one wants to keep these choices constant, such as to be useful. 

The actual _constants of nature_ are instead quotients of physical units. For instance the [[fine structure constant]] is the [[quotient]]

$$
  \alpha \coloneqq \frac{e^2}{ (4 \pi \epsilon_0) \hbar c} \in \mathbb{R}
$$

where $e$ is the [[electric charge]] of the [[electron]] expressed in physical units of charge (such as [[coulomb]]s), $\hbar$ is [[Planck's constant]] etc. The resulting quotient is then independent of any choices and is hence a [[real number]] characterizing nature independently of any conventions about how to parameterize it.

Notice that _choice of unit_ is also called _choice of gauge_. This is indeed the same "[[gauge]]" as in "[[gauge theory]]", as it is how ([Weyl 23](gauge#Weyl23)) introduced the concept of gauge theory: as a theory in which the choice of unit of length may change along paths in space.

## Units of length in Lagrangian field theory
 {#UnitsOfLengthInLagrangianFieldTheory}

> under construction

Let $\Sigma \simeq \mathbb{R}^{p,1}$ be [[Minkowski spacetime]] and 
let $E \overset{fb}{\to} \Sigma$ be a [[fiber bundle]] thought of as a [[field]] bundle. Write $\{\phi^a\}$ for local [[coordinates]] on the typical fiber of this bundle. 

The total space of the corresponding [[jet bundle]] $J^\infty_\Sigma(E) \overset{jb^\infty}{\to} \Sigma$ carries an [[action]] 

$$
  sc \;\colon\; \mathbb{R}^\times \times J^\infty_\Sigma(E) \longrightarrow J^\infty_\Sigma(E)
$$

of the multiplicative [[group of units]] $\mathbb{R}^\times$ of the [[real numbers]], given on the induced jet coordinates by

$$
  \begin{aligned}
    x^\mu & \mapsto r x^\mu
    \\
    \phi^a & \mapsto \phi^a
    \\
    \phi^a_{,\mu_1, \cdots \mu_k} & \mapsto r^{-k} \phi^a_{,\mu_1 \cdots \mu_k}
  \end{aligned}
  \,.
$$

Let then 

$$
  \mathbf{L}_{(-)}
   \;\colon\;
  \mathbb{R}^n \longrightarrow \mathbf{\Omega}^{p+1}(J^\infty_\Sigma(E))
$$

be a smoothly $n$-parameterized collection of [[Lagrangian densities]], equipped with an $R^\times$-action 

$$
  scp \;\colon\; \mathbb{R}^\times \times \mathbb{R}^n \longrightarrow \mathbb{R}^n
$$

on $\mathbb{R}^n$. 

Observe that the [[Euler-Lagrange equations]] induced by a Lagrangian density $\mathbf{L}$ equal those induced by the rescaled Lagrangian $r \mathbf{L}$, and that the [[presymplectic current]] $\Omega_{BFV}$ induced by $\mathbf{L}$ scales linearly with $r$ itself. Upon [[quantization]], this rescaling of $\Omega_{BFV}$ may be absorbed in [[Planck's constant]]. In conclusion, as long as Lagrangian densities scale _homogeneously_ the rescaled Lagrangian induces the same physics.

Hence we require that the combined scaling action of $\mathbb{R}^\times$ on $J^\infty_\Sigma(E)$ via $sc$ and on the parameters in $\mathbb{R}^n$ via $scp$ is homogeneous on $\mathbf{L}$ in that there exists $dim \in \mathbb{Z}$ such that  for every $r \in \mathbb{R}^\times$ we have

$$
  sc_r^\ast \mathbf{L}_{( scp(-))} = r^{dim} \mathbf{L}_{(-)}
  \,.
$$


Then a parameter $a \colon \mathbb{R}^n \to \mathbb{R}$ such that there exists $w \in \mathbb{Z}$ with 

$$
  scp_r^\ast a = r^{w} a
$$

is said to have _dimension_ $[length]^{w}$.

For example the Lagrangian density for the [[free field theory|free]] [[scalar field]]

$$
  \mathbf{L}_{(-)} 
     \;\colon\; 
   \mathbb{R}^1 
     \longrightarrow 
   \mathbf{\Omega}^{p+1}(J^\infty_\Sigma(\Sigma \times \mathbb{R})
$$

given by

$$
  \mathbf{L}_{m}
  \;\coloneqq\;
  \tfrac{1}{2}
  \left(
    \eta^{\mu \nu}\phi_{,\mu} \phi_{,\nu} 
    -
    m^2 \phi^2
  \right)
  dvol
$$

is parameterized by the [[mass]] $m$. For the Lagrangian to scale homogenously with $r^{p-1}$ the mass parameter has to have dimension $[length]^{-1}$. To indicate this action one writes the mass in the combination $m c / \hbar$, called the inverse _[[Compton wavelength]]_, so that the homogenously scaling collection of Lagrangians is 

$$
  \mathbf{L}_{m c / \hbar}
  \;\coloneqq\;
  \tfrac{1}{2}
  \left(
    \eta^{\mu \nu}\phi_{,\mu} \phi_{,\nu} 
    -
    \left(
      \tfrac{m c}{\hbar}
    \right)
   \phi^2
  \right)
  dvol
$$




(...)



## Examples

* [[meter]], [[femtometer]]

* [[electronvolt]], [[MeV]], [[GeV]], [[TeV]]

* [[Boltzmann constant]]

[[!include fundamental scales -- contents]]


## Related concepts

* [[comoving time]]

## References

Discussion in the context of [[philosophy of science]] includes

* [[Georg Hegel]], [Book I, third section, first chapter](Science+of+Logic#TheMeasureFirstChapter)  of _[[Science of Logic]]_


[[!redirects physical unit]]
[[!redirects physical units]]
