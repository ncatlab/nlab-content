

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

The canonical kind of [[morphisms]] between [[multicategories]] are _multifunctors_. This generalized the concept of [[functor]] between categories and that of [[monoidal functors]] between [[monoidal categories]]. 

## Examples


+-- {: .num_prop #MonoidalFunctoriality}
###### Proposition

The construction of [[K-theory spectra of permutative categories]] constitutes a multifunctor

$$
  \mathbb{K}
  \;\colon\;
  PermCat
    \longrightarrow
  Spectra
$$

between [[multicategories]] of [[permutative categories]] (under [[Deligne tensor product]]) and [[spectra]] (under [[smash product of spectra]]). 

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

See for instance

* Ross Tate, p. 2 of _Multicategories_, 2018 ([pdf](http://www.cs.cornell.edu/courses/cs6117/2018sp/Lectures/Multicategories.pdf))

[[!redirects multifunctors]]

[[!redirects multi-functor]]
[[!redirects multi-functors]]
