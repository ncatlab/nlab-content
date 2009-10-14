<div class="rightHandSide toc">
[[!include synthetic differential geometry - contents]]
</div>


This entry is about the book

* [[Ieke Moerdijk]], [[Gonzalo Reyes|Gonzalo E. Reyes]], _Models for Smooth Infinitesimal Analysis_ Springer (1991)

#Contents#
* automatic table of contents goes here
{:toc}

# Summary #

The book discusses the construction and the properties of [[smooth topos]]es $(\mathcal{T},R)$ that model the axioms of [[synthetic differential geometry]] and are _well-adapted_ to [[differential geometry]] in that there is a [[full and faithful functor]] $Diff \to \mathcal{T}$ embedding the [[category]] [[Diff]] of smooth [[manifold]]s into the more general catgeory $\mathcal{T}$.

All models are obtained as [[category of sheaves|categories of sheaves]] on [[site]]s whose underlying category is a [[subcategory]] of that of [[smooth loci]].

#Models#

The following tabulates various models for [[smooth topos]]es and lists their properties.

## the topos $\mathcal{G}$ ##

## the topos $\mathcal{F}$ ##

## the topos $\mathcal{Z}$ ##

+-- {: .un_defn}
###### Definition

$\mathcal{Z} := Sh_{fin-open}(\mathbb{L})$ is the [[category of sheaves]] on the [[site]] $\mathbb{L}$ of [[smooth locus|smooth loci]] with [[cover]]ing [[sieve]]s given by finite open covers (...explain...).

=--

+-- {: .um_prop}
###### Proposition
**(properties)**

For the [[topos]] $\mathbb{Z}$ the following is true.

* the [[Grothendieck topology]] is [[subcanonical coverage|subcanonical]]

* the [[category]] [[Diff]] of smooth [[manifold]]s embeds [[full and faithful functor|full and faithfully]], $Diff \hookrightarrow \mathcal{Z}$

  (chapter VI, corollary 1.4)

* the general [[Kock-Lawvere axiom]] holds 

  (chapter VI, 1.9)

* the [[integration axiom]] holds
  
  (chapter VI, 1.10)

=--



## the topos $\mathcal{B}$ ##


+-- {: .un_defn}
###### Definition
**(chapter VI, 5.1)**

$\mathcal{B} := Sh_{fin-open/proj}(\mathbb{L})$ is the [[category of sheaves]] on the [[site]] $\mathbb{L}$ of [[smooth locus|smooth loci]] with [[cover]]ing [[sieve]]s given by finite open covers together with projections $\ell A \times \ell B \to \ell A$.
=--

+-- {: .um_prop}
###### Proposition
**(properties)**

For the [[topos]] $\mathcal{B}$ the following is true. 
    
* the [[Grothendieck topology]] is [[subcanonical coverage|subcanonical]]
  
  (chapter VI, 5.2)
    
* the [[category]] [[Diff]] of smooth [[manifold]]s embeds [[full and faithful functor|full and faithfully]], $Diff \hookrightarrow \mathcal{B}$

  (chapter VI, 5.2)
    
* the general [[Kock-Lawvere axiom]] holds
  
  (chapter VI, below 5.4)
 
* the [[integration axiom]] holds
  
  (chapter VI, below 5.4)
    
* a version of [[nonstandard analysis]] is realized
  
  (chapter VI, below 5.4)
    
=--


category: reference