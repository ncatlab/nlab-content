
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A **Horn theory** is a [[theory]] in which every axiom has certain special form.

## Definition

Let $\Sigma$ be a [[signature (in logic)|signature]]. A **term** of $\Sigma$ is an expression built out of variables and function symbols. For example, $x y^{-1} z$ is a term in the language of groups. An **atomic formula** relative to $\Sigma$ is a formula that consists of a relation symbol of $\Sigma$ (including equality) applied to terms. A **Horn clause** is a logical expression of the form 

$$\phi_1 \wedge \ldots \wedge \phi_n \vdash \phi$$ 

where each $\phi_i$ and $\phi$ is atomic. A (universal) **Horn theory** is a [[theory]] in which every axiom is a Horn clause. 