
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Finite categories
* table of contents
{: toc}

## Definition

A **finite category** $C$ is a [[category]] [[internal category|internal to]] the category [[FinSet]] of finite sets.

This means that a finite category consists of

* a finite set of [[object]]s;
* a finite set of [[morphism]]s.

(Notice that the latter implies the former, since for every object there is the [[identity morphism]] on that object). Finite categories form the [[2-category]], [[FinCat]].

Similarly, a **locally finite category** is a category [[enriched category|enriched]] over $Fin Set$, that is a category whose [[hom-set]]s are all finite.

(Locally) finite categories may also be called (locally) **$\omega$-small**; this generalises from $\omega$ (the set of [[natural number]]s) to (other) [[inaccessible cardinal]]s (or, equivalently, [[Grothendieck universe]]s).


## Limits and colimits

One is often interested in whether an arbitrary category $D$ has [[limit]]s and [[colimit]]s indexed by finite categories.  A category with all finite limits is called **[[finitely complete category|finitely complete]]** or **left exact** (or **lex** for short).  A category with all finite colimits is called **finitely cocomplete** or **right exact**.

## In dependent type theory

In dependent type theory, there are multiple notions of category. Because the type of objects in a category is required to be a [[finite set]], all finite categories are [[strict categories]], and the only finite [[univalent categories]] are the finite [[gaunt categories]]. 

## Related concepts

* [[finite set]]

* [[finite graph]]

* [[homotopy type with finite homotopy groups]]

* [[finite homotopy type]]

* [[finite (∞,1)-category]]

* [[locally finite type]]

* [[finitely complete category]], [[finitely cocomplete category]]


[[!redirects finite category]]
[[!redirects finite categories]]
[[!redirects locally finite category]]
[[!redirects locally finite categories]]
