+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


\tableofcontents

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


## Related concepts

* Under the [[duality between algebra and geometry]], generalized smooth spaces correspond to [[generalized smooth algebras]] of functions on them.



## Literature
 {#Literature}

The notion of [[diffeological spaces]]:

* {#Souriau79} [[Jean-Marie Souriau]]: _Groupes diff&#233;rentiels_, in _Differential Geometrical Methods in Mathematical Physics_ (Proc. Conf., Aix-en-Provence/Salamanca, 1979), Lecture Notes in Math. **836**, Springer (1980) 91-128. &lbrack;[doi:10.1007/BFb0089728](https://doi.org/10.1007/BFb0089728), [mr:607688](http://www.ams.org/mathscinet-getitem?mr=607688)&rbrack;

* [[Kuo-Tsai Chen]]: _On differentiable spaces_, in:  [[William Lawvere]], [[Stephen Schanuel]] (eds.), _[[Categories in Continuum Physics]]_, Lectures given at a Workshop held at SUNY, Buffalo 1982, Lecture Notes in Mathematics **1174** (1986) &lbrack;[doi:10.1007/BFb0076928](https://link.springer.com/book/10.1007/BFb0076928)&rbrack;

* [[Patrick Iglesias-Zemmour]], _Diffeology_, Mathematical Surveys and Monographs **185**, AMS (2013) &lbrack;[doi:10.1090/surv/185](https://doi.org/10.1090/surv/185), ([book site](http://math.huji.ac.il/~piz/Site/TheBook-AMS.html)&rbrack;

Amplification that [[diffeological spaces]] form a [[quasi-topos]] and hence a fairly "convenient category" of smooth spaces:
 
* Martin Laubinger: _Differential Geometry in Cartesian Closed Categories of Smooth Spaces_, LSU Doctoral Dissertations **3981** (2008) &lbrack;[lsu:3981](https://repository.lsu.edu/gradschool_dissertations/3981)&rbrack;

* [[Alexander Hoffnung]]: _Smooth spaces: convenient categories for differential geometry_, talk slides (2009) &lbrack;[[Hoffnung-Goettingen2009.pdf:file]]&rbrack;

* [[Alexander Hoffnung]]: _From Smooth Spaces to Smooth Categories_, talk slides (2009) &lbrack;[[Hoffnung-Ottawa2009.pdf:file]]&rbrack;

* [[John Baez]], [[Alexander Hoffnung]]: _Convenient Categories of Smooth Spaces_, Trans. Amer. Math. Soc. **363** 11 (2011) 5789-5825 &lbrack;[doi:10.1090/S0002-9947-2011-05107-X](https://doi.org/10.1090/S0002-9947-2011-05107-X), [arXiv:0807.1704](http://arxiv.org/abs/0807.1704), [blog](http://golem.ph.utexas.edu/category/2008/05/convenient_categories_of_smoot.html)&rbrack;

* {#Stacey11} [[Andrew Stacey]]: _Comparative Smootheology_, Theory and Applications of Categories, **25** 4 (2011) 64-117, &lbrack;[tac:25-4](http://www.tac.mta.ca/tac/volumes/25/4/25-04abs.html)), [arXiv:0802.2225](http://arxiv.org/abs/0802.2225)&rbrack;


Discussion in the "more convenient" full [[topos theory|topos theoretic]] context of [[synthetic differential geometry]]:

* [[William Lawvere]]: _Taking categories seriously_, Reprints in Theory and Applications of Categories **8** (2005) 1-24 &lbrack;[tac:tr8](http://www.tac.mta.ca/tac/reprints/articles/8/tr8abs.html)&rbrack;

Specifically on the "well-adapted" [[Cahiers topos]] of [[formal smooth sets]]:

* {#Dubuc79} [[Eduardo Dubuc]], *Sur les modèles de la géométrie différentielle synthétique*, [[Cahiers|Cahiers de Topologie et Géométrie Différentielle Catégoriques]] **20**  3 (1979) 231-279  &lbrack;[numdam:CTGDC_1979__20_3_231_0](http://www.numdam.org/item?id=CTGDC_1979__20_3_231_0)&rbrack; 

* {#KhavkineSchreiber17} [[Igor Khavkine]], [[Urs Schreiber]]: _[[schreiber:Synthetic variational calculus|Synthetic geometry of differential equations: I. Jets and comonad structure]]_, J. Geom. Physics (2026) &lbrack;[arXiv:1701.06238](https://arxiv.org/abs/1701.06238)&rbrack;

* [[Grigorios Giotopoulos]], [[Hisham Sati]]: *Field Theory via Higher Geometry II: Thickened Smooth Sets as Synthetic Foundations* &lbrack;[arXiv:2512.22816](https://arxiv.org/abs/2512.22816)&rbrack;

extending the [[topos]] of [[smooth sets]] (which in turn subsumes the above [[diffeological spaces]] as its [[concrete objects]] and further extends to [[smooth infinity-groupoids|smooth $\infty$-groupoids]]):

* {#Schreiber25} [[Urs Schreiber]]: *[[schreiber:Higher Topos Theory in Physics]]*, [[nLab:Encyclopedia of Mathematical Physics 2nd ed]]$\;$**4** (2025) 62-76 &lbrack;[doi:10.1016/B978-0-323-95703-8.00210-X](https://doi.org/10.1016/B978-0-323-95703-8.00210-X), [ISBN:9780323957038](https://shop.elsevier.com/books/encyclopedia-of-mathematical-physics/szabo/978-0-323-95703-8), [arXiv:2311.11026](https://arxiv.org/abs/2311.11026)&rbrack;

* {#GiotopoulosSati23} [[Grigorios Giotopoulos]], [[Hisham Sati]]: *Field Theory via Higher Geometry I: [[schreiber:Smooth Sets of Fields]]*, Journal of Geometry and Physics **213** (2025) 105462 &lbrack;[arXiv:2312.16301](https://arxiv.org/abs/2312.16301), [doi:10.1016/j.geomphys.2025.105462](https://doi.org/10.1016/j.geomphys.2025.105462)&rbrack;

* [[Alberto Ibort]], Arnau Mas: *Smooth sets of fields: A pedagogical introduction*, Geometric Mechanics (2025) &lbrack;[arXiv:2510.20422](https://arxiv.org/abs/2510.20422), [doi:10.1142/S2972458925400052](https://doi.org/10.1142/S2972458925400052), [ResearchGate:394210704](https://www.researchgate.net/publication/394210704)&rbrack;


On [[stratifolds]]:

* [[Matthias Kreck]]: _Differential Algebraic Topology: From Stratifolds to Exotic Spheres_, Graduate Studies in Mathematics Volume **110**, AMS (2010)  ([publisher page](https://bookstore.ams.org/gsm-110)), ([author pdf](https://www.hcm.uni-bonn.de/fileadmin/user_upload/kreck-DA.pdf)).


On [[derived smooth manifolds]]:

* [[David Spivak]], _Quasi-smooth derived manifolds_, thesis (2010) &lbrack;[pdf](https://web.archive.org/web/20221206173621/https://math.mit.edu/~dspivak/files/thesis1.pdf)&rbrack;


There are also Hofer's [[polyfolds]].


[[!redirects generalized smooth space]]
[[!redirects generalized smooth spaces]]
[[!redirects generalised smooth space]]
[[!redirects generalised smooth spaces]]

[[!redirects generalized smooth structure]]
[[!redirects generalized smooth structures]]


