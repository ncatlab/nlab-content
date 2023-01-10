+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition ##

In a [[dependent type theory]] with [[identity types]], a **subtype** of a [[type]] $A$ is a type $B$ with a term $i: B \subseteq A$, with the inclusion relation defined as the [[bracket type]] of the [[embedding type]] from $B$ to $A$:
$$B \subseteq A \coloneqq [B \hookrightarrow A]$$ 
indicating the mere existence of an [[embedding]]. $A$ is a **supertype** of $B$. 

This is different from a subtype with a chosen embedding $i:B \hookrightarrow A$, in the same way that [[inhabited sets]] and [[pointed sets]] are different. However, equipping a type with an explicit embedding is usually more useful in mathematics without the [[axiom of choice]]. 

In a [[dependent type theory]] with [[identity types]] and a hierarchy of [[type universes]] a la Tarski, given a universe $(\mathcal{U},\mathcal{T}_{\mathcal{U}})$ a subtype of a type $A:\mathcal{U}$ is a function $B:\mathcal{T}_{\mathcal{U}}(A) \to \mathrm{Prop}_\mathcal{U}$. In a universe these are the same as subtypes equipped with an embedding as structure. 

The type of all subtypes of $B$ in a universe is defined as 

$$Sub_\mathcal{U}(B) \coloneqq \sum_{A:\mathcal{U}} \mathcal{T}_\mathcal{U}(A) \subseteq B$$

## See also ##

* [[subobject]]

* [[embedding]], [[embedding type]]

* [[n-monomorphism]]

* [[coercion]]

[[!redirects subtypes]]
[[!redirects subtyping]]

[[!redirects supertype]]
[[!redirects supertypes]]

[[!redirects type of subtypes]]