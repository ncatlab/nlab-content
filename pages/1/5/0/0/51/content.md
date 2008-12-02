#Essentially, surjective, faithful and full functors#

... the standard stuff...

#Generalization to $\infty$-categories#

## $k$-surjectivity##

An $\omega$-functor $f : C \to D$ between [[omega-category|omega-categories]] is _$k$-surjective_ for $k \in \mathbb{N}$ if the universal morphism 
$$
  C_{k+1} \to P_{k+1}
$$
to the pullback $P_{k+1}$ in
$$
  \array{
     P_{k+1}
     &\to&
     D_{k+1}
     \\
     \downarrow && \downarrow^{s \times t}
     \\
     C_k \times C_k
     &\stackrel{F_k \times F_k}{\to}&
     D_k \times D_k
  }
$$
coming from the commutativity of the square
$$
  \array{
     C_{k+1}
     &\stackrel{f_{k+1}}{\to}&
     D_{k+1}
     \\
     \downarrow^{s \times t} && \downarrow^{s \times t}
     \\
     C_k \times C_k
     &\stackrel{F_k \times F_k}{\to}&
     D_k \times D_k
  }
$$
(which commutes due to the functoriality axioms of $f$) is an [[epimorphism]].

**Proposition** For $C$ and $D$ 1-categories we have

 1. ($f$ is 0-surjective) $\Leftrightarrow$
    $f$ is surjective on objects

 2. ($f$ is 1-surjective) $\Leftrightarrow$ ($f$ is full)

 3. ($f$ is 2-surjective) $\Leftrightarrow$ ($f$ is faithful)


## essential $k$-surjectivity##

same, but epi only after projecting to $\omega$-equivalence classes

#Literature#

For the general idea of $k$-surjectivity see Baez-Shulman. For the definition for $\omega$-category see Metayer-Lafont-Worytkewicz


... have to run now, more later...