
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
{:toc} 

## Definition

A [[functor]] $F \colon  C \to D$ is **continuous** if it [[preserved limit|preserves]] all small ([[weighted limit|weighted]]) [[limits]] that exist in $C$, i.e. if for 
every [[small category]] [[diagram]] $A \colon E \to C$ in $C$ the limit $\lim (F \circ A)$ exists and the natural [[map]] induced by the [[universal property]] of the limit

$$
  F(\lim A) \longrightarrow \lim (F\circ A)
  
$$

is an [[isomorphism]].

Since all limits can be obtained from (small) [[products]] and binary [[equalizers]], it follows that a functor from a [[complete]] category is continuous if and only if it preserves all products and all binary equalizers.

## Relation to other concepts

* The [[adjoint functor theorem]] states that any continuous functor between [[complete category|complete]] categories has a [[adjoint functor|left adjoint]] if it satisfies a certain 'small solution set' criterion.

* If $C$ has finite [[limit]]s, then functors commuting 
with these _finite_ limits are precisely what are
called left [[exact functor]]s.  Sometimes they are called "finitely continuous."


#Examples#

* The archetypical example is the [[Set]]-valued [[hom-functor]]: its continuity in both arguments is indeed equivalent to the very definition of [[limit]]: for 
$F : D^{op} \to C$ a diagram and $c \in C$, the covariant [[hom-functor]] $Hom_C(c,-) : C \to Set$ satisfies by definition of [[limit]]
$$
  Hom_C(c, \lim F)
  \simeq
  \lim Hom(c,F(-))
  \,.
$$

## Warnings

1. It is not enough to demand that there exists an abstract isomorphism $F(\lim A) \cong \lim (F\circ A)$.

2. Topologists sometimes use "continuous functor" to mean a [[Top]]-[[enriched functor]], since a functor between topologically [[enriched categories]] is enriched iff its actions on hom-spaces are [[continuous functions]].

3. Sheaf-theorists sometimes say "continuous functor" for a [[cover-preserving functor]] between [[sites]], with the intuition being that it generalizes the [[inverse image]] induced by a [[continuous function]] of topological spaces.

4. H. Bass in his treatment of [[K-theory]] uses the older term 'right continuous functor' for the dual notion of [[cocontinuous functor]] in a version which is [[additive functor|additive]]. If the domain of an additive functor which commutes with direct sums is a [[cocomplete category]], then the functor automatically has [[adjoint functor|right adjoint]]. Following this fact, some people in ring theory and noncommutative geometry use the simple term 'continuous functor' for a functor with a right adjoint (even if the domain [[abelian category]] is not cocomplete). In general, of course, this is just a bit more than *co*continuous in the standard sense.

## Examples

\begin{example}
Every [[right adjoint functor]] is continuous, since [[right adjoints preserve limits]].
\end{example}

## Related concepts

* [[cocontinuous functor]]

* [[complete category]]

* [[adjoint functor theorem]]


[[!include properties of functors -- contents]]



## References


* [[Peter Freyd]], [[Max Kelly]], *Categories of continuous functors*, J. Pure. Appl. Algebra **2** (1972) 169-191 &lbrack;<a href="https://doi.org/10.1016/0022-4049(72)90001-1">doi:10.1016/0022-4049(72)90001-1</a>&rbrack;

[[!redirects continuous functors]]


