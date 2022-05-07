
[[frame#As sites|section link test]]

Please do not delete the following example for the moment!

An article by \cite{vandenBergGarner2011} and another by \cite{MarraReggio2020}.

\section{References}

\bibitem{MarraReggio2020}

\bibitem{vandenBergGarner2011}

\linebreak

\bibitem{Witten1995}

\linebreak

\linebreak

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
        pre-image of regular value
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
  }{
    \pi^n
    \big(
      M^d
    \big)
  }
\end{xymatrix}



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
        pre-image of regular value
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
  }{
    {\widetilde \pi}{}^n
    \Big(
      \big(
        M^d
      \big)^{\mathrm{cpt}}
    \Big)
  }
\end{xymatrix}



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
        pre-image of $B \mathrm{SO}(n)$
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

\begin{prop}
  For $n \geq 1$ a [[positive number|positive]] [[natural number]] and $(X,x)$ a [[pointed topological space]]/[[pointed homotopy type]], the canonical [[morphism]] from reduced to unreduced Cohomotopy of $X$ in degree $n$ is an [[isomorphism]]:

$$
  {\widetilde \pi}^{n \geq 1}(X,x)
    \overset{\;\;\simeq\;\;}{\longrightarrow}
  {\pi}^{n \geq 1}(X)
  \,.
$$
\end{prop}
\begin{proof}
  For $Maps(-,-)$ denoting [[compact-open topology|mapping space]] for [[topological spaces]] and $Maps^{\ast/}(-,-)$ the subspace for [[pointed topological spaces]], observe that 

$$
  Maps^{\ast/}\big((X,x),(S^n,\ast) \big)
    \overset{fib(ev_x)}{\longrightarrow}
  Maps\big(X,S^n \big)
    \overset{ev_x}{\longrightarrow}
  S^n
$$

(where $ev_x$ is the [[evaluation map]] at $x \in X$) is a [[homotopy fiber sequence]] as soon as $X$ is represented by a [[cell complex]] (e.g. [[CW-complex]]). 

(This follows either from the [pullback-power axiom](enriched+model+category#PullbackPowerAxiom) in the [[classical model structure on topological spaces]], or, more abstractly from the characterization of [[derived hom-spaces]] in [[slice (infinity,1)-category|coslice (infinity,1)-categories]] [here](slice+infinity-category#HamSpacesInASlice)).

Therefore we have the corresponding [[long exact sequence of homotopy groups]], which starts out as

\begin{xymatrix@C=20pt}
  \pi_1\big( S^n \big)
  \ar[r]
  \ar@{=}[d]
  & 
  \pi_0 \mathrm{Maps}^{\ast/}\big((X,x),(S^n,\ast) \big)
  \ar[r]^{  }
  \ar@{=}[d]
  &
  \pi_0 \mathrm{Maps}\big(X,S^n \big)
  \ar[r]
  \ar@{=}[d]
  &
  \pi_0(S^n)
  \ar@{=}[d]
  \\
  {\overbrace{
  \begin{array}{ccc}
    \mathbb{Z} &\!\!\vert\!\!& n = 1
    \\
    \ast &\!\!\vert\!\!& n \geq 2
  \end{array}
  }}
  \ar[r]
  &
  {\widetilde \pi}{}^n(X,x)    
  \ar[r]
  &
  {\pi}{}^n(X)
  \ar[r]
  &
  \ast
  \,.
\end{xymatrix}

By exactness, this yields the claim for $n \geq 2$; while for $n = 1$ it gives the desired isomorphism only up to a possibly non-trivial [[quotient set|quotient]] by an [[action]] of $\mathbb{Z} \simeq \pi_1(S^1)$:

$$
  {\widetilde \pi}{}^1(X,x)/\pi_1(S^1)
  \simeq
  \pi^1(X)
  \,.
$$

Hence it is now sufficient to see that the $\pi_1(S^1)$-[[action]] on reduced 1-Cohomotopy is always trivial:

The action of $n \in \pi_1(S^1)$ takes $\big[ (X,x) \overset{ \;c\; }{\longrightarrow} (S^1,\ast) \big]$ to any $\big[ (X,x) \overset{ \;c'\; }{\longrightarrow} (S^1,\ast) \big]$ such that $[X \overset{c}{\longrightarrow} S^1] \overset{\eta}{\Rightarrow} [X \overset{c'}{\longrightarrow} S^1]$ in $\pi^1(X)$, with $[\eta(x,-)] = n \in \pi_1(S^1)$. 

But using the [[group]]-structure on $S^1 = \mathbb{R}/\mathbb{Z}$  we have that one such $\eta$ is given by $\eta(x,t) \coloneqq c(x) + n t \,mod\, \mathbb{Z}$, which yields $c'(x) = c(x) + n \,mod\, \mathbb{Z}$ and hence $c' = c$.

\end{proof}


\medskip


#Contents#
* table of contents
{:toc}


## Idea

Several classes of [[string theory vacua]] require the presence of exactly 24 [[branes]] of [[codimension]] 4 transverse to a [[K3-surface]]-[[fiber]]:

This happens notably

* in [[F-theory]] on an [[elliptically fibered K3-surface]], which requires/implies the presence of 24 [[D7-branes]];

* in [[HET-theory]] [[KK-compactification|KK-compactified]] on a [[K3-surface]] with vanishing [[gauge field]] [[instanton number]], which requires/implies the presence of 24 [[NS5-branes]]. 

In both cases the condition arises as a kind of [[tadpole cancellation]]-condition, where the charge of the 24 branes in the [[compact topological space|compact]] K3-fiber space, which naively would be 24 in natural units, cancels out to zero, due to some subtle effect.

Despite the superficial similarity, this subtle effect is, at the face of it, rather different in the two cases:

* for [[F-theory]] it results from the [[Kodeira classification]] of [[elliptic fibrations]], which implies that an [[elliptically fibered K3]] as exactly 24 singular points, counted with multiplicity,

* for [[HET-theory]] it results, via the [[Green-Schwarz mechanism]], from the [[Euler characteristic]] of a [[K3-surface]] being 24, and hence vanishing, via the [[Poincare-Hopf theorem]], after the locus of 24 [[NS5-brane]] loci are cut out.

An argument that these two different-looking mechanisms are in fact equivalent, under suitable [[duality in string theory]], is given in [Braun-Brodie-Lukas-Ruehle 18, Sec. III](#BraunBrodieLukasRuehle18), following detailed analysis due to [Aspinwall-Morrison 97](#AspinwallMorrison97).




### In F-theory on K3
 {#InFTheoryOnK3}


In passing from [[M-theory]] to [[type IIA string theory]], the locus of any [[Kaluza-Klein monopole]] in 11d becomes the locus of [[D6-branes]] in 10d. The locus of the [[Kaluza-Klein monopole]] in turn (as discussed there) is the locus where the $S^1_A$-circle fibration degenerates. Hence in F-theory this is the locus where the fiber of the $S^1_A \times S^1_B$-[[elliptic fibration]] degenerates to the [[nodal curve]]. Since the [[T-duality|T-dual]] of [[D6-branes]] are [[D7-branes]], it follows that [[D7-branes]] in F-theory "are" the singular locus of the elliptic fibration.

Now an [[elliptically fibered complex K3-surface]] 

$$
  \array{
    T &\longrightarrow& K3
    \\
    && \downarrow
    \\
    && \mathbb{C}\mathbb{P}^1
  }
$$

may be parameterized via the [[Weierstrass elliptic function]] as the solution locus of the equation

$$
  y^2 = x^3 + f(z) x + g(z)
$$

for $x,y,z \in \mathbb{C}\mathbb{P}^1$, with $f$ a [[polynomial]] of degree 8 and $g$ of degree twelve. The [[j-invariant]] of the complex [[elliptic curve]] which this parameterizes for given $z$ is

$$
  j(\tau(z)) = \frac{4 (24 f)^3}{27 g^2 + 4 f^3} 
  \,.
$$

The [[poles]] $j\to \infty$ of the [[j-invariant]] correspond to the [[nodal curve]], and hence it is at these poles that the [[D7-branes]] are located. 

\begin{imagefromfile}
        "file_name": "K3CobordismBetween24ThreeSpheres.jpg",
        "web": "nlab",
        "width": 260,
        "unit": "px",
        "float": "right",
        "margin": {
            "top": -40,
            "right": 0,
            "bottom": 20,
            "left": 20,
            "unit": "px"
        },
        "alt": "homotopy pasting diagram exhibiting the homotopy Whitehead integral",
        "caption": "from [SS21](https://ncatlab.org/schreiber/show/Equivariant+Cohomotopy+and+Oriented+Cohomology+Theory)"
\end{imagefromfile}

Since the order of the poles is 24 (the polynomial degree of the [[discriminant]] $\Delta = 27 g^2 + 4 f^3$, see at _[[elliptically fibered K3-surface]]  -- [singular points](elliptic+fibration+of+a+K3-surface#SingularPoints)_) there are necessarily _24 D7-branes_ ([Sen 96, page 5](#Sen96), [Sen 97b](#Sen97b), see also [Morrison 04, sections 8 and 17](#Morrison04), [Denef 08, around (3.41)](#Denef08), [Douglas-Park-Schnell 14](duality+between+M%2FF-theory+and+heterotic+string+theory#DouglasParkSchnell14)).


Notice that the _net charge_ of these 24 D7-branes is supposed to vanish, due to [[S-duality]] effects (e.g. [Denef 08, below (3.41)](#Denef08)).

### In IIA-theory on K3

Under [[T-duality]] the [above](#InFTheoryOnK3) discussion in [[F-theory]] translates to 24 [[D6-branes]] in [[type IIA string theory]] on [[K3]] ([Vafa 96, Footnote 2 on p. 6](#Vafa96)).

### In HET-theory on K3

In [[heterotic string theory]] [[KK-compactification|KK-compactified]] on [[K3]] with vanishing [[gauge fields]]-[[instanton number]], the existence of exactly 24 [[NS5-branes]] is implied by the [[Green-Schwarz mechanism]]: This requires that the 3-flux density $H_3$ measuring the [[NS5-brane]] charge satisfies $ d H_3 = \trac{1}{2} p_1(\nabla)$; and using that on [[K3]] we have $\int_{K3} \tfrac{1}{2} p_1(\nabla)  = \int_{K3} \chi_4(\nabla) = \chi_4[K3] = 24$ this implies, with [[Stokes' theorem]], that the $H_3$-flux through the [[3-spheres]] around transversal [[NS5-brane]]-punctures of the K3 equals 24
(e.g. [Schwarz 96, around p. 50](duality+in+string+theory#Schwarz97), [Aspinwall-Morrison 97, Sec. 4-5](#AspinwallMorrison97), [Johnson 98, p. 30](#Johnson98), [Braun-Brodie-Lukas-Ruehle 18, Section III.A](#BraunBrodieLukasRuehle18), [Choi-Kobayashi 19, Sec. 1.1](#ChoiKobayashi19)).


The [[duality in string theory|duality]] of this HET-phenomenon with that in F-theory [above](#InFTheoryOnK3) is discussed in [Braun-Brodie-Lukas-Ruehle 18, Section III](#BraunBrodieLukasRuehle18).

### Under Hypothesis H

The vanishing of the [[Euler characteristic]] of K3 after cutting out the [[complement]] of 24 points is precisely the mechanism which witnesses the [[order of a group|order]] 24 of the [[third stable homotopy group of spheres]], seen under [[Pontryagin's theorem]] as the existence of a [[framed manifold|framed]] [[cobordism]] $K3 \setminus 24 \cdot D^4$ between 24 [[3-spheres]]:

\begin{imagefromfile}
    "web": "schreiber",
    "file_name": "24BranesTransversalToK3ViaHypothesisH-20210207.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [SS21](https://ncatlab.org/schreiber/show/M-Theory+as+Mf-Theory)"
\end{imagefromfile}

This relates the number of 24 branes transverse on K3 to [[schreiber:Hypothesis H]]:

\begin{imagefromfile}
    "web": "schreiber",
    "file_name": "KKOn24PuncturedK3ViaHypothesisH-20210207.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [SS21](https://ncatlab.org/schreiber/show/M-Theory+as+Mf-Theory)"
\end{imagefromfile}





## References

### In F-theory

Discussion in [[F-theory]]:

* {#Sen96} [[Ashoke Sen]], _F-theory and Orientifolds_, Nucl. Phys. B475:562-578,1996 ([arXiv:hep-th/9605150](http://arxiv.org/abs/hep-th/9605150))


* {#Sen97b} [[Ashoke Sen]], _A Note on Enhanced Gauge Symmetries in M- and String Theory_, JHEP 9709:001,1997 ([arXiv:hep-th/9707123](http://arxiv.org/abs/hep-th/9707123))

* {#Morrison04} [[David Morrison]], _TASI Lectures on Compactification and Duality_ ([arXiv:hep-th/0411120](http://arxiv.org/abs/hep-th/0411120))

* {#DouglasParkSchnell14} [[Michael Douglas]], Daniel S. Park, Christian Schnell, _The Cremmer-Scherk Mechanism in F-theory Compactifications on K3 Manifolds_, JHEP05 (2014) 135 ([arXiv:1403.1595](https://arxiv.org/abs/1403.1595))

### In HET-theory

Discussion in [[heterotic string theory]] via the [[Green-Schwarz mechanism]] on K3 (see also at _[[small instantons]]_):


* {#Schwarz96} [[John Schwarz]], _Lectures on Superstring and M Theory Dualities_, Nucl. Phys. Proc. Suppl. 55B:1-32, 1997 ([arXiv:hep-th/9607201](https://arxiv.org/abs/hep-th/9607201))

* {#Johnson98} [[Clifford Johnson]], _Études on D-Branes_, in: [[Mike Duff]] et. al. (eds.) _Nonperturbative aspects of strings, branes and supersymmetry_, Proceedings, Trieste, Italy, March 23-April 3, 1998 ([arXiv:hep-th/9812196](https://arxiv.org/abs/hep-th/9812196), [spire:481393](https://inspirehep.net/literature/481393))

* {#ChoiKobayashi19} Kang-Sin Choi, Tatsuo Kobayashi, _Transitions of Orbifold Vacua_,   JHEP07 (2019) 111 ([arXiv:1901.11194](https://arxiv.org/abs/1901.11194))


### In F- and HET-theory

Joint discussion in F- and [[duality in string theory|dual]] HET-theory:

* {#AspinwallMorrison97} [[Paul Aspinwall]], [[David Morrison]], _Point-like Instantons on K3 Orbifolds_, Nucl. Phys. B503 (1997) 533-564 ([arXiv:hep-th/9705104](https://arxiv.org/abs/hep-th/9705104), <a href="https://doi.org/10.1016/S0550-3213(97)00516-6">doi:10.1016/S0550-3213(97)00516-6</a>)


* {#BraunBrodieLukasRuehle18} [[Andreas Braun]], Callum Brodie, [[Andre Lukas]], [[Fabian Ruehle]], _NS5-Branes and Line Bundles in Heterotic/F-Theory Duality_, Phys. Rev. D 98, 126004 (2018) ([arXiv:1803.06190](https://arxiv.org/abs/1803.06190), [doi:10.1103/PhysRevD.98.126004](https://doi.org/10.1103/PhysRevD.98.126004))








