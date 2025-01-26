
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--



#Contents#
* table of contents
{: toc}


## Definition

A [[category]] $C$ is **cocomplete** if it has all [[small diagram|small]] [[colimit|colimits]]: that is, if every [[small diagram]] $F: D \to C$ where $D$ is a [[small category]] has a [[colimit]] in $C$. Equivalently, a category $C$ is **cocomplete** if it has all small [[wide pushouts]] and an [[initial object]]. 

The most natural [[morphisms]] between cocomplete categories are the [[cocontinuous functor|cocontinuous functors]].

## Remarks

* Dually, a category with all small limits is a [[complete category]].
* A category $D$ is cocomplete if and only if $D^{op}$ is complete, so the abstract properties of cocompleteness mimic those of completeness.
* If a category has not all small colimits but all _finite_ colimits, then it is a [[finitely cocomplete category]].

## Examples

Many familiar categories of mathematical structures are cocomplete: to name just a few examples, [[Set]], [[Grp]], [[Ab]], [[Vect]] and [[Top]] are cocomplete.

For a small category $C$, the presheaf category $[C^{op},Set]$ is cocomplete, and the [[Yoneda embedding]] exhibits it as the [[free cocompletion]] of $C$.

## The 2-category of cocomplete categories

### Properties

- The 2-category of cocomplete categories is [[2-monadic]] over $Cat$, and [[complete]] and [[cocomplete]] as a 2-category. (See [this MathOverflow answer](https://mathoverflow.net/a/65999/152679) by [[Mike Shulman]].)
- The [[copower]] $C \cdot A$ where $C$ is a category and $A$ is a cocomplete category, is given by $[C^{op}, A]$. The [[power]] $C \pitchfork A$ is given by $[C, A]$ (see [Pitts 1985](#Pitts)).

## Related concepts

* [[complete category]]

* [[bicomplete category]]

* [[M-complete category]]

## References

* {#Pitts} [[Andrew M. Pitts]], _On product and change of base for toposes_ , Cah. Top. Géom. Diff. Cat. **XXVI** no.1 (1985) pp.43-61.

[[!redirects cocomplete categories]]
[[!redirects cocomplete]]
[[!redirects mplete category]]