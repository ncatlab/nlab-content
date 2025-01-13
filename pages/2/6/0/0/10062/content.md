
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

> This section is no good...

Any pretriangulated [[dg-category]] $\mathcal{C}$ presents a [[stable (infinity,1)-category]]. A plain dg-category only presents a spectrally enriched (infinity,1)-category. One way to construct this is to apply the [[Dold-Kan correspondence]] on each [[hom-object]] to produce a fibrant [[sSet-enriched category]] and then, if desired, form the [[homotopy coherent nerve]] of that to obtain a [[quasi-category]]. 

On the other hand, the _dg-nerve_ of $\mathcal{C}$ is a more direct construction that directly sends the dg-category to a [[simplicial set]] which is the [[quasi-category]] incarnation of the corresponding [[stable (∞,1)-category]].

To the extent that one may think of $\mathcal{C}$ as analogous to a [[category of chain complexes]], the dg-nerve may be thought of producing the [[simplicial set]] whose $k$-[[simplices]] are the [[local systems]] on $\Delta^k$ with [[coefficients]] in $\mathcal{C}$ ([[flat ∞-connections]] with coefficients in $\mathcal{C}$). The formula is just as for [[Lie integration]] of [[L-infinity algebroids]]. 

## Properties

### Compatibility with the simplicial nerve
 {#CompatibilityWithSimplicialNerve}

Recall:

\begin{remark}\label{QuasiCategoricalLocalization}
From a [[relative category]] $(\mathcal{C}, \mathrm{W})$ (a [[category with weak equivalences]] $\mathrm{W} \subset Mor(\mathcal{C})$) one obtains:

1. the [[sSet-enriched category]] $\mathcal{C}[\mathrm{W}^{-1}]$ which is its [[simplicial localization]],

1. the [[quasi-category]] which is the [[homotopy coherent nerve]] $N \mathcal{C}[\mathrm{W}^{-1}]$ of that.

or alternatively, up to [[equivalence of quasi-categories]]:

1. the [[simplicial nerve]] $N \mathcal{C}$,

1. its [[localization of a quasi-category|localization as a quasi-category]] $N\mathcal{C}[\mathrm{W}^{-1}]$.

\end{remark}

Now:

\begin{proposition}
For $\mathcal{A}$ an [[additive category]], write

1. $Ch_\bullet(\mathcal{A})$ for the plain [[category of chain complexes]] in $\mathcal{A}$,

1. $\mathbf{Ch}_\bullet(\mathcal{A})$ for the [[dg-category]] obtained form the [[enriched category|self-enrichment]] of $Ch_\bullet(\mathcal{A})$ 

   (via its [[symmetric monoidal category|symmetric monoidal]] structure given by the [[tensor product of chain complexes]]),

1. $\mathrm{W}_{che} \,\subset\, Mor\big(Ch_\bullet(\mathcal{A})\big)$ for the [[class]] of [[chain homotopy equivalences]]

   (which for $\mathcal{A} = k$ [[Vect]] coincide with the [[quasi-isomorphisms]], but not otherwise).

Then the dg-nerve of $\mathbf{Ch}_\bullet(\mathcal{A})$ is [[equivalence of quasi-categories|equivalent as a quasi-category]] to the (homotopy coherent) nerve of the (simplicial) localization of $Ch_\bullet(\mathcal{A})$ at $\mathrm{W}_{che}$ in the sense of Rem. \ref{QuasiCategoricalLocalization}:

$$
  N_{dg}
  \big(
    \mathbf{Ch}_\bullet(\mathcal{A})
  \big)
  \;\;
  \simeq
  \;\;
  N Ch_\bullet(\mathcal{A})[\mathrm{W}^{-1}_{che}]
  \,.
$$
\end{proposition}
&lbrack;[Lurie (2017), Prop. 1.3.4.5](#Lurie17)&rbrack;

Similarly:
\begin{proposition}
  Given $\mathbf{C}$ a [[category of chain complexes|$Ch_\bullet(R Mod)$]]-[[enriched model category]] (over some [[ring]] $R$) all of whose [[objects]] are [[cofibrant object|cofibrant]], then
$$
  N_{dg}(\mathbf{C})
  \;\;
  \simeq
  \;\;
  N C[\mathrm{W}_{che}^{-1}]
$$
where $C$ denotes the [[underlying]] ordinary category and $\mathrm{W}_{che} \subset Mor(C)$ again the class of [[chain homotopy equivalences]].
\end{proposition}
&lbrack;[Gwilliam & Pavlov (2018), Prop. 5.17](#GwilliamPavlov18)&rbrack;


## References

The definition originates with:

* [[Vladimir Hinich]],  [[Vadim Schechtman]], *On homotopy limit of homotopy algebras*, in: *K-Theory, Arithmetic and Geometry -- Seminar, Moscow University, 1984–1986*, Lecture Notes in Mathematics **1289**, Spinger (2006) 240–264 &lbrack;[doi:10.1007/BFb0078363](https://doi.org/10.1007/BFb0078363)&rbrack;

Further discussion:

* {#BlockSmith14} [[Jonathan Block]], [[Aaron M. Smith]], Def. 2.3 (2.4 in the preprint) of: *The higher Riemann--Hilbert correspondence*, Advances in Mathematics **252** (2014) 382-405 &lbrack;[arXiv:0908.2843](https://arxiv.org/abs/0908.2843), [doi:10.1016/j.aim.2013.11.001](https://doi.org/10.1016/j.aim.2013.11.001)&rbrack;
 
* {#Lurie17} [[Jacob Lurie]], Construction 1.3.1.6 in: *[[Higher Algebra]]* (2017)

Extension to [[A-infinity categories|$A_\infty$-categories]], proof that the dg-nerve maps [[pretriangulated dg-categories]] to [[stable (∞,1)-categories]].

* {#Faonte13} [[Giovanni Faonte]], *Simplicial nerve of an $\mathcal{A}_\infty$-category*, Theory and Applications of Categories **32** 2 (2017) 31-52 &lbrack;[arXiv:1312.2127](http://arxiv.org/abs/1312.2127), [tac:32-02](http://www.tac.mta.ca/tac/volumes/32/2/32-02abs.html)&rbrack;

Further discussion:

* {#GwilliamPavlov18} [[Owen Gwilliam]], [[Dmitri Pavlov]], *Enhancing the filtered derived category*, Journal of Pure and Applied Algebra **222** 11 (2018) 3621-3674 &lbrack;[arXiv:1602.01515](https://arxiv.org/abs/1602.01515), [doi:10.1016/j.jpaa.2018.01.004](https://doi.org/10.1016/j.jpaa.2018.01.004)&rbrack;


[[!redirects dg-nerves]]
[[!redirects nerve of a dg-category]]
[[!redirects nerves of dg-categories]]
