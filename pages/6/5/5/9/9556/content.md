
#Contents#
* table of contents
{:toc}

## Idea

The generalization of [[∞-group]] [[∞-actions]] to $\infty$-actions of [[groupoid objects in an (∞,1)-category]].

## Definition

+-- {: .num_defn #GroupoidAction}
###### Definition

For $\mathcal{G}_\bullet \in Grpd_\infty(\mathbf{H})$ a [[groupoid object in an (∞,1)-category|groupoid object]], $P \in \mathbf{H}$ any object equipped with a morphsim $a \colon P \to \mathcal{G}_0$ to the object of objects of $\mathcal{G}$, a **$\mathcal{G}_\bullet$-[[groupoid ∞-action]]** on $X$ with **anchor** $a$ is a [[groupoid object in an (∞,1)-category|groupoid]] $(X//\mathcal{G})_\bullet$ over $\mathcal{G}_\bullet$ of the form

$$
  \array{  
    \vdots && && \vdots
    \\
    \downarrow \downarrow \downarrow \downarrow
    && &&
    \downarrow \downarrow \downarrow \downarrow
    \\
    X \underset{\mathcal{G}_0}{\times} \mathcal{G}_2
    && \to && \mathcal{G}_2    
    \\
    \downarrow \downarrow \downarrow && &&   
    \downarrow \downarrow \downarrow
    \\
    X \underset{\mathcal{G}_0}{\times} \mathcal{G}_1
    && \to && \mathcal{G}_1
    \\
    \downarrow \downarrow && && \downarrow \downarrow
    \\
    X  && \stackrel{a}{\to} && \mathcal{G}_0
  }
  \,,
$$

where the [[homotopy fiber products]] on the left are those of the anchor $a$ with the leftmost 0-face map $\mathcal{G}_{(\{0\} \hookrightarrow \{0, \cdots, n\})}$ and  the horizontal morphisms are the corresponding [[projections]] on the second factor.

We call $(X//\mathcal{G})_\bullet$ also the **[[action groupoid]]** of the action of $\mathcal{G}_\bullet$ on $(X,a)$ and call its [[realization]] $X \to (X//\mathcal{G})$ the [[homotopy quotient]] of the action.

=--

+-- {: .num_example }
###### Example

For $\mathcal{G}_\bullet = (\mathbf{B}G)_\bullet$ the [[delooping]] of a [[group object in an (∞,1)-category|group object]], def. \ref{GroupoidAction} reduces to the definition of an [[∞-action]] of the [[∞-group]] $G$.

=--

## Related concepts

* [[∞-groupoid-principal ∞-bundle]]

* [[∞-groupoid bibundle]]

[[!redirects groupoid action]]
[[!redirects groupoid actions]]

[[!redirects groupoid infinity-actions]]

[[!redirects groupoid ∞-action]]
[[!redirects groupoid ∞-actions]]

[[!redirects infinity-groupoid infinity-actions]]
[[!redirects infinity-groupoid infinity-actions]]

[[!redirects ∞-groupoid ∞-action]]
[[!redirects ∞-groupoid ∞-actions]]

