
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Positive types
* table of contents
{: toc}

## Idea

In [[type theory]], a **positive type** is one whose *constructors* are regarded as primary.  Its eliminators are derived from these by the rule that "to use an element of a positive type, it is necessary and sufficient to specify what should be done for all possible ways that element could have been constructed".

The opposite notion is a [[negative type]], forming two [[polarity in type theory|polarities]].


In [[categorical semantics]] of type theory, positive types correspond to "from the left" [[universal properties]] (i.e. for mapping out).

In [[denotational semantics]], positive types behave well with respect to "[[call-by-value]]" and other [[eager evaluation]] strategies.


## Examples

* [[inductive type]]
  * [[sum type]]
  * [[product type]] (but see below)
  * [[dependent sum type]] (but see below)
  * [[empty type]]
  * [[unit type]] (but see below)
  * [[identity type]]

* [[unit types]], [[dependent sum types]] and cartesian [[product types]] can be presented both positively (as a particular inductive type) and negatively.  The two definitions are equivalent in ordinary type theory, but distinct in [[linear logic]].  The same is true for binary [[sum types]] if we allow [[sequents]] with multiple conclusions.

[[!redirects positive types]]
