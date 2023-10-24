
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--


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

Consider a $\mathbb{K}$-[[module]] $\mathscr{V} \,\in\, \mathbb{K}Mod$ (say *right* modules for possibly non-commutative $\mathbb{K}$, but being just $\mathbb{K}$-[[vector spaces]] if $\mathbb{K}$ is a [[field]]).

\begin{definition}
The *anti-dual* space $\overline{\mathscr{V}^\ast}$ of $\mathscr{V}$ is the space of [[anti-linear maps]] to the [[ground ring]] ([[ground field]]):

$$
  \overline{\mathscr{V}^\ast}
  \;\coloneqq\;
  \Big\{
    \phi \,\colon\, 
    \mathscr{V} \to \mathbb{K}   
    \,\Big\vert\,
    \underset{v, v' \in \mathscr{V}}{\forall}
    \,
    \phi(v + v') = \phi(v) + \phi(v')
    ,\;
    \underset{
      { v \in \mathscr{V} }
      \atop
      { \lambda \in \mathbb{K} }
    }{\forall}
    \,
    \phi(v \cdot \lambda) \,=\, \overline{\lambda} \cdot v
  \Big\}
$$

equipped itself with the structure of a (right) module by

$$
  \phi \in \overline{\mathscr{V}^\ast}
  ,\,
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
(eg. [Karoubi & Villamayor 1973, Ex. 1](KaroubiVillamayor73); [Karoubi 2010, §1](#Karoubi10))

As the notation already indicates, an equivalent definition is:
\begin{definition}
  The anti-dual $\overline{\mathscr{V}^\ast}$ has as [[underlying]] [[abelian group]] the ordinary [[linear dual ]] $\mathscr{V}^\ast$ but equipped with its anti-linear structure, namely with the (right) module action twisted by the involution as:
$$
  \phi \,\in\, Hom_{\mathbb{K}}(\mathscr{V}, \mathbb{K})
  \;\;\;
    \vdash
  \;\;\;
  \underset{v \in \mathscr{V}}{\forall}
  \,
  (\phi \cdot \lambda)(v)
  \;=\;
  \overline{\lambda} \cdot \phi(v)
  \,.
$$
\end{definition}
(eg. [Mishchenko 1976 §1.1](#Mishchenko76)).

An [[isomorphism]] between the two definitions 
$$
  \array{
    \mathscr{V}^\ast
    &\longrightarrow&
    \mathscr{V}^\ast
    \\
    \phi &\mapsto& \overline{\phi}
  }
$$
is established by postcomposing linear forms with the star-involution
$$
  \overline{\phi} 
    \,\colon\,
  v \,\mapsto\, \overline{\phi(v)}
$$
which respects the above (right) $\mathbb{K}$-actions due to
$$
  \array{
    \big(
      v \,\mapsto\,
      \phi(v)\cdot \lambda
    \big)
    &\mapsto&
    \big(
      v
      \,\mapsto\,
      \overline{\phi(v) \cdot \lambda}
    \big)
    \\
    & = &
    \big(
      v
      \,\mapsto\,
      \overline{\lambda} \cdot \overline{\phi(v)}
    \big)    
    \mathrlap{\,.}
  }
$$


## References

Discussion in the context of [[Hermitian K-theory]]:

* {#KaroubiVillamayor73} [[Max Karoubi]], [[Orlando Villamayor]], Ex. 1 in: *K-théorie algébrique et K-théorie topologique II*, Math. Scand. **32** (1973) 57-86 &lbrack;[jstor:24490565](https://www.jstor.org/stable/24490565)&rbrack;

* {#Mishchenko76} [[Alexandr S. Mishchenko]], §1.1 (pp. 76) in: *Hermitian K-Theory. The Theory of characteristic classes and methods of functional analysis*, Uspeki Mat. Nauk **31** 2 (1976) 69-134,  Russ. Math. Surv. **31** 71 (1976) &lbrack;[doi:10.1070/RM1976v031n02ABEH001478](https://iopscience.iop.org/article/10.1070/RM1976v031n02ABEH001478), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/mishch5.pdf)&rbrack;

* {#Karoubi10} [[Max Karoubi]], §1 in: *Le théorème de périodicité en K-théorie hermitienne*, Quanta of Maths **1**, AMS and Clay Math Institute Publications (2010) &lbrack;[arXiv:0810.4707](https://arxiv.org/abs/0810.4707)&rbrack;

See also:

* Wikipedia, *[Anti-dual space](https://en.wikipedia.org/wiki/Antilinear_map#Anti-dual_space)*




[[!redirects anti-dual linear spaces]]

[[!redirects anti-dual vector space]]
[[!redirects anti-dual vector spaces]]
