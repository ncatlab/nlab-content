# Idea #

The notion of _Ehresmann connection_ describes a [[connection on a bundle|connection on]] a $G$-[[principal bundle]] $p : P \to X$ (for $G$ some [[Lie group]]) in terms of a [[Lie algebra]]-valued $1$-[[differential form|form]] $A \in \Omega^1(P,Lie(G))$ on $P$ that satisfies two conditions.

This can be understood as the special case of [[schreiber:Differential Nonabelian Cohomology|nonabelian differential G-cocycle]] in [[Cech cohomology]] using the "canonical" [[Cech cover]] 

$$\cdots \to P \times_X P \simeq P \times G \stackrel{\to}{\to} P
$$ 

that comes from the total space surjection $p : P \to X$ of the [[bundle]] itself.

It is an exercise to deduce the conditions on $A$ from that. One find the following two:


1. **first Ehresmann condition** restricted to the fibers, i.e. pulled back along $\array{G &\stackrel{i_x}{\to}& P \\ \downarrow && \downarrow \\ {*} &\stackrel{x}{\to}& X}$ it becomes the canonical left-invariant $Lie(G)$-valued 1-form $\theta \in \Omega^1(G,Lie(G))$ on $G$

  $$
    i_x^* A = \theta
  $$

2. **second Ehresmann condition** The form $A$ is _equivariant_ with respect to the $G$-[[action]] on $P$ in some sense. 

The crucial implication of the second property is that all [[characteristic form]]s of $A$ in $\Omega^\bullet(P)$ are pullbacks of forms on $X$: for $I$ any degree $k$ [[invariant polynomial]] on $Lie(G)$ and for $F_A \in \Omega^2(P,Lie(G))$ the curvature 2-form, we have

$$
  \exists c_I \in  \Omega^{2k}(X) : 
  I(F_A) = p^* c_I
  \,.
$$


[[!redirects Ehresmann-connection]]