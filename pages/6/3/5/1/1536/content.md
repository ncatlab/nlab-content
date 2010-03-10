#Contents#
* automatic table of contents
{:toc}

## Idea 

In any context it is of interest to ask which kind of [[morphisms]] 

$$
  \array{
    E
    \\
    \downarrow^{\mathrlap{p}}
    \\
    C
  }
$$

arise as [[pullbacks]] along a classifying morphism $S_p : C \to U$ to 
some universal object $U$ of some universal morphism 

$$
  \array{
    \hat U
    \\
    \downarrow^{\mathrlap{p_{univ}}}
    \\
    U
  }
  \,.
$$

The Grothendieck construction describes this in the context of [[Cat]]: a morphism $p : E \to C$ of [[category|categories]] -- i.e. a [[functor]] -- is called a [[fibered category]] or [[Grothendieck fibration]] if it is encoded in a [[pseudofunctor]]/[[2-functor]] $S_p : C^{op} \to Cat$.

The reconstruction of $p$ from the pseudofunctor $S_p$ is the **Grothendieck construction** 

$$
  \int \;\; : \;\; Func(C^{op}, Cat) \to Cat/C
$$

which is a [[2-functor]] from the [[2-category]] of pseudofunctors $C^{op} \to Cat$ to the [[overcategory]] of [[Cat]] over $C$.

The essential image of this functor consists of [[Grothendieck fibration]]s and this establishes an [[equivalence of categories|equivalence]] of [[2-categories]]

$$
  \int : Func(C^{op}, Cat) \stackrel{\simeq}{\to} Fib(C) 
$$

between 2-functors $C^{op} \to Cat$ and [[Grothendieck fibration]]s over $C$.

When restricted to pseudofunctors with values in [[Grpd]] $\subset$ [[Cat]] this identifies the [[fibration fibered in groupoids|Grothendieck fibrations in groupoids]]

$$
  \int \;\;:\;\; Func(C^{op}, Grpd) \stackrel{\simeq}{\to} FibGrpd(C) 
  \,.
$$

This equivalence notably allows to discuss [[stack]]s equivalently as pseudofunctors or as groupoid fibrations (in each case satisfying a [[descent]] condition with respect to a [[Grothendieck topology]] on $D$).

The Grothendieck construction is one of the central aspects of [[category theory]], together with the notions of universal constructions such as [[limit]], [[adjunction]] and [[Kan extension]]. It is expected to have suitable analogs in all sufficiently good contexts of [[higher category theory]]. Notably there is an [[(∞,1)-Grothendieck construction]] in [[(∞,1)-category]] theory.

## Definition 

> under construction

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
    F(c) && \stackrel{F(f)}{\to} && F(c')
    \\
    \\
    c &&\stackrel{f}{\to}&& c'
  }
  \right\}
  \,.
$$


## Adjoints to the Grothendieck construction {#adjunction}

The Grothendieck construction functor

$$
  \int : [C^{op}, Cat] \to Cat/C
$$

has a left and a right [[adjoint functor]].

### The left adjoint

The [[left adjoint]] is the functor

$$
  L : (p : E \to C) \mapsto ( (-)/p : C^{op} \to Cat) 
$$

that assigns to a functor $p$ the presheaf which sends $c \in C$ to the [[comma category]] 

$$
  c/p = 
  \left\{
    \array{
      && c
      \\
      & \swarrow && \searrow
      \\
      p(e_1) &&\to&& p(e_2)
    }
  \right\}
  \,,
$$

i.e.

$$
  L(E \stackrel{p}{\to}C) : c \mapsto c/p
  \,.
$$

This functor may equivalently be expressed as follows:

for given $(E \stackrel{p}{\to} C)$ consider the [[weak limit|weak pushout]]

$$
  \array{
    E &\hookrightarrow& E^{\triangleright}
    \\
    \downarrow^{\mathrlap{p}} &\swArrow& \downarrow
    \\
    C &\to& K(p)
  }
$$

of _[[2-categories]]_  (so that $K(p)$ is a [[2-category]]) where $K^{\triangleright}$ is $K$ with one [[terminal object]] $v$ adjoined (a [[join of quasi-categories|join]] of categories).

### In terms of a cone construction {#Cone}

+-- {: .un_lemma }
###### Claim

We have

$$
  c/p \simeq Hom_{K(p)}(c,v)
  \,.
$$

And hence the left adjoint to the Grothendieck construction may be realized as the assignment that sends $p : E \to C$ to the pseudofunctor 

$$
  L(p) := Hom_{K(p)}(-, v) : C^{op} \to Cat
  \,.
$$

=--

+-- {: .proof}
###### Proof

It is convenient to compute the weak pushout by embedding the situation from [[Cat]] into the bigger context of [[(∞,1)-categories]] and using the [[model category|model]] of that provided by [[sSet]]: the [[model structure for quasi-categories]]. This also facilitates the generalization of the argument from 1-categories to higher categories.

So consider equivalently the weak pushout diagram

$$
  \array{
    N(E) &\hookrightarrow& N(E)^{\triangleright}
    \\
    \downarrow^{\mathrlap{N(p)}} &\swArrow& \downarrow
    \\
    N(C) &\to& N(K(p))
  }
$$

of [[quasi-categories]], where $N(-)$ is the [[nerve]] operation and where $N(E)^{\triangleright} = N(E) \star *$ is the [[join of simplicial sets]] of $N(E)$ with the [[point]]. 

By the general yoga of [[homotopy colimit]]s (see there for details) we know that this $\infty$-pushout here may be computed as an ordinary [[pushout]] in the 1-category [[sSet]] if the pushout diagram $N(C) \leftarrow N(E) \to N(E)^{\triangleright} $ has the property that

* all three objects are cofibrant;

* at least one of the two morphisms is a cofibration

in the [[model structure for quasi-categories]] $sSet_{Joyal}$.

But this is trivially verified since the cofibrations in $sSet_{Joyal}$ are just the [[monomorphism]]s in [[sSet]]: the degreewise injective maps of simplicial sets. So every object in $sSet_{Joyal}$ is cofibrant and the inclusion $N(E) \hookrightarrow N(E)^{\triangleright}$ is a cofibration. 

(The same conclusion would hold for the same simple reasons in the standard [[model structure on simplicial sets]] $sSet_{Quillen}$.)

From this it follows that simply because we passed from categories to their [[nerve]]s, the computation of the weak pushout reduces to the computation of an ordinary pushout (one may think of passing to nerves as providing a cofibrant replacement: since in the nerve all composition of [[k-morphism]]s is "freed", the nerve is a suitably "puffed up" version of a category that is suitable for computing $\infty$-pushouts).

So we are reduced to computing the ordinary [[pushout]]

$$
  \array{
    N(E) &\hookrightarrow& N(E)^{\triangleright}
    \\
    \downarrow^{\mathrlap{N(p)}} && \downarrow
    \\
    N(C) &\to& Q
  }
$$
 
in [[sSet]]. The fibrant replacement of $Q$ is then the [[nerve]] of [[generalized the|the]] [[bicategory]] $K(p)$ that we are after.

As recalled at [[limits and colimits by example]] in the section [limits in presheaf categories](http://ncatlab.org/nlab/show/limits+and+colimits+by+example#limitsinpresheafcat), [[colimit]]s (and hence pushouts) in the [[presheaf]]-category [[sSet]] $= Func(\Delta^{op}, Set)$ are computed for each object $[n] \in \Delta$ as ordinary colimits in [[Set]].

For **$n=0$** we see that $Q_0$ is the collection 0-cells in the image of $p$ 

$$
 Q_0 = N(C)_0  \coprod \{ v\} = p(Obj(E)) \coprod \{v \}
$$

is the collection of objects of $C$ in the image of $p$ and one additional vertex $v$.

For **$n=1$**  similarly we find that $Q_1$ consists of the 1-cells in the image of $p$ and in addition of one 1-cell $e : c \to v$ for each $e \in Obj(E)$ with $p(e) = c$ (this 1-cell is really the terminal 1-cell $e \to v$ in $E^{\triangleright}$ but with its source re-interpreted as being $p(e) = c$ according to the identification of $Q_0$ as above). In the fibrant replacement of $Q$ the composite of original 1-cells $c_1 \to c_2$ and the new 1-cells $e : c_2 \to v$ will be freely added, so that the general 1-morphism $c_1 \to v$ will consist of a 1-morphism $c_1 \to c_2$ in $C$ together with a lift of $c_2$ to $E$. This is just as in the [[comma category]] $c/p$.

For **$n=2$** we have in $Q_2$ the 2-cells in the image of $p$ as well as one 2-cell

$$
  \array{
    c_1 &&\to&& c_2
    \\
    & \searrow &{}^{(e_1 \to e_2)}\swArrow& \swarrow
    \\
    && v
  }
$$

for each 1-cell $(e_1 \to e_2)$ in $N(E)$ with $p(e_1 \to e_2)$ = $(c_1 \to c_2)$.

In particular this means that if $e_2: c_2 \to v$ is a morphism in $Q$ and $c_1 \to c_2$ is a morphism in $C$, then the composite $c_1 \to c_2 \to v$ in $Q$ is homotopic to any compatible direct morphism $c_1 \to v$ in $Q$.

This means that forming the fibrant replacement of $Q$ in $sSet_{Joyal}$ will not throw in superfluous 1-morphisms on top of those we already discussed in the previous paragraph...


Now furthermore...

=--


This formulation of the Grothendieck construction as an adjunction

$$
  (L \dashv \int) : Fib(C) \stackrel{\leftarrow}{\to} [C^{op}, Cat]
$$

with the left adjoint given by hom-objects in a pushout object as above
is the starting point for the [[vertical categorification]] described at [[(∞,1)-Grothendieck construction]]. 




## Generalizations 

### $n = 0$ 

The analog of the Grothendieck construction one categorical dimension down is the [[category of elements]] of a [[presheaf]].

### $n = (\infty,1)$  {#(oo1)case}

The analog of the Grothendieck construction for [[(infinity,1)-category|(∞,1)-categories]] is described at [[Cartesian fibration]] and at [[universal fibration of (∞,1)-categories]]. 

The correspondence between $(\infty,1)$-categorical [[cartesian fibrations]] $E \to C$ and [[(infinity,1)-presheaf|(∞,1)-presheaves]] $C \to (\infty,1)Cat^{op}$ is [[model category|modeled]] by the [[Quillen equivalence]] between the [[model structure on marked simplicial over-sets]] and the projective [[global model structure on simplicial presheaves]].

For more details see

* [[(∞,1)-Grothendieck construction]]


## Warning on terminology ##

The term 'Grothendieck Construction' is applied in the literature to at least two very different constructions (and as [[Alexander Grothendieck|Grothendieck]] introduced so many new ideas and constructions to mathematics, perhaps there are others!). One concerns the construction of a [[fibered category]] from a [[pseudofunctor]] and will be treated in more detail in the entry on [[Grothendieck fibration]].  The other referes to constructing the [[Grothendieck group]] is  in the context of [[K-theory]] from isomorphism classes of vector bundles on a space by the introduction of formal inverses, 'virtual bundles'.  This constructs an Abelian group from the semi-group of isomorphism classes.




##References##

* [Grothendieck construction](http://en.wikipedia.org/wiki/Grothendieck_construction) (Wikipedia)
* [The Grothendieck Construction](http://online.itp.ucsb.edu/online/ktheory/wu/) (UCSB ITP Seminar)
* [The Homotopy Theory of n-Fold Categories](http://www.math.uchicago.edu/~fiore/1/ThomasonNFoldBeamerSlides.pdf)
* [Inference System Integration via Logic Morphisms](http://www.kestrel.edu/home/projects/logicware/slides-9806/sld001.htm)
* [Category Theory for Computing Science](http://www.cwru.edu/artsci/math/wells/pub/ctcs.html)
