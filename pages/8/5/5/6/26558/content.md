
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
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

For $X$ a [[smooth manifold]], the traditional [[coboundary]]-relation which defines the ordinary [[de Rham cohomology]]-classes $[\omega] \in H^n{dR}(X)$ of [[closed differential forms|closed]] [[differential n-forms]] $\omega \in \Omega_{dR}^n(X)_{clsd}$

$$
  [\omega] = [\omega'] 
  \;\;\;\;
     \Leftrightarrow
  \;\;\;\;
  \underset{
    \alpha \in \Omega_{dR}^{n-1}(X)
  }{\exists}
  \omega' = \mathrm{d}\alpha+ \omega
$$

is equivalent to the [[concordance]]-relation &lbrack;[FSS20, Prop. 6.4](#FSS20)&rbrack;

\[
  \label{OrdinaryDeRhamCoboundaryAsConcordance}
  [\omega] = [\omega'] 
  \;\;\;\;
     \Leftrightarrow
  \;\;\;\;
  \underset{
    \widehat{\omega} \in \Omega_{dR}^{n1}(X \times [0,1])_{clsd}
  }{\exists}
  \;
  \left\{
  \begin{array}{l}
    \omega = \widehat\omega\vert_{0}
    \,,
    \\
    \omega' = \widehat\omega\vert_{1}   
    \,.
  \end{array}
  \right.
\]

But the latter [[concordance]]-relation immediately generalizes to [[flat L-infinity algebra valued differential forms|flat $L_\infty$-algebra valued differential forms]]

$$
  \Omega_{dR}\big(
    X;
    \mathfrak{a}
  \big)_{clsd}
  \;\;
  \coloneqq
  \;\;
  Hom_{dgAlg}\big(
    CE(\mathfrak{a})
    ,\,
    \Omega^\bullet_{dR}(X)
  \big)
$$

with [[coefficients]] in any $L_\infty$-algebra $\mathfrak{a}$, which reduces to the ordinary case for $\mathfrak{a} \equiv b^{n-1} \mathbb{R}$ the [[line Lie n-algebra|line Lie $n$-algebra]].

Therefore it makes sense to define &lbrack;[FSS20, Def. 6.3](#FSS20)&rbrack;: 

\begin{definition}
The *non-abelian de Rham cohomology* of a smooth manifold $X$ with [[coefficients]] in a [[L-infinity algebra|$L_\infty$-algebra]] $\mathfrak{a}$ is the [[set]] of [[concordance]] [[equivalence class|classes]] of [[flat L-infinity algebra valued differential forms|flat $\mathfrak{a}$-valued differential forms]] on $X$:

\[
  \label{NonabelianDeRhamCohomology}
  H_{dR}\big(
    X
    ;\,
    \mathfrak{a}
  \big)
  \;\;
  \coloneqq
  \;\;
  \Omega_{dR}\big(
    X
    ;\,
    \mathfrak{a}
  \big) _{clsd}
  \big/
  \mathrm{concordance}
  \,.
\]
\end{definition}

## Examples

\begin{example}
  With (eq:OrdinaryDeRhamCoboundaryAsConcordance) it follows that the ordinary [[de Rham cohomology]] in degree $n$ is equivalently non-abelian de Rham cohomology with [[coefficients]] in the [[line Lie n-algebra]] $b^{n-1}\mathfrak{u}(1)$:
$$
  H_{dR}\big(
    X
    ;\,
    b^{n-1}\mathfrak{u}(1)
  \big)
  \;\;
  \simeq
  \;\;
  H^n_{dR}\big(
    X
    ;\,
    b^{n-1}\mathbb{R}
  \big)
  \,.
$$
\end{example}

\begin{example}\label{TotalFluxInHigherGaugeTheories}
  In [[higher gauge theories]] [of Maxwell-type](higher+gauge+field#HigherGaugeTheoryOfMaxwellType), nonabelian de Rham cohomology of a [[Cauchy surface]] with coefficients in an [[L-infinity algebra]] characteristic of the theory's [[Gauss law]] reflects the *total [[flux]]* of the [[higher gauge fields]]. 

See at *[[geometry of physics -- flux quantization]]* the section *[Total flux in Nonabelian de Rham cohomology](geometry+of+physics+--+flux+quantization#TotalFluxInNonabelianDeRhamCohomology)*.
\end{example}

## Properties

### Recipient of non-abelian character map

For $\mathcal{A}$ (the [[homotopy type]] of) a [[topological space]] which is [[nilpotent topological space|nilpotent]] (for instance: [[simply connected topological space|simply connected]]) and of rational [[finite type]] (all its [[rational cohomology]]-groups are [[finite-dimensional vector spaces|finite-dimensional $\mathbb{Q}$-vector spaces]]) one may regard the [[homotopy classes]] of [[maps]] into $\mathcal{A}$ as the [[nonabelian cohomology]] classified by $\mathcal{A}$ (the non-abelian cohomology in degree=1 with coefficients in the [[loop space]] [[infinity-group|$\infty$-group]] $\Omega \mathcal{A}$ ):

\[
  \label{NonabelianCohomology}
  H\big(
    X
    ;\,
    \mathcal{A}
  \big)
  \;\;
  \coloneqq
  \;\;
  \pi_0
  \,
  Maps\big(
    X
    ,\,
    \mathcal{A}
  \big)
  \;\;
  \simeq
  \;\;
  \pi_0
  \,
  Maps\big(
    X
    ,\,
    B \Omega \mathcal{A}
  \big)
  \;\;
  \equiv
  \;\;
  H^1\big(
    X
    ;\,
    \Omega \mathcal{A}
  \big)
  \,.
\]

For example, in the case that 

$$
  \mathcal{A} \,\equiv\, K(n,A)
$$

is an [[Eilenberg-MacLane space]] for a [[discrete group|discrete]] [[abelian group]] $A$, this reduces to [[ordinary cohomology]]:

$$
  H\big(
    X
    ;\,
    K(n,A)
  \big)
  \;\;
  \simeq
  \;\;
  H^n(X;\, A)
  \,,
$$

or if 

$$
  \mathcal{A}
  \;\equiv\;
  KU_0 
  \,\simeq\,
  B U \times \mathbb{Z}
$$

is the [[classifying space]] [[KU]]$_0$ for complex [[topological K-theory]], then this reduces to to complex topological K-theory:

$$
  H\big(
    X
    ;\,
    KU_0
  \big)
  \;\;
  \simeq
  \;\;
  K(X)
  \,.
$$

Generally, if $\mathcal{E}$ is an [[Omega-spectrum]] of spaces, then 

$$
  H\big(
    X
    ;\,
    E_n
  \big)
  \;\;
  \simeq
  \;\;
  E^n(X)
$$

coincides with the [[Whitehead-generalized cohomology|Whitehead-generalized $E$-cohomology]].
 

Now the [[rationalization]]-[[unit of an adjunction|unit]] $\eta^{\mathbb{Q}}_{\mathcal{A}} \,\colon\, \mathcal{A} \to \mathcal{A}_{\mathbb{Q}}$ followed by suitable [[extension of scalars]] along $\mathbb{Q} \to \mathbb{R}$ induces [[cohomology operations]] in the non-abelian cohomology (eq:NonabelianCohomology), to what may be called non-abelian [[rational cohomology]], and non-abelian [[real cohomology]] with coefficients in $\mathcal{A}$


\[
  \label{TheNonabelianCharacterMap}
  H\big(
    -;\,
    \mathcal{A}
  \big)
  \longrightarrow
  H\big(
    -;\,
    \mathcal{A}_{\mathbb{Q}}
  \big)
  \longrightarrow
  H\big(
    -;\,
    \mathcal{A}_{\mathbb{R}}
  \big)
  \;\;
  \simeq
  \;\;
  H_{dR}\big(
    -
    ;\,
    \mathfrak{l}\mathcal{A}
  \big)
  \,,
\]

and, shown on the right, a non-abelian version of the [[de Rham theorem]] --- given essentially by the [[fundamental theorem of dg-algebraic rational homotopy theory]] --- identifies this non-abelian real cohomology with coefficients in $\mathcal{A}$ with the non-abelian de Rham cohomology (eq:NonabelianDeRhamCohomology) with coefficients in the real-[[Whitehead L-infinity algebra|Whitehead $L_\infty$-algebra]] $\mathfrak{l}\mathcal{A}$ of $\mathcal{A}$.

For the case that $\mathcal{A} = KU_0$ the [[cohomology operation]] (eq:TheNonabelianCharacterMap) coincides with the [[Chern character]] on complex [[topological K-theory]], and generally for $\mathcal{A} = \mathcal{E}_n$ a term in an [[Omega-spectrum]] it coincides with  the [[Chern-Dold character]] map on [[Whitehead-generalized cohomology]] ([Prop. 7.2](#FSS20)).

Therefore, it makes sense to refer to (eq:TheNonabelianCharacterMap) generally as the *character map on nonabelian cohomology* taking values in non-abelian de Rham cohomology ([FSS20, Part IV](#FSS20)).


\begin{imagefromfile}
    "file_name": "NonabCharacter-240123.jpg",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

## Related entries

* [[non-abelian cohomology]]

* [[differential non-abelian cohomology]]


## References

* {#FSS20} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], Part III of: _[[schreiber:The Character Map in Twisted Non-Abelian Cohomology|The Character Map in Nonabelian Cohomology --- Twisted, Differential, Generalized]]_, World Scientific (2023) &lbrack;[arXiv:2009.11909](https://arxiv.org/abs/2009.11909), [doi:10.1142/13422](https://doi.org/10.1142/13422)&rbrack;


[[!redirects nonabelian de Rham cohomology]]

[[!redirects nonabelian de Rham theorem]]
[[!redirects nonabelian de Rham theorems]]

[[!redirects non-abelian de Rham theorem]]
[[!redirects non-abelian de Rham theorems]]



