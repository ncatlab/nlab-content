
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### Directed homotopy type theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

In [[simplicial type theory]], a **skeletal Segal type** is a [[Segal type]] $A$ such that for all $x:A$ and $y:A$ the canonical function which by the [[J rule]] takes an identification of elements $p:x =_A y$ to a witness that $x$ and $y$ are [[isomorphism in a Segal type|merely isomorphic]] 
$$\vert J(\lambda t.\mathrm{id}_A(t), x, y, p) \vert:[\mathrm{iso}_A(x, y)]$$ 
is an [[equivalence of types]], where $[A]$ is the [[propositional truncation]] of $A$.  

$$\mathrm{isSkeletal}(A) \coloneqq \mathrm{isSegal}(A) \times \prod_{x:A} \prod_{y:A} \mathrm{isEquiv}(\lambda p.\vert J(\lambda t.\mathrm{id}_A(t), x, y, p) \vert)$$ 

Every skeletal Segal type is a [[set]]. 

## Related concepts

* [[Segal type]]

* [[complete Segal type]]

* [[skeletal category]]

* [[gaunt Segal type]]

* [[isomorphism in a Segal type]]

[[!redirects skeletal Segal type]]
[[!redirects skeletal Segal types]]