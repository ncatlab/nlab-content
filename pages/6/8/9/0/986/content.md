
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# The specialisation order
* table of contents
{: toc}

## Idea

The __specialisation order__ is a way of turning any [[topological space]] $X$ into a [[preorder]]ed set (with the same underlying set).

## Definition

+-- {: .un_defn}
###### Definition 
Given a topological space $X$ with topology $\mathcal{O}(X)$, the specialization order $\leq$ is defined by either of the following two equivalent conditions: 

1. $x \leq y$ if and only if $x$ belongs to the [[topological closure]] of $\{y\}$; we say that $x$ is a __specialisation__ of $y$. 

1. $x \leq y$ if and only if $\forall_{U \colon \mathcal{O}(X)} (x \in U) \Rightarrow (y \in U).$

(Note: some authors use the opposite ordering convention.) 
=-- 

## Properties

The specialization order on a topological space is always a [[preorder]], because the specialization order is defined as $\forall_{U \colon \mathcal{O}(X)} (x \in U) \Rightarrow (y \in U)$. Given any two [[sets]] $A$ and $B$ and any [[binary relation]] $R(x, y)$ between $A$ and $B$,  the relation $\forall_{w \colon B} R(x, w) \implies R(y, w)$ is a [[preorder]] on $A$. 

$X$ is $T_0$ if and only if its specialisation order is a [[partial order]].  $X$ is $T_1$ iff its specialisation order is [[equality]].  $X$ is $R_0$ (like $T_1$ but without $T_0$) iff its specialisation order is an [[equivalence relation]].  (See [[separation axioms]].)

Given a [[continuous map]] $f: X \to Y$ between topological spaces, it is order-preserving relative to the specialisation order.  Thus, we have a [[faithful functor]] $Spec$ from the category of $\Top$ of topological spaces to the category $\ProSet$ of preordered sets.

In the other direction, to each proset $X$ we may associate a topological space whose elements are those of $X$, and whose open sets are precisely the upward-closed sets with respect to the preorder. This topology is called the [[specialization topology]]. This defines a functor 

$$i \colon ProSet \to Top$$ 

which is a full embedding; the [[essential image]] of this functor is the category of [[Alexandroff spaces]] (spaces in which an arbitrary intersection of open sets is open). Hence the category of prosets is equivalent to the category of Alexandroff spaces. 

In fact, we have an adjunction $i \dashv Spec$, making $ProSet$ a [[coreflective subcategory]] of $Top$. In particular, the counit evaluated at a space $X$, 

$$i(Spec(X)) \to X,$$ 

is the identity function at the level of sets, and is continuous because any open $U$ of $X$ is upward-closed with respect to $\leq$, according to the second equivalent condition of the definition of the specialization order. 

This [[adjunction]] restricts to an [[adjoint equivalence]] between the categories $\Fin\Pros$ and $\Fin\Top$ of finite prosets and finite topological spaces. The unit and counit are both identity functions at the level of sets, so we in fact have an equivalence between these categories as [[concrete categories]]. 

## Related entries

* [[finite topological space]]

* [[separation axioms in terms of lifting properties]]

* [[specialization topology]]

[[!redirects specialization orders]]

[[!redirects specialisation order]]
[[!redirects specialisation orders]]

[[!redirects specialization ordering]]
[[!redirects specialization orderings]]

[[!redirects specialisation ordering]]
[[!redirects specialisation orderings]]

[[!redirects specialization preorder]]
[[!redirects specialization preorders]]

[[!redirects specialisation preorder]]
[[!redirects specialisation preorders]]


