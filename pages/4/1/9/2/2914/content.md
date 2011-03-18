

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Definition ##

+-- {: .un_prop}
###### Proposition


For $C$ a [[model category]] and $X \in C$ an [[object]], the [[over category]] $C/X$ as well as the [[undercategory]] $X/C$ inherit themselves structures of model categories whose [[fibrations]], [[cofibration]]s and [[weak equivalences]] are precisely the morphism that become fibrations, cofibrations and weak equivalences in $C$ under the forgetful functor $C/X \to C$ or $X/C \to C$.

=--

## Properties ##

+-- {: .num_prop}
###### Proposition


If $C$ is

* a [[cofibrantly generated model category]]

* or a [[proper model category]]

* or a [[cellular model category]]

then so are $C/X$ and $X/C$.

=--

The proofs are in ([OvMod](#OvMod)).

+-- {: .num_prop}
###### Proposition

If $C$ is a [[simplicial combinatorial model category]] and $X \in C$ is fibrant, then
$C/X$ [[presentable (infinity,1)-category|presentation]] for the 
[[over-(infinity,1)-category]] $C^\circ / X$

$$
  (C/X)^\circ \simeq C^\circ / X
$$

=--

To see this, use the description of the [[derived hom-space]] in an [[over-(infinity,1)-category]] (see there) as a [[homotopy pullback]]

$$
  \array{
    C^\circ/X(a : A \to X, b : B \to X) &\to& C(A,B)
    \\
    \downarrow && \downarrow^{\mathrlap{b_*}}
    \\
    {*} &\stackrel{a}{\to}& C(A,X)
  }
  \,.
$$

If $a : A \to X$ is cofibrant then $A$ is cofibrant, and if then $b : B \to X$ is fibrant, $B$ is fibrant and $b_* : C(A,B) \to C(A,X)$ is a fibration in the standard [[model structure on simplicial sets]] (by the axioms on an [[enriched model category]].) Therefore in this case the above [[homotopy pullback]] is computed by the ordinary pullback in [[sSet]]. This computes indeed the hom-space of the ordinary [[overcategory]] $C/X$.

## Related concepts


* [[over-category]] 

  * [[slice category]] 

  * [[under category]] 

  * [[over topos]]


* [[over (∞,1)-category]],

  * **model structure on an over-category**

  * [[over-(∞,1)-topos]]


## References ##

* Hirschhorn, _Overcategories and undercategories of model categories_ ([pdf](http://www-math.mit.edu/~psh/undercat.pdf))
{#OvMod}

[[!redirects model structure on an overcategory]]
[[!redirects model structure on an under category]]
[[!redirects model structure on an undercategory]]