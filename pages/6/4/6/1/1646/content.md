
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
 {#Idea}

> *Dr. von Neumann, ich möchte gerne wissen, was ist denn eigentlich ein Hilbertscher Raum ?*  [^Hilbert]

[^Hilbert]: *Dr. von Neumann, I would like to know what is a Hilbert space?* -- Question asked by [[David Hilbert]], in a 1929 talk by [[John von Neumann]] in Göttingen (cf. [von Neumann 1930, §I](#vonNeumann30)). The anecdote is narrated for instance in [MacLane 1988, §5](#MacLane88).
(We have corrected 'dann' in the original quotation to the more likely 'denn', in either case expressing a certain sense of puzzlement that is not quite captured by the direct English translation.)

A Hilbert space is (see Def. \ref{HilbertSpace} for details):

1. a ([[real vector space|real]] or,  usually, [[complex vector space|complex]]) [[vector space]], possibly of infinite [[dimension of a vector space|dimension]],

1. equipped with a positive definite [[Hermitian form|Hermitian]] [[inner product]], 

2. which, as a [[topological space]], is [[complete metric space|complete]] with respect to the induced [[metric]].

Hilbert spaces are central to [[quantum physics]] and specifically to [[quantum mechanics]], where they serve as [[space of quantum states|spaces of]] [[pure quantum states]]. Here the [[inner product]] encodes the [[probability amplitudes]] for one [[pure state]] to "[[collapse of the wavefunction|collapse]]" to another one under [[quantum measurement|measurement]]. When the space of pure states is of [[finite-dimensional vector space|finite dimension]] (as is the case of interest in [[quantum information theory]]/[[quantum computation]]) then the completeness condition on a Hilbert space is automatic (see Rem. \ref{FiniteDimensionalInnerProductSpaces} below), otherwise it naturally encodes the possibility of an infinite number of [[quantum measurement|measurement]] outcomes.

Hilbert spaces with ([[bounded linear map|bounded]]) [[linear maps]] between them form a ([[dagger category|dagger]]-)[[category]], often denoted *[[Hilb]]* or similar, with the [[dagger-category|dagger]]-structure given by sending [[bounded linear maps]] to their [[adjoint operators]] with respect to the Hermitian inner product. Finite-dimensional Hilbert spaces form a [[dagger-compact category]].

See also:

* [[an elementary treatment of Hilbert spaces]].


## Definition
 {#Definition}

We first state the 

* [standard formulation](#StandardDefinition)

of the definition of Hilbert spaces and then various equivalent 

* [alternative formulations](#AlternativeDefinitions)


### Standard formulation
 {#StandardDefinition}

We first state the definition as such and then recall the ingredients that go into it:

\begin{definition}\label{HilbertSpace}
**(Hilbert space)**
\linebreak

A *Hilbert space* $\big(\mathscr{H}, \langle -,-\rangle\big)$ is 

1. a ([[complex vector space|complex]] or [[real vector space|real]]) [[vector space]] $\mathscr{H}$ (possibly infinite-[[dimension of a vector space|dimensional]]), 

1. equipped with a [[Hermitian form|Hermitian]] [[inner product]] $\langle -,- \rangle$ (Def. \ref{HermitianInnerProduct})

which is

1. complete (Def. \ref{CompleteInnerProduct});

1. positive definite (Def. \ref{DefiniteInnerProduct}).

\end{definition}

\begin{remark}\label{MorphismOfHilbertSpaces}
**(morphisms of Hilbert spaces)**
\linebreak
There are different notions of [[morphisms]] between [[Hilbert spaces]]:

At the very least, a [[morphism]] of [[Hilbert spaces]] is a [[linear map]] between the underlying [[vector spaces]], and this is the default notion usually considered. Notice that such morphisms do not need to respect the [[inner product]]-[[structure]]. Often one restricts to [[bounded linear maps]] or sometimes [[short maps]] (see at *[maps of Banach spaces](Banach+space#morphisms)*) which respect part of the inner product structure.

Instead of being fully respected by maps, the inner product on Hilbert spaces induces the [[dagger-category|dagger]] [[involution]] on their [[hom-spaces]] given by sending any [[bounded linear map]] $A \colon \mathscr{H}_1 \to \mathscr{H}_2$ to its [[Hermitian form|Hermitian]] [[adjoint operator]] $A^\dagger \colon \mathscr{H}_2 \to \mathscr{H}_1$, characterized by

\[
  \label{AdjointnessRelation}
  \langle A^\dagger(-), -\rangle_{1}
  \;=\;
  \langle -, A(-)\rangle_{2}
\]

\end{remark}


\begin{remark}\label{FiniteDimensionalInnerProductSpaces}
**([[finite-dimensional Hilbert space]])**
\linebreak
  In the case that the underlying vector space $\mathscr{H}$ happens to be [[finite dimensional vector space]], any hermitian inner product is necessarily complete. Therefore: 

A *finite-dimensional Hilbert space* is equivalently a positive-definite [[hermitian inner product]]-space of [[finite set|finite]] [[dimension of a vector space|dimension]].

Finite-dimensional Hilbert spaces form a [[dagger-compact category]] and play a central role in [[quantum information theory]] and [[quantum computation]], see also at *[[quantum information theory via dagger-compact categories]]*.
\end{remark}

\linebreak

We recall now the meaning of the concepts entering Def. \ref{HilbertSpace}. In the following, let $\mathcal{H}$ be a [[vector space]] over the [[ground field]] $\mathbb{C}$ of [[complex numbers]]. For $z \in \mathbb{C}$ a [[complex number]], we write $\overline{z}$ for its [[complex conjugate]].


\begin{remark}\label{AlternativeGroundFields}
**(alternative ground fields)**
\linebreak
The following applies verbatim also for the ground field of [[real numbers]] $\mathbb{R}$, in which case the sesquilinear inner product [below](#HermitianInnerProduct) becomes [[bilinear form|bilinear]] and one speaks of *real Hilbert spaces*. Under mild assumptions, $\mathbb{C}$ and $\mathbb{R}$ are the only possible [[ground fields]] for Hilbert spaces (see [MO:a/4184099](https://math.stackexchange.com/a/4184099/58526)).
\end{remark}


\begin{definition}\label{HermitianInnerProduct}
**(Hermitian inner product)**
\linebreak
A *[[Hermitian form|Hermitian]] [[inner product]]* on $\mathscr{H}$ is a function

$$ 
  \langle {-},{-} \rangle
  \;\colon\; 
  \mathscr{H} \times \mathscr{H} \to \mathbb{C} 
$$

that is

1. **sesquilinear**:

   1. $ \langle 0, x \rangle = 0 $ and $ \langle x, 0 \rangle = 0 $;

   1.  $ \langle x + y, z \rangle = \langle x, z \rangle + \langle y, z \rangle $ and $ \langle x, y + z \rangle = \langle x, y \rangle + \langle x, z \rangle $;

   1.  $ \langle c x, y \rangle = \bar{c} \langle x, y \rangle $ and $ \langle x, c y \rangle = c \langle x, y \rangle $;

1. **conjugate-symmetric**:

   \[
     \label{ConjugateSymmetryOfInnerProduct}
     \langle x, y \rangle = \overline{\langle y, x \rangle} 
   \]


\end{definition}

\begin{remark}\label{ConventionsForInnerProduct}
**(convention for the inner product)**
\linebreak
Def. \ref{HermitianInnerProduct} uses the _physicist\'s convention_ that the inner product is conjugate-linear in the first variable rather than in the second, instead of the _mathematician\'s convention_, which is the reverse.  The physicist\'s convention fits in a little better with $2$-[[2-Hilbert space|Hilbert spaces]]. 
\end{remark}

\begin{remark}
The axiom list in Def. \ref{HermitianInnerProduct} is rather redundant.  First of all, (1.1) follows from (1.3) by setting $c = 0$; besides that, (1.1--1.3) come in pairs, only one of which is needed, since each half follows from the other using (2).  It is even possible to derive (1.3) from (1.2) by supposing that $V$ is a [[topological vector space]] and that the inner product is [[continuous function|continuous]] (which, as we will see, is always true anyway for a Hilbert space).
\end{remark}

\begin{definition}\label{DefiniteInnerProduct}
**(definite inner product)**
\linebreak
Given an inner product according to Def. \ref{HermitianInnerProduct}, consider the (norm square)
function 

\[
  \label{NormSquare}
  \array{
    \mathllap{
    \|{-}\|^2 
    \;\colon\;
    }
    \mathscr{H} &\longrightarrow& 
    \mathbb{R}
    \hookrightarrow
    \mathbb{C}
    \\
    v &\mapsto&
    \langle v, v \rangle
  }
\]

Notice that this takes only real values, by (eq:ConjugateSymmetryOfInnerProduct).

The [[Hermitian form|Hermitian]] [[inner product]] is called:

* **positive semidefinite**, or simply **positive**, if $\|v\|^2 \geq 0$ for all $v \in \mathscr{H}$;


* **non-degenerate** if $\|v\|^2 = 0$ implies that $v = 0$;

* **positive definite** if it is both positive and non-degenerate.

\end{definition}

\begin{remark}
An inner product is called _indefinite_ if some $\|v\|^2$ are positive and some are negative.
\end{remark}

\begin{definition}\label{CompleteInnerProduct}
**(complete inner product)**
\linebreak
The inner product (Def. \ref{HermitianInnerProduct}) is __complete__ if, given any infinite [[sequence]] $(v_1, v_2, \ldots)$ in $\mathscr{V}$ such that we have the [[limit of a sequence|limit]]

\[ 
  \label{Cauchy} 
  \lim_{m,n\to\infty} 
  \left\|\sum_{i=m}^{m+n} v_i\right\|^2 = 0
  \,,
\]

then there exists a (necessarily unique) *[[sum]]* $S$ such that

\[ 
  \label{converge} 
  \lim_{n\to\infty} \left\|S 
  - 
  \sum_{i=1}^n v_i\right\|^2 = 0
  \,.
\]

If the inner product is definite (Def. \ref{DefiniteInnerProduct}), then this sum, if it exists, must be unique, and we write

$$ 
  S = \sum_{i=1}^\infty v_i 
$$

(with the right-hand side undefined if no such sum exists).

\end{definition}


### Alternative formulations
 {#AlternativeDefinitions}

#### As Banach spaces and metric spaces
 {#AsBanachSpacesAndMetricSpaces}

If an inner product (Def. \ref{HermitianInnerProduct}) is positive (Def. \ref{DefiniteInnerProduct}), then there exists the principal [[square root]] of the norm square $\|v\|^2 = \langle v, v \rangle$ (eq:NormSquare) being the *[[norm]]* $\|v\|$ of $v \in \mathscr{H}$.

This norm satisfies all of the requirements of a [[Banach space]].  It additionally satisfies the _parallelogram law_

\[
  \label{ParallelogramLaw}
  \|v_1 + v_2\|^2 
  + 
  \|v_1 - v_2\|^2 
  \;=\; 
  2 \|v_1\|^2 + 2 \|v_2\|^2
  \,.
\]

which not all Banach spaces need satisfy.  (The name of this law comes from its geometric interpretation: the norms in the left-hand side are the lengths of the diagonals of a parallelogram, while the norms in the right-hand side are the lengths of the sides.)

Furthermore, any Banach space satsifying the parallelogram law (eq:ParallelogramLaw) has a unique inner product that reproduces the norm, defined by

$$ 
  \langle v_1, v_2 \rangle 
  \;\coloneqq\; 
  \frac{1}{4}
  \left(
    \|v_1 + v_2\|^2 
    - 
    \|v_1 - v_2\|^2 
    - 
    \mathrm{i} 
    \|v_1 + \mathrm{i}v_2\|^2 
    + 
    \mathrm{i} 
    \|v_1 - \mathrm{i}v_2\|^2
  \right) ,
$$

or $\frac{1}{2}(\|v_1 + v_2\|^2 - \|v_1 - v_2\|^2)$ in the real case.

Therefore: A Hilbert space is equivalently [[Banach space]] that satisfies the parallelogram law (eq:ParallelogramLaw).  

This actually works a bit more generally; a positive semidefinite inner product space is a pseudonormed vector space that satisfies the parallelogram law.  (We cannot, however, recover an indefinite inner product from a norm.)

Moreover, in any positive semidefinite inner product space, let the __distance__ $d(x,y)$ be

$$ 
  d(x,y) 
  \;\coloneqq\; 
  \|y - x\| 
  \,.
$$

Then $d$ is a [[pseudometric]]; and it is a complete metric if and only if we have a Hilbert space.

In fact, the axioms of a [[Banach space]] (or pseudonormed vector space) can be written entirely in terms of the metric; we can also state the parallelogram law as follows:
$$ d(x,y)^2 + d(x,-y)^2 = 2 d(x,0)^2 + 2 d(x,x+y)^2 .$$

In definitions, it is probably most common to see the metric introduced only to state the completeness requirement.  Indeed, (eq:Cauchy) says that the sequence of partial sums is a [[Cauchy sequence]], while (eq:converge) says that the sequence of partial sums converges to $S$.




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
 {#Properties}

### Bases

A basic result is that abstractly, Hilbert spaces of the same dimension are all of the same type: every Hilbert space $H$ admits an [[orthonormal basis]], meaning a [[subset]] $S \subseteq H$ whose inclusion map extends (necessarily uniquely) to an isomorphism
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

* [[finite-dimensional Hilbert space]]

* [[rigged Hilbert space]]

* [[Hilbert C-star-module]], [[Hilbert bimodule]]

* [[measurable field of Hilbert spaces]]

* [[Kähler vector space]]


## References

Hilbert spaces were effectively introduced and used by [[David Hilbert]] and others in the context of [[integration]] theory, but the terminology and the formal definition is due to:

* {#vonNeumann30} [[John von Neumann]], §I in: *Allgemeine Eigenwerttheorie Hermitescher Funktionaloperatoren*, Math. Ann. **102** (1930) 49–131 &lbrack;[doi:10.1007/BF01782338](https://doi.org/10.1007/BF01782338)&rbrack;

motivated from laying foundations for [[quantum mechanics]]:

* {#vonNeumann32} [[John von Neumann]]: 

  *Mathematische Grundlagen der Quantenmechanik*, Springer (1932, 1971) &lbrack;[doi:10.1007/978-3-642-96048-2](https://link.springer.com/book/10.1007/978-3-642-96048-2)&rbrack;

  *Mathematical Foundations of Quantum Mechanics* Princeton University Press (1955) &lbrack;[doi:10.1515/9781400889921](https://doi.org/10.1515/9781400889921), [Wikipedia entry](https://en.wikipedia.org/wiki/Mathematical_Foundations_of_Quantum_Mechanics)&rbrack;

(where the definition occupies section II.1)

but see:

* [[Miklos Rédei]], *Why John von Neumann did not Like the Hilbert Space formalism of quantum mechanics (and what he liked instead)*, Studies in History and Philosophy of Modern Physics **27** 4 (1996) 493-510 &lbrack;<a href="https://doi.org/10.1016/S1355-2198(96)00017-2">doi:10.1016/S1355-2198(96)00017-2</a>&rbrack;


Early history:

* {#MacLane88} [[Saunders Mac Lane]]: *Hilbert space*, §5 in: *Concepts and Categories in Perspective*, in: P. Duren, *A century of mathematics in America* Part 1, AMS (1988) 323-365. &lbrack;[pdf](http://www.ams.org/samplings/math-history/hmath1-maclane25.pdf), [ISBN:0-8218-0124-4](https://www.ams.org/publicoutreach/math-history/hmath1-index)&rbrack; 

Textbook account:

* [[Nicolas Bourbaki]], §V in: *Topological Vector Spaces*, Chapters 1–5, Masson (1981), Springer (2003) &lbrack;[doi:10.1007/978-3-642-61715-7](https://doi.org/10.1007/978-3-642-61715-7)&rbrack;


Review:

* [[George Mackey]], _The Mathematical Foundations of Quamtum Mechanics_ A Lecture-note Volume, The mathematical physics monograph series. Princeton university (1963)

* E. Prugove&#265;ki, _Quantum mechanics in Hilbert Space_. Academic Press (1971)

An [[axiom|axiomatic]] characterization of the [[dagger-category]] [[Hilb]] of Hilbert spaces, with [[linear maps]] between them:

* {#HeunenKornell21} [[Chris Heunen]], [[Andre Kornell]], *Axioms for the category of Hilbert spaces*, PNAS **119** 9 (2022) e2117024119 &lbrack;[arXiv:2109.07418](https://arxiv.org/abs/2109.07418), [doi:10.1073/pnas.2117024119](https://doi.org/10.1073/pnas.2117024119)&rbrack;

* [[Chris Heunen]], [[Andre Kornell]], [[Nesta van der Schaaf]], *Axioms for the category of Hilbert spaces and linear contractions* &lbrack;[arXiv:2211.02688](https://arxiv.org/abs/2211.02688)&rbrack;



category: analysis

[[!redirects Hilbert spaces]]
[[!redirects category of Hilbert spaces]]
[[!redirects categories of Hilbert spaces]]
