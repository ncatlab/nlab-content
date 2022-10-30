
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
* automatic table of contents goes heree
{:toc}

## Idea

The notion of [[cohomology]] finds its natural general formulation in terms of [[hom-space]]s in an [[(∞,1)-topos]], as described at [[cohomology]]. Much of the cohomologies which have been traditionally considered, such as [[abelian sheaf cohomology|sheaf cohomology]] turn out to be just a special case of the general situation, for objects which are sufficiently abelian in the sense of [[stable (infinity,1)-category|stable (∞,1)-categories]].

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

Both approaches are different, but closely related. Their relation is via the notion of [[descent|codescent]].

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

For instance nonabelian [[?ech cohomology]] played a special role in the motivation of the notion of [[gerbe]]s (see in particular [[gerbe (in nonabelian cohomology)]]), concretely thought of in terms of [[pseudofunctor]]s at least in the context of nonabelian [[group cohomology]], while more abstract (and less explicit) [[homotopy theory]] methods dominate the discussion of [[infinity-stack]]s.

Either way, one obtains a notion of _cohomology on $\infty$-categories with coefficients in $\infty$-catgories_. This is, most generally, the setup of "[[nonabelian cohomology]]".

This is conceptually best understood today in terms of [[Higher Topos Theory|higher topos theory]], using [[(infinity,1)-category of (infinity,1)-sheaves|(infinity,1)-categories of (infinity,1)-sheaves]]. 

This perspective on nonabelian cohomology is discussed for instance in

* [[Bertrand Toen]], _Non-abelian cohomology_ ([slides](http://www.msri.org/publications/ln/msri/2002/introstacks/toen/1/index.html) [ps](http://www.msri.org/publications/ln/msri/2002/introstacks/toen/1/meta/aux/toen.ps))

## Properties

### Postnikov decomposition and Whitehead principle

In an [[(∞,1)-topos]] every object has a [[Postnikov tower in an (∞,1)-category]]. This means that in some sense general nonabelian cohomology can be decomposed into nonabelian cohomology in degree 1 and abelian cohomology in higher degrees, twisted by this nonabeloan cohomology. This has been called ([To&#235;n](#Toen)) the [[Whitehead principle of nonabelian cohomology]].

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


## Objects classified by nonabelian cohomology

For $g : X \to A$ a [[cocycle]] in nonabelian cohomology, we say the [[fibration sequence|homotopy fibers]] of $g$ is the object _classified_ by $g$.

For examples and discussion of this see

* [[principal bundle]]

* [[principal 2-bundle]], [[gerbe]]

* [[principal 3-bundle]], [[2-gerbe]]

* [[principal ∞-bundle]], [[∞-gerbe]] .

## References


A readable survey on nonabelian cohomology is

* [[Bertrand Toën]], _Non-abelian cohomology_ ([pdf](http://www.math.univ-toulouse.fr/~toen/msri2002.pdf))
{#Toen}

A useful motivation is

* [[Nicolas Addington]], _Fiber bundles and nonabelian cohomology_ ([pdf](http://www2.imperial.ac.uk/~naddingt/notes/gstc2007.pdf))

Early original references include

* [[Paul Dedecker]], _Cohomologie de dimension 2 &#224; coefficients non ab&#233;liens_, C. R. Acad. Sci. Paris, 247 (1958), 1160&#8211;1163;

  (with coefficients in certain [[2-group]])

* [[Paul Dedecker]], A. Frei, _Les relations d'&#233;quivalence des morphismes de la suite exacte de cohomologie non ab&#234;lienne_, C. R. Acad. Sci. Paris, 262(1966), 1298-1301

* [[Paul Dedecker]], _Three dimensional non-abelian cohomology for groups_, Category theory, homology theory and their applications, II (Battelle Institute Conf.) 1969 ([MathSciNet](http://www.ams.org/mathscinet/pdf/263894.pdf?pg1=IID&s1=55880&vfpref=html&r=15))

  (with coefficients in certain [[3-group]]s presented by [[crossed square]]s)

The standard classical monograph focusing on low-dimensional cases is

* J. Giraud, _Cohomologie non ab&#233;lienne_ , Springer  (1971)

  (aspects of classification of $G$-[[gerbe]]s by cohomology with coefficients in the [[automorphism 2-group]] $AUT(G)$, but imposes extra constraints)

* [[Larry Breen]], _Bitorseurs et cohomologie non-Ab&#233;lienne_ , The Grothendieck Festschrift: a collection of articles written in honour of the 60th birthday of Alexander Grothendieck, Vol. I, edited P.Cartier, et al., Birkh&#228;user, Boston, Basel, Berlin, 401-476, (1990)

* [[Ieke Moerdijk]], _Lie Groupoids, Gerbes, and Non-Abelian Cohomology _ ([journal](http://www.springerlink.com/content/ul554x3077444545/))

The classification of [[∞-gerbe]]s is secretly in 

* [[Matthias Wendt]], _Classifying spaces and fibrations of simplicial sheaves_ , Journal of  Homotopy and Related Structures 6(1), 2011, pp. 1--38.  ([arXiv](http://arxiv.org/abs/1009.2930)) ([published version](http://tcms.org.ge/Journals/JHRS/volumes/2011/volume6-1.htm))
{#Wendt}

see the discussion at [[∞-gerbe]] for more on this.

Carlos Simpson has studied [[nonabelian Hodge theory]].

* [[Carlos Simpson]], _The Hodge filtration on nonabelian cohomology_ ([arXiv](http://arxiv.org/abs/alg-geom/9604005))

* [[Carlos Simpson]], _Secondary Kodaira-Spencer classes and nonabelian Dolbeault cohomology_ ([arXiv](http://arxiv.org/abs/alg-geom/9712020))

* [[Carlos Simpson]], _Algebraic aspects of higher nonabelian Hodge theory_ ([arXiv](http://arxiv.org/abs/math/9902067))

* [[Carlos Simpson]], [[Tony Pantev]], [[Ludmil Katzarkov]], _Nonabelian mixed Hodge structures_ ([arXiv](http://arxiv.org/abs/math/0006213))

Some links and references can be found at Alsani's descent and category theory [page](http://north.ecc.edu/alsani/descent.html).

In as far as nonabelian cohomology is nothing but the study of [[(infinity,1)-categorical hom-space|hom-spaces]] between [[∞-stack]]s, see also the references at [[∞-stack]].
