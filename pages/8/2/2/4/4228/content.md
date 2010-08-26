

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The _Cahier topos_ is a [[smooth topos]] that constitutes a [[Models for Smooth Infinitesimal Analysis|well-adapted model]] for [[synthetic differential geometry]].

It is the [[sheaf topos]] on the [[site]] [[ThCartSp]] of [[infinitesimal object|infinitesimally thickened]] [[Cartesian space]]s.

## Definition

Let [[ThCartSp]] be the [[full subcategory]] of the category of [[smooth loci]] on those of the form 

$$
  \mathbb{R}^n \times \ell W
  \,,
$$

consisting of a [[product]] of a [[Cartesian space]] with an [[infinitesimal space]], i.e. a formal dual of a _Weil algebra_ .

Define a structure of a [[site]] on [[ThCartSp]] by declaring a [[covering]] family to be a family of the form

$$
  \{
    U_i \times \ell W \stackrel{p_i \times Id}{\to} U \times \ell W
  \}
$$

where $\{U_i \stackrel{p_i}{\to} U\}$ is an [[open cover]] of the [[Cartesian space]] $U$ by Cartesian spaces $U_i$. 

The **Cahiers topos** $\mathcal{CT}$ is the [[category of sheaves]] on this site:

$$
  \mathcal{CT} := Sh(ThCartSp)  
  \,.
$$

## Properties


+-- {: .un_prop}
###### Proposition

The [[category]] of [[convenient vector space]]s embeds as a [[full subcategory]] into the Cahiers topos.

=--

+-- {: .proof}
###### Proof

[Kock86](http://www.numdam.org/item?id=CTGDC_1986__27_1_3_0)

=--

## Higher categorical version

The [[(∞,1)-topos]] of [[(∞,1)-sheaves]] on the [[site]] [[ThCartSp]] is discussed at [[∞-Lie groupoid]] as a context for $\infty$-Lie groupoids and [[∞-Lie algebroid]]s.

## References

The Cahiers topos was introduced in 

* [[Eduardo Dubuc]], _Sur les modeles de la geometrie differentielle synthetique_ Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 20 no. 3 (1979), p. 231-279  ([numdam](http://www.numdam.org/item?id=CTGDC_1979__20_3_231_0)).

and got its name from this journal publication. The definition appears in theorem 4.10 there, which asserts that it is a well-adapted model for [[synthetic differential geometry]].

A detailed review discussion is in section 5 of

* [[Anders Kock]], _Convenient vector spaces embed into the Cahiers topos_ ([numdam](http://www.numdam.org/item?id=CTGDC_1986__27_1_3_0))

It appears briefly mentioned in example 2) on p. 191 of the standard textbook

* [[Anders Kock]], _Synthetic differential geometry_ ([pdf](http://home.imf.au.dk/kock/sdg99.pdf))

With an eye towards [[Frölicher space]]s the site is also considered in section 5 of 

* Hirokazu Nishimura, _Beyond the Regnant Philosophy of Manifolds_ ([arXiv:0912.0827](http://arxiv.org/abs/0912.0827))
