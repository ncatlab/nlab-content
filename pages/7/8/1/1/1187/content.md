
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Compact objects
+--{: .hide}
[[!include compact object - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _compact object in an $(\infty,1)$-category_ is the analogue in [[(∞,1)-category theory]] of the notion of [[compact object]] in [[category theory]].

## Definition

+-- {: .num_defn}
###### Definition

Let $\kappa$ be a [[regular cardinal]] and $C$ an [[(∞,1)-category]]
with $\kappa$-[[filtered (∞,1)-colimits]].

Then an [[object]] $c \in C$ is called **$\kappa$-compact** if the [[(∞,1)-categorical hom space]] functor

$$
  C(c,-) : C \to \infty Grpd
$$

preserves $\kappa$-[[filtered (∞,1)-colimits]].

For $\omega$-compact we just say _compact_. 

=--

This appears as ([[Higher Topos Theory|HTT, def. 5.3.4.5]]).




## Properties

### General

Let $\kappa$ be a [[regular cardinal]].

+-- {: .num_prop #StabilityUnderColimits}
###### Proposition

Let $C$ be an [[(∞,1)-category]] which admits small 
$\kappa$-[[filtered (∞,1)-colimits]]. Then the full [[sub-(∞,1)-category]]
of $\kappa$-compact objects in closed under $\kappa$-small [[(∞,1)-colimits]]
in $C$.

=--

This is ([[Higher Topos Theory|HTT, cor. 5.3.4.15]]).

### Presentation in model categories

If the [[(∞,1)-category]] $\mathcal{C}$ is a [[locally presentable (∞,1)-category]], then it is the [[simplicial localization]] of a [[combinatorial model category]] $C$, and one may ask how the 1-categorical notion of [[compact object]] in $C$ relates to the $(\infty,1)$-categorical notion of compact in $\mathcal{C}$.

Since compactness is defined in terms of colimits, the question is closely related to the question which 1-categorical $\kappa$-[[filtered colimits]] in $C$ are already [[homotopy colimits]] (without having to [[derived functor|derive]] them first).

General statements seem not to be in the literature yet, but see [this MO discussion](http://mathoverflow.net/questions/95165/compact-objects-in-model-categories-and-infty-1-categories). For discussion of compactness in a [[model structure on simplicial sheaves]], see for instance ([Powell, section 4](#Powell)).

## Examples

*  In $C =$ [[(∞,1)Cat]], for uncountable $\kappa$, the $\kappa$-compact objects
   are precisely the $\kappa$-[[essentially small (∞,1)-categories]]. (See there
   for more details.)

*  In $C =$ [[∞Grpd]], for uncountable $\kappa$, the $\kappa$-compact objects are precisely the $\kappa$-[[essentially small ∞-groupoids]]. When $\kappa = \omega$, the compact objects in ∞Grpd are the [[retracts]] of the $\omega$-small ∞Grpds, i.e., the retracts of the [[finite homotopy types]] ([[finite CW-complexes]]). Not every such retract is equivalent to a $\omega$-small ∞-groupoid; the vanishing of [[Wall's finiteness obstruction]] is a necessary and sufficient condition for such an equivalence to exist.


## Related concepts

* [[compact object]]

* [[compact topos]]

* **compact object in an $(\infty,1)$-category**

* [[relatively k-compact morphism in an (infinity,1)-category]]



## References

The general definition appears as definition 5.3.4.5  in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

Compactness in presenting model categories of simplicial sheaves is discussed for instance in 

section 4 of 

* [[Geoffrey Powell]], _The adjunction between $\mathcal{H}(k)$ and $DM^{eff}_-(k)$_ (2001) ([pdf](http://math.univ-angers.fr/~powell/documents/2001/adjoint.pdf))
  {#Powell}


[[!redirects compact object in an (∞,1)-category]]