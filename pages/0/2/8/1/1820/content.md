
<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

#Definition#

+-- {: .un_defn}
###### Definition
(Jeff Smith)

A [[model category]] $C$ is **combinatorial** if

* it is a [[presentable category]]

* it has a [[set]] (not a proper [[class]]) $I$ of generating cofibrations and and a set of trivial generating cofibrations, meaning that

  $$ 
    cof = llp(rlp(I))
  $$
  
  $$
    fib = llp(rlp(J))
    \,.
  $$

=--

Here $fib, cof \subset Mor(C)$ is the collection of fibrations and cofibration, respectively, and $llp(S), rlp(S)$ is the collection of morphisms satisfying the left or right, respectively, [[lifting property]] with respect to a collection of morphisms $S$. See also [[cofibrantly generated model category]].

The central theorem about combinatorial model categories is **Jeff Smith's theorem** which establishes the existence of model category structures from a comparatively small amount of input data.

+-- {: .num_theorem }
###### Theorem (Smith)

Let $C$ be a [[locally presentable category]], $W$ an accessibly embedded [[accessible category|accessible]] [[subcategory]] of the [[arrow category]] $Arr(C)$, and $I \subset Mor(C)$ a [[set]] (not a proper class) of morphisms of $C$ such that

* $W$ satisfies [[category with weak equivalences|2-out-of-3]];

* the set $rlp(I)$ of morphism with [[weak factorization system|right lifting property]] with respect to $I$ is contained in $W$

  $$
    rlp(I) \subset W
  $$

* the set $llp(rlp(I))$ of all morphism with [[weak factorization system|left lifting property]] with respect to $rlp(I)$ is closed under pushout and transfinite composition (see [[cofibrantly generated model category]]).

Then $C$ is a combinatorial model category with

* weak equivalences $W$;

* cofibrations $cof(I) = llp(rlp(I))$

* fibrations $fib = rlp(W \cap cof(I))$

=--

This theorem is used to establish various familiar model structures. For instance the [[folk model structure]] on [[strict omega-category|strict omega-categories]].


# Remarks #

Of interest are the combinatorial model categories that are at the same time [[simplicial model categories]]. These are precisely those that present [[presentable (∞,1)-categories]].

See [[combinatorial simplicial model category]].


#References#

Definition A.2.6.1 in 

* [[Jacob Lurie]], [[Higher Topos Theory]]

definition 1.3 in 

* Clark Barwick, _On (enriched) left Bousfield localization of model categories_ ([arXiv](http://arxiv.org/abs/0708.2067))

Smith's theorem is recalled as theorem xyz in [[Higher Topos Theory|HTT]], as proposition 1.7 in Barwick. After Smith presented it at a conference in Barcelona, its first appearance in a publication is apparently lemma 1.8 in 

* Tibor Beke, _Sheafifiable homotopy model categories_ ([arXiv](http://arxiv.org/abs/math.CT/0102087))


[[!redirects Smith's theorem]]
[[!redirects Smith theorem]]
[[!redirects Smith's theorem]]