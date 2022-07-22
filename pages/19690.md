

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

The canonical kind of [[morphisms]] between [[multicategories]] generalize the concept of *[[functors]]* between [[categories]] and that of *[[monoidal functors]]* between [[monoidal categories]]. 

It is common to speak here of "multifunctors" (e.g. [Elmendorf & Mandell 2004, p. 2](#ElmendorfMandell04), review in [Tate 2018, p. 2](#Tate18)) but see at *[[multifunctor]]* for other meanings of this term.

## Examples

+-- {: .num_prop #MonoidalFunctoriality}
###### Proposition

The construction of [[K-theory spectra of permutative categories]] constitutes a morphism of multicategories

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

([May 80, theorem 1.6, Theorem 2.1](K-theory+of+a+permutative+category#May80), [Elmendorf-Mandell 04, theorem 1.1](#ElmendorfMandell04), [Guillou 10, Theorem 1.1](K-theory+of+a+permutative+category#Guillou10)


## References

Review:

* {#Tate18} Ross Tate, p. 2 of: *Multicategories* (2018) &lbrack;[pdf](http://www.cs.cornell.edu/courses/cs6117/2018sp/Lectures/Multicategories.pdf), [[Tate-Multicategories.pdf:file]]&rbrack;

See also:

* {#ElmendorfMandell04} [[Anthony Elmendorf]], [[Michael Mandell]], _Rings, modules and algebras in infinite loop space theory_, Adv. in Math. **205** 1 (2006) 163-228 &lbrack;[arXiv:math/0403403](https://arxiv.org/abs/math/0403403), [doi:10.1016/j.aim.2005.07.007](https://doi.org/10.1016/j.aim.2005.07.007)&rbrack;
 

[[!redirects morphisms of multicategories]]


