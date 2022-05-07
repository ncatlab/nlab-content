

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
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

__Homotopy weighted colimits__ (alias __weighted homotopy colimits__)
are the analog of [[weighted colimits]] in [[homotopy theory]].

## In relative categories

\[ ... \]

## In model categories

For the special case of [[model categories]], we can define homotopy weighted colimits as follows.

Fix a [[monoidal model category]] $V$,
a $V$-[[enriched model category]] $C$,
and a small $V$-[[enriched category]] $J$.

For simplicity, assume all [[enriched hom]] objects of $J$ are [[cofibrant]].
If this is not the case, we can first cofibrantly replace $J$
in the [[Dwyer-Kan model structure on enriched categories]].

We have a [[left Quillen bifunctor]]
$$V^{J^{op}} \times C^J \to C$$
given by the ordinary [[weighted colimit]] functor.

The _homotopy weighted colimit_ can then be defined
as the [[left derived]] [[Quillen bifunctor]] of the weighted colimit functor.

## References

See Section 9.2 in

* [[Emily Riehl]], _[[Categorical Homotopy Theory]]_, New Mathematical Monographs 24, Cambridge University Press, 2014.

Other references:

* [[Lukáš Vokřínek]], _Homotopy weighted colimits_, [arXiv:1201.2970](https://arxiv.org/abs/1201.2970).

* [[Nicola Gambino]], _Weighted limits in simplicial homotopy theory_, Journal of Pure and Applied Algebra 214:7 (2010), 1193–1199.  [doi](https://doi.org/10.1016/j.jpaa.2009.10.006).

* [[Michael Shulman]], _Homotopy limits and colimits and enriched homotopy theory_, [arXiv:math/0610194](https://arxiv.org/abs/math/0610194).

* [[Sergey Arkhipov]], [[Sebastian Ørsted]], _Homotopy (co)limits via homotopy (co)ends in general combinatorial model categories_, [arXiv:1807.03266](https://arxiv.org/abs/1807.03266).


[[!redirects homotopy weighted colimits]]
[[!redirects weighted homotopy colimit]]
[[!redirects weighted homotopy colimits]]
