
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

A _rigged Hilbert space_ is a formal device which makes it possible to treat spectral theory of normal [[unbounded operator]]s on a [[Hilbert space]] as if it were about actual eigenvalues and eigenvectors. It may be used to make rigorous the idea of eigenstates for observables as they commonly arise in [[quantum mechanics]]. 

## Example 

Let $H$ be the Hilbert space $L^2(\mathbb{R}, d x)$ consisting of square integrable functions $f$ with respect to [[Lebesgue measure]]. There is an unbounded self-adjoint operator 

$$m_x: H \to H: f \mapsto x \cdot f$$ 

where $(x \cdot f)(y) := y f(y)$. This operator is not defined on all of $H$, but it is defined on a dense subspace of $H$. For example, if $S$ is the Schwartz space consisting of smooth functions $f$ on $\mathbb{R}$ all of whose derivatives $f^{(n)}(x)$ decay rapidly at infinity (more rapidly than any negative power of $|x|$), then there is a dense inclusion map $i: S \to H$, and $m_x$ is defined globally on $S$. 

Meanwhile the Schwartz space $S$ carries its own topology (as described in the article [[distribution]]), stronger than the topology it inherits from $H$, and the space of tempered distributions $S^*$ is defined to be the continuous dual of the [[topological vector space]] $S$. Since the continuous inclusion $i: S \to H$ is dense, it follows that any continuous functional 

$$f: S \to \mathbb{C}$$ 

has at most one extension to a continuous functional $H \to \mathbb{C}$. In other words, the adjoint map 

$$i^*: H^* \to S^*$$ 

is injective. In addition, the topology on $S$ is such that the operator $m_x: S \to S$ is continuous. 

In this example, there is a dense inclusion $S \to S^*$ defined by the inner product pairing, and the operator $m_x$ extends uniquely to an operator $S^* \to S^*$, called $m_x$ by abuse of notation. Again, in this example, the operator $m_x: S^* \to S^*$ has an eigenvector $s_{\xi}$ for each $\xi \in \mathbb{R}$:  

$$m_x(s_{\xi}) = \xi s_{\xi}$$ 

_Ugh. Lousy start on something that would be nice to understand properly. Maybe an expert can help out. John, you there?_ 


## References

Among the original treatises on the theory of rigged Hilbert spaces is

* [[John Roberts]], _Rigged Hilbert spaces in quantum mechanics_, Communications in Mathematical Physics, *3*  (1966)  98–119. doi:[10.1007/BF01645448](https://doi.org/10.1007/BF01645448)

A unification of various inequivalent approaches is claimed to be achieved in 

* M. Gadella, F. Gómez, _A Unified Mathematical Formalism for the Dirac Formulation of Quantum Mechanics_, Foundations of Physics *32* (2002) 815–869, doi:[10.1023/A:1016069311589](https://doi.org/10.1023/A:1016069311589)

See also

* S. Wickramasekara, A. Bohm, _Symmetry Representations in the Rigged Hilbert Space Formulation of Quantum Mechanics_ ([arXiv](http://arxiv.org/abs/math-ph/0302018))

Rigged Hilbert spaces are also known as [[Gelfand triple]]s, written about in his series on generalized functions

* Gel'fand, I. M., and Shilov, Georgiĭ Evgenʹevich. Generalized Functions. United States, American Mathematical Society, (2016)

## See also

Discussion on MathOverflow

* [_Good references for Rigged Hilbert spaces?_](https://mathoverflow.net/questions/43313/good-references-for-rigged-hilbert-spaces)

[[!redirects rigged Hilbert spaces]]