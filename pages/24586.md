
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
* [[extensional type theory]], including both
  * definitionally extensional type theory
  * propositionally/typally extensional type theory, such as [[MLTT]] with [[UIP]], the default type theory of [[Agda]], [[observational type theory]], and [[XTT]].

By contrast, "set-level foundations" does *not* include foundations of mathematics in which there are basic objects of higher [[h-level]], which behave like [[groupoids]] or [[infinity-groupoids]] (or even [[categories]] or [[infinity-categories]]).  Thus, it excludes:

* [[homotopy type theory]] of all sorts:
  * [[Book HoTT]]
  * [[cubical type theory]], including CCHM cubical type theory, Cubical Agda, and Cartesian cubical type theory
  * [[higher observational type theory]]
* More generally, [[intensional type theory]], in which no types of higher h-level can be shown to exist, but neither can all types be shown to be [[h-sets]].
* Hypothetical elementary theories of the [[bicategory]] of [[categories]] and the [[(2,1)-category]] of [[groupoids]], expressed in [[first-order logic]] with dependent sorts in the same way that [[ETCS]] is.  One extant theory along these lines is [[ETCC]], although it hasn't been successfully made into a full [[foundation of mathematics]].

### Characteristic axiom

Even though all the basic objects in a set-level foundation are sets, it's of course possible to talk about objects of higher [[h-level]] (e.g., via [[Kan complexes]], [[model categories]], [[quasicategories]], etc.). However, as compared to a higher-level foundation, in any set-level foundation, these objects will satisfy the principle that [[sets cover]]. For example, in a set-level foundation, every [[homotopy type]] admits a surjection from a set and every [[(∞,1)-category]] admits a surjection from a set to its [[core]] [[∞-groupoid]].