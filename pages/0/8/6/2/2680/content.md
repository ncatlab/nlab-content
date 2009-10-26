#Contents#
* automatic table of contents goes here
{:toc}


# Definition in terms of symplectic geometry #

Hamiltonian mechanics is best formalized in terms of [[symplectic geometry]] as described for instance in the monograoph

* [[Vladimir Arnold]], _Mathemtical Methods of Classical Mechanics_ Springer.


A classical Hamiltonian system is a pair $((X,\omega), H)$ consisting of a 

* [[symplectic manifold]] $(X,\omega)$ 

* and a function $H \in C^\infty(X)$.

Here 

* $X$ is the **phase space** of the physical system;

* a curve $\gamma : \mathbb{R} \to X$ is a **trajectory** of the physical system in time;

* $(X,\omega)$ defines the **kinematics** of the system;

* $H$ is the **Hamiltonian** that defined the **dynamics** of the system.

The **dynamics** is encoded by declaring that those trajectories $\gamma : \mathbb{R} \to X$ are the physically realized trajectories that satisfy the equation

$$
  d H = \omega(\gamma', -)
$$

The components of this are **Hamilton's equations**. 

In more detail this equation means that for each $t \in \mathbb{R}$ the [[differential form|1-form]]

$$
  (d H)_{\gamma(t)}
$$

and the 1-form 

$$
  \omega_{\gamma(t)}((\frac{d}{d t}\gamma(t), -)
$$

coincide.


## comments on this definition ##


At first, this formulation of Hamilton's mechanics is just that, an equivalent reformulation. 
But as any reformulation in more abstract terms, it serves to

1. clarify a structure

1. allow more powerful thinking about that structure

1. and eventually it bears in it the seed for further developments pointing beyond this structure

Regarding the first point: this formulation of Hamiltonian mechanics makes clear what th meaning of Hamilton's equations is for systems topologically more interesting than the example $X = \mathbb{R}^{2 n}$ that many introductory physics texts concentrate on-

Regarding the second point: the differential calculus formulation lends itself much more to high-powered arguments than the traditional component-ridden presentation. Of course the latter may still be the preferred method for some concrete computations.

Regarding the second point: after Hamilton's times people started thinking about what [[quantization]] of a classical system should mean. One successful formalization is that of [[geometric quantization]] which takes a symplectic manifold with Hamiltonian function on it as input datum.

The impact that this idea of quantization from symplectic geometry eventually had is hard to underestimate. In the hands of [[Alan Weinstein]] and his school it led to [[symplectic groupoid]]s, [[Courant algebroid]]s and other higher [[Lie theory|Lie theoretic structures]].  In the hands of [[Maxim Kontsevich]] it led to the theorem on formal [[deformation quantization]] and the vast machinery nowadays associated with that.