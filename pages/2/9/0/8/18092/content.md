
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

For $p \in \mathbb{R}$, $p \geq 1$, the _$p$-norm_ is a [[norm]] on suitable [[real vector spaces]] given by the $p$th [[root]] of the [[sum]] (or [[integral]]) of the $p$th-[[powers]] of the [[absolute values]] of the vector components. With due care the definition makes sense for non-[[finite dimensional vector spaces]] such as [[sequence spaces]] and [[Lebesgue spaces]], making them into [[normed vector spaces]], hence [[metric spaces]].

For $p = 1$ the $p$-norm is the _Taxicab norm_ or _Manhattan norm_.

For $p = 2$ the $p$-norm is the standard _Euclidean norm_, defining [[Euclidean spaces]] and [[Hilbert spaces]] of [[square integrable functions]].

For $p = \infty$ the $p$-norm (found by taking the limit $p \to \infty$) is the [[supremum]] (or [[essential supremum]] in the continuous case) of the absolute values of the components of vectors, then called the _supremum norm_.

For $0 \leq p \lt 1$ one may still make sense of the formulas that define $p$-norms for $p \geq 1$ (see at _[Generalizations](#Generalizations)_ below), but the resulting concepts are no longer genuine norms.


## Definition

The concept of $p$-norm makes sense in increasing generality, 

* _[For finite-dimensional vector spaces](#ThePNorm)_;

* _[For spaces of sequences of real numbers](#OnSequenceSpaces)_;

* _[For spaces of measurable functions](#OnLebesgueSpaces)_.


### The $p$-norm on finite dimensional vector spaces
 {#ThePNorm}

For $n \in \mathbb{N}$, $p \in \mathbb{R}$, $p \gt 0$, the _$p$-norm_ $\Vert - \Vert_p$ is the [[norm]] on the [[real vector space|real]] [[finite dimensional vector space]] $\mathbb{R}^n$ given by the $p$th [[root]] of the [[sum]] of the $p$-[[powers]] of the [[absolute value]] of the components of a given [[vector]] $\vec x = (x)_{i = 1}^n \in \mathbb{R}^n$: 

$$ 
  {\Vert \vec x \Vert_p}  \coloneqq \root p {\sum_i {\vert x_i\vert^p}} 
$$

Equipping it with this [[norm]] makes $\mathbb{R}^n$ a  _[[normed vector space]]_.

For $p = 2$ this is the _Euclidean norm_, the standard norm that defines [[Euclidean space]].

For $p = \infty$ one takes the [[supremum]] over the [[absolute values]] of the components

$$
  {\Vert \vec x\Vert_\infty}
    \;\coloneqq\;
  \underset{1 \leq i \leq n}{sup} {\vert x_i\vert}
  \,.
$$

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d4/Vector-p-Norms_qtl1.svg/220px-Vector-p-Norms_qtl1.svg.png" width="200">
</div>

The graphics on the right (from Wikipedia) shows unit circles in $\mathbb{R}^2$ with respect to various [[p-norms]].


### The $\mathcal{l}^p$-norm on sequence spaces
 {#OnSequenceSpaces}

For $p \in \mathbb{R}$, write $\ell^p$ for the vector space of those [[sequences]] $(x_i)_{i \in \mathbb{N}}$ in $\mathbb{R}$ for which the [[series]]

$$
  \underset{i \in \mathbb{N}}{\sum} {\vert x_i\vert}^p
    \;\lt\; 
  \infty
$$

(the [[sum]] of the $p$th [[powers]] of the [[absolute value]] of the components of the sequence) [[convergence|converges]].

For $p \geq 1$ the the [[function]]

$$
  {\Vert -\Vert_p}
  \;\colon\;
  \ell^p
    \longrightarrow
  \mathbb{R}
$$

$$
  {\Vert (x_i)_{i \in \mathbb{N}} \Vert_p}
    \;\coloneqq\;
  \root{p}{\underset{i \in \mathbb{N}}{\sum} {\vert x_i\vert^p}}
$$

defines a [[norm]] on this [[real vector space]]. This [[normed vector space]] is [[complete metric space|complete]], hence a [[Banach space]]. This is called the _[[sequence space]]_.

For $p = \infty$ one takes $\ell^\infty$ to be the space of bounded sequences and

$$
  {\Vert (x_i)_{i \in \mathbb{N}} \Vert_\infty}
   \;\coloneqq\;
  \underset{k \in \mathbb{N}}{sup} {\vert x_k\vert }
$$

to be the [[supremum]] over the [[absolute values]] of the components of the sequence. This is also called the _supremum norm_.


### The $L^p$-norm on Lebesgue spaces
 {#OnLebesgueSpaces}

More generally, for $(X,\mu)$ a [[measure space]], write $L^p(X)$ for the [[vector space]] of [[equivalence classes]] of those [[measurable functions]] $f \colon X \to \mathbb{R}$, for which the [[integral]]

$$
  \int_X {\vert f \vert^p}  d\mu \;\lt\; \infty
$$

exists, and where two such functions are regarded as equivalent, $f_1 \sim f_2$, if

$$
  \int_X {\vert f_2 - f_1 \vert^p}  d\mu \;=\; 0
  \,. 
$$

On this space the function

$$
  {\Vert -\Vert_p}
  \;\colon\;
  L^p(X) \longrightarrow \mathbb{R}
$$

$$
  {\Vert f \Vert_p}
  \;\coloneqq\;
  \root{p}{\int_X {\vert f\vert^p}} d\mu 
$$

defines a [[norm]]. The [[triangle inequality]] holds due to [[Minkowski's inequality]].  The [[normed vector space]] $(L^p(X), {\Vert- \Vert_p})$ is also called a _[[Lebesgue space]]_.


## Generalizations for $0 \leq p \lt 1$
 {#Generalizations}

For $0 \leq p \lt 1$, the above definitions for $\Vert {-}\Vert_p$ still make sense in themselves, but the result is no longer a norm, as [[Minkowski's inequality]] (the [[triangle inequality]] for $p$-norms) fails.

A variant definition for $0 \lt p \leq 1$ (which agrees with the usual definition for $p = 1$, preserving continuity in $p$) leaves out the $p$th root; then the result satisfies the triangle inequality (and indeed is a [[metric]]) but fails to be a norm because it is not positive-homogeneous of degree $1$ (but of degree $p$ instead).  Such a thing is called an [[F-norm]].

For $p = 0$, we might try to take the limit as $p \searrow 0$.  For the unmodified $p$-norm (with the root), this is infinite if there is more than one nonzero entry and is the absolute value of the one nonzero entry if there is only one (or 0 if there is none); for the modified $p$-norm (without the root), it is the (possibly infinite) number of nonzero entries.  In either case, however the triangle inequality fails.  Therefore, there is a further modified $0$-norm, given by
$$ {\|(x_1, x_2, \ldots)\|_0} = \sum_{n=1}^\infty \frac {2^{-n} {|x_n|}} {1 + {|x_n|}} $$
for $l^0$, and this is an $F$-norm.  (But I don\'t know what is the justification for thinking of this as a $p$-norm for $p = 0$.)


## References

* Wikipedia, _[Lp space -- The p-norm in finite dimensions](https://en.wikipedia.org/wiki/Lp_space#The_p-norm_in_finite_dimensions)_

* German Wikipedia, _[p-Norm](https://de.wikipedia.org/wiki/P-Norm)_

[[!redirects p-norm]]
[[!redirects p-norms]]

[[!redirects Lebesgue norm]]
[[!redirects Lebesgue norms]]

[[!redirects taxicab norm]]
[[!redirects taxicab norms]]

[[!redirects Manhattan norm]]
[[!redirects Manhattan norms]]

[[!redirects Euclidean norm]]
[[!redirects Euclidean norms]]

[[!redirects supremum norm]]
[[!redirects supremum norms]]

[[!redirects sup-norm]]
[[!redirects sup-norms]]

