#Contents#
* automatic table of contents
{:toc}

# Idea #

In any context it is of interest to ask which kind of [[morphisms]] $p : C \to D$ arise as [[pullbacks]] along a classifying morphism $S_p : D \to U$ to some universal object $U$ of some universal morphism $p_{univ} : \hat U \to U$.

The Grothendieck construction describes this in the context of [[Cat]]: a morphism $p : C \to D$ of [[category|categories]] -- i.e. a [[functor]] -- is called a [[fibered category]] or [[Grothendieck fibration]] if it is encoded in a [[pseudofunctor]] $S_p : D \to Cat$.

The reconstruction of $p$ from the pseudofunctor $S_p$ is the Grothendieck construction.

# Definition #

Let for the time being [[Grpd]] be the 1-category of [[groupoids]] and [[functors]] between them.

Recall from [[generalized universal bundle]] that the "universal [[Grpd]]-[[bundle]]" is $Grpd_* \to Grpd$, where $Grpd_*$ is the category of [[pointed object|pointed]] [[groupoids]].

Then for $F : C \to Grpd$ a [[functor]], the Grothendieck construction for $F$ is the [[pullback]] $\int F \to C$ of $Grpd_* \to Grpd$ along $F$:

$$
  \array{
    \int F &\to& Grpd_*
    \\
    \downarrow && \downarrow
    \\
    C &\stackrel{F}{\to}& Grpd
  }
  \,.
$$

This means that the objects of $\int F$ are pairs $(c,a)$, where $c \in Obj(C)$ and $a \in Obj(F(c))$ and morphisms in $\int F$ are given by pairs $(c \stackrel{f}{\to} c', \alpha : F(f)(a) \to a')$. This is to be visualized as

$$
  \int F = 
  \left\{
  \array{
    && {*}
    \\
    & {}^a\swarrow &\Downarrow^{\alpha}& \searrow^{a'}
    \\
    F(c) && \stackrel{F(f)}{\to} F(c')
    \\
    \\
    c &&\stackrel{f}{\to}&& c'
  }
  \right\}
  \,.
$$


## Generalizations ##

### $n = 0$ ###
The analog of the Grothendieck construction one categorical dimension down is the [[category of elements]] of a [[presheaf]].

### $n = (\infty,1)$  ###

The analog of the Grothendieck construction for [[(infinity,1)-category|(∞,1)-categories]] is described at [[Cartesian fibration]] and at [[universal fibration of (∞,1)-categories]]. 

The correspondence between $(\infty,1)$-categorical [[cartesian fibrations]] $E \to C$ and [[(infinity,1)-presheaf|(∞,1)-presheaves]] $C \to (\infty,1)Cat^{op}$ is [[model category|modeled]] by the [[Quillen equivalence]] between the [[model structure on marked simplicial over-sets]] and the projective [[global model structure on simplicial presheaves]].


## Warning on terminology ##

The term 'Grothendieck Construction' is applied in the literature to at least two very different constructions (and as [[Alexander Grothendieck|Grothendieck]] introduced so many new ideas and constructions to mathematics, perhaps there are others!). One concerns the construction of a [[fibered category]] from a [[pseudofunctor]] and will be treated in more detail in the entry on [[Grothendieck fibration]].  The other referes to constructing the [[Grothendieck group]] is  in the context of [[K-theory]] from isomorphism classes of vector bundles on a space by the introduction of formal inverses, 'virtual bundles'.  This constructs an Abelian group from the semi-group of isomorphism classes.




##References##

* [Grothendieck construction](http://en.wikipedia.org/wiki/Grothendieck_construction) (Wikipedia)
* [The Grothendieck Construction](http://online.itp.ucsb.edu/online/ktheory/wu/) (UCSB ITP Seminar)
* [The Homotopy Theory of n-Fold Categories](http://www.math.uchicago.edu/~fiore/1/ThomasonNFoldBeamerSlides.pdf)
* [Inference System Integration via Logic Morphisms](http://www.kestrel.edu/home/projects/logicware/slides-9806/sld001.htm)
* [Category Theory for Computing Science](http://www.cwru.edu/artsci/math/wells/pub/ctcs.html)
* [On the Classification of Topological Field Theories (Draft)](http://www-math.mit.edu/~lurie/papers/cobordism.pdf) Lurie
