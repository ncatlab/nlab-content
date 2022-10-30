

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[functional analysis]], [[distributional densities]] are usefully thought of as _generalized smooth functions_ in that every [[distribution]] is the [[limit of a sequence|limit]] of a [[sequence]] of [[smooth functions]], thought of as [[non-singular distributions]] ([this prop.](non-singular+distribution#NonSingularDistributionsAreDenseInAllDistributions)).

More in detail, regarding a [[smooth function]] $f \in C^\infty(X)$ as a [[distributional density]] means to regard it as the [[integral kernel]]

$$
  u_f 
  \;\colon\;
  b \mapsto \underset{X}{\int} f(x) b(x) \, dvol_X(x)
$$

on [[bump functions]] $b \in C^\infty_{cp}(X)$. Therefore a [[limit of a sequence|limit]] over a sequence $\{f_n\}_{n \in \mathbb{N}}$ of smooth functions, which may not really exists as a smooth function but just as a distribition, is nevertheless usefully thought of as the integral against the "generalized function" which would be "$\underset{\underset{n}{\longrightarrow}}{\lim} f_n$" if that limit existed in $C^\infty(X)$:

$$
  \underset{X}{\int}
    \left(\underset{\underset{n}{\longrightarrow}}{\lim} f_n\right)(x)
    b(x) \, dvol_X(x)
  \;\coloneqq\;
  \underset{\underset{n}{\longrightarrow}}{\lim}
  \underset{X}{\int}
    f_n(x) b(x), dvol_X(x)
  \,.
$$

It is common and convenient to write evaluation of [[distributions]] on test functions in this way, and the name of many distributions reflects this habit, such as "[[Dirac delta function]]" for the [[delta distribution]] or "[[commutator function]]" for a [[causal propagator]].

In particular [[distributions]] that arise from [[integral]] expressions appearing in [[Fourier analysis]] are often conveniently written this way: For $f \in \mathbb{R}^n$ a [[smooth function]] (or [[distribution]]) in a [[variable]] $k$, its [[Fourier transform of distributions]] $\hat f$ generally is given as a generalized function by the integral expression

$$
  \hat f(x) 
    \;=\; 
  \underset{\mathbb{R}^n}{\int} f(k) e^{i k \cdot x} \, d^n k
$$

which however in general is not an actual _function_ of $x$, in that this [[integral]] need not [[convergence of a sequence|converge]] for fixed $x \in \mathbb{R}^n$, but is a generalized function in that for appropriate test functions $b$ the further integral 

$$
  \underset{\mathbb{R}^n}{\int} \underset{\mathbb{R}^n}{\int} f(k) e^{i k \cdot x}  b(x) \, d^n x \, d^n k
 \;\in\;
 \mathbb{C}
$$

does make sense.

For example it is in this sense that the [[delta-distribution]], regarded as a generalized function, is given by the common [[integral]] expression

$$
  \delta(x) \;=\; \underset{k \in \mathbb{R}^n}{\int} e^{2 \pi i k x} d^n k
$$

(see at _[[delta distribution]]_ [this example](Dirac+distribution#FourierTransformOfDeltaDistribution)).

Thinking of distributions as generalized functions this way motivates and streamlines the extension of a variety of concepts from functions to distributions, such as the concepts of _[[product of distributions]]_, _[[derivative of distributions]]_, _[[support of distributions]]_, [[distributional solutions to a PDE]] and so on.

## Related concepts

* [[distribution]]

* [[hyperfunction]]

[[!redirects generalized functions]]
