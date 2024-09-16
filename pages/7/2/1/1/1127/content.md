
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

_Grothendieck categories_ are those [[abelian category|abelian categories]] $\mathcal{A}$

* such that for [[presheaf|presheaves]] on a [[site]] with values in $\mathcal{A}$ there is an existence theorem for the  [[sheafification]] functor;

* such that all [[complexes]] in $\mathcal{A}$ (with respect to a [[category with translation|translation]]) are [[quasi-isomorphism|quasi-isomorphic]] to [[injective object|homotopically injective]] complexes (so that [[derived functor on a derived category|derived functor]] can be computed on homotopically injective replacements).

More abstractly, Grothendieck categories are precisely [[Ab-enriched]] [[Grothendieck topos]]es. This follows from the [[Gabriel-Popescu theorem]] together with the theory of [[enriched sheaves]].

## Definition

In terms of the AB$n$ hierarchy discussed at [[additive and abelian categories]] we have

A **Grothendieck category** is an [[additive and abelian categories|AB5-category]] which has a [[separator|generator]].

This means that a **Grothendieck category** is an [[abelian category]]

* that admits a [[separator|generator]];

* that admits small [[colimits]];

* such that small [[filtered category|filtered]] [[colimits]] are _[[exact functor|exact]]_ in the following sense:

  * for $I$ a [[direction|directed set]] and $0 \to A_i \to B_i \to C_i \to 0$ an [[exact sequence]] for each $i \in I$, then $0 \to colim_i A_i \to colim_i B_i \to colim_i C_i \to 0$ is also an [[exact sequence]].

Dually a *co-Grothendieck category* is an AB5$^*$ category 
with a [[cogenerator]]. The category of abelian groups is not a co-Grothendieck category. Any abelian category which is simultaneously Grothendieck and co-Grothendieck has just a single object (see Freyd's book, p.116). 


## Properties

A Grothendieck category $C$ satisfies the following properties.

* it admits small [[limits]];

* if a functor $F : C^{op} \to Set$ commutes with small [[limits]], the $F$ is [[representable functor|representable]];

* if a functor $F : C^{op} \to Set$  commutes with small [[colimits]], then $F$ has a [[adjoint functor|right adjoint]].

* The [[Gabriel-Popescu theorem]] exhibits any [[Grothendieck abelian category]] as a [[reflective subcategory]] of a [[category of modules]] over a [[ring]].

* Any [[Grothendieck abelian category]] is [[locally presentable]].

  ([Beke (2000), Prop. 3.10](#Beke00), see also [Krause (2015), Corollary 5.2](#Krause) and references therein.)

* More generally, any [[cocomplete]] [[abelian category]] with a [[set]] of [[generators]] in which $\kappa$-[[filtered colimits]] commute with [[finite limits]] for some [[regular cardinal]] $\kappa$ is a [[locally presentable category]].  See [Positselski-Rosicky](#PositselskiRosicky), Theorem 2.2.

* If $C$ is equipped with [[category with translation|translation]] $T : C \to C$, then for every [[complex]] $X \in Cplx(C)$ there exists a [[quasi-isomorphism]] of [[complex]]es $X \to I$ such that $I$ is [[injective object|homotopically injective]].

* it satisfies Pierre Gabriel's sup property: every small family of subobjects of a given object $X$ has a [[supremum]] which is a subobject of $X$; 

* it admits an [[injective object|injective]] [[cogenerator]] (see [Kashiwara-Schapira](#KS), Theorem 9.6.3). 

Much of the localization theory of rings generalizes to general Grothendieck categories. 

## Examples

\begin{example}\label{CateoriesOfModules}
**($R$[[Mod]] is Grothendieck abelian)**
\linebreak
For $R$ a [[commutative ring]], its [[category of modules]] $R$[[Mod]] is a Grothendieck category. 
(See e.g [Kiersz 06, prop. 4](#Kiersz) for the proof that filtered colimits here are exact.)
This statement remains true [[internalization|internal]] to any [[Grothendieck topos]] &lbrack;[Johnstone (1977), Thm. 8.11 (iii)](#Johnstone1977)&rbrack;.
\end{example}

\begin{example}\label{CategoriesOfVectorSpaces}
**([[Vect]] is Grothendieck abelian)**
\linebreak
Taking $R$ in Exp. \ref{CateoriesOfModules} to be a [[field]] it follows that [[categories of vector spaces]] are Grothendieck abelian. 
\end{example}

\begin{example}\label{ChainComplexesInGrothAbCat}
**([[category of chain complexes|$Ch_\bullet(\mathcal{A}_{Gr})$]] is Grothendieck abelian)**
\linebreak
For $\mathcal{A}$ a Grothendieck category, the (unbounded) [[category of chain complexes]] $Ch_\bullet(\mathcal{A})$ in $\mathcal{A}$ is again a Grothendieck category (e.g. [Hovey (1999), p. 3](#Hovey99)).

With Exp. \ref{CateoriesOfModules} it follows that the usual categories $Ch_\bullet(R Mod)$ of [[chain complexes]] of [[modules]] over a [[ring]] are all Grothendieck abelian.
\end{example}

\begin{example}
**([[category of ind-objects|$Ind(\mathcal{A})$]] is Grothendieck abelian)**
\linebreak
For $\mathcal{A}$ a [[small category|small]] [[abelian category]], the category $Ind(\mathcal{A})$ of [[ind-objects]] in $C$ is a Grothendieck category. \end{example}


## Related concepts

* [[sheaf of abelian groups]]

* [[abelian sheaf cohomology]]


## References

A dedicated survey is

* Grigory Garkusha, _Grothendieck categories_, Algebra i Analiz 2001, 55 pp. [pdf](https://www.researchgate.net/profile/Grigory_Garkusha/publication/2142579_Grothendieck_Categories/links/570e36d408aec783ddd1ba89.pdf)

Grothendieck categories are mentioned at the end of section 8.3 in

* {#KS} [[Masaki Kashiwara]], [[Pierre Schapira]], _[[Categories and Sheaves]]_

The relation to complexes is in section 14.1.

The proof that filtered colimits in $R Mod$ are exact is spelled out for instance in 

* {#Kiersz} Andy Kiersz, _Colimits and homological algebra_, 2006 ([pdf](http://www.math.uchicago.edu/~may/VIGRE/VIGRE2006/PAPERS/Kiersz.pdf))

Proof that $R$[[Mod]] internal to any Grothendieck topos is Grothendieck abelian:

* {#Johnstone1977} [[Peter Johnstone]]: Theorem 8.11 in: *[[Topos Theory]]*, Academic Press (1977) Dover reprint (2014)

See also:

* [[Peter Freyd]], _Abelian categories_, Harper (1966O) 

* Nicolae Popescu, *An introduction to Abelian categories with applications to rings and modules*_, Academic Press 1973

The fact that all Grothendieck categories are [[locally presentable]]:

* {#Beke00} [[Tibor Beke]], Prop. 3.10 in: *Sheafifiable homotopy model categories*, Math. Proc. Cambridge Philosophical Society **129** 3 (2000) 447-475 &lbrack;[arXiv:math/0102087](https://arxiv.org/abs/math/0102087), [doi:10.1017/S0305004100004722](https://doi.org/10.1017/S0305004100004722)&rbrack;

* {#Krause15} [[Henning Krause]], Corollary 5.2 in: _Deriving Auslander's formula_, Documenta Math. **20** (2015) 669-688 &lbrack;[arXiv:1409.7051](https://arxiv.org/abs/1409.7051)&rbrack;

A generalization to $\kappa$-Grothendieck categories (defined using $\kappa$-filtered colimits) is proved in Theorem 2.2 of

* {#PositselskiRosicky} [[Leonid Positselski]], [[Jiří Rosický]], _Covers, envelopes, and cotorsion theories in locally presentable abelian categories and contramodule categories_, [arXiv:1512.08119](https://arxiv.org/abs/1512.08119).

The duality of Grothendieck categories with categories of modules over [[linearly compact ring]]s is discussed in

*  U. Oberst, _Duality theory for Grothendieck categories and linearly compact rings_, J. Algebra __15__ (1970), p. 473 --542, [pdf](https://core.ac.uk/download/pdf/82581773.pdf)

Discussion of [[model structures on chain complexes]] in Grothendieck abelian categories is in

* [[Denis-Charles Cisinski]], F. D&#233;glise, _Local and stable homologial algebra in Grothendieck abelian categories_, Homology, Homotopy and Applications, vol. 11 (1) (2009)  ([pdf](http://www.intlpress.com/HHA/v11/n1/a11/v11n1a11.pdf))

Formalization of Grothendieck categories as [[univalent categories]] in [[homotopy type theory]]:
Formalization of [[abelian category|abelian]] [[univalent categories]] of [[ring]]-[[modules]], in [[homotopy type theory]] ([[univalent foundations of mathematics]]):

* [[Jarl G. Taxerås Flaten]], Section 3.1 in *Univalent categories of modules* &lbrack;[arXiv:2207.03261](https://arxiv.org/abs/2207.03261)&rbrack;

On Grothendieck abelian categories of chain complexes:

* {#Hovey99} [[Mark Hovey]], p. 3 of: *Model category structures on chain complexes of sheaves* (1999) &lbrack;[K-theory:0366](https://faculty.math.illinois.edu/K-theory/0366), [pdf](https://faculty.math.illinois.edu/K-theory/0366/sheaves.pdf), [[Hovey-SheavesOfChainComplexesPreprint.pdf:file]]&rbrack;

which was published as

* {#Hovey01} [[Mark Hovey]], _Model category structures on chain complexes of sheaves_, Trans. Amer. Math. Soc. **353** 6 (2001) &lbrack;[ams:S0002-9947-01-02721-0](https://www.ams.org/journals/tran/2001-353-06/S0002-9947-01-02721-0), [jstor:221954](https://www.jstor.org/stable/221954)&rbrack;  

Two bicategories of $k$-linear Grothendieck categories as a [[bicategories of fractions]]

* [[Julia Ramos González]], _Grothendieck categories as a bilocalization of linear sites_, Appl Categor Struct 26, 717--745 (2018) [doi](https://doi.org/10.1007/s10485-017-9511-1)


[[!redirects Grothendieck categories]]

[[!redirects Grothendieck abelian category]]
[[!redirects Grothendieck abelian categories]]
