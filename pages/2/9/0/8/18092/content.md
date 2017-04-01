
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $p \in \mathbb{R}$, $p \geq 1$, the _$p$-norm_ is a [[norm]] on suitable [[real vector spaces]] given by the $p$th [[root]] of the [[sum]] (or [[integral]]) of the $p$th-[[powers]] of the [[absolute values]] of the vector components. With due care the definition makes sense for non-[[finite dimensional vector spaces]] such as [[sequence spaces]] and [[Lebesgue spaces]], making them into [[normed vector spaces]], hence [[metric spaces]].

For $p = 2$ the $p$-norm is the standard _Euclidean norm_, defining [[Euclidean spaces]] and [[Hilbert spaces]] of [[square integrable functions]].

For $p = \infty$ one takes the $p$-norm to be given by the [[supremum]] over the components of vectors, then called the _supremum norm_.

## Definition

The concept of $p$-norm makes sense in increasing generality, 

* _[For finite-dimensional vector spaces](#ThePNorm)_;

* _[For spaces of sequences of real numbers](#OnSequenceSpaces)_;

* _[For spaces of measurable functions](#OnLebesgueSpaces)_.



### The $p$-norm on finite dimensional vector spaces
 {#ThePNorm}

For $n \in \mathbb{N}$, $p \in \mathbb{R}$, $p \gt 0$, the _$p$-norm_ ${\Vert - \Vert}_p$ is the [[norm]] on the [[real vector space|real]] [[finite dimensional vector space]] $\mathbb{R}^n$ given by the $p$th [[root]] of the [[sum]] of the $p$-[[powers]] of the [[absolute value]] of the components of a given [[vector]] $\vec x = (x)_{i = 1}^n \in \mathbb{R}^n$: 

$$ 
  {\Vert \vec x \Vert}_p  \coloneqq \root p {\sum_i {\vert x_i\vert^p}} 
$$

Equipping it with this [[norm]] makes $\mathbb{R}^n$ a  _[[normed vector space]]_.

For $p = 2$ this is the _Euclidean norm_, the standard norm that defines [[Euclidean space]].

For $p = \infty$ one takes the [[supremum]] over the [[absolute values]] of the components

$$
  \Vert \vec x\Vert_\infty
    \;\coloneqq\;
  \underset{1 \leq i \leq n}{\sub} {\vert x_i\vert}
  \,.
$$

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d4/Vector-p-Norms_qtl1.svg/220px-Vector-p-Norms_qtl1.svg.png" width="200">
</div>

The graphics on the right (grabbed from Wikipedia) shows unit circles in $\mathbb{R}^2$ with respect to various [[p-norms]].


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
  {\Vert -\Vert}_p
  \;\colon\;
  \ell^p
    \longrightarrow
  \mathbb{R}
$$

$$
  \Vert (x_i)_{i \in \mathbb{N}} \Vert
    \;\coloneqq\;
  \root{p}{\underset{i \in \mathbb{N}}{\sum} {\vert x_i\vert}^p}
$$

defines a [[norm]] on this [[real vector space]]. This [[normed vector space]] is [[complete metric space|complete]], hence a [[Banach space]]. This is called the _[[sequence space]]_.

For $p = \infty$ one takes $\ell^\infty$ to be the space of bounded sequences and

$$
  \Vert (x_i)_{i \in \mathbb{N}} \Vert
   \;\coloneqq\;
  \underset{k \in \mathbb{N}}{sup} {\vert x_k\vert }
$$

to be the [[supremum]] over the [[absolute values]] of the components of the sequence. This is also called the _supremum norm_.


### The $L^p$-norm on Lebesgue spaces
 {#OnLebesgueSpaces}

More generally, for $(X,\mu)$ a [[measure space]], write $L^p(X)$ for the [[vector space]] of [[equivalence classes]] of those [[measurable functions]] $f \colon X \to \mathbb{R}$, for which the [[integral]]

$$
  \int_X {\vert f \vert}^p  d\mu \;\lt\; \infty
$$

exists, and where two such functioons are regarded as equivalent, $f_1 \sim f_2$, if

$$
  \int_X {\vert f_2 - f_1 \vert}^p  d\mu \;=\; 0
  \,. 
$$

On this space the function

$$
  {\Vert -\Vert}_p
  \;\colon\;
  L^p(X) \longrightarrow \mathbb{R}
$$

$$
  {\Vert f \Vert}_p
  \;\colon\;
  \root{p}{\int_X {\vert f\vert}^p} d\mu 
$$

defines a [[norm]]. The [[triangle inequality]] holds due to [[Minkowki's inequality]].  The [[normed vector space]] $(L^p(X), {\Vert- \Vert}_p)$ is also called a _[[Lebesgue space]]_.


## References

* Wikipedia, _[Lp space -- The p-norm in finite dimensions](https://en.wikipedia.org/wiki/Lp_space#The_p-norm_in_finite_dimensions)_

* German Wikipedia, _[p-Norm](https://de.wikipedia.org/wiki/P-Norm)_

[[!redirects p-norms]]

[[!redirects Euclidean norm]]
[[!redirects Euclidean norms]]

[[!redirects supremum norm]]
[[!redirects supremum norms]]
