
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Variational calculus
+-- {: .hide}
[[!include variational calculus - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In [[physics]] the [[dynamics]] of a [[physical system]] may be encoded by a [[nonlinear functional]] -- called the **action functional** -- on its [[configuration space]]:

* in [[classical mechanics]] and [[classical field theory]] -- by the **action principle** or **[[principle of least action]]** -- the extrema of the action functional -- obtained by [[variational calculus]] and given by [[Euler-Lagrange equation]]s -- encode the physically observable configurations  ;

* in [[quantum mechanics]] and [[quantum field theory]] the evolution of the [[quantum state]]s is encoded by the integral -- the [[path integral]] -- of the exponentiated action functional over the space of field configurations.

For emphasis the description of dynamics by action functionals is called the **Lagrangean** approach. Another formulation of dynamics in physics that does not involve an action functional explicitly is [[Hamiltonian mechanics]] on [[phase space]]. At least in certain classes of cases the relation and equivalence of both approaches is understood. Generally the formulation of [[quantum field theory]] in terms of action functionals suffers from a lack of precise understanding of what the [[path integral]] over the action functional really means. 

\begin{imagefromfile}
  "file_name": "action_functional_on_a_napkin.jpg",
  "float": "left",
  "margin": {
    "top": 0,
    "right": 10,
    "bottom": 10,
    "left": 0,
    "unit": "px"
  },
  "alt": "Action functional on a napkin",
  "caption": "Taken from A Zee, Fearful Symmetry"
\end{imagefromfile}

## Definition

Let $\mathbf{H}$ be the ambient [[(∞,1)-topos]] with a [[natural numbers object]] and equipped with an additive [[continuum]] [[line object]] $\mathbb{A}^1$ (see there). Let $C \in \mathbf{H}$ be the [[configuration space]] of a physical system. Then an **action functional** is a morphism

$$
  \exp(\tfrac{i}{\hbar} S(-)) : C \to \mathbb{A}^1 / \mathbb{Z}
  \,
$$

(here $\hbar$ refers to [[Planck's constant]]).

If $\mathbf{H}$ is a [[cohesive (∞,1)-topos]] then there is an <a href="https://ncatlab.org/nlab/show/cohesive+(infinity,1)-topos+--+structures#CurvatureCharacteristics">intrinsic differential</a> of the action functional to a morphism

$$
  \mathbf{d} \exp(\tfrac{i}{\hbar} S(-)) : C \to \mathbf{\flat}_{dR}\mathbb{A}^1/\mathbb{Z}
  \,.
$$

The [[equation]]

$$  
  \mathbf{d} \exp(\tfrac{i}{\hbar} S(-)) = 0
$$

is the [[Euler-Lagrange equation]] of the system. It characterizes the [[critical locus]] of $S$ is the [[covariant phase space]] inside the configuration space: the space of classically realized trajectories/histories of the system. If $\mathbf{H}$ models [[derived geometry]] then this critical locus is presented by a [[BRST-BV complex]].


### Local action functionals (traditional theory)
 {#LocalActionFunctional}

An action functional is called **local** if it arises from integration of a [[Lagrangian]]. 

In traditional theory this is interpreted as follows: an action functional $S : C \to \mathbb{A}^1$ is called local if

* the [[configuration space]] $C$ is the space $C = \Gamma_X(E)$ of [[section]]s of a [[fiber bundle]] $E \to X$ over some parameter space ([[spacetime]] $X$);

* there is a [[Lagrangian]] density $J_\infty(E) \to \Omega^{\dim X}(X)$ on the [[jet bundle]] of $E$;

* on a section/field configuration $\phi : X \to E$ the action $S$ takes the value

  $$
    S(\phi) = \int_X L(j_\infty(\phi))
    \,,
  $$

  where $j_\infty(\phi) = (\phi, \partial_i \phi, \cdots)$ is the jet-prolongation of $\phi$ (the collection of all its higher partial derivatives).

Consider action functional for on a configuration space of 
[[smooth function]]s from the line to a [[smooth manifold]] $X$.

We can consider

1. $ S(q) = \int_a^b L(q,\dot{q}) \,\mathrm{d}t $, where $q$ is a path through configuration space, on the time interval $[a,b]$, with derivative $\dot{q} = \mathrm{d}q/\mathrm{d}t$.  When minimising the action, we fix the values of $q(a)$ and $q(b)$.
2. $ L(q,\dot{q}) = \int_{S} \mathcal{L}(q,\dot{q}) \,\mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z $, where now $q$ is a configuration of fields on $S$, which is a region of space.  We fix boundary conditions on the boundary of $S$ (typically that $q$ and $\dot{q}$ go to zero if $S$ is all of space).
3. $ S(q) = \int_{R} \mathcal{L}(q,\dot{q}) \,\mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z\,\mathrm{d}t $, where now $q$ is a configuration of fields on $R$, which a region of spacetime, with time derivative $\dot{q} = \partial{q}/\partial{t}$.  We fix boundary conditions on the boundary of $R$.

The formulation of (3) above is still not manifestly coordinate independent.  However, $\mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z\,\mathrm{d}t$ is simply the [[volume form]] on spacetime and $\dot{q}$ is merely one choice of coordinate on [[configuration space|state space]] and could just as easily be replaced by a derivative with respect to any timelike coordinate on spacetime (or drop coordinates altogether).

### Extended local action functionals in (higher) gauge theory
 {#ExtendedLocalInGaugeTheory}

For [[gauge theories]] and [[higher gauge theories]] the configuration spaces of the physical system are in general not plain [[manifolds]] or similar, but are [[orbifolds]] or more generally [[smooth groupoids]], [[smooth ∞-groupoids]]. (An exposition of and introduction to much of the following is at _[[geometry of physics]]_.)

For instance for $G$ a [[Lie group]] and $\mathbf{B}G_{conn}$ the smooth [[moduli stack]] of $G$-[[principal connections]] (see at [[connection on a bundle]]), then the [[smooth groupoid]] of $G$-[[gauge field]] configurations is the [[internal hom]]/[[mapping stack]] $[\Sigma, \mathbf{B}G_{conn}] \in $[[Smooth∞Grpd]] (or some concretification thereof, see at _[geometric of physics -- differential moduli](geometry%20of%20physics#DifferentialModuli)_: this is the [[smooth groupoid]] whose [[objects]] are $G$-[[gauge field]]-configurations on $\Sigma$ ([[connection on a bundle|connections]] on $G$-[[principal bundles]] over $\Sigma$), and whose [[morphisms]] are [[gauge transformations]] between these. The [[infinitesimal space|infinitesimal]] approximation to this [[smooth ∞-groupoid]], its _[[∞-Lie algebroid]]_ is the (off-shell) [[BRST complex]] of the theory. The tangent to the $n$-fold [[higher gauge transformations]] becomes the $n$-fold _ghosts_ in the BRST complex.

More generally $G$ here can by any [[smooth ∞-group]], such as the [[circle n-group]] $\mathbf{B}^{n-1}U(1)$ or the [[String 2-group]] or the [[Fivebrane 6-group]], and so on, in which case $[\Sigma, \mathbf{B}G_{conn}]$ is the [[smooth ∞-groupoid]] of [[higher gauge theory|higher gauge field]], [[gauge transformations]] between these, [[higher gauge transformations]] between those, and so on.

Notice that this means in particular that in [[higher geometry]] a [[gauge theory]] is a [[sigma-model]] [[quantum field theory]]: one whose [[target space]] is not just a plain [[manifold]] but is a [[moduli stack]] of gauge field configurations.

A [[gauge invariance|gauge invariant]] action functional is then a morphism of [[smooth ∞-groupoids]]

$$
  \exp( i S(-)) \colon [\Sigma, \mathbf{B}G_{conn}] \to U(1)
  \,.
$$

This is of particular interest, again, if it is _local_. In fact, in this context now we can also ask that it is "extended" in the sense of [[extended topological quantum field theory]]: that we have an action functional not only in top dimension, being a function, but also in codimension 1, being a [[prequantum bundle]], and in higher codimension, being a [[prequantum n-bundle]].

This is notably the case for all (higher) gauge theories of [[schreiber:infinity-Chern-Simons theory]] type, such as ordinary [[Chern-Simons theory]] and such as ordinary [[Dijkgraaf-Witten theory]], as well as its higher generalizations. In these cases the action functional $\exp(i S(-)) \colon [\Sigma, \mathbf{B}G_{conn}]$ arises itself from [[transgression]] of an [[extended Lagrangian]] that is defined on the universal [[moduli stack]] of gauge field configurations $\mathbf{B}G_{conn}$ itself, namely from a [[universal characteristic class]] in higher nonabelian [[differential cohomology]] of the form

$$
  \mathbf{L} \colon \mathbf{B}G_{conn} \to \mathbf{B}^n U(1)_{conn}
  \,.
$$

Here $\mathbf{B}^n U(1)_{conn}$ is the universal [[smooth infinity-groupoid|smooth]] [[moduli infinity-stack]] for [[circle n-bundles with connection]]. Such a morphism of moduli stacks locally takes a [[connection on a bundle|connection]] [[differential form]] $A$ to a [[Chern-Simons form]] $CS(A)$, but globally it sends the underlying [[principal bundle]] to a [[circle n-group|circle (n-1)-group]] [[principal ∞-bundle]] and accordingly acts globally on the connection. 
This is hence a fully local [[Lagrangian]]: an _[[extended Lagrangian]]_. Alternatively, one may think of this whole morphism as modulating a [[prequantum circle n-bundle]] on the universal moduli stack $\mathbf{B}G_{conn}$ of [[gauge fields]] itself. 

For instance for ordinary [[Chern-Simons theory]] here $n = 3$ $G$ is a [[semisimple Lie group]] and $\mathbf{L}$ is a smooth and differential refinement of the [[first Pontryagin class]]/[[second Chern class]], or of an integral multiple of that (the "level" of the theory). In this case $\mathbf{L}$ may also be thought of as modulating the universal [[Chern-Simons circle 3-bundle]]. If instead $G$ is a [[discrete group]] then $\mathbf{L}$ is a [[cocycle]] in the $U(1)$-[[group cohomology]] and this is the [[extended Lagrangian]] of [[Dijkgraaf-Witten theory]].

This [[extended Lagrangian]] becomes an extended action functional after [[transgression]]: the operation of [[fiber integration in ordinary differential cohomology]] refines to a morphism of moduli stacks of the form

$$
  \exp(2 \pi i \int_{\Sigma_k} (-))
  \colon
  [\Sigma_k, \mathbf{B}^n U(1)_{\mathrm{conn}} ]
  \to 
  \mathbf{B}^{n-k}U(1)_{conn}
 \,,
$$

where $\Sigma$ is an [[orientation|oriented]] [[closed manifold]] of [[dimension]] $k$. This morphism locally simply takes a [[differential n-form]] to its ordinary [[integration of differential forms]] over $\Sigma_k$, but globally it takes the correct [[higher holonomy]] of [[circle n-bundles with connection]]. 

Combining this with an extended [[schreiber:∞-Chern-Simons theory]] [[Lagrangian]] $\mathbf{L} \colon \mathbf{B}G_{conn} \to \mathbf{B}^n U(1)_{conn}$ as above yields for each dimension $k$ a [[prequantum circle n-bundle]] on the space of gauge field configurations over $\Sigma_k$, by forming the [[transgression]] composite

$$
  \exp(i S(-))
  \coloneqq
  \exp(2 \pi i \int_{\Sigma_k} [\Sigma_k, \mathbf{L}])
   \;\; \colon \;\;
  [\Sigma_k, \mathbf{B}G_{conn}]
  \stackrel{[\Sigma_k, \mathbf{L}]}{\to}
  [\Sigma_k, \mathbf{B}^n U(1)_{conn}]
  \stackrel{\exp(2 \pi i \int_{\Sigma_k}(-))}{\to}
  \mathbf{B}^{n-k}U(1)_{conn}
  \,.
$$

This morphism locally takes the local [[differential form]] incarnation $A$ of a [[connection on an ∞-bundle]]  to the exponentiation of the [[integration of differential forms]] $\int_\Sigma CS(A)$ of some higher [[Chern-Simons form]], but globally it computes the correct [[higher holonomy]] of the higher [[circle n-bundle with connection]] over the universal moduli stack of fields, as modulated by the extended [[Lagrangian]] $\mathbf{L}$.


## Examples

For [[spacetime]] [[field theory]]:

* [[Einstein-Hilbert action]]

  * [[Einstein-Maxwell theory]]

  * [[Einstein-Yang-Mills theory]]

  * [[Einstein-Yang-Mills-Dirac theory]]

  * [[Einstein-Maxwell-Yang-Mills-Dirac-Higgs theory]]

For [[branes]]:

* [[Nambu-Goto action]]

* [[Dirac-Born-Infeld action]]

* [[Perry-Schwarz action]]

* A large class of examples of action functionals arises in [[schreiber:∞-Chern-Simons theory]]. See there for details.


## Related concepts

[[!include action (physics) - table]]

* [[principle of extremal action]], [[Euler-Lagrange equations]]

* [[path integral]] [[quantization]]

* [[effective action functional]], [[background field formalism]]

* [[parent action functional]]

[[!include extended prequantum field theory - table]]


## References

Historical and expository accounts of the "[[principle of extremal action]]" or "action principle", for short:

* Agamenon R. E. Oliveira, *History of Two Fundamental Principles of Physics: Least Action and Conservation of Energy*, Advances in Historical Studies **3** 2 (2014) &lbrack;[doi:10.4236/ahs.2014.32008](http://dx.doi.org/10.4236/ahs.2014.32008)&rbrack;

* Walter Dittrich, *The Development of the Action Principle -- A Didactic History from Euler-Lagrange to Schwinger*, SpringerBriefs in Physics, Springer (2021) &lbrack;[doi:10.1007/978-3-030-69105-9](https://doi.org/10.1007/978-3-030-69105-9)&rbrack;

* [[Douglas Cline]], *Variational Principles in Classical Mechanics*, University of Rochester (2021) &lbrack;[pdf](http://classicalmechanics.lib.rochester.edu/pdf/Variational_Principles_in_Classical_Mechanics_3e_final_fbcover.pdf), <a href="https://phys.libretexts.org/Bookshelves/Classical_Mechanics/Variational_Principles_in_Classical_Mechanics_(Cline)">online version</a>&rbrack;

Textbook account in the context of [[gauge theories]]:

* [[Marc Henneaux]], [[Claudio Teitelboim]], §1.1.1 in: _[[Quantization of Gauge Systems]]_, Princeton University Press (1992) &lbrack;[ISBN:9780691037691](https://press.princeton.edu/books/paperback/9780691037691/quantization-of-gauge-systems), [jstor:j.ctv10crg0r](https://www.jstor.org/stable/j.ctv10crg0r)&rbrack;



Lecture notes with more details are in the section _[Lagrangians and Action functionals](geometry+of+physics#LagrangiansAndActionFunctionals)_ of 

* _[[geometry of physics]]_ .


Discussion of extended higher local action functional for (higher) gauge theories of generalized [[schreiber:∞-Chern-Simons theory]] type are discussed in

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Hisham Sati]], _[[schreiber:Extended higher cup-product Chern-Simons theories]]_

The extended local action functionals for ordinary 3d [[Chern-Simons theory]]/[[Dijkgraaf-Witten theory]] and for 7d [[String 2-group]] Chern-Simons theory are constructed in 

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Cech cocycles for differential characteristic classes]]_

and discussed further in 

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Hisham Sati]], _[[schreiber:7d Chern-Simons theory and the 5-brane]]_

A comprehensive discussion in a general context of higher differential geometry is in 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_


[[!redirects action functional]]
[[!redirects action functionals]]
[[!redirects action functinal]]

[[!redirects local action functional]]
[[!redirects local action functionals]]