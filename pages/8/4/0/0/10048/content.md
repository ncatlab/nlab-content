# Totally distributive categories

* table of contents
{: toc}

## Definition

Recall that a [[locally small category]] $\mathcal{K}$ is [[total category|total]] if its [[Yoneda embedding]] $Y:\mathcal{K}\to [\mathcal{K}^{op},Set]$ has a [[left adjoint]] $X$.

+-- {: .un_defn}
###### Definition
A total category $\mathcal{K}$ is **totally distributive** if $X:[\mathcal{K}^{op},Set] \to \mathcal{K}$ has a further left adjoint $W$.
=--

## Properties

If $\mathcal{K}$ is totally distributive, then since $Y$ is fully faithful, by the properties of [[adjoint triples]], so is $W$.  Thus, $\mathcal{K}$ is a coreflective subcategory of $[\mathcal{K}^{op},Set]$, which is cototal (or more precisely, [[pro-cototal category|pro-cototal]], since it is not locally small) --- hence $\mathcal{K}$ is also cototal.

## Examples

* If $C$ is small, then the presheaf category $[C^{op},Set]$ is totally distributive.

* If $\mathcal{K}$ is totally distributive and $\mathcal{L}\subseteq \mathcal{K}$ is a full [[subcategory]] that is both [[reflective subcategory|reflective]] and [[coreflective subcategory|coreflective]], then $\mathcal{L}$ is totally distributive.

## Waves

By the [[adjoint functor theorem]] for total categories, a total category is totally distributive if and only if the functor $X$ preserves all limits.  Moreover, for any total category, it is possible to define the functor $W:\mathcal{K} \to [\mathcal{K}^{op},Set]$ which ought to be the left adjoint of $X$.  The elements of $W(A)(K)$ are called **waves** from $K$ to $A$, and as in the case of [[continuous categories]] they form an [[idempotent comonad]] on $\mathcal{K}$ in the [[bicategory]] of [[profunctors]].

## References

* R. Rosebrugh and R.J. Wood. *An adjoint characterization of the category of sets*. PAMS, Vol. 122, No. 2, 409&#8211;413, 1994.

* Rory Lucyshyn-Wright, *Totally distributive toposes*.  [spnet](https://selectedpapers.net/arxiv/1108.4032).

* [[Francisco Marmolejo]], [[Bob Rosebrugh]], and [[Richard Wood]], *Completely and totally distributive categories I*, JPAA 216 no. 8-9 (2012).  [PDF](http://www.mta.ca/~rrosebru/articles/ctd.pdf&#8206;)

[[!redirects totally distributive categories]]
