(Posted on behalf of Jim Stasheff, needs a little polishing before announcing.)

+-- {: .num_subsection #sectiona }
=--
### The pentagonal algebra of open string field theory ### {: .num_subsection}


One version of an open string in physics is a geometric object - something like an oriented arc in a Riemannian manifold $(M, g)$. One of the subtleties of string theory is the use of parametrized strings (paths) to obtain results that are independent of the choice of parameterization. String interactions are handled by "joining two strings to form a third" or "splitting a string in two". These are often pictured in one of three ways:

Fig. 3.

#### E: endpoint interaction ####

Here we are dealing with a space of maps $Map(I, M)$ where $I = [0, 1]$. (Physicists prefer $[0, \pi ]$.) The endpoint joining $E$ requires a reparameterization; define $X + Y :[0, 1] \to M$ by $X(2t) \text{for} t \leq 1/2$ and $Y(2t-1) \text{for} 1/2 \leq t \leq 1.$ This operation failed to have units, inverses or associativity, though all were present "up to homotopy".

So as to restore associativity, we follow J. C. Moore [?] and consider the space PM of parametrized paths $X : [0, r] \to M.$ (Fixing r can be regarded as a (partial) choice of 'gauge'.) Now we define the endpoint joining operation $X \vee Y$ for for paths $X,Y$ such that $X(r) = Y(0)$ so that $X \vee Y : [0, r + s] \to M$ by $X(t) \text{for} 0\leq t \leq r$ and $Y(t-r) \text{for} r\leq t\leq r+s.$ This operation is associative where defined and has units $x : [0,0] \to M,$ but has inverses only up to homotopy.

Conversely, splitting of the picture of a string at an arbitrary point led naturally to the use of parametrized paths $X : [0, r] \to M$ and to what are known as 4-point functions in physics. This splitting rather than combining paths seems to have occurred first in physics in the work of Kaku and Kikkawa [?]. Although couched in the physics language of light-cone Feynman diagrams, channels, Lagrangians, etc., they remark:

> the four-string interaction corresponds to the continuous defomation of the t-channel topology into the u-channel topology...([?], p.1124),

in other words, an associating homotopy. In considering multiple string interactions, they remark that the number of relevant light-cone Feynman diagrams is equal to the number of non-crossing triangulations of a convex $N$-gon, hence the Catalan number, though unnamed. Further, they remark that for an N-point functions, there is a relevant $N-3$-dimensional 'surface' (what is now known as the associahedron). They sketch a reason why for their string field theory there is no need for $N$-point functions for $N\gt 4.$ Translation:the pentagonal condition is satisfied on the nose, no need for higher homotopies.

#### M: midpoint or half overlap interaction ####

Here when the latter half of one path is the same as the first half of the second path but with reversed orientation, the interaction produces a third path by 'cancelling' the overlapping halves. The picture is symmetric with respect to cyclic permutations and is so interpreted.

The endpoint case E is familiar in mathematics as far back as the study of the fundamental group; the midpoint case M was considered by Witten in 1986 [?] for string field theory, although in fact it had been considered independently in mathematics by Lashof [?] in 1956.

#### V: variable overlap interaction ####

But if overlapping halves can be cancelled, why not vary the portion that is cancelled? This idea seems to have occurred first in physics in the work of Kaku [?], although it follows from an interpretation of the HIKKO [^1] interaction [?] of open string field theory. This (independently) uses Moore's associative endpoint interaction, but then creates inverses by cancellation as in the midpoint case. (see also the work of Kaku [?]). From the physicist's symmetrical point of view, this picture also gives inverses in the endpoint gauge by reversing orientation and cancellation of a portion of one string by all of another.

FIGURE

This variable overlap joining V of paths is given by the operation $X \star Y$ defined as follows: Let $u = \text{max} \{ r \text{such that} Y(t) = X(r-t) \text{for} 0 \leq t \leq r\} $, then $X \star Y: [0, r+s-2u] \to M$ by $X(t ) \text{for} 0\leq t \leq r-u$ and $Y(t-r+2u) \text{for} r-u\leq t\leq r+s-2u.$ Again $m: [0, 0] \to M$ is a unit, and the reversal $\bar{X}(t) = X(r - t)$ provides a strict inverse, but now $\star $ occasionally fails to be associative; there is a hidden destruction of associativity in what HIKKO refer to as 'horn' diagrams. for example in the configuration of Fig. \ref{horn}

On the other hand, $(X \star Y) \star Z$ and $X \star (Y\star Z)$ are clearly homotopic - just gradually shrink the back-and-forth part of $(X \star Y) \star Z$ - and hence $\star $ is homotopy associative. Denote such a homotopy $X \star Y \star Z$. From our point of view, it is this homotopy which gives rise to the "4-string vertex" in physics. Corresponding to the ways of combining $m_{2}$ and $m_{3}$ in defining an $A_{\infty }$-algebra, there are Remarkably, the five ways of combining the operations $ \star \star $ with $ \star $ on $W, X, Y, Z,$ e.g. $W\star (X\star Y) \star Z$, which remarkably add to give $0$ in this string interpretation.

[^1]: Hata, Itoh, Kugo, Kunitomo, Ogawa
