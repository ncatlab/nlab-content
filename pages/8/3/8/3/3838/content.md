
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Compact objects
+--{: .hide}
[[!include compact object - contents]]
=--
#### $(\infty,1)$-Category theory
+-- {: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

The notion of _essentially small $(\infty,1)$-category_ is the generalization of the notion of [[essentially small category]] from [[category theory]] to [[(∞,1)-category]] theory.


## Definitions

+-- {: .num_defn}
###### Definition
  
A [[quasi-category]] $C$ is **essentially $\kappa$-small** for some [[regular cardinal]] $\kappa$ if 

1. the collection of [[equivalence in a quasi-category|equivalence classes]] in $C$ is $\kappa$-small;

2. for every [[morphism]] $f : x \to y$ in $C$ the [[simplicial homotopy group|homotopy sets]] of the [[hom-object in a quasi-category|hom ∞-groupoid]] at $f$ (that is, the  sets $\pi_i(Hom^R(x,y),f)$) are $\kappa$-small.

$C$ is **essentially small** if the above conditions hold "absolutely," i.e. with "$\kappa$-small" replaced by "small."

=--

This appears as [[Higher Topos Theory|HTT, def. 5.4.1.3, prop. 5.4.1.2]].

In the presence of the [[regular extension axiom]] (which follows from the [[axiom of choice]]), essential smallness is equivalent to being essentially $\kappa$-small for some small [[regular cardinal]] $\kappa$.

## Properties

+-- {: .num_prop #Characterization}
###### Proposition

Let $C$ be an [[(∞,1)-category]] and $\kappa$ an [[countable set|uncountable]] [[regular cardinal]]. The following are equivalent:

1. $C$ is $\kappa$-small.

2. $C$ is a $\kappa$-[[compact object in an (infinity,1)-category|compact object]] in [[(∞,1)Cat]].

3. $C$ is equivalently given by a [[quasi-category]] whose underlying [[simplicial set]] is a $\kappa$-[[small set]].

=--

This is [[Higher Topos Theory|HTT, prop. 5.4.1.2]]

The analogous statement holds for [[∞-groupoids]].

+-- {: .num_prop #CharacterizationOfSmallInfinityGroupoids}
###### Proposition

For $X$ an [[∞-groupoid]] and $\kappa$ an [[countable set|uncountable]]
[[regular cardinal]], the following are equivalent

1. For each [[object]] $x \in C$ the [[simplicial homotopy group|homotopy sets]]
   $\pi_n(X,x)$ are $\kappa$-[[small sets]].

1. $X$ is presented by a $\kappa$-[[small set|small]] [[simplicial set]]/[[Kan complex]].

1. $X$ is a $\kappa$-[[compact object in an (∞,1)-category|compact object]] in [[∞Grpd]].

=--

This is ([[Higher Topos Theory|HTT, corollary 5.4.1.5]]).

Notice that this proposition really requires that $\kappa$ be uncountable. When $\kappa = \omega$ it is not true: the $\omega$-compact objects of ∞Grpd are the homotopy retracts of finite CW-complexes, while the $\omega$-small ∞-groupoids are just the finite CW-complexes. Not every retract of a finite CW-complex has the homotopy type of a finite CW-complex: there is an obstruction, defined for a retract $X$ of a finite CW-complex, which is an element of $\tilde{K}_0(\mathbb{Z}[\pi_1(X)])$, is called Wall's finiteness obstruction, and vanishes if and only if $X$ has the homotopy type of a finite CW-complex. See Wall's paper in the references.

## Related concepts

* [[essentially small category]]

* [[compact object in an (∞,1)-category]]

## References

This is the topic of section 5.4.1 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

Wall's finiteness obstruction was defined in

* [[C. T. C. Wall]], _Finiteness conditions for CW-complexes_.

[[!redirects essentially small (∞,1)-category]]
[[!redirects essentially small (∞,1)-categories]]
[[!redirects essentially small (infinity,1)-category]]
[[!redirects essentially small (infinity,1)-categories]]

[[!redirects small (∞,1)-category]]
[[!redirects small (∞,1)-categories]]
[[!redirects small (infinity,1)-category]]
[[!redirects small (infinity,1)-categories]]


[[!redirects essentially small ∞-groupoid]]
[[!redirects essentially small ∞-groupoids]]
[[!redirects essentially small infinity-groupoid]]
[[!redirects essentially small infinity-groupoids]]

[[!redirects small ∞-groupoid]]
[[!redirects small ∞-groupoids]]
[[!redirects small infinity-groupoid]]
[[!redirects small infinity-groupoids]]
