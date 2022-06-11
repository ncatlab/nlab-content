
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

##Idea 

Given two maps between homotopy types with a common codomain, $f: A \to X$ and $g: B \to X$, we denote by $A \ast_X B$ the [[pushout]] of their [[pullback]], $A \times_X B$. Then the **join** of $f$ and $g$, written $f \ast g$, is the induced map from $A \ast_X B$ to $X$.

When $X \equiv \mathbf{1}$, the unit type, we write $A \ast_{\mathbf{1}} B$ as $A \ast B$, the join of the two types. 

The join of two maps is the fiberwise join of their respective fibres. 

## Examples

The [[sequential colimit]] $f \ast^{\infty}$ of the join
powers $f \ast^{n}$ is equivalent to the [[image]] inclusion of $f$. 

When $X \equiv \mathbf{1}$, the infinite join power $A \ast^{\infty}$ is the [[propositional truncation]] of $A$.

When $pt: \mathbf{1} \to \mathbf{B} G$, the point in a delooped group, $pt \ast^{\infty}$ is the [[Milnor construction]].

The join of two [[embeddings]] is an embedding, and an embedding is [[idempotent]] for the join construction. 

The unique map of type $\mathbf{0} \to X$ is a unit for the join operation.

The join of two [[mere propositions]], $P \ast Q$, is equal to the [[propositional truncation]] of their sum, $\vert \vert P + Q \vert \vert$.



##Related concepts

* [[join of simplicial sets]]

##References

* {#Rijke17} [[Egbert Rijke]], _[[The join construction]]_ ([arXiv:1701.07538](https://arxiv.org/abs/1701.07538))

