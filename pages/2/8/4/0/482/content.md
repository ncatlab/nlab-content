The **kernel pair** of a morphism $f:X\to Y$ in a category $C$ is a pair of morphisms $R\,\rightrightarrows \, X$ which are a [[pullback]] of $f$ against itself, i.e. a [[limit]] of the diagram

$$\array{
X &            &   &            & X \\
  & \searrow^f &   & \swarrow_f \\
  &            & Y \\
}$$

also called the [[fiber product]] $X \times_Y X$ of $X$ with itself over $Y$.

The kernel pair is always an [[congruence]] on $X$; informally, $R$ is the subobject of $X \times X$ consisting of pairs of elements which have the same value under $f$ (sometimes called the 'kernel' of a function in $\Set$).

The [[coequalizer]] of the kernel pair, if it exists, is supposed to be the "object of equivalence classes" of the internal [[equivalence relation]] $R$. In other words, it is the [[quotient object]] of $X$ in which [[generalized element]]s are identified if they are mapped by $f$ to equal values in $Y$. In a [[regular category]] (at least), this can be identified with a [[subobject]] of $Y$ called the [[image]] of $f$.

See also: [[regular epimorphism]], [[regular category]], [[exact category]]


[[!redirects kernel pairs]]