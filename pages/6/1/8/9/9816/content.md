
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _K-orientation_ is an [[orientation in generalized cohomology]] for [[K-theory]].

## Definition

### In topological K-theory

For ordinary [[topological K-theory]] a [[smooth function]] between [[smooth manifolds]] $f \colon X \to Y$ is K-oriented if $T X \oplus f^\ast(T Y)$ has a [[spin^c structure]].

In this case there is an [[Umkehr map]]

$$
  f_! \colon K^\bullet(X) \to K^{\bullet + dim(Y) - dim(X)}(Y)
  \,.
$$

### In KK-theory

In the context of [[KK-theory]], a morphism $f \colon A \to B$ of [[C*-algebra]], a _K-orientation_ of this morphism is a map

$$
  f! \in KK_d(B,A)
$$

such that (...). The corresponding [[fiber integration]]/[[Gysin map]] on [[operator K-theory]] is then the postcomposition operation

$$
  f_! \colon K_\bullet(B) \simeq KK_\bullet(\mathbb{C}, B) \stackrel{f! \circ (-)}{\to} KK_\bullet(\mathbb{C}, A) \simeq K_{\bullet + d}(A)
  \,.
$$

([BMRS 07](#BMRS07))

## Related concepts

* [[spin^c structure]]

* [[Grothendieck-Riemann-Roch theorem]]

## References

Discussion in [[noncommutative topology]]/[[KK-theory]] is in 

* [[Alain Connes]], , [[Georges Skandalis]], _The longitudinal index theorem for foliations_. Publ. Res. Inst. Math. Sci. 20,
no. 6, 1139&#8211;1183 (1984)
 {#ConnesSkandalis84}

* Jacek Brodzki, [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]], _Noncommutative correspondences, duality and D-branes in bivariant K-theory_, Adv. Theor. Math. Phys.13:497-552,2009 ([arXiv:0708.2648](http://arxiv.org/abs/0708.2648))
 {#BMRS07}


[[!redirects K-orientations]]

[[!redirects KU-orientation]]
[[!redirects KU-orientations]]
