
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of *enriched monoidal categories* is a compatible combination of the notions of *[[enriched categories]]* and *[[monoidal categories]]*. The main point is that the [[tensor product]]-[[functor]] on the [[underlying]] [[monoidal category]] is properly an [[enriched functor]] with respect to the [[underlying]] [[enriched category]].

Special cases include [[tensor categories]], which are ([[Vect]],[[tensor product of vector spaces|$\otimes$]])-enriched monoidal categories.

## Definition

### The monoidal 2-category of enriched categories

For $V$ a *[[braided monoidal category|symmetric monoidal]]* [[cosmos]],  the [[2-category]] [[VCat]] of $V$-[[enriched categories]] becomes a [[monoidal 2-category]] by declaring the [[tensor product]] $\mathbf{C} \otimes \mathbf{D}$ of a [[pair]] $\mathbf{C}$, $\mathbf{D}$ of $V$-[[enriched categories]] to have

* as [[set]] of [[objects]] the [[cartesian product]] of the given sets of objects:
  
  $$
    Obj(\mathbf{C} \otimes \mathbf{D}) 
      \;\coloneqq\;
    Obj(\mathbf{C}) \times Obj(\mathbf{D})
  $$

* as [[hom-objects]] the [[tensor product]] in $V$ between the given [[hom-objects]]:

  $$
    (\mathbf{C} \otimes \mathbf{D})\big((c,d), (c',d')\big)
    \;\coloneqq\;
    \mathbf{C}(c,c') \otimes \mathbf{D}(d,d')
    \,.
  $$

* [[composition]] obtained by the given composition operations, after using the [[braiding]] in $V$ to align factors:

  $$
    \array{
      (\mathbf{C} \otimes \mathbf{D})
        \big((c',d'), (c'', d'')\big)
      \otimes
      (\mathbf{C} \otimes \mathbf{D})
        \big((c,d), (c',d')\big)
      &\overset
         {\circ_{\mathbf{C} \otimes \mathbf{D}}}{
        \longrightarrow
        }
       &
      (\mathbf{C} \otimes \mathbf{D})
        \big((c,d), (c'',d'')\big)
      \\
      \mathllap{{}^\simeq}\Big\downarrow
      \phantom{---------}
      &&
      \Big\uparrow\mathrlap{{}^{\simeq}}
      \\
      \mathbf{C}(c',c'') 
        \otimes 
      \mathbf{D}(d',d'')
        \otimes
      \mathbf{C}(c,c') 
        \otimes 
      \mathbf{D}(d,d')
      \underoverset
        {braid}
        {\sim}
        {\to}
      \mathbf{C}(c',c'') 
        \otimes 
      \mathbf{C}(c,c') 
        \otimes
      \mathbf{D}(d',d'')
        \otimes 
      \mathbf{D}(d,d')
      &\overset{
        \circ_{\mathbf{C}} \otimes \circ_{\mathbf{D}}
      }{\longrightarrow}&
      \mathbf{C}(c,c'') \otimes \mathbf{D}(d,d'')
    }
  $$

### Enriched monoidal categories

A $V$-enriched monoidal category $\mathbf{C}$ is a [[pseudomonoid]] [[internalization|internal]] to the above monoidal 2-category $V Cat$.

This means mainly that

* $\mathbf{C}$ is a $V$-[[enriched category]]

* whose [[underlying]] category $C$ is equipped with [[monoidal category]]-[[structure]], hence with a [[tensor product]]-[[functor]]

  $$
    \otimes \,\colon\, C \times C \longrightarrow C
  $$

* which is compatibly lifted for each [[pair]] of [[pairs]] of [[objects]] of $C$ to a [[morphisms]] on [[hom-objects]] in $V$:

  $$  
    \otimes_{\mathbf{C}}\big( (c,d),\, (c',c') \big)
    \,\colon\,
    \mathbf{C}(c,c') \otimes \mathbf{C}(d,d')
    \longrightarrow
    \mathbf{C}(c \otimes_C d ,\, c' \otimes_C d')
  $$ 

in a compatible way.

## Examples

(...)

## Related concepts

* [[cartesian closed enriched category]], [[locally cartesian closed enriched category]]

* [[enriched category]], [[monoidal category]]

* [[enriched monoidal model category]], [[simplicial monoidal model category]]

## References

* [[Jacob Lurie]], Section 1.6 in: *Derived Algebraic Geometry II: Noncommutative Algebra* &lbrack;[arXiv:math/0702299](https://arxiv.org/abs/math/0702299)&rbrack;

  which is Def. 4.1.7.7 in *[[Higher Algebra]]* &lbrack;[pdf](https://www.math.ias.edu/~lurie/papers/HA.pdf)&rbrack;

  > (focus on [[sSet]]-enrichment for [[simplicial monoidal model categories]])

* {#BataninMarkl12} [[Michael Batanin]], [[Martin Markl]], Section 2 of: *Centers and homotopy centers in enriched monoidal categories*, Advances in Mathematics **230** 4–6 (2012) 1811-1858 &lbrack;[doi:10.1016/j.aim.2012.04.011](https://doi.org/10.1016/j.aim.2012.04.011), [arXiv:1109.4084](https://arxiv.org/abs/1109.4084)&rbrack;

* [[Michael Ching]], Def. 1.10 in: *Bar constructions for topological operads and the Goodwillie derivatives of the identity*, Geom. Topol. **9** (2005) 833-934 &lbrack;[arXiv:math/0501429](https://arxiv.org/abs/math/0501429), [doi:10.2140/gt.2005.9.833](http://dx.doi.org/10.2140/gt.2005.9.833)&rbrack;

* [[Rune Haugseng]], answer to *Definitions of enriched monoidal category*, [MO:a/315075](https://mathoverflow.net/a/315075/381) (2018)

* [[Scott Morrison]], [[David Penneys]], *Monoidal Categories Enriched in Braided Monoidal Categories*, International Mathematics Research Notices **2019** 11 June 2019 3527–3579 &lbrack;[doi:10.1093/imrn/rnx217](https://doi.org/10.1093/imrn/rnx217), [arXiv:1701.00567](https://arxiv.org/abs/1701.00567)&rbrack;

* [[Liang Kong]], Wei Yuan, Zhi-Hao Zhang, Hao Zheng, *Enriched monoidal categories I: centers* &lbrack;[arXiv:2104.03121](https://arxiv.org/abs/2104.03121)&rbrack;

[[!redirects enriched monoidal categories]]

[[!redirects monoidal enriched category]]
[[!redirects monoidal enriched categories]]

