
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition


+-- {: .un_theorem}
###### Theorem

Let 

* $\mathcal{E}$ be a [[cofibrantly generated model category|cofibrantly generated]] [[symmetric monoidal category|symmetric]] [[monoidal model category]];

* $P$ an admissible $\Sigma$-cofibrant [[operad]] in $\mathcal{E}$ (see [[model structure on operads]]);

* $A$ a cofibrant $P$-algebra (see [[model structure on algebras over an operad]]).

Then then category $Mod_P(A)$ of [[modules over an algebra over an operad]] carries the [[transferred model structure]] along the [[forgetful functor]]
$U : Mod_P(A) \to \mathcal{E}$.

Every [[morphism]] of cofibrant $P$-algebras $f : A \to B$ induced a [[Quillen adjunction]]

$$
  (f_! \dashv f^*) : Mod_P(B) \stackrel{\overset{f_!}{\leftarrow}}{\underset{f^*}{\to}} Mod_P(A)
$$

which is a [[Quillen equivalence]] if $f$ is a weak equivalence.
=--

This is ([BergerMoerdijk, theorem 2.6](#BergerMoerdijk)).


## References


* [[Clemens Berger]], [[Ieke Moerdijk]], _On the derived category of an algebra over an operad_ ([arXiv](http://arxiv.org/abs/0801.2664))
{#BergerMoerdijk}