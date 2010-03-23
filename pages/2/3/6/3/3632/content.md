
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of **Postnikov tower in an $(\infty,1)$-category** is the  generalization of the notion of [[Postnikov tower]] from the archetypical [[(∞,1)-category]] [[Top]]$\simeq$ [[∞Grpd]] to more general $(\infty,1)$-categories.

## Definition

+-- {: .un_prop}
###### Proposition

For $C$ a [[presentable (∞,1)-category]] the subcategory $C_{\leq n}$ of [[n-truncated object in an (∞,1)-category|n-truncated objects]] is a [[reflective (∞,1)-subcategory]]

$$
  C_{\leq n} \stackrel{\overset{\tau_{\leq n}}{\leftarrow}}{\hookrightarrow}
  C
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 5.5.6.18]]

=--

We write 

$$
  \mathbf{\tau_{\leq n}} : C \stackrel{\tau_{\leq n}}{\to} C_{\leq n} \hookrightarrow C
$$

for the corresponding localization. For $X \in C$, we say that $\mathbf{\tau}_{\leq n} C$ is the **$n$-truncation of $C$**. 

The reflector of the reflective embedding provides morphisms

$$
  X \to \mathbf{\tau}_{\leq n} X
$$

from each object to its $n$-truncation.




+-- {: .un_def}
###### Definition

A **Postnikov tower** for $X \in C$ is a diagram

$$
  X \to \cdots \to X_2 \to X_1 \to X_0
$$

such that each $X \to X_n$ exhibits $X_n$ as [[generalized the|the]] $n$-truncation of $X$.

=--

This is [[Higher Topos Theory|HTT, def. 5.5.6.23]].

## Relation to other concepts

At least if the ambient $(\infty,1)$-category is a [[locally contractible (∞,1)-topos]] $\mathbf{H}$, so that there is a notion of structured [[schreiber:path ∞-groupoid]]-functor $\mathbf{\Pi} : \mathbf{H} \to \mathbf{H}$, the [[homotopy fiber]]s of the morphisms $X \to \mathbf{\Pi}_n(X)$ into the Postnikov tower of $\mathbf{\Pi}(X)$ form the

* [[Whitehead tower in an (∞,1)-topos|Whitehead tower in the (∞,1)-topos]] $\mathbf{H}$ of the object $X$.



[[!redirects Postnikov tower in an (∞,1)-category]]
[[!redirects Postnikov system in an (∞,1)-category]]
[[!redirects Postnikov system in an (infinity,1)-category]]
