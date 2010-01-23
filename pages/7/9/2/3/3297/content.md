
## Idea

For any category $S$ with pullbacks, it is easy to define the notion of [[internal category|category]] in $S$, and the definition of an internal [[functor]] between such is similarly straightforward.  But it is not so obvious how to define [[presheaf|presheaves]] on internal categories, because they must land in the ambient category $S$.

The solution lies in thinking of presheaves on an ordinary category $C$, and more generally [[profunctor]]s $C &#8696; D$, as giving sets equipped with an _action_ of the arrows of $C,D$, i.e. as their [[category of elements|categories of elements]].

## Definition

Here is the slick definition: let $S$ be a category with pullbacks. Then the bicategory $Prof(S)$ of internal categories, profunctors and transformations in $S$ is defined to be $Mod(Span(S))$, the category of [[monad]]s and [[module over a monad|bimodules]] in $Span(S)$, the [[bicategory]] of [[span]]s in $S$.

### Details

Recall that an [[internal category]] $C$ in $S$ is a monad in $Span(S)$, and so has an underlying span $(s,t) : C_1 \rightrightarrows C_0$.  Given $C,D \in Cat(S)$, a bimodule $H : C &#8696; D$ must be given by a span $H : C_0 \leftarrow H \to D_0$, together with a right action $H \circ C \to H$ of $C$ and a left action $D \circ H \to H$ of $D$ that are compatible in the sense described at [[module over a monad]].

Composition of spans is given by pullback, so the action of $C$ on $H$ is given by a morphism of spans $H_r : C_1 \times_{C_0} H \to H$, where the pullback is
$$
\array{
C_1 \times_{C_0} H & \to & H \\
\downarrow & & \downarrow \\
C_1 & \underset{t}{\to} & C_0
}
$$
To say that $H_r$ is a morphism of spans is to require that
$$
\array{
C_1 \times_{C_0} H & \to & H \\
\downarrow & & \downarrow \\
C_1 & \underset{s}{\to} & C_0
}
$$
commutes.  This action must satisfy unit and associativity axioms expressing functoriality of the corresponding presheaf.  Similarly, $H_\ell : H \times_{D_0} D_1 \to H$, where the pullback is along $s$, so that this represents a copresheaf.  Finally, compatibility of the two actions represents bifunctoriality of the profunctor.

An **internal presheaf** on an internal category is just a right action as above.

## Internal diagrams

An internal presheaf as above may take values in any [[Grothendieck fibration]] over $S$.  Given a fibration in the guise of an [[indexed category]] $E : S^{op} \to Cat$, a **$C$-diagram in $E$** is given by

* an object $P \in E(C_0)$, together with
* a morphism $\phi : t^* P \to s^* P$ in $E(C_1)$

satisfying 'cocycle equations'

* $i^*\phi = 1_P$
* $c^*\phi = p_1^* \phi \circ p_2^* \phi$

modulo coherent isos, where the $p_i$ are the projections out of $C_2$.

+-- {.query}
[[Finn Lawler|Finn]]:  Is there a slicker way to define these, or the category of them?  Anyone know a good reference?
=--

### Examples

* An internal presheaf on $C$ in the sense above is a $C$-diagram in the [[codomain fibration]] of $S$, that is the pseudofunctor $X \mapsto S/X$.

* If $S$ is equipped with a [[coverage]] and $C$ is the [[Cech nerve]] associated to a cover $p : U \to X$ in $S$, then the category of $C$-diagrams in $E$ is the [[descent]] category $Des_p(E)$.

+-- {.query}
[[Finn Lawler|Finn]]:  I _think_ these are right, but I'm still a bit shaky on this stuff.
=--
