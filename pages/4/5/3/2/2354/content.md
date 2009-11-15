# $2$-pullbacks

* tic
{: toc}


An ordinary [[pullback]] is a [[limit]] over a [[diagram]] of the form $A \to C \leftarrow B$.  Accordingly, a __2-pullback__ is a [[2-limit]] over such a diagram.

+-- {: .query}
Zoran: I disagree with a second part of the sentence. If it were a 2-limit of THAT diagram strictly speaking we would have from it an arrow to $C$ (which can be skipped in 1-categorical situation as it is superfluous) and several 2-cells in the story. So there is some confusion between sisters like comma objects, 2-pullbacks and alike. 

_Toby_:  It seems to me that (without loss of generality) you can take the arrow to $C$ to be (following the picture below) the composite $P \overset{p}\to A \overset{f}\to C$ (or the composite $P \overset{q}\to B \overset{g}\to C$ if you prefer).  But identifying comma objects with lax pullbacks may be trickier.
=--


## Definition

Explicitly, a 2-pullback in a [[2-category]] is a square
$$\array{P & \overset{p}{\to} &A \\
  ^q\downarrow & \cong & \downarrow^f\\
  B& \underset{g}{\to} &C }$$
which commutes up to [[isomorphism]], and which is universal among such squares in a 2-categorical sense.  This means that (1) given any other such square
$$\array{Z & \overset{r}{\to} &A \\
  ^s\downarrow & \cong & \downarrow^f\\
  B& \underset{g}{\to} &C }$$
which commutes up to isomorphism, there exists a morphism $u:Z\to P$ and isomorphisms $p u \cong r$ and $q u \cong s$ which are coherent with the given ones above, and (2) given any two morphisms $u,v:Z\to P$ and 2-cells $\alpha:p u \to p v$ and $\beta:q u \to q v$ such that $f \alpha = g \beta$ (modulo the given isomorphism $f p \cong g q$), there exists a unique 2-cell $\gamma:u\to v$ such that $p \gamma = \alpha$ and $q \gamma = \beta$.


## Variations

If we are in a [[strict 2-category]] and all the coherence isomorphisms are required to be identities and $u$ in (1) is required to be unique, then we obtain the notion of a **strict 2-pullback**, which is an example of a [[strict 2-limit]].  Obviously not every 2-pullback is a strict 2-pullback, but also not every strict 2-pullback is a 2-pullback, although the latter is true if either $f$ or $g$ is an [[isofibration]] (and in particular if either is a [[Grothendieck fibration]]).  A strict 2-pullback is, in particular, an ordinary pullback in the underlying 1-category of our strict 2-category, but it has a stronger universal property than this, referring to 2-cells as well.

If the coherence isomorphisms in the squares are retained, but in (1) the isomorphisms $p u \cong r$ and $q u \cong s$ are required to be identities and $u$ is required to be unique, we obtain the notion of a **strict iso-comma object** (so named because if the isomorphisms in the squares are then replaced by mere morphisms, we obtain the notion of strict [[comma object]]).  Every strict iso-comma object is a 2-pullback, and many 2-pullbacks (such as those in [[Cat]]) are in fact strict iso-comma objects.

In a [[(2,1)-category]], any [[comma object]] or [[lax pullback]] is also a 2-pullback, but this is not true in general.

2-pullbacks can also be identified with [[homotopy pullbacks]], when the latter are interpreted in $Cat$-enriched homotopy theory.
