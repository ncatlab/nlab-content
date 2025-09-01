
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

A [[transfor]] between [[pseudonatural transformation|pseudo]]/[[lax natural transformations]] is sometimes called a _modification_. Hence modifications are the [[3-morphisms]] in a [[3-category]] [[2Cat]] of [[2-categories]] and [[2-functors]] between them.

Just as a [[natural transformation]] between [[functor]]s is a
collection of $1$-cells indexed by $0$-cells, a _modification_ between transformations is an indexed collection of 2-cells.


## Definitions

Given

* $\mathcal{X}, \mathcal{Y}$ a [[pair]] of [[2-categories]], 

* $F,G \colon \mathcal{X} \longrightarrow \mathcal{Y}$ a [[pair]] of [[parallel morphism|parallel]] [[2-functors]] between these,

* a [[pair]] of [[parallel morphism|parallel]] [[lax natural transformations|lax]]/[[pseudonatural transformations]] between those,

\begin{tikzcd}
      \mathcal{X}
      \ar[
        rr,
        bend left=40,
        "{ F }"{description, name=s}
      ]
      \ar[
        rr,
        bend right=40,
        "{ G }"{description, name=t}
      ]
      \ar[
        from=s, to=t,
        bend right=40,
        Rightarrow,
        "{ \eta }"{description}
      ]
      \ar[
        from=s, to=t,
        bend left=40,
        Rightarrow,
        "{ \eta' }"{description}
      ]
      &&
      \mathcal{Y}
\end{tikzcd}

then a *modification* from $\eta$ to $\eta'$ is a [[function]] from [[objects]] of $\mathcal{X}$ to [[2-morphisms]] of $\mathcal{Y}$ of the form

\begin{tikzcd}
      x
      \ar[
        r,
        shorten=5pt,
        |->
      ]
      &
      F(x)
      \ar[
        rr,
        bend left=40,
        "{ \eta(x) }"{description,name=s}
      ]
      \ar[
        rr,
        bend right=40,
        "{ \eta'(x) }"{description,name=t}
      ]
      \ar[
        from=s, to=t,
        Rightarrow,
        "{ m(x) }"{description}
      ]
      &&
      G(x)
\end{tikzcd}

which satisfies the following [[equations]] for all 1-morphisms $x \xrightarrow{f} y$ in $\mathcal{X}$:

\begin{tikzcd}
       F(x_1)
       \ar[
         dd,
         "{ F(f) }"{description}
       ]
       \ar[
         rr,
         bend left=40,
         "{ \eta(x) }"{description, name=s}
       ]
       \ar[
         rr,
         bend right=40,
         "{ \eta'(x) }"{description, name=t}
       ]
       \ar[
         from=s,
         to=t,
         shorten=7pt,
         Rightarrow,
         "{ m(x_1) }"
       ]
       &&
       G(x_1)
       \ar[
         dd,
         "{ G(f) }"{description}
       ]
       \\
       &
       \ar[
         dl,
         shorten <=5pt,
         shorten >=5pt,
         Rightarrow,
         shift left=3,
         bend left=20,
         "{ \eta'(f) }"{pos=.7}
       ]
       \\
       F(x_2)
       \ar[
         rr,
         bend right=40,
         "{ \eta'(x_2) }"{description}
       ]
       &&
       G(x_2)
\end{tikzcd}
$$=$$
\begin{tikzcd}
       F(x_1)
       \ar[
         dd,
         "{ F(f) }"{description}
       ]
       \ar[
         rr,
         bend left=40,
         "{ \eta(x) }"{description}
       ]
       &&
       G(x_1)
       \ar[
         dd,
         "{ G(f) }"{description}
       ]
       \ar[
         dl,
         shorten <=5pt,
         shorten >=5pt,
         Rightarrow,
         shift right=3,
         bend right=20,
         "{ \eta(f) }"{pos=.7}
       ]
       \\
       &
       {}
       \\
       F(x_2)
       \ar[
         rr,
         bend left=40,
         "{ \eta(x_2) }"{description, name=s}
       ]
       \ar[
         rr,
         bend right=40,
         "{ \eta'(x_2) }"{description, name=t}
       ]
       \ar[
         from=s,
         to=t,
         shorten=7pt,
         Rightarrow,
         "{ m(x_2) }"
       ]
       &&
       G(x_2)
\end{tikzcd}




## Related concepts

* [[2-functor 2-category]]

* [[(n,k)-transformation]]


## References

* [[John W. Gray]], section I.4 of: _[[Adjointness for 2-Categories|Formal category theory: Adjointness for 2-categories]]_, Lecture Notes in Mathematics **391**, Springer (1974) &lbrack;[doi:10.1007/BFb0061280](https://doi.org/10.1007/BFb0061280)&rbrack; 

For review see most texts on [[2-categories]], such as:

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], Section 4.4 of: *2-Dimensional Categories*, Oxford University Press 2021 &lbrack;[arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378)&rbrack;

* [[Tom Leinster]], _Basic bicategories_ &lbrack;[arXiv:math/9810017](http://arxiv.org/abs/math/9810017)&rbrack;


[[!redirects modification]]
[[!redirects modifications]]
