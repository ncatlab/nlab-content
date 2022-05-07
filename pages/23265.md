
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The notion of *homotopy Kan fibration* is the evident [[homotopy theory|homotopy-theoretic]] generalization ([[(infinity,1)-category|$(\infty,1)$-]][[categorification]]) of the notion of [[Kan fibration]]: where a [[Kan fibration]] is a morphism of [[simplicial sets]] (hence: [[simplicial objects]] [[internalization|internal]] to [[Sets]]) which satisfies the [[right lifting property]] against [[horn]] inclusions, so a homotopy Kan fibration is a morphism of [[simplicial object in an (infinity,1)-category|simplicial]] [[infinity-groupoids|$\infty$-groupoids]] ("[[simplicial spaces]]", [[bisimplicial sets]]) which satisfies a *homotopy*-lifting property along all [[horn]] inclusions.

Just like [[Kan fibrations]] serve as the [[fibrations]] in the [[classical model structure on simplicial sets]], so homotopy Kan fibrations are the fibrations in the archetypical [[model (infinity,1)-category|model $\infty$-category]]-structure on [[simplicial object in an (infinity,1)-category|simplicial]] [[infinity-groupoids|$\infty$-groupoids]].


## Definition

\begin{definition}

A morphism $f_\bullet \,\colon\, X_\bullet \xrightarrow{\;} Y_\bullet$ is a *homotopy Kan fibration* if for all $n \in \mathbb{N}$ and $0 \leq k \leq n$ the induced map

\[
  \label{HomotopyTheoreticKanFibration}
  X(\Delta^n)
  \xrightarrow{\;\;}
  X(\Lambda^n_k)
    \underset
      { Y(\Lambda^n_k) }
      {\times^h}
  Y(\Delta^n)
\]

(into the [[homotopy fiber product]] of the space of space of [[horns|$(n,k)$-horns]] in $X$ with that of [[simplex|$n$-simplices]] in $Y$)

is [[surjective]] on [[connected components]], 

hence in that for all solid homotopy-commutative squares as follows, there exists a dashed lift up to homotopy (with the left morphism being the [[horn|$(n,k)$-horn]]-inclusion in [[simplicial sets]] regarded as degree-wise [[discrete topological spaces]]):

\begin{tikzcd}
        \Lambda^n_k
        \ar[
          rr,
          "{\ }"{below, name=s1, pos=.7}
        ]
        \ar[d]
        &&
        \mathrm{X}_\bullet
        \ar[
          d,
          "{f_\bullet}"{right}
        ]
        \\
        \Delta^n
        \ar[
          rr,
          "{\ }"{above, name=t2, pos=.3}
        ]
        \ar[
          urr,
          dashed,
          "{\ }"{above, name=t1},
          "{\ }"{below, name=s2}
        ]
        &&
        \mathrm{Y}_{\bullet}
        \mathrlap{\,,}
        %
        \ar[
          from=s1,
          to=t1,
          Rightarrow,
          dashed
        ]
        \ar[
          from=s2,
          to=t2,
          Rightarrow,
          dashed
        ]
\end{tikzcd}

\end{definition}

([Lurie 2011, Def. 3](#Lurie11); [Mazel-Gee 2014, p. 2](#MazelGee14))

## Examples

For $G \,\in\, Grp(Grpd_\infty)$ an [[infinity-group|$\infty$-group]], consider a homomorphism of $G$-[[infinity-action|$\infty$-actions]]

\begin{tikzcd}
  X 
    \ar[r]
  &
  X /\!/ G
  \ar[d]
  \\
  &
  B G
\end{tikzcd}

(...)

## Properties

### Relation to homotopy colimit (geometric realization)

See at *[[geometric realization of simplicial topological spaces]]* the section *[Preservation of homotopy limits](geometric+realization+of+simplicial+topological+spaces#PreservationOfHomotopyLimits)*.



## Related concepts

* [[Kan fibration]]

* [[model (infinity,1)-category|model $\infty$-category]]


## References

* {#Lurie11} [[Jacob Lurie]], *Simplicial spaces*, Def. 3 in: *[Algebraic L-theory and Surgery](https://www.math.ias.edu/~lurie/287x.html)*, 2011 ([pdf](https://www.math.ias.edu/~lurie/287xnotes/Lecture7.pdf))

* {#MazelGee14} [[Aaron Mazel-Gee]], _Model $\infty$-categories I: some pleasant properties of the $\infty$-category of simplicial spaces_ ([arXiv:1412.8411](https://arxiv.org/abs/1412.8411))

[[!redirects homotopy Kan fibrations]]

