#Idea#

In a category $C$ with [[biproduct]]s, morphisms between objects are naturally encoded in terms of arrays of morphisms between the [[direct sum|direct summands]] of the objects. The natural operations on  morphisms (addition, composition) correspond to the usual matrix calculus operations on these arrays. 

For the special case that $C =$ [[Vect]] this reproduces the standard matrix calculus of linear algebra.

#Definition#

Let $f : X \to Y$ be a [[morphism]] in a [[category]] with [[biproduct]]s where the objects $X$ and $Y$ are given as [[direct sum]]s
$$
  X = \oplus_{j = 1}^m X_j
  \,,
  \;\;
  Y = \oplus_{i = 1}^n Y_i
  \,.
$$

Since a [[biproduct]] is both a [[product]] as well as a [[coproduct]], the morphism $f$ is fixed by all its compositions $f_{i j}$ with the product projections $p_i : Y \to Y_i$ and the coproduct injections $i_j : X_j \to X$:

$$
  f_{i j}
  :=
  X_j \stackrel{i_j}{\to}
  X \stackrel{f}{\to}
  Y \stackrel{p_i}{\to}
  Y_i
  \,.
$$

In **matrix calculus** one therefore writes

$$
  f := 
  \left(
    \array{
       f_{11} & f_{12} & \cdots & f_{1 m}
       \\
       \vdots & \vdots && \vdots
       \\
       f_{n1} & f_{n2} & \cdots & f_{n m}
    }
  \right)
  \,.
$$

With this notation one has the following rules for computation:

**matrix addition**

$$
  (f + g)_{i j} = f_{i j} + g_{i j}
$$


**matrix product **

$$
  (g \circ f)_{i j}
  =
  \sum
     g_ {k j} \circ f_{i k}
  \,,
$$

where in each case the sum of morphisms is taken using the canonical [[enriched category|enrichment]] of $C$ in abelian [[monoid]]s (as described at [[biproduct]]).

#In dagger categories#

If the category $C$ is in addition a [[dagger category]] with an obvious compatibility condition between the dagger operation $(-)^\dagger : C \to C$ and the biproduct structure, then the usual rules of computation for matrices over complex numbers have analogs in $C$.

**conjugation**

$$
  (f^\dagger)_{i j} =  (f_{j i})^\dagger
$$



#References#

For instance section 2 of 

* John Harding, [[matrixcalculus.pdf:file]]