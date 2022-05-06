

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Write $\mathbb{S}$ for the [[sphere spectrum]] and _[[tmf]]_ for the [[connective spectrum]] of [[topological modular forms]].

Since [[tmf]] is an [[E-∞ ring|E-∞]][[ring spectrum]], there is an essentially unique homomorphism of [[E-∞ ring|E-∞]][[ring spectra]]

$$
  \mathbb{S}
  \overset{e_{tmf}}{\longrightarrow}
  tmf
  \,.
$$

Regarded as a morphism of [[generalized homology]]-theories, this is called the [[Hurewicz homomorphism]], or rather the [[Boardman homomorphism]] for $tmf$

## Properties

+-- {: .num_prop}
###### Proposition
**(Boardman homomorphism in $tmf$ is 6-connected)**

The [[Boardman homomorphism in tmf]]

$$
  \mathbb{S}
  \overset{e_{tmf}}{\longrightarrow}
  tmf
$$

induces an [[isomorphism]] on [[stable homotopy groups]] 
(hence from the [[stable homotopy groups of spheres]] to the stable homotopy groups of tmf), up to degree 6:

$$
  \pi_{\bullet \leq 6}(\mathbb{S})
  \underoverset{\simeq}{\pi_{\bullet \leq 6}(e_{tmf})}{\longrightarrow}
  \pi_{\bullet\leq 6}(tmf)
  \,.
$$


=--

([Hopkins 02, Prop. 4.6](#Hopkins02), [DFHH 14, Ch. 13](#DFHH14))

## Related concepts

* [[stable cohomotopy]]

## References

* {#Hopkins02} [[Michael Hopkins]], section 4 of _Algebraic topology and modular forms_, Proceedings of the ICM, Beijing 2002, vol. 1, 283--309 ([arXiv:math/0212397](http://arxiv.org/abs/math/0212397))


* {#DFHH14} [[Christopher Douglas]], [[John Francis]], [[André Henriques]], [[Michael Hill]], Chapter 13 of: _Topological Modular Forms_, Mathematical Surveys and Monographs Volume 201, AMS 2014  ([ISBN:978-1-4704-1884-7](https://bookstore.ams.org/surv-201))

