+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--



# Contents
* table of contents
{:toc}

## Idea

In the context of [[2-category theory]], the concept of a **2-pro-object** is the [[categorification]] of the concept of a [[pro-object]]. A 2-pro-object in a 2-category, $\mathcal{C}$, is a 2-functor (or diagram) indexed by a 2-cofiltered 2-category. These 2-pro-objects form a 2-category, $2Pro(\mathcal{C})$, which is closed under small 2-cofiltered pseudolimits.

Pre-composition with the inclusion $c:\mathcal{C} \to 2Pro(\mathcal{C})$ is an [[equivalence of 2-categories]]:
$$
c^{\ast}: Hom(2Pro(\mathcal{C}),Cat)_+ \to Hom(\mathcal{C},Cat),
$$
where $Hom(2Pro(\mathcal{C}),Cat)_+$ is the full subcategory whose objects are those 2-functors that preserve small 2-cofiltered pseudolimits ([Descotte &amp; Dubuc, Thrm 2.4.2](#DescotteDubuc)).

## References

* {#DescotteDubuc} [[Maria Emilia Descotte]], [[Eduardo Dubuc]], _A theory of 2-pro-objects (with expanded proofs)_, ([arXiv:1406.5762](https://arxiv.org/abs/1406.5762))

* [[Maria Emilia Descotte]], _A theory of 2-pro-objects, a theory of 2-model 2-categories and the 2-model structure for 2-Pro(C)_, ([arXiv:2010.10636](https://arxiv.org/abs/2010.10636))