
> This page is about characterization of [[flat modules]]. For the characterization of the *[[Lazard ring]]* (in [[formal group laws]]) see instead at *[[Lazard's theorem]]*.

***


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


\tableofcontents

## Statement

Let $R$ be a [[ring]], not necessarily [[commutative ring|commutative]].


\begin{proposition}\label{LazardCriterion}
**(Lazard's criterion)**

An left $R$-[[module]] is a [[flat module]] precisely if it is a [[filtered colimit]] of [[finitely generated module|finitely generated]] [[free modules]]. 

\end{proposition}

This is due to [Lazard 1964](#Lazard1964) and [Govorov 1965](#Govorov1965). See at _[[flat module]]_ for more.

\begin{remark}
  Regarding $R$-[[modules]] as [[algebra over a Lawvere theory|models]] of the [[Lawvere theory]] of $R$-modules, whose [[representable functor|representable]] models are the finitely generated free ones, Lazard's criterion (Prop. \ref{LazardCriterion}) splits into two parts:

1. The formal part is the general fact that a model is a [[filtered colimit]] of [[representable functor|representable models]] iff its [[category of elements]] is [[filtered category|filtered]], i.e. iff it is [[flat functor|flat as a functor]] on the theory.

   (This is classical, cf. [[SGA4]] Exp. I; [[Handbook of Categorical Algebra|Borceux 1994]] §I.6.3. For models of [[clans]], which include models of all algebraic theories via finite-product clans, this is stated as [Frey 2026 Lem. 5.4](#Frey2026), where it is likewise deduced from [[Handbook of Categorical Algebra|Borceux 1994]] §I.6.3.) 

2. The genuinely module-theoretic content of Lazard's criterion is that this categorical flatness coincides with [[flat module|flatness of the module]] in the sense of [[homological algebra]].

\end{remark}


## References

The original articles:

* {#Lazard1964} [[Daniel Lazard]]: _Sur les modules plats_, C. R. Acad. Sci. Paris **258** (1964) 6313--6316 

* {#Govorov1965} V. E. Govorov: *On flat modules*, Sibirsk. Mat. Zh., **6** 2 (1965) 300--304 &lbrack;[mathnet:smj5139](https://www.mathnet.ru/eng/smj5139)&rbrack;
 
Exposition for the case of [[commutative rings|commutative]] [[ground rings]]:

* Robert Hines, *Lazard’s theorem (characterizing flatness)* (2016) &lbrack;[pdf](https://math.colorado.edu/~rohi1040/expository/lazardstheorem.pdf), [[Hines-LazardTheorem.pdf:file]]&rbrack;

* [[Stacks Project]], *Lazard's theorem* &lbrack;[tag:058G](https://stacks.math.columbia.edu/tag/058G)&rbrack;

The formal aspect stated in the generality of [[clan]] models:

* {#Frey2026} [[Jonas Frey]]: _Duality for clans: an extension of Gabriel--Ulmer duality_, The Journal of Symbolic Logic  **91** 3 (2026) 913--950 &lbrack;[doi:10.1017/jsl.2024.79](https://doi.org/10.1017/jsl.2024.79), [arXiv:2308.11967](http://arxiv.org/abs/2308.11967)&rbrack;

