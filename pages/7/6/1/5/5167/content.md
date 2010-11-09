
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

What is called _[[nonabelian cohomology]]_ is the general [[cohomology|intrinsic cohohomology]] of any [[(∞,1)-topos]] $\mathbf{H}$ with coefficients in any object $A \in \mathbf{H}$, not necessarily an [[Eilenberg-MacLane object]].

But there is a general notion of [[Postnikov tower in an (∞,1)-category]] that applies in any [[locally presentable (∞,1)-category]], in particular in [[(∞,1)-topos]]es. 

This implies that every object $A\in \mathbf{H}$ has a decomposition as a sequence of objects

$$
  A \to \cdots \to A_3 \to A_2\to A_1 \to A_0 \to *
  \,,
$$

where $A_k$ is an $k$-[[truncated]] object, in fact the $n$-truncation of $A$.


This implies that every $n$-[[truncated]] [[connected]] object $A$ is given by a possibly nonabelian 0-truncated group object $G$ and a sequence of abelian extensions of the [[delooping]] $\mathbf{B}G$ in that we have [[fiber sequence]]s 

$$
  \mathbf{B}^2 K_1 \to A_2 \to \mathbf{B}G = A_1
$$

etc.

(...)

It follows that any [[cocycle]] $X \to A_2$ decomposes into the [[principal bundle]] classified by $X \to \mathbf{B}G$ and an abelian $\mathbf{B}^2 K$-cocycle on its total space

(...)

## Examples

A [[string structure]] is a nonabelian cocycle with coefficients in the [[string 2-group]]. This is equivalently a $\mathbf{B}U(1)$-cocycle (a [[bundle gerbe]]) on the total space of the underlying $Spin$-[[principal bundle]]. See the section <a href="http://ncatlab.org/nlab/show/string+structure#ClassesOnTotalSpace">In terms of classes on the total space</a>.

## References

The term "Whitehead principle" for nonabelian cohomology is used in 

* [[Bertrand Toën]], _Stacks and non-abelian cohomology_ ([pdf](http://www.math.univ-toulouse.fr/~toen/msri2002.pdf))

