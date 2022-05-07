
#Contents#
* table of contents
{:toc}

## Idea

Kripke's schema is a principle first found implicit in the school of Brouwer, going beyond base constructive logic. It ties propositions (or, in some formulations, membership of subsets of the naturals) to the values of infinite sequences in {0, 1}. 

## Formulation
KS:
For every statement P, there exists a binary sequence A, such that P holds iff there is some n such that A(n) equals 1.

In the formalization of evolving [[choice sequences]] by [[Saul Kripke]], this may be motivated by the idea that to any provable proposition, roughly speaking, there would be a sequence that captures the proof search which eventually terminates.

Sequences are nicely behaved objects and, in turn, KS can be shown to be equivalent to the claim that every inhabited subset of the naturals is countable. 

## Weaker variants
KS implies, for example, the following Weak Principle of Finite Possibility, which can be stated just in terms of sequences:

WPFP:
For every binary sequence B, there exists a binary sequence A, such that B is the zero sequence iff A is not the zero sequence.

This is to say, to any sequence there is a certain sort of inverse sequence. Classically, of course, the value 1-max(B) exactly determines whether B is the zero sequence and thus the constant sequence with that value does the job. But constructively one can't generally inspect all return values of a sequence B.

## Implications
It can be shown that (WPFP + MP) iff LPO. Those principles are thus not provable in Russian constructivism (adopting MP but not LPO). Indeed, formulations of KS contradict the so called Constructive Church's Thesis. They are however implied by Brouwer's (or Kripke's) concept of sequence.

It also has implications for metric spaces.

## Related concepts

* [[intuitionism]]

* [[Markov's principle]], MP

## References

* D. Van Dalen, _The Use of Kripke's Schema as a Reduction Principle_, The Journal of Symbolic Logic Vol. 42, No. 2 (1977) ([euclid:jsl/1183739949](https://projecteuclid.org/euclid.jsl/1183739949))

* Mark van Atten, _The Creating Subject, the Brouwer-Kripke Schema, and infinite proofs_, Indagationes Mathematicae
Volume 29, Issue 6, 2018
([arXiv:1805.00404](https://arxiv.org/abs/1805.00404), [doi:10.1016/j.indag.2018.06.005](https://doi.org/10.1016/j.indag.2018.06.005))

[[!redirects Kripke schema]]
