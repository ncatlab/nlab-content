+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

\tableofcontents

## Idea

*Wu's formula* is a relation between the [[cup product]] and the second [[Stiefel-Whitney class]], which connects [[spin manifold|spin]] [[topological manifold|topological]] [[4-manifold]] and even [[intersection forms]].

## Statement

\begin{proposition}
For a [[oriented]] [[closed manifold|closed]] [[topological manifold|topological]] [[4-manifold]] $M$, one has:
$$
  x \smile x
   =
  w_2(T M)\smile x
$$
for all classes $x\in H^2(M,\mathbb{Z}_2)$.
\end{proposition}

([Scorpan 05, p. 163](#Scorpan74))

## Application

An important application of Wu's formula is the connection with the [[intersection form]] $Q_M\colon H^2(M,\mathbb{Z})\times H^2(M,\mathbb{Z})\rightarrow\mathbb{Z},(x,y)\mapsto\langle x\smile y,[M]\rangle$. Considering the reduction of its diagonal, one has:
$$
  Q_M(x,x)mod 2
  =Q_M(x mod 2,x mod 2)
  =Q_M(w_2(T M),x mod 2)
$$
for all classes $x\in H^2(M,\mathbb{Z})$. It leads to the following results:

\begin{proposition}
The [[intersection form]] of a [[closed manifold|closed]] [[spin manifold|spin]] [[topological manifold|topological]] [[4-manifold]] is even.
\end{proposition}

([Scorpan 05, p. 163](#Scorpan74))

\begin{proposition}
A [[simply connected]] [[oriented]] [[closed manifold|closed]] [[topological manifold|topological]] [[4-manifold]] with even [[intersection form]] is [[spin manifold|spin]].
\end{proposition}

In particular, a [[simply connected]] [[oriented]] [[closed manifold|closed]] [[topological manifold|topological]] [[4-manifold]] is [[spin manifold|spin]] if and only if its [[intersection form]] is even.

([Scorpan 05, p. 164](#Scorpan74))

## Related concepts

* [[Wu class]]

[[!include four-dimensional geometry and topology -- table]]

## References

Named after 

* [[Wen-Tsun Wu]]: _On Pontrjagin classes: II_, Sientia Sinica **4** (1955) 455--90

See also:

* {#Scorpan05} [[Alexandru Scorpan]], _The Wild World of 4-Manifolds_, American Mathematical Society (2005) &lbrack;[ISBN 978-1470468613](https://bookstore.ams.org/fourman)&rbrack;

[[!redirects Wu's formula]]
[[!redirects Wu lemma]]
[[!redirects Wu's lemma]]
[[!redirects Wu theorem]]
[[!redirects Wu's theorem]]
[[!redirects Wu identity]]
[[!redirects Wu's identity]]