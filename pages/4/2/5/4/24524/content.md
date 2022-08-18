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

We consider rigs as having an additive unit $0$, a multiplicative unit $1$ and being such that $0.x=x.0=0$, as in the entry [[rig]].

We recall that a [[rig]] [[homomorphism]] $f:R \rightarrow S$ is a funtion which is a [[monoid]] homorphism for both the additive [[underlying]] monoid and the multiplicative underlying monoid.

## Initial object

\begin{proposition}
$\mathbb{N}$ is an [[initial object]] in **Rig**.
\end{proposition}
\begin{proof}
Let $R$ be a rig and suppose that we have a morphism $f:\mathbb{N} \rightarrow R$. Then $f(n) = n.f(1) = n.1_{R}$. Let's verify that if we have any rig $R$, we indeed define a rig homomorphism by putting $f(n)=n.1_{R}$. We obviously have $f(1)=1_{R}$, $f(0)=0.1_{R}=0_{R}$. We have $f(n+p)=(n+p).1_{R}=(n.1_{R})+(p.1_{R})$ (by induction) and $f(np)=np.1_{R}=(n.1_{R})(p.1_{R})$ (by induction).
\end{proof}

