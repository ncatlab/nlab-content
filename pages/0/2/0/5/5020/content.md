
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

One analog in [[(∞,1)-category theory]] of _[[epimorphism]]_ in [[category theory]]. Beware that there are other variants such as _[[effective epimorphism in an (infinity,1)-category]]_ and generally the concept of _[[n-epimorphism]]_.

## Definition

For $C$ an [[(∞,1)-category]], a [[morphism]] $f \colon X \to Y$ in $\mathcal{C}$ is an **epimorphism** if for all [[objects]] $A \in \mathcal{C}$ the induced morphism on [[hom infinity-groupoids|hom $\infty$-groupoids]]

$$
  \mathcal{C}(f,A) 
  \,\colon\, 
  \mathcal{C}(Y,A) 
    \xhookrightarrow{\;\;}
  \mathcal{C}(X,A)
$$

is a [[monomorphism in an (∞,1)-category|monomorphism in]] [[∞Grpd]].


## Examples
 {#Examples}

* A morphism $A \to B$ of [[E-infinity rings]] is an epimorphism iff $B$ is [[smashing localization|smashing]] over $A$, i.e., if $ B \wedge_A B \approx B$.

* A morphism $X\to Y$ between [[connected spaces]] is an epimorphism iff $Y$ is formed via a [[Quillen plus construction]] from a [[perfect group|perfect]] [[normal subgroup]] of the [[fundamental group]] $\pi_1(X)$.  

  More generally, a map of spaces is an epi iff all its fibers are acyclic spaces in the sense that their [[suspensions]] are [[contractible]].  This is discussed in [Raptis 17](#Raptis17).

* A generalization of this to epimorphisms and acyclic spaces in [[(infinity,1)-toposes]] is discussed in [Hoyois 19](#Hoyois19).

## References

* {#Raptis17} [[George Raptis]], *Some characterizations of acyclic maps*, Journal of Homotopy and Related Structures volume 14, pages 773–785 (2019) 2017 ([arxiv:1711.08898](https://arxiv.org/abs/1711.08898), [doi:10.1007/s40062-019-00231-6](https://doi.org/10.1007/s40062-019-00231-6))

* {#Hoyois19} [[Marc Hoyois]], *On Quillen's plus construction*, 2019 ([pdf](http://www.mathematik.ur.de/hoyois/papers/acyclic.pdf))


[[!redirects epimorphisms in an (infinity,1)-category]]

[[!redirects epimorphism in an (∞,1)-category]]
[[!redirects epimorphisms in an (∞,1)-category]]

[[!redirects epimorphism in an infinity1-category]]
