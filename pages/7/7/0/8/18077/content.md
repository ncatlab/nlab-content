
# Contents
* table of contents
{: toc}

## Definition

The **law of double negation** is the statement that the [[double negation]] of a [[proposition]] [[implication|implies]] that proposition

$$
  \not \not A \Rightarrow A
  \,.
$$

In [[classical logic]], this is simply true.  In [[constructive logic]], it is equivalent to the law of [[excluded middle]] (because $\not \not (P \vee \not P)$ is a constructive theorem), and is not assertable in general.

## In dependent type theory

In [[dependent type theory]], the law of double negation states that given a type $A$ and a witness that it is an [[h-proposition]], one could derive that one could get an element of $A$ in the context of a function from the function type from $A$ to the [[empty type]] to the [[empty type]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, a:A, b:A \vdash \mathrm{proptrunc}_A(a, b):a =_A b}{\Gamma, c:(A \to \emptyset) \to \emptyset \vdash \mathrm{doubleneg}(c):A}$$

If one doesn't have function types, the law of double negation could be expressed as

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, a:A, b:A \vdash \mathrm{proptrunc}_A(a, b):a =_A b}{\Gamma, a:A, b(a):\emptyset, c(a, b):\emptyset \vdash \mathrm{doubleneg}(a, b, c):A}$$

## Related concepts

* [[excluded middle]]

* [[closed subspace]]


## References

* [[eom]] _[Double negation, law of](https://www.encyclopediaofmath.org/index.php/Double_negation,_law_of)_


[[!redirects law of double negation]]
[[!redirects double negation law]]
