#Idea#

_Complete [[Segal spaces]]_ are one model for $(\infty,1)$-[[(infinity,1)-category|categories]]. 

The rough idea is that a complete Segal space is the [[nerve]] of a [[enriched category|category enriched]] [[homotopical enrichment|weakly]] over [[Top]]: it is not a [[simplicial set]], but a simplicial [[topological space]] which satisfies the [[homotopy theory|homotopy theoretic]] analog of the condition that otherwise implies that a [[simplicial set]] is the [[nerve]] of a [[category]].

A bit more precisely: to determine if a [[simplicial set]] $X_\bullet$ arises from a [[category]] by passing to its [[nerve]] one has to check if for all natural numbers $m,n$ the square

$$
  \begin{aligned}
    X_{m+n} &\stackrel{
      p^*_{0,\cdots, m}
    }{\to}&& X_m
    \\
    \scriptsize{p^*_{m, \cdots, m+n}}\downarrow 
    &&& \downarrow^{p^*_m}
    \\
    X_n &\stackrel{\quad p^*_0\quad}{\to}&& X_0
  \end{aligned}
$$

is a [[pullback]] square (where the maps $p^*_{\cdots}$ project out the indicated parts of the objects of the [[simplex category]] $\Delta$ regarded as [[posets]]). $X^\bullet$ is the [[nerve]] of a [[category]] precisely if this is the case for all $n, m$.

This condition is internalized homotopically in the category of spaces to get the definition of a _Segal space_.  One can interpret "spaces" here as meaning either (sufficiently [[nice category of spaces|nice]]) [[topological spaces]] or [[simplicial sets]]; in the latter case a Segal space is a particular sort of [[bisimplicial set]].

+-- {: .un_defn}
###### Definition

A **Segal space** $X_\bullet$
  is a simplicial space
  $X_\bullet : \Delta^{op} \to Top$ for which for all $m,n \in \mathbb{N}$ the square

$$
  \array{
    X_{m+n} &\stackrel{
      p^*_{0,\cdots, m}
    }{\to}& X_m
    \\
    {}^{p^*_{m, \cdots, m+n}}\downarrow 
    && \downarrow^{p^*_m}
    \\
    X_n &\stackrel{p^*_0}{\to}& X_0
  }
$$

is a [[homotopy pullback]] square.

=--

Next, the idea is that, roughly,
a Segal space $X_\bullet$ is a **complete Segal space** if the the [[fundamental ∞-groupoid]] of $X_0$ is the maximal topological groupoid contained in the topologically enriched category of which $X_\bullet$ is like the nerve of.

More precisely...

#Remarks#

* One definition of $(\infty,n)$-[[(infinity,n)-category|category]] is in terms of complete Segal spaces.


#References#

Complete Segal spaces were originally defined by
Charles Rezk. 

Information is for instance on pages 29 to 31 of

* Jacob Lurie, _On the classification of TFTs_ ([pdf](http://www.math.harvard.edu/~lurie/papers/cobordism.pdf))

or section 4 of 

* Julia E. Bergner, _A survey of $(\infty, 1)$-categories_ ([arXiv](http://arxiv.org/abs/math.AT/0610239)).

[[!redirects complete Segal spaces]]
