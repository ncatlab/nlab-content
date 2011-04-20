
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A _logical morphism_ or _logical functor_ is a [[homomorphism]] between [[elementary topos]]es that preserves the structure of a topos as a context for [[logic]]: a functor which preserves all the elementary topos structure, including in particular [[power objects]], but not necessarily any infinitary structure (such as present additionally in [[sheaf topos]]).  

If instead a topos is regarded as a context for [[geometry]] or specifically [[geometric logic]], then the notion of [[homomorphism]] preserving this is that of a  _[[geometric morphism]]_ . 

## Definition

Since all the topos structure follows from having [[finite limits]] and [[power objects]], it suffices to define a logical functor to preserve these.  It then follows that it is also a [[locally cartesian closed functor]], a [[Heyting functor]], etc.

## Properties

### Preserved structures

In particular, a logical functor preserves the truth of all sentences in the [[internal logic]].  If it is moreover [[conservative functor|conservative]], then it also *reflects* the truth of such sentences.  For example, the [[transfer principle]] of [[nonstandard analysis]] can be stated as the fact that a certain functor is logical and conservative.

### Relation to geometric morphisms

The difference between geometric and logical functors between toposes is, in a certain sense, a [[categorification]] of the difference between a [[homomorphism]] of [[frames]] and a homomorphism of [[Heyting algebras]].  When the latter are [[complete lattice|complete]], these are the same objects with the same [[isomorphisms]] but different morphisms.  

However, while frame homomorphisms naturally categorified by geometric functors, a more precise categorification of Heyting algebra homomorphisms would be [[Heyting functors]], which preserve the internal first-order logic, but not the higher-order logic as logical functors do.


[[!redirects logical functor]]
[[!redirects logical functors]]
[[!redirects logical morphism]]
[[!redirects logical morphisms]]
