
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


# Linearly independent subsets
* table of contents
{: toc}

## Idea

A [[concrete set|set]] of [[vector]]s is linearly dependent if one can be written as a [[linear combination]] of the others, and linearly independent otherwise.  In the latter case, the vectors in the set form a [[basis of a vector space|basis]] of their [[linear span|span]].


## Definitions

Let $K$ be a [[rig]], and let $V$ be a (left or right) [[module]] over $K$.  (Often $K$ is a [[field]] so that $V$ is a [[vector space]], but this is unnecessary.)  Let $S$ be a [[subset]] of the [[underlying set]] ${|V|}$ of $V$.


### Abstractly

By the [[adjunction]] between the underlying-set functor and the [[free functor]], the subset inclusion
$$ i_S\colon S \to {|V|} $$
corresponds to a [[homomorphism]]
$$ \hat{i}_S\colon K[S] \to V .$$
Although $i_S$ is (by hypothesis) a [[monomorphism]] in $Set$, $\hat{i}_S$ need not be a monomorphism in $K Mod$.

+-- {: .num_defn}
###### Definition

The subset $S$ is __linearly independent__ if $\hat{i}_S$ is a monomorphism; otherwise, $S$ is __linearly dependent__.
=--

Conversely, if we start with an (abstract!) [[set]] $S$ and a monomorphism from $K[S]$ to $V$, then the corresponding [[function]] from $S$ to ${|V|}$ must be a monomorphism (because the underlying-set functor is [[faithful functor|faithful]]).  Thus, our considering only subsets of ${|V|}$ loses no generality.


### Concretely

Given a [[linear combination]]
$$ \sum_{i=1}^n a_i v_i ,$$
this may or may not equal the [[zero vector]] $0_V$.  Of course, if every $a_i$ is the zero scalar $0_K$, then the sum must be $0_V$.

+-- {: .num_defn}
###### Definition

The subset $S$ is __linearly independent__ if, conversely, for every finite subset $\{v_1, \ldots, v_n\} \subseteq S$, we have $a_i = 0_K$ for all $i$ whenever 
$$ \sum_{i=1}^n a_i v_i = 0_V ;$$
otherwise, $S$ is __linearly dependent__.
=-- 

Observe that the empty set is linearly independent by a vacuous implication. 


### Constructively

In [[constructive mathematics]], the definitions above of linear independence are all right (and still equivalent), but the definition of linear dependence as simply the [[negation]] of linear independence is unsatisfying.  Furthermore, we sometimes want something stronger than mere linear independence.

If $K$ is a [[Heyting field]], then the field structure defines a [[tight apartness relation]] $\ne$.  Even if $K$ is not a field, we may still suppose that it is equipped with a tight apartness, or at least some [[inequality relation]] $\ne$.  If we restrict attention to modules with a compatible inequality relation and homomorphisms that preserve this, then we also get an inequality relation $\ne$ on the [[hom-sets]] of the category $K Mod$.  This allows us to define stronger notions of both linear dependence (which we take to be the default notion) and linear independence (to which we give a new name).

+-- {: .num_defn}
###### Definition

The subset $S$ is __linearly dependent__ if $\hat{i}_S$ is non-monic in the strong sense that there exist [[generalised elements]] $f, g\colon A \to K[S]$ such that
$$ A \overset{f}\underset{g}\rightrightarrows K[S] \to V $$
are equal but $f \ne g$.  Concretely, $S$ is __linearly dependent__ if some linear combination
$$ \sum_{i = 1}^n a_i v_i = 0_V $$
but at least one $a_i \ne 0_K$.
=--

+-- {: .num_defn}
###### Definition

The subset $S$ is __linearly free__ if $\hat{i}_S$ is a [[regular monomorphism]], or equivalently if it is monic in the strong sense that $f ; \hat{i}_S \ne g ; \hat{i}_S$ whenever $f \ne g$.  Concretely, $S$ is __linearly free__ if
$$ \sum_{i = 1}^n a_i v_i \ne 0_V $$
whenever at least one $a_i \ne 0_K$.
=--

Then we have the following implications (assuming that $\ne$ is tight, so that $a = b$ holds iff $a \ne b$ fails) but not (in general) their unstated converses:
$$ LF \Rightarrow LI \Leftrightarrow \neg{LD} ;$$
$$ \neg{LF} \Leftarrow \neg{LI} \Leftarrow LD .$$

It may also be instructive to look at the logical structure of each condition:
*  $LI$: $\forall (a,v),\; \sum a v = 0 \;\Rightarrow\; \forall i,\; a_i = 0$;
*  $LD$: $\exists (a,v),\; \sum a v = 0 \;\wedge\; \exists i,\; a_i \ne 0$;
*  $LF$: $\forall (a,v),\; \sum a v \ne 0 \;\Leftarrow\; \exists i,\; a_i \ne 0$.

## Related concepts

* [[algebraically independent subset]]

[[!redirects linearly independent subset]]
[[!redirects linearly independent set]]
[[!redirects linearly independent]]
[[!redirects linear independence]]

[[!redirects linearly dependent subset]]
[[!redirects linearly dependent set]]
[[!redirects linearly dependent]]
[[!redirects linear dependence]]

[[!redirects linearly free subset]]
[[!redirects linearly free set]]
[[!redirects linearly free]]
[[!redirects linear freedom]]
[[!redirects linear freeness]]
