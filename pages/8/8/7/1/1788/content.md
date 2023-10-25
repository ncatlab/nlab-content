
#Contents#
* table of contents
{:toc}


## Idea

If the [[ground ring]] ([[ground field]]) is equipped with a [[star-ring|star structure]] (an [[anti-involution]], such as [[complex conjugation]] in the complex numbers), then the operation of forming [[dual linear spaces]] may be "twisted" by this involution to yield a notion of "anti-dual" spaces. These relate to [[Hermitian forms]] as ordinary dual spaces relate to ordinary [[inner products]].
 
## Definition

Let $\mathbb{K}$ be a [[star-ring]], hence a [[unital ring]] (often a [[field]], whence our notation, and here often the [[complex numbers]]) equipped with an [[anti-involution]] (for instance [[complex conjugation]]):

$$
  \overline{(-)} \,\colon\, \mathbb{K} \to \mathbb{K}
$$
$$
  \overline{x \cdot y} 
    \,=\, 
  \overline{y} \cdot \overline{x}
  \,.
$$

\begin{definition}
For a $\mathbb{K}$-[[module]] $\mathscr{V} \,\in\, \mathbb{K}Mod$ (say *right* modules for possibly non-commutative $\mathbb{K}$, but being just $\mathbb{K}$-[[vector spaces]] if $\mathbb{K}$ is a [[field]]), its *anti-dual* space $\mathr{V}^\ast$ is the space of [[anti-linear maps]] to the [[ground ring]] ([[ground field]])

$$
  \mathscr{V}^\ast
  \;\coloneqq\;
  \Big\{
    \phi \,\colon\, 
    \mathscr{V} \to \mathbb{K}   
    \,\Big\vert\,
    \underset{
      { v \in \mathscr{V} }
      \atop
      { \lambda \in \mathbb{K} }
    }{\forall}
    \,
    \phi(v \cdot \lambda) \,=\, \overline{\lambda} \cdot v
  \Big\}
$$

equipped with the structure of a (right) module by

$$
  \phi \in \mathscr{V}^\ast
  \,\lambda \in \mathbb{K}
  \;\;\;
    \vdash
  \;\;\; 
  (\phi \cdot \lambda)(c)
    \;=\;
  \phi(v) \cdot \lambda
  \,.
$$

\end{definition}
(eg. [Karoubi 2010, §1](#Karoubi10))

## Properties

\begin{example}
  
\end{example}

## References

* {#Karoubi10} [[Max Karoubi]], §1 in: *Le théorème de périodicité en K-théorie hermitienne*, Quanta of Maths **1**, AMS and Clay Math Institute Publications (2010) &lbrack;[arXiv:0810.4707](https://arxiv.org/abs/0810.4707)&rbrack;

See also:

* Wikipedia, *[Anti-dual space](https://en.wikipedia.org/wiki/Antilinear_map#Anti-dual_space)*


#Commuting diagrams

$$
  \array{
    A &\overset{\Delta}{\longrightarrow}& A \otimes A
    \\
    &
    {}_{\mathllap{id}}\searrow
    & \downarrow^{\mathrlap{\epsilon \otimes id}}
    \\
    && A
  }
$$

$$
  \array{
    A &\overset{\Delta}{\longrightarrow}& A \otimes A
    \\
    &   {}_{\mathllap{id}}\searrow
    & \downarrow^{\mathrlap{id \otimes \epsilon}}
    \\
    && A
  }
$$

$$
  \array{
    A &\overset{\Delta}{\longrightarrow}& A \otimes A
    \\
    &
    {}_{\mathllap{id}}\searrow
    & \downarrow^{\mathrlap{\epsilon \otimes id}}
    \\
    && A
  }
  \,.
$$

$$
  \array{
    A &\overset{\Delta}{\longrightarrow}& A \otimes A
    \\
    &   {}_{\mathllap{id}}\searrow
    & \downarrow^{\mathrlap{id \otimes \epsilon}}
    \\
    && A
  }
  \,.
$$
