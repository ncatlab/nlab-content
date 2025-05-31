
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition


+-- {: .num_defn}
###### Definition

An [[object]] $U$ in a [[category]] $C$ is **subterminal** or **preterminal** if any two [[morphism]]s with [[target]] $U$ and the same source are equal.  In other words, $U$ is subterminal if for any object $X$, there is at most one morphism $X\to U$.

=--

+-- {: .num_defn}
###### Definition


An __[[umbrella category]]__ is a nonempty category $C$ such that for every object $X$ in $C$, there is at least one subterminal object $T$ such that $C(X,T)$ is nonempty (hence being a singleton). 

=--

## Properties

If $C$ has a [[terminal object]] $1$, then $U$ is subterminal precisely if the unique morphism $U \to 1$ is [[monomorphism|monic]], so that $U$ represents a [[subobject]] of $1$; hence the name "sub-terminal."  

This is equivalent to the hypothesis that the [[cone]] given by identity morphisms $U \leftarrow U \rightarrow U$ is a [[product]] cone, or that *some* [[product]] $U \times U$ exists and the [[diagonal]] $U \to U \times U$ is an [[isomorphism]], or that some [[product]] $U \times U$ exists and the projections $\pi_1, \pi_2 : U \times U \to U$ are equal. In a [[cartesian monoidal category]], the condition that the [[diagonal]] $U \to U \times U$ be invertible equivalently means that the unique [[comonoid]] structure on $U$ is [[idempotent monoid in a monoidal category|idempotent]].

Therefore for a [[sheaf topos]] over a [[topological space]] the subterminal objects of the topos are the [[open subsets]] of the topological space. Accordingly, the subterminal objects in any [[topos]] are also called _open objects_ (e.g. [Johnstone 77, p. 94](#Johnstone77))

The [[classifying topos]] for subterminal objects (hence open objects) in [[toposes]] is the [[Sierpinski topos]] (see e.g. [Johnstone 77, p. 117](#Johnstone77)).

## Examples

The subterminal objects in a [[topos]] can be viewed as its "external [[truth value]]s."  For example, in the topos $Sh(X)$ of [[sheaf|sheaves]] on a [[topological space]] $X$, the subterminal objects are precisely the open sets in $X$. 

The *support* of an object $X$ in a topos is the [[image]] $U \hookrightarrow 1$ of the unique map $X \to 1$. Any map $U \to X$ is necessarily a [[section]] of $X \to U$. 

## Related concepts

* [[subsingleton]]

* [[support object]]

[[!include types and logic - table]]

## References

* {#Johnstone77} [[Peter Johnstone]], _Topos theory_, London Math. Soc. Monographs __10__, Acad. Press 1977

* [[Dieter Pumplün]], _Initial morphisms and monomorphisms_, Manuscripta mathematica 32 (1980): 309-333.

[[!redirects subterminal]]
[[!redirects subterminals]]
[[!redirects subterminal objects]]

[[!redirects preterminal]]
[[!redirects preterminal object]]
[[!redirects preterminal objects]]

[[!redirects open object]]
[[!redirects open objects]]
