## Idea 

An ordinary [[category]] consists of a set of objects and a set of arrows, each with a single input or domain object and a single output or codomain object. Arrows are composed by plugging outputs into inputs, as when one composes unary operations. 

An ordinary [[multicategory]] consists of a set of objects and a set of "multi-arrows", each with a finite list of inputs or domain objects and a single output or codomain object. These multi-arrows are composed by means of multiple plug-ins or substitutions, as when one substitutes a list of $m$ operations of varying arities into an $m$-ary operation. 

Both categories and multicategories can be seen as [[monad]]s in an appropriate [[bicategory]] of [[span]]-like objects. Categories are monads in the category of ordinary spans (of sets). Multicategories are monads in a bicategory of spans of shape 

$$X^* \to Y$$ 

where $X^*$ is the set of finite lists of elements of $X$. 

In order to compose spans of this type, one takes advantage of certain properties of the list monad or free monoid monad $(-)^*$, namely that it is a [[cartesian monad]] $T$. This suggests the following wide extrapolation. 

## Definition 

Let $V$ be a finitely complete category, and let $T$ be a cartesian monad on $V$. Then there is a bicategory of $T$-spans in $V$, whose objects $X$ are objects of $V$, whose morphisms $X \to Y$ are spans from $T X$ to $Y$, and whose 2-cells are morphisms of such spans. The identity $X \to X$ is the span 

$$T X \overset{u X}{\leftarrow} X \overset{id}{\to} X$$ 

where $u: 1_V \to T$ is the unit of $T$, and morphisms $X \to Y$, $Y \to Z$ are composed by taking pullbacks of shape  

$$\array{
& & & & & & R \circ S & & & &\\
& & & & & \swarrow & & \searrow & & & \\
& & & & T S & & & & R & &\\
& & & T f \swarrow & & \searrow T g & & h \swarrow & & \searrow k & \\
T X & \overset{m X}{\leftarrow} & T T X & & & & T Y & & & & Z}$$

A $T$**-multicategory** in $V$ is by definition a monad in the bicategory described above. 