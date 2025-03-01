
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
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

The _derived (infinity,1)-category_ or _derived category_ of an [[abelian category]] $\mathcal{A}$ is the setting for [[homological algebra]] in $\mathcal{A}$: the [[(infinity,1)-categorical localization]] of the [[category of chain complexes]] in $\mathcal{A}$ at the class of [[quasi-isomorphisms]]. The derived category is a fundamental example of a [[stable (infinity,1)-category]]. In the case that $\mathcal{A} \simeq$ [[Mod|$R Mod$]] (cf. the [[Freyd-Mitchell embedding theorem]]), the [[stable Dold-Kan correspondence]] says that the derived $\infty$-category of $\mathcal{A}$ is equivalently the [[stable (infinity,1)-category of spectra|stable $\infty$-category of]] [[Eilenberg-MacLane spectrum|$H R$]]-[[module spectra]].

The derived $\infty$-category is presented by various [[dg-model structures]] on the [[category of chain complexes]], as described at [[model structures on chain complexes]]. As such it has also a natural incarnation as a [[pretriangulated dg-category]], which might be called the _derived dg-category_.

Like any [[stable (infinity,1)-category]], the [[homotopy category of an (infinity,1)-category|homotopy category]] of the derived (infinity,1)-category admits a canonical [[triangulated category]] structure. Often in the literature, the term _derived category_ refers to the [[homotopy category of an (infinity,1)-category|homotopy category]], viewed only as a [[triangulated category]]. The loss of information can often be problematic, but for many purposes is not important.

In what follows, we will describe only the homotopy category. See [[(infinity,1)-category of chain complexes]] for the full [[(infinity,1)-category]].

Associated to $\mathcal{A}$ is

* the [[category of chain complexes]] $Ch_\bullet(\mathcal{A})$ in $\mathcal{A}$ which is naturally a [[homotopical category]];

* the "[[homotopy category of chain complexes]]" $K(\mathcal{A})$;

* the [[stable ∞-category]] $K_\infty(\mathcal{A})$ of [[chain complexes]] in $C$.

The  _derived category_ $D(C)$ of $\mathcal{A}$ is equivalently

* the [[homotopy category|1-categorical homotopy category]] of $Ch_\bullet(\mathcal{A})$ with respect to the [[quasi-isomorphisms]];

* the [[homotopy category of an (infinity,1)-category|(∞,1)-categorical homotopy category]] of $K_\infty(\mathcal{A})$.

In either case, this means that under the canonical [[localization]] functor

$$
  Q : Ch_\bullet(\mathcal{A}) \to D(\mathcal{A})
$$

the [[quasi-isomorphisms]] of [[chain complexes]] become true [[isomorphisms]]
and that $D(\mathcal{A})$ is [[universal property|universal]] with respect to this property.

Hence the derived category is an approximation to the full [[simplicial localization]] of $K(\mathcal{A})$. It is or can be equipped with several further [[properties]] and [[structure]] that give a more accurate approximation. Notably every derived category is a _[[triangulated category]]_, which is a way of remembering the [[suspension]] and de-suspension operations on its objects -- the [[suspension of chain complexes]] -- hence its "[[stable (infinity,1)-category|stability]]".

## History

Derived categories were introduced by [[Jean-Louis Verdier]] in his thesis under the supervision of [[Alexandre Grothendieck]].  It was originally used to extend [[Serre duality]] to a relative context.  See [[Robin Hartshorne|Hartshorne]]'s lecture notes "Residues and duality".

## Definition 

Let $\mathcal{A}$ be an [[abelian category]] and $K(\mathcal{A})$ its 
[[category of chain complexes]] modulo [[chain homotopy]] (the "[[homotopy category of chain complexes]]"). 

Equip $K(\mathcal{A})$ with the structure of a [[homotopical category]]
by declaring the [[weak equivalences]] to be the
**quasi-isomorphisms**: those morphisms
$f : V \to W$
which induce [[isomorphisms]] in [[homology]], 
$H(f) : H(V) \stackrel{\simeq}{\to} H(W)$. 

+-- {: .num_defn}
###### Definition

The **derived category** $D(\mathcal{A})$ is the [[homotopy category]] of
$K(\mathcal{A})$ with respect to these weak equivalences.

=--

Analogously, for $K^{+,-,b}(\mathcal{A})$ denoting the [[full subcategory]] on the chain complexes bounded above, bounded below, or bounded, respectively (see at _[[category of chain complexes]]_), one writes

$$
  D^{+,-,b}(\mathcal{A}) \hookrightarrow D(\mathcal{A})
$$

for the correspponding full subcategory of the derived category.


## Equivalent characterizations and constructions
 {#Properties}

There are various ways to construct or express the derived category more explicitly in terms of various special objects or morphisms in the [[category of chain complexes]].

* _[In terms of localization at a null system](#AsLOcalizationAtNullSystem)_

* _[In terms of resolutions](#InTermsOfResolutions)_.

### In terms of localization at a null system
 {#AsLOcalizationAtNullSystem}


The "[[homotopy category of chain complexes]]" $K(\mathcal{A})$ is already a [[triangulated category]].  The derived category can be obtained as the construction of a [[homotopy category]] of a [[triangulated category]] with respect to a [[null system]].

+-- {: .num_defn}
###### Definition

Let 

$$
  N(\mathcal{A}) \subset K(\mathcal{A})
$$ 

and analogously

$$
  N^{+,-n,b}(\mathcal{A}) \subset K^{+,-,b}(\mathcal{A})
$$ 


be the [[full subcategory]] of $K(C)$ or on $K^{+,-,b}$, respectively, on those [[chain complexes]] $V$ whose  [[chain homology]] vanishes in every degree, $H_\bullet(V) = 0$. 

=--

+-- {: .num_prop}
###### Proposition


A [[chain map]] $f_\bullet : V_\bullet \to W_\bullet$ is a 
[[quasi-isomorphism]] precisely there exists a [[distinguished triangle]] in $K(\mathcal{A})$ of the form

$$
  V \stackrel{f}{\to} W \to cone(f)
$$

with the [[mapping cone]] $cone(f) \in N(\mathcal{C})$.

=--

+-- {: .num_prop}
###### Proposition

The derived category is equivalently the localization of $K(\mathcal{A})$ at the [[null system]] $N(\mathcal{A})$.

$$
  D(\mathcal{A}) \simeq K(\mathcal{A})/N(\mathcal{A})
  \,.
$$

=--

This perspective is discussed in ([Kashiwara-Schapira, section 13](#KashiwaraSchapira)) and ([Schapira, section 6.2, 72](#Schapira)).

### In terms of injective and projective resolutions
 {#InTermsOfResolutions}

In the case that the underlying [[abelian category]] $\mathcal{A}$ has [enough injectives](injective%20object#EnoughInjectives) or [enough projectives](projective%20object#EnoughInjectives), the [[hom sets]] in the derived category may equivalently be obtained as [[homotopy]]-classes of [[chain maps]] from [[projective resolutions]] to [[injective resolutions]] of chain complexes. 

In view of the existence of the injective and projective [[model structure on chain complexes]] this is a special case of the general fact that [[homotopy categories]] of [[model categories]] may be obtained by forming homotopy classes of maps in the model category from  [[cofibrant resolutions]] to [[fibrant resolutions]]. For more details on the model-category point of view, see e.g. Appendix C of [Toën, Vaquié](#TV2007). But here we spell out an direct discussion of this fact for chain complexes.


+-- {: .num_defn}
###### Definition

Write $K^+(\mathcal{I}_{\mathcal{A}}) \hookrightarrow K^+(\mathcal{A})$
for the [[full subcategory]] of the [[homotopy category of chain complexes]] bounded above on those that are degreewise [[injective objects]].

Dually, let $K^-(\mathcal{P}_{\mathcal{A}}) \hookrightarrow K^-(\mathcal{A})$
for the [[full subcategory]] of the [[homotopy category of chain complexes]] bounded below on those that are degreewise [[projective objects]].

=--

+-- {: .num_theorem}
###### Theorem

If $\mathcal{A}$ has [enough injectives](http://ncatlab.org/nlab/show/injective%20object#EnoughInjectives) then the canonical functor

$$
  K^+(\mathcal{I}_{\mathcal{A}}) \to D^+(\mathcal{A})
$$

is an [[equivalence of categories]].

Dually, if $\mathcal{A}$ has [enough projectives](http://ncatlab.org/nlab/show/projective%20object#EnoughProjectives) then the canonical functor

$$
  K^-(\mathcal{P}_{\mathcal{A}}) \to D^-(\mathcal{A})
$$

is an [[equivalence of categories]].

=--

For instance ([Schapira, cor. 7.2.3](#Schapira)).


## Related concepts

* [[derived functor]]
* [[triangulated categories]]

## References 

The original reference:

* [[Verdier, Jean-Louis]], _Des Catégories Dérivées des Catégories Abéliennes_, Astérisque **239** (1996) &lbrack;[doi:10.24033/ast.364](https://smf.emath.fr/publications/des-categories-derivees-des-categories-abeliennes), [numdam:AST_1996__239__R1_0](http://www.numdam.org/issues/AST_1996__239__R1_0), [pdf](http://www.numdam.org/item/AST_1996__239__R1_0.pdf)&rbrack;

* {#GelfandManin96} [[Sergei Gelfand]], [[Yuri Manin]], Section III of: *[[Methods of homological algebra]]*,  transl. from the 1988 Russian (Nauka Publ.) original, Springer (1996, 2002) &lbrack;[doi:10.1007/978-3-662-12492-5](https://doi.org/10.1007/978-3-662-12492-5)&rbrack;


Systematic discussion from the point of view of [[localization]] and [[homotopy theory]]:

* {#KashiwaraSchapira} [[Masaki Kashiwara]], [[Pierre Schapira]], section 13 of  *[[Categories and Sheaves]]* (2006)
 

and, similarly, in section 7 of 

* [[Pierre Schapira]], _Categories and homological algebra_ (2011) ([pdf](http://people.math.jussieu.fr/~schapira/lectnotes/HomAl.pdf), [archive.org](https://archive.org/details/Pierre_Schapira___Categories_and_Homological_Algebra), [newer version(pdf)](https://perso.imj-prg.fr/pierre-schapira/wp-content/uploads/schapira-pub/lectnotes/HomAl.pdf))
 {#Schapira}

For the model-category version of this story for an arbitrary ringed site, including details about the tensor, internal hom, and $(-)_!$ and $(-)^*$, see Appendix C of

* {#TV2007} Bertrand Toën, Michel Vaquié, _Algebraization of complex analytic varieties and derived categories_ ([arXiv:math/0703555v1](https://arxiv.org/abs/math/0703555v1))

A detailed treatment of derived categories (including of DG modules over DG 
rings), with applications to noncommutative algebra, is in the book 

* [[Amnon Yekutieli]], *Derived Categories*, Cambridge University Press (2019) &lbrack;[doi:10.1017/9781108292825]( https://doi.org/10.1017/9781108292825), [arXiv:1610.09640](https://arxiv.org/abs/1610.09640)&rbrack;


A pedagogical introduction:

* R. P. Thomas, _Derived categories for the working mathematician_ ([arXiv:math.AG/0001045](http://arxiv.org/abs/math.AG/0001045))

A good survey of the more general topic of derived categories is 

* [[Bernhard Keller]], _Derived categories and their uses_ ([ps](http://www.google.de/url?sa=t&source=web&ct=res&cd=6&ved=0CC8QFjAF&url=http%3A%2F%2Fwww.math.jussieu.fr%2F~keller%2Fpubl%2Fdcu.ps&rct=j&q=derived+category&ei=Ib76SsSdAsjb-QaAw7moDw&usg=AFQjCNGIgXLHlprAoR70bGLWQmyKGHDjTQ))

See in particular also the list of references given there.

Other lecture notes include

* Theo B&#252;hler, _An introduction to the derived category_ ([pdf](https://ncatlab.org/nlab/files/intro-derived.PDF)).

and for applications to [[coherent sheaves]],

* [[Franco Rota]], _An introduction to the derived category of coherent sheaves_ ([pdf](https://drive.google.com/file/d/12fhshN_lFOi54pjBdjVEPzUb1XBxz-TW/view))

For a discussion in the context of [[(∞,1)-category|(∞,1)-categories]] and in particular [[stable (∞,1)-category|stable (∞,1)-categories]] see [section 13, p. 53](http://www.math.harvard.edu/~lurie/papers/DAG-I.pdf#page=53) of

* [[Jacob Lurie]], _[[Stable ∞-Categories]]_

On applications of derived categories in [[algebraic geometry]]:

* [[Dmitri Orlov]], _Derived categories of coherent sheaves and equivalences between them_, Uspekhi Mat. Nauk, 2003, Vol. 58, issue 3(351), pp. 89&#8211;172, [English translation (PDF)](http://www.mi.ras.ru/~orlov/papers/Uspekhi2003.pdf)

* [[Aleksei Bondal]], [[Dmitri Orlov]], _[Reconstruction of a variety from the derived category and groups of autoequivalences](http://www.mi.ras.ru/~orlov/papers/Compositio2001.pdf)_, Compositio Mathematica 125 (03), 327-344.  See also [[Bondal-Orlov reconstruction theorem]].

* [[Daniel Huybrechts]], _Fourier-Mukai Transforms in Algebraic Geometry_, Oxford University Press, USA, 2006.

* [[Igor Dolgachev]], [_Derived categories_](http://www.math.lsa.umich.edu/~idolga/derived9.pdf).

* Andrei Caldararu, _Derived categories of coherent sheaves: a skimming_.  Lecture notes from _Algebraic Geometry: Presentations by Young Researchers_ in Snowbird, Utah, July 2004 &lbrack;[arXiv:math/0501094](http://arxiv.org/abs/math/0501094)&rbrack;

On the [[algebraic K-theory]] of rings being encoded in the respective derived categories:

* {#DuggerShipley04} [[Daniel Dugger]], [[Brooke Shipley]], *K-theory and derived equivalences*,  Duke Math. J. **124** 3 (2004) 587-617 &lbrack;[arXiv:math/0209084](https://arxiv.org/abs/math/0209084), [doi:10.1215/S0012-7094-04-12435-2](https://projecteuclid.org/journals/duke-mathematical-journal/volume-124/issue-3/K-theory-and-derived-equivalences/10.1215/S0012-7094-04-12435-2.short)&rbrack;




[[!redirects derived categories]]
[[!redirects bounded derived category]]
[[!redirects bounded derived categories]]

[[!redirects derived (infinity,1)-category]]
[[!redirects derived (infinity,1)-categories]]
[[!redirects derived (∞,1)-category]]
[[!redirects derived (∞,1)-categories]]
[[!redirects derived dg-category]]
[[!redirects derived dg-categories]]