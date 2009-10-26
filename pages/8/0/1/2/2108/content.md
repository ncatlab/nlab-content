
#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

_Geometric quantization_ is the approach of Kirillov ("orbit method"), Kostant and Souriau for attaching a [[Hilbert space]] to a [[symplectic manifold]] with a [[line bundle]] with [[connection]], provided the symplectic manifold satisfies certain quantization conditions.

It can be interpreted as a procedure of [[quantization]] that sends a classical system defined by the [[symplectic geometry]] $(P,\omega)$ of its [[phase space]] $P$ equipped with a Hamiltonian vector field to a [[Hilbert space]] of states on which a [[Hamiltonian operator]] acts, whose flow describes the [[quantum field theory|quantum dynamics]] of the physical system in question. Geometric quantization is closely related to [[Berezin quantization]] and the subject of [[coherent states]].

The basic idea is to let the quantum Hilbert space of states be _half_ the space of [[section]]s of a [[vector bundle|line bundle]] [[connection on a bundle|with connection]] whose curvature $2$-form coincides with the symplectic form $\omega$.

In a long term project [[Alan Weinstein]] and many of his students have followed the idea that the true story behind this prescription crucially involves [[Lie groupoid]]s.

This idea has been developed quite far. A good reference is the work of [[Eli Hawkins]]

* Eli Hawkins, _A Groupoid Approach to Quantization_ ([arXiv](http://arxiv.org/abs/math.SG/0612363))

Blog discussion of this is at

* [Eli Hawkins on Geometric Quantization, I](http://golem.ph.utexas.edu/category/2008/06/eli_hawkins_on_geometric_quant.html)

* [Eli Hawkins on Geometric Quantization, II](http://golem.ph.utexas.edu/category/2008/06/eli_hawkins_on_geometric_quant_1.html)

* [Landsman on Quantization of Poisson Algebras Associated to Lie Algebroids](http://golem.ph.utexas.edu/category/2008/06/landsmanon_quantization_of_poi.html)


# Overview #

Geometric quantization is a marvelous tool for understanding the relation between classical physics and [[quantum field theory|quantum physics]]. However, it's a bit like a power tool -- you have to be an expert to operate it without running the risk of seriously injuring your brain. Here's a brief sketch of how it goes. This is pretty terse; for the details you'll have to read the series of articles on geometric quantization on the sci.physics.research archive.

1. We start with a *classical phase space*: mathematically, this is a [[manifold]] $X$ with a [[symplectic geometry|symplectic structure]] $\omega$.

1. Then we do *prequantization*: this gives us a Hermitian [[vector bundle|line bundle]] $L$ over $X$, equipped with a $U(1)$ [[connection on a bundle|connection]] $D$ whose curvature equals $i \omega$. $L$ is called the *prequantum line bundle*.

   **Warning:** we can only do this step if $\omega$ satisfies the *Bohr--Sommerfeld condition*, which says that $\omega/2\pi$ defines an [[Eilenberg-MacLane spectrum|integral cohomology]] class. If this condition holds, $L$ and $D$ are determined up to [[isomorphism]], but not canonically.

1. The [[Hilbert space]] $H_0$ of square-integrable [[section]]s of $L$ is called the *prequantum Hilbert space*. This is not yet the Hilbert space of our quantized theory -- it's too big. But it's a good step in the right direction. In particular, we can *prequantize classical observables*: there's a map sending any smooth function on $X$ to an operator on $H_0$. This map takes [[Poisson bracket]]s to [[commutator]]s, just as one would hope. The formula for this map involves the [[connection on a bundle|connection]] $D$.

1. To cut down the prequantum Hilbert space, we need to choose a *[[polarization]]*, say $P$. What's this? Well, for each point $x \in X$, a polarization picks out a certain subspace $P_x$ of the complexified [[tangent bundle|tangent space]] at $x$. We define the *quantum Hilbert space*, $H$, to be the space of all square-integrable sections of $L$ that give zero when we take their [[covariant derivative]] at any point $x$ in the direction of any vector in $P_x$. The quantum Hilbert space is a subspace of the prequantum Hilbert space.

   **Warning:** for $P$ to be a polarization, there are some crucial technical conditions we impose on the subspaces $P_x$. First, they must be *isotropic*: the complexified symplectic form $\omega$ must vanish on them. Second, they must be *Lagrangian*: they must be maximal isotropic subspaces. Third, they must vary smoothly with $x$. And fourth, they must be *integrable*.

1. The easiest sort of polarization to understand is a *real polarization*. This is where the subspaces $P_x$ come from subspaces of the tangent space by complexification. It boils down to this: a real polarization is an integrable distribution $P$ on the classical phase space where each space $P_x$ is Lagrangian subspace of the tangent space $T_x X$.

1. To understand this rigamarole, one must study examples! First, it's good to understand how good old *Schr&#246;dinger quantization* fits into this framework. Remember, in [[Schrodinger quantization|Schrödinger quantization]] we take our classical [[phase space]] $X$ to be the [[cotangent bundle]] $T^* M$ of a [[manifold]] $M$ called the *classical configuration space*. We then let our quantum Hilbert space be the space of all square-integrable functions on $M$.

   Modulo some technical trickery, we get this example when we run the above machinery and use a certain god-given real polarization on $X = T*M$, namely the one given by the vertical vectors.

1. It's also good to study the *Bargmann--Segal representation*, which we get by taking $X = \mathbb{C}^n$ with its god-given symplectic structure (the imaginary part of the inner product) and using the god-given *K&#228;hler polarization*. When we do this, our quantum Hilbert space consists of analytic functions on $\mathbb{C}^n$ which are square-integrable with respect to a Gaussian measure centered at the origin.

1. The next step is to *quantize classical observables*, turning them into linear operators on the quantum Hilbert space $H$. Unfortunately, we can't quantize all such observables while still sending [[Poisson bracket]]s to [[commutator]]s, as we did at the prequantum level. So at this point things get trickier and my brief outline will stop. Ultimately, the reason for this problem is that quantization is not a [[functor]] from the [[category]] of symplectic manifolds to the category of Hilbert spaces -- but for that one needs to learn a bit about [[category theory]]. 

# Basic Jargon # 

Here are some definitions of important terms. Unfortunately they are defined using other terms that you might not understand. If you are really mystified, you need to read some books on [[differential geometry]] and the math of [[classical mechanics]] before proceeding.

* **complexification**: We can tensor a real vector space with the complex numbers and get a complex vector space; this process is called complexification. For example, we can complexify the tangent space at some point of a manifold, which amounts to forming the space of complex linear combinations of tangent vectors at that point.

* **distribution**: The word "distribution" means many different things in mathematics, but here's one: a "distribution" $V$ on a manifold $X$ is a choice of a subspace $V_x$ of each tangent space $T_p X$, where the choice depends smoothly on $x$.

* **Hamiltonian vector field**: Given a manifold $X$ with a symplectic structure $\omega$, any smooth function $f: X \to \mathbb{R}$ can be thought of as a "Hamiltonian", meaning physically that we think of it as the energy function and let it give rise to a flow on $X$ describing the time evolution of states. Mathematically speaking, this flow is generated by a vector field $v(f)$ called the "Hamiltonian vector field" associated to $f$. It is the unique vector field such that

  $$
    \omega(-, v(f)) = d f
  $$

  In other words, for any vector field $u$ on $X$ we have

  $$
    \omega(u,v(f)) = d f(u) = u f
  $$


  The vector field $v(f)$ is guaranteed to exist by the fact that $\omega$ is nondegenerate.

* **integrable distribution**: A distribution on a manifold $X$ is "integrable" if at least locally, there is a foliation of $X$ by submanifolds such that $V_x$ is the tangent space of the submanifold containing the point $x$.

* **integral cohomology class**: Any closed $p$-form on a manifold $M$ defines an element of the $p$th [[de Rham cohomology]] of $M$. This is a finite-dimensional vector space, and it contains a lattice called the $p$th integral [[cohomology group]] of $M$. We say a cohomology class is integral if it lies in this lattice. Most notably, if you take any $U(1)$ [[connection on a bundle|connection]] on any Hermitian line bundle over $M$, its curvature $2$-form will define an integral cohomology class once you divide it by $2 \pi i$. This cohomology class is called the first [[Chern class]], and it serves to determine the line [[bundle]] up to [[isomorphism]].

* **[[Poisson bracket]]s**: Given a symplectic structure on a manifold $M$ and given two smooth functions on that manifold, say $f$ and $g$, there's a trick for getting a new smooth function $\{f,g\}$ on the manifold, called the Poisson bracket of $f$ and $g$.

  This trick works as follows: given any smooth function $f$ we can take its differential $d f$, which is a $1$-form. Then there is a unique vector field $v(f)$, the Hamiltonian vector field associated to $f$, such that

  $$
    \omega(-,v(f)) = d f
  $$

   Using this we define

   $$
     \{f,g\} = \omega(v(f),v(g))
   $$

   It's easy to check that we also have $\{f,g\} = d g(v(f)) = v(f) g$. So $\{f,g\}$ says how much $g$ changes as we differentiate it in the direction of the Hamiltonian vector field generated by $f$.

   In the familiar case where $M$ is $\mathbb{R}^{2n}$ with momentum and position coordinates $p_i$, $q_i$, the Poisson brackets of $f$ and $g$ work out to be

   $$
     \{f,g\} = \sum_i \frac{d f}{d p_i} \frac{d g}{d q_i} - \frac{d f}{d q_i}\frac{d g}{d p_i}
   $$

* **square-integrable sections**: We can define an inner product on the sections of a Hermitian line bundle over a manifold $X$ with a symplectic structure. The symplectic structure defines a volume form which lets us do the necessary integral. A section whose inner product with itself is finite is said to be square-integrable. Such sections form a Hilbert space $H_0$ called the "prequantum Hilbert space". It is a kind of preliminary version of the Hilbert space we get when we quantize the classical system whose phase space is $X$.

* **symplectic structure**: A symplectic structure on a manifold $M$ is a closed $2$-form $\omega$ which is nondegenerate in the sense that for any nonzero tangent vector $u$ at any point of $M$, there is a tangent vector $u$ at that point for which $w(u,v)$ is nonzero.

* **$U(1)$ [[connection on a bundle|connection]]**: The [[group]] $U(1)$ is the group of unit complex numbers. Given a complex line bundle $L$ with an inner product on each fiber $L_x$, a $U(1)$ connection on $L$ is a connection such that parallel translation preserves the inner product.

* **vertical vectors**: Given a bundle $E$ over a manifold $M$, we say a tangent vector to some point of $E$ is vertical if it projects to zero down on $M$. 

>The only way to learn the rules of this Game of games is to take the usual prescribed course, which requires many years, and none of the initiates could ever possibly have any interest in making these rules easier to learn. --- Hermann Hesse, The Glass Bead Game

# of Poisson manifolds #

One can also consider the theory of geometric quantization of just [[Poisson manifold]]s. This is done in terms of [[symplectic groupoid]]s.

#References#

many references should go here. 

The above "Overview" and "Basic Jargon" sections are taken from 

* [[John Baez]], _Geometric Quantization_ ([web](http://math.ucr.edu/home/baez/quantization.html))
