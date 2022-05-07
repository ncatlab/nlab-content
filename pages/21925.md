

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Let 

\[
  \label{TheMap}
  \big[
    X \overset{f}{\longrightarrow} Y
  \big]
\] 

be a [[morphism]] in the [[stable homotopy category]] (for instance the [[stabilization]] of a morphism in the [[classical homotopy category]]) and let $E$ be a [[Whitehead-generalized cohomology theory]] (usually assumed to be at least [[multiplicative cohomology theory|multiplicative]]).

Then the _$d$-invariant of $f$ with respect to $E$_ ([Adams 66, Sec. 3, p. 26](#Adams66), short for "degree invariant", see Example \ref{DInvariantSpecializesToDegreeOfAContinuousFunction} below)  is the class of the corresponding [[pullback in cohomology|pullback]] morphism $f^\ast_E$, regarded as an element of the 0th [[Ext-group]] (i.e. the plain [[hom-object]]) between the $E$-cohomologies of $X$ and $Y$:

\[
  \label{ThePullbackInECohomology}
  d(f)
  \;\coloneqq\;
  f^\ast_E
  \;\in\;
  \big(
    E^\bullet(Y);
    \,
    E^\bullet(X)
  \big)
  \;=\;
  Ext^0
  \big(
    E^\bullet(Y);
    \,
    E^\bullet(X)
  \big)
  \,.
\]

The fancy name is justified by the fact that this is beginning of a hierarchy of more interesting invariants of stable maps seen in $E$-cohomology, each of which defined when the previous one vanishes: The next is the _[[e-invariant]]_, then comes the _[[f-invariant]]_ (e.g. [BL 09, Section 2](#BL09)). These are the elements that appear in the first lines on the second page of the $E$-[[Adams spectral sequence]] for $[X,Y]_\bullet$.

## Properties

### Relation to the Hopf degree
  {#RelationToHopfDegree}

+-- {: .num_example #DInvariantSpecializesToDegreeOfAContinuousFunction} 
###### Example
**([[d-invariant]] specializes to [[degree of a continuous function]])**


In the special case that 

* $E = H\mathbb{Z}$ is [[integral cohomology|integral]] [[ordinary cohomology]];

* $X$ and $Y$ are [[connected topological space|connected]] [[closed manifold|closed]] [[orientation|oriented]] [[topological manifolds]] of the same [[dimension]] $n = dim(X) = dim(Y)$

then the $n$-component of the $d$-invariant (eq:ThePullbackInECohomology)  is the _[[degree of a continuous function|degree]] of $f$_

\[
  \label{DegreeOfAContinuousFunction}
  d^n(f) 
  =
  deg(f)
  \;\in\; 
  Hom_{Ab}
  \big(
    H^n(Y;\mathbb{Z}),
    \,
    H^n(YX;\mathbb{Z})
  \big)
  \;\simeq\;
  \mathbb{Z}
  \,.
\]

If moreover $Y = S^n$ is the [[n-sphere]], so that $f$ represents a class in the $n$th [[Cohomotopy]] of $X$, then $\widetilde H^\bullet(Y; \mathbb{Z})$ is concentrated on $\mathbb{Z}$ in degree $n$ and hence the $n$ component $d^n(f)$ is the full information in the d-invariant.

In this case, the [[Hopf degree theorem]] says that the degree of $f$, and hence the d-invariant of $f$ in integral cohomology, completely characterizes the homotopy class $[f]$.

=--

### Trivializations of the d-invariant
  {#TrivializationsOfThedInvariant}

When the d-invariant vanishes, then the [[e-invariant]] exists. But in fact, classical constructions of the e-invariant proceed via a _choice of a trivialization_ of the d-invariant and conclude by showing the result to be independent of this choice (this is meant to be brought out at _[Adams e-invariant -- Construction via unit cofiber theories](Adams+e-invariant#ConstructionViaUnitCofiberTheories)_). 

Here we discuss the space of choices of trivializations of the d-invariant 
(following [[schreiber:M-Theory as Mf-Theory|SS 21]]):



\begin{definition}[Set of trivializations of the d-invariant]
  \label{SetOfTrivializationsOfTheDInvariant}
  For $E$ a [[multiplicative cohomology theory]] 
  and $n, d \in \mathbb{N}$,
  write
  \begin{equation}
    \label{SetOfTrivializationsOfdInvariant}
    \begin{aligned}
    H^E_{n-1}\!Fluxes\!\big( S^{n+d-1} \big)
    &
    \;\coloneqq\;
    \underset{
      [c] \in \mathbb{S}_{d-1}
    }{\sqcup}
    \pi_0
    \mathrm{Paths}_0^{c^\ast (1^E)}
    \Big(
    \mathrm{Maps}^{\ast/}\!
      \big(
        S^{n+d-1}
        \,,\,
        E^{n}
      \big)
    \Big)
    \end{aligned}
  \end{equation}
  for the [[set]] of [[tuples]] consisting of the 
  [[stable Cohomotopy]] class 
  $\big[ G^{\mathbb{S}}_{n}\!(c) \big]$ 
  of a [[map]] $S^{n+d-1} \xrightarrow{\;c\;}S^{n}$
  and the [[2-homotopy]] class 
  $\big[ H^E_{n-1}\!(c) \big]$
  of a trivialization (if any) of its
  [[d-invariant]] $c^\ast(1^E)$ in $E$-cohomology.    

So an element of $H^E_{n-1}\!Fluxes\!\big( S^{n+d-1} \big)$ (eq:SetOfTrivializationsOfdInvariant) is the [[2-homotopy]] class relative the boundary of a [[homotopy coherent diagram]]of the following form:

\begin{xymatrix@C=75pt@R=36pt}
      S^{n+d-1}
      \ar[rr]_>>{\ }="s"
      \ar[d]
        |-{
          \mathclap{\phantom{\vert^{\vert}}}
          c
          \mathclap{\phantom{\vert_{\vert}}}
        }
      \ar[dr]|-{
        G^{\mathbb{S}}_{n}\!(c)
      }
      ^>>>>>{\ }="t"
      &&
      \ast
      \ar[d]
        |-{
          \mathclap{\phantom{\vert^{\vert}}}
          0
          \mathclap{\phantom{\vert_{\vert}}}
        }
      \\
      S^{n}
      \ar@/_1.3pc/[rr]|-{ \;\Sigma^{n}(1^E)\; }
      \ar[r]|-{
        \;
        \Sigma^{n}
        (1^{\mathbb{S}})
        \;
      }
      &
      \mathbb{S}^{n}
      \ar[r]|-{
        \;
        (e^E)^{n}
        \;
      }
      &
      E^{n}
      %
      \ar@{==>}
        |-{
          \;
          \color{orange}
          H^E_{n-1}\!(c)
          \;
        }
        "s"; "t"
\end{xymatrix}

\end{definition}

\begin{definition}[Unit cofiber cohomology theory]
  \label{UnitCofiberCohomologyTheory}

For $E$ a [[multiplicative cohomology theory]] with unit map $\mathbb{S} \overset{ e^E }{\longrightarrow} E$ we denote the corresponding [[homotopy cofiber]]-theory as follows:

\begin{xymatrix@C=50pt@R=12pt}

    \mathbb{S}
    \ar[dd]
      ^>>{\ }="t"
    \ar[rr]
      ^-{
        \;1^E\;
      }
      _>>{\ }="s"
    &&
    \overset{
      \mathclap{
      \raisebox{4pt}{
        \tiny
        \color{blue}
        \bf
        \begin{tabular}{c}
          $E$-cohomology
        \end{tabular}
      }
      }
    }{
      E
    }
    \ar[dd]
      _-{
        \mathclap{\phantom{\vert^{\vert^{\vert}}}}
        i^E
        \mathclap{\phantom{\vert_{\vert}}}
      }
      ^>>{\ }="t2"
    \ar[rr]
      ^-{
      }
      _>>{\ }="s2"
    &&
    \ast
    \ar[dd]
    \\
    {\phantom{A}}
    \\
    \ast
    \ar[rr]
    &&
    \underset{
      \mathclap{
      \raisebox{-4pt}{
        \tiny
        \color{blue}
        \bf
        \begin{tabular}{c}
          $E$-cofiber
          \\
          cohomology
          \\
          theory
        \end{tabular}
      }
      }
    }{
      E/\mathbb{S}
    }
    \ar[rr]
      |-{ \;\partial^E\; }
      _-{
        \mbox{
          \tiny
          \color{green}
          \bf
          \begin{tabular}{c}
            \phantom{-}
            \\
            boundary
            \\
            operation
          \end{tabular}
        }
      }
    &&
    \underset{
      \mathclap{
      \raisebox{-6pt}{
        \tiny
        \color{blue}
        \bf
        \begin{tabular}{c}
          shifted stable
          \\
          Cohomotopy
        \end{tabular}
      }
      }
    }{
      \Sigma \mathbb{S}
    }
    \,,
    &
    {\phantom{AAA}}
    %
    \ar@{=>}^-{ \mbox{\tiny\rm(po)} }
      "s"; "t"
    \ar@{=>}^-{ \mbox{\tiny\rm(po)} }
      "s2"; "t2"


\end{xymatrix}


\end{definition}



\begin{proposition}[Trivializations of d-invariant are classes in cofiber theory]
  \label{EFluxesAreCocycleInCofiberTheory}
  There is a [[bijection]] 

> No, this is wrong. It's just a map. Will fix...

  between the set
  (eq:SetOfTrivializationsOfdInvariant)
  of trivializations of the d-invariant
  and the [[cohomology group]] of the unit cofiber theory
  $E\!/\mathbb{S}$ (Def. \ref{UnitCofiberCohomologyTheory}):
  
\begin{xymatrix@=18pt}    
     \Big(
       \big[
         G^{\mathbb{S}}_n\!(c)
       \big]
       \,,\,
       \big[
         H^E_{n-1}\!(c)
       \big]
      \Big)
    \ar@{|->}[dd]
    &
     \overset{ \mathllap{
        \mbox{
          \tiny
          \bf
          \begin{tabular}{c}
          \end{tabular}
        }
      }}{
      H^E_{n-1}\mbox{\rm{Fluxes}}\!
      \big(
        S^{n + d - 1}
      \big)
      }
      \ar[rr]^-{ \simeq }
      \ar[dd]
      &&
      \big(
        E \!/\mathbb{S}
      \big)_{d}
      \ar[dd]^{\partial}
      \\
      \\
        \big[
          G^{\mathbb{S}}_n\!(c)
        \big]
      &
      G^{\mathbb{S}}_n\mathrm{Fluxes}
      \big(
        S^{n+d-1}
      \big)
      \ar@{=}[rr]
      &&
      \mathbb{S}_{d-1}
\end{xymatrix}
  compatible with the fibrations
  of both over the underlying stable Cohomotopy classes
  $
    G^{\mathbb{S}}_n Fluxes
    \big(
      S^{n+d-1}
    \big)   
    \;\coloneqq\; 
    \widetilde {\mathbb{S}}{}^d
    \big( S^{n + d - 1}\big)
    \,\simeq\, 
    \mathbb{S}_{d-1}
  $.
\end{proposition}

We give two proofs: A quick abstract one and a more explicit one that proceeds via classes on the cofiber space of $c$. The latter is close to the old argument of [Conner-Floyd 66, Thm. 16.2](MUFr#ConnerFloyd66) (there for $E/\mathbb{S} = $ [[MUFr]], see [this section](MUFr#RelationToMUAndFr) for more).

\begin{proof}\label{QuickAbstractProof}[quick abstract]

By Definition \ref{SetOfTrivializationsOfTheDInvariant}, an element in $H_{n-1}Fluxes^E\big( S^{n+d-1} \big)$ is equivalently the class of a homotopy [[cone]] with tip $\Sigma^{n+d-1} \mathbb{S}$ over the [[cospan]] formed by the ring spectrum unit $e^E$ and the [[zero morphism]]:

\begin{xymatrix@=26pt}
    \Sigma^{n+d-1}\mathbb{S}
    \ar[rr]_>>>{\ }="s"
    \ar[dd]^>>>{\ }="t"
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        c
        \mathclap{\phantom{\vert_{\vert}}}
      }
    &&
    \ast
    \ar[dd]
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        0
        \mathclap{\phantom{\vert_{\vert}}}
      }
    \\
    \\
    \Sigma^n \mathbb{S}
    \ar[rr]
      |-{
        \; \Sigma^n(e^E) \;
      }
    &&
    \Sigma^n E
    %
    \ar@{=>}
      |-{
        \mathclap{\phantom{\vert^{\vert^{\vert}}}}
        {
          \color{orange}
          H^E_{n-1}\!(c)
        }
        \mathclap{\phantom{\vert_{\vert_{\vert}}}}
      }
      "s"; "t"
\end{xymatrix}

But in [[Spectra]] [[homotopy cofiber sequences]] are [[homotopy fiber sequences]] (by [this Prop.](Spectrum#InSpectraHomotopyFiberSequencesAreHomotopyCofiberSequences)), so that by the [[universal property]] of [[homotopy fibers]] the class of the above diagram is equivalently the class of a map from $\Sigma^{n+d-1}\mathbb{S}$ to  $fib\big( \Sigma^{n} e^E \big) \,\simeq\, \Sigma^{n-1} (E/\mathbb{S}$):

\begin{xymatrix@=26pt}
    \Sigma^{n+d-1}\mathbb{S}
    \ar@/_1pc/[dddr]
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        c
        \mathclap{\phantom{\vert_{\vert_{\vert}}}}
      }
    \ar@/^1pc/[rrrd]
    \ar@{-->}[dr]
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        \vdash
        {
          \color{orange}
          H^E_{n-1}\!(c)
        }
        \mathclap{\phantom{\vert_{\vert}}}
      }
    \\
    & 
    \Sigma^{n-1}
    (\mathbb{S}/E)
    \ar[rr]_>>>{\ }="s"
    \ar[dd]^>>>{\ }="t"
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        \partial
        \mathclap{\phantom{\vert_{\vert}}}
      }
    &&
    \ast
    \ar[dd]
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        0
        \mathclap{\phantom{\vert_{\vert}}}
      }      
    \\
    \\
    &
    \Sigma^n \mathbb{S}
    \ar[rr]
      |-{
        \;\Sigma^n(e^E)\;
      }
    &&
    \Sigma^n E
    %
    \ar@{=>} 
      ^-{ \mbox{\tiny\color{orange}(pb)} }
    "s"; "t"
\end{xymatrix}


This implies the claim, by 

$$
  \pi_0
  Maps
  \Big(
    \Sigma^{n+d - 1}\mathbb{S}
    \,,\,
    \Sigma^{n-1} (E/\mathbb{S})
  \Big)
  \;\simeq\;
  (E/\mathbb{S})_{d}
  \,.
$$


\end{proof}

\begin{proof}[more explicit, Conner-Floyd-style]

Let
$\big[ S^{n + d - 1} \overset{c}{\longrightarrow} S^{n} \big] \;\in\; \pi^n\big(S^{n+d-1}\big)$ be a given class in Cohomotopy.
We need to produce a map of the form

\begin{xymatrix@R=10pt}
    {
      \color{orange}
      H^E_{n-1}\!(c)
    }
    \ar@{}[rr]|-{\longmapsto}
    &&
    M^d
    \\
    H_{n-1}\mbox{Fluxes}(X)_c
    \ar[rr]
    \ar[dd]
    &&
    \big(
      E\!/\mathbb{S}
    \big)_d
    \ar[dd]^-{ \partial }
    \\
    {\phantom{A}}
    \\
    \big\{
      [
        \Sigma^\infty c
      ]
    \big\}
    \;
    \ar@{^{(}->}[rr]
    &&
    \;
    \mathbb{S}_{d-1}
\end{xymatrix}

and show that it is a bijection onto this fiber, hence that the square is [[cartesian square|cartesian]]. To this end, we discuss the following [[homotopy coherent diagram|homotopy]] [[pasting diagram]], all of whose cells are homotopy cartesian:

\begin{xymatrix@R=15pt@C=60pt}
    \Sigma^\infty S^{n + d - 1}
    \ar[dd]_-{
      \Sigma^\infty
      {\color{green}
        c
      }
    }
    \ar[rr]
    &&
    \ast
    \ar[dd]
    \\
    \\
    \Sigma^\infty S^{n}
    \ar[dd]
    \ar[rr]|-{ 
      %\;\Sigma^\infty q_c\; 
    }
    \ar@/_1.4pc/[rrr]
      |<<<<<<<<<<<<<<<<<<<{
        \; \Sigma^{n}(e^{E}) \;
      }
    &&
    \Sigma^\infty C_c
    \ar[dd]|<<<<{ \phantom{A} }
    \ar@{-->}[r]
    \ar@{}[r]
    |-{
      \scalebox{.7}{$
        \begin{array}{c}
          \vdash
          {\color{orange}
            H^E_{n-1}\!(c)
          }
          \\
          {\phantom{a}}
        \end{array}
      $}
    }
    \ar@/^2pc/[rr]
    &
    \Sigma^n E
    \ar[r]
    \ar[dd]
    &
    \ast
    \ar[dd]
    \\
    \\
    \ast
    \ar[rr]
    &&
    \Sigma^{\infty\scalebox{.6}{$+1$}} S^{n + d - 1}
    \ar[r]^-{
      \color{magenta}
      M^{d}
    }
    \ar@/_1.2pc/[rr]|-{
      \;
      \Sigma^{\infty\scalebox{.5}{$+1$}}
      {\color{green}
        c
      }
      \;
    }
    &
    \Sigma^{n}(E\!/\mathbb{S})
    \ar[r]^{ \partial }
    &
    \Sigma^{\infty\scalebox{.6}{$+1$}} S^{n}
\end{xymatrix}

For given $H^E_{n-1}\!(c)$, this diagram is constructed as follows
(where we say "square" for any _single_ cell and "rectangle" for the pasting composite of any adjacent _pair_ of them):

* The two squares on the left are the stabilization of the homotopy pushout squares defining the cofiber space $C_c$ and the suspension of $S^{n + d - 1}$

* The bottom left rectangle (with $\Sigma^n(e^E)$ at its top)
is the homotopy pushout defining $\Sigma^n(E\!/\mathbb{S})$.

* The classifying map for the given $(n-1)$-flux, shown as a dashed arrow,
completes a co-cone under the bottom left square. Thus the map ${\color{magenta}M^d}$ forming the bottom middle square is uniquely implied by the homotopy pushout property of the bottom left square.
Moreover, the [[pasting law]] implies that this bottom middle square is itself homotopy cartesian.

* The bottom right square is the homotopy pushout defining $\partial$.

* By the [[pasting law]] it follows that also the bottom right rectangle is homotopy cartesian, hence that, after the two squares on the left, it exhibits the third step in the long homotopy cofiber sequence of $\Sigma^\infty c$. This means that its total bottom morphism is $\Sigma^{\infty + 1} c$, and hence that $\partial \big[ M^d \big] = [c]$.


In conclusion, these construction steps yield a map map $H^E_{n-1}\!(c) \mapsto M^d$ which is as required.

It only remains to see that this map is bijective over any $\Sigma^\infty c$: So assume conversely that $M^d$ is given, and with it the above diagram  except for the dashed arrow. But since the bottom right square is homotopy cartesian, a dashed morphism is uniquely implied. By its uniqueness, this reverse assignment $M^{2d} \mapsto H^E_{n-1}\!(c)$ must be the inverse of the previous construction.

\end{proof}




## Related concepts

* [[degree of a continuous function]], [[Hopf degree theorem]]

* [[e-invariant]]

* [[f-invariant]]

[[!include notions of pullback -- contents]]

## References

The notion was introduced, together with that of the [[e-invariant]], in:

* {#Adams66} [[John Adams]], Section 3 of: _On the groups $J(X)$ IV_, Topology 5: 21 (1966)   ([pdf](http://math.unice.fr/~cazanave/Gdt/ImJ/J-IV.pdf), <a href="https://doi.org/10.1016/0040-9383(66)90004-8">doi:10.1016/0040-9383(66)90004-8</a>)

Discussion in the broader context including also the [[f-invariant]]:

* {#BL09} Mark Behrens, Gerd Laures, _$\beta$-Family congruences and the $f$-invariant_, Geometry & Topology Monographs 16 (2009) 9–29 ([arXiv:0809.1125](https://arxiv.org/abs/0809.1125), [doi: 10.2140/gtm.2009.16.9](https://msp.org/gtm/2009/16/p002.xhtml))
