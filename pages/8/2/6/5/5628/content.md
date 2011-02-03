### The HOMFLY-PT Polynomial ###

* tic
{: toc}

### Idea ###

### Definition ###

The HOMFLY-PT polynomial is a [[knot]] and [[link]] [[knot invariants|invariant]].  Confusingly, there are several variants depending on exactly which relationships are used to define it.  All are related by simple substitutions.  To compute it, one starts from an oriented link diagram and uses the following rules:

1. $P$ is an isotopy invariant (thus, unchanged by [[Reidemeister moves]]).
1. $P(\text{unknot}) = 1$
1. Let $L_+$, $L_-$, and $L_0$ be links which are the same except for one part where they differ according to the diagrams below.  Then, depending on the choice of variables:

   1. $l \cdot P(L_+) + l^{-1} \cdot P(L_-) + m \cdot P(L_0) = 0$.
   1. $a \cdot P(L_+) - a^{-1} \cdot P(L_-) = z \cdot P(L_0)$.  (Sometimes $\nu$ is used instead of $a$)
   1. $\alpha^{-1} \cdot P(L_+) - \alpha \cdot P(L_-) = z \cdot P(L_0)$.
   1. Using *three* variables: $x \cdot P(L_+) + y \cdot P(L_-) + z \cdot P(L_0) = 0$.

$$
\begin{array}{ccc}
\begin{svg}[[!include SVG skein positive crossing]]\end{svg} &
\begin{svg}[[!include SVG skein negative crossing]]\end{svg} &
\begin{svg}[[!include SVG skein no crossing]]\end{svg} \\
L_+ & L_- & L_0
\end{array}
$$

### Properties ###

The HOMFLY polynomial generalises both the [[Jones polynomial]] and the [[Alexander polynomial]].  To get the Jones polynomial, substitute $a = q^{-1}$ and $z = q^{1/2} - q^{-1/2}$.  To get the [[Conway polynomial]], substitute $a = 1$, from which one can read off the [[Alexander polynomial]].


[[!redirects HOMFLY polynomial]]