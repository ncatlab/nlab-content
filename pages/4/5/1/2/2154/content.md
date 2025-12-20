

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

In regarding $E^n = (\mathbb{R}^n, d_{Eucl})$ (only) as a [[metric space]], some [[extra structure]] still carried by $\mathbb{R}^n$ is disregarded, such as its [[vector space]] structure, hence its [[affine space]] structure and its canonical [[inner product space]] structure. Sometimes "Euclidean space" is 
used to refer to $E^n$ with that further extra structure remembered, which might then be called _[[Cartesian space]]_.

Retaining the [[inner product]] on top of the [[metric space]] structure means that on top of [[distances]] one may also speak of [[angles]] in a Euclidean space.

Then of course $\mathbb{R}^n$ carries also non-canonical [[inner product space]] structures, not corresponding to the [[Euclidean norm]]. Regarding $E^n$ as equipped with these one says that it is a  __pseudo-Euclidean space__. These are now, again in the sense of [[Cartan geometry]], the local model spaces for [[pseudo-Riemannian geometry]]. 

Finally one could generalize and allow the [[dimension]] to be countably infinite, and regard separable [[Hilbert spaces]] as generalized Euclidean spaces.

## Remarks on terminology

Arguably, the spaces studied by Euclid were not really modelled on inner product spaces, as the distances were lengths, not [[real numbers]] (which, if non-negative, are *ratios* of lengths).  So we should say that $V$ has an inner product valued in some [[orientation|oriented]] [[line]] $L$ (or rather, in $L^2$).  Of course, Euclid did not use the inner product (which takes negative values) directly, but today we can recover it from what Euclid did discuss: lengths (valued in $L$) and angles (dimensionless).

Since the days of [[René Descartes]], it is common to identify a Euclidean space with a [[Cartesian space]], that is $\mathbb{R}^n$ for $n$ the dimension.  But Euclid\'s spaces had no coordinates; and in any case, what we do with them is still coordinate-independent.

## Euclidean spaces with infinitesimals

Instead of working in the real numbers $\mathbb{R}$ and $n$-[[dimension|dimensional]] real vector spaces $V$, one could instead work in a [[Archimedean ordered Artinian local ring|Archimedean ordered Artinian local $\mathbb{R}$-algebra]] $A$ and [[rank]] $n$ $A$-modules $V$. $A$ has [[infinitesimals]], and so the $A$-modules $V$ have [[infinitesimals]] as well. Nevertheless, it is still possible to define the Euclidean distance function on $V$; the only difference is that the distance function is a [[pseudometric]] rather than a [[metric]] here. 

Since $A$ is an [[local ring]], the quotient of $A$ by its [[ideal]] of non-invertible elements $I$ is $\mathbb{R}$ itself, and the canonical function used in defining the [[quotient ring]] is the function $\Re:A \to \mathbb{R}$ which takes a number $a \in A$ to its purely real component $\Re(a) \in \mathbb{R}$. Since $A$ is an ordered $\mathbb{R}$-algebra, there is a [[strictly monotone]] [[ring homomorphism]] $h:\mathbb{R} \to A$. 

The real numbers have [[lattice]] structure $\min:\mathbb{R} \times \mathbb{R} \to \mathbb{R}$ and $\max:\mathbb{R} \times \mathbb{R} \to \mathbb{R}$. This means that $A$ has a distance function given by the function $\rho:A \times A \to \mathbb{R}$, defined as 

$$\rho(a, b) \coloneqq \max(\Re(a), \Re(b)) - \min(\Re(a), \Re(b))$$

as well as an [[absolute value]] given by the function $\vert-\vert:A \to \mathbb{R}$, defined as 

$$\vert a \vert \coloneqq \rho(a, 0)$$

Since $\min(a, b) \leq \max(a, b)$, the [[pseudometric]] and multiplicative [[seminorm]] are always non-negative. In addition, by definition, the pseudometric takes any two elements $a \in A$ and $b \in A$ whose difference $a - b \in I$ is an infinitesimal to zero $\rho(a, b) = 0$. 

Since $\mathbb{R}$ is an [[Euclidean field]], it has a [[metric square root function]] $\sqrt{-}:[0, \infty) \to [0, \infty)$. Every [[rank]] $n$ $A$-module $V$ with basis $v:\mathrm{Fin}(n) \to V$ thus has a **Euclidean pseudometric** $\rho_V:V \times V \to K$ defined by 

$$\rho_V(a, b) \coloneqq \sqrt{\sum_{i \in \mathrm{Fin}(n)} \rho(a_i, b_i)^2}$$
for module elements $a \in V$ and $b \in V$ and scalars $a_i \in A$ and $b_i \in A$ for index $i \in \mathrm{Fin}(n)$, where
$$a = \sum_{i \in \mathrm{Fin}(n)} a_i v_i \quad b = \sum_{i \in \mathrm{Fin}(n)} b_i v_i$$

If $A$ is an [[ordered field]], then this reduces down to the Euclidean metric defined above. 

## In constructive mathematics

In [[constructive mathematics]], the [[real numbers]] used to define Euclidean spaces are the [[Dedekind real numbers]] $\mathbb{R}_{D}$, as those are the only ones that are [[Dedekind complete]], in the sense of not having any gaps in the [[dense linear order]]. The Dedekind real numbers are also the real numbers that are geometrically contractible: whose [[shape]] is [[homotopy theory|homotopically]] [[contractible]] $\esh(\mathbb{R}_D) \cong \mathbb{1}$. 

### In predicative constructive mathematics

In [[predicative mathematics|predicative]] constructive mathematics, the [[Dedekind real numbers]] are defined relative to a universe $\mathcal{U}$, and thus there are many different such Dedekind real numbers that could be used to define Euclidean spaces, one $\mathbb{R}_\mathcal{U}$ for each $\mathcal{U}$. However, each set of Dedekind real numbers $\mathbb{R}_\mathcal{U}$ would be large relative to the sets in the universe $\mathcal{U}$. 

If the predicative constructive foundations does not have universes, then there doesn't exist any [[dense linear order]] that is actually [[Dedekind complete]] in the usual sense, and so the usual definition of Euclidean space does not work. Some mathematicians have proposed to use [[Sierpinski space]]  $\Sigma$, the [[initial object|initial]] [[sigma-frame|$\sigma$-frame]], for defining the real numbers, in place of the large set of all [[propositions]] in a universe $\mathrm{Prop}_\mathcal{U}$, but the real numbers in that case are only [[sigma Dedekind complete|$\Sigma$-Dedekind complete]], which is a weaker condition than being [[Dedekind complete]]. Furthermore, Lešnik showed that for any two $\sigma$-frames $\Sigma$ and $\Sigma^{'}$ that embed into $\mathrm{Prop}_\mathcal{U}$ such that $\Sigma \subseteq \Sigma^{'}$, if $A$ is the $\Sigma$-Dedekind completion of $\mathbb{Q}$ and $B$ is the $\Sigma^{'}$-Dedekind completion of $\mathbb{Q}$, then $A \subseteq B$, so the $\Sigma$-Dedekind real numbers are not complete. 

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

* [[Cartesian space]]

* [[Euclidean field]]

* [[Euclidean G-space]]

* [[super-Euclidean space]]

* [[Euclidean geometry]]

* [[synthetic geometry]]

* [[Euclidean field theory]]

* [[geometric algebra]]

## References

* {#Euclid300BC} [[Euclid]], _[[Elements]]_, 300BC 

Textbook accounts:

* [[Igor R. Shafarevich]], [[Alexey O. Remizov]]: §7 in: *Linear Algebra and Geometry* (2012) &lbrack;[doi:10.1007/978-3-642-30994-6](https://doi.org/10.1007/978-3-642-30994-6), [MAA-review](https://maa.org/press/maa-reviews/linear-algebra-and-geometry)&rbrack; 

On the [[piecewise-linear manifold]] [[structure]] and the [[smooth manifold]] [[structure]] of finite-dimensional Euclidean spaces:

* [[John Stallings]]: *The Piecewise-Linear Structure of Euclidean Space*, Mathematical Proceedings of the Cambridge Philosophical Society **58** 3 (1962) 481--488 &lbrack;[doi:10.1017/S0305004100036756](https://doi.org/10.1017/S0305004100036756), [pdf](https://www.maths.gla.ac.uk/~mpowell/stallings-structures-of-euclidean-space.pdf)&rbrack;

On the use of the [[Dedekind real numbers]] in constructive and predicative constructive mathematics, such as for Euclidean spaces:

* [[Univalent Foundations Project]], [[Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

* [[Mike Shulman]], Brouwer’s fixed-point theorem in real-cohesive homotopy type theory, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

* Davorin Lešnik, Synthetic Topology and Constructive Metric Spaces, ([arxiv:2104.10399](https://arxiv.org/abs/2104.10399))

[[!redirects Euclidean space]]
[[!redirects Euclidean spaces]]
[[!redirects euclidean space]]
[[!redirects euclidean spaces]]

[[!redirects Euclidean metric]]
[[!redirects Euclidean metrics]]
[[!redirects euclidean metric]]
[[!redirects euclidean metrics]]

[[!redirects Euclidean pseudometric]]
[[!redirects Euclidean pseudometrics]]
[[!redirects euclidean pseudometric]]
[[!redirects euclidean pseudometrics]]