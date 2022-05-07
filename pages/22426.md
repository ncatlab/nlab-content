
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--


#Contents#
* tabla of contents
{:toc}

## Idea

The *Kendall tau distance* between two [[permutations]] is the [[minimum]] [[natural number|number]] of [[transpositions]] (swaps) of *adjacent* elements needed to turn one into the other.

(This is in contrast to the [[Cayley distance]] which counts the minimum number of [[transpositions]] of any pairs of elements, not necessarily adjacent.)



## Definition

For $n \in \mathbb{N}$ consider the [[symmetric group]] $Sym(n)$ with its [[mathematical structure|structure]] as a [[finitely generated group]] exhibited by the [[finite set]] of [[generators]] given by the *adjacent* [[transposition permutations]]

$$
  Gen
  \;\coloneqq\;
  \big\{
    \sigma_{i,i+1}
    \,\vert\,
    1 \leq i \lt n
  \big\}
  \;\subset\;
  Sym(n)
  \,.
$$

Then the *Kendall tau distance* ([Kendall 1938](#Kendall1938), see also [Diaconis 88, p. 112](#Diaconis88)) is the [[distance]] on $Sym(n)$ which is the [[graph distance]] of the corresponding [[Cayley graph]], hence the [[function]] 

$$
  d_K(-,-)
  \;\colon\;
   Sym(n) \times Sym(n)
 \longrightarrow
 \mathbb{N}
    \hookrightarrow
  \mathbb{R} 
$$

which sends any [[pair]] of [[permutations]] $\sigma_1, \sigma_2 \in Sym(n)$ to the [[minimum]] [[number]] $d(\sigma_1, \sigma_2) \in \mathbb{N}$ of adjacent [[transpositions]] $\sigma_{i_1, i_1 + 1}, \sigma_{i_2, i_2 + 1}, \cdots, \sigma_{i_d, i_d+1}$ such that 

$$
  \sigma_2
  \;=\;
  \sigma_{i_d, i_d+1}
  \circ
  \cdots
  \circ
  \sigma_{i_2, i_2 + 1}
  \circ
  \sigma_{i_1, i_1 + 1}
  \circ
  \sigma_1
  \,.
$$

The [[exponential]] of minus this distance is known as the *Mallows kernel*:

\[
  \label{MallowsKernel}
  (\sigma_1,\sigma_2)
  \;\mapsto\;
  \exp
  \big(
    - d_K(\sigma_1, \sigma_2)
  \big)
\]

## Properties


\begin{theorem}
The Mallows kernel (eq:MallowsKernel) is [[positive definite bilinear form|positive definite]].
\end{theorem}

([Jiao-Vert 18, Theorem 1](#JiaoVert18))

## Related concepts

* [[Cayley distance]]

* [[Mallows kernel]]

* [[kernel method]]

## References

The distance function is due to:

* {#Kendall1938} [[Maurice Kendall]], *A new measure of rank correlation*, Biometrika, Volume 30, Issue 1-2, June 1938, Pages 81–93 ([doi:10.1093/biomet/30.1-2.81](https://doi.org/10.1093/biomet/30.1-2.81))

The corresponding exponential kernel is named after

* [[C. L. Mallows]], *Non-Null Ranking Models. I*,  Biometrika Vol. 44, No. 1/2 (Jun., 1957), pp. 114-130 ([jstor:2333244](https://www.jstor.org/stable/2333244))

Textbook account:

* {#Diaconis88} [[Persi Diaconis]], Chapter 6B of: *Group Representations  in Probability  and  Statistics*, Lecture Notes - Monographs Series, Institute of Mathematical Statistics 1988 ([pdf](https://jdc.math.uwo.ca/M9140a-2012-summer/Diaconis.pdf))

See also:

* Wikipedia, *[Kendall tau distance](https://en.wikipedia.org/wiki/Kendall_tau_distance)*

Review and [[proof]] that the exponentiated negative Kendall tau distance (the [[Mallows kernel]]) is a [[positive definite bilinear form]]:

* {#JiaoVert18} [[Yunlong Jiao]], [[Jean-Philippe Vert]], *The Kendall and Mallows Kernels for Permutations*, IEEE Transactions on Pattern Analysis and Machine Intelligence, vol. 40, no. 7, pp. 1755-1769, 1 July 2018 ([doi:10.1109/TPAMI.2017.2719680](https://doi.org/10.1109/TPAMI.2017.2719680), [hal:01279273](https://hal.archives-ouvertes.fr/hal-01279273/document))

Discussion of weighted variants:

* [[Yunlong Jiao]], [[Jean-Philippe Vert]], *The Weighted Kendall and High-order Kernels for Permutations*, Proceedings of the 35th International Conference on Machine Learning, PMLR 80:2314-2322, 2018 ([arXiv:1802.08526](https://arxiv.org/abs/1802.08526), [mlr:v80/jiao18a](http://proceedings.mlr.press/v80/jiao18a.html), [hal:hal-01717385](https://hal.inria.fr/hal-01717385))



[[!redirects Kendall tau distances]]

[[!redirects Kendall distance]]
[[!redirects Kendall distances]]

[[!redirects Kendall kernel]]
[[!redirects Kendall kernels]]

[[!redirects Mallows kernel]]
[[!redirects Mallows kernels]]


