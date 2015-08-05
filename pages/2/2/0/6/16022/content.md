
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Every [[geometric morphism]] factors as surjective morphism followed by an inclusion. The **(dense-closed)-factorization** can be viewed as a refinement of [[(geometric surjection, embedding) factorization system|this factorization]] for [[geometric embeddings]] where the surjectivity of the first morphisms is weakened to [[dominant geometric morphism|dominance]] or 'density' and the inclusion is strengthened to a [[closed subtopos|closed inclusion]] in return.

So from a topological perspective, what one does, is by taking the closure of the image in which the image is merely dense, one approximates the image inclusion by a closed-subspace inclusion.

## Statement

A [[geometric embedding]] of [[elementary toposes]]

$$
  Sh_j(\mathcal{E}) \hookrightarrow \mathcal{E}
$$


factors as

$$
  Sh_j(\mathcal{E}) 
    \hookrightarrow
  Sh_{c(ext(j))}(\mathcal{E})
    \hookrightarrow
  \mathcal{E}
$$

where $ext(j)$ (the "exterior" of $j$) denotes the $j$-closure of $\emptyset \rightarrowtail 1$ and 

$$
  \bar j \coloneqq c(ext(j))
$$ 

the [[closed subtopos|closed topology]] that corresponds to the [[subterminal object]] $ext(j)$.

Here the first inclusion exhibits a [[dense subtopos]] and the second a [[closed subtopos]].

## Remark

$Sh_{c(ext(j))}(\mathcal{E})$ can be viewed as the 'best approximation' of $Sh_j(\mathcal{E})$ by a closed subtopos and therefore might be called the _closure_ $Cl(Sh_j(\mathcal{E}))$ of $Sh_j(\mathcal{E})$.[^sga4] 

[^sga4]: ([SGA4](#SGA4), p.461) uses the term '_l'adh&#233;rence_' for it.

Its complement, the [[open subtopos]] $Ext(Sh_j(\mathcal{E}))$ corresponding to the [[subterminal object]] $ext(j)$ deserves in turn to be called the _exterior_ of $Sh_j(\mathcal{E})$.

## Related entries

* [[dense subtopos]]
* [[dominant geometric morphism]]
* [[(geometric surjection, embedding) factorization system]]

## References

* {#SGA4}[[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas ([[SGA4]])_, LNM **269** Springer Heidelberg 1972. (Expos&#233; IV 9.3.4-9.4.,pp.456ff)

* {#Johnstone}[[Peter Johnstone]], _[[Sketches of an Elephant]] vol.I_ , Oxford UP 2002. (around Lemma A 4.5.19, p. 219)

* {#Caramello09} [[Olivia Caramello]], _Lattices of theories_ , [arXiv:0905.0299](http://arxiv.org/abs/0905.0299) (2009). (section 8)
