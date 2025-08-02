
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


# Radon--Nikodym derivatives
* table of contents
{: toc}

## Idea

Given two [[measures]] $\mu, \nu$ on the same [[measurable space]], their Radon--Nikodym derivative is essentially their ratio $\mu/\nu$, although this is traditionally written $\mathrm{d}\mu/\mathrm{d}\nu$ because of analogies with [[differentiation]].  This ratio or derivative is a [[measurable function]] which is defined up to [[almost equality|equality almost everywhere]] with respect to the divisor $\nu$.  It only exists iff $\mu$ is [[absolutely continuous measure|absolutely continuous]] with respect to $\nu$.

Integration on a general [[measure space]] can be seen as the process of multiplying a measure by a function to get a measure.  Then the Radon--Nikodym derivative is the reverse of this: dividing two measures to get a function.


## The Radon–Nikodym theorem

\begin{definition}
Suppose $X$ is a [[set]], $\Sigma$ is a [[σ-algebra]] of subsets of $X$,
$\mu\colon\Sigma\to[0,\infty]$ is a countably additive measure,
and $\nu\colon\Sigma\to\mathbf{R}$ is a finitely additive map.
We say that $\nu$ is _absolutely continuous_ with respect to $\mu$
if for any $\epsilon\gt0$ there is $\delta\gt0$ such that $|\nu E|\lt\epsilon$
for any $E\in\Sigma$ such that $\mu(E)\lt\delta$.
We say that $\nu$ is _truly continuous_ with respect to $\mu$
if for any $\epsilon\gt0$ we can find $E\in\Sigma$ and $\delta\gt0$ such that $\mu(E)$ is finite and $|\nu(F)|\lt\epsilon$ whenever $F\in\Sigma$
and $\mu(E\cap F)\lt\delta$.
\end{definition}

\begin{remark}
If we assume $\nu$ to be countably additive, then the definition
of absolutely continuity simplifies as follows:
$\nu$ is absolutely continuous with respect to $\mu$ if and only if
for any $E\in\Sigma$ we have $\nu(E)=0$ whenever $\mu(E)=0$.
\end{remark}

\begin{remark}
$\nu$ is truly continuous with respect to $\mu$ if and only if
$\nu$ it is countable additive,
$\nu$ absolutely continuous with respect to $\mu$,
and for any $E\in\Sigma$ such that $\nu(E)\gt0$
we can find $F\in\Sigma$ such that $F\subset E$, $\mu(F)$ is finite,
and $\nu(F)\gt0$.
\end{remark}

\begin{theorem}
Suppose $X$ is a [[set]], $\Sigma$ is a [[σ-algebra]] of subsets of $X$,
$\mu\colon\Sigma\to[0,\infty]$ is a countably additive measure,
and $\nu\colon\Sigma\to\mathbf{R}$ is a function.
Then there is a $\mu$-integrable function $f$ such that $\nu(E)=\int_E f$ for all $E\in\Sigma$ if and only if $\nu$ is finitely additive and truly continuous with respect to $\mu$.
\end{theorem}

\begin{corollary}
In the context of the above theorem,
if $(X,\Sigma,\mu)$ is [[σ-finite]], then there is a $\mu$-integrable function $f$ such that $\nu(E)=\int_E f$ for all $E\in\Sigma$ if and only if
$\nu$ is countably additive and absolutely continuous with respect to $\mu$.
If $\mu(X)$ is finite, it suffices to require that $\nu$ is finitely additive.
\end{corollary}

\begin{example}
The following example shows that the condition of being truly continuous
is necessary in the non-σ-finite case.
Consider an uncountable set $X$,
a [[σ-algebra]] $\Sigma$ of subsets of $X$ that are countable or have countable complement,
the counting measure $\mu\colon\Sigma\to[0,\infty]$,
and the measure $\nu\colon\Sigma\to[0,1]$ that vanishes on countable sets
and takes value 1 on all uncountable subsets.
Then $\nu$ is absolutely continuous with respect to $\mu$ because $\mu$ only vanishes on the empty set.
However, $\nu$ is not truly continuous with respect to $\mu$
because $\mu$ takes finite values only on finite sets,
but for any such a set $E$ we have $\nu(X\setminus E)=1$,
which yields a contradiction if $\epsilon\lt1$.
\end{example}

\begin{example}
The [[measure space]] in the last example is quite pathological: it is not [[localizable measure | localizable]].
A [[localizable measure | localizable]] example can be constructed if and only if [[real-valued-measurable cardinals]] exist.
In this case, take $X$ to be a [[real-valued-measurable cardinal]],
$\mu\colon 2^X\to[0,\infty]$ to be the counting measure,
and $\nu\colon 2^X\to[0,1]$ a probability measure that vanishes on all countable subsets of $X$.
Then $\nu$ is absolutely continuous with respect to $\mu$ because only the empty subset of $X$ has $\mu$-measure 0.
However, $\nu$ is not truly continuous with respect to $\mu$
because $\mu$ takes finite values only on finite sets,
but for any such a set $E$ we have $\nu(X\setminus E)=1$,
which yields a contradiction if $\epsilon\lt1$.
\end{example}

\begin{remark}
Truly continuous countably (or finitely) additive measures
on a measure space $(X,\Sigma,\mu)$
form a module over the complex [[*-algebra]]
of measurable maps $X\to\mathbf{R}$ modulo equality almost everywhere.
The Radon–Nikodym theorem then says that this module
is a free module of rank 1.
Furthermore, generators of this module can be identified
with truly continuous measures $\nu$ such that $\mu$ is absolutely continuous with respect to $\nu$.
\end{remark}

## The Lebesgue decomposition

\begin{theorem}
Suppose $X$ is a [[set]], $\Sigma$ is a [[σ-algebra]] of subsets of $X$,
$\mu\colon\Sigma\to[0,\infty]$ is a countably additive measure,
and $\nu\colon\Sigma\to\mathbf{R}$ is a countably additive function.
Then there is a unique decomposition
$$\nu=\nu_s+\nu_t+\nu_e,$$
where $\nu_t$ is truly continuous with respect to $\mu$,
$\nu_e$ is absolutely continuous with respect to $\mu$ and vanishes
on every measurable set of finite $\mu$-measure,
and $\nu_s$ is singular with respect to $\mu$,
meaning there is a set $F\in\Sigma$ such that $\mu(F)=0$
and $\nu(E)=0$ for all $E\in\Sigma$ such that $E\subset X\setminus F$.
In particular, setting $\nu_a=\nu_t+\nu_e$ yields a unique decomposition $\nu=\nu_s+\nu_a$ of $\nu$ as a sum of a singular and absolutely continuous measure.
\end{theorem}

## Definitions

Let $X$ be a [[measurable space]] (so $X$ consists of a [[set]] ${|X|}$ and a $\sigma$-[[sigma-algebra|algebra]] $\mathcal{M}_X$), and let $\mu$ and $\nu$ be [[measures]] on $X$, valued in the [[real numbers]] (and possibly taking infinite values) or in the [[complex numbers]] (and taking only finite values).  Let $f$ be a [[measurable function]] $f$ (with real or complex values) on $X$.

+-- {: .un_defn}
###### Definition
The function $f$ is a __Radon--Nikodym derivative__ of $\mu$ with respect to $\nu$ if, given any [[measurable subset]] $A$ of $X$, the $\mu$-measure of $A$ equals the integral of $f$ on $A$ with respect to $\nu$:
$$ \mu(A) = \int_A f \nu = \int_{x \in A} f(x) \mathrm{d}\nu(x) .$$
(The latter two expressions in this equation are different notations for the same thing.)
=--


## Properties

These properties are basic to the concept; the notation is as in the definition above.

+-- {: .num_theorem}
###### Theorem

Let $f$ be a Radon--Nikodym derivative of $\mu$ with respect to $\nu$, and let $g$ be a measurable function on $X$.  Then $g$ is a Radon--Nikodym derivative of $\mu$ with respect to $\nu$ if and only if $f$ and $g$ are equal almost everywhere with respect to $\nu$.
=--

+-- {: .num_theorem}
###### Theorem
If a Radon--Nikodym derivative of $\mu$ with respect to $\nu$ exists, then $\mu$ is [[absolutely continuous measure|absolutely continuous]] with respect to $\nu$.
=--

+-- {: .num_theorem}
###### Theorem
If $\mu$ is [[absolutely continuous measure|absolutely continuous]] with respect to $\nu$ and both $\mu$ and $\nu$ are $\sigma$-[[sigma-finite measure|finite]], then a Radon--Nikodym derivative of $\mu$ with respect to $\nu$ exists.
=--

+-- {: .proof}
###### Proofs

For fairly elementary proofs, see [Bartels (2003)](#Bartels2003).
=--

(This last theorem is not as general as it could be.)

Note the repetition of 'with respect to $\nu$' in various guises; let us fix $\nu$ (assumed to be $\sigma$-finite) and take everything with respect to it.  Then it is convenient to treat all measurable functions up to [[almost equality|equality almost everywhere]]; and given any absolutely continuous $\mu$ (also assumed to be $\sigma$-finite), we speak of [[the]] Radon--Nikodym derivative of $\mu$.


## Notation

See also the discussion of notation at [[measure space]].

Using the simplest notation for integrals, the definition of Radon--Nikodym derivative reads
$$ \mu(A) = \int_A f \nu ,$$
or equivalently
$$ \int_A \mu = \int_A f \nu .$$
In other words, the measure $\mu$ is the product of the function $f$ and the measure $\nu$:
$$ \mu = f \nu ;$$
and so $f$ is the ratio of $\mu$ to $\nu$:
$$ f = \mu/\nu .$$
So this is the simplest notation for the Radon--Nikodym derivative.

However, this notation for integrals is uncommon; one is more likely to see
$$ \int_A \mathrm{d}\mu = \int_A f \,\mathrm{d}\nu ,$$
which leads to
$$ f = \mathrm{d}\mu/\mathrm{d}\nu $$
for the Radon--Nikodym derivative.  But none of these '$\mathrm{d}$'s are really necessary.

We can also use a fuller notation with a dummy variable as the object of the symbol '$\mathrm{d}$':
$$ \int_{x \in A} \mu(\mathrm{d}x) = \int_{x \in A} f(x) \,\nu(\mathrm{d}x) ;$$
this leads to
$$ f(x) = \mu(\mathrm{d}x)/\nu(\mathrm{d}x) ,$$
which does not give a symbol for $f$ directly.  If instead of $\mu(\mathrm{d}x)$ one unwisely writes $\mathrm{d}\mu(x)$, then this gives the previous notation for the Radon--Nikodym derivative.

Now let $\nu$ be [[Lebesgue measure]] on the [[real line]] and let $F$ be an upper [[semicontinuous function]] on the real line, so that $F$ defines a [[Borel measure]] $\mu$ generated by
$$ \mu({]-\infty,a]}) \coloneqq F(a) .$$
Then $F$ is [[absolutely continuous function|absolutely continuous]] if and only if $\mu$ is absolutely continuous, in which case the [[derivative]] $F'$ exists almost everywhere and is a Radon--Nikodym derivative of $\mu$.  That is,
$$ \mu/\nu = F' = \mathrm{d}F/\mathrm{d}t .$$
The presence of '$\mathrm{d}$' on the right-hand side inspires people to put it on the left-hand side as well; but this is spurious, since we really want to write
$$ \mu = \mathrm{d}F $$
and
$$ \nu = \mathrm{d}t ,$$
where $t$ is the [[identity function]] on the real line.


## References

A comprehensive treatment can be found in Chapter 23 of

* [[David H. Fremlin]], _Measure Theory_.

Some fairly elementary proofs prepared for a substitute lecture in [[John Baez]]\'s introductory measure theory course are here:

*  [[Toby Bartels]] (2003): _The Radon Nikodym Theorem_; [web](http://tobybartels.name/notes/#Radon).
   {#Bartels2003}

The strategy there is based on:

*  Richard Bradley (1989): An Elementary Treatment of the Radon-Nikodym Derivative, American Mathematical Monthly 96(5), 437--440.


[[!redirects Radon-Nikodym derivative]]
[[!redirects Radon-Nikodym derivatives]]
[[!redirects Radon–Nikodym derivative]]
[[!redirects Radon–Nikodym derivatives]]
[[!redirects Radon--Nikodym derivative]]
[[!redirects Radon--Nikodym derivatives]]

[[!redirects Radon-Nikodym ratio]]
[[!redirects Radon-Nikodym ratios]]
[[!redirects Radon–Nikodym ratio]]
[[!redirects Radon–Nikodym ratios]]
[[!redirects Radon--Nikodym ratio]]
[[!redirects Radon--Nikodym ratios]]

[[!redirects Radon-Nikodym theorem]]
[[!redirects Radon-Nikodym theorems]]
[[!redirects Radon–Nikodym theorem]]
[[!redirects Radon–Nikodym theorems]]
[[!redirects Radon--Nikodym theorem]]
[[!redirects Radon--Nikodym theorems]]
[[!redirects Radon-Nikodym Theorem]]
[[!redirects Radon-Nikodym Theorems]]
[[!redirects Radon–Nikodym Theorem]]
[[!redirects Radon–Nikodym Theorems]]
[[!redirects Radon--Nikodym Theorem]]
[[!redirects Radon--Nikodym Theorems]]
