
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

>_Dr. von Neumann, ich m&#246;chte gerne wissen, was ist denn eigentlich ein Hilbertscher Raum ?_  [^Hilbert]

[^Hilbert]: _Dr. von Neumann, I would like to know what is a Hilbert space ?_ Question asked by Hilbert in a 1929 talk by v. Neumann in G&#246;ttingen. The anecdote is narrated together with additional information on the introduction of adjoint operators to quantum mechanics by Saunders Mac Lane in _Concepts and Categories_ ([link](http://www.ams.org/samplings/math-history/hmath1-maclane25.pdf), p.330). Note, that we have corrected 'dann' in the original quotation to the more likely 'denn'.

A _Hilbert space_ is a (possibly) infinite-dimensional generalisation of the traditional spaces of Euclidean geometry in which the notions of distance and angle still make good sense.  This is done through an algebraic operation, the _inner product_, that generalises the dot product.

Hilbert spaces were made famous to the world at large through their applications to [[physics]], where they organise the pure states of quantum systems.

Hilbert spaces form a category, [[Hilb]].

See also

* [[an elementary treatment of Hilbert spaces]].

## Definitions

Let $V$ be a [[vector space]] over the field of [[complex number]]s.  (One can generalise the choice of [[field]] somewhat.)  An __inner product__ (in the most general, possibly indefinite, sense) on $V$ is a function
$$ \langle {-},{-} \rangle: V \times V \to \mathbb{C} $$
that is (1--3) _sesquilinear_ and (4) _conjugate-symmetric_; that is:

1.  $ \langle 0, x \rangle = 0 $ and $ \langle x, 0 \rangle = 0 $;
1.  $ \langle x + y, z \rangle = \langle x, z \rangle + \langle y, z \rangle $ and $ \langle x, y + z \rangle = \langle x, y \rangle + \langle x, z \rangle $;
1.  $ \langle c x, y \rangle = \bar{c} \langle x, y \rangle $ and $ \langle x, c y \rangle = c \langle x, y \rangle $;
1.  $ \langle x, y \rangle = \overline{\langle y, x \rangle} $.

Here we use the _physicist\'s convention_ that the inner product is conjugate-linear in the first variable rather than in the second, rather than the _mathematician\'s convention_, which is the reverse.  The physicist\'s convention fits in a little better with $2$-[[2-Hilbert space|Hilbert space]]s.  Note that we use the same field as values of the inner product as for [[scalars]]; the complex conjugation will be irrelevant for some choices of field.

The axiom list above is rather redundant.  First of all, (1) follows from (3) by setting $c = 0$; besides that, (1--3) come in pairs, only one of which is needed, since each half follows from the other using (4).  It is even possible to derive (3) from (2) by supposing that $V$ is a [[topological vector space]] and that the inner product is continuous (which, as we will see, is always true anyway for a Hilbert space).

The next concept to define is (semi)definiteness.  We define a function $\|{-}\|^2: V \to \mathbb{C}$ by $\|x\|^2 = \langle x, x \rangle$; in fact, $\|{-}\|^2$ takes only real values, by (4).
*  The inner product is __positive semidefinite__, or simply __positive__, if $\|x\|^2 \geq 0$ always.
*  Notice that (by 1), $\|x\|^2 = 0$ if $x = 0$; the inner product is __definite__ if the converse holds.
*  An inner product is __positive definite__ if it is both positive and definite.
*  As an aside, there are also _negative (semi)definite_ inner products, which are slightly less convenient but not really different.  An inner product is _indefinite_ if some $\|x\|^2$ are positive and some are negative; these have a very different flavour.

The inner product is __complete__ if, given any infinite [[sequence]] $(v_1, v_2, \ldots)$ such that
\[ \label{Cauchy} \lim_{m,n\to\infty} \left\|\sum_{i=m}^{m+n} v_i\right\|^2 = 0 ,\]
there exists a (necessarily unique) **sum** $S$ such that
\[ \label{converge} \lim_{n\to\infty} \left\|S - \sum_{i=1}^n v_i\right\|^2 = 0 .\]
If the inner product is definite, then this sum, if it exists, must be unique, and we write
$$ S = \sum_{i=1}^\infty v_i $$
(with the right-hand side undefined if no such sum exists).

Then a __Hilbert space__ is simply a vector space equipped with a complete positive definite inner product.


### Hilbert spaces as Banach spaces

If an inner product is positive, then we can take the principal square root of $\|x\|^2 = \langle x, x \rangle$ to get the a real number $\|x\|$, the __norm__ of $x$.

This norm satisfies all of the requirements of a [[Banach space]].  It additionally satisfies the _parallelogram law_
$$ \|x + y\|^2 + \|x - y\|^2 = 2 \|x\|^2 + 2 \|y\|^2 ,$$
which not all Banach spaces need satisfy.  (The name of this law comes from its geometric interpretation: the norms in the left-hand side are the lengths of the diagonals of a parallelogram, while the norms in the right-hand side are the lengths of the sides.)

Furthermore, any Banach space satsifying the parallelogram law has a unique inner product that reproduces the norm, defined by
$$ \langle x, y \rangle = \frac{1}{4}\left(\|x + y\|^2 - \|x - y\|^2 - \mathrm{i} \|x + \mathrm{i}y\|^2 + \mathrm{i} \|x - \mathrm{i}y\|^2\right) ,$$
or $\frac{1}{2}(\|x + y\|^2 - \|x - y\|^2)$ in the real case.

Therefore, it is possible to *define* a Hilbert space as a Banach space that satisfies the parallelogram law.  This actually works a bit more generally; a positive semidefinite inner product space is a pseudonormed vector space that satisfies the parallelogram law.  (We cannot, however, recover an indefinite inner product from a norm.)


### Hilbert spaces as metric spaces

In any positive semidefinite inner product space, let the __distance__ $d(x,y)$ be
$$ d(x,y) = \|y - x\| .$$
Then $d$ is a [[pseudometric]]; it is a complete metric if and only if we have a Hilbert space.

In fact, the axioms of a [[Banach space]] (or pseudonormed vector space) can be written entirely in terms of the metric; we can also state the parallelogram law as follows:
$$ d(x,y)^2 + d(x,-y)^2 = 2 d(x,0)^2 + 2 d(x,x+y)^2 .$$

In definitions, it is probably most common to see the metric introduced only to state the completeness requirement.  Indeed, (eq:Cauchy) says that the sequence of partial sums is a [[Cauchy sequence]], while (eq:converge) says that the sequence of partial sums converges to $S$.


### Hilbert spaces as conformal spaces

Given two vectors $x$ and $y$, both nonzero, let the __angle__ between them be the angle $\theta(x,y)$ whose cosine is
$$ \cos \theta(x,y) = \frac { \langle x, y \rangle } { \|x\| \|y\| } .$$
(Note that this angle may be imaginary in general, but not for a Hilbert space over $\mathbb{R}$.)

A Hilbert space cannot be reconstructed entirely from its angles, however (even given the underlying vector space).  The inner product can only be recovered up to a positive scale factor.

### Morphisms of Hilbert spaces

See discussion at [[Banach space]].  There is more to be said here concerning duals (including why the theory of Hilbert spaces is slightly nicer over $\mathbb{C}$ while that of Banach spaces is slightly nicer over $\mathbb{R}$).


## Examples

### Banach spaces

All of the $p$-parametrised examples at [[Banach space]] apply if you take $p = 2$.

In particular, the $n$-dimensional [[vector space]] $\mathbb{C}^n$ is a complex Hilbert space with
$$ \langle x, y \rangle = \sum_{u=1}^n \bar{x}_u y_u .$$
Any subfield $K$ of $\mathbb{C}$ gives a positive definite inner product space $K^n$ whose completion is either $\mathbb{R}^n$ or $\mathbb{C}^n$.  In particular, the [[cartesian space]] $\mathbb{R}^n$ is a real Hilbert space; the geometric notions of distance and angle defined above agree with ordinary [[Euclidean space|Euclidean geometry]] for this example.

### Of Lebesgue square-integrable functions over a manifold

The [[L-2-spaces|L-]] Hilbert spaces $L^2(\mathbb{R})$, $L^2([0,1])$, $L^2(\mathbb{R}^3)$, etc (real or complex) are very well known.  In general, $L^2(X)$ for $X$ a [[measure space]] consists of the almost-everywhere defined functions $f$ from $X$ to the scalar field ($\mathbb{R}$ or $\mathbb{C}$) such that $ \int |f|^2 $ converges to a finite number, with functions identified if they are equal almost everywhere; we have $\langle f, g\rangle = \int \bar{f} g$, which converges by the Cauchy--Schwarz inequality.  In the specific cases listed (and in general, when $X$ is a [[locally compact space|locally compact]] [[Hausdorff space]]), we can also get this space by completing the positive definite inner product space of compactly supported continuous functions.

### Of square-integrable half-densities

* [[canonical Hilbert space of half-densities]]

## Properties

### Bases

A basic result is that abstractly, Hilbert spaces are all of the same type: every Hilbert space $H$ admits an orthonormal basis, meaning a [[subset]] $S \subseteq H$ whose inclusion map extends (necessarily uniquely) to an isomorphism
$$l^2(S) \to H$$
of Hilbert spaces. Here $l^2(S)$ is the vector space consisting of those [[function]]s $x$ from $S$ to the scalar field such that
$$ \|x\|^2 = \sum_{u: S} |x_u|^2 $$
converges to a finite number; this may also be obtained by completing the vector space of formal linear combinations of elements of $S$ with an inner product uniquely determined by the rule
$$\langle u, v \rangle = \delta_{u v} \qquad u, v \in S$$
in which $\delta_{u v}$ denotes [[Kronecker delta]]. We thus have, in $l^2(S)$,
$$ \langle x, y \rangle = \sum_{u: S} \bar{x}_u y_u .$$
(This sum converges by the Cauchy--Schwarz inequality.)

In general, this result uses the [[axiom of choice]] (usually in the form of [[Zorn's lemma]] and [[excluded middle]]) in its proof, and is equivalent to it.  However, the result for [[separable space|separable]] Hilbert spaces needs only [[dependent choice]] and so is [[constructive mathematics|constructive]] by most schools\' standards.  Even without dependent choice, explicit orthornormal bases for particular $L^2(X)$ can often be produced using [[approximation of the identity]] techniques, often in concert with a [[Gram-Schmidt process]].

In particular, all infinite-dimensional separable Hilbert spaces are abstractly isomorphic to $l^2(\mathbb{N})$.



### Cauchy--Schwarz inequality

The _Schwarz inequality_ (or _Cauchy--&#1041;&#1091;&#1085;&#1103;&#1082;&#1086;&#1074;&#1089;&#1082;&#1080;&#1081;--Schwarz inequality_, etc) is very handy:
$$ |\langle x, y \rangle| \leq \|x\| \|y\| .$$


This is really two theorems (at least): an abstract theorem that the inequality holds in any Hilbert space, and concrete theorems that it holds when the inner product and norm are defined by the formulas used in the examples $L^2(X)$ and $l^2(S)$ above.  The concrete theorems apply even to functions that don\'t belong to the Hilbert space and so prove that the inner product converges whenever the norms converge.  (A somewhat stronger result is needed to conclude this convergence constructively; it may be found in Errett Bishop\'s book.)


## Related concepts

* [[rigged Hilbert space]]

* [[Hilbert C-star-module]], [[Hilbert bimodule]]

* [[Kähler vector space]]

## References

Standard accounts of Hilbert spaces in [[quantum mechanics]] include

* [[John von Neumann]], _Mathematische Grundlagen der Quantenmechanik_.
(German) Mathematical Foundations of Quantum Mechanics. Berlin,
Germany: Springer Verlag, 1932.

* [[George Mackey]], _The Mathematical Foundations of Quamtum Mechanics_ A
Lecture-note Volume, ser. The mathematical physics monograph series.
Princeton university, 1963

* E. Prugove&#265;ki, _Quantum mechanics in Hilbert Space_. Academic Press,
1971.


category: analysis

[[!redirects Hilbert spaces]]
[[!redirects category of Hilbert spaces]]
[[!redirects categories of Hilbert spaces]]
