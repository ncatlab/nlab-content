
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Kripke's schema is a principle first found implicitly in the [[intuitionistic mathematics|school of Brouwer]], going beyond base [[constructive logic]]. It ties [[propositions]] (or, in some formulations, membership of [[subsets]] of the [[natural numbers|naturals]]) to the values of infinite [[sequences]] in $\{0, 1\}$. 

## Formulation
__KS__:
For every statement $\phi$ holds: There exists a binary sequence $a$, such that $\phi$ holds iff there is some $n$ such that $a_n=1$.

In the formalization of evolving [[choice sequences]] by [[Saul Kripke]], this may be motivated by the idea that, roughly speaking, for any proposition there would be a sequence capturing its proof search, so that, thus, if and only if the proposition is provable, that search eventually terminates.

## Weaker variants
KS implies, for example, the following Weak Principle of Finite Possibility, which can be stated just in terms of sequences:

__WPFP__:
For every binary sequence $b$, there exists a binary sequence $a$, such that $b$ is the zero sequence iff $a$ is not the zero sequence.

This is to say, to any sequence there is a certain sort of value-inverted sequence. Classically, of course, the value $1 - {\mathrm{max}}({\mathrm{range}}(b))$ exactly determines whether $b$ is the zero sequence and thus the constant sequence $a$ with that value does the job. But constructively one generally cannot inspect all, infinitely many return values of a sequence $b$.

## Implications
Binary sequences are nicely behaved objects and, in turn, KS can be shown to be equivalent to the claim that every inhabited subset of the naturals is countable. 

The principles also has implications for [[metric spaces]].

It can be shown that (WPFP + [[Markov's principle | MP]]) iff [[principle of omniscience | LPO]]. Those principles are thus not provable in Russian constructivism (adopting MP but not LPO). Indeed, formulations of KS contradict the so called Constructive Church's Thesis.

## Related concepts

* [[intuitionism]]

* [[Markov's principle]], MP

* [[principle of omniscience]], LPO

## References

* D. Van Dalen, _The Use of Kripke's Schema as a Reduction Principle_, The Journal of Symbolic Logic Vol. 42, No. 2 (1977) ([euclid:jsl/1183739949](https://projecteuclid.org/euclid.jsl/1183739949))

* Mark van Atten, _The Creating Subject, the Brouwer-Kripke Schema, and infinite proofs_, Indagationes Mathematicae
Volume 29, Issue 6, 2018
([arXiv:1805.00404](https://arxiv.org/abs/1805.00404), [doi:10.1016/j.indag.2018.06.005](https://doi.org/10.1016/j.indag.2018.06.005))

[[!redirects Kripke schema]]
