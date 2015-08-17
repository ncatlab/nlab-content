
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The [[sphere]] of [[dimension]] 7.

This is one of the [[parallelizable manifold|parallelizable]] spheres, as such corresponds to the [[octonions]] among the [[division algebras]], being the manifold of unit octonions, and is the only one of these which does not carry ([[Lie group|Lie]]) [[group]] structure but just [[Moufang loop]] structure.


## Properties



### Hopf fibration

The 7-sphere participates in the [[quaternionic Hopf fibration]], the analog of the complex [[Hopf fibration]] with the field of [[complex numbers]] replaced by the division ring of [[quaternions]] or Hamiltonian numbers $\mathbb{H}$.

$$
  \array{
    S^3 &\hookrightarrow& S^7
    \\
    && \downarrow \mathrlap{p}
    \\
    && S^4 &\stackrel{}{\longrightarrow}& \mathbf{B} SU(2)
  }
$$

Here the idea is that $S^7$ can be construed as $\{(x, y) \in \mathbb{H}^2: {|x|}^2 + {|y|}^2 = 1\}$, with $p$ mapping $(x, y)$ to $x/y$ as an element in the [[projective line]] $\mathbb{P}^1(\mathbb{H}) \cong S^4$, with each [[fiber]] a [[torsor]] parametrized by quaternionic [[scalars]] $\lambda$ of unit [[norm]] (so $\lambda \in S^3$).  This canonical $S^3$-bundle (or $SU(2)$-bundle) is classified by a map $S^4 \to \mathbf{B} SU(2)$. 

## Smooth structures 

A celebrated result of Milnor is that $S^7$ admits [[exotic smooth structures]] (exotic spheres), i.e., there are [[smooth manifold]] structures on the [[topological manifold]] $S^7$ that are not [[diffeomorphism|diffeomorphic]] to the standard smooth structure on $S^7$. More structurally, considering smooth structures up to [[orientation|oriented]] diffeomorphism, the different smooth structures form a [[monoid]] under a (suitable) operation of [[connected sum]], and this monoid is isomorphic to the [[cyclic group]] $\mathbb{Z}/(28)$. With the notable possible exception of $n = 4$ (where the question of existence of exotic 4-spheres is wide open), exotic spheres first occur in dimension $7$. This phenomenon is connected to the [[h-cobordism theorem]] (the monoid of smooth structures is identified with the monoid of h-cobordism classes of oriented [[homotopy spheres]]). 

One explicit construction of the smooth structures is given as follows (see [Milnor 1968](#Mil2)). Let $W_k$ be the algebraic variety in $\mathbb{C}^5$ defined by the equation 

$$z_1^{6 k - 1} + z_2^3 + z_3^2 + z_4^2 + z_5^2 = 0$$ 

and $S_\epsilon \subset \mathbb{C}^5$ a sphere of small radius $\epsilon$ centered at the origin. Then each of the $28$ smooth structures on $S^7$ is represented by an intersection $W_k \cap S_\epsilon$, as $k$ ranges from $1$ to $28$. These manifolds sometimes go by the name _Brieskorn manifolds_ or [[Brieskorn sphere]]s[^1]. 

[^1]: Not surprisingly, these exotic spheres are also called _Milnor spheres_. 

## References

* [[Martin Cederwall]], Christian R. Preitschopf, _The Seven-sphere and its Kac-Moody Algebra_, Commun. Math. Phys. 167 (1995) 373-394 ([arXiv:hep-th/9309030](http://arxiv.org/abs/hep-th/9309030))

* Takeshi &#212;no, _On the Hopf fibration $S^7 \to S^4$ over $Z$_, Nagoya Math. J.
Volume 59 (1975), 59-64. ([Euclid](http://projecteuclid.org/euclid.nmj/1118795554))

An [[ADE classification]] of finite subgroups of groups $SO(8)$ [[free action|acting freely]] on $S^7$ such that the quotient is spin and has at least four [[Killing spinors]]


* Paul de Medeiros, [[José Figueroa-O'Farrill]], Sunil Gadhia, [[Elena Méndez-Escobar]], _Half-BPS quotients in M-theory: ADE with a twist_, 	JHEP 0910:038,2009 ([arXiv:0909.0163](http://arxiv.org/abs/0909.0163), [pdf slides](http://www.maths.ed.ac.uk/~jmf/CV/Seminars/YRM2010.pdf))

* Paul de Medeiros, [[José Figueroa-O'Farrill]], _Half-BPS M2-brane orbifolds_ ([arXiv:1007.4761](http://arxiv.org/abs/1007.4761))

* Wikipedia, _Exotic sphere_, [link](https://en.wikipedia.org/wiki/Exotic_sphere). 

The explicit construction of exotic 7-spheres by intersecting algebraic varieties with spheres is described in 

* J. Milnor, "Singular points of complex hypersurfaces" , Princeton Univ. Press (1968). 
 {#Mil2}

[[!redirects 7-spheres]]

[[!redirects seven sphere]]
[[!redirects seven spheres]]

[[!redirects quaternionic Hopf fibration]]