
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of [[cohomology]] finds its natural general formulation in terms of [[hom-spaces]] in an [[(∞,1)-topos]], as described at [[cohomology]]. Many of the cohomologies which have been traditionally considered, such as [[abelian sheaf cohomology|sheaf cohomology]], turn out to be just a special case of the general situation, for objects which are sufficiently abelian in the sense of [[stable (infinity,1)-category|stable (∞,1)-categories]].

Therefore to amplify that one is looking at general [[cohomology]] without restricting to [[abelian sheaf cohomology|abelian cohomology]] one sometimes speaks of  **nonabelian cohomology**. 

## History

It was originally apparently John Roberts who understood (remarkably: while thinking about [[quantum field theory]] in the guise of [[AQFT]]) that general cohomology is about coloring simplices in $\infty$-categories.  

* John E. Roberts, _Mathematical Aspects of Local Cohomology_
talk at Colloqium on Operator Algebras and their Applications to Mathematical Physics, Marseille 20-24 June, 1977 .

This is recounted for instance by Ross Street in

* [[Ross Street]], _Categorical and combinatorial aspects of descent theory_ ([pdf](http://arxiv.org/ftp/math/papers/0303/0303175.pdf))

and 

* [[Ross Street]], _An australian conspectus on higher categories_ ([pdf](http://www.math.mq.edu.au/~street/Minneapolis.pdf)).

Parallel to this development of the notion of [[descent|descent and codescent]] there was the development of [[homotopical cohomology theory]] as described in

* Kenneth S. Brown, _Abstract Homotopy Theory and Generalized Sheaf Cohomology_, Transactions of the American Mathematical Society, Vol. 186 (1973), 419-458 ([pdf](http://www.math.uni-hamburg.de/home/schreiber/Abstract%20homotopy%20theory%20and%20generalized%20sheaf%20cohomology.pdf))

The two approaches are different, but closely related. Their relation is via the notion of [[descent|codescent]].

There is a chain of inclusions

$$
  AbelianGroups \hookrightarrow
  ChainComplexesOfAbelianGroups
  \hookrightarrow
  CrossedComplexes
  \hookrightarrow
  \omega Groupoids
  \hookrightarrow
  \omega Categories
$$

along which one can generalize the coefficient objects of ordinary cohomology. (See [[strict omega-groupoid]], [[strict omega-category]]). Since doing so in particular generalizes abelian groups to nonabelian groups (but goes much further!) this is generally addressed as leading to _nonabelian cohomology_.

Depending on the [[model category|models]] chosen, there are different concrete realizations of nonabelian cohomology. 

For instance nonabelian [[Čech cohomology]] played a special role in the motivation of the notion of [[gerbe]]s (see in particular [[gerbe (in nonabelian cohomology)]]), concretely thought of in terms of [[pseudofunctor]]s at least in the context of nonabelian [[group cohomology]], while more abstract (and less explicit) [[homotopy theory]] methods dominate the discussion of [[infinity-stack]]s.

Either way, one obtains a notion of _cohomology on $\infty$-categories with coefficients in $\infty$-catgories_. This is, most generally, the setup of "[[nonabelian cohomology]]".

This is conceptually best understood today in terms of [[Higher Topos Theory|higher topos theory]], using [[(infinity,1)-category of (infinity,1)-sheaves|(infinity,1)-categories of (infinity,1)-sheaves]]. 

This perspective on nonabelian cohomology is discussed for instance in [Toen 02](#Toen02)


## Properties

### Postnikov decomposition and Whitehead principle

In an [[(∞,1)-topos]] every object has a [[Postnikov tower in an (∞,1)-category]]. This means that in some sense general nonabelian cohomology can be decomposed into nonabelian cohomology in degree 1 and abelian cohomology in higher degrees, twisted by this nonabelian cohomology. This has been called ([To&#235;n](#Toen02)) the [[Whitehead principle of nonabelian cohomology]].

## Special cases

### Nonabelian group cohomology

Sometimes the term _nonabelian cohomology_ is used in a more restrictive sense. Often people mean 
[[nonabelian group cohomology]] when they say nonabelian cohomology, hence restricting to the domains to [[group|groups]], which are [[groupoid|groupoids]] with a single object.

This kind of nonabelian cohomology is discussed for instance in

* [[John Baez]], [[Mike Shulman]], [[Lectures on n-Categories and Cohomology]] ([arXiv](http://arxiv.org/abs/math.CT/0608420)).

That and how ordinary [[group cohomology]] is reproduced from the [[homotopical cohomology theory]] of [[strict omega-groupoid|strict omega-groupoids]] is discussed in detail in chapter 12 of 

* [[Ronnie Brown]], P. Higgins, R. Sivera, [[nonabelian algebraic topology|Nonabelian algebraic topology]].

For more see

* [[nonabelian group cohomology]].



### Nonabelian sheaf cohomology with constant coefficients {#NonabelianSheafCohomology}

For $X$ a [[topological space]] and $A$ an [[∞-groupoid]], the standard way to define the [[nonabelian cohomology]] of $X$ with coefficients in $A$ is to define it as the intrinsic cohomology as seen in [[∞Grpd]] $\simeq$ [[Top]]:

$$
  H(X,A) := \pi_0 Top(X, |A|) \simeq \pi_0 \infty Func(Sing X, A)
  \,,
$$

where $|A|$ is the [[geometric realization]] of $A$ and $Sing X$ the [[fundamental ∞-groupoid]] of $X$.

But both $X$ and $A$ here naturally can be regarded, in several ways, as objects of [[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaf (∞,1)-topos]]es $\mathbf{H} = Sh_{(\infty,1)}(C)$ over nontrivial [[(∞,1)-site]]s $C$. The intrinsic cohomology of such $\mathbf{H}$ is a [[nonabelian cohomology|nonabelian sheaf cohomology]]. The following discusses two such choices for $\mathbf{H}$ such that the corresponding nonabelian sheaf cohomology coincides with $H(X,A)$ (for [[paracompact space|paracompact]] $X$).

#### Petit $(\infty,1)$-sheaf $(\infty,1)$-topos

For $X$ a [[topological space]] and $Op(X)$ its [[category of open subsets]] equipped with the canonical structure of an [[(∞,1)-site]], let 

$$
  \mathbf{H}
  :=
  Sh_{(\infty,1)}(X) := Sh_{(\infty,1)}(Op(X))
$$

be the [[(∞,1)-category of (∞,1)-sheaves]] on $X$. The space $X$ itself is naturally identified with the [[terminal object]] $X = * \in Sh_{(\infty,1)}(X)$. This is the [[petit topos]] incarnation of $X$.

Write

$$
  (LConst \dashv \Gamma) :  Sh_{(\infty,1)}(X)
  \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
$$

be the [[global section]]s terminal [[geometric morphism]]. 

Under the [[constant (∞,1)-sheaf]] functor $LConst$ an an [[∞-groupoid]] $A \in \infty Grpd$ is regarded as an object $LConst A \in Sh_{(\infty,1)}(X)$. 

There is therefore the _intrinsic_ [[cohomology]] of the $(\infty,1)$-topos $Sh_{(\infty,1)}(X)$ with coefficients in the [[constant ∞-stack|constant (∞,1)-sheaf]] on $A$
  
$$
  H'(X,A) := \pi_0 Sh_{(\infty,1)}(X)(X, LConst A)
  \,.
$$

This is [[cohomology with constant coefficients]].

Notice that since $X$ is in fact the [[terminal object]] of $Sh_{(\infty,1)}(X)$ and that $Sh_{(\infty,1)}(X)(X,-)$ is in fact that [[global section]]s functor, this is equivalently

$$
  \cdots \simeq \pi_0 \Gamma LConst A
  \,.
$$

+-- {: .un_theorem }
###### Theorem

If $X$ is a [[paracompact space]], then these two definitins of [[nonabelian cohomology]] of $X$ with [[constant ∞-stack|constant coefficients]] $A \in \infty Grpd$ agree:

$$
  H(X,A) := \pi_0 \infty Grpd(Sing X,A)  \simeq Sh_{(\infty,1)}(X)(X,LConst A)
  \,.
$$

=--

This is [[Higher Topos Theory|HTT, theorem 7.1.0.1]]. See also [[(∞,1)-category of (∞,1)-sheaves]] for more.


#### Gros $(\infty,1)$-sheaf $(\infty,1)$-topos

Another alternative is to regard the space $X$ as an object in the [[cohesive (∞,1)-topos]] [[ETop∞Grpd]]. 

$$
  (\Pi \dashv LConst \dashv \Gamma)
  :
  ETop\infty Grpd
  \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}}
  \infty Grpd
  \,,
$$

with the further [[left adjoint]] $\Pi$ to $LConst$ being the intrinsic [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] functor.  The intrinsic [[nonabelian cohomology]] in there also coincides with nonabelian cohomology in [[Top]]; even the full [[cocycle]] [[∞-groupoid]]s are equivalent:

+-- {: .un_theorem }
###### Theorem

For [[paracompact space|paracompact]] $X$ we have an equivalence of [[cocycle]] [[∞-groupoid]]s

$$
  ETop\infty Grpd(X, LConst A)
  \simeq
  Top(X, |A|)
$$

and hence in particular an isomorphism on cohomology

$$
  H(X,A) \simeq \pi_0   ETop\infty Grpd(X, LConst A)
$$

=--

+-- {: .proof}
###### Proof

See [[ETop∞Grpd]].

=--

## Examples

Examples of *generalized* nonabelian cohomology (with general classifying spaces):

* [[unstable topological K-theory]]

* [[Cohomotopy]]


## Objects classified by nonabelian cohomology

For $g : X \to A$ a [[cocycle]] in nonabelian cohomology, we say the [[fibration sequence|homotopy fibers]] of $g$ is the object _classified_ by $g$.

For examples and discussion of this see

* [[principal bundle]]

* [[principal 2-bundle]], [[gerbe]]

* [[principal 3-bundle]], [[2-gerbe]]

* [[principal ∞-bundle]], [[∞-gerbe]]

* [[twisted form|twisted forms]] .

## Related concepts

* [[nonabelian Poincaré duality]]

* [[nonabelian de Rham cohomology]]

* [[differential non-abelian cohomology]]

* [[generalized cohomology]]

* [[Chern-Weil theory]]

## References
 {#References}

### Classical theory -- bundles and groups

The classical notion of non-abelian ([[Čech cohomology|Čech]]-)cohomology in degree 1 and its relation to [[fiber bundles]]/[[principal bundles]]:


* [[Alexander Grothendieck]], Chapter V of: *A General Theory of Fibre Spaces With Structure Sheaf*, University of Kansas, Report No. 4 (1955, 1958) &lbrack;[pdf](https://webusers.imj-prg.fr/~leila.schneps/grothendieckcircle/Kansasnotes.pdf), [[Grothendieck-FibreSpaces.pdf:file]]&rbrack;

* [[Jean Frenkel]], *Cohomologie à valeurs dans un faisceau non abélien*, C. R. Acad. Se., t. 240 (1955) 2368-2370
 
* [[Jean Frenkel]], *Cohomologie non abélienne et espaces fibrés*, Bulletin de la Société Mathématique de France, **85** (1957) 135-220 &lbrack;[numdam:BSMF_1957__85__135_0](http://www.numdam.org/item/BSMF_1957__85__135_0)&rbrack;

Review:

* [[Torsten Wedhorn]], *Torsors and Non-abelian Čech Cohomology*, chapter 7 in: *Manifolds, Sheaves, and Cohomology*, Springer (2016) &lbrack;[doi:10.1007/978-3-658-10633-1](https://doi.org/10.1007/978-3-658-10633-1)&rbrack;

Review in topological spaces (via [[classifying spaces]]):

* Nicolas Addington, _Fiber bundles and nonabelian cohomology_ (2007) &lbrack;[pdf](http://pages.uoregon.edu/adding/notes/gstc2007.pdf)&rbrack;

* {#Mitchell11} [[Stephen Mitchell]], around Theorem 7.4 in: _Notes on principal bundles and classifying spaces_, Lecture Notes. University of Washington (2011) &lbrack;[pdf](https://sites.math.washington.edu/~mitchell/Notes/prin.pdf), [[MitchellPrincipalBundles.pdf:file]]&rbrack;

* {#RudolfSchmidt17} [[Gerd Rudolph]], [[Matthias Schmidt]], Thm. 3.5.1 of: *Differential Geometry and Mathematical Physics Part II. Fibre Bundles, Topology and Gauge Fields*, Springer (2017) &lbrack;[doi:10.1007/978-94-024-0959-8](https://link.springer.com/book/10.1007/978-94-024-0959-8)&rbrack;

See also:

*  Jinpeng An. Zhengdong Wang, _Nonabelian cohomology with coefficients in Lie groups_, Trans. Amer. Math. Soc. **360** (2008) 3019-3040 &lbrack;[doi:10.1090/S0002-9947-08-04278-5](https://doi.org/10.1090/S0002-9947-08-04278-5)&rbrack;


The case of [[nonabelian group cohomology]]:

* {#Milne17} [[James Milne]], Section 27.a (of the [pdf](https://www.jmilne.org/math/CourseNotes/iAG200.pdf), not present in the published version) of: *Algebraic Groups*, Cambridge University Press 2017  ([doi:10.1017/9781316711736](https://doi.org/10.1017/9781316711736), [webpage](http://www.jmilne.org/math/Books/iag.html), [pdf](https://www.jmilne.org/math/CourseNotes/iAG200.pdf))


### Categorified theory -- 2-bundles/gerbes 
 {#CategorifiedTheory}

Early discussion, of higher non-abelian cohomology with [[coefficients]] in certain [[2-groups]] (implicitly):

* [[Paul Dedecker]], *Cohomologie à coefficients non abéliens et espaces fibrés*,  Bulletins de l'Académie Royale de Belgique **41** (1955) 1132-1146 &lbrack;[persee:barb_0001-4141_1955_num_41_1_69497](https://www.persee.fr/doc/barb_0001-4141_1955_num_41_1_69497)&rbrack;

* [[Paul Dedecker]], *Cohomologie de dimension 2 à coefficients non abéliens*, C. R. Acad. Sci. Paris **247** (1958) 1160-1163 &lbrack;[BnF](https://gallica.bnf.fr/ark:/12148/bpt6k7258/f192.item.r=dedecker)&rbrack;

* [[Paul Dedecker]], *Sur La Cohomologie Non Abelienne I (Dimension Deux)*, Canadian Journal of Mathematics **12** (1960) 231-251 &lbrack;[doi:10.4153/CJM-1960-019-7](https://doi.org/10.4153/CJM-1960-019-7)&rbrack;

and with coefficients in certain [[3-groups]] presented by [[crossed squares]]:

* [[Paul Dedecker]], A. Frei, _Les relations d'&#233;quivalence des morphismes de la suite exacte de cohomologie non ab&#234;lienne_, C. R. Acad. Sci. Paris **262** (1966) 1298-1301

* [[Paul Dedecker]], _Three dimensional non-abelian cohomology for groups_, Category theory, homology theory and their applications, II (Battelle Institute Conf.) 1969 ([MathSciNet](http://www.ams.org/mathscinet/pdf/263894.pdf?pg1=IID&s1=55880&vfpref=html&r=15))


The correct definition using [[crossed modules]] of sheaves then appeared in 

* {#Debremaeker76} Raymond Debremaeker, _Cohomologie met waarden in een gekruiste groepenschoof op een situs_, PhD thesis, 1976 (Katholieke Universiteit te Leuven). English translation: 
_Cohomology with values in a sheaf of crossed groups over a site_, arXiv:[1702.02128](https://arxiv.org/abs/1702.02128)

Of [[algebra|algebraic]] [[structures]]:

*  [[René Lavendhomme]], J. R. Roisin, _Cohomologie non abélienne de structures algèbriques_, Journal of Algebra **67** 2 (1980) 385-414 &lbrack;<a href="https://doi.org/10.1016/0021-8693(80)90168-4">doi:10.1016/0021-8693(80)90168-4</a>&rbrack;


Discussion in terms of [[gerbes]]:

* [[Jean Giraud]], _Cohomologie non ab&#233;lienne_ , Springer  (1971) &lbrack;[doi:10.1007/978-3-662-62103-5](https://link.springer.com/book/10.1007/978-3-662-62103-5)&rbrack;

  > (aspects of classification of $G$-[[gerbes]] by cohomology with coefficients in the [[automorphism 2-group]] $AUT(G)$, but imposes extra constraints)


* [[Larry Breen]], _Bitorseurs et cohomologie non-Ab&#233;lienne_, The Grothendieck Festschrift: a collection of articles written in honour of the 60th birthday of Alexander Grothendieck, Vol. I, edited P.Cartier, et al., Birkh&#228;user, Boston, Basel, Berlin, 401-476, (1990) ([doi:10.1007/978-0-8176-4574-8_10](https://doi.org/10.1007/978-0-8176-4574-8_10))

* [[John Duskin]]: _Non-abelian cohomology in a topos_, reprinted as: Reprints in Theory and Applications of Categories **23** (2013) 1-165 &lbrack;[tac:tr23](http://www.tac.mta.ca/tac/reprints/articles/23/tr23abs.html)&rbrack;

* [[Ieke Moerdijk]]: _Lie Groupoids, Gerbes, and Non-Abelian Cohomology_, K-Theory **28** 3 (2003) 207-258 &lbrack;[journal](http://www.springerlink.com/content/ul554x3077444545/), [doi:10.1023/A:1026251115381](http://dx.doi.org/10.1023/A:1026251115381)&rbrack;

* [[Amnon Yekutieli]], *Combinatorial descent data for gerbes*, Journal of Noncommutative Geometry **8** 4 (2014) 1083–1099 &lbrack;[arXiv:1109.1919](https://arxiv.org/abs/1109.1919), [webpage](https://www.math.bgu.ac.il/~amyekut/publications/comb-descent/comb-descent.html)&rbrack;

* [[Alexander Campbell]], _A higher categorical approach to Giraud's non-abelian cohomology_, PhD thesis, Macquarie University (2016) &lbrack;[hdl:1959.14/1261186](http://hdl.handle.net/1959.14/1261186)&rbrack;


Existence of [[classifying spaces]] for [[principal 2-bundles]]/[[nonabelian gerbes]]:

* [[John Baez]], [[Danny Stevenson]], _The Classifying Space of a Topological 2-Group_,  In: Baas N., Friedlander E., Jahren B., Østvær P. (eds.) *Algebraic Topology*, Abel Symposia, vol 4. Springer 2009 ([arXiv:0801.3843](https://arxiv.org/abs/0801.3843), [doi:10.1007/978-3-642-01200-6_1](https://doi.org/10.1007/978-3-642-01200-6_1))


### General theory -- $\infty$-bundles/$\infty$-gerbes

Discussion of the general theory via [[principal ∞-bundles]] and/or [[∞-gerbes]] and/or [[∞-stacks]]:

* [[Paul Glenn]], _Realization of cohomology classes in arbitrary exact categories_, J. Pure Appl. Algebra 25, 1982, no. 1, 33- 105 (<a href="https://doi.org/10.1016/0022-4049(82)90094-9">doi:10.1016/0022-4049(82)90094-9</a>)

In a context of [[nonabelian Hodge theory]]:

* [[Carlos Simpson]], _The Hodge filtration on nonabelian cohomology_, in: János Kollár, Robert Lazarsfeld, [[David Morrison]] (eds.) _Algebraic Geometry Santa Cruz 1995, Part 2_, Proceedings of Symposia in Pure Mathematics Volume 62.2, AMS 1997 ([arXiv:alg-geom/9604005](http://arxiv.org/abs/alg-geom/9604005), [doi:10.1090/pspum/062.2](https://doi.org/10.1090/pspum/062.2))

* [[Carlos Simpson]], _Secondary Kodaira-Spencer classes and nonabelian Dolbeault cohomology_ ([arXiv:alg-geom/9712020](http://arxiv.org/abs/alg-geom/9712020))

* [[Carlos Simpson]], _Algebraic aspects of higher nonabelian Hodge theory_,  in: [[Fedor Bogomolov]], [[Ludmil Katzarkov]] (eds.), _Motives, polylogarithms and Hodge theory, Part II_ (Irvine, CA, 1998), Int. Press Lect. Ser., 3, II, Int. Press, 2002, 2016, 417-604.  ([arXiv:math/9902067](http://arxiv.org/abs/math/9902067), [ISBN:9781571462909](https://www.intlpress.com/site/pub/pages/books/items/00000089/index.php))

* [[Carlos Simpson]], [[Tony Pantev]], [[Ludmil Katzarkov]], _Nonabelian mixed Hodge structures_ ([arXiv:math/0006213](http://arxiv.org/abs/math/0006213))

Generally:

* {#Toen02} [[Bertrand Toën]], Def. 6.0.6 in: _Stacks and Non-abelian cohomology_, lecture at _[Introductory Workshop on Algebraic Stacks, Intersection Theory, and Non-Abelian Hodge Theory](https://www.msri.org/realvideo/index04.html)_, MSRI 2002 ([slides](http://www.msri.org/publications/ln/msri/2002/introstacks/toen/1/index.html), [ps](http://www.msri.org/publications/ln/msri/2002/introstacks/toen/1/meta/aux/toen.ps), [pdf](https://perso.math.univ-toulouse.fr/btoen/files/2015/02/msri2002.pdf), [[ToenStacksAndNonabelianCohomology.pdf:file]])

* [[J. F. Jardine]], Z. Luo, _Higher principal bundles_, Mathematical Proceedings of the Cambridge Philosophical Society,  Volume 140, Issue 2 March 2006 , pp. 221-243 ([pdf](http://www.math.uiuc.edu/K-theory/0681/cocycles6.pdf), [doi:10.1017/S0305004105008911](https://doi.org/10.1017/S0305004105008911))

* [[J. F. Jardine]], _Cocycle categories_, In: [[Nils Baas]], [[Eric Friedlander]], B. Jahren , [[Arne Østvær]] (eds.) _Algebraic Topology_, Abel Symposia, vol 4. Springer 2009 ([arXiv:math/0605198](https://arxiv.org/abs/math/0605198), [doi:10.1007/978-3-642-01200-6_8]( https://doi.org/10.1007/978-3-642-01200-6_8))

* [[Jacob Lurie]], Thm. 7.1.0.1 in: _[[Higher Topos Theory]]_, Annals of Mathematics Studies 170, Princeton University Press 2009 ([pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf))


* {#Wendt} [[Matthias Wendt]], *Classifying spaces and fibrations of simplicial sheaves*, Journal of  Homotopy and Related Structures **6** 1 (2011) 1-38  &lbrack;[arXiv:1009.2930](http://arxiv.org/abs/1009.2930), [JHRS:6-1](http://tcms.org.ge/Journals/JHRS/volumes/2011/volume6-1.htm)&rbrack;

* {#RobertsStevenson16} [[David Roberts]], [[Danny Stevenson]], _Simplicial principal bundles in parametrized spaces_, New York Journal of Mathematics Volume 22 (2016) 405-440 ([arXiv:1203.2460](https://arxiv.org/abs/1203.2460), [nyjm:22-19](http://nyjm.albany.edu/j/2016/22-19.html))

* [[Danny Stevenson]], _Classifying theory for simplicial parametrized groups_ ([arXiv:1203.2461](https://arxiv.org/abs/1203.2461))

* [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _[[schreiber:Principal ∞-bundles -- theory, presentations and applications|Principal ∞-bundles -- General theory]]_, Journal of Homotopy and Related Structures, Volume 10, Issue 4 (2015), pages 749-801 ([doi:10.1007/s40062-014-0083-6](http://link.springer.com/article/10.1007/s40062-014-0083-6), [arXiv:1207.0248](http://arxiv.org/abs/1207.0248))

* [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _[[schreiber:Principal ∞-bundles -- theory, presentations and applications|Principal ∞-bundles -- Presentations]]_, Journal of Homotopy and Related Structures, Volume 10, Issue 3 (2015), pages 565-622 ([doi:10.1007/s40062-014-0077-4](http://link.springer.com/article/10.1007/s40062-014-0077-4), [arXiv:1207.0249](http://arxiv.org/abs/1207.0249))

* [[John F. Jardine]]: *Non-abelian Cohomology*, chapter 9 in: *[[Local Homotopy Theory]]*, Springer Monographs in Mathematics (2015) &lbrack;[doi:10.1007/978-1-4939-2300-7_9](https://doi.org/10.1007/978-1-4939-2300-7_9)&rbrack;

On [[cohomology operations]] on components of [[Whitehead-generalized cohomology theories]] seen in non-abelian cohomology:

* [[John Michael Boardman]], [[David Copeland Johnson]], [[W. Stephen Wilson]], _Unstable Operations in Generalized Cohomology_ ([pdf](https://hopf.math.purdue.edu/Boardman-Johnson-Wilson/bjw.pdf)), in: [[Ioan Mackenzie James]] (ed.) _[[Handbook of Algebraic Topology]]_ Oxford 1995 ([doi:10.1016/B978-0-444-81779-2.X5000-7](https://doi.org/10.1016/B978-0-444-81779-2.X5000-7))

The suggestion that *every* ([[pointed topological space|pointed]]) [[topological space|space]] may be regarded as being the [[classifying space]] of a non-abelian cohomology theory, and that this is what defines non-abelian cohomology in general:

* {#Schreiber09} [[Urs Schreiber]]: *[[schreiber:Background fields in twisted differential nonabelian cohomology|Background fields in twisted differential nonabelian cohomology]]*, talk at *[[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology]]*, Oberwolfach Report **28** (2009) &lbrack;[[OWR_2009_28.pdf:file]]&rbrack;
 > (in [[twisted cohomology|twisted]] and [[differential cohomology|differential]] generality)

* {#Lurie14} [[Jacob Lurie]], Def. 6 in: *Nonabelian Poincaré Duality*, Lecture 8 in *[Tamagawa Numbers via Nonabelian Poincare Duality (282y)](https://www.math.ias.edu/~lurie/282y.html)* (2014) &lbrack;[pdf](http://www.math.harvard.edu/~lurie/282ynotes/LectureVIII-Poincare.pdf), [[Lurie-NonabPoincareDuality.pdf:file]]&rbrack;
  > (in view of [[nonabelian Poincaré duality]])

* {#FSS20} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The Character Map in Twisted Non-Abelian Cohomology|The Character Map in Nonabelian Cohomology --- Twisted, Differential, Generalized]]_, World Scientific (2023) &lbrack;[arXiv:2009.11909](https://arxiv.org/abs/2009.11909), [doi:10.1142/13422](https://doi.org/10.1142/13422)&rbrack;
  > (generalizing the [[Chern-Dold character]] to nonabelian cohomology in this sense)



[[!redirects non-abelian cohomology]]

[[!redirects nonabelian cohomology theory]]
[[!redirects nonabelian cohomology theories]]

[[!redirects non-abelian cohomology theory]]
[[!redirects non-abelian cohomology theories]]


