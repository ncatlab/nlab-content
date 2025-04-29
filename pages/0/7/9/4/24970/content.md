#Contents#
* table of contents
{:toc}

## Idea

The _relative Langlands program_ is a generalization of the [[Langlands program]] that is phrased in terms of [[spherical varieties]] instead of directly in terms of [[reductive groups]]. It is expected to recover the usual Langlands program in the group case. In more recent work, instead of focusing on a spherical variety $X$, the main focus is on a [[Hamiltonian action|Hamiltonian]] [[G-space|$G$-space]] $M$, which is often related to $X$ via its [[cotangent bundle]] $M=T^{*}X$. The tools of [[geometric quantization]] can then be used, with $M$ playing the role of the classical [[phase space]] to be quantized.

Recent ongoing work by Ben-Zvi, Sakellaridis, and Venkatesh attempt to relate it to [[topological quantum field theory]] (as inspired by both the [[Kapustin-Witten TQFT]] as well as the analogies of [[arithmetic topology]]). This is expected as well to illuminate topics in special values of [[L-functions]].

## Quantization in the relative Langlands program

The reference for this section is [#Sakellaridis2021](#Sakellaridis2021).

Let $F$ be the [[global field|global]] [[base field]] and let $G$ be a [[reductive group]]. Locally, the idea of "quantization" in the relative Langlands program refers to obtaining a [[unitary representation]] $\omega_{v}$ of $G(F_{v})$ out of the [[Hamiltonian action|Hamiltonian]] [[G-space|$G$-space]] $M$, analogous to the theory of [[geometric quantization]]. We also want a "base vector" $\Phi_{v}^{0}\in \omega_{v}$ for almost all $v$. Globally, we want to put together these local representations and have an automorphic realization $\otimes'\omega_{v}\to C^{\infty}\big(G(F)\backslash G(\mathbb{A}_{F})\big)$. An example of this is given by the [[Segal-Shale-Weil representation]] and the formation of [[theta series]].

Once one has obtained the theta series, one may investigate the following:

* The integral of the theta series against an automorphic form. This is related to periods of L-functions.

* The projection of the $L^{2}$-norm of the theta series to an automorphic representation. This is related to the relative trace formula. 

## References

* [[David Ben-Zvi]], [[Yiannis Sakellaridis]], [[Akshay Venkatesh]], _Relative Langlands duality_ ([arXiv: 2409.04677](https://arxiv.org/abs/2409.04677))

* [[David Ben-Zvi]], _Relative Geometric Langlands Duality_ ([MSRI lectures](https://www.msri.org/workshops/918/schedules/28232))

* [[David Ben-Zvi]], _Relative Langlands_ ([pdf](https://www.msri.org/workshops/918/schedules/28233/documents/50487/assets/88599))

* [[Yiannis Sakellaridis]], _Spherical Varieties, Functoriality, and Quantization_ ([arXiv:2111.03004](https://arxiv.org/abs/2111.03004))

* {#Sakellaridis2021}[[Yiannis Sakellaridis]], _Hamiltonian Spaces and Periods of Automorphic Forms_ ([slides](https://math.jhu.edu/~sakellar/KAST.pdf))

* Raphael Beuzart-Plessis, _The Relative Langlands Program_ ([YouTube] (https://www.youtube.com/watch?v=J4xgPDJCymw)) ([Part 2] (https://www.youtube.com/watch?v=w4qn_WCb0bk)) ([Part 3] (https://www.youtube.com/watch?v=0rXaBG58YEs))



