
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea 

Hamiltonian mechanics is a formulation of [[mechanics]] in which the basic datum in a mechanical system is a function $H$, the [[Hamiltonian]] of the system, which gives the total energy in the system in terms of the [[position|positions]] and [[momentum|momenta]] of the objects in the system.

More abstractly, the Hamiltonian is a function on [[phase space]], a [[manifold]] whose coordinates are [[generalized position|generalised]] positions $q^i$ and momenta $p_i$.  (Compare this to [[Lagrangian mechanics]], in which the [[Lagrangian]] is a function on [[state space]], whose coordinates are generalised positions and [[velocity|velocities]].)  So to do Hamiltonian mechanics properly, you must 'mind your $p$s and $q$s' (blame [[John Baez]] for this pun).

To begin with, we often take phase space to be the [[cotangent bundle]] of [[configuration space]].  (Compare that state space is the [[tangent bundle]] of configuration space.)  This comes equipped with a natural $2$-[[differential form|form]]
$$ \omega = \sum_i \mathrm{d}p_i \wedge \mathrm{d}q^i ,$$
or simply $\omega = \mathrm{d}p_i \wedge \mathrm{d}q^i$ using the [[Einstein summation convention]].  This $2$-form is closed, in fact exact, since it is the [[exterior derivative|differential]] of the [[action functional|action form]] $\bar{\mathrm{d}}S = p_i \wedge \mathrm{d}q^i$, and therefore it is a [[symplectic form]].

However, it is also possible to take phase space to be *any* [[symplectic manifold]], or even any [[Poisson manifold]].  In any case, phase space itself gives only the [[kinematics]] (in a momentum-based rather than velocity-based sense); you need the Hamiltonian $H$ to get the [[dynamics]].

Hamiltonian mechanics was developed originally for [[classical mechanics]], but it is also the best known formulation of [[quantum mechanics]]; many students of [[physics]] (and even more so, students of [[chemistry]]) learn it only when they study the latter.  This sometimes leads to confusion about the essential differences between classical and quantum physics.


## Definition in terms of symplectic geometry 

Hamiltonian mechanics is best formalized in terms of [[symplectic geometry]] as described for instance in the monograoph

* [[Vladimir Arnold]], _Mathemtical Methods of Classical Mechanics_ Springer.


A classical Hamiltonian [[mechanical system]] is a pair $((X,\omega), H)$ consisting of a 

* [[symplectic manifold]] $(X,\omega)$ 

* and a [[Hamiltonian]] function $H \in C^\infty(X)$.

Here 

* $X$ is the **[[phase space]]** of the physical system;

* a curve $\gamma : \mathbb{R} \to X$ is a **[[trajectory]]** of the physical system in time;

* $(X,\omega)$ defines the **[[kinematics]]** of the system;

* $H$ is the **[[Hamiltonian]]** that defined the **[[dynamics]]** of the system.

The **dynamics** is encoded by declaring that those trajectories $\gamma : \mathbb{R} \to X$ are the physically realized trajectories that satisfy the equation

$$
  d H = \omega(\gamma', -)
$$

The components of this are **[[Hamilton's equations]]**. 

In more detail this equation means that for each $t \in \mathbb{R}$ the [[differential form|1-form]]

$$
  (d H)_{\gamma(t)}
$$

and the 1-form 

$$
  \omega_{\gamma(t)}((\frac{d}{d t}\gamma(t), -)
$$

coincide.


### Comments on this definition 


At first, this formulation of Hamilton's mechanics is just that, an equivalent reformulation. 
But as any reformulation in more abstract terms, it serves to

1. clarify a structure

1. allow more powerful thinking about that structure

1. and eventually it bears in it the seed for further developments pointing beyond this structure

Regarding the first point: this formulation of Hamiltonian mechanics makes clear what the meaning of Hamilton's equations is for systems topologically more interesting than the example $X = \mathbb{R}^{2 n}$ that many introductory physics texts concentrate on-

Regarding the second point: the differential calculus formulation lends itself much more to high-powered arguments than the traditional component-ridden presentation. Of course the latter may still be the preferred method for some concrete computations.

Regarding the second point: after Hamilton's times people started thinking about what [[quantization]] of a classical system should mean. One successful formalization is that of [[geometric quantization]] which takes a symplectic manifold with Hamiltonian function on it as input datum.

The impact that this idea of quantization from symplectic geometry eventually had is hard to underestimate. In the hands of [[Alan Weinstein]] and his school it led to [[symplectic groupoid]]s, [[Courant algebroid]]s and other higher [[Lie theory|Lie theoretic structures]].  In the hands of [[Maxim Kontsevich]] it led to the theorem on formal [[deformation quantization]] and the vast machinery nowadays associated with that.

### Examples 

The symplectic-geometry description of Hamiltonian mechanics is especially well-suited to describe topologically nontrivial phase spaces that are not [[cotangent bundle]]s.

#### Vortices on the sphere 

$n$ vortices on the sphere as finite dimensional limit of 2D [[equation of motion|Euler equations]]: the phase space of the system of $n$ vortices is not a [[cotangent bundle]] but is $(S^2)^n$ .

## Related entries

* [[Hamilton's equations]]

* [[Hamilton-Jacobi equation]]

* traditional [[Lagrangian mechanics]] and [[Hamiltonian mechanics]] are naturally embedding into [[local prequantum field theory]] by the notion of [[prequantized Lagrangian correspondences]]

## References

Named after [[William Rowan Hamilton]].

Formulation in [[symplectic geometry]]:

* [[Vladimir Arnol'd]], _[[Mathematical methods of classical mechanics]]_, Graduate Texts in Mathematics **60**, Springer (1978) &lbrack;[doi:10.1007/978-1-4757-1693-1](https://doi.org/10.1007/978-1-4757-1693-1)&rbrack;

A motivation for formulating Hamiltonian mechanics in terms of [[symplectic manifolds]]:

 * Henry Cohn, _[Why symplectic geometry is the natural setting for classical mechanics ](http://math.mit.edu/~cohn/Thoughts/symplectic.html)_

