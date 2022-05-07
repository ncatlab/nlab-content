
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

## Idea

In [[type theory]], a _term in context_ is a [[term]] such as

$$
  a \colon A \; \vdash \; b(a) \colon B(a)
$$

which may involve [[free variables]] from some [[context]] (here, $a:A$).  In [[dependent type theory]], the [[type]] of a term in context may also depend on the same context, an $A$-[[dependent type]], such as

$$
  a \colon A \;\vdash \; B(a) \colon Type
  \,.
$$

## Related concepts

* [[hypothetical judgment]], [[generic judgment]]

* [[telescope]]

[[!redirects terms in context]]
