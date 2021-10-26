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

The relationships between (some) of the categories can be sumarised by the following diagram.

$$
\begin{svg}
[[!include generalized smooth space > relationships]]
\end{svg}
$$

+-- {: .query}
I subtracted $20$ from the $x$-coordinates on the names in the diagram so that they would stay in the boxes on my screen, but I\'m not sure if this is right; the original looks fine to me as [a free-standing diagram](http://www.math.ntnu.no/~stacey/documents/smooth.7-1.svg), so I don\'t know why it looks wrong here.

Anyway, if anybody finds that this version is worse than the previous one, then change it back to the previous one and chalk it up to an error in my browser.  ---Toby

Thanks, Toby.  I was just heading over to see if I could fix it myself but you beat me to it.  There seem to be a few subtleties over how Instiki imports SVG and I'm learning them by trial and error (and by bugging Jacques!).  The picture in the Sandbox now looks right and, thanks to you, so does this one.  Text boxes seems to be the trickiest to get right when doing TikZ-to-SVG conversion.  ---Andrew

It it helps any, I think that the problem was that the alphabetic text (but not the dates) *began* where it ought to have been *centred*.  ---Toby
=--


## Literature

Eventually the following will be a _commented_ list -- promised.

* John Baez and Alexander Hoffnung, _Convenient Categories of Smooth Spaces_ ([arXiv](http://arxiv.org/abs/0807.1704), [blog](http://golem.ph.utexas.edu/category/2008/05/convenient_categories_of_smoot.html))

* Patrick Iglesias-Zemmour, _Diffeology_ ([pdf](http://math.huji.ac.il/~piz/Site/The%20Book/The%20Book.html))

* Matthias Kreck, _Stratifolds and differential algebraic topology_ ([pdf](http://www.hausdorff-research-institute.uni-bonn.de/files/kreck-DA24_08_07.pdf))

* William Lawvere, _Taking categories seriously_ ([pdf](http://www.emis.de/journals/TAC/reprints/articles/8/tr8.pdf))

* David Spivak, _Quasi-smooth derived manifolds_ ([pdf](http://math.mit.edu/~dspivak/files/thesis1.pdf))

* Andrew Stacey, _Comparative Smootheology_ ([arXiv](http://arxiv.org/abs/0802.2225))

* Martin Laubinger, _Differential Geometry in Cartesian Closed Categories of Smooth Spaces_ ([pdf](http://etd.lsu.edu/docs/available/etd-02212008-165645/unrestricted/laubingerdiss.pdf))

* Alexander Hoffnung, _Smooth spaces: convenient categories for differential geometry_, ([pdf slides](http://math.ucr.edu/~alex/goettingen.pdf))

* Alexander Hoffnung, _From Smooth Spaces to Smooth Categories_, ([pdf slides](http://aix1.uottawa.ca/~scpsg/Fields09/alex.hoffnung.pdf))

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

[[!redirects generalized smooth strcuture]]
[[!redirects generalized smooth structures]]


