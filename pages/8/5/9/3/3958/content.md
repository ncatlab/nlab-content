
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea


A [[differentiable manifold]] is a [[topological space]] which is _locally_ [[homeomorphism|homeomorphic]] to a [[Euclidean space]] (a [[topological manifold]]) and such that the [[gluing functions]] which relate these Euclidean [[local charts]] to each other are [[differentiable functions]], for a fixed degree of differentiability. If one considers arbitrary differentiablity, then one speaks of _smooth manifolds_. For a general discussion see at _[[manifold]]_.


Differential and smooth manifolds are the basis for much of [[differential geometry]]. They are the analogs in differential geometry of what [[schemes]] are in [[algebraic geometry]].

If one relaxes the condition from being locally isomorphic to a Euclidean space to admitting local smooth maps from a Euclidean space, then one obtains the concept of [[diffeological spaces]] or even [[smooth sets]], see at _[[generalized smooth space]]_ for more on this.

The generalization of differentiable manifolds to [[higher differential geometry]] are [[orbifolds]] and more generally [[differentiable stacks]]. If one combines this with the generalization to [[smooth sets]] then one obtains the concept of [[smooth stacks]] and eventually [[smooth infinity-stacks]].

Smooth manifolds form a category, [[SmoothManifolds]].

## Definition

### Traditional definition

For the traditional definition see at _[[differentiable manifold]]_.

### Patching as idempotent splitting

In an exercise of his 1973 Perugia lectures [[F. William Lawvere]] reported a somewhat surprising observation:

In the case of [[smooth manifolds]] the process of piecing together the local data can be elegantly summed up as [[Karoubi envelope|splitting of idempotents]] in a category of open subsets of Euclidean spaces. More precisely:

Let $Diff$ be the category of [[smooth manifolds]] and [[smooth maps]], where by a "smooth manifold", we mean a finite-dimensional, second-countable, Hausdorff, $C^\infty$ [[manifold]] without boundary.  Let $i: Open \hookrightarrow Diff$ be the [[full subcategory]] whose objects are the [[open subspaces]] of finite-dimensional [[Cartesian spaces]]. 

+-- {: .num_theorem} 
###### Theorem 
The subcategory $i: Open \hookrightarrow Diff$ exhibits $Diff$ as an idempotent-splitting completion of $Open$. 
=-- 

+-- {: .proof} 
###### Proof 
By a general [[Karoubi envelope#def2|lemma for idempotent splittings]], it suffices to prove that 

* Every smooth manifold is a smooth retract of an open set in Euclidean space; 

* If $p : U \to U$ is a smooth idempotent on an open set $U \subseteq \mathbb{R}^n$, then the subset $Fix(p) \hookrightarrow U$ is an [[embedding of smooth manifolds|embedded]] submanifold. 

For the first statement, we use the fact that any manifold $M$ can be realized as a closed submanifold of some $\mathbb{R}^n$, and every closed submanifold has a [[tubular neighborhood theorem|tubular neighborhood]] $U \subseteq \mathbb{R}^n$. In this case $U$ carries a structure of vector bundle over $M$ in such a way that the inclusion $M \hookrightarrow U$ is identified with the zero section, so that the bundle projection $U \to M$ provides a retraction, with right inverse given by the zero section. 

For the second statement, assume that the origin $0$ is a fixed point of $p$, and let $T_0(U) \cong \mathbb{R}^n$ be its tangent space (observe the presence of a _canonical_ isomorphism to $\mathbb{R}^n$). Thus we have idempotent linear maps $d p(0), Id-d p(0): T_0(U) \to T_0(U)$ where the latter factors through the inclusion $\ker \; d p(0) \hookrightarrow T_0(U)$ via a projection map $\pi: T_0(U) \to \ker \; d p(0)$. We have a map $f: U \to \mathbb{R}^n$ that takes $x \in U$ to $x - p(x)$; let $g$ denote the composite 

$$U \stackrel{f}{\longrightarrow} \mathbb{R}^n \cong T_0(U) \stackrel{\pi}{\longrightarrow} \ker\; d p(0).$$ 

Now we make some easy observations: 

1. $Fix(p) \subseteq g^{-1}(0)$. 

1. The map $p: U \to U$ restricts to a map $p: g^{-1}(0) \to g^{-1}(0)$, by idempotence of $p$. 

1. The derivative $d g(0): T_0(U) \to T_0(\ker \; d p(0)) \cong \ker \; d p(0)$ is $\pi$ again since $Id - d p(0)$ is idempotent. Thus $d g(0)$ has full rank ($m$ say), and so the restriction of $g$ to some neighborhood $V$ has $0$ as a regular value, and $g^{-1}(0) \cap V$ is a manifold of dimension $m$ by the [[implicit function theorem]]. The tangent space $T_0(g^{-1}(0) \cap V)$ is canonically identified with $im(d p(0))$. 


1. There are smaller neighborhoods $V'' \subseteq V' \subseteq V$ so that $p$ restricts to maps $p_1, p_2$ as in the following diagram ($i, i', i''$ are inclusion maps, all taking a domain element $x$ to itself): 
$$\array{
g^{-1}(0) \cap V'' & \stackrel{i''}{\hookrightarrow} & g^{-1}(0) \\ 
 _\mathllap{p_2} \downarrow & & \downarrow _\mathrlap{p} \\ 
g^{-1}(0) \cap V' & \stackrel{i'}{\hookrightarrow} & g^{-1}(0) \\ 
 _\mathllap{p_1} \downarrow & & \downarrow _\mathrlap{p} \\ 
g^{-1}(0) \cap V & \stackrel{i}{\hookrightarrow} & g^{-1}(0)
}$$ 
and such that $p_1, p_2$ are diffeomorphisms by the [[implicit function theorem|inverse function theorem]] (noting here that $d p_i(0): im(d p(0)) \to im(d p(0))$ is the identity map, by idempotence of $p$). 

1. Letting $q: g^{-1}(0) \cap V' \to g^{-1}(0) \cap V''$ denote the smooth inverse to $p_2$, we calculate $i' = p \circ i'' \circ q$, and 
$$i p_1 = p i' = p p i''q = p i'' q = i',$$ 
so that $p_1(x) = x$ for every $x \in g^{-1}(0) \cap V'$. Hence $g^{-1}(0) \cap V' \subseteq Fix(p)$. 

From all this it follows that $Fix(p) \cap V' = g^{-1}(0) \cap V'$, meaning $Fix(p)$ is locally diffeomorphic to $\mathbb{R}^m$, and so $Fix(p)$ is an embedded submanifold of $\mathbb{R}^n$. 
=--

+-- {: .num_remark} 
###### Remark 
Another proof of this result may be found [here](http://www.mat.univie.ac.at/~michor/dgbook.pdf). 
=-- 

[[F. William Lawvere|Lawvere]] comments on this fact as follows:
 
> {#LawvereComment} "This powerful theorem justifies bypassing the complicated considerations of charts, coordinate transformations, and atlases commonly offered as a "basic" definition of the concept of manifold. For example the 2-sphere, a manifold but not an open set of any Euclidean space, may be fully specified with its smooth structure by considering any open set $A$ in 3-space $E$ which contains it but not its center (taken to be $0$) and the smooth idempotent endomap of $A$ given by $e(x) = x/{|x|}$. All general constructions (i.e., functors into categories which are Cauchy complete) on manifolds now follow easily (without any need to check whether they are compatible with coverings, etc.) provided they are known on the opens of Euclidean spaces: for example, the tangent bundle on the sphere is obtained by splitting the idempotent $e'$ on the tangent bundle $A \times V$ of $A$ ($V$ being the vector space of translations of $E$) which is obtained by differentiating $e$. The same for cohomology groups, etc."  ([Lawvere 1989](#Law89), p.267)


### General abstract geometric definition
 {#GeneralAbstractCharacterization}

There is a fundamental and [[category theory|general abstract]] way to think of smooth manifolds, which realizes their theory as a special case of general constructions in [[higher geometry]]. 

In this context one specifies for instance $\mathcal{G}$ a [[geometry (for structured (∞,1)-toposes)]] and then plenty of geometric notions are defined canonically in terms of $\mathcal{G}$. The theory of smooth manifolds appears if one takes $\mathcal{G} = $ [[CartSp]]. 

Alternatively one can specify [[differential cohesion]] and proceed as discussed at _[differential cohesion -- structures - Cohesive manifolds (separated)](cohesive+%28infinity%2C1%29-topos+--+infinitesimal+cohesion#CohesivemanifoldsSeparated)_.

This is discussed in [The geometry CartSp](#TheGeometryCartSp) below.



#### The geometry $CartSp$ {#TheGeometryCartSp}

Let [[CartSp]] be the [[category]] of [[Cartesian space]]s and [[smooth function]]s between them. This has finite [[product]]s and is in fact (the [[syntactic category]]) of a [[Lawvere theory]]: the theory of [[smooth algebras]].

Moreover, $CartSp$ is naturally equipped with the [[good open cover]] [[coverage]] that makes it a [[site]]. 

Both properties together make it a [[pregeometry (for structured (∞,1)-toposes)]] (if the notion of [[Grothendieck topology]] is relaxed to that of [[coverage]] in [StrSp](#StrSp)).

For $\mathcal{X}$ a [[topos]], a [[product]]-preserving [[functor]]

$$
  \mathcal{O} : \mathcal{G} \to \mathcal{X}
$$

is a $\mathcal{G}$-[[algebra over an algebraic theory|algebra]] in $\mathcal{X}$. This makes $\mathcal{X}$ is $\mathcal{G}$-[[ringed topos]]. For $\mathcal{G} = $ [[CartSp]] this algebra is a [[smooth algebra]] in $\mathcal{X}$. If $\mathcal{X}$ has a [[site]] of definition $X$, then this is a [[sheaf]] of [[smooth algebra]]s on $X$. 

If $\mathcal{O}$ sends [[covering]] families $\{U_i \to U\}$ in $\mathcal{G}$ to [[effective epimorphism]] $\coprod_i \mathcal{O}(U_i) \to \mathcal{O}(U)$ we say that it is a _local $\mathcal{G}$-algebra_ in $\mathcal{X}$, making $\mathcal{X}$ a $\mathcal{G}$-[[locally ringed topos]].

The [[big topos]] $Sh(\mathcal{G})$ itself is canonically equipped with such a local $\mathcal{G}$-algebra, given by the [[Yoneda embedding]] $j$ followed by [[sheafification]] $L$

$$
  \mathcal{O} : \mathcal{G} \stackrel{j}{\to} PSh(\mathcal{G}) \stackrel{L}{\to}
  Sh(\mathcal{G})
  \,.
$$

It is important in the context of [[locally representable structured (infinity,1)-topos|locally representable locally ringed toposes]] that we regard $Sh(\mathcal{G})$ as equipped with this local $\mathcal{G}$-algebra. This is what remembers the [[site]] and gives a notion of local representability in the first place.

The [[big topos]] $Sh(CartSp)$ is a [[cohesive topos]] of [[generalized smooth space]]s. Its [[concrete sheaves]] are precisely the [[diffeological space]]s. See there for more details. We now discuss how with $Sh(CartSp)$ regarded as a $CartSp$-structured topos, smooth manifolds are precisely its [[locally representable structured (infinity,1)-toposes|locally representable objects]].

#### Cartesian spaces as representable objects of $Sh(CartSp)$

The representables themselves should evidently be locally representable and canonically have the structure of $CartSp$-structured toposes.

Indeed, every object $U \in \mathrm{CartSp}$ is canonically a [[CartSp]]-[[ringed space]], meaning a [[topological space]] equipped with a local sheaf of [[smooth algebra]]s. More generally: every object $U \in CartSp$ is canonically incarnated as the $CartSp$-[[structured (∞,1)-topos]] 

$$
  (\mathcal{X}, \mathcal{O}_{\mathcal{X}})
  :=
  (Sh_{(\infty,1)}(CartSp)/U ,
    \;\;\; \mathcal{O}_U : CartSp \stackrel{j}{\to} Sh_{(\infty,1)}(CartSp) \stackrel{U^*}{\to} Sh_{(\infty,1)}(CartSp)/U)
$$ 

given by the [[over-(∞,1)-topos]] of the [[big topos|big]] [[(∞,1)-sheaf (∞,1)-topos]] over $CartSp$ and the [[structure sheaf]] given by the composite of the [[(∞,1)-Yoneda embedding]] and the [[inverse image]] of the [[etale geometric morphism]] induced by $U$.


#### Smooth manifolds as locally representable objects of $Sh(CartSp)$ {#smoothManifoldsAsLocallyRepresentableObjects}

+-- {: .num_defn}
###### Definition

Say a [[concrete sheaf|concrete object]] $X$ in the [[sheaf topos]] $Sh(CartSp)$ -- a [[diffeological space]] -- is _locally representable_ if there exists a family of open embeddings $\{U_i \hookrightarrow X\}_{i \in X}$ with $U_i \in CartSp \stackrel{j}{\hookrightarrow} Sh(CartSp)$ such that the canonical morphism out of the [[coproduct]]

$$
  \coprod_i U_i \to X
$$

is an [[effective epimorphism]] in $Sh(CartSp)$.

Let $LocRep(CartSp) \hookrightarrow Sh(CartSp)$ be the full [[subcategory]] on locally representable sheaves.

=--

+-- {: .num_prop}
###### Proposition

There is an [[equivalence of categories]]

$$
  Diff \simeq LocRep(CartSp)
$$


of the category [[Diff]] of smooth manifolds with that of locally representable sheaves for the [[geometry (for structured (infinity,1)-toposes)|pre-geometry]] $CartSp$.

=--


+-- {: .proof}
###### Proof


Define a functor $Diff \to LocRep(CartSp)$ by sending each smooth manifold to the sheaf over $CartSp$ that it naturally represents. By definition of [[manifold]] there is an [[open cover]] $\{U_i \hookrightarrow X\}$. We claim that $\coprod_i U_i \to X$ is an [[effective epimorphism]], so that this functor indeed lands in $LocRep(CartSp)$. (This is a standard argument of sheaf theory in [[Diff]], we really only need to observe that it goes through over [[CartSp]], too.)

For that we need to show that

$$
  \coprod_{i, j} U_i \times_X U_j \stackrel{\longrightarrow}{\longrightarrow} \coprod_i U_i \to X
$$

is a [[coequalizer]] diagram in $Sh(CartSp)$ (that the [[Cech groupoid]] of the cover is equivalent to $X$.). Notice that the [[fiber product]] here is just the intersection in $X$ $U_i \times_X U_j \simeq U_i \cap U_j$. By the fact that the [[sheaf topos]] $Sh(CartSp)$ is by definition a [[reflective subcategory]] of the [[presheaf topos]] $PSh(CartSp)$ we have that [[colimit]]s in $Sh(CartSp)$ are computed as the [[sheafification]] of the corresponding colimit in $PSh(CartSp)$. The colimit in $PSh(CartSp)$ in turn is computed objectwise. Using this, we see that that we have a coequalizer diagram

$$
  \coprod_{i, j} U_i \times_X U_j \stackrel{\longrightarrow}{\longrightarrow} \coprod_i U_i \to S(\{U_i\})
$$

in $PSh(CartSp)$, where $S(\{U_i\})$ is the [[sieve]] corresponding to the cover: the [[subfunctor]] $S(\{U_i\}) \hookrightarrow X$ of the functor $X : CartSp^{op} \to Set $ which assigns to $V \in CartSp$ the set of [[smooth function]]s $V \to X$ that have the property that they factor through any one of the $U_i$.

Essentially by the definition of the [[coverage]] on $CartSp$, it follows that [[sheafification]] takes this subfunctor inclusion to an [[isomorphism]]. This shows that $X$ is indeed the tip of the coequalizer in $Sh(CartSp)$ as above, and hence that it is a locally representable sheaf.

Conversely, suppose that for $X \in Conc(Sh(CartSp)) \hookrightarrow Sh(CartSp)$ there is a family of open embeddings $\{U_i \hookrightarrow X\}$ such that we have a coequalizer diagram

$$
  \coprod_{i, j} U_i \times_X U_j \stackrel{\longrightarrow}{\longrightarrow} \coprod_{i} U_i \to X
$$

in $Sh(CartSp)$, which is the sheafification of the corresponding coequalizer in $PSh(CartSp)$. By evaluating this on the point, we find that the underlying set of $X$ is the coequalizer of the underlying set of the $U_i$ in $Set$. Since every plot of $X$ factors locally through one of the $U_i$ it follows that $X$ is a [[diffeological space]].  

It follows that in the pullback diagrams

$$
  \array{
    U_i \times_X U_j &\to& U_j
   \\
    \downarrow && \downarrow
   \\
   U_i &\to& X 
  }
$$

the object $U_i \cap U_j$ is the diffeological space whose underlying topological space is the intersection of $U_i$ and $U_j$ in the topological space underlying $X$. In particular the inclusions $U_i \times_X U_j \hookrightarrow U_i$ are open embeddings. 

=--

#### As locally representable $CartSp$-structured $(\infty,1)$-toposes

We may switch from regarding smooth manifolds as objects in the [[big topos]] $X \in Sh(CartSp)$ to regrading them as [[topos]]es themselves, by passing to the [[over-topos]] $Sh(CartSp)/X$. This remembers the extra (smooth) structure on the [[topological space]] $X$ by being canonically a [[locally ringed topos]] with the [[structure sheaf]] of [[smooth function]]s on $X$: a [[CartSp]]-[[structured (∞,1)-toposes]]


For every choice of [[geometry (for structured (∞,1)-toposes)]]   there is a notion of $\mathcal{G}$-[[locally representable structured (∞,1)-topos]] ([StrSp](#StrSp)). 

+-- {: .num_prop}
###### Claim

Smooth manifolds are equivalently the [[n-localic (infinity,1)-topos|0-localic]] [[CartSp]]-[[generalized scheme]]s of locally finite presentation.

=--

+-- {: .proof}
###### Sketch of proof

The statement says that a smooth manifold $X$ may be identified with an [[∞-stack]] on [[CartSp]] (an [[∞-Lie groupoid]]) which is represented by a [[CartSp]]-[[structured (∞,1)-topos]] $(\mathcal{X}, \mathcal{O}_{\mathcal{X}})$ such that

1. $\mathcal{X}$ is a [[n-localic (∞,1)-topos|0-localic (∞,1)-topos]];

1. There exists a family of objects $\{U_i \in \mathcal{X}\}$ such that the canonical morphism $\coprod_i U_i \to *_{\mathcal{X}}$ to the [[terminal object in an (∞,1)-category|terminal object]] in $\mathcal{X}$ is a [[regular epimorphism]];

1. For every $i \in I$ there is an equivalence

  $$
    (\mathcal{X}/U_i, \mathcal{O}_{\mathcal{X}|U_i})
    \underoverset{\simeq}{t_i}{\to} (Sh_{(\infty,1)}(\mathbb{R}^n), \mathcal{O}(\mathbb{R}^n))
     \,.
  $$

The second and third condition say in words that $(\mathcal{X}, \mathcal{O}_{\mathcal{X}})$ is locally equivalent to the ordinary cannonically [[CartSp]]-[[locally ringed space]] $\mathbb{R}^n$ (for $n \in \mathbb{N}$ the [[dimension]]. The first condition then says that these local identifications cover $\mathcal{X}$.

(...)

(...)


=--

## Properties

### Faithful embedding into $cAlg^{op}$

+-- {: .num_prop}
###### Proposition
**(Milnor's exercise)**

The [[functor]]

$$
  C^\infty(-) \colon SmthMfd \hookrightarrow cAlg_{\mathbb{R}}^{op}
$$

(from the category of smooth manifolds to the [[opposite category]] of [[commutative algebras]] over the [[real numbers]]) that sends a smooth manifold $X$ to its commutative $\mathbb{R}$-[[associative algebra|algebra]] of [[smooth functions]] $X \to \mathbb{R}$ is a [[fully faithful functor]], hence exhibits $SmthMfd$ as a [[full subcategory]] of $cAlg^{op}$.

=--

([Kolar-Slovak-Michor 93, lemma 35.8, corollaries 35.9, 35.10](#KolarSlovakMichor93))

For more see at _[[embedding of smooth manifolds into formal duals of R-algebras]]_.

### Further properties

* [[Borel's theorem]]

* [[Tietze extension theorem]]

* [[Whitney extension theorem]]

* [[Steenrod-Wockel approximation theorem]]

* [[derivations of smooth functions are vector fields]]


## Classes of examples

* [[CR manifold]]

* [[symplectic manifold]]

* etc.

## Related concepts


* [[embedding of smooth manifolds]]

* [[infinite dimensional smooth manifold]]

* [[pro-manifold]]

* [[diffeological space]], [[smooth set]]

* [[orbifold]]

* [[differentiable stack]], [[smooth stack]], [[smooth infinity-stack]]


* [differential cohesion -- structures - Cohesive manifolds (separated)](cohesive+%28infinity%2C1%29-topos+--+infinitesimal+cohesion#CohesivemanifoldsSeparated)



## References

The original works include

\bibitem{VeblenWhitehead1931}

\bibitem{VeblenWhitehead1932}

\bibitem{Whitney1936}



Early account with an eye towards [[cobordism theory]] and the [[Pontrjagin-Thom isomorphism]]:

* {#Pontrjagin55} [[Lev Pontrjagin]], _Smooth manifolds and their applications in Homotopy theory_, Trudy Mat. Inst. im Steklov, No 45, Izdat. Akad. Nauk. USSR, Moscow, 1955 (AMS Translation Series 2, Vol. 11, 1959) ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/pont4.pdf), [doi:10.1142/9789812772107_0001](https://www.worldscientific.com/doi/abs/10.1142/9789812772107_0001))


Textbook accounts:

* {#MilnorStasheff74} [[John Milnor]], [[James Stasheff]], Section 1 of: _Characteristic Classes_, Annals of Mathematics Studies, Princeton University Press 1974 ([ISBN:9780691081229](https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes-am-76-volume-76))


* {#KolarSlovakMichor93} [[Ivan Kolar]], [[Jan Slovak]] and [[Peter Michor]], _Natural operations in differential geometry_, 1993, 1999 ([web](http://www.emis.de/monographs/KSM/))

* {#Kosinski93} [[Antoni Kosinski]], _Differential manifolds_, Academic Press 1993 ([pdf](http://www.maths.ed.ac.uk/~v1ranick/papers/kosinski.pdf))


* {#Lee12} [[John Lee]], _Introduction to Smooth Manifolds_, Springer 2012 ([doi:10.1007/978-1-4419-9982-5](https://doi.org/10.1007/978-1-4419-9982-5), [book webpage](https://sites.math.washington.edu/~lee/Books/ISM/), [pdf](https://lost-contact.mit.edu/afs/adrake.org/usr/rkh/Books/books/Introduction%20to%20Smooth%20Manifolds%20-%20J.%20Lee.pdf))

* [[Theodore Frankel]], chapter 1 of _[[The Geometry of Physics - An Introduction]]_, Cambridge University Press (1997, 2004, 2012)

* Jet Nestruev, _Smooth Manifolds and Observables_ , Springer LNM **220** Heidelberg 2003 ([doi:10.1007/b98871](https://link.springer.com/book/10.1007/b98871))




With an eye towards application in [[mathematical physics]]:

* [[Mikio Nakahara]], Chapter 3 of _[[Geometry, Topology and Physics]]_, IOP 2003 ([doi:10.1201/9781315275826](https://doi.org/10.1201/9781315275826), <a href="http://alpha.sinp.msu.ru/~panov/LibBooks/GRAV/(Graduate_Student_Series_in_Physics)Mikio_Nakahara-Geometry,_Topology_and_Physics,_Second_Edition_(Graduate_Student_Series_in_Physics)-Institute_of_Physics_Publishing(2003).pdf">pdf</a>)


Smooth manifolds are defined as locally ringed spaces in

* Juan A. Navarro Gonz&#225;lez, and Juan B. Sancho de Salas, _$C^\infty$-Differentiable Spaces_, Springer LNM **1824** 2003.

Discussion of smooth manifolds as colimits of the Cech nerves of their good open covers is also at 

* MathOverflow, _[Gluing of manifolds and the Hausdorff condition](http://mathoverflow.net/questions/65684/gluing-of-manifolds-and-the-hausdorff-condition)_

The general abstract framework of [[higher geometry]] referred to above is discussed in 

* {#StrSp} [[Jacob Lurie]], _[[Structured Spaces]]_


The proof that idempotents split in the category of smooth manifolds was adapted from this MO answer: 

* Zack (http://mathoverflow.net/users/300/zack), Idempotents split in category of smooth manifolds?, URL (version: 2014-04-06): http://mathoverflow.net/q/162556 ([web](http://mathoverflow.net/a/162556/2926)) 

Which provides a solution to exercise 3.21 in

* [[William Lawvere]], _Perugia Notes - Theory of Categories over a Base Topos_ , Ms. Universit&#224; di Perugia 1973.

The [above comment](#LawvereComment) by Lawvere is taken from 

* {#Law89}  [[F. William Lawvere]], _Qualitative distinctions between some toposes of generalized graphs_, Contemporary Mathematics 92 (1989), 261-299. ([pdf](http://conceptualmathematics.files.wordpress.com/2013/01/toposesofgeneralizedgraphs.pdf)) 


[[!redirects smooth manifolds]]