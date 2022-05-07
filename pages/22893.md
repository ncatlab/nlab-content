
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given a pair of [[adjoint functors]]

$$
  \mathcal{D}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\;\;\;\;\bot\;\;\;\;}
  \mathcal{C}
$$

there is induced an [[adjunction]] of [[opposite functors]]  between their [[opposite categories]] of the form

$$
  \mathcal{D}^{op}
    \underoverset
      {\underset{L^{op}}{\longrightarrow}}
      {\overset{R^{op}}{\longleftarrow}}
      {\;\;\;\;\bot\;\;\;\;}
  \mathcal{C}^{op}
  \,.
$$

Hence where $L$ was the [[left adjoint]], its [[opposite functor|opposite]] becomes the [[right adjoint]], and dually for $R$.

This is immediate from the definition of [[opposite categories]] and the characterization of adjoint functors via the corresponding [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism).

The [[adjunction unit]] of the opposite adjunction has as components the components of the original [[adjunction counit]], regarded in the opposite category, and dually:

$$
  \epsilon^{R^{op} C^{op}}_{d}
  \;\colon\;
  R^{op}\circ L^{op}(d)
  \xrightarrow{\;\;  \big( \eta^{R L}_d \big)^{op}  \;\;}
  d
  \,,
  {\phantom{AAAAAA}}
  \eta^{L^{op} R^{op}}_{c}
  \;\colon\;
  c
  \xrightarrow{\;\;  \big( \epsilon^{L R}_c \big)^{op}  \;\;}
  L^{op} \circ R^{op}(c)
  \,.
$$



## Related concepts

* [[opposite Quillen adjunction]]

* [[opposite category]], [[opposite functor]]

* [[adjunction]]

* [[opposite 2-category]]


[[!redirects opposite adjunctions]]

[[!redirects opposite adjoint functor]]
[[!redirects opposite adjoint functors]]

[[!redirects adjoint opposite functor]]
[[!redirects adjoint opposite functors]]


