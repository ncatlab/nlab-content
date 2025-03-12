
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

For $p$ a [[prime number]], a [[group]] is _$p$-primary_ if each of its elements $g$ has a [[prime power]] [[order of a group|order]] $p^{n(g)}$.

(Also called _primary group_ a _$p$-group_, but NO relation to _[[n-group]]_.)

## Properties

### Relation to finite abelian group

The [[fundamental theorem of finite abelian groups]] stats that every [[finite abelian group]] is a [[direct sum]] of its $p$-primary subgroups.

These are often called its _$p$-primary parts_ or _$p$-primary components_. See also at _[[Adams spectral sequence]]_ and for instance at _[[stable homotopy groups of spheres]]_.

### Nilpotency 

+-- {: .num_prop #center} 
###### Proposition 
Every [[finite set|finite]] $p$-primary group $G$ has a nontrivial [[center of a group|center]] $Z(G)$. 
=-- 

For a proof, see [[class equation]]. 

Since the center $Z(G)$ is a [[normal subgroup]] of $G$, we may define by induction (with the help of this proposition [here](/nlab/show/normal+subgroup#inverse)) a series of inclusions of normal subgroups $Z^k(G) \subseteq G$ where $Z^0(G)$ is the trivial subgroup and $Z^k(G)$ is the inverse image of the center $Z(G/Z^{k-1}(G))$ along the canonical homomorphism $G \to G/Z^{k-1}(G)$. The resulting series 

$$Z^0(G) \subseteq \ldots \subseteq Z^{k-1}(G) \subseteq Z^k(G) \subseteq \ldots$$ 

is called the *upper central series* of $G$, and Proposition \ref{center} shows that in the case of a finite $p$-group, this series consists of strict inclusions that eventually terminate in the full subgroup $G$. A group with that property is a [[nilpotent group]]. In particular it is a [[solvable group]]. 

## Examples

* for the primary components of the [[stable homotopy groups of spheres]] see at _[homotopy groups of spheres -- Table](homotopy+groups+of+spheres#Tables)_.

## Related concepts

* [[stem]]

* [[elementary group]]

## References

* {#Sullivan} John Sullivan, _Classification of finite abelian groups_ ([pdf](http://www.isama.org/jms/m317/handouts/finabel.pdf))
 


[[!redirects p-primary groups]]

[[!redirects p-group]]
[[!redirects p-groups]]


[[!redirects primary group]]
[[!redirects primary groups]]

[[!redirects p-primary component]]
[[!redirects p-primary components]]

