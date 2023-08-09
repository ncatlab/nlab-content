
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
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

A family of [[axioms]] depending on parameters.

Axiom schemata are formalized in a [[deductive system]] by the use of [[inference rules]] which have [[hypotheses]]. For example, the [[axiom schema of replacement]] in [[set theory]] is given by the following [[inference rule]]:

$$\frac{\Gamma, x, y \vdash \phi(x, y) \; \mathrm{prop} \quad \Gamma \vdash a \quad \Gamma \vdash \forall x.(x \in a) \implies \exists! y.\phi(x, y) \; \mathrm{true}}{\Gamma \vdash \{y \vert \exists x.(x \in a) \implies \phi(x, y)\}}$$

Compare with the bare notion of [[axiom]], which are inference rules without any hypotheses. 

## Examples

* [[axiom schema of separation]]

* [[axiom schema of replacement]]

* The [[set-theoretic axiom of choice]] in bare [[Martin-Löf type theory]] or [[cubical type theory]] with a [[type of all propositions]] $\mathrm{Prop}$ but without any general [[type universes]] is an axiom schema, since without universes one cannot quantify over sets as one could in [[set theory]] or in a [[type theory]] with [[universes]], and so the only way to express the axiom of choice is as an inference rule with a hypothesis; i.e. an axiom schema. 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{ac}_{A, B}:(\mathrm{isSet}(A) \times \Pi x:A.\mathrm{isSet}(B(x))) \to (\Pi P:((\Sigma x:A.B(x)) \to \mathrm{Prop}).(\exists y:B(x).P(x, y)) \to (\exists g:(\Pi x:A.B(x)).\Pi x:A.P(x, g(x))))}$$

## Related concepts

* [[inference rule]]

## References

See also:

* Wikipedia, *[Axiom schema](https://en.wikipedia.org/wiki/Axiom_schema)*

[[!redirects axiom schemas]]
[[!redirects axiom schemata]]

[[!redirects axiom scheme]]
[[!redirects axiom schemes]]
