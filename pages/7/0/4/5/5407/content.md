

#Contents#
* table of contents
{:toc}

## Idea

A _locally ringed topos_ is a [[locally algebra-ed topos]] for the [[theory of local ring]]s.

## Definition

+-- {: .num_defn #InTermsOfStalks}
###### Definition

A [[ringed topos]] $(X, \mathcal{O}_X)$ with [[point of a topos|enough points]] (such as the [[sheaf topos]] over a [[topological space]]) is a **locally ringed topos** if all [[stalk]]s $\mathcal{O}_X(x)$ are [[local ring]]s.

=--

More generally

+-- {: .num_defn #InTermsOfClassifyingTopos}
###### Definition

A [[ringed topos]] $(X, \mathcal{O}_X)$ is a [[locally algebra-ed topos]] for the [[theory of local rings]]: 

* a [[topos]] $X$

* equipped with a [[geometric morphism]]

  $$
    X \stackrel{\overset{\mathcal{O}_X}{\leftarrow}}{\underset{}{\to}}
    Sh(CRing^{op}_{fp}, Z )
  $$

  into the [[Zariski topos]], the  [[classifying topos]] for the [[theory of local rings]].

=--

## Properties

+-- {: .num_prop}
###### Proposition

Definition \ref{InTermsOfStalks} is indeed a special case of def. \ref{InTermsOfClassifyingTopos}.

=--

This is for instance in ([Johnstone]{#Johnstone}) and in ([Lurie, remark 2.5.11](#Lurie))

## Related concepts

* [[ringed space]], [[locally ringed space]]

* [[ringed site]]

* [[ringed topos]], [[locally ringed topos]]

* [[locally algebra-ed topos]]

* [[locally algebra-ed (∞,1)-topos]]

## References

Section abc of

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
 {#Johnstone}

Section 2.5 of 

* [[Jacob Lurie]], _[[Structured Spaces]]_
 {#Lurie}

[[!redirects locally ringed toposes]]