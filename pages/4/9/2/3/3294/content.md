
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Fr&#233;chet spaces
* table of contents
{: toc}

## Idea

Fr&#233;chet spaces are particularly well-behaved [[topological vector spaces]] (TVSes).  Every [[Cartesian space]] is a Fr&#233;chet space, but Fr&#233;chet spaces may have infinite [[dimension]].  There is [[analysis]] on Fr&#233;chet spaces, yet they are more general than [[Banach spaces]]; as such, they are popular as test spaces for possibly [[infinite-dimensional manifolds]]: _[[Fréchet manifolds]]_.

Beware the clash ofterminology: a 'Fr&#233;chet topology' on a 'Fr&#233;chet topological space' is something different; this just means that a [[topological space]] satisfies the $T_1$ [[separation axiom]].  (Like all Hausdorff TVSes, Fr&#233;chet spaces satisfy this axiom, but they have a good deal of additional structure and properties.)

A basic example of a Fr&#233;chet space is $\mathbb{R}^\infty = \underset{\longleftarrow}{\lim} \mathbb{R}^n$, as a [[topological space]] the _[[projective limit]]_ over the finite dimensional [[Cartesian spaces]] $\mathbb{R}^n$ (example \ref{ProjRInfinity} below) . This is not a [[Banach space]] anymore, since it does not carry a compatible [[norm]] anymore (e.g. [Saunders 89](#Saunders89), p. 253). But it evidently does carry the functions $\mathbb{R}^\infty \overset{p^n}{\longrightarrow} \mathbb{R}^n \overset{\Vert -\Vert_n}{\longrightarrow} \mathbb{R}$ for all $n \in \mathbb{N}$, where $p^n$ is the defining [[projection]] and where ${\Vert -\Vert}_n$ is the standard [[norm]] on $\mathbb{R}^n$. While not norms, these composites are [[seminorms]] on $\mathbb{R}^\infty$, they only fail the condition that only the 0-vector has vanishing norm. A Fr&#233;chet space is equivalently a vector space equipped with a countable familiy of seminorms, with compatibility conditions modeled on this example. See def. \ref{FrechetSpaceAsCompleteTVSWithCompatibleSeminorms} below.


## Definition

There are various equivalent definitions of Fr&#233;chet spaces:

+-- {: .num_defn #FrechetSpaceAsMetisableCompleteTVS}
###### Definition

A __Fr&#233;chet space__ is equivalently a [[complete space|complete]] [[Hausdorff space|Hausdorff]] [[locally convex vector space]] that is [[metric space|metrisable]].  The metric can be chosen to be translation-invariant.

=--

+-- {: .num_defn #FrechetSpaceAsCompleteTVSWithCompatibleSeminorms}
###### Definition

A **Fr&#233;chet space** is a [[complete space|complete]] [[Hausdorff space|Hausdorff]] [[topological vector space]] $V$ whose topology may be given (as a [[gauge space]]) by a [[countable set|countable]] family of [[seminormed vector space|seminorms]], hence for which there exists a family of [[seminorms]]

$$
  {\Vert - \Vert}_n \;\colon\; V \longrightarrow \mathbb{R}
  \;\;\;
   \,,n \in \mathbb{N}
$$

such that the set of all [[open balls]] of the form

$$
  B_\epsilon^{(n)}(x)
  \coloneqq
  \left\{
    y \in V \,\vert\,  {\Vert x-y \Vert}_n \lt \epsilon
  \right\}
  \;\;\;\;\;\;\;\;
  for
  \;
  x \in V\,, \epsilon \gt 0 \,, n \in \mathbb{N}
$$

is a [[base of neighborhoods]] of $x$. 
=--

+-- {: .num_defn }
###### Definition

We accept as an [[automorphism]] of Fr&#233;chet spaces any [[linear map|linear]] [[homeomorphism]]; in particular, the particular translation-invariant metric or countable family of [[seminorms]] used to prove that a space is a Fr&#233;chet space is *not* required to be preserved.  More generally, the [[morphisms]] of Fr&#233;chet spaces are the [[continuous map|continuous]] linear maps, so that Fr&#233;chet spaces form a [[full subcategory]] of the category $TVS$ of [[topological vector spaces]].

=--

## Examples

+-- {: .num_example }
###### Example

Every [[Banach space]] is a Fr&#233;chet space.

=--

+-- {: .num_example }
###### Example

If $X$ is a [[compact space|compact]] [[smooth manifold]], then the space of [[smooth map|smooth maps]] on $X$ is a Fr&#233;chet space.  This can be extended to some non-compact manifolds, in particular when $X$ is the [[real line]].

=--

+-- {: .num_example }
###### Example

The [[Lebesgue space]] $L^p(\mathbb{R})$ for $p \lt 1$ is *not* a Fr&#233;chet space, because it is not locally convex.

=--


+-- {: .num_example #ProjRInfinity}
###### Example

Consider the [[direct product]] (as [[topological vector spaces]]) of a countable number of copies of the [[real line]] $\mathbb{R}$ 

Equivalently the [[projective limit]] (as [[topological vector spaces]])

$$
  \mathbb{R}^\infty 
    \coloneqq
  \underset{\longleftarrow}{\lim}_n \mathbb{R}^n
  =
  \underset{\longleftarrow}{\lim}
  \left(
    \cdots \to \mathbb{R}^2 \overset{}{\to} \mathbb{R}^1 \to \mathbb{R}^0
  \right)
$$

over all [[Cartesian spaces]] via their canonical [[projection maps]].

(Beware that the same symbol "$\mathbb{R}^\infty$" is also used for the limit of
the same sequence but with $\mathbb{R}^n$ with discrete topology, what leads to a [[linearly compact vector space]] as well as for the [[direct sum]]/[[inductive limit]] of $\mathbb{R}\to \mathbb{R}\hookrightarrow\mathbb{R{^3\hookrightarrow\ldots$, which is different.)

Write

$$
  \pi_n \colon \mathbb{R}^\infty \longrightarrow \mathbb{R}^n
$$ 

for the induced [[projection]] maps onto the first $n$ copies and let $\|\cdot\|_n$ be the canonical [[norm]] on $\mathbb{R}^n$.  

Then a compatible countable family of seminorms on $\mathbb{R}^\infty$, according to def. \ref{FrechetSpaceAsCompleteTVSWithCompatibleSeminorms}, is given by $v \mapsto {\Vert\pi_n(v) \Vert_n}$. Hence equipped with these, $\mathbb{R}^\infty$ becomes a Fr&#233;chet space.


=--

On the other hand, the locally convex direct sum of a countable number of copies of $\mathbb{R}$ is not a Fr&#233;chet space.





## Properties

### General

Fr&#233;chet spaces are [[barrelled]] and [[bornological]]. 

### Duals

The dual of a Fr&#233;chet space $F$ is a Fr&#233;chet space iff $F$ is a [[Banach space]].

This follows from the statement paragraph 29.1 (7) in ([Koethe](#Koethe)), which is: The strong dual of a locally convex metrizable TVS $F$ is metrizable iff $F$ is normable.

See also ([Saunders 89, p. 255](#Saunders89)).

### As projective limits
 {#AsProjectiveLimits}

Every *[[complete topological space|complete]]* [[locally convex topological vector space]] $X$ is the [[cofiltered category|cofiltered]] [[projective limit]] of [[Banach spaces]] in the [[category]] of [[locally convex spaces]].

To see this, choose a base $\{U_{\alpha}\}_{\alpha \in A}$ of the neighborhood filter of $0$, consisting of convex, balanced and absorbing sets and let $p_{\alpha}$ be Minkowski functional associated to $U_{\alpha}$. The Hausdorffification $X_{\alpha}$ of $(X, p_{\alpha})$ is easily seen to be a Banach space and because $A$ is directed by reverse inclusion so is $X_{\alpha}$. It is straightforward to check that $X = \underset{\longleftarrow}{\lim} X_{\alpha}$ in the category of locally convex spaces. For details, see ([Schaefer-Wolff 99, Chapter&#160;II.&#167;5](#SchaeferWolff99),  [page&#160;51ff](http://books.google.com/books?id=9kXY742pABoC&pg=PA51).

Now given that a Fr&#233;chet space admits a *decreasing sequence* of convex balanced and absorbing neighborhoods, it follows immediately that:

Every Fr&#233;chet space is a [[sequential limit|sequential]] [[projective limit]] of [[Banach spaces]]. 

Conversely, any limit of a sequence of Banach spaces is a Fr&#233;chet space.

See ([Schaefer-Wolff 99](#SchaeferWolff99)), Chapter II.&#167;4, page 48f (as well as Theorem I.6.1, page 28). 

(from [this MO comment](http://math.stackexchange.com/a/53020/58526))

See also example \ref{ProjRInfinity} below.

## Differentiable and smooth functions
 {#DifferentiableAndSmoothFunctions}

It is possible to generalize some aspects of [[analysis]] (differential calculus) to Fr&#233;chet spaces (e.g. [Michor 80, chapter 8](#Michor80), [Saunders 89, p. 256](#Saunders89)). 

For example the definition of the [[derivative]] of a curve is simply the same as in finite dimensions:


+-- {: .num_defn}
###### Definition
For a continuous path in a Fr&#233;chet space $f(t)$ we define
$$
f'(t) = \lim_{h \to 0} \frac{1}{h} (f(t + h) - f(t))
$$
If the limit exists and is continuous, we say that $f$ is continuously differentiably or $C^1$.
=--

And just as in the finite dimensional case, we can define the partial derivative, or rather: the [[directional derivative|directional]] or G&#226;teaux derivative:

+-- {: .num_defn}
###### Definition
**directional derivative**

Let F and G be Fr&#233;chet spaces, $U \subseteq F$ open and $P: U \to G$ a nonlinear continuous map. The derivative of $P$ at the point $f \in U$ in the direction $h \in F$ is the map
$$
D P: U \times F \to G
$$
$$
D P(f) h = \lim_{t \to 0} \frac{1}{t} ( P(f + t h) - P(f))
$$
If the limit exists and is jointly continuous in both variables we say that $P$ is continuous differentiable or $C^1$.
=--

A simple, but nontrivial example is the operator 
$$
P: C^{\infty}[a, b] \to C^{\infty}[a, b]
$$
$$
P(f) \coloneqq f f'
$$
with the derivative
$$
D P(f) h = f'h + f h'
$$

It is possible to generalize the Riemann integral to Fr&#233;chet spaces, too: For a continuous path $f(t)$ on an interval $[a, b]$ in a Fr&#233;chet space $F$ we look for an element $\int_a^b f(t) d t \in F$. It turns out that such an element exists and is unique, if we impose some properties of the integral known from the finite dimensional case:


+-- {: num_theorem}
###### Theorem
There exists a unique element $\int_a^b f(t) d t \in F$ such that

(i) for every continuous functional $\phi$ we have  $\phi(\int_a^b f(t) d t) = \int_a^b \phi(f(t)) d t$,

(ii) for every continuous seminorm ${\| \cdot \|}$ we have ${\| \int_a^b f(t) d t \|} \leq \int_a^b {\| f(t) \|} d t$

(iii) integration is linear and 

(iv) additive, i.e. $ \int_a^b f(t) d t + \int_b^c f(t) d t = \int_a^c f(t) d t $

=--

There is a version of the fundamental theorem of calculus:


+-- {: .num_theorem}
###### Theorem
If P is $C^1$ and $f + t h \in Domain(P)$ for $0 \leq t \leq 1$, then 
$$
P(f + h) - P(f) = \int_0^1 D P(f + t h) \;h \; d t
$$

=--

The [[chain rule]] is valid:

+-- {: .num_theorem}
###### Theorem
If P and Q are $C^1$ then so is their composition $Q \circ P$ and
$$
D [Q \circ P](f) h = D Q(P(f)) \; D P(f) \; h
$$
=--

The first derivative $D P$ is a function of two variables, the base point $f$ and the direction $h$. Since $D P$ is already linear in $h$, we define the second derivative with respect to $f$ only:

+-- {: .num_defn}
###### Definition
**second derivative**
The second derivative of $P$ in the direction $k$ is defined to be
$$
D^2 P(f) (h, k) = \lim_{t \to 0} \frac{1}{t} (D P(f + t k) h - D P(f) h)
$$
=--

It is a theorem that the second derivative, if it exists and is jointly continuous, is bilinear in $(h ,k)$.

We can iterate this procedure to define derivatives of arbitrary order, and thus the notion of **smooth functions between Fr&#233;chet spaces**. This allows to define the concept of smooth _[[Fréchet manifolds]]_.



## References

* {#Vogt00} [[Dietmar Vogt]], _Lectures on Fr&#233;chet spaces_, 2000 ([pdf](http://www2.math.uni-wuppertal.de/~vogt/vorlesungen/fs.pdf))

* PlanetMath, _[Fr&#233;chet space](http://planetmath.org/frechetspace)_

* Wikipedia, _[Fr&#233;chet space](https://secure.wikimedia.org/wikipedia/en/wiki/Fr&#233;chet_space)_

* {#Koethe} Gottfried Koethe: _Topological Vector Spaces I_

* {#SchaeferWolff99} H. Schaefer, Manfred Wolff *[Topological Vector Spaces](http://books.google.com/books?id=9kXY742pABoC)*, Springer (1999)

Discussion of analysis on Fr&#233;chet spaces includes

* {#Michor80} [[Peter Michor]], chapter 8 of _Manifolds of differentiable mappings_, Shiva Publishing (1980) [pdf](http://www.mat.univie.ac.at/~michor/manifolds_of_differentiable_mappings.pdf)

* Richard S. Hamilton: _The Inverse Function Theorem of Nash and Moser_ (Bulletin (New Series) of the American Mathematical Society Volume 7, Number 1, July 1982)

Discussion in the context of [[jet bundle]] theory includes

* {#Saunders89} [[David Saunders]], chapter 7 of _The geometry of jet bundles_, London Mathematical Society Lecture Note Series __142__, Cambridge Univ. Press 1989.

Refinement to [[noncommutative geometry]] by suitable smoothed [[C-star-algebras]] is discussed in 

* Nikolay Ivankov, _Unbounded bivariant K-theory and an Approach to Noncommutative Fr&#233;chet spaces_ [pdf](http://hss.ulb.uni-bonn.de/2011/2624/2624.pdf)

[[!redirects Frechet space]]
[[!redirects Frechet spaces]]
[[!redirects Fréchet space]]
[[!redirects Fréchet spaces]]