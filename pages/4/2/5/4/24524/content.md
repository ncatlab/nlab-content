+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

[[Rigs]] and rig [[homomorphisms]] form the [[category]] **Rig**.

## Definition

We consider rigs as having an additive [[unit]] $0$, a multiplicative [[unit]] $1$ and being such that $0.x = x.0 = 0$, as discussed in the entry *[[rig]]*.

We recall that a [[rig]] [[homomorphism]] $f \colon R \rightarrow S$ is a [[function]] which is a [[monoid]] [[homomorphism]] for both the additive [[underlying]] monoid and the multiplicative underlying monoid.

## Properties

\begin{proposition}
**(initial object)**
\linebreak
The rig of [[natural numbers]], $\mathbb{N}$, is an [[initial object]] in **Rig**.
\end{proposition}
\begin{proof}
Let $R$ be any rig. 
First suppose that we have a [[homomorphism]] $f \colon \mathbb{N} \rightarrow R$. Then $f(n) = n.f(1) = n.1_{R}$. This shows that if such a homomorphism exists, then it is unique.
To show existence, let's verify that we indeed define a rig homomorphism by setting $f(n)=n.1_{R}$. First, we obviously have $f(1)=1_{R}$, $f(0)=0.1_{R}=0_{R}$. Moreover, by [[induction]] on $n, p \,\in\, \mathbb{N}$ we have $f(n+p)=(n+p).1_{R}=(n.1_{R})+(p.1_{R})$ and $f(n p) = n p.1_{R}=(n.1_{R})(p.1_{R})$.
\end{proof}

