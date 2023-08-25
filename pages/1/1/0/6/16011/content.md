

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

The term _heteromorphism_ ([Ellerman 2006](#Ellerman06), [Ellerman 2007](#Ellerman07)) refers to concept of a [[morphism]] not (necessarily) between two [[objects]] in the same [[category]], but between objects in two different categories that are related by a [[functor]], and typically by an [[adjoint functor]], in which case the notion is first made explicit in [Pareigis 1970, §2.2](#Pareigis70). Indeed, sets of heteromorphism may be used to characterize [[adjoint functors]]. Generally, the set of heteromorphisms is that assigned by the corresponding [[profunctor]] to the pair of objects.

The concept is also known as the *[[cograph of a functor]]*. While in traditional [[category theory]] literature this is maybe somewhat neglected, it serves for instance as the very definition of [[adjoint (infinity,1)-functors|adjoint $(\infty,1)$-functor]] in the context of [[quasi-categories]] in [Lurie 2009](#Lurie09)) (without using the term "heteromorphism" there).


## Definition

Given two [[categories]] $\mathcal{C}$ and $\mathcal{D}$ and a [[functor]] $L \colon \mathcal{C} \to \mathcal{D}$, then for $c\in \mathcal{C}$ and $d \in \mathcal{D}$ two [[objects]], the set of _heteromorphisms_ between them is the [[hom set]]

$$
  Het(c,d) \coloneqq \mathcal{D}\big(L(c),d\big)
  \,.
$$

When $L$ has a [[right adjoint]] $R \colon \mathcal{D}\to \mathcal{C}$ then this is of course equivalent to 

$$
  Het(c,d) \cong \mathcal{C}\big(c,R(d)\big)
  \,.
$$

More generally, for $Het \colon \mathcal{C}^{op}\times \mathcal{D}\to Set$ a [[profunctor]] from $\mathcal{C}$ to $\mathcal{D}$, then $Het(c,d)$ may be called its set of heteromorphisms from $c$ to $d$.

A pair of [[adjoint functors]] arise when a Het profunctor is a [[representable functor]] on both the left and right. The [[left adjoint]] is representing functor on the left:
$$
  \mathcal{D}\big(L(c),d\big) \cong  Het(c,d)
  \,
$$
and symmetrically the [[right adjoint]] is the representing functor on the right:
$$
  Het(c,d) \cong \mathcal{C}\big(c,R(d)\big)
  \,.
$$

Putting the two representations together gives the usual natural isomorphism characterization of a [[adjunction]] but with the het middle term:
$$
\mathcal{D}\big(L(c),d\big) \cong  Het(c,d) \cong \mathcal{C}\big(c,R(d)\big)
\,.
$$

## Properties

### Characterization of adjunctions

Heteromorphisms may be used to express/characterize [[adjunctions]]. For more on this see at

* [adjoint functor -- In terms of cographs/heteromorphisms](adjoint+functor#InTermsOfCographsHeteromorphisms)

* _[adjoint (infinity,1)-functor -- In terms of cographs/Heteromorphisms](adjoint+%28infinity%2C1%29-functor#InTermsOfCographsHeteromorphisms)_

## References

* {#Pareigis70} [[Bodo Pareigis]], section 2.2 in: *Categories and Functors*, Pure and Applied Mathematics **39**, Academic Press (1970) &lbrack;[doi:10.5282/ubm/epub.7244](https://doi.org/10.5282/ubm/epub.7244)&rbrack;

* {#Ellerman06} [[David Ellerman]], _A Theory of Adjoint Functors --- with Some Thoughts on Their Philosophical Significance_, in: G. Sica (e.) _What Is Category Theory?_, 12783. Milan: Polimetrica. (2006)

* {#Ellerman07} [[David Ellerman]], _Adjoint Functors and Heteromorphisms_ &lbrack;[arXiv:0704.2207](http://arxiv.org/abs/0704.2207)&rbrack;

* [[David Ellerman]], *Mac Lane, Bourbaki, and Adjoints: A Heteromorphic Retrospective* (2015) &lbrack;[pdf](http://www.ellerman.org/wp-content/uploads/2015/06/Maclane-Bourbaki-Redux.pdf), [doi:10.2139/ssrn.2620333](https://dx.doi.org/10.2139/ssrn.2620333)&rbrack;

* {#Lurie09} [[Jacob Lurie]], _[[Higher Topos Theory]]_, Annals of Mathematics Studies **170**, Princeton University Press (2009) &lbrack;[pup:8957](https://press.princeton.edu/titles/8957.html), [arXiv:0608040](http://arxiv.org/abs/math/0608040)&rbrack

[[!redirects heteromorphisms]]

