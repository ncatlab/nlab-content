+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

* table of contents
{: toc}

## Definition

Recall that a [[locally small category]] $\mathcal{K}$ is [[total category|total]] if its [[Yoneda embedding]] $Y\colon\mathcal{K}\longrightarrow [\mathcal{K}^{op},Set]$ has a [[left adjoint]] $X$.

+-- {: .num_defn}
###### Definition

A total category $\mathcal{K}$ is **totally distributive** if $X \colon [\mathcal{K}^{op},Set] \longrightarrow \mathcal{K}$ has a further [[left adjoint]] $W$.

$$
  (W \dashv X \dashv Y)
  \;\colon\;
  \mathcal{K}
   \stackrel{\overset{W}{\hookrightarrow}}{\stackrel{\overset{X}{\leftarrow}}{\underset{Y}{\hookrightarrow}}}
  PSh(\mathcal{K})
  \,.
$$

=--


## Properties

If $\mathcal{K}$ is totally distributive, then since $Y$ is [[full and faithful functor|fully faithful]], then, by the properties of [[adjoint triples]], so is $W$.  Thus, $\mathcal{K}$ is a [[coreflective subcategory]] of $[\mathcal{K}^{op},Set]$, which is cototal (or more precisely, [[pro-cototal category|pro-cototal]], since it is not locally small) --- hence $\mathcal{K}$ is also cototal.

Moreover this means that the induced [[adjoint pair]] of ([[comonad|co]]-)[[monads]]

$$
  W X \dashv  Y X \;\colon\; PSh(\mathcal{K}) \leftrightarrow PSh(\mathcal{K})
$$

is an [[adjoint modality]].

Every totally distributive category is an example of a [[completely distributive category]].

## Examples

* If $C$ is a [[small category]], then its [[presheaf category]] $[C^{op},Set]$ is totally distributive.

* If $\mathcal{K}$ is totally distributive and $\mathcal{L}\subseteq \mathcal{K}$ is a full [[subcategory]] that is both [[reflective subcategory|reflective]] and [[coreflective subcategory|coreflective]], then $\mathcal{L}$ is totally distributive.

## Waves

For any total category, it is possible to define the functor $W:\mathcal{K} \to [\mathcal{K}^{op},Set]$ which "wants to be" the left adjoint of $X$. The elements of $W(A)(K)$ are called **waves** from $K$ to $A$ (just because they are usually denoted by wavy arrows), and as in the case of [[continuous categories]] they form an [[idempotent comonad]] on $\mathcal{K}$ in the [[bicategory]] of [[profunctors]]. A total category is totally distributive if and only if $W \dashv X$.

## Related pages

* [[distributive category]]

* [[completely distributive category]]

* Totally distributive categories are "almost" an example of [[continuous algebras]] for a [[lax-idempotent 2-monad]].

## References

* [[Robert Rosebrugh]], [[Richard J. Wood]], *An adjoint characterization of the category of sets*. PAMS **122** 2 (1994) 409-413 &lbrack;[jstor:2161031](https://www.jstor.org/stable/2161031)&rbrack;

* Rory Lucyshyn-Wright, *Totally distributive toposes*.  [spnet](https://selectedpapers.net/arxiv/1108.4032).

* [[Francisco Marmolejo]], [[Bob Rosebrugh]], and [[Richard Wood]], *Completely and totally distributive categories I*, JPAA 216 no. 8-9 (2012).  [PDF](http://www.mta.ca/~rrosebru/articles/ctd.pdf)

* [[Richard J. Wood]], "The waves of a total category." Theory and Applications of Categories 30.47 (2015): 1624-1646.

[[!redirects totally distributive categories]]
