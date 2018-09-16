
#Contents#
* table of contents
{:toc}

## Idea

The [[2-category]] of [[permutative categories]]. With respect to multi-linear functors ([[Deligne tensor product]]) this canonically becomes a [[multicategory]] ([Elmendorf-Mandell 04, Section 3](#ElmendorfMandell04)).

## Properties


+-- {: .num_prop #MonoidalFunctoriality}
###### Proposition

The construction of [[K-theory spectra of permutative categories]] constitutes a [[multifunctor]]

$$
  \mathbb{K}
  \;\colon\;
  PermCat
    \longrightarrow
  Spectra
$$

between [[multicategories]] [[permutative categories]] (under [[Deligne tensor product]]) and [[spectra]] (under [[smash product of spectra]]). 

Hence for a multilinear functor of permutative categories

$$
  F 
    \;\colon\;
  \mathcal{A}_1 \times \cdots \times \mathcal{A}_n
  \longrightarrow
  \mathcal{B}
$$

there is a compatibly induced morphism of K-[[spectra]] out of the [[smash product of spectra|smash product]]

$$
  \mathbb{K}(\mathcal{A}_1) 
    \wedge
    \cdots
    \wedge
  \mathbb{K}(\mathcal{A}_n)
  \longrightarrow
  \mathbb{K}(\mathcal{B})
  \,.
$$


This implies that the construction further extends to a [[2-functor]] from the [[2-category]] $PermCat Cat$ of [[enriched categories]] over the [[multicategory]] of [[permutative categories]] to that of [[enriched categories]] of [[spectra]]:

$$
  \mathbb{K}_\bullet
  \;\colon\;
  PermCat Cat \longrightarrow Spectra Cat
$$

which applies $\mathbb{K}$ to each [[hom-object]].

=--

([May 80, theorem 1.6, Theorem 2.1](K-theory+of+a+permutative+category#May80), [Elmendorf-Mandell 04, theorem 1.1](K-theory+of+a+permutative+category#ElmendorfMandell04), [Guillou 10, Theorem 1.1](K-theory+of+a+permutative+category#Guillou10)




## References

* {#ElmendorfMandell04} [[Anthony Elmendorf]], [[Michael Mandell]], secton 3 of _Rings, modules and algebras in infinite loop space theory_, Adv. in Math. 205 (2006), no. 1, 163-228 ([arXiv:math/0403403](https://arxiv.org/abs/math/0403403))


category: category