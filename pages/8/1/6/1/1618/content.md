# The points of a topos #
* tic
{: toc}


## Definition ##

A **point $x$ of a [[topos]] $E$** is a [[geometric morphism]]
$$
  x : Set \to E
  \,.
$$

That is, it\'s a [[global element]] of the topos.

+--{.query}
Zoran: now one can redefine easily each functor by taking isomorphic representatives. So, in this definition one clearly does not count isomorphic geometric morphisms, or instead of adjoint functors takes classes of isomorphisms of them. Right ? 

Todd: How much does it matter? It matters if for example you want to say that points of $Sh(X)$, $X$ a sober space, are in bijection with points of $X$. Otherwise one can just refer back to equivalence of categories, unless you see a problem with that. 

[[Mike Shulman]]: I would argue that "a point" of a topos really should mean "a geometric morphism from $Set$," *not* "an isomorphism class of geometric morphisms from $Set$," for the same reason that "a group" means, well, "a group" and not "an isomorphism class of groups."  Following from that, I would say that it's not really correct to say that points of $Sh(X)$ (for $X$ sober) are in bijection with $X$, but rather that the category of points of $Sh(X)$ is equivalent to the category of points of $X$.  Note that that's actually a stronger statement than saying that their sets of isomorphism classes of objects are in bijection.

[[Zoran Škoda]]: I want to use reconstruction theorems to get some geometric spaces; I need really to get points of underlying spaces without multiplicities! The equivalence is not satisfactory for my purposes, as I would like to use the (more general situations) in which one has some category $T$ of nice categories (e.g. abelian, topoi etc.) with a subcategory $A'$, where the morphisms are adjoint functors with possibly additional properties; possibly I want to pass to a comma category of the whole thing, for a specific object (the reasons for that are very specific and somewhat nontrivial, having to do with affinity of morphisms). Then I have an equivalence of categories between $A'$ and some category of local or test objects $NAff$, which is in my examples some category of noncommutative algebras. Then I look at categories in $T$ which are obtained from gluing objects in $A'$, where gluing is via descent using say localizations with some flatness properties; this way I get some bigger category $A''$. I do not assume that the localizations commute, i.e. the covers are more general than in the picture of Grothendieck topologies. Then I want to say that $A''$ are represented by some class of presheaves on $NAff$. For that I need to look at morphisms from objects in $A'$ to objects in $A''$ without spurious multiplicity. Of course I can look at 2-Yoneda and getting some presheaf of categories on $A'$ and then afterwards try to decategorify to get down to a presheaf of sets on $A$. I do not know what is the best approach. Any advice ?

[[Mike Shulman]]: It sounds to me like you want to prove that the resulting (pseudo) presheaves of categories are essentially discrete, and hence are equivalent to presheaves of sets.

[[Urs Schreiber]]: yes, I think, too, that this is what Zoran is talking about. I think effectively he has the setup discussed at [notions of space](http://ncatlab.org/nlab/show/A+Survey+of+Elliptic+Cohomology+-+the+derived+moduli+stack+of+derived+elliptic+curves#notions_of_space_4) only that there $(\infty,1)$-toposes are usesd in place where Zoran wants to use abelian categories, $A_\infty$-categories and eventually stable $\infty$-categories as formal duals of spaces.

In that context, Mike: how do I see that the category $[Set,T]_{geom}$ of geometric topos morphisms with natural transformations between them is equivalent to a set?

[[Mike Shulman]]: It depends on what $T$ is.  For an arbitrary topos $T$, of course $[Set,T]_{geom}$ will not be equivalent to a set.  What sort of $T$ are you considering?

[[Zoran Škoda]]: My main examples are not in topos theory, but I would like to see the way similar proofs work. Instead of 2cat of topoi I need to consider certain slice 2cat of abelian categories. More precisely, start with a 2cat $pCT$ whose objects are pairs $(a,O)$ where $a$ is an abelian category and $O$ an object in $a$; the morphisms are pairs of additive adjoint functors (no additional assumptions at start) together with maps $O'\to f_* O$. The slice category is over a category $k-Mod$ where $k$ is a fixed unital ring, commutative or not, it does not matter. This is a ground category. The subcategory $A'\subset pCT$ is given by the requirement that the pair of adjoint functors to the ground category is supposed to be affine (the right adjoint is faithful and has its own right adjoint). This forces the objects in sub2category $A'$ to be equivalent to $R-Mod$ for some $k$-ring $R$; the fact that we are in 2-category means that the triangles in slice category commute up to isomorphisms, this nontrivially forces that the maps between two different $R-Mod$ will not be general tensoring with a bimodule but really something coming from a ring map (affine morphisms satisfy such factorization conditions: similarly if $c$ is monadic over $a$ and $b$ over $a$ then $c$ is monadic over $b$ what is a special case of one of the adjoint lifting theorems; monadicity is weaker than affiness. In particular that means that in decategorified version (classes of geometric functors) the morphisms between categories of modules and underlying rings are the same (the Morita morphisms are excluded by the slice category trick). Now I glue such representable functors on $NAff_k = (k-Rings)^op$ like in [[zoranskoda:gluing categories from localizations]]. I can assume that the cover is not only comonadic but in fact forms a [[noncommutative scheme]] of Rosenberg (plus that we work with choice of object $O$ not stated there, though automatic as inverse image of $R$ in $k-Mod$ via the grounding morphism). Now I want to use some decategorification theorem to state that instead of gluing categories $R-Mod$ I can glue representable presheaves $h_X$ with $X = R^op$; notice that localizations do not commute and the consecutive localizations do not form pullbacks, so we do not have stability axiom of Grothendieck topologies. I would like to be able to present all information on the glued category (noncommutative scheme) by a presheaf of sets on $NAff \cong A'$; or understand if I really need presheaf of cats on $NAff$. The strange locality given by localizations should give a subcategory of "sheaves" which is not a topos, but some subcategory of presheaves whose embedding into presheaves has weaker exactness conditions. Notice that while I glue representable presheaves on NAff, the consecutive (double) localizations where I compare them for gluing are NOT representable by objects in NAff, but only in the big ambient slice category of all abelian categories. In commutative case this may happen for nonsemiseparated schemes, but then we have still represent by the locally ringed spaces where we do not deal with 2-categories.
=--


### In sheaf topoi ###

For the special case that $E = Sh(X)$ is the [[category of sheaves]] on a [[category of open subsets]] $Op(X)$ of a [[topological space]] $X$ this notion of point of a topos comes from the ordinary notion of points of $X$.

For notice that

* $Set = Sh(*)$ is simply the [[topos]] of [[sheaf|sheaves]] on a one-[[point]] [[topological space|space]].  

* [[geometric morphisms]] $f : Sh(Y) \to Sh(X)$ between [[category of sheaves|sheaf topoi]] are in a bijection with continuous functions of topological spaces $f : Y \to X$ (denoted by the same letter, by convenient abuse of notation).

It follows that for $E = Sh(X)$ points of $E$ in the sense of points of topoi are in bijection with the ordinary points of $X$.

The action of the [[direct image]] $x^* : Set \to Sh(X)$ and the [[inverse image]] $x_* : Sh(X) \to Set$ of a point $x : Set \to Sh(X)$ of a sheaf topos have special interpretation and relevance:

* The [[direct image]] of a set $S$ under the point $x : {*} \to X$ is, by definition of [[direct image]] the sheaf
  $$
    x_*(S) : (U \subset X) \mapsto S(x^{-1}(U)) = 
    \left\{
      \array{
        S & if x \in U
        \\
        {*} & otherwise
      }
    \right.
  $$
 This is the [[skyscraper sheaf]] $skysc_x(S)$ with value $S$ supported at $X$. (In the first line on the right in the above we identify the set $S$ with the unique sheaf on the point it defines. Notice that $S(\emptyset) = pt$).

* The [[inverse image]] of a sheaf $A$ under the point $x : {*} \to X$ is by definition of [[inverse image]] (see the [[Kan extension]] formula discussed there), the set
  $$
    \begin{aligned}
       x^*(A) & = 
       colim_{{*} \to x^{-1}(V)} A(V)
       \\
       &=
       colim_{V\subset X| x \in V} F(V)
    \end{aligned}
    \,.
  $$
  This is the [[stalk]] of $A$ at he point $x$,
  $$
    x^*(-) = stalk_x(-)
    \,.
  $$

By definition of [[geometric morphisms]], taking the stalk at $x$ is [[left adjoint]] to forming the skyscraper sheaf at $x$:

for all $S \in Set$ and $A \in Sh(X)$ we have
$$
  Hom_{Set}(stalk_x(A), S) \simeq
  Hom_{Sh(X)}(A, skysc_x(S))
  \,.
$$


### In classifying topoi ###

On the other hand, if $E$ is the [[classifying topos]] of a [[geometric theory]] $T$, then a point of $E$ is the same as a model of $T$ in [[Set]].


## Having enough points ##

A [[topos]] is said to have **enough points** if isomorphy can be tested [[stalk]]wise.

More precisely: if it is true that every morphism $f : A \to B$ such that for every point $p$ of the topos the morphism of [[stalks]] $p^* f : p^* A \to p^* B$ is an isomorphism implies already that $f$ itself is an isomorphism.


### Examples ###

* For $X$ any [[topological space]], the  [[category of sheaves|topos of sheaves]] on (the [[category of open subsets]] of) $X$ has enough points: a morphism of sheaves is a mono-/epi-/isomorphism precisely if it is so on every [[stalk]]. 

* Let $Diff$ be a [[small category]] version of the category of smooth manifolds (for instance take it to be the category of manifolds embedded in $\mathbb{R}^\infty$). Then the sheaf topos $Sh(Diff)$ has precisely one point $p_n$ per natural number $n \in \mathbb{N}$ , corresponding to the $n$-ball: the [[stalk]] of a sheaf on $Diff$ at that point is the colimit over the result of evaluating the sheaf on all $n$-dimensional smooth balls.

  This is discussed for instance on p. 36 of 

  * Dan Dugger, _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf))

  in the context of the [[model structure on simplicial presheaves]].


## References ##

section 7.5 of 

* MacLane Moerdijk, [[Sheaves in Geometry and Logic]]


[[!redirects point of topos]]