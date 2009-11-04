**Diagrammatic order** is a way of writing the composite of [[morphisms]] in a [[category]] which aligns more closely with the way in which [[commutative diagrams]] are often drawn.  Given arrows
$$A \overset{f}{\to} B \overset{g}{\to} C$$
in the "classical" notation their composite would be written as
$$A \overset{g\circ f}{\to} C.$$
Note that the order has been reversed from the original diagram, although it aligns more closely with the traditional way of writing function application $(g\circ f)(x) = g(f(x))$.  By contrast, in diagrammatic order the composite of $f$ and $g$ above would be written
$$A \overset{f; g}{\to} C.$$
with the order preserved from the original diagram.

Although diagrammatic order has advantages and partisans, especially among category theorists and computer scientists, the "classical" order of composition is firmly entrenched in much of mathematics.  Many people who agree that diagrammatic order is "better" on its own merits nevertheless believe that trying to change the established "classical" order of composition creates more confusion than it removes.

In some older category theory papers, arrows were written pointing from right to left, so that the composition of arrows could be written in the "classical" style, while still preserving the diagrammatic intuition. Hom-sets were accordingly written $C(b,a)$, where $a$ is the domain, and $b$ is the codomain.