

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea


The _[[Pontryagin theorem]]_ ([Pontryagin 38a](#Pontryagin38a), [50](#Pontryagin50), [55 II.6](#Pontryagin55)) identifies, for a [[closed manifold|closed]] [[smooth manifold]] $M^d$

* the [[cobordism classes]] of [[normally framed submanifolds|normally framed]] [[closed manifold|closed]] [[submanifolds]] of [[codimension]] $n$  in $M^d$

with 

* the $n$-[[Cohomotopy]] of $M^d$ -- the [[homotopy classes]] of [[maps]] from $M^d$ into the [[n-sphere]];

via 

\begin{imagefromfile}
    "file_name": "PontryaginConstruction.jpg",
    "float": "right",
    "width": 540,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [SS 2021](https://ncatlab.org/schreiber/show/M-Theory+as+Mf-Theory)"
\end{imagefromfile}


* the _[[Cohomotopy charge map]]_, often known as the _[[Pontryagin-Thom collapse construction]]_, which sends a [[normally framed submanifold]] $\Sigma^{d-n} \subset M^d$ to the [[continuous function]] taking values in the [[one-point compactification]] $\big( \mathbb{R}^n \big)^{cpt} \simeq S^n$ that assigns to points in $M^d$ sufficiently close to $\Sigma$ their "directed distance" from $\Sigma$, namely their [[normal vector]], and regards all other points as being "[[vanishing at infinity|at infinity]]":

\begin{xymatrix@C=20pt}
  {\phantom{AAA}}
  \overset{
    \mathclap{
    \raisebox{3pt}{
      \tiny
      \color{blue}
      \bf
      \begin{tabular}{c}
        unstable
        \\
        framed Cobordism
      \end{tabular}
    }
    }
  }{
  \mathrm{Cob}^{n}_{\mathrm{Fr}}
    \big(
      M^d
    \big)
  }
  \ar@{}[r]
  |-{:=}
  &
  \mathrm{NFramedSubMflds}_{d-n}
  \big(
    M^d
  \big)_{\!\!\big/\mathrm{brdsm}}
  \ar@<+10pt>[rr]
    ^-{
      \mbox{
        \tiny
        \color{olive}
        \bf
        \begin{tabular}{c}
          asymptotic directed distance
        \end{tabular}
      }
    }
  \ar@{}[rr]
    |-{ \simeq }
  \ar@<-10pt>@{<-}[rr]
    _-{
      \mbox{
        \tiny
        \color{olive}
        \bf
        regular pre-image of $0$
      }
    }
  &
  {\phantom{AAAAA}}
  &
  \mathrm{Maps}
  \big(
    M^d
    \,,\,
    S^n
  \big)_{\!\!\big/ \mathrm{hmpty}}
  \ar@{}[r]
    |-{ =: }
  &
  \overset{
    \mathclap{
    \raisebox{3pt}{
      \tiny
      \color{blue}
      \bf
      \begin{tabular}{c}
        unstable
        \\
        Cohomotopy
      \end{tabular}
    }
    }
  }{
    \pi^n
    \big(
      M^d
    \big)
  }
\end{xymatrix}

In this form, with the assumption that $M^d$ is [[closed manifold|closed]], hence [[compact topological space|compact]], the statement appears for instance in [Kosinski 93, Sec. IX Prop. 5.5](#Kosinski93).

More generally, if the [[smooth manifold]] $M^d$ is not assumed to be [[compact topological space|compact]], essentially the same [[Pontryagin-Thom construction]] still gives an identification of the [[cobordism classes]] of its [[normally framed submanifolds]] with the _[reduced Cohomotopy](cohomotopy#ReducedCohomotopy)_ of its [[one-point compactification]]:

\begin{xymatrix@C=20pt}
  \overset{
    \mathclap{
    \raisebox{3pt}{
      \tiny
      \color{blue}
      \bf
      \begin{tabular}{c}
        unstable
        \\
        framed Cobordism
      \end{tabular}
    }
    }
  }{
  \mathrm{Cob}^{n}_{\mathrm{Fr}}
    \big(
      M^d
    \big)
  }
  \ar@{}[r]
  |-{:=}
  &
  \mathrm{NFramedSubMflds}_{d-n}
  \big(
    M^d
  \big)_{\!\!\big/\mathrm{brdsm}}
  \ar@<+10pt>[rr]
    ^-{
      \mbox{
        \tiny
        \color{olive}
        \bf
        \begin{tabular}{c}
          asymptotic directed distance
        \end{tabular}
      }
    }
  \ar@{}[rr]
    |-{ \simeq }
  \ar@<-10pt>@{<-}[rr]
    _-{
      \mbox{
        \tiny
        \color{olive}
        \bf
        regular pre-image of $0$
      }
    }
  &
  {\phantom{AAAAA}}
  &
  \pi_0
  \mathrm{Maps}^{\ast/\!}
  \Big(
    \big(
      M^d
    \big)^{\mathrm{cpt}}
    \,,\,
    S^n
  \Big)
  \ar@{}[r]
    |-{ =: }
  &
  \overset{
    \mathclap{
    \raisebox{3pt}{
      \tiny
      \color{blue}
      \bf
      \begin{tabular}{c}
        unstable
        \\
        reduced Cohomotopy
      \end{tabular}
    }
    }
  }{
    {\widetilde \pi}{}^n
    \Big(
      \big(
        M^d
      \big)^{\mathrm{cpt}}
    \Big)
  }
\end{xymatrix}

This form of Pontryagin's theorem seems to be [[folklore]] (e.g. [here](https://www.tdx.cat/bitstream/handle/10803/129511/FCM_THESIS.pdf#page=8)). It is made fully explicit in [Csépai 20, p. 12-13](#Csepai20).

An analogous statement, identifying [[cobordism classes]] of [[normally oriented submanifolds]] with [[homotopy classes]] of maps into the [[universal vector bundle|universal]] [[special orthogonal group|special orthogonal]] [[Thom space]] $M SO(n)$, is _[[Thom's theorem]]_ ([Thom 54](#Thom54)):

\begin{xymatrix@C=20pt}
  {\phantom{AA}}
  \overset{
    \mathclap{
    \raisebox{3pt}{
      \tiny
      \color{blue}
      \bf
      \begin{tabular}{c}
        unstable
        \\
        oriented Cobordism
      \end{tabular}
    }
    }
  }{
  \mathrm{Cob}^{n}_{\mathrm{SO}}
    \big(
      M^d
    \big)
  }
  \ar@{}[r]
  |-{:=}
  &
  \mathrm{NOrientedSubMflds}_{d-n}
  \big(
    M^d
  \big)_{\!\!\big/\mathrm{brdsm}}
  \ar@<+10pt>[rr]
    ^-{
      \mbox{
        \tiny
        \color{olive}
        \bf
        \begin{tabular}{c}
          asymptotic directed distance
        \end{tabular}
      }
    }
  \ar@{}[rr]
    |-{ \simeq }
  \ar@<-10pt>@{<-}[rr]
    _-{
      \mbox{
        \tiny
        \color{olive}
        \bf
        regular pre-image of $B \mathrm{SO}(n)$
      }
    }
  &
  {\phantom{AAAAA}}
  &
  \pi_0
  \mathrm{Maps}^{\ast/\!}
  \Big(
    \big(
      M^d
    \big)^{\mathrm{cpt}}
    \,,\,
    M \mathrm{SO}(n)
  \Big)
  {\phantom{AAAAAAAA}}
\end{xymatrix}

(Now the notion of asymptotic directed distance depends on the [[normal bundle|normal tangent spaces]], along $\Sigma$, which themselves vary now in the [[Grassmannian]] $Gr_n$, hence in the [[classifying space]] $B SO(n) \subset M SO(n)$.)


Both statements, Pontryagin's and Thom's, as well as their joint generalization to other [[tangential structures]] (besides framing and orientation structure) and notably their [[stabilization]] to [[Whitehead-generalized cohomology theory|Whitehead-generalized]] [[Cobordism cohomology theory]], have all come to be widely known as _the [[Pontryagin-Thom construction]]_, or similar, a term commonly used also for rather more involved cases, such as in [[MUFr]]-theory. This type of construction constitutes the basis of modern [[cobordism theory]] and its application in [[stable homotopy theory]].

\linebreak

## References


[[!include Pontryagin-Thom construction -- references]]





[[!redirects Pontryagin isomorphism]]
[[!redirects Pontryagin's isomorphism]]

[[!redirects Pontrjagin isomorphism]]
[[!redirects Pontrjagin's isomorphism]]

[[!redirects Pontryagin theorem]]
[[!redirects Pontrjagin theorem]]

[[!redirects Pontryagin's theorem]]
[[!redirects Pontrjagin's theorem]]

[[!redirects Pontryagin construction]]
[[!redirects Pontryagin's construction]]
[[!redirects Pontryagin constructions]]
[[!redirects Pontryagin's constructions]]

[[!redirects Pontrjagin construction]]
[[!redirects Pontrjagin's construction]]
[[!redirects Pontrjagin constructions]]
[[!redirects Pontrjagin's constructions]]


