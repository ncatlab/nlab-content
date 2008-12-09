Given an [[higher category theory|infinity-category]]-valued (pseudo)presheaf $\mathbf{A} : Spaces^{op} \to \infty-Cat$, its _cohomology_ $H(-,\mathbf{A})$ is the $\infty$-category valued (pseudo)presheaf which assigns to each space the directed limit over all [[descent and codescent|descent data]]:
$$
  H(X, \mathbf{A}) := colim_{Y^\bullet \to X}
  Desc(Y^\bullet, \mathbf{A})
  \,.
$$
Here the colimit is over all [[hypercover|hypercovers]] of $X$.
