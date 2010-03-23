

+-- {: .query}

[[Urs Schreiber]]: here is something [[Domenico Fiorenza]] and myself were thinking about

=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

If an [[(∞,1)-topos]] $\mathbf{H}$ is [[locally contractible (∞,1)-topos|locally contractible]] it has a good notion of  [[homotopy groups in an (∞,1)-topos|geometric homotopy groups]] of its objects. In terms of these, there is an analog in $\mathbf{H}$ of the notion of the classical notion of [[Whitehead tower]] in the archetypical $(\infty,1)$-topos [[Top]]:

the Whitehead tower of an object $X \in \mathbf{H}$ is the tower of [[homotopy fiber]]s of the canonical morphism into the [[Postnikov tower in an (∞,1)-category|(∞,1)-topos-theoretic Postnikov tower]] $\cdots \to \mathbf{\Pi}_{n+1}(X) \to \mathbf{\Pi}_n(X) \to \cdots$ of the [[schreiber:path ∞-groupoid|structured path ∞-groupoid]] $\mathbf{\Pi}(X)$ of $X$.

## Definition

Let $\mathbf{H}$ be a [[locally contractible (∞,1)-topos]] $\mathbf{H} \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}} \infty Grpd$. Write 

$$
  \mathbf{\Pi} := LConst \circ \Pi : \mathbf{H} \to \mathbf{H}
$$

for the _internal_ [[schreiber:homotopy ∞-groupoid]] functor. From the adjunction relation this comes with the canonical natural morphism

$$
  X \to \mathbf{\Pi}(X)
  \,.
$$

For $n \in \mathbb{N}$ write

$$
  \mathbf{H}_{\leq n} \stackrel{\overset{\tau_{\geq n}}{\leftarrow}}{\overset{}{\hookrightarrow}} \mathbf{H}
$$

for the [[reflective (∞,1)-subcategory]] of [[n-truncated object of an (∞,1)-category|n-truncated objects]] of $\mathbf{H}$ and write $\mathbf{\tau}_{\leq n}$ for the [[localization of an (∞,1)-category|localization]]

$$
  \mathbf{\tau}_{\leq n} : \mathbf{H} \stackrel{\tau_{\leq n}}{\to}
  \mathbf{H}_{\leq n} \hookrightarrow \mathbf{H}
  \,.
$$

Write

$$
  \mathbf{\Pi}_n : \mathbf{H} \stackrel{\mathbf{\Pi}}{\to} \mathbf{H} \stackrel{\mathbf{\tau}_{\leq n}}{\to} \mathbf{H}
$$

for the internal **homotopy $n$-groupoid**. For $X \in \mathbf{H}$ we have the [[Postnikov tower in an (∞,1)-category|(∞,1)-Postnikov tower]]

$$
  \cdots \to \mathbf{\Pi}_2(X) \to \mathbf{\Pi}_1(X) \to \mathbf{\Pi}_0(X)
$$

of $\mathbf{\Pi}(X)$.

+-- {: .un_def}
###### Definition
**(Whitehead tower)**

For $X \in \mathbf{H}$, its **Whitehead tower** is the sequence of objects 

$$
  * \to \cdots \to X^{(2)} \to X^{(1)} \to X^{(0)} \simeq X
$$

in $\mathbf{H}$, where for each $n \in \mathbb{N}$ the object $X^{(n+1)}$ is the [[homotopy fiber]] of the canonical morphism $X \to \mathbf{\Pi}_{n+1}$, i.e. the object defined by the [[pullback]] diagram

$$
  \array{
    X^{(n+1)} &\to& *
    \\
    \downarrow && \downarrow
    \\
    X &\to& \mathbf{\Pi}_{n+1}(X)
  }
  \,.
$$

=--

Here the morphisms $X^{(n+1)} \to X^{(n)}$ are induced from the universality of the pullback:


$$
  \array{
    X^{(n+1)}&\to&X^{(n)}&& \mathbf{\Pi}_{(n+1)}(X)
    \\
    &\searrow &\downarrow&\nearrow& \downarrow
    \\
    &&X &\to& \mathbf{\Pi}_n(X)
  }
$$

+-- {: .un_remark}
###### Remark


We have that $\mathbf{\Pi}_n(X) \simeq LConst \tau_{\leq n} \Pi(X)$.

A homotopy-commuting diagram

$$
  \array{
    X^{(n)} &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    X &\to& \mathbf{\Pi}_n(X)
  }
$$

in $\mathbf{H}$ corresponds by the [[adjoint (∞,1)-functor|adjunction relation]] to diagram 

$$
  \array{
    \Pi(X^{(n)}) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    \Pi(X) &\to& {\Pi}_n(X)
  }
$$

in [[∞Grpd]]. This being universal means that $\Pi(X^{(n)})$ is $n$-connected, and universal with that property as an object over $\Pi(X)$.

=--


## Examples

### In $Top$

In $\mathbf{H} = Top \simeq $ [[∞Grpd]] the functors $\Pi$ and $\mathbf{\Pi}$ are the identity and so 
$\cdots \to \mathbf{\Pi}_1(X) \to \mathbf{\Pi}_0(X)$ is just the standard [[Postnikov tower]] $\cdots \to X_1 \to  X_0 $.

[[!redirects Whitehead tower in an (∞,1)-topos]]
