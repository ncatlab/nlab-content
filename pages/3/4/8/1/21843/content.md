

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The [[cobordism cohomology theory]] for [[special unitary group]]-[[G-structure|structure]].

## Properties

+-- {: .num_prop #SUBordismRingAwayFromTwo}  
###### Proposition
**(SU-Bordism ring away from 2 is polynomial)**

The [[SU-bordism ring]] with [[localization of a ring|2 inverted]] is the [[polynomial algebra]] over $\mathbb{Z}\big[\tfrac{1}{2}\big]$ on one generator in every even degree $\geq 4$:

$$
  \Omega^{SU}\big[\tfrac{1}{2}\big]
  \;\simeq\;
  \mathbb{Z}
  \big[
    \tfrac{1}{2}
  \big]
  \big[
    \{
      y_{2i+4}
    \}_{i \in \mathbb{N}}
  \big]
  \,.
$$

=--

(due to [Novikov 62](#Novikov62), review in [LLP 17, Thm. 1.2](#LLP17))

+-- {: .num_prop #K3SurfaceSpansSUBordismRingInDegree4}  
###### Proposition
**([[K3-surface]] spans [[SU-bordism ring]] in degree 4)**

The degree-4 generator $y_4 \in \Omega^{SU}_4$ in the [[SU-bordism ring]] (Prop. \ref{SUBordismRingAwayFromTwo}) is represented by minus the class of any (non-[[torus]]) [[K3-surface]]:

$$
  \Omega^{SU}_4 \;\simeq\; \mathbb{Z}\big[ \tfrac{1}{2}\big]\big\langle -[K3] \big\rangle
  \,.
$$

=--

([LLP 17, Lemma 1.5, Example 3.1](#LLP17), [CLP 19, Theorem 13.5a](#CLP19))


+-- {: .num_prop }  
###### Proposition
**([[Calabi-Yau manifold|Calabi-Yau n-folds]] for $2 \leq n \leq 4$ span [[SU-bordism ring]] in degrees $4 \leq d \leq 8$)**

The [[SU-bordism ring]] up to degree 8 is spanned by classes of [[Calabi-Yau manifolds]]: the [[K3 surface]] from Prop. \ref{K3SurfaceSpansSUBordismRingInDegree4} in degree 4 and certain CY 3-folds and CY4-folds in degrees 6 and 8.

=--

([CLP 19, Theorem 13.5](#CLP19))

For more see at _[[Calabi-Yau manifolds in SU-bordism theory]]_.

## Related concepts

* [[Calabi-Yau manifold]]


\linebreak

[[!include flavours of cobordism cohomology theories -- table]]




## References

* {#Novikov62} [[Sergei Novikov]], _Homotopy properties of Thom complexes_, Mat. Sbornik 57 (1962), no. 4, 407–442, 407&#8211;442 ([pdf](http://www.mi-ras.ru/~snovikov/6.pdf), [[NovikovThomComplexes.pdf:file]])

Relation to [[Calabi-Yau manifolds]]:

* {#LLP17} [[Ivan Limonchenko]], [[Zhi Lu]], [[Taras Panov]], _Calabi-Yau hypersurfaces and SU-bordism_, Proceedings of the Steklov Institute of Mathematics 302 (2018), 270-278 ([arXiv:1712.07350](https://arxiv.org/abs/1712.07350))

Survey:

* {#CLP19} Georgy Chernykh, [[Ivan Limonchenko]], [[Taras Panov]], _$SU$-bordism: structure results and geometric representatives_, Russian Math. Surveys 74 (2019), no. 3, 461-524 ([arXiv:1903.07178](https://arxiv.org/abs/1903.07178))

* [[Taras Panov]], _A geometric view on $SU$-bordism_, talk at Moscow State University 2020 ([webpage](https://www.math.princeton.edu/events/geometric-view-su-bordism-2020-09-17t170000), [pdf](http://higeom.math.msu.su/people/taras/talks/2019SPb-Panov.pdf), [[PanovSU-Bordism.pdf:file]])




[[!redirects SU-bordism]]
[[!redirects SU-bordism theory]]


[[!redirects SU-cobordism]]
[[!redirects SU-cobordism theory]]

[[!redirects special unitary bordism ring]]
[[!redirects special unitary bordism rings]]

[[!redirects SU-bordism ring]]
[[!redirects SU-bordism rings]]

[[!redirects special unitary cobordism ring]]
[[!redirects special unitary cobordism rings]]

[[!redirects SU-cobordism ring]]
[[!redirects SU-cobordism rings]]



