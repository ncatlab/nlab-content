

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc} 

## Definition

### Explicitly

A **section** of a [[morphism]] $f : A \to B$ in some [[category]] is a **right-[[inverse]]**: a [[morphism]] $\sigma : B \to A$ such that
$$
  f \circ \sigma : B \stackrel{\sigma}{\to} A \stackrel{f}{\to} B
$$
equals the [[identity morphism]] on $B$.

Typically $A \stackrel{f}{\to} B$ is thought of as a [[bundle]] and then one speaks of sections of bundles. For topological bundles one considers _continuous sections_, for smooth bundles _smooth sections_, etc.

### In terms of dependent product
 {#InTermsOfDependentProduct}

In a [[locally cartesian closed category]] $\mathcal{C}$, regard the morphism $f\colon A \to B$ as an object $[f] \in \mathcal{C}_{/B}$ in the [[slice category]] over $B$. Then there is the [[dependent product]]

$$
  \underset{B}{\prod} [f] \in \mathcal{C}
  \,.
$$

This is the [[space of sections]] of $f$. A single section $\sigma$ is a [[global element]] in here

$$
  \sigma \colon \ast \to \underset{B}{\prod} [f]
  \,.
$$ 

See at _[dependent product -- In terms of spaces of sections](dependent%20product#RelationToSpacesOfSections)_ for more on this.

## Split idempotents

In the case that $f$ has a section $\sigma$, $f$ may also be called a [[retraction]] or **cosection** of $\sigma$, $A$ may be called a [[retract]] of $B$, and the entire situation is said to split the [[idempotent]]
$$
  A \stackrel{f}{\to} B \stackrel{\sigma}{\to} A
  \,.
$$

A **[[split epimorphism]]** is a morphism that *has* a section; a **[[split monomorphism]]** is a morphism that *is* a section.  A [[split coequalizer]] is a particular kind of split epimorphism.

## Sections of bundles and sheaves

If one thinks of $f : A \to B$ as a [[bundle]] then its sections are sometimes called [[global sections]]. This leads to a notion of global sections of [[sheaves]] and further of objects in a general [[topos]]. See 

* [[global section]]

for more on this.

## Related concepts

* [[local section]], [[global section]]

* [[flat section]]

* [[space of sections]]

* [[ex-space]]

* [[field history]]

[[!redirects sections]]
[[!redirects cross section]]
[[!redirects cross-section]]
[[!redirects right inverse]]
[[!redirects right-inverse]]
[[!redirects cross sections]]
[[!redirects cross-sections]]
[[!redirects right inverses]]
[[!redirects right-inverses]]

[[!redirects smooth section]]
[[!redirects smooth sections]]

[[!redirects continuous section]]
[[!redirects continuous sections]]

