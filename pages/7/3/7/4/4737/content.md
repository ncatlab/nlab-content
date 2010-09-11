
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

* [[principal bundle]] / [[torsor]] / **groupoid principal bundle**

* [[principal 2-bundle]] / [[gerbe]] / [[bundle gerbe]]

* [[principal 3-bundle]] / [[bundle 2-gerbe]]

* [[principal ∞-bundle]]

***


#Contents#
* table of contents
{:toc}

## Idea

For $\mathcal{G}$ a [[groupoid object in an (infinity,1)-category|groupoid object]] a _$\mathcal{G}$-principal bunde_ is a [[morphism]] $P \to X$ with an principal [[action]] of $\mathcal{G}$ on $P$.

## Definition

For $G$ a [[group object]] in some [[(infinity,1)-topos]] $\mathbf{H}$ (for instance that of [[infinity-Lie groupoid]]s for smooth groupoid bundles), and $\mathbf{B}G$ the corresponding [[delooping]] object, $G$-principal bundles are the [[(infinity,1)-pullback]]s of the form

$$
  \array{
    P &\to& * 
    \\
    \downarrow && \downarrow
    \\
    X &\to& \mathbf{B}G
  }
  \,.
$$

One equivalently (with non-negligible but conventional chance of confusion of terminology) calls such $P \to G$ a $\mathbf{B}G$-**groupoid principal bundle.

So more generally, for $\mathcal{G}$ any groupoid object with collection $\mathcal{G}_0$ of [[object]]s, the $(\infty,1)$-pullbacks

$$
  \array{
    P &\to& \mathcal{G}_0
    \\
    \downarrow && \downarrow
    \\
    X &\to& \mathcal{G}
  }
$$

are **groupoid principal bundles** .

## Examples

For $\mathbf{H}$ = $\infty LieGrpd$ and $\mathcal{G}$ a [[Lie groupoid]], a $\mathcal{G}$-prinipal bundle is locally of the form

$$
  U_i \times \mathcal{G}_{x_i}
$$

for $\mathcal{G}_{x_i}$ the source fiber over an object $x_i$.

## Applications

* As groupoid [[bibundle]], groupoid principal bundles serve as models for morphisms between [[Lie groupoid]]s.