

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea


The [[model category|model structure]] $sPSh(C)$ on [[sSet]]-[[enriched functor category|enriched presheaves]] is supposed to be a [[presentable (infinity,1)-category|presentation]] of the [[(∞,1)-category of (∞,1)-sheaves]] on an [[sSet-site]] $C$.

It generalizes the [[model structure on simplicial presheaves]] which is the special case obtained when $C$ happens to be just an ordinary [[category]].

This means that in as far as the [[model structure on simplicial presheaves]] models [[∞-stack]]s, the model structure on [[sSet]]-[[enriched category|enriched categories]] model [[derived stack]]s.

## Definition 

The construction of the model structure on [[sSet]]-[[enriched category|enriched categories]] closely follows the discussion of the [[model structure on simplicial presheaves]], only that everything now takes place in [[enriched category theory]].

To define the [[model category|model structure]] first consider the ordinary [[category]]

$$
  sPSh(C) := sSet Cat(C^{op}, sSet)
$$

of [[sSet]]-[[enriched functor]]s.

A morphism $f : A \to B$ in $sPSh(C)$ is a transformation  given by a collection of morphisms $f_c : A(c) \to B(c)$ in [[sSet]].

The **global projective model structure** on $sPSh(C)$ has (as the [[global model  structure on simplicial presheaves]]) as fibrations and weak equivalences the objectwise fibrations and weak equivalences, i.e. those transformations for which all $f_c$ are a fibration or weak equivalence, respectively.

But $sPSh(C)$ is naturally enriched to an [[sSet]]-[[enriched functor category]], 

$$
  sPSh(C)_{proj} := [C^{op}, SSet]
$$

and with the above model structure this extends to the structure of a [[simplicial model category]], called the **global projective simplicial model structure on SSet-presheaves**.

The model structure that we are after is the left [[Bousfield localization]] 
$
  sPSh(C)_{proj}^{l loc}
$
of $sPSh(C)_{proj}$ at the following set of morphisms (...see [TV page 14](http://arxiv.org/PS_cache/math/pdf/0207/0207028v4.pdf#page=14)...)


It seems that the claim is that, indeed, in the special case that $C$ happens to be an ordinary category, the model structure on $sPSh(C)_{proj}^{l loc}$ reproduces the projective [[local model structure on simplicial presheaves]].

## References

The theory of model structures on SSet-enriched presheaf categories was developed in

* [[Bertrand Toen]], [[Gabriele Vezzosi]], _Topos Theory_ ([arXiv](http://arxiv.org/abs/math/0207028))


[[!redirects model structure on SimpSet-enriched presheaves]]
[[!redirects model structure on sSet-enriched presheaves]]
[[!redirects model structure on SSet-enriched presheaves]]
[[!redirects model structure on sSet-presheaves]]
[[!redirects model structure on SSet-presheaves]]
[[!redirects model structure on simplicially enriched presheaves]]