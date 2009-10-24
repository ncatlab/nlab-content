<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>


#Contents#
* automatic table of contents goes heree
{:toc}

#Idea#

The notion of [[cohomology]] finds its natural general formulation in terms of [[hom-space]]s in an [[(infinity,1)-topos]], as described at [[cohomology]]. Much of the cohomologies which have been traditionally considered, such as [[abelian sheaf cohomology|sheaf cohomology]] turn out to be just a special case of the general situation, for objects which are sufficiently abelian in the sense of [[stable (infinity,1)-category|stable (infinity,1)-categories]].

Therefore to amplify that one is looking at general [[cohomology]] without restricting to [[abelian sheaf cohomology|abelian cohomology]] one sometimes speaks of  **nonabelian cohomology**. 

#History#

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

For instance nonabelian [[Cech cohomology]] played a special role in the motivation of the notion of [[gerbe]]s (see in particular [[gerbe (in nonabelian cohomology)]]), cocretely thought of in terms of [[pseudofunctor]]s at least in the context of nonabelian [[group cohomology]], while more abstract (and less explicit) [[homotopy theory]] methods dominate the discussion of [[infinity-stack]]s.

Either way, one obtaines a notion of _cohomology on $\infty$-categories with coefficients in $\infty$-catgories_. This is, most generally, the setup of "[[nonabelian cohomology]]".

This is conceptually best understood today in terms of [[Higher Topos Theory|higher topos theory]], using [[(infinity,1)-category of (infinity,1)-sheaves|(infinity,1)-categories of (infinity,1)-sheaves]]. 

This perspective on nonabelian cohomology is discussed for instance in

* [[Bertrand Toen]], _Non-abelian cohomology_ ([slides](http://www.msri.org/publications/ln/msri/2002/introstacks/toen/1/index.html) [ps](http://www.msri.org/publications/ln/msri/2002/introstacks/toen/1/meta/aux/toen.ps))


#Nonabelian group cohomology#

Sometimes the term _nonabelian cohomology_ is used in a more restrictive sense. Often people mean 
"nonabelian [[group cohomology]]" when they say nonabelian cohomology, hence restricting to the domains to [[group|groups]], which are [[groupoid|groupoids]] with a single object.

This kind of nonabelian cohomology is discussed for instance in

* [[John Baez]], [[Mike Shulman]], [[Lectures on n-Categories and Cohomology]] ([arXiv](http://arxiv.org/abs/math.CT/0608420)).

That and how ordinary [[group cohomology]] is reproduced from the [[homotopical cohomology theory]] of [[strict omega-groupoid|strict omega-groupoids]] is discussed in detail in chapter 12 of 

* [[Ronnie Brown]], P. Higgins, R. Sivera, [[nonabelian algebraic topology|Nonabelian algebraic topology]].

#Objects classified by nonabelian cohomology#

For $g : X \to A$ a cocycle in nonabelian cohomology, we say the [[fibration sequence|homotopy fibers]] of $g$ is the object _classified_ by $g$.

For examples and discussion of this see

* [[principal bundle]]

* [[gerbe]]

* [[principal 2-bundle]]

* [[principal infinity-bundle]] .

#References#


A readable survey is

* [[Bertrand Toen]], _Non-abelian cohomology_ ([ps](http://www.msri.org/publications/ln/msri/2002/introstacks/toen/1/meta/aux/toen.ps))

A useful motivation is

* [[Nicolas Addington]], _Fiber bundles and nonabelian cohomology_ ([pdf](http://www.math.wisc.edu/~adding/notes/gstc2007.pdf))

Early references include

* P. Dedecker, _Cohomologie de dimension 2 &#224; coefficients non ab&#233;liens_, C. R. Acad. Sci. Paris, 247 (1958), 1160&#8211;1163;

* P. Dedecker, A. Frei, _Les relations d'&#233;quivalence des morphismes de la suite exacte de cohomologie non ab&#234;lienne_, C. R. Acad. Sci. Paris, 262(1966), 1298-1301

* P. Dedecker, _Three dimensional non-abelian cohomology for groups_, Category theory, homology theory and their applications, II (Battelle Institute Conf.) 1969

The standard classical monograph focusing on low-dimensional cases is

* J. Giraud, _Cohomologie non ab&#233;lienne_ , Springer  (1971)

See also [[gerbe|nonabelian gerbe]].

* [[Larry Breen]], _Bitorseurs et cohomologie non-Ab&#233;lienne_ , The Grothendieck Festschrift: a collection of articles written in honour of the 60th birthday of Alexander Grothendieck, Vol. I, edited P.Cartier, et al., Birkh&auml;user, Boston, Basel, Berlin, 401-476, 1990.

* [[Ieke Moerdijk]], _Lie Groupoids, Gerbes, and Non-Abelian Cohomology _ ([journal](http://www.springerlink.com/content/ul554x3077444545/))


Carlos Simpson has studied nonabelian versions of [[Hodge theory]].

* [[Carlos Simpson]], _The Hodge filtration on nonabelian cohomology_ ([arXiv](http://arxiv.org/abs/alg-geom/9604005))

* [[Carlos Simpson]], _Secondary Kodaira-Spencer classes and nonabelian Dolbeault cohomology_ ([arXiv](http://arxiv.org/abs/alg-geom/9712020))

* [[Carlos Simpson]], _Algebraic aspects of higher nonabelian Hodge theory_ ([arXiv](http://arxiv.org/abs/math/9902067))

* [[Carlos Simpson]], [[Tony Pantev]], [[udmil Katzarkov]], _Nonabelian mixed Hodge structures_ ([arXiv](http://arxiv.org/abs/math/0006213))

Some links and references can be found at Alsani's descent and category theory [page](http://north.ecc.edu/alsani/descent.html).