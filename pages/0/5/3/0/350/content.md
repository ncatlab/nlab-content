# Idea

A Lawvere--Tierney topology (or operator, or modality, also called _geometric modality_) is a way of saying that something is 'locally' true.  Unlike a [[Grothendieck topology]], this is done directly at the stage of [[logic]], defining a _geometric logic_.  In fact, it is a generalisation of Grothendieck topology in this sense: If $C$ is a small category, then choosing a Grothendieck topology on $C$ is equivalent to choosing a Lawvere--Tierney topology in the topos $\Set^{C^\op}$ of [[presheaf|presheaves]] on $C$.

The use of "topology" for this and the related Grothendieck concept is regarded by some people as unfortunate; see [[Grothendieck topology]] for some reasons why.  A proposed replacement for "Grothendieck topology" is [[coverage|(Grothendieck) coverage]]; see [[Grothendieck topology]] for some possible replacements for "Lawvere--Tierney topology."

# Definition

Let $E$ be a [[topos]], with [[subobject classifier]] $\Omega$. A __Lawvere--Tierney topology__ in $E$ is a map $j: \Omega \to \Omega$ that satisfies certain axioms.

The axioms say that $j$ is ([[internalization|internally]]) a [[exact functor|left exact]] [[monad]] on the internal meet-[[semilattice]] $\Omega$. To be explicit:
* $\id_\Omega \leq j: \Omega \to \Omega$ ('if $p$ is true, then $p$ is locally true');
* $j \circ j = j: \Omega \to \Omega$ ('$p$ is locally locally true iff $p$ is locally true');
* $j \circ \wedge = \wedge \circ j \times j: \Omega \times \Omega \to \Omega$ ('$p \wedge q$ is locally true iff $p$ and $q$ are each locally true').

Here $\leq$ is the internal [[partial order]] on $\Omega$, and $\wedge: \Omega \times \Omega \to \Omega$ is the internal [[meet]].

Equivalently, the third axiom above can be replaced with the (internal) statement that $j$ is order-preserving; the equivalence amounts to the fact that, within the internal logic of topoi, one can demonstrate that every monad on the preorder of truth values is in fact [[strong monad|strong]] (a special case of the fact that, for an endofunctor on some monoidal closed $V$, [[tensorial strength|tensorial strengths]] are the same as $V$-enrichments, as described in the article on the former), and therefore _automatically_ preserves finite meets. Thus, a Lawvere-Tierney topology is the same thing as an internal [[closure operator]] on the preorder $\Omega$ (aka, a [[Moore closure]] on the one-element set), which amounts to the same thing as a natural closure operator on subobjects.

Specifically, given any [[subobject]] inclusion $X \hookrightarrow Y$ in $E$, consider its [[characteristic morphism]] $\chi_X: Y \to \Omega$. Then $j \circ \chi_X$ is another morphism $Y \to \Omega$, which defines another subobject $j_*(X)$ of $Y$, taken as the closure of our original subobject. The elements of $j_*(X)$ are those elements of $Y$ that are 'locally' in $X$.


# Equivalence with Grothendieck topologies

As mentioned above, a Lawvere--Tierney topology on $\Set^{C^\op}$ is equivalent to a [[Grothendieck topology]] on $C$.  Suppose that $C$ is a small site.  Then given a [[subpresheaf]] inclusion $F \hookrightarrow G$ in $\Set^{C^\op}$, an object $X$ of $C$, and an element $f$ of $G(X)$, we say $f$ is locally in $F$ (that is, $f \in j_*(F)(X)$) if and only if, for some [[cover|covering family]] $c = (c_i: U_i \to X)_i$ on $X$, the restriction $c^*(f)$ of $f$ to $c$ is in $F$ (that is, each $c_i^*(f) \in F(U_i)$).  This intuitively defines the "local" modality that is the Lawvere--Tierney topology corresponding to the given Grothendieck topology on $C$.

As a specific example, take the usual Grothendieck topology on [[Top]], given by the usual notion of open cover. Taking real-valued functions on a space defines a presheaf (in fact a sheaf) $G: X \mapsto [X,R]$ on $\Top$; the constant functions form a subpresheaf $F$ of $G$. A real-valued function $f: X \to R$ belongs to $j_*(F)$ iff it is *locally* constant; that is, for some open cover $(U_i)_i$ of the domain $X$, each restriction $f|U_i$ is constant.

To make this precise in terms of the above definition, we need to understand the subobject classifier in $E = Set^{C^{op}}$.  But according to the definition, $\Omega$ is simply the representing object for the functor 
$$Sub: E^{op} \to Set$$ 
which takes an object $F$ of $E$ to the collection of subobjects of $F$, $Sub(F)$. In other words, $Sub(F) \cong \hom_E(F, \Omega)$. Applied to $F = \hom_C(-, c)$, we have then 
$$Sub(\hom_C(-, c)) \cong \hom_{Set^{C^{op}}}(\hom_C(-, c), \Omega) \stackrel{Yoneda}{\cong} \Omega(c)$$ 
In other words, we find that the functor $\Omega: C^{op} \to Set$ is defined by 
$$\Omega(c) = \{sieves on c\}$$ 

Next, if $J$ is a Grothendieck topology on $C$, then the collection of $J$-covering sieves on $c$ [which we denote by $J(c)$] is a subcollection of all sieves on $c$, and so we have an inclusion 
$$J(c) \hookrightarrow \Omega(c)$$ 
and this inclusion is natural in $c$, by virtue of the first axiom on covering sieves. Thus we have a subobject
$$J \hookrightarrow \Omega$$ 
and again, by definition of subobject classifier, this subobject corresponds to a uniquely determined element 
$$j \in \hom_E(\Omega, \Omega)$$ 
which is just the Lawvere--Tierney operator $j: \Omega \to \Omega$.

Conversely, any morphism $j:\Omega\to\Omega$ determines a subobject $J$ of $\Omega$, which therefore associates to every object $c$ a set of sieves on $c$.  It is easy to check that the axioms for covering sieves in a Grothendieck topology correspond exactly to the required properties of the operator $j$.




#Sheaves#

Using Lawvere--Tierney topologies, 
the notion of [[sheaf]] and [[sheafification]] generalizes from [[Grothendieck topos|Grothendieck topoi]] to arbitrary topoi. 

Technically this is achieved essentially by replaxing [[local isomorphism]]s everywhere with [[dense monomorphism]]s.

If $E = PSh(S)$ is a [[presheaf]] [[Grothendieck topos]] for a [[site]] $S$ regarded as a [[topos]] with Lawvere--Tierney topology and hence equipped with a notion of [[dense monomorphism]]s, then 
a [[presheaf]] $F \in PSh(S)$ is a [[sheaf]] with respect to the given topology precisely if 
$$
  Hom_{PSh(S)}(-, F):
  PSh(S)^{op} \to Set
$$ 
sends all [[dense monomorphism]]s to [[isomorphism]]s.

This condition clearly makes sense for every topos with Lawvere--Tierney topology.


## Sheafification ##

By using [[dense monomorphism]]s in place of [[local isomorphism]]s, this induces a notion of [[sheafification]] on an arbitrary [[topos]] $E$ with a Lawvere--Tierney topology.

This sheafification is a [[functor]] 

$$
  \bar {(-)} : E \to Sh(E)
$$

to the [[subcategory]] $i : Sh(E) \hookrightarrow E$ of objects local with respect to [[dense monomorphism]]s which is

* [[exact functor|left exact]] (commutes with all small limits);

* [[adjoint functor|left adjoint]] to $i$.

In the case that $E = PSh(S)$ and the Lawvere--Tierney topology is that corresponding to a Grothendieck topology on $S$, the two notions of [[sheafification]] coincide.


#References#

Lawvere--Tierney topologies are discussed in section V.1 of

* MacLane, Moerdijk, [[Sheaves in Geometry and Logic]]

the notion of sheaves in section V.3, the sheafification functor in section V.3 and the relation to Grothendieck topologies in section V.4.


[[!redirects sheafification in a Lawvere-Tierney topos]]
[[!redirects sheafification in a Lawvere--Tierney topos]]
[[!redirects sheafification in a Lawvere–Tierney topos]]
[[!redirects Lawvere–Tierney topology]]
[[!redirects Lawvere--Tierney topology]]