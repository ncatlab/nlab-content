#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

__Symplectic geometry__ is a branch of [[differential geometry]] studying [[symplectic manifold]]s and some generalizations; it originated as a formalization of the mathematical aparatus of [[classical mechanics]] and geometric optics (and the related WKB-method in [[quantum mechanics]] and, more generally, the method of stationary phase in [[harmonic analysis]]). A wider branch including symplectic geometry is [[Poisson geometry]] and a sister branch in odd dimensions is [[contact geometry]]. A special and central role in the subject belongs to certain real-like half-dimensional submanifolds, called [[Lagrangian submanifold|lagrangian (or Lagrangean) submanifolds]], which are in some sense classical points. Symplectic geometry radically changed after the 1985 article of Gromov on pseudoholomorphic curves and the subsequent work of Floer giving birth to symplectic topology or "hard methods" of symplectic geometry. 

*  Online reference (for soft period): Victor Guillemin, Shlomo Sternberg, _Geometric asymptotics_, AMS 1977, [online](http://www.ams.org/online_bks/surv14)


# Related concepts and applications #

* In its application to [[physics]], symplectic geometry is the fundamental mathematical language for [[Hamiltonian mechanics]], [[geometric quantization]], geometrical optics. 


* A tremendous amount of insight into higher [[Lie theory]] ([[Lie groupoid]]s, [[Lie ∞-groupoid]]s, [[Lie ∞-algebroid]]s) has derived from [[Alan Weinstein]]'s long-term project of understanding the role of symplectic geometry in [[geometric quantization]]. See there for more details.

+--{.query}
[[Zoran ?koda]]: it is true that large influence of Weinstein's program can not be overestimated, but it is not the origin of these considerations; it rather builds up on earlier fundamental works of Kirillov, Kostant, Souriau who invented geometric quantization, all of them originally in symplectic context; and the florishing of the subject from mid 1960s till mid 1980-s is related to their work; and other related tracks of Guillemin, Sternberg, Kashiwara, Karasev, Arnold and so on; and vast developments in harmonic analysis and representation theory (Kostant, Auslander, Vogan, Wallach, Stein...), microlocal analysis (Kashiwara, Saito, Hormander, Maslov, Karasev, Duistermaat...),  integrable systems/quantum groups (this is more into more general Poisson geometry: Lie-Poisson groups, classical r-matrices, bihamiltonian systems...), and  related approaches to quantization (Berezin method, coherent states...).  
=--

* There is a [[vertical categorification]] of symplectic geometry, called _multisymplectic geometry_ . For more on this see

  * [[John Baez]], [[Chris Rogers]], _Categorified Symplectic Geometry and the String Lie 2-Algebra_, ([arXiv](http://arxiv.org/abs/0901.4721))

* [[T-duality]] and mirror symmetry interchange the symplectic data and geometric structure data. Some cases of it can be unified in a broader concept of [[generalized complex geometry]].


# Symplectic geometry and classical Hamiltonian mechanics #

The notion of symplectic geometry may be understood as the mathematical structure that underlies the physics of [[Hamiltonian mechanics]]. A classical monograph that emphasizes this point of view is

* [[Vladimir Arnold]], _Mathemtical Methods of Classical Mechanics_ Springer.


In this framework, a classical Hamiltonian system is precisely a pair $((X,\omega), H)$ consisting of a symplectic manifold $(X,\omega)$ and a function $H \in C^\infty(X)$.

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

At first, this reformulation of Hamilton's mechanics is just that, an equivalent reformulation. 
But as any reformulation in more abstract terms, it serves to

1. clarify a structure

1. allow more powerful thinking about that structure

1. and eventually it bears in it the seed for further developments pointing beyond this structure

Regarding the first point: this formulation of Hamiltonian mechanics makes clear what th meaning of Hamilton's equations is for systems topologically more interesting than the example $X = \mathbb{R}^{2 n}$ that many introductory physics texts concentrate on-

Regarding the second point: the differential calculus formulation lends itself much more to high-powered arguments than the traditional component-ridden presentation. Of course the latter may still be the preferred method for some concrete computations.

Regarding the second point: after Hamilton's times people started thinking about what [[quantization]] of a classical system should mean. One successful formalization is that of [[geometric quantization]] which takes a symplectic manifold with Hamiltonian function on it as input datum.

The impact that this idea of quantization from symplectic geometry eventually had is hard to underestimate. In the hands of [[Alan Weinstein]] and his school it led to [[symplectic groupoid]]s, [[Courant algebroid]]s and other higher [[Lie theory|Lie theoretic structures]].  In the hands of [[Maxim Kontsevich]] it led to the theorem on formal [[deformation quantization]] and the vast machinery nowadays associated with that.