

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Trigonometry
+-- {: .hide}
[[!include trigonometry -- contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--



# Euclidean spaces
* table of contents
{: toc}

## Idea

The concept of  _Euclidean space_ in [[analysis]], [[topology]], [[differential geometry]] and specifically _[[Euclidean geometry]]_, and [[physics]] is a fomalization in modern terms of the [[spaces]] studied in [Euclid 300BC](#Euclid300BC), equipped with the [[extra structure|structures]] that Euclid recognised his spaces as having.

In the strict sense of the word, Euclidean space $E^n$ of dimension $n$ is, up to [[isometry]], [[generalized the|the]] [[metric space]] whose underlying [[set]] is the [[Cartesian space]] $\mathbb{R}^n$ and whose [[distance]] function $d$ is given by the [[Euclidean norm]]: 

$$
  d_{Eucl}(x,y) \coloneqq {\Vert x-y\Vert} = \sqrt{ \sum_{i = 1}^n (y_i - x_i)^2 }
  \,.
$$

In [Euclid 300BC](#Euclid300BC) this is considered for $n = 3$; and it is considered not in terms of [[coordinate functions]] as above, but via [[axioms]] of _[[synthetic geometry]]_.

This means that in a Euclidean space one may construct for instance the [[unit sphere]] around any point, or the shortest [[curve]] connecting any two points. These are the operations studied in ([Euclid 300BC](#Euclid300BC)), see at _[[Euclidean geometry]]_.

Of course these operations may be considered in _every_ (other) [[metric space]], too, see at _[[non-Euclidean geometry]]_. [[Euclidean geometry]] is distinguished notably from [[elliptic geometry]] or [[hyperbolic geometry]] by the fact that it satisfies the [[parallel postulate]].

In regarding $E^n = (\mathbb{R}^n, d_{Eucl})$ (only) as a [[metric space]], some [[extra structure]] still carried by $\mathbb{R}^n$ is disregarded, such as its [[vector space]] structure, hence its [[affine structure]] and its canonical [[inner product space]] structure. Sometimes "Euclidean space" is 
used to refer to $E^n$ with that further extra structure remembered, which might then be called _[[Cartesian space]]_.

Retaining the [[inner product]] on top of the [[metric space]] structure means that on top of [[distances]] one may also speak of [[angles]] in a Euclidean space.

Then of course $\mathbb{R}^n$ carries also non-canonical [[inner product space]] structures, not corresponding to the [[Euclidean norm]]. Regarding $E^n$ as equipped with these one says that it is a  __pseudo-Euclidean space__. These are now, again in the sense of [[Cartan geometry]], the local model spaces for [[pseudo-Riemannian geometry]]. 

Finally one could generalize and allow the [[dimension]] to be countably infinite, and regard separable [[Hilbert spaces]] as generalized Eclidean spaces.

## Remarks on terminology

Arguably, the spaces studied by Euclid were not really modelled on inner product spaces, as the distances were lengths, not [[real numbers]] (which, if non-negative, are *ratios* of lengths).  So we should say that $V$ has an inner product valued in some [[orientation|oriented]] [[line]] $L$ (or rather, in $L^2$).  Of course, Euclid did not use the inner product (which takes negative values) directly, but today we can recover it from what Euclid did discuss: lengths (valued in $L$) and angles (dimensionless).

Since the days of [[René Descartes]], it is common to identify a Euclidean space with a [[Cartesian space]], that is $\mathbb{R}^n$ for $n$ the dimension.  But Euclid\'s spaces had no coordinates; and in any case, what we do with them is still coordinate-independent.


## Lengths and angles

Given two points $x$ and $y$ of a Euclidean space $E$, their difference $x - y$ belongs to the vector space $V$, where it has a norm
$$ {\|x - y\|} = \sqrt{\langle{x - y, x - y}\rangle} .$$
This real number (or properly, element of the line $L$) is the __distance__ between $x$ and $y$, or the __length__ of the line segment $\overline{x y}$.  This distance function makes $E$ into an ($L$-valued) [[metric space]].

Given three points $x, y, z$, with $x, y \ne z$ (so that ${\|x - z\|}, {\|y - z\|} \ne 0$), we can form the ratio
$$ \frac{\langle{x - z, y - z}\rangle}{{\|x - z\|} {\|y - z\|}} ,$$
which is a (dimensionless) real number.  By the Cauchy--Schwartz inequality, this number lies between $-1$ and $1$, so it\'s the [[cosine]] of a unique angle measure between $0$ and $\pi$ radians.  This is the measure of the __angle__ $\angle x z y$.  In a $2$-dimensional Euclidean space, we can interpret $\angle x z y$ as a signed angle (so taking values anywhere on the [[unit circle]]) if we fix an [[orientation]] of $E$.

Conversely, knowing angles and lengths, we may recover the inner product on $V$;
$$ \langle{x - z, y - z}\rangle = {\|\overline{x z}\|} {\|\overline{y z}\|} \cos \angle x z y ,$$
and other inner products are recovered by linearity.  (We must then use the axioms of [[Euclidean geometry]] to prove that this is well defined and actually an inner product.)  It's actually possible to recover the inner product and angles from lengths alone; this is discussed at [[Hilbert space]].


## Related concepts

* [[Euclidean G-space]]

* [[super-Euclidean space]]

* [[Euclidean geometry]]

* [[synthetic geometry]]

* [[Euclidean field theory]]

* [[geometric algebra]]

## References

* {#Euclid300BC} [[Euclid]], _[[Elements]]_, 300BC 


[[!redirects Euclidean space]]
[[!redirects Euclidean spaces]]
[[!redirects euclidean space]]
[[!redirects euclidean spaces]]
