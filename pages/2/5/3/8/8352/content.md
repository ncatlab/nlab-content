
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[homological resolution]] of a [[chain complex]] by a complex of [[free modules]].

## Properties

### Existence
 {#Existence}

+-- {: .num_prop}
###### Proposition

For $R$ a [[ring]], every $R$-[[module]] admits a free resolution.

=--


## Examples

+-- {: .num_prop #AbelianGroupHasFreeResolutionOfLength2}
###### Proposition

Assuming the [[axiom of choice]], then every [[abelian group]] $A$ admits a free resolution of just length 2, hence with trivial [[syzygies]], hence there exists a [[short exact sequence]] of abelian groups of the form

$$
  0 \to F_2 \longrightarrow F_1 \longrightarrow A \to 0
$$

where both $F_1$ and $F_2$ are [[free abelian groups]].

=--

+-- {: .proof}
###### Proof

Let $F_1 = \mathbb{Z}[A]$ be the [[free abelian group]] on the underlying [[set]] of $A$, and let $F_1 \to A$ be the canonical morphism that sends a generator to itself (the [[adjunction counit]] of the [[free-forgetful adjunction]]).

Then let $F_2 \to F_1$ be the [[kernel]] of that map, hence $F_2$ a [[subgroup]] of $F_1$. Assuming the [[axiom of choice]] then every [[subgroup]] of a [[free abelian group]] is itself free abelian, hence $F_2$ is free abelian ([prop.](free+abelian+group#SubgroupsOfFreeAbelianGroupsAreFree)).

=--

+-- {: .num_remark }
###### Remark

Prop. \ref{AbelianGroupHasFreeResolutionOfLength2} implies that all [[Ext]]-groups between abelian groups are concentrated in degrees 0 and 1. 

(By the discussion at _[[derived functor in homological algebra]]_.)

=--


+-- {: .num_example}
###### Example
**([[Koszul complex]] is free resolution of [[quotient ring]])

For $R$ a [[commutative ring]] and $(x_1, \cdots, x_d)$ a [[regular sequence]] of elements, then the [[Koszul complex]] $K(x_1, \cdots, x_d)$ is a free resolutions of the [[quotient ring]] $R/(x_1, \cdots, x_d)$ by free $R$-modules.

=--

## Related concepts

* [[Adams resolution]]

* [[projective object]], [[projective presentation]], [[projective cover]], [[projective resolution]]

  * [[projective module]]

* [[injective object]], [[injective presentation]], [[injective envelope]], [[injective resolution]]

  * [[injective module]]

* [[free object]], **free resolution**
 
  * [[free module]]

* flat object, [[flat resolution]]

  * [[flat module]]


## References

Lecture notes include for instance

around page 5 of 

* [[Andrew Baker]], _Notes on chain complexes_ ([pdf](http://www.maths.gla.ac.uk/~ajb/dvi-ps/chaincomplexes.pdf))

[[!redirects free resolutions]]
