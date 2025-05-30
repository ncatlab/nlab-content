
{:warning: .un_remark style="border:solid #cc0000;background: #fe0000;border-width:2px 1px;padding:2px 1em;margin:2px 1em;"}


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

## Idea

This entry is meant to be about the analog of the notion of *[[simplicial skeleta]]* for [[types]] of [[simplicial type theory]].



## Definition

+-- {: warning}
###### Warning

The following definition is lacking reference or justification.

=--

In [[simplicial type theory]], given some notion of [[isomorphism in simplicial type theory|isomorphism]] $\mathrm{iso}_A(x, y)$, a **skeletal type** is a [[type]] $A$ such that for all $x:A$ and $y:A$ the canonical function which by the [[J rule]] takes an identification of elements $p:x =_A y$ to a witness that $x$ and $y$ are [[isomorphism in a Segal type|merely isomorphic]] 
$$\vert J(\lambda t.\mathrm{id}_A(t), x, y, p) \vert:[\mathrm{iso}_A(x, y)]$$ 
is an [[equivalence of types]], where $[A]$ is the [[propositional truncation]] of $A$.  

$$\mathrm{isSkeletal}(A) \coloneqq \prod_{x:A} \prod_{y:A} \mathrm{isEquiv}(\lambda p.\vert J(\lambda t.\mathrm{id}_A(t), x, y, p) \vert)$$ 

Every skeletal type is a [[set]]. If $A$ is also a [[Segal type]], then the notion corresponds to the concept of a [[skeletal category|skeletal]] [[(infinity,1)-category]]. 

## Related concepts

* [[skeleton]]

* [[Rezk complete type]]

* [[gaunt type]]

* [[isomorphism in simplicial type theory]]

[[!redirects skeletal type]]
[[!redirects skeletal types]]

[[!redirects skeletal Segal type]]
[[!redirects skeletal Segal types]]