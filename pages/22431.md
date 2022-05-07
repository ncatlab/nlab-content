
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The *Cayley distance* between two [[permutations]] is the [[minimum]] [[natural number|number]] of [[transpositions]] of elements needed to turn one into the other.

(This is in contrast to the [[Kendall distance]] which counts the minimum number of [[transpositions]] of *adjacent* pairs of elements.)


## Definition

## Definition

For $n \in \mathbb{N}$ consider the [[symmetric group]] $Sym(n)$ with its [[mathematical structure|structure]] as a [[finitely generated group]] exhibited by the [[finite set]] of [[generators]] given by all [[transposition permutations]]

$$
  Gen
  \;\coloneqq\;
  \big\{
    \sigma_{i,j}
    \,\vert\,
    1 \leq i, j \lt n
  \big\}
  \;\subset\;
  Sym(n)
  \,.
$$

Then the *Cayley distance* (e.g [Diaconis 88, p. 112](#Diaconis88)) is the [[distance]] on $Sym(n)$ which is the [[graph distance]] of the corresponding [[Cayley graph]], hence the [[function]] 

$$
  d_K(-,-)
  \;\colon\;
   Sym(n) \times Sym(n)
 \longrightarrow
 \mathbb{N}
    \hookrightarrow
  \mathbb{R} 
$$

which sends any [[pair]] of [[permutations]] $\sigma_1, \sigma_2 \in Sym(n)$ to the [[minimum]] [[number]] $d(\sigma_1, \sigma_2) \in \mathbb{N}$ of [[transpositions]] $\sigma_{i_1, j_1}, \sigma_{i_2, j_2}, \cdots, \sigma_{i_d, j_d}$ such that 

$$
  \sigma_2
  \;=\;
  \sigma_{i_d, j_d}
  \circ
  \cdots
  \circ
  \sigma_{i_2, j_2}
  \circ
  \sigma_{i_1, j_1}
  \circ
  \sigma_1
  \,.
$$

## References

* {#Diaconis88} [[Persi Diaconis]], Chapter 6B of: *Group Representations  in Probability  and  Statistics*, Lecture Notes - Monographs Series, Institute of Mathematical Statistics 1988 ([pdf](https://jdc.math.uwo.ca/M9140a-2012-summer/Diaconis.pdf))

