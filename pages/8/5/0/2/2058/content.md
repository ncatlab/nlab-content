
<div class="rightHandSide toc">
[[!include (infinity,1)-topos - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

One says -- at least in the context of [[Giraud's axioms]] for [[topos]]es and [[(∞,1)-toposes]]) -- that _[[colimit]]s are universal_ in a context in which they are _stable under [[pullback]]_. This is described in more detail at [[commutativity of limits and colimits]].

The statement "colimits are universal" is then one of [[Giraud's axioms]] that characterize [[Grothendieck topos]]es in the [[category theory|1-categorical context]] and Grothendieck-Rezk-Lurie [[(∞,1)-topos]]es in the [[higher category theory|higher categorical context]].

## Definition

+-- {: .un_defn}
###### Definition

A [[locally presentable (∞,1)-category]] $C$ has **universal colimits** if for every [[morphism]] $f : X \to Y$ in $C$ the induced [[limit in a quasi-category|pullback]]-[[(∞,1)-functor]] on [[over quasi-category|over-(∞,1)-categories]]

$$
  f^* : C^{/X} \to C^{/Y}
$$

preserves all [[colimit in a quasi-category|colimits]].

=--

For $F : K \to C^{/Y}$ a colimit diagram, this says in particular that

$$
  ({\lim_\to}_k F_k ) \times_Y X \simeq
  {\lim_\to}_k (F_k \times_Y X)
  \,.
$$ 

## Properties

+-- {: .un_prop}
###### Proposition

If $C$ is an [[(∞,1)-topos]], then it has universal colimits.

=--

This is [[Higher Topos Theory|HTT, theorem 6.1.0.6 (3) ii)]]



## References 

Section 6.1.1 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
