
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--

# Set-level foundations
* toc
{: toc}

## Definition

By **set-level foundations** we mean any [[foundation of mathematics]] in which *all* the basic objects are, or behave like, [[sets]].  This includes:

* axiomatic [[set theory]] of all sorts:
  * [[material set theory]], such as [[ZFC]] and its variations
  * [[structural set theory]], such as [[ETCS]] and [[SEAR]].
* [[set-level type theory]], including both
  * definitionally [[extensional type theory]]
  * propositionally/typally extensional type theory, such as [[MLTT]] with [[UIP]], [[Lean]], the default type theory of [[Agda]], [[observational type theory]], and [[XTT]].

By contrast, "set-level foundations" does *not* include foundations of mathematics such as [[homotopy type theory]] in which there are basic objects of higher [[h-level]], which behave like [[groupoids]] or [[infinity-groupoids]] (or even [[categories]] or [[infinity-categories]]).  We call these [[higher-level foundations]].

### Characteristic axiom

Even though all the basic objects in a set-level foundation are sets, it's of course possible to talk about objects of higher [[h-level]] (e.g., via [[Kan complexes]], [[model categories]], [[quasicategories]], etc.). However, as compared to a higher-level foundation, in any set-level foundation, these objects will satisfy the principle that [[sets cover]]. For example, in a set-level foundation, every [[homotopy type]] admits a surjection from a set and every [[(∞,1)-category]] admits a surjection from a set to its [[core]] [[∞-groupoid]].

The axiom of "sets cover" is not equivalent to being set-level, however.  Even if we add this axiom to a higher foundation it remains "higher", since it still has basic objects of higher h-level, even if they are each covered by some set.
