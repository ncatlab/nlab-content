
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition
 {#Definition}

Originally, t-structures were defined 

* [on triangulated categories](#OnTriangulatedCategories)

These typically arise as [[homotopy category of an (infinity,1)-category|homotopy categories]] of t-structures

* [on stable $\infty$-categories](#InStableInfinityCategories).


### On triangulated categories
 {#OnTriangulatedCategories}

\begin{definition}\label{tStructure}
**(t-structure on a triangulated category)**
\linebreak
Let $C$ be a [[triangulated category]]. A _t-structure_ on $C$ is a [[pair]] $\mathfrak{t}=(C_{\ge 0}, C_{\le 0})$ of [[strictly full subcategories]]

$$
   C_{\geq 0}, C_{\leq 0} \hookrightarrow C
$$

such that

1. for all $X \in C_{\geq 0}$ and $Y \in C_{\leq 0}$ the [[hom object]] is the [[zero object]]: $Hom_{C}(X, Y[-1]) = 0$;

1. the subcategories are closed under [[suspension]]/desuspension: $C_{\geq 0}[1] \subset C_{\geq 0}$ and $C_{\leq 0}[-1] \subset C_{\leq 0}$.

1. For all [[objects]] $X \in C$ there is a [[fiber sequence]] (i.e. an [[exact triangle]]) $Y \to X \to Z$ with $Y \in C_{\geq 0}$ and $Z \in C_{\leq 0}[-1]$.

\end{definition} 

\begin{definition}
\label{HeartOfATStructure}
Given a t-structure (Def. \ref{tStructure}), its _heart_ is the intersection

$$
  C_{\geq 0} \cap C_{\leq 0}
  \hookrightarrow
  C
  \,.
$$

\end{definition}



### On stable $\infty$-categories
 {#InStableInfinityCategories}


\begin{definition}\label{tStructureOnStableInfinityCategory}
**(t-structure in a stable $\infty$-category)**
\linebreak
  A *t-structure* on a [[stable (∞,1)-category]] $\mathcal{C}$ is a t-structure in the above sense (Def. \ref{tStructure}) on its [[underlying]] [[homotopy category of an (∞,1)-category|homotopy category]] (which is [[triangulated category|triangulated]], see [there](stable+infinity-category#TheTriangulatedHomotopyCategory)).
\end{definition}
([Lurie, Higher Algebra, Def. 1.2.1.4](#LurieHA))

Therefore, a t-structure on a stable $\infty$-category $\mathcal{C}$ is a system of [[full sub-(∞,1)-categories]] $\mathcal{C}_{\geq n}$, $\mathcal{C}_{\leq n}$, $n \in \mathbb{Z}$.

\begin{proposition}
  In this situation (Def. \ref{tStructureOnStableInfinityCategory}) 

1. the $\mathcal{C}_{\leq n} $ are [[reflective sub-(∞,1)-categories]]

   $$
     \mathcal{C}_{\leq n}
     \underoverset
       {\underset{}{\hookrightarrow}}
       {\overset{\tau_{\leq n}}{\longleftarrow}}
       {\;\; \bot \;\;}
     \mathcal{C}
   $$

1. the $\mathcal{C}_{\geq n}$ are [[coreflective sub-(∞,1)-categories]];

   $$
     \mathcal{C}
     \underoverset
       {\underset{\tau_{\geq n}}{\longrightarrow}}
       {\hookleftarrow}
       {\;\; \bot \;\;}
     \mathcal{C}_{\leq n}
   $$
 
\end{proposition}
([Lurie, Higher Algebra, Def. 1.2.1.5, Cor. 1.2.1.6, Ntn. 1.2.1.7](#LurieHA))

<center>
<img src="https://ncatlab.org/nlab/files/HeartOfTStructureAsCoModals-230408.jpg" width="600">
</center>



## Properties

### General

+-- {: .num_prop }
###### Proposition

The heart of a stable $(\infty,1)$-category is an [[abelian category]]. 

=--

([BBD 82](#BeilinsonBernsteinDeligne82), [[Higher Algebra|Higher Algebra, remark 1.2.1.12]], [FL16, Ex. 4.1](#FL16) and [FLM19, &#167;3.1](#FLM19))


### Relation to spectral sequences

If the heart (Def. \ref{HeartOfATStructure}) of a t-structure on a [[stable (∞,1)-category]] with [[sequential limits]] is an [[abelian category]], then the [[spectral sequence of a filtered stable homotopy type]] [converges](spectral+sequence#ConvergenceOfSpectralSequences) (see there).

### Relation to normal torsion theories
 {#RelationToNormalTorsionTheories}

In the [[(∞,1)-category theory]], $t$-structures arise as [[torsion theory|torsion/torsionfree]] classes associated with suitable [[orthogonal factorization system|factorization systems]] on [[stable ∞-categories]] $C$.

* In [[stable ∞-category]]-theory, the relevant sub-[[(∞,1)-categories]] are closed under de/suspension simply because they are (co-)[[reflective sub-(∞,1)-categories|reflective]], arising from co/[[reflective factorization systems]] on $C$.

* A _bireflective_ factorization system on a $\infty$-category $C$ consists of a [[orthogonal factorization system|factorization system]] $\mathbb{F}=(E,M)$ where both classes satisfy the [[two-out-of-three]] property.

* A bireflective factorization system $(E,M)$ on a stable $\infty$-category $C$ is called _normal_ if the diagram $S x\to x\to R x$ obtained from the reflection $R\colon C\to M/0$ and the coreflection $S\colon C\to *\!/E$ (where the category $M/\!* =\{A\mid (0\to A)\in M\}$ is obtained as $\Psi(E,M)$ under the adjunction $\Phi \dashv \Psi$ described at *[[reflective factorization system]]* and in [CHK85](#CHK85); see also [FL16, &#167;1.1](#FL16)) is _exact_, meaning that the square in
$$
\begin{array}{cccccc} 
0 &\to& S X &\to& X\\
&& \downarrow&&\downarrow\\
&& 0 &\to& R X\\
&& && \downarrow\\
&& && 0
\end{array}
$$
is a fiber sequence for any object $X$; see [FL16, Def 3.5 and Prop. 3.10](#FL16) for equivalent conditions for normality.

\begin{remark}
[CHK85](#CHK85) established a hierarchy between the three notions of simple, semi-exact and normal factorization system: in the setting of stable $\infty$-category the three notions turn out to be equivalent: see [FL16, Thm 3.11](#FL16).
\end{remark}

\begin{proposition}
\label{CorrespondenceWithNormalTorsionTheories}
There is a bijective correspondence between the class $TS( C )$ of $t$-structures and the class of normal torsion theories on a stable $\infty$-category $C$, induced by the following correspondence:

* On the one side, given a normal, bireflective factorization system $(E,M)$ on $C$ we define the two classes $(C_{\ge0}(\mathbb{F}), C_{\lt 0}(\mathbb{F}))$ of a $t$-structure $\mathfrak{t}(\mathbb{F})$ to be the torsion and torsionfree classes $(*\!/E, M/\!*)$  associated to the factorization $(E,M)$.

* On the other side, given a $t$-structure on $C$ we set
$$E(t)=\{f\in C^{\Delta[1]} \mid \tau_{\lt 0}(f) \;\text{ is an equivalence}\};$$
$$
  M(t)=\{f\in C^{\Delta[1]} \mid \tau_{\geq0}(f) \;\text{ is an equivalence}\}.
$$

\end{proposition}

This is [FL16, Theorem 3.13](#FL16)

\begin{proposition}
There is a natural monotone action of the group $\mathbb{Z}$ of integers on the class $TS( C )$ (now confused with the class $FS_\nu( C )$ of normal torsion theories on $C$) given by the suspension functor: $\mathbb{F}=(E,M)$ goes to $\mathbb{F}[1] = (E[1], M[1])$. 
\end{proposition}

This correspondence leads to study _families_ of $t$-structures $\{\mathbb{F}_i\}_{i\in I}$; more precisely, we are led to study _$\mathbb{Z}$-equivariant_ [[k-ary factorization system|multiple factorization systems]] $J\to TS( C )$.

\begin{proposition}
\label{StableTStructure}
Let $\mathfrak{t} \in TS(C)$ and $\mathbb{F}=(E,M)$ correspond each other under the above bijection (Prop. \ref{CorrespondenceWithNormalTorsionTheories}); then the following conditions are equivalent:

1. $\mathfrak{t}[1]=\mathfrak{t}$, i.e. $C_{\geq 1}= C_{\geq 0}$;

2. $C_{\geq 0}=*\!/E$ is a stable $\infty$-category;

3. the class $E$ is closed under pullback.

\end{proposition}

In each of these cases, we say that $\mathfrak{t}$ or $(E,M)$ is _stable_.

This is [FLM19, Theorem 6.3](#FLM19)

This results allows us to recognize _$t$-structures with stable classes_ precisely as those which are fixed in the natural $\mathbb{Z}$-action on $TS( C )$.

Two "extremal" choices of $\mathbb{Z}$-chains of $t$-structures draw a connection between two apparently separated constructions in the theory of derived categories: _Harder-Narashiman filtrations_ and _semiorthogonal decompositions_ on triangulated categories: we adopt the shorthand $\mathfrak{t}_{1,\dots, n}$ to denote the tuple $\mathfrak{t}_1\preceq \mathfrak{t}_2\preceq\cdots\preceq \mathfrak{t}_n$, each of the $\mathfrak{t}_i$ being a $t$-structure $((C_i)_{\ge 0}, (C_i)_{\lt 0})$ on $C$, and we denote similarly $\mathfrak{t}_\omega$. Then

* In the _stable case_ the tuple $t_{1,\dots, n}$ is endowed with a (monotone) $\mathbb{Z}$-action, and the map $\{0\lt 1\cdots\lt n\}\to TS( C )$ is equivariant with respect to this action; the absence of nontrivial $\mathbb{Z}$-actions on $\{0\lt 1\cdots\lt n\}$ forces each $t_i$ to be stable.
* In the _orbit case_ we consider an _infinite_ family $t_\omega$ of $t$-structures on $C$, obtained as the orbit of a fixed $(E_0, M_0)\in TS( C )$ with respect to the natural $\mathbb{Z}$-action.


### Towers

The HN-filtration induced by a $t$-structure and the factorization induced by a [[semiorthogonal decomposition]] on $C$ both are the byproduct of the _tower_ associated to a tuple $\mathfrak{t}_{1,\dots, n}$:


## Examples
 {#Examples}

The archetypical and historically motivating example (cf. [Gelfand & Manin (1996), IV.4 §1](#GelfandManin96)) is the following:

\begin{example}
\label{TStructureOnDerivedCategoryOfAbelianCategory}
**(canonical t-structure on the [[derived category]] of an [[abelian category]])**
\linebreak
  For $\mathcal{A}$ an [[abelian category]], its unbounded [[derived category]] $\mathcal{D}_\bullet(\mathcal{A})$

1. carries a t-structure (Def. \ref{tStructure}) for which $\mathcal{D}(\mathcal{A})_{\geq n}$ (rep. $\mathcal{D}(\mathcal{A})_{\leq n}$) is the [[full subcategory]] of [[objects]] presented by [[chain complexes]] $V_\bullet$ whose [[chain homology]]-[[homology groups|groups]] are [[trivial group|trivial]] in degrees $\lt n$ (resp. $\gt n$);

1. whose heart (Def. \ref{HeartOfATStructure}) is [[equivalence of categories|equivalent]] to $\mathcal{A}$ (embedded as the [[chain complexes]] which are concentrated in degree 0).

\end{example}

(eg. [Gelfand & Manin (1996), IV.4 §3](#GelfandManin96))

\begin{example}
\label{CanonicalTStructureOnSpectra}
**(canonical t-structure on spectra)**
\linebreak
The [[stable (infinity,1)-category of spectra]], $Spectra$, carries a canonical t-structure for which 

* $Spectra_{\geq 0}$ is the sub-category of [[connective spectra]], with $\tau_{\geq 0} \colon Spectra \to Spectra_{\geq 0}$ the [[connective cover]]-construction.

* ...

\end{example}

(e.g. [Lurie, Higher Algebr, pp. 150](#LurieHA))

## Related concepts

* [[Bridgeland stability]]

* [[n-connective object]]

* [[connective cover]]

* [[theorem of the heart]]

## References

For [[triangulated categories]]:

the notion is due to 

* {#BeilinsonBernsteinDeligne82} [[Alexander Beilinson]], [[Joseph Bernstein]], [[Pierre Deligne]], *Faisceaux pervers*, Astérisque **100** (1982) &lbrack;[ISBN:978-2-85629-878-7](https://smf.emath.fr/publications/faisceaux-pervers), [pdf](https://publications.ias.edu/sites/default/files/Faisceaux%20pervers.pdf), [MR86g:32015](http://www.ams.org/mathscinet-getitem?mr=751966)&rbrack;

  > (otherwise introducing [[perverse sheaves]])

Further development:

* {#GelfandManin96} [[Sergei Gelfand]], [[Yuri Manin]], Section IV.4  of: *[[Methods of homological algebra]]*,  transl. from the 1988 Russian (Nauka Publ.) original, Springer (1996, 2002) &lbrack;[doi:10.1007/978-3-662-12492-5](https://doi.org/10.1007/978-3-662-12492-5)&rbrack;

* [[Donu Arapura]], _Triangulated categories and $t$-structures_ &lbrack;[pdf](http://www.math.purdue.edu/~dvb/preprints/perv2.pdf)&rbrack;

 
* [[Dan Abramovich]], [[Alexander Polishchuk]], *Sheaves of t-structures and valuative criteria for stable complexes*, J. reine angew. Math. **590** (2006) 89-130 &lbrack;[arXiv:math/0309435](https://arxiv.org/abs/math/0309435), [doi:10.1515/CRELLE.2006.005](https://doi.org/10.1515/CRELLE.2006.005)&rbrack;

* A. L. Gorodentsev, S. A. Kuleshov, A. N. Rudakov, _t-stabilities and t-structures on triangulated categories_, Izv. Ross. Akad. Nauk Ser. Mat. __68__ (2004), no. 4, 117-150

* [[Alexander Polishchuk]], *Constant families of t-structures on derived categories of coherent sheaves*, Moscow Math. J. __7__ (2007) 109-134 &lbrack;[arXiv:math/0606013](https://arxiv.org/abs/math/0606013)&rbrack;

* John Collins, [[Alexander Polishchuk]], _Gluing stability conditions_ &lbrack;[arxiv/0902.0323](http://arxiv.org/abs/0902.0323)&rbrack;


For [[stable (∞,1)-categories]]:

* {#LurieHA} [[Jacob Lurie]], Section 1.2.1 in: *[[Higher Algebra]]*


On [[reflective factorization systems]]:

* {#CHK85} C. Cassidy, M. Hébert, [[Max Kelly]], _Reflective subcategories, localizations, and factorization systems_,  J. Austral. Math Soc. (Series A) **38** (1985) 287-329 &lbrack;[doi:10.1017/S1446788700023624](https://doi.org/10.1017/S1446788700023624)&rbrack;
 
* {#RosickyTholen08} [[Jiri Rosicky]], [[Walter Tholen]], _Factorization, Fibration and Torsion_, Journal of Homotopy and Related Structures, Vol. 2(2007), No. 2, pp. 295-314  &lbrack;[arXiv:0801.0063](http://arxiv.org/abs/0801.0063), [publisher](http://www.emis.de/journals/JHRS/volumes/2007/n2a14/)&rbrack;

and on normal torsion theories in stable $\infty$-categories:

* {#FL16} [[Domenico Fiorenza]], [[Fosco Loregian]], *$t$-Structures are normal torsion theories*, Appl Categor Struct **24** (2016) 181–208 &lbrack;[arxiv:1408.7003](http://arxiv.org/abs/1408.7003), [doi:10.1007/s10485-015-9393-z](https://doi.org/10.1007/s10485-015-9393-z)&rbrack; 

* {#FLM19} [[Domenico Fiorenza]], [[Fosco Loregian]], [[Giovanni Marchetti]], *Hearts and towers in stable $\infty$-categories*,  J. Homotopy Relat. Struct. **14**  (2019) 993–1042 &lbrack;[arXiv:1501.04658](https://arxiv.org/abs/1501.04658), [doi:10.1007/s40062-019-00237-0](https://doi.org/10.1007/s40062-019-00237-0)&rbrack;

* [[Fosco Loregian]], [[Simone Virili]] *Triangulated factorization systems and t-structures*, Journal of Algebra **550** (2020) 219-241 &lbrack;[doi:10.1016/j.jalgebra.2019.12.021](https://doi.org/10.1016/j.jalgebra.2019.12.021)&rbrack;


[[!redirects t-structures]]

[[!redirects t-structure on a stable (∞,1)-category]]
[[!redirects t-structures on a stable (∞,1)-category]]

[[!redirects t-structure on a stable (infinity,1)-category]]
[[!redirects t-structures on a stable (infinity,1)-category]]


[[!redirects heart]]
[[!redirects hearts]]


[[!redirects heart of a t-structure]]
[[!redirects hearts of t-structures]]

[[!redirects heart of a stable (∞,1)-category]]
[[!redirects hearts of stable (∞,1)-categories]]

[[!redirects heart of a stable (infinity,1)-category]]
[[!redirects hearts of stable (infinity,1)-categories]]
