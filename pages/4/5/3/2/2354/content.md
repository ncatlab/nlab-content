An ordinary [[pullback]] is a [[limit]] over a [[diagram]] of the form $A \to C \leftarrow B$.  Accordingly, a __2-pullback__ is a [[2-limit]] over such a diagram.

# Definition

Explicitly, a 2-pullback is a square
$$\array{P & \overset{p}{\to} &A \\
  ^q\downarrow & \cong & \downarrow^f\\
  B& \underset{g}{\to} &C }$$
which commutes up to [[isomorphism]], and which is universal among such squares in a 2-categorical sense.  This means that (1) given any other such square
$$\array{Z & \overset{r}{\to} &A \\
  ^s\downarrow & \cong & \downarrow^f\\
  B& \underset{g}{\to} &C }$$
which commutes up to isomorphism, there exists a morphism $u:Z\to P$ and isomorphisms $p u \cong r$ and $q u \cong s$ which are coherent with the given ones above, and (2) given any two morphisms $u,v:Z\to P$ and 2-cells $\alpha:p u \to p v$ and $\beta:q u \to q v$ such that $f \alpha = g \beta$ (modulo the given isomorphism $f p \cong g q$), there exists a unique 2-cell $\gamma:u\to v$ such that $p \gamma = \alpha$ and $q \gamma = \beta$.

# Variations

If all the coherence isomorphisms are required to be identities and $u$ in (1) is required to be unique, then we obtain the notion of a **strict 2-pullback**, which is an example of a [[strict 2-limit]].  Obviously not every 2-pullback is a strict 2-pullback, but also not every strict 2-pullback is a 2-pullback, although the latter is true if either $f$ or $g$ is an [[isofibration]] (and in particular if either is a [[Grothendieck fibration]]).

If the coherence isomorphisms in the squares are retained, but in (1) the isomorphisms $p u \cong r$ and $q u \cong s$ are required to be identities and $u$ is required to be unique, we obtain the notion of a **strict iso-comma object** (so named because if the isomorphisms in the squares are then replaced by mere morphisms, we obtain the notion of strict [[comma object]]).  Every strict iso-comma object is a 2-pullback, and many 2-pullbacks (such as those in [[Cat]]) are in fact strict iso-comma objects.

In a [[(2,1)-category]], any [[comma object]] or [[lax pullback]] is also a 2-pullback, but this is not true in general.

2-pullbacks can also be identified with [[homotopy pullbacks]], when the latter are interpreted in $Cat$-enriched homotopy theory.
