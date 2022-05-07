
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

Then the *Kendall tau distance*  is the [[distance]] on $Sym(n)$ which is the [[graph distance]] of the corresponding [[Cayley graph]], hence the [[function]] 

$$
  d(-,-)
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

## References

Review and [[proof]] that the exponentiated negative Kendall tau distance (the [[Mallows kernel]]) is a [[positive definite bilinear form]]:

* [[Yunlong Jiao]], [[Jean-Philippe Vert]], *The Kendall and Mallows Kernels for Permutations*, IEEE Transactions on Pattern Analysis and Machine Intelligence, vol. 40, no. 7, pp. 1755-1769, 1 July 2018 ([doi:10.1109/TPAMI.2017.2719680](https://doi.org/10.1109/TPAMI.2017.2719680), [hal:01279273](https://hal.archives-ouvertes.fr/hal-01279273/document))

See also

* Wikipedia, *[Kendall tau distance](https://en.wikipedia.org/wiki/Kendall_tau_distance)*

[[!redirects Kendall tau distances]]

[[!redirects Kendall distance]]
[[!redirects Kendall distances]]

[[!redirects Kendall kernel]]
[[!redirects Kendall kernels]]

[[!redirects Mallows kernel]]
[[!redirects Mallows kernels]]


