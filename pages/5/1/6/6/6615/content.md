
# Nabla
* table of contents
{: toc}

## Idea

The operator __nabla__ (also called __Atled__ or __Del__, and written __$\nabla$__) is an operator introduced in [[quaternion]]ic analysis and now heavily used in elementary [[vector analysis]].  The [[gradient]], [[curl]], and [[divergence]] may all be defined in terms of it.


## Definition

Informally, nabla is defined to be a [[vector]] (to be thought of as a [[tangent vector]] on some [[manifold]], which is often taken to be the [[cartesian space]] $\mathbb{R}^3$) of [[differential operator]]s
$$ \nabla = \sum_{k = 1}^n e_k \frac{\partial}{\partial x^k} ,$$
and it may be applied to a [[scalar field]] or [[vector field]] in any way that it may be possible to multiply a scalar or vector (respectively) by a vector.  Classically, this gives three applications: the [[gradient]] of a scalar field (corresponding to scalar multiplication), the [[divergence]] of a vector field (corresponding to the [[inner product|dot product]]), and the [[curl|curl or rotation]] of a vector field (corresponding to the [[cross product]]).

Formally, all uses may be combined into a single definition based on [[integration]] on [[hypersurface]]s.  If $M$ is a smooth [[Riemannian manifold]], $V$ and $W$ are [[vector bundles]] over $M$, $\odot$ is a smooth [[bilinear operator]] from the [[tangent bundle]] and $V$ to $W$, and $T$ is a smooth [[section]] of $V$, then $\nabla \odot T$ is a smooth section of $W$ whose value at any point $x$ is given by the integral formula
$$
(\nabla \odot T)(x) = lim_{vol D\to 0} \frac{1}{vol D} \oint_{\partial D} \vec{n} \odot T \,d S,\,\,\,\,\stackrel{\circ}{D}\ni x,
$$
where $D$ runs over the regions with smooth boundary $\partial{D}$ containing the point $x$ and $\vec{n}$ is the unit vector of outer normal to the surface $S=\partial D$.

The formula does not depend (when everything in smooth) on the shape of boundaries taken in limiting process, so one can typically take a [[coordinate chart]] containing balls $D = D_r$ with decreasing radius $r \gt 0$ in this particular coordinate chart.  The formula also does not depend on [[orientation]]; $\partial{D}$ is naturally a [[pseudo-oriented submanifold|pseudo-oriented]] [[submanifold]] and so $\vec{n} \odot T \,d S$ (also written $d\vec{S} \odot T$) is a $W$-valued [[pseudoform|pseudo]]-$(n-1)$-[[differential form|form]], and we can integrate pseudoforms on pseudo-oriented submanifolds.  Perhaps most surprisingly, although it makes no sense in general to integrate $W$-valued (pseudo)forms (unless $W$ is a [[trivial bundle]]), we may simply perform the integration using any coordinate chart as if we were in the cartesian space $\mathbb{R}^n$ (where every vector bundle is trivial), and the limit is again independent of this choice.

This formula can also be extended to the case where $T$, or anything else up to $M$ itself, is only $C^k$ and not smooth, at the risk that $\nabla \odot T$ might not be defined or that the choice of coordinate chart might make a difference even in the limit.  In that case, we consider that $\nabla \odot T$ is defined only if the choice of coordinate chart in fact makes no difference.


## Historical and terminological notes 

The nabla is an old instrument in the shape of inverted triangle, sort of an Assyrian harp.  [[William Hamilton]] introduced the operator $\nabla$ (sometimes called Hamilton's or Hamiltonian operator, but distinguish strictly from [[Hamiltonian]] in the mechanics sense) and [[James Maxwell]] used it to write [[Maxwell's equations|his equations]].

* History of nabla [nabla.txt](https://arnold-neumaier.at/contrib/nabla.txt)

The terms 'Atled' and 'Del' are based on the idea that the nabla is an upside-down capital Greek Delta.  Sometimes the [[partial derivative]] symbol $\partial$ is taken to be the lowercase equivalent, as it is a variant (but not upside-down) of the lowercase Delta.


## Related concepts


* **nabla**

* [[gradient]]

  * [[gradient flow]]

  * [[symplectic gradient]]

* [[Hamiltonian flow]]

* [[curl]]

* [[divergence]]


## References

* G.E. Shilov, _Mathematical analysis (functions of several real variables)_, part 1--2


[[!redirects nabla]]
[[!redirects Atled]]
[[!redirects Del]]
