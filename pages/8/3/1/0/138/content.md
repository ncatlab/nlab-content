A _hypercover_ is the simplicial analog of an $\infty$-functor which is [[k-surjectivity|k-surjective]] for all $k$:

For $\Delta^n$ the standard simplicial simplex, $\partial \Delta^n$ its boundary and 
$$
  i_i : \partial \Delta^n \hookrightarrow \Delta^n
$$ 
the canonical inclusion, a morphism $f : Y^\bullet \to X^\bullet$ of [[simplicial object|simplicial objects]] is a _hypercover_ if it has the right lifting property with respect to all $i_n$, i.e. if for all commuting squares of the form
$$
  \array{
     \partial \Delta^n
     &\to&
     Y
     \\
     \downarrow^{i_n}
     &&
     \downarrow^{f}
     \\
     \Delta^n
     &\to&
     X
  }
$$
there exists a diagonal filler
$$
  \array{
     \partial \Delta^n
     &\to&
     Y
     \\
     \downarrow^{i_n}
     &\nearrow&
     \downarrow^{f}
     \\
     \Delta^n
     &\to&
     X
  }
  \,.
$$


In words this means that for every boundary of an $n$-simplex hit by $f$, every filler of this $n$-simplex lifts through $f$.

#Remark.#

The word "hypercover" originates from the fact that this generalizes the situation where $Y \to X$ is a regular epimorphism of spaces, such that the simplicial space
$$
  Y^\bullet := (\cdots \to Y \times_X Y \times_X Y \to Y \times_X Y \to Y)
$$
exists. Here everything is determined by the original choice of cover $Y \to X$. More generally, one can choose iterativley further covers of the spaces in higher degree and thus obtain a more general hypercover of $X$.