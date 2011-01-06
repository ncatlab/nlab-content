

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A *connected site* is a [[site]] satisfying sufficient conditions to make its [[topos of sheaves]] into a [[connected topos]].


## Definition

Let $C$ be a [[locally connected site]]; we say it is a **connected site** if it is also has a [[terminal object]]


## Properties


+-- {: .un_prop}
###### Proposition

If $C$ is connected site, then the [[sheaf topos]] $Sh(C)$ is a [[connected topos]]. 

=--


+-- {: .proof}
###### Proof

We need to check that $\Pi_0$ preserves the [[terminal object]].

The terminal object in the site [[representable functor|represents]] the terminal presheaf on $C$, which is the presheaf constant on the point. By the discussion at [[locally connected site]] we have that every constant presheaf is a [[sheaf]] over $C$, hence the terminal object of $Sh(C)$ is also represented by the terminal object in the site, and we just write "$*$" for all these terminal objects.

By the discussion there, the left adjoint $\Pi_0$ in the [[sheaf topos]] over a [[locally connected site]] is given by the [[colimit]] functor $\lim_\to : [C^{op}, Set]\to Set$. The colimit over a [[representable functor]] is always the point (this is the ([[co-Yoneda lemma|co]])-[[Yoneda lemma]] in slight disguise), hence indeed $\Pi_0 * = *$. 

=--

## Examples

* The [[category of open subsets]] $Op(X)$ of a [[locally connected topological space|locally connected]] and [[connected topological space]] $Op(X)$ with the standard [[open cover]]-[[coverage]] is a connected site. The terminal object is $X$ itself.

* [[CartSp]], [[ThCartSp]].

## Related concepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]

and

* [[locally connected site]] / [[locally ∞-connected site]]

  * **connected site** / [[∞-connected site]]

  * [[strongly connected site]] / [[strongly ∞-connected site]]

  * [[totally connected site]] / [[totally ∞-connected site]]

* [[local site]] / [[∞-local site]]

* [[cohesive site]], [[∞-cohesive site]]





[[!redirects connected sites]]
