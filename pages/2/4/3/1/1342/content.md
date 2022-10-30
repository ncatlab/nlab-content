

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea
From the point of view of infinity category theory (nPOV), _descent_ is the study of generalizations of the [[sheaf]] condition on [[presheaf|presheaves]] to presheaves with values in [[higher category theory|higher categories]]. Those higher presheaves that satisfy descent are called [[infinity-stack]]s.

More generally,
**descent theory** studies existence and (non)uniqueness of an object $u$ in a (possibly higher) category $C_X$ provided some "inverse image" functor $f^*:C_X\to C_Y$ which applied to $u$ produces an object in some (possibly higher) category $C_Y$, or a collection of inverse image functors $\{f^*_\alpha:C_X\to C_{Y_\alpha}\}_{\alpha\in I}$ is given. Labels $Y_\alpha$ are considered as labels of local regions, over which objects in $C_{Y_\alpha}$ live and the inverse image functor is considered as some sort of restriction along geometric morphism of spaces from $Y_\alpha\to X$. In favourable cases, the nonuniqueness is parametrized by equipping the object $f^*(u)$ with additional "gluing" data $\xi$. The pair $(f^*(u),\xi)$ is called a __descent datum__, the existence of a reconstruction procedure of $u$ from $(f^*(u),\xi)$ is also called a descent, and it describes the property that the (higher) category of descent data in $C_Y$ is equivalent to the category $C_X$, or at least that it embeds via a canonical fully faithful functor. Descent theory in 1-categorical context has been first formulated by Grothendieck in FGA using pseudofunctors and in [[SGA1]] using fibered categories.

The most important case is when there is a descent (in the sense of [[equivalence of higher categories]]) along an [[inverse image]] functor along every cover of a [[Grothendieck topology]] or its higher analogue; though many cases (for example [[descent in noncommutative algebraic geometry]]) do not fit into this framework. These cases of descent along all covers is also called (higher) stack theory and may be phrased in modern viewpoint as a characterization of $(\infty,1)$-[[(infinity,1)-sheaf|sheaves]] (i.e. $\infty$-[[infinity-stack|stacks]]) among all $(\infty,1)$-[[(infinity,1)-presheaf|presheaves]] as those $(\infty,1)$-presheaves which are [[local objects]] with respect to certain morphisms $Y \to X$ which are to be regarded as [[covers]] or [[hypercover]] of the $(\infty,1)$-presheaf $X$: the idea is that an $(\infty,1)$-sheaf "descends from the cover $Y$ down to $X$".

More concretely 

* every [[(∞,1)-category of (∞,1)-sheaves]] is characterized as being a sub-[[(∞,1)-topos]] $Sh(S) \hookrightarrow PSh(S)$ of the $(\infty,1)$-topos of [[(∞,1)-presheaves]] on some (small) [[(∞,1)-category]] $S$;

* every such $(\infty,1)$-topos is a [[reflective (∞,1)-subcategory]] of $PSh(S)$, hence a [[localization of an (∞,1)-category]] at a collection $W = \{Y \to X\}$ of morphisms which are sent to equivalences by the left adjoint of the inclusion;

* and the sheaves in $Sh(S) \hookrightarrow PSh(S)$ are precisely the [[local objects]] with respect to this collection $W$ of morphisms, i.e. precisely those objects $A \in PSh(S)$ such that $PSh(S)(X,A) \to PSh(S)(Y,A)$ is an isomorphism in the [[homotopy category of an (infinity,1)-category|homotopy category]], which we shall write $PSh(S)(X,A) \stackrel{\simeq}{\to} PSh(S)(Y,A)$ in the following paragraphs.

* This condition is essentially the _descent conditon_.

In concrete models for the [[(∞,1)-category of (∞,1)-sheaves]] -- notably in terms of the [[model structure on simplicial presheaves]] -- the morphisms $Y \to X$ in $W$ usually come from [[hypercovers]]  $Y \to X$;

in this case the above condition becomes $PSh(S)(X,A) \stackrel{\simeq}{\to} PSh(S)(colim^\Delta Y_\bullet, A)$ which is equivalent to $ PSh(S)(X,A) \stackrel{\simeq}{\to} lim^\Delta PSh(S)(Y_\bullet, A) $. This in turn is usually equivalently written 

$$
  A(X) 
  \stackrel{\simeq}{\to} 
   Desc(Y_\bullet \to X, A) 
   := lim^\Delta A(Y_\bullet)
  \,.
$$ 

And this is the form of the [[local object]]-condition which is usually called **descent condition**.



## Descent for ordinary sheaves

Descent is best understood as a direct generalization of the  situation for 0-stacks, i.e. ordinary sheaves, which we briefly  recall in a language suitable for the following generalization.

For $S$ any small [[category]] and [[Set]] the category of small sets, write $\mathrm{PSh}(S) = [S^{op}, Set]$ for the category of [[presheaf|presheaves]] on $S$. Categories of this form enjoy various nice properties which are familiar from $Set$ itself,  and which are summarized by saying that $\mathrm{PSh}(S)$ is a [[topos]]. The relevance of
this for the present purpose is that there is a natural notion of morphisms of topoi, which are [[functors]] respecting this structure in some sense: these are called [[geometric morphisms]].

A [[category of sheaves]] on $S$ is a sub-topos of $PSh(S)$ in that it is a [[full and faithful functor]] $Sh(S)\hookrightarrow PSh(S)$ which is a [[geometric morphism]].

One finds that the [[reflective subcategory]] $Sh(S) \hookrightarrow PSh(S)$ of sheaves inside presheaves is the [[localization]] of $PSh(S)$ at morphisms $f : Y \to X$ called [[local isomorphisms]], which are determined by and determine the choice of topos-inclusion. A [[presheaf]] $A$ is a [[sheaf]] precisely if it is a [[local object]] with respect to these [[local isomorphisms]], that is precisely if

$$
  Hom_{PSh(S)}(X,A) \stackrel{Hom_{PSh(S)}(f,A)}{\to} Hom_{PSh(S)}(Y,A)
$$

is an [[isomorphism]] for all [[local isomorphisms]] $f$.


This locality condition is in fact the _descent_ condition: the sheaf has to descend from $Y$ down to $X$. More concretely, this condition is called a _descent condition_ when evaluated on morphisms $f : Y \to X$ which are [[hypercovers]]: 

namely if $\pi : Y^1 \to X$ is a [[local epimorphism]] with respect to the [[coverage]] that corresponds to the [[localization]] and if $\pi_2 : Y^2 \to Y^1 \times_X Y^1$ is a [[local epimorphism]], then with

$$
  Y^\bullet := (Y^2 \rightrightarrows Y^1)
$$

being the two canonical morphisms out of $Y^2$, it follows that the canonical morphism 

$$
  colim Y^\bullet \to X
$$

is a [[local isomorphism]]. 

(This is exercise 16.6 in [[Categories and Sheaves]]).

Therefore for a  [[presheaf]] $A$ to be a [[sheaf]], it is necessary that

$$
  Hom_{PSh(S)}(X,A) \stackrel{\simeq}{\to} Hom_{PSh(S)}(colim Y^\bullet, A)
$$

is an [[isomorphism]]. The [[colimit]] may be taken out of the [[hom-functor]] to make this equivalently

$$
  Hom_{PSh(S)}(X,A) 
   \stackrel{\simeq}{\to}  
  lim Hom_{PSh(S)}(Y^\bullet, A)
  \,.
$$

It is convenient, suggestive and common to write $A(X) := Hom_{PSh(S)}(X,A)$, $A(Y^\bullet) := Hom_{PSh(S)}(Y^\bullet,A)$, following the spirit of the [[Yoneda lemma]] whether or not $X$ and/or $Y^\bullet$ are [[representable functor|representable]]. In that notation the above finally becomes

$$
  A(X)   
  \stackrel{\simeq}{\to}  
  lim A(Y^\bullet)
  \,.
$$

This is the form of the condition that is most commonly called the _descent condition_.



## Descent for simplicial presheaves 

For more references and background on the following see [[descent for simplicial presheaves]].



A well-studied class of models/presentations for an [[(∞,1)-category of (∞,1)-sheaves]] is obtained using the [[model structure on simplicial presheaves]] on an  ordinary (1-categorical) [[site]] $S$, as follows.

Let $[S^{op}, SSet]$ be the [[SimpSet|SSet]]-[[enriched category]] of [[simplicial presheaf|simplicial presheaves]] on $S$. 

Recall from [[model structure on simplicial presheaves]] that there is the _global_ and the _local_ injective simplicial model structure on $[S^{op}, SSet]$ which makes it a [[simplicial model category]] and that the local model structure is a (Bousfield-)localization of the global model structure.

So in terms of simplicial presheaves the [[localization of an (∞,1)-category]] that we want to describe, namely [[∞-stackification]], is modeled as the [[localization of a simplicial model category]]. 


Recall that the [[(∞,1)-category]] modeled/presented by a [[simplicial model category]] is the full [[SimpSet|SSet]]-subcategory on fibrant-cofibrant objects.
According to [section 6.5.2](http://www.math.harvard.edu/~lurie/papers/highertopoi.pdf#page=528)  of [[Higher Topos Theory|HTT]] we have:

* the full simplicial subcategory on fibrant-cofibrant objects of $[S^{op}, SSet]$ with respect to the _global_ injective model structure is (the [[SimpSet|SSet]]-[[enriched category]] realization of) the $(\infty,1)$-category  $PSh_{(\infty,1)}(S)$ of [[(∞,1)-presheaves]] on $S$.

* the full simplicial subcategory on fibrant-cofibrant objects of $[S^{op}, SSet]$ with respect to the _local_ injective model structure is (the [[SimpSet|SSet]]-[[enriched category]] realization of) the $(\infty,1)$-category  $\bar{Sh}_{(\infty,1)}(S)$ which is the [[hypercompletion]] of the $(\infty,1)$-category $Sh_{(\infty,1)}(S)$ of [[(∞,1)-sheaves]] on $S$.

Since with respect to the local or global injective model structure all objects are automatically cofibrant, this means that $\bar Sh_{(\infty,1)}(S)$ is the full sub-$(\infty,1)$-category of $PSh_{(\infty,1)}(S)$ on simplicial presheaves which are fibrant with respect to the local injective model structure: these are the [[∞-stacks]] in this model.




By the general properties of [[localization of an (∞,1)-category]] there should be a class of morphisms $f : Y \to X$ in $PSh_{(\infty,1)}(S)$ -- hence between injective-fibrant objects in $[S^{op}, PSh(S)]$ -- such that the simplicial presheaves representing $\infty$-stacks are precisely the [[local objects]] with respect to these morphisms.

The general idea of descent in this simplicial context is the precise analog of the situation for ordinary sheaves, but with ordinary [[limit|(co)limits]] replaced everywhere with the [[limit in quasi-categories|(∞,1)-categorical (co)limits]], which in terms of the [[presentable (infinity,1)-category|presentation]] by the [[model structure on simplicial presheaves]] amounts to the [[homotopy limit|homotopy (co)limit]].


So for $Y \to X$ a morphism of simplicial presheaves, the condition that a simplicial presheaf $A$ is [[local object|local]] with respect to it, hence satisfies descent with respect to it, is generally that

$$
  \begin{aligned}
    RHom(X,A)  \stackrel{}{\to} & RHom(Y,A)
    \\
    & \simeq RHom(hocolim_n Y_n, A)
    \\
    & \simeq holim_n RHom(Y_n, A)
    \\
    & =: holim_n A(Y_n)
  \end{aligned}
$$

is a weak equivalence, where $RHom$ denotes the corresponding $(\infty,1)$-categorical hom, i.e. the derived hom with respect to the [[model structure on simplicial presheaves]] -- for instance the ordinary simplicial hom if both $Y$ and $A$ are fibrant with respect to the given model structure.


The details on which morphisms $Y \to X$ one needs to check against here have been worked out in

* D. Dugger, S. Hollander, D. Isaksen, _Hypercovers and simplicial presheaves_ ([pdf](http://hopf.math.purdue.edu//Dugger-Hollander-Isaksen/hypspre.pdf))

We now describe central results of that article.
 
+-- {: .un_defn}
###### Definition

For $X \in S$ an object in the [[site]] regarded as a simplicial presheaf and $Y \in [S^{op}, SSet]$ a simplicial presheaf on $S$, a morphism $Y \to X$ is a **[[hypercover]]** if it is a _local acyclic fibration_, i.e. of for all $V \in S$ and all diagrams
$$
  \array{
    \Lambda^k[n]\otimes V &\to & Y
    \\
    \downarrow && \downarrow
    \\
    \Delta^n\otimes V &\to& 
    X
  }
  \;\; respectively \;\,
  \array{
    \partial \Delta^n\otimes V &\to & Y
    \\
    \downarrow && \downarrow
    \\
    \Delta^n\otimes V &\to& 
    X
  }
$$
there exists a covering  [[sieve]] $\{U_i \to V\}$ of $V$ with respect to the given [[Grothendieck topology]] on $S$ such that for every $U_i \to V$ in that [[sieve]] the pullback of the abve diagram to $U$ has a lift
$$
  \array{
    \Lambda^k[n]\otimes U_i &\to & Y
    \\
    \downarrow &\nearrow & \downarrow
    \\
    \Delta^n\otimes U_i &\to& 
    X
  }
  \;\; respectively \;\,
  \array{
    \partial \Delta^n\otimes U_i &\to & Y
    \\
    \downarrow &\nearrow& \downarrow
    \\
    \Delta^n\otimes U_i &\to& 
    X
  } 
  \,.
$$
=--

If $S$ is a [[Verdier site]] then every such hypercover $Y \to X$ has a refinement by a hypercover which is cofibrant with respect to the projective global [[model structure on simplicial presheaves]]. We shall from now on make the assumption that the hypercovers $Y \to X$ we discuss are cofibrant in this sense. These are called _split hypercovers_. (This works in many cases that arise in practice, see the discussion after [DHI, def. 9.1](http://hopf.math.purdue.edu//Dugger-Hollander-Isaksen/hypspre.pdf#page=29).)

+-- {: .un_prop}
###### Proposition

The objects of $Sh_{(\infty,1)}(S)$ -- i.e. the fibrant objects with respect to the projective model structure on $[S^{op}, SSet]$ -- are precisely those objects $A$ of $PSh_{(\infty,1)}(S)$ -- i.e. [[Kan complex]]-valued simplicial presheaves -- which
**satisfy descent for all split hypercovers**, i.e. those for which for all split hypercover $f : Y \to X$ in $[S^{op}, SSet]$ we have that
$$
  [S^{op}, SSet](X,A) \stackrel{\simeq}{\to}
  [S^{op}, SSet](Y,A)
$$
is a [[model structure on simplicial sets|weak equivalence of simplicial sets]].
=--

+-- {: .proof}
###### Proof

This is [DHI, thm 1.3](http://hopf.math.purdue.edu//Dugger-Hollander-Isaksen/hypspre.pdf#page=3) formulated in the light of [DHI, lemma 4.4 ii)](http://hopf.math.purdue.edu//Dugger-Hollander-Isaksen/hypspre.pdf#page=9).
=--

Notice that by the [[co-Yoneda lemma]] every simplicial presheaf $F : S^{op} \to SSet$, which we may regard as a presheaf $F : \Delta^{op}\times S^{op} \to Set$, is isomorphic to the [[weighted limit|weighted colimit]] 

$$
    F \simeq colim^\Delta F_\bullet
$$

which is equivalently the [[end|coend]]

$$
  F \simeq \int^{[n] \in \Delta} \Delta^n \cdot F_n
  \,,
$$ 

where $F_n$ is the Set-valued presheaf of $n$-cells of $F$ regarded as an $SSet$-valued presheaf under the inclusion $Set \hookrightarrow SSet$, and
where the [[SimpSet|SSet]]-weight is the canonical cosimplicial simplicial set $\Delta$, i.e. for all $X \in S$

$$
  F : X \mapsto \int^{[n] \in \Delta} \Delta^n \times F(X)_n
  \,.
$$

In particular therefore for $A$ a [[Kan complex]]-valued presheaf the descent condition reads

$$
  [S^{op}, SSet](X,A) \stackrel{\simeq}{\to}
  [S^{op}, SSet](colim^\Delta Y_\bullet,A)
  \simeq
  lim^\Delta [S^{op}, SSet](Y_\bullet,A)
  \,.
$$

With the shorthand notation introduced above the **descent condition** finally reads, for all global-injective fibrant simplicial presheaves $A$ and hypercovers $U \to X$:

$$
  A(X) \stackrel{\simeq}{\to} lim^\Delta A(Y_\bullet)
  \,.
$$

The right hand here is often denoted $Desc(Y_\bullet \to X, A)$, in which case this reads

$$
  A(X) \stackrel{\simeq}{\to} Desc(Y_\bullet \to X, A)
  \,.
$$









## Descent for strict $\omega$-groupoid valued presheaves 

While simplicial sets are a very convenient model for general reasoning about higher weak categories and [[∞-groupoids]], often concrete computations in particular with $(\infty)$-groupoids are more convenient in the context of more strictified models. 

Notably, by the generalized [[Dold-Kan correspondence]] the [[oriental|? nerve]] injects [[crossed complex]]es -- nonabelian generalizations of [[chain complex]]es of abelian groups which are equivalent to [[strict ∞-groupoids]] -- to simplicial sets

$$
  CrsCmplx \stackrel{\simeq}{\to}
  Str \omega Grpd \stackrel{N}{\to}
  SSet
  \,.
$$

Since for instance something as simple as an abelian group $A$ regarded as a complex of groups in degree $n$ (hence as an $n$-group) already bcomes a somewhat involved object to understand under the nervet operation, 

_it is desireable to have a means to control descent for simplicial presheaves which happen to factor through the $\omega$-nerve directly in the context of $Str \omega Cat$._


In his work on descent

* Ross Street, _Categorical and combinatorial aspects of descent theory_, [arXiv:math.CT/0303175](http://arxiv.org/abs/math.CT/0303175)

Ross Street considered presheaves with values in [[strict ∞-categories]]

$$
  A : S^{op} \to Str \omega Cat
$$

and declared the descent $\omega$-category with respect to a simplicial object $Y_\bullet : \Delta^{op} \to S$ to be the [[weighted limit]] in $Str\omega-Cat$-[[enriched category theory]]


$$
  lim^{F \Delta} A(U^\bullet) 
  \,,
$$

where $O := F \Delta : \Delta \to Str \omega Cat$ are the [[orientals]], i.e. the free $\omega$-categories on the simplicial [[simplex|simplices]]

$$
  O = F \circ \Delta
  \,,
$$

where $F : SSet \to Str\omega Cat$ is the [[right adjoint]] to the [[oriental|∞-nerve]] $N : Str \omega Cat \to SSet$.

The two precscriptions

$$
 \array{
  lim^\Delta N A(U^\bullet) & in SSet
  \\
  \\
  lim^{F \Delta} A(U^\bullet) & in Str \omega Grpd
 }
$$

have a very similar appearance. The following theorem asserts if and when they are actually equivalent.

+-- {: .un_theorem }
###### Theorem (Dominic Verity)

There exists a canonical comparison map

$$
  N(Desc_{Street}(U^\bullet, A))
  :=
  N(lim^{F \Delta} A(U^\bullet))
  \;\;\;\stackrel{\;\;\;\;\;\;\;\;\;}{\hookrightarrow}\;\;\;
  Desc_{simp}(U^\bullet, N \circ A)
  :=
  holim_\bullet N(A(U^\bullet))
  \,.
$$

This is a [[model structure on simplicial sets|weak equivalence]] of [[Kan complex]]es if the cosimplicial simplicial set $N(A(U^\bullet))$ is [[Reedy category|Reedy fibrant]].

=--

+-- {: .proof}
###### Proof

The full proof is given at [[Verity on descent for strict omega-groupoid valued presheave|Verity on descent for strict omega-groupoid valued presheaves]].

=--

## Descent in terms of gluing conditions {#AsGluing}

We unwrap the expression 

$$
  lim^\Delta A(Y_\bullet)
$$

for the descent data for a presheaf $A$ with respect to a (hyper)cover $Y \to X$


This [[weighted limit]] (whether taken in $SSet$- or in $Str \omega Cat$-[[enriched category theory]]) is given by the [[end|coend]]

$$
  lim^W\Delta A(Y_\bullet)
  \simeq
  \int^{[n] \in \Delta} [\Delta^n, A(Y_n)]
  \,.
$$


Unwrapping what this means one finds that an object/vertex of this is a choice of $n$-simplex in each $A(Y_n)$, subject to conditions which say that the boundary of this $n$-simplex must be obtained from pullback of $A$ along the maps $Y_n \to Y_{[n-1]}$ of the $(n-1)$-simplex in $A(Y_{n-1})$

Namely an object in 

$
  lim^W\Delta A(Y_\bullet)
  \simeq
  \int^{[n] \in \Delta} [\Delta^n, A(Y_n)]
$

is a commuting diagram

$$
  \array{ 
    \uparrow &&&& \uparrow && \uparrow
    \\
    [2]
    &&&&
    \Delta^2 &\stackrel{f}{\to}& 
    A(Y_2)
    \\
    \uparrow &&&& \uparrow && \uparrow
    \\
    [1]
    &&&&
    \Delta^1 &\stackrel{g}{\to}& 
    A(Y_1)
    \\
    \uparrow &&&& \uparrow && \uparrow
    \\
    [0]
    &&&&
    \Delta^0 &\stackrel{a}{\to}& 
    A(Y_0)
  }
$$

where the vertical arrows indicate all the simplicial maps of the cosimplicial objects $\Delta$ and $A(Y_\bullet)$.

So this is

* on $Y_0$ an object $a \in A(Y_0)$;

* on "double intersections" (might be a cover of double intersections) $Y_1$ a gluing isomorphism $g : \pi_1^* a \to \pi_2^* a$ which identifies the two copies of $a$ obtained by pullback along the two projection maps $\pi_1, \pi_2 : U \times_X U \to U$.

* on "triple intersections" $Y_2$ a gluing 2-isomorphism
$
 \array{
   && \pi_2^* a
   \\
   &
   {}^{\pi_{12}^* g}\nearrow
   &\Downarrow^f&
   \searrow^{\pi_{23}^* g}
   \\
   \pi_1^* a
   &&
     \stackrel{\pi_{13}^* g}{\to}
   &&
   \pi_3^* a
 }
$
which identifies the different gluing 1-isomorphisms.

And so on.


### Gluing for ordinary stacks 

The article 

* Sharon Hollander, _A Homotopy Theory for Stacks_ ([arXiv](http://arxiv.org/abs/math.AT/0110247))

spells out how the familiar formulation of the descent condition for ordinary [[stacks]] is equivalent to the corresponding descent condition for simplicial presheaves, duscussed above.

## Codescent

Sometimes one wishes to compute the descent objects for presheaves of the form

$$
  [B(-), A] : S^{op} \to SSet
  \,,
$$

where $B : S \to [S^{op}, SSet]$ is a given presheaf-valued co-presheaf. For instance in the context of [[schreiber:Differential Nonabelian Cohomology|differential nonabelian cohomology]] one is interested in the co-presheaf that assigns [[fundamental ∞-groupoids]]

$$
  B := \Pi : U \mapsto (V \mapsto S(V \times \Delta^\bullet, U))
$$

in which case the presheaf

$$
  [\Pi(-),A]
$$

would assign to $U \in S$ the pre-$\infty$-stack of "trivial $A$-principial bundles with flat connection".

For $Y \to X$ a given (hyper)cover, the descent object for $[B(-), A]$ can be expressed as

$$
  \begin{aligned}
    Desc(Y_\bullet \to X, [B(-), A])
    & := lim^\Delta [B(Y_\bullet),A]
    \\
    & \simeq \int^{[n]\in \Delta} [ \Delta^n, [B(Y_n),A] ]
    \\
    & \simeq \int^{[n]\in \Delta}
      [ \Delta^n \otimes B(Y_n), A]
    \\
    & \simeq [\int_{[n] \in \Delta} \Delta^n \otimes B(Y_n)\;,\; A ]
     \\
      & \simeq [colim^\Delta B(Y_\bullet), A]
  \end{aligned}
  \,.
$$

This way the descent for $[B(-),A]$ on the object $U = colim^\Delta U_\bullet$ is reexpressed as descent for $A$ of the $B$-modified object $colim^\Delta B(Y_\bullet)$. Following Street, this we may call the **codescent** object, as it co-represents descent.

## Monadic descent

In some context the descent condion may algebraically be encoded in an [[adjunction]]. This leads to the notion of [[monadic descent]]. See there for more details.

## Related concepts

* **descent**

  * [[cover]]

  * [[cohomological descent]]

  * [[fibered category]], [[descent morphism]]
  * [[Bénabou-Roubaud theorem]]
  * [[monadic descent]]: 

    * [[Sweedler coring]], [[Amitsur complex]], 
    * [[higher monadic descent]], [[descent in noncommutative algebraic geometry]]

  * [[van Kampen colimit]]
  * [[descent along a torsor]], [[Schneider's descent theorem]]

* [[sheaf]], [[(2,1)-sheaf]], [[2-sheaf]] [[(∞,1)-sheaf]], [[stack]]


## References

* [[A. Grothendieck]], M. Raynaud et al. _Rev&#234;tements &#233;tales et groupe fondamental_ ([[SGA1]]), Lecture Notes in Mathematics __224__, Springer 1971 (retyped as [math.AG/0206203](http://arxiv.org/abs/math/0206203); published  version Documents Math&#233;matiques __3__, Soci&#233;t&#233; Math&#233;matique de France, Paris 2003)
*  [[Angelo Vistoli]], _Grothendieck topologies, fibered categories and descent theory_ [MR2223406](http://www.ams.org/mathscinet-getitem?mr=2223406); [math.AG/0412512](http://arxiv.org/abs/math/0412512) pp. 1--104 in Barbara Fantechi, Lothar G&#246;ttsche, Luc Illusie, Steven L. Kleiman, Nitin Nitsure, Angelo Vistoli, _Fundamental algebraic geometry. Grothendieck's [[FGA explained]]_, Mathematical Surveys and Monographs __123__, Amer. Math. Soc. 2005. x+339 pp. [MR2007f:14001](http://www.ams.org/mathscinet-getitem?mr=2007f:14001)  
* [[Ross Street]], _Categorical and combinatorial aspects of descent theory_, [arXiv:math.CT/0303175](http://arxiv.org/abs/math.CT/0303175)
* [[Jacob Lurie]], _[[Descent Theorems]]_
* Daniel Sch&#228;ppi, _Descent via Tannaka duality_, [arxiv/1505.05681](http://arxiv.org/abs/1505.05681)

A connection between the monadic descent and the descent in the language of fibered categories is proved in 

* [[Jean Bénabou]], [[Jacques Roubaud]], _Monades et descente_, C. R. Acad. Sc. Paris, t. 270 (12 Janvier 1970), Serie A, 96--98, ([link](http://gallica.bnf.fr/ark:/12148/bpt6k480298g/f100), Biblioth&#232;que nationale de France)

[[!redirects descent and codescent]]

[[!redirects codescent]]

[[!redirects codescent object]]
[[!redirects codescent objects]]


[[!redirects descent theory]]


