
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The __recollement__ situation is a [[diagram]] of six [[additive functors]] 

$$
  \mathcal{A}' 
    \stackrel{\overset{i^*}{\longleftarrow}}{\stackrel{\overset{i_*}{\longrightarrow}}{\underset{i^!}{\longleftarrow}}}
  \mathcal{A}\stackrel{\overset{j_!}{\longleftarrow}}{\stackrel{\overset{j^*}{\longrightarrow}}{\underset{j_*}{\longleftarrow}}}\mathcal{A}''
$$

among three [[abelian category|abelian]] or [[triangulated categories]] satisfying a strong list of [[exact functor|exactness]] and [[adjoint functor|adjointness]] axioms. 

The paradigmatic situation is about the categories of [[abelian sheaves]] $\mathcal{A}' = Sh(C)$, $\mathcal{A} = Sh(X)$, $\mathcal{A}'' = Sh(U)$, where $U\subset X$ is an [[open subset]] of a [[topological space]], $C = X\backslash U$ the [[complement]], and the functors among the [[category of sheaves|sheaf categories]] are induced by the [[open embedding]] $j \colon U\hookrightarrow X$ and [[closed embedding]] $i \colon C\hookrightarrow X$. As suggested by this example, recollement may in fact be regarded as the additive or triangulated version of [[Artin gluing]]. 

## Definition

A modern treatment for the recollement of abelian categories is in ([Franjou-Pirashvili 04](#FranjouPirashvili04)), where the following axioms are listed:

(i) $j_!\dashv j^*\dashv j_*$ 

(ii) the [[unit of an adjunction|unit]] $Id_{\mathcal{A}''}\to j^* j_!$ and the [[counit of an adjunction|counit]] $j^* j_*\to Id_{\mathcal{A}''}$ are [[isomorphism|iso]] ([hence](adjoint%20functor#FullyFaithfulAndInvertibleAdjoints) $j_\ast$ and $j_!$ are [[fully faithful functor|fully faithful]])

(iii) $i^*\dashv i_*\dashv i^!$

(iv) the unit $Id_{\mathcal{A}'}\to i^! i_*$ and the counit $i^* i_*\to Id_{\mathcal{A}'}$ are iso

(v) the functor $i_*:\mathcal{A}'\to Ker(j^*)$ is an equivalence of categories.

In fact (i) and (ii) for $j^*:\mathcal{A}\to\mathcal{A}''$ enable one to define $\mathcal{A}'$ as the full subcategory of $\mathcal{A}$ whose objects $a$ satisfy $j^* a = 0$ such that one satisfies the recollement situation. 

A standard treatment for the sequence of triangulated functors
$$
  \mathcal{D}' 
   \overset{i_*}{\to}
  \mathcal{D}\overset{j^*}{\to}\mathcal{D}''
$$

is in ([Beilinson-Bernstein-Deligne 82](#BeilinsonBernsteinDeligne82)) where in 1.4.3 the following axioms are listed 

(a) $i_* = i_!$ admits a triangulated left adjoint $i^*$ and triangulated right adjoint $i^!$

(b) $j^* = j^!$ admits a triangulated left adjoint $j_!$ and triangulated right adjoint $j_*$

(c) $j^* i_* = 0$ (hence by adjointness, also $i^*j_! = 0$ and $i^! j_*=0$)

(d) given $d\in Ob{\mathcal{D}}$, there exist (necessarily unique) distinguished triangles

$$
i_! i^! d \to d\to j_* j^* d\to (i_! i^! d) [1]
$$
$$
j_! j^! d \to d\to i_* i^* d\to (j_! j^! d) [1]
$$

(e) $i_*, j_*, j_!$ are full embeddings.

Again in good situations, less data is needed to provide the recollement. 

## Examples

* The prototypical example of recollement is provided by a closed-open decomposition. In this setup (which works equally well for locally compact Hausdorff spaces and schemes) there is the following diagram of inclusions.

$$
\begin{array}{ccccc}
Z & \xhookrightarrow{i} & X & \xhookleftarrow{j} & U \\
\end{array}
$$

Here $i$ is a _closed_ inclusion and $j$ is an _open_ inclusion. Then the categories of sheaves on $X,Z$ and $U$ fit into the recollement structure described above. The recollement structure on the category of sheaves on $X$ enables one to argue inductively about sheaves on $X.$ This idea is usually referred to as [[Noetherian induction]]. This technique allows to deduce results about higher dimensional schemes from information about lower dimensional schemes and analysis of locally standard schemes (e.g. smooth schemes for étale topology). See [Achar Exercise 1.3.4, Lemma 2.2.1](#Achar2021).

* The [[forgetful functor]] from [[global equivariant stable homotopy theory]] to plain [[stable homotopy theory]] exhibits a recollement,

See at _[global equivariant stable homotopy theory -- Relation to plain stable homotopy theory](global+equivariant+stable+homotopy+theory#RelationToPlainStableHomotopyTheory)_.

## Related concepts

* [[adjoint modality]]

## References

* {#FranjouPirashvili04} V. Franjou, [[T. Pirashvili]], _Comparison of abelian categories recollements_, Doc. Math. 9 (2004), 41&#8211;56, [MR2005c:18008](http://www.ams.org/mathscinet-getitem?mr=2054979), [pdf](http://www.math.uni-bielefeld.de/documenta/vol-09/03.pdf)

* {#BeilinsonBernsteinDeligne82} A.A. Beilinson, J. Bernstein, [[Pierre Deligne]], _Faisceaux pervers. Analysis and topology on singular spaces_, I (Luminy, 1981), 5&#8211;171, Aste'risque 100, Soc. Math. France, Paris 1982.

* {#Achar2021} P. Achar. _Perverse Sheaves and Applications to Representation Theory._ Vol. 258. Mathematical Surveys and Monographs. Providence, Rhode Island: American Mathematical Society, 2021. [doi:10.1090/surv/258](https://doi.org/10.1090/surv/258).


In references

* E. Cline, B. Parshall, L. Scott, _Finite dimensional algebras and highest weight categories_, J. Reine Angew. Math, 1988, 391: 85&#8212;99, [MR90d:18005](http://www.ams.org/mathscinet-getitem?mr=961165), [goettingen](http://resolver.sub.uni-goettingen.de/purl?GDZPPN002205971)
* E. Cline, B. Parshall, L. Scott, _Algebraic stratification in representative categories_, J. of Algebra 117, 1988, 504&#8212;521.

one studies the following kind of sources of recollement situations for triangulated categories: $k$ is a commutative [[field]], $A$ a finite dimensional unital associative $k$-algebra, $e$ an idempotent, and $D^b(A)$ the bounded derived category of right $A$-modules. Suppose $eA(1-e) = 0$ and the global dimension of $A$ is finite. Then there is a recollement of triangulated categories involving $D^b(eAe)$, $D^b(A)$ and $D^b((1-e)A(1-e))$. 

* S. Koenig, _Tilting complexes, perpendicular categories and recollements of derived module categories of rings._, [MR92k:18009](http://www.ams.org/mathscinet-getitem?mr=1124785), <a href="http://dx.doi.org/10.1016/0022-4049(91)90029-2">doi</a>
* Qinghua Chen,Yanan Lin, _Recollements of extension algebras_, Science in China 46, 4, 2003 [pdf](http://www.springerlink.com/content/h185372128726855/fulltext.pdf)

Another source of examples is due MacPherson and Vilonen

* Kari Vilonen, _Perverse sheaves and finite dimensional algebras_, Trans.
A.M.S. 341 (1994), 665&#8211;676, [MR94d:16012](http://www.ams.org/mathscinet-getitem?mr=1135104), [doi](http://dx.doi.org/10.2307/2154577)

* Michael Artin, Grothendieck Topologies. Harvard University, 1962. 
* Yuri Berest, Oleg Chalykh, Farkhod Eshmatov, _Recollement of deformed preprojective algebras and the Calogero-Moser correspondence_, Mosc. Math. J. 8 (2008), no. 1, 21&#8211;37, 183, [arxiv/0706.3006](http://arxiv.org/abs/0706.3006), [MR2009h:16030](http://www.ams.org/mathscinet-getitem?mr=2422265)
* Roy Joshua, [pdf](http://www.math.osu.edu/~joshua.1/GV.pdf)
* Yang Han, _Recollements and Hochschild theory_, [arxiv/1101.5697](http://arxiv.org/abs/1101.5697)

For treatment in the setting of $\infty$-categories:

* [[Jacob Lurie]], section A.8 of _[[Higher Algebra]]_, 

* [[Clark Barwick]], [[Saul Glasman]], _A note on stable recollements_ ([arXiv:1607.02064](https://arxiv.org/abs/1607.02064))
