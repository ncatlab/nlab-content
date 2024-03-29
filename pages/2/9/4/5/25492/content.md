
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

In [[parameterized homotopy theory]], by a *retractive space* (older terminology: "ex-space" &lbrack;[James (1995)](#James95)&rbrack;, cf. footnote 1, [p. 19](http://www.math.uchicago.edu/~may/EXTHEORY/MaySig.pdf#page=27) in [May & Sigurdsson (2006)](#MaySigurdsson06)) one means a [[retraction]] in a given [[category]] $\mathcal{S}$ of [[model category|models]] for [[homotopy types]] (usually in [[TopologicalSpaces]] or [[SimplicialSets]]), to be thought of as a *[[bundle]] $p \colon E \to B$ of [[pointed topological spaces]]* over a *base space* $B$, where the [[section]] $i \colon B \to E$ exhibits the [[fiber]]-wise [[base points]].

Just as plain [[pointed topological spaces]] serve as the basis on which to construct [[spectra]], so retractive spaces serve as a basis on which to construct [[parameterized spectra]].

## Definition

A *retractive space* is a [[commuting diagram]] in a [[category]] $\mathcal{S}$ "of spaces", of this form:

\begin{tikzcd}[
    column sep=10pt
  ]
    & E
    \ar[
      d,
      "{ p }"
    ]
    \\
    B
    \ar[r, equals]
    \ar[ur, "i"]
    &
    B
    \mathrlap{\,.}
\end{tikzcd}


Taking the [[category]] $\mathcal{S}_{\mathcal{R}}$ of retractive spaces to have as [[morphisms]] the evident [[commuting diagrams]]

\begin{tikzcd}[
  sep=20pt
]
    B 
    \ar[d, "{i}"]
    \ar[rr, "{f}"]
    &&
    B' 
    \ar[d, "{ i' }"]    
    \\
    E 
    \ar[d, "{p}"]
    \ar[rr, "{\widehat f}"]
    &&
    E'
    \ar[d, "{p'}"]
    \\
    B
    \ar[rr, "{f}"]
    &&
    B'
\end{tikzcd}

reflecting [[bundle]]-[[homomorphisms]] respecting the [[base points]], this is [[equivalence of categories|equivalent]] to the [[Grothendieck construction]] on the [[pseudo-functor]] 

$$
  \big(\mathcal{S}_{/(-)}\big)^{\ast/}
  \;\colon\;
  \mathcal{S} \longrightarrow Cat
$$

which sends 

* spaces $B \in \mathcal{B}$ to the [[pointed category]] $\big(\mathcal{S}_{/B}\big)^{\ast/}$ of [[pointed objects]] in the [[slice category]] of $\mathcal{S}$ over $B$ (i.e. in the category of "[[bundles]]" over the fixed base space $B$),

* morphisms $f \colon B \to B'$ of base spaces to the [[functor]] $f_!$ forming [[pushouts]] of bundles along $f_!$:

\begin{tikzcd}[
    row sep=30pt
  ]
    B 
    \ar[d, "{i}"{description}]
    \ar[rr, "{f}"{description}]
    \ar[
      drr,
      phantom,
      "{
        \scalebox{.6}{
          (po)
        }
      }"{pos=.7}
    ]
    &&
    B' 
    \ar[d, "{ f_!(i) }"{description}]    
    \\
    E 
    \ar[d, "{p}"{description}]
    \ar[rr, "{\widehat f}"{description}]
    \ar[
      drr,
      phantom,
      "{
        \scalebox{.6}{
          (po)
        }
      }"{pos=.7}
    ]
    &&
    f_! E
    \ar[d, "{f_!(p)}"{description}]
    \\
    B
    \ar[
      rr, 
      "{f}"{description}
    ]
    &&
    B'
\end{tikzcd}

i.e. 

$$
  \mathcal{S}_{\mathcal{R}}
  \;\simeq\;
  \int_{B \in \mathcal{S}} \big(\mathcal{S}_{/B}\big)^{\ast/}
  \,.
$$

This follows readily from the definitions, but see also [Braunack-Mayer (2021), Rem. 1.15](#BraunackMayer19); [Hebestreit, Sagave & Schlichtkrull (2020), Lem. 2.14](#HebestreitSagaveSchlichtkrull20).

## Related concepts

* [[retraction]]

* [[parameterized homotopy theory]]

* [[parameterized spectrum]]

* [[model structure for parameterized spectra]]

## References

The terminology "ex-spaces" is due to Ioan James, used for instance in:

* {#James95}  [[Ioan Mackenzie James]], _[[Introduction to fibrewise homotopy theory]]_ in [[Ioan Mackenzie James]] (ed.), _[[Handbook of Algebraic Topology]]_ (1995)

Early discussion of their [[model category]] structures includes

* Michele Intermont, [[Mark Johnson]], *Model structures on the category of ex-spaces*, Topology and its Applications **119** 3 (2002) 325-353 &lbrack;<a href="https://doi.org/10.1016/S0166-8641(01)00076-1">doi:10.1016/S0166-8641(01)00076-1</a>&rbrack;


Discussion in the context of [[model structures for parameterized spectra]]:

* {#MaySigurdsson06} [[Peter May]], [[Johann Sigurdsson]], Sections 1.3 and 8.5 of: _[[Parametrized Homotopy Theory]]_,  Mathematical Surveys and Monographs, vol. 132, AMS 2006   ([ISBN:978-0-8218-3922-5](https://bookstore.ams.org/surv-132), [arXiv:math/0411656](https://arxiv.org/abs/math/0411656), [pdf](http://www.math.uchicago.edu/~may/EXTHEORY/MaySig.pdf))


* {#BraunackMayer21} [[Vincent Braunack-Mayer]], *Combinatorial parametrised spectra*, Algebr. Geom. Topol. **21** (2021) 801-891 &lbrack;[arXiv:1907.08496](https://arxiv.org/abs/1907.08496), [doi:10.2140/agt.2021.21.801](https://doi.org/10.2140/agt.2021.21.801)&rbrack;

  > (based on the [[schreiber:thesis Braunack-Mayer|PhD thesis]], 2018)

* {#HebestreitSagaveSchlichtkrull20} [[Fabian Hebestreit]], [[Steffen Sagave]], [[Christian Schlichtkrull]], *Multiplicative parametrized homotopy theory via symmetric spectra in retractive spaces*, Forum of Mathematics, Sigma **8** (2020) e16 &lbrack;[arXiv:1904.01824](https://arxiv.org/abs/1904.01824), [doi:10.1017/fms.2020.11](https://doi.org/10.1017/fms.2020.11)&rbrack;

* [[Cary Malkiewich]], Section 2.1 in: *Parametrized spectra, a low-tech approach* &lbrack;[arXiv:1906.04773](https://arxiv.org/abs/1906.04773), user guide: [pdf](https://people.math.binghamton.edu/malkiewich/users_guide_parametrized.pdf), [[Malkiewich-ParametrizedSpectraUserGuide.pdf:file]]&rbrack;


[[!redirects retractive spaces]]

[[!redirects retractive topological space]]
[[!redirects retractive topological spaces]]

[[!redirects ex-space]]
[[!redirects ex-spaces]]

[[!redirects ex-object]]
[[!redirects ex-objects]]


