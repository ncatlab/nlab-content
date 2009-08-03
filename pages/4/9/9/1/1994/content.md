Given crossed modules $\mathbb{X}=(\partial_X : X_1\to X_0)$, $\mathbb{Y}=(\partial_Y:Y_1\to Y_0)$ (actions surpressed from the notation), a crossed profunctor $\mathbb{X}\to\mathbb{Y}$ consists of a group $P$ and morphisms $x_1:X_1\to P$, $x_0:P\to X_0$, $y_1:Y_1\to P$, $y_0:P\to Y_0$ such that $x_0\circ x_1=\partial_X$, $y_0\circ y_1=\partial_Y$, $y_0\circ x_1 = 1$, $x_0\circ y_1 = 1$, and

$$
x_1 ({}^{x_0(p)}x) = p x_1(x) p^{-1}, \,\,\,\,\,y_1 ({}^{y_0(p)}y = py_1(y)p^{-1}
$$

where $x\in X_1$, $p\in P$, $y\in Y_1$. (Nonabelian) complexes of groups $Y_1\to P\to X_0$
and $X_1\to P\to Y_1$ are usually drawn in a diagram as a cross of diagonals within two vertical arrows, namely the crossed modules $\mathbb{X}$ and $\mathbb{Y}$ are left and eight vertical arrows pointing down. Then the complex $Y_1\to P\to X_0$ is NE-SW and $X_1\to P\to Y_0$ is NW-SE. 

This notion appeared in

* M. Jibladze, COEFFICIENTS FOR COHOMOLOGY OF "LARGE" CATEGORIES, pp. 169--179, in H. Inassaridze (Ed.), K-theory and Homological Algebra (A Seminar held at the Razmadze Mathematical Institute in Tbilisi, Georgia, USSR 1987-88), Lec. Notes in Math. 1437, Springer 1990 (_[[jibladzeCoeffLargeCats.djvu:file]]_).

If we add additional property that the SE-NW sequence $Y_1\to P\to X_0$ is exact, we get a papillon or [[butterfly]].