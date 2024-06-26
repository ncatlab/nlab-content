
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Negative types
* table of contents
{: toc}

## Idea

In [[type theory]], a **negative type** is one whose *[[term elimination|eliminators]]* are regarded as primary.  Its [[term introduction|constructors]] are derived from these by the rule that "to construct an element of a negative type, it is necessary and sufficient to specify how that element behaves upon applying all of the eliminators to it".

The opposite notion is that of a *[[positive type]]*, forming two [[polarity in type theory|polarities of type theory]].

In [[categorical semantics]] of type theory, negative types correspond to "from the right" [[universal properties]] (i.e. for mapping in).

In [[denotational semantics]], negative types behave well with respect to "[[call-by-name]]" and other [[lazy evaluation]] strategies.


## Examples

* [[dependent product type]]

  * [[function type]]

* [[coinductive type]]

* [[record type]]

* [[unit types]], [[dependent sum types]] and cartesian [[product types]] can be presented both positively and negatively.  The two definitions are equivalent in ordinary type theory, but distinct in [[linear logic]].  The same is true of binary [[sum types]] if we allow [[sequents]] with multiple conclusions.

[[!redirects negative types]]
