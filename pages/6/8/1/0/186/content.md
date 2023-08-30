+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


# Generalised smooth spaces
* table of contents
{: toc}

## Idea

Generalised smooth spaces are, roughly speaking, generalisations of [[smooth manifolds]].  Their _raison d'etre_ is the following

> Manifolds are fantastic spaces.  It's a pity that there aren't more of them.

Many spaces that occur in mathematics aren't manifolds but one would like to be able to treat them as if they were manifolds; in particular, they should have some *smooth* structure that goes beyond mere topology.  By considering examples of these spaces and by considering what specifically one would like to do with or to them, it is possible to generalise the idea of a smooth manifold to encompass the new examples whilst preserving enough structure to retain the old tools.  There have been several such generalisations in recent mathematical history.  A (partial) list is below.

Often the examples of spaces that one would like to consider as manifolds are formed by applying a categorical construction to ordinary manifolds; such as limits, quotients, or function spaces.  This leads one to ask for the categorical properties of each of the resulting categories of generalised smooth spaces.

Another obvious question to ask is what tools and techniques can be extrapolated from smooth manifolds to generalised smooth spaces.  In addition, whilst some techniques have obvious generalisations there may be some hidden twists that are not apparent on just smooth manifolds.


## Examples

According to the general nonsense of [[space and quantity]], generalized smooth spaces may be determined by [[sheaf|sheaves]] on smooth test spaces, in which case we call them [[smooth spaces]] here, or by co-(pre)sheaves on test spaces, in which case we call them [[structured generalized spaces]] here.

* [[smooth space|Smooth spaces]]

  * [[Chen space|Chen spaces]] (called _differentiable spaces_ in Chen's works).
  * [[diffeological space|Diffeological spaces]]

    * [[differentiable stack|Differentiable stacks]]/[[Lie groupoid]]
      * [[orbifold|Orbifolds]]

  * [[∞-Lie groupoid]]

  * [[Kriegl and Michor's cartesian closed category of manifolds]]

* [[CartSp]]-[[structured (∞,1)-topos|Structured (∞,1)-topos]]

  * [[differential module|Differential modules]]
  * [[Smith space (generalized smooth space)|Smith spaces]]
  * [[stratifold|Stratifolds]]
  * [[polyfold|Polyfolds]]
  * [[derived smooth manifold|Derived smooth manifolds]]

* both

  * [[Froelicher space|Frölicher spaces]]

{#DiagramOfAdjointFunctors} The relationships between (some) of the categories can be sumarised by the following diagram of [[adjoint functors]]:

\begin{imagefromfile}
    "file_name": "Stacey-NotionsOfSmoothSpaceRelationships.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "(from [Stacey 2011](#Stacey11))"
\end{imagefromfile}



## Literature


* John Baez and Alexander Hoffnung, _Convenient Categories of Smooth Spaces_, Trans. Amer. Math. Soc., Vol. 363 No. 11 (2011), 5789-5825, doi:[10.1090/S0002-9947-2011-05107-X](https://doi.org/10.1090/S0002-9947-2011-05107-X), [arXiv:0807.1704](http://arxiv.org/abs/0807.1704), [blog](http://golem.ph.utexas.edu/category/2008/05/convenient_categories_of_smoot.html).

* Patrick Iglesias-Zemmour, _Diffeology_, Mathematical Surveys and Monographs **185**, AMS (2013), [publisher page](https://doi.org/10.1090/surv/185), ([book site](http://math.huji.ac.il/~piz/Site/TheBook-AMS.html)).

* Matthias Kreck, _Differential Algebraic Topology: From Stratifolds to Exotic Spheres_, Graduate Studies in Mathematics Volume **110**, AMS (2010)  ([publisher page](https://bookstore.ams.org/gsm-110)), ([author pdf](https://www.hcm.uni-bonn.de/fileadmin/user_upload/kreck-DA.pdf)).

* William Lawvere, _Taking categories seriously_, Reprints in Theory and Applications of Categories, No. 8 (2005) pp. 1-24 ([journal](http://www.tac.mta.ca/tac/reprints/articles/8/tr8abs.html)).

* David Spivak, _Quasi-smooth derived manifolds_, thesis (2010) ([pdf](https://web.archive.org/web/20221206173621/https://math.mit.edu/~dspivak/files/thesis1.pdf)).

* {#Stacey11} [[Andrew Stacey]], _Comparative Smootheology_, Theory and Applications of Categories, **25** 4 (2011) 64-117, &lbrack;[tac:25-4](http://www.tac.mta.ca/tac/volumes/25/4/25-04abs.html)), [arXiv:0802.2225](http://arxiv.org/abs/0802.2225)&rbrack;

* Martin Laubinger, _Differential Geometry in Cartesian Closed Categories of Smooth Spaces_ ([pdf](https://web.archive.org/web/20150920152120/http://etd.lsu.edu/docs/available/etd-02212008-165645/unrestricted/laubingerdiss.pdf))

* Alexander Hoffnung, _Smooth spaces: convenient categories for differential geometry_, ([pdf slides](https://web.archive.org/web/20100629002755/http://math.ucr.edu/~alex/goettingen.pdf))

* Alexander Hoffnung, _From Smooth Spaces to Smooth Categories_, ([pdf slides](https://web.archive.org/web/20110714114128/http://aix1.uottawa.ca/%7Escpsg/Fields09/alex.hoffnung.pdf))

There are also Hofer's [[polyfold|polyfolds]].

Concerning [[smooth ∞-stacks]] there is useful material in 

* Daniel Dugger, _Sheaves and homotopy theory_ ([web](http://math.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf))


## Remarks

Dual to generalized smooth spaces are [[generalized smooth algebra|generalized smooth algebras]] of functions on them, according to the general lore of [[space and quantity]].


## Further discussion

We had extensive discussion of generalized smooth spaces at the $n$-Caf&#233;:

 * _Comparative Smootheology_ ([I](http://golem.ph.utexas.edu/category/2008/01/comparative_smootheology.html), [II](http://golem.ph.utexas.edu/category/2008/04/comparative_smootheology_ii.html), [III](http://golem.ph.utexas.edu/category/2008/09/comparative_smootheology_iii.html)), [IV](http://golem.ph.utexas.edu/category/2009/04/comparative_smootheology_iv.html)

 * [_Convenient categories of smooth spaces_](http://golem.ph.utexas.edu/category/2008/05/convenient_categories_of_smoot.html)

 * [_Spivak on derived manifolds_](http://golem.ph.utexas.edu/category/2008/08/david_spivak_on_derived_manifo.html)

 * [_B&#228;r on fiber integration in differential cohomology_](http://golem.ph.utexas.edu/category/2008/11/br_on_fiber_integration_in_dif.html)



[[!redirects generalized smooth space]]
[[!redirects generalized smooth spaces]]
[[!redirects generalised smooth space]]
[[!redirects generalised smooth spaces]]

[[!redirects generalized smooth structure]]
[[!redirects generalized smooth structures]]


