
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Judgments
* table of contents
{: toc}

## Idea

In [[formal logic]], a __judgment__, or __judgement__, is a "meta-[[proposition]]"; that is, a proposition belonging to the [[meta-language]] rather than to the [[object language]].


## Examples

Two examples of judgements are "The formula $\phi$ has no free variables" or "The string $\phi$ of symbols is a well-formed formula".

### Non-hypothetical judgements

One very important type of judgement is that of the derivability of a formula $\phi$ in a given calculus consisting of logical axioms and inference rules. This judgement is written like that:
$$\vdash \phi.$$

This judgement is not the same thing as the formula $\phi$ itself. In fact, $\phi$ is a statement *in* the logic, while $\vdash\phi$ is a statement *about* the logic. One uses non-hypothetical judgements when working with a *Hilbert system*.

### Hypothetical judgements

It may happen that a proposition $\phi$ is only derivable under the assumption of a set of axioms $\Gamma$. The judgement that expresses this situation is written
$$\Gamma\vdash \phi.$$

This type of judgement is often used in the context of *natural deduction systems*. 

## Sequents vs. judgements

Note that such a natural deduction system deals with so-called *sequents*, which are ordered pairs of the form $(\Gamma, \phi)$ where $\Gamma$ is a set of formulae and $\phi$ is a single formula; and these sequents are also often written $\Gamma\vdash\phi$. One therefore has to distinguish between the judgement $\Gamma\vdash\phi$, which is a statement in the metatheory, and the expression $\Gamma\vdash\phi$ which denotes a sequent (and is therefore a mathematical object).

For instance, in order to conclude the truth of an [[implication]] $\phi\rightarrow\psi$, we must conclude $\psi$ *assuming* $\phi$; thus the [[introduction rule]] for implication is
$$ \frac{\{\phi\} \vdash \psi}{\emptyset\vdash\phi\rightarrow\psi}$$
with a hypothetical formula $\phi$ as its hypothesis and another formula $\psi$ as its [[conclusion]]. In this inference rule, $\{\phi\} \vdash \psi$ and $\emptyset\vdash\phi\rightarrow\psi$ are sequents.