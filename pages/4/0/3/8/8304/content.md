
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Abelianisation is the process of [[free functor|freely]] making an [[algebraic structure]] 'abelian'. There are several notions of abelianizations for various algebraic structures, notably there is the abelianization of [[non-abelian groups]] to [[abelian groups]].

There is also [[Verdier's abelianization functor]] from a [[triangulated category]] to an [[abelian category]] with some universal property; this is treated in a separate entry.  


## For groups

### Definition

+-- {: .num_defn }
###### Definition

For $G$ a [[group]], its **abelianization** $G^{ab} \in $ [[Grp]] is the [[quotient]] of $G$ by its [[commutator subgroup]]:

$$
  G^{ab} \coloneqq G/[G,G]
  \,,
$$

=--

A group whose abelianization is the [[trivial group]] is called a _[[perfect group]]_.

The abelianization is an [[abelian group]]. Indeed, it is the [[universal construction|universal]] abelian group induced by $G$, in the following sense:

+-- {: .num_prop }
###### Proposition

Abelianization extends to a [[functor]] $(-)^{ab} \colon $ [[Grp]] $\to$ [[Ab]] and this functor is [[left adjoint]] to the [[forgetful functor]] $U \colon Ab \to Grp$ from abelian groups to group. 

=--

Hence abelianization is the _[[free construction]]_ of an abelian group from a group.


### Examples

#### Homotopy groups

+-- {: .num_example }
###### Example

Given a [[pointed space|pointed]] [[connected topological space]] $(X,a)$, its first [[singular homology|singular]] [[homology group]] with coefficients in the [[integers]] is the abelianisation of its [[fundamental group]]:
$$ H_1(X,\mathbb{Z}) \cong \pi_1(X,a)^{ab} .$$
This is a [[natural isomorphism]] filling the following diagram of [[functors]]:
$$ \array {
   Top_{\geq 1}^{*/} & \overset{\pi_1}\longrightarrow & Grp \\
   \llap{U}\downarrow & & \downarrow\rlap{ab} \\
   Top & \underset{H_1({-},\mathbb{Z})}\longrightarrow & Ab Grp
} $$
(where $U$ [[forgetful functor|forgets]] the point).

This example can also be done starting with an arbitrary pointed topological space and letting $U$ take the [[connected component]] of the point.  Of course, this example really lives in [[∞ Grpd]] and so we could start with a (pointed, maybe connected) [[simplicial set]], [[Kan complex]], etc.
=--

For more discussion of this see at _[[singular homology]]_ the section _[Relation to homotopy groups](singular%20homology#RelationToHomotopyGroups)_.


#### Free abelian groups

A [[free abelian group]] on a set $S$ is the abelianization of the [[free group]] on $S$.

In other words, if $F \colon Set \to Grp$ is the [[free group]]-functor and $F_{Ab} \colon Set \to Ab$ is the [[free abelian group]] functor, then 

$$
  \array{
    Set &&\stackrel{F_{ab}}{\to}&& Ab
    \\
    & {}_{\mathllap{F_{grp}}}\searrow && \nearrow_{\mathrlap{(-)^{ab}}}
    \\
    && Grp
  }
$$ 

commutes up to a canonical isomorphism. This is because we have a corresponding commutative diagram of forgetful functors 

$$
  \array{
    Set &&\stackrel{U_{ab}}{\leftarrow}&& Ab
    \\
    & {}_{\mathllap{U_{grp}}}\nwarrow && \swarrow_{\mathrlap{U}}
    \\
    && Grp
  }
$$ 

and $(-)^{ab} \circ F_{grp}$ is left adjoint to $U_{grp} \circ U$. 


## For monoids etc

Abelianisation of monoids works pretty much like abelianisation of groups.

We can also do abelianisation of [[monoid objects]] in many [[monoidal categories]] (or [[closed categories]] or more generally [[multicategories]]).  For example, we can form abelianisations of [[rings]], which are monoid objects in [[Ab]].

We can even form abelianisations of [[semigroups]] or [[magmas]].


## For Lie algebras

Lie algebras are not monoid objects in any category, but one still considers [[abelian Lie algebras]], which may be identified with their underlying [[vector spaces]].  These are so called because they correspond to abelian [[Lie groups]].  Lie algebras also can be abelianised.


[[!redirects abelianization]]
[[!redirects abelianizations]]
[[!redirects abelianisation]]
[[!redirects abelianisations]]
