
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

A __bicartesian closed category__ is a [[cartesian closed category]] with finite [[coproducts]]. In the case where this is furthermore a [[preorder]] or [[poset]], it is called a [[Heyting prealgebra]] or [[Heyting algebra]], respectively. They provide the semantics and proof theory of [[intuitionistic logic|intuitionistic]] [[propositional logic]].


Note that a bicartesian closed category is [[bicartesian category|bicartesian]] (that is, it is both [[cartesian monoidal category|cartesian]] and [[cocartesian monoidal category|cocartesian]]), and furthermore it is cartesian closed, but it is usually *not* [[cocartesian closed category|cocartesian closed]] (as the only such category is the trivial terminal category), nor co-(cartesian closed) (i.e., the dual of a cartesian closed category; aka, cocartesian coclosed). Thus the terminology could be confusing, but since the only categories which are both cartesian closed and co-(cartesian closed) are preorders, there is not much danger.

Also note that a bicartesian closed category is automatically a [[distributive category]]. This follows since the functors $X\mapsto A\times X$ have right adjoints (by closedness), so they preserve colimits. 

A bicartesian closed category is one kind of [[2-rig]].

## See also

* [[bicartesian closed preordered object]]