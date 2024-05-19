Schur complement of (i,j)-entry of a block $2\times 2$ [[matrix]]

$$
\left(\begin{matrix}
A & B          \\
C & D
\end{matrix}\right)
$$

is the following expression involving the inverse of that entry

* $D- C A^{-1} B$ if the entry is (1,1)
* $C- D B^{-1} A$ if the entry is (1,2)
* $B- A C^{-1} D$ if the entry is (2,1)
* $A- B D^{-1} C$ if the entry is (2,2)

whenever the inverses involved make sense.

These expressions are related to [[quasideterminant]]s, Gauss elimination procedure and [[matrix inverse]]. Typically the case at main diagonal are used compatibly with a standard choice of the shape of triangular matrices in Gauss procedure.

There are alternative expressions for those (if certain inverses exist) thanks to the homological identities for quasideterminants or equivalently Woodbury matrix identity ([wikipedia](https://en.wikipedia.org/wiki/Woodbury_matrix_identity)).

## References

* wikipedia [Schur complement](https://en.wikipedia.org/wiki/Schur_complement), [Woodbury matrix identity](https://en.wikipedia.org/wiki/Woodbury_matrix_identity).

category: algebra