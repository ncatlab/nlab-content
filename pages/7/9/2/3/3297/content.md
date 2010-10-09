
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

For any [[category]] $S$ with pullbacks, it is easy to define the notion of [[internal category|category in]] $S$, and the definition of an internal [[functor]] between such is similarly straightforward.  But it is not so obvious how to define [[presheaf|presheaves]] on internal categories, because they must land in the ambient category $S$.

The solution lies in thinking of presheaves on an ordinary category $C$, and more generally [[profunctor]]s $C &#8696; D$, as giving sets equipped with an _action_ of the arrows of $C,D$, i.e. as their [[category of elements|categories of elements]].

## Definition

Here is the slick definition: let $S$ be a category with pullbacks. Then the bicategory $Prof(S)$ of internal categories, profunctors and transformations in $S$ is defined to be $Mod(Span(S))$, the category of [[monad]]s and [[module over a monad|bimodules]] in $Span(S)$, the [[bicategory]] of [[span]]s in $S$.

So an **internal profunctor** $C &#8696; D$ between internal categories $C$ and $D$ is a bimodule from $C$ to $D$.  An **internal presheaf** on $C$ is a right $C$-module, or equivalently a bimodule $1 &#8696; C$, where $1$ is the discrete category on the terminal object of $S$ (as long as $S$ has one, of course).

An internal presheaf in $S$ is the same thing as an [[internal diagram]] in $S$.

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

