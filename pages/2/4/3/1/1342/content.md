#Idea#

Descent is a notion used to characterize [[(infinity,1)-sheaf|(infinity,1)-sheaves]] (i.e. [[infinity-stack]]s) among all [[(infinity,1)-presheaf|(infinity,1)-presheaves]] as those $(\infty,1)$-presheaves which are [[local object]]s with respect to certain morphisms $Y \to X$ which are to be regarded as [[cover]]s or [[hypercover]]s of the $(\infty,1)$-presheaf $X$: the idea is that an $(\infty,1)$-sheaf "descends from the cover $U_\bullet$ down to $X$".

More concretely 

* every [[(infinity,1)-category of (infinity,1)-sheaves]] is characterized as being a sub-[[(infinity,1)-topos]] $Sh(S) \hookrightarrow PSh(S)$ of the $(\infty,1)$-topos of [[(infinity,1)-presheaf|(infinity,1)-presheaves]] on some (small) [[(infinity,1)-category]] $S$;

* every such $(\infty,1)$-topos is a [[reflective (infinity,1)-subcategory]] of $PSh(S)$, hence a [[localization of an (infinity,1)-category]] at a collection $W = \{Y \to X\}$ of morphisms which are sent to equivalences by the left adjoint of the inclusion;

* and the sheaves in $Sh(S) \hookrightarrow PSh(S)$ are precisely the [[local object]]s with respect to this collection $W$ of morphisms, i.e. precisely those objects $A \in PSh(S)$ such that $PSh(S)(X,A) \to PSh(S)(Y,A)$ is an isomorphism in the [[homotopy category of an (infinity,1)-category|homotopy category]], which we shall write $PSh(S)(X,A) \stackrel{\simeq}{\to} PSh(S)(Y,A)$ in the following paragraphs.

* This condition is essentially the _descent conditon_.

* In concrete models for the [[(infinity,1)-category of (infinity,1)-sheaves]] -- notably in terms of the [[model structure on simplicial presheaves]] -- the morphisms $Y \to X$ in $W$ usually come from [[hypercover]]s  $Y$ which are [[homotopy limit|homotopy colimits]] $Y = hocolim U^\bullet$ in [[SSet]]-[[enriched category theory]]  over a  [[simplicial object]] $U^\bullet$.

  * In this case the above condition becomes $PSh(S)(X,A) \stackrel{\simeq}{\to} PSh(S)(hocolim U^\bullet, A)$ which is equivalent to $ PSh(S)(X,A) \stackrel{\simeq}{\to} holim PSh(S)(U^\bullet, A) $. This in turn is usually equivalently written $ A(X) \stackrel{\simeq}{\to} holim A(U^\bullet) $. And this is the form of the [[local object]]-condition which is usually called _descent condition_.



# Descent for ordinary sheaves#

Descent is best understood as a direct generalization of the  situation for 0-stacks, i.e. ordinary sheaves, which we briefly  recall in a language suitable for the following generalization.

For $S$ any small [[category]] and [[Set]] the category of small sets, write $\mathrm{PSh}(S) = [S^{op}, Set]$ for the category of [[presheaf|presheaves]] on $S$. Categories of this form enjoy various nice properties which are familiar from $Set$ itself,  and which are summarized by saying that $\mathrm{PSh}(S)$ is a [[topos]]. The relevance of
this for the present purpose is that there is a natural notion of morphisms of topoi, which are [[functor]]s respecting this structure in some sense: these are called [[geometric morphism]]s.

A [[category of sheaves]] on $S$ is a sub-topos of $PSh(S)$ in that it is a [[full and faithful functor]] $Sh(S)\hookrightarrow PSh(S)$ which is a [[geometric morphism]].

One finds that the [[reflective subcategory]] $Sh(S) \hookrightarrow PSh(S)$ of sheaves inside presheaves is the [[localization]] of $PSh(S)$ at morphisms $f : Y \to X$ called [[local isomorphism]]s, which are determined by and determing the choice of topos-inclusion. A [[presheaf]] $A$ is a [[sheaf]] precisely if it is a [[local object]] with respect to these [[local isomorphism]]s, that is precisely if

$$
  Hom_{PSh(S)}(X,A) \stackrel{Hom_{PSh(S)}(f,A)}{\to} Hom_{PSh(S)}(Y,A)
$$

is an [[isomorphism]] for all [[local isomorphism]]s $f$.


This locality condition is in fact the _descent_ condition: the sheaf has to descend from $Y$ down to $X$. More concretely, this condition is called a _descent condition_ when evaluated on morphisms $f : Y \to X$ which are [[hypercover]]s: 

namely if $\pi : Y^1 \to X$ is a [[local epimorphism]] with respect to the [[coverage]] that corresponds to the [[localization]] and if $\pi_2 : Y^2 \to Y^1 \times_X Y^1$ is a [[local epimorphism]], then with

$$
  Y^\bullet := (Y^2 \stackrel{\to}{\to} Y^1)
$$

being the two canonical morphisms out of $Y^2$, it follows that the canonical morphism 

$$
  colim Y^\bullet \to X
$$

is a [[local isomorphism]]. 

(This is excercise 16.6 in [[Categories and Sheaves]]).

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



# Descent for simplicial presheaves #

For more references and background on the following see [[descent for simplicial presheaves]].



A well-studied class of models/presentations for an [[(infinity,1)-category of (infinity,1)-sheaves]] is obtained using the [[model structure on simplicial presheaves]] on an  ordinary (1-categorical) [[site]] $S$, as follows.

Let $[S^{op}, SSet]$ be the [[SSet]]-[[enriched category]] of [[simplicial presheaf|simplicial presheaves]] on $S$. 

Recall from [[model structure on simplicial presheaves]] that there is the _global_ and the _local_ injective simplicial model structure on $[S^{op}, SSet]$, and that the local model structure is a (Bousfield-)localization of the global model structure.

According to [section 6.5.2](http://www-math.mit.edu/~lurie/papers/highertopoi.pdf#page=528)  of [[Higher Topos Theory|HTT]] we have:

* the full simplicial subcategory on fibrant-cofibrant objects of $[S^{op}, SSet]$ with respect to the _global_ injective model structure is (the [[SSet]]-[[enriched category]] realization of) the $(\infty,1)$-category  $PSh_{(\infty,1)}(S)$ of [[(infinity,1)-presheaf|(infinity,1)-presheaves]] on $S$.

* the full simplicial subcategory on fibrant-cofibrant objects of $[S^{op}, SSet]$ with respect to the _local_ injective model structure is (the [[SSet]]-[[enriched category]] realization of) the $(\infty,1)$-category  $\bar{Sh}_{(\infty,1)}(S)$ which is the [[hypercompletion]] of the $(\infty,1)$-category $Sh_{(\infty,1)}(S)$ of [[(infinity,1)-sheaf|(infinity,1)-sheaves]] on $S$.

Since with respect to the local or global injective model structure all objects are automatically cofibrant, this means that $\bar Sh_{(\infty,1)}(S)$ is the full sub-$(\infty,1)$-category of $PSh_{(\infty,1)}(S)$ on simplicial presheaves which are fibrant with respect to the local injective model structure: these are the [[infinity-stack]]s in this model.

By the general properties of [[localization of an (infinity,1)-category]] there should be a class of morphisms $f : Y \to X$ in $PSh_{(\infty,1)}(S)$ -- hence between injective-fibrant objects in $[S^{op}, PSh(S)]$ -- such that the simplicial presheaves representing $\infty$-stacks are precisely the [[local object]]s with respect to these morphisms.

This was worked out in 

* D. Dugger, S. Hollander, D. Isaksen, _Hypercovers and simplicial presheaves_ ([pdf](http://hopf.math.purdue.edu//Dugger-Hollander-Isaksen/hypspre.pdf))
 
**Definition**

For $X \in S$ an object in the [[site]] regarded as a simplicial presheaf and $U \in [S^{op}, SSet]$ a simplicial presheaf on $S$, a morphism $U \to X$ is a **[[hypercover]]** if it is an acyclic fibration with respect to the local injective [[model structure on simplicial presheaves]].

**Proposition**

The objects of $Sh_{(\infty,1)}(S)$ -- i.e. the fibrant objects with respect to the local injective model structure on $[S^{op}, SSet]$ -- are precisely those objects $A$ of $PSh_{(\infty,1)}(S)$ -- i.e. the fibrant objects with respect to the global injective model structure on $[S^{op}, SSet]$ -- which **satisfy descent for all hypercovers**, i.e. those for which for all hypercover $f : U \to X$ in $[S^{op}, SSet]$ we have that

$$
  [S^{op}, SSet](X,A) \stackrel{\simeq}{\to}
  [S^{op}, SSet](U,A)
$$

is a [[model structure on simplicial sets|weak equivalence of simplicial sets]].

Proof. This is theorem, 1.2 in [DHI](http://hopf.math.purdue.edu//Dugger-Hollander-Isaksen/hypspre.pdf) formulated in the light of lemma 4.4.


By the [[co-Yoneda lemma]] every simplicial presheaf $F : S^{op} \to SSet$ which we may regard as a presheaf $F : \Delta^{op}\times S^{op} \to Set$ is isomorphic to the [[weighted limit|weighted colimit]] $F \simeq lim^\Delta F_\bullet$ with [[SSet]]-weight the canonical cosimplicial simplicial set $\Delta$, i.e. for all $X \in S$

$$
  F : X \mapsto \int^{[n] \in \Delta} \Delta^n \times F(X)_n
  \,.
$$

In particular therefore for $A$ global-injective fibrant the descent condition reads

$$
  [S^{op}, SSet](X,A) \stackrel{\simeq}{\to}
  [S^{op}, SSet](colim^\Delta U_\bullet,A)
  \simeq
  lim^\Delta [S^{op}, SSet](U_\bullet,A)
  \,.
$$

With the shorthand notation introduced above the **descent condition** finally reads, for all global-injective fibrant simplicial presheaves $A$ and hypercovers $U \to X$:

$$
  A(X) \stackrel{\simeq}{\to} lim^\Delta A(U_\bullet)
  \,.
$$

The right hand here is often denoted $Desc(U_\bullet \to X, A)$, in which case this reads

$$
  A(X) \stackrel{\simeq}{\to} Desc(U_\bullet \to X, A)
  \,.
$$

## formulation in terms of homotopy limit ##

(expanded version of remark 2.1 in [DHI](http://hopf.math.purdue.edu//Dugger-Hollander-Isaksen/hypspre.pdf))


Using the [[Bousfield-Kan map]] every simplicial presheaf $F$ is also weakly equivalent to the weighted limit over $F_\bullet$ with weight given by $N(\Delta/(-)) : \Delta \to SSet$.

$$
  lim^{N(\Delta/(-))} F_\bullet \stackrel{\simeq}{\to}
  lim^\Delta F_\bullet
  \,.
$$

But by the discussion at [[weighted limit]], the left hand computes the [[homotopy limit]] of $F_\bullet$ (since $F_\bullet$ is objectwise fibrant, since $F_n$ factors through $Set \hookrightarrow SSet$), hence we have a weak equivalence

$$
  holim F_\bullet \stackrel{\simeq}{\to}
  F
  \,.
$$

Often the descent condition is therefore formulated with the cover $U$ replaced by its homotopy limit, whence it reads

$$
  [S^{op}, SSet](X,A) \stackrel{\simeq}{\to}
  [S^{op}, SSet](hocolim U_\bullet,A)
  \,.
$$

With $A$ global-injective fibrant this is equivalent to

$$
  [S^{op}, SSet](X,A) \stackrel{\simeq}{\to}
  holim [S^{op}, SSet](U_\bullet,A)
  \,.
$$

Using the notation introduced above this becomes finally

$$
  A(X) \stackrel{\simeq}{\to} holim A(U_\bullet)
  \,.
$$








# Descent for strict $\omega$-groupoid valued presheaves #

While simplicial sets are a very convenient model for general reasoning about higher weak categories and [[infinity-groupoid]]s, often concrete computations in particular with $(\infty)$-groupoids are more convenient in the context of more strictified models. 

Notably, by the generalized [[Dold-Kan correspondence]] the [[oriental|omega nerve]] injects [[crossed complex]]es -- slightly nonabelian generalizations of complexes of abelian groups which are equivalent to [[strict omega-groupoid]]s -- to simplicial sets

$$
  CrsCmplx \stackrel{\simeq}{\to}
  Str \omega Grpd \stackrel{N}{\to}
  SSet
  \,.
$$

And for instance something as simple as an abelian group $A$ regarded as a complex of groups in degree $n$ (hence as an $n$-group) already bcomes a somewhat involved object to understand under the nerve operation. 

_Therefore it is desireable to have a means to control descent for simplicial presheaves which happen to factor through the $\omega$-nerve directly in the context of $Str \omega Cat$._



In his work on descent, Ross Street took such a description in terms of gluing functions as the definition of descent. In

* Ross Street, _Categorical and combinatorial aspects of descent theory_ ([arXiv](http://arxiv.org/abs/math.CT/0303175))

he considers presheaves with values in [[strict omega-category|strict omega-categories]]

$$
  A : S^{op} \to Str \omega Cat
$$

and declares the descent $\omega$-category with respect to a simplicial object $U^\bullet : \Delta^{op} \to S$ to be the [[weighted limit]] in $Str\omega-Cat$-[[enriched category theory]]


$$
  lim^{F \Delta} A(U^\bullet) 
  \,,
$$

where $O := F \Delta : \Delta \to Str \omega Cat$ are the [[oriental]]s, i.e. the free $\omega$-categories on the simplicial [[simplex|simplices]]

$$
  O = F \circ \Delta
  \,,
$$

where $F : SSet \to Str\omega Cat$ is the [[right adjoint]] to the [[oriental|omega-nerve]] $N : Str \omega Cat \to SSet$.

The two precscriptions

$$
 \array{
  lim^\Delta N A(U^\bullet) & in SSet
  \\
  \\
  lim^{F \Delta} A(U^\bullet) & in Str \omega Grpd
 }
$$

have a very similar appearance. Street took his weighted limit as the _definition_ of higher descent. In view of the above general nonsense introduction, it would be desireable to understand how and to which extent this definition actually describes parts of an [[(infinity,1)-category of (infinity,1)-sheaves]].

To that end, notice that:

* a simplicial presheaf of the form $N \circ A$ with $A : S^{op} \to Str \omega Grpd$ is always global-injective fibrant (right?)

* by work of Domic Verity the $\omega$-nerve $N : Str \omega Cat \to SSet$ prolonged to taking values in stratified simplicial sets has a left adjoint $F : Strat \to Str \omega Cat$ which is strict monoidal.

Therefore...




# Descent in terms of gluing conditions #

We unwrap the expression 

$$
  lim^\Delta A(U^\bullet)
$$

for the descent data for a presheaf $A$ with respect to a cover $U \to X$


This [[weighted limit]] (whether taken in $SSet$- or in $Str \omega Cat$-[[enriched category theory]]) is given by the [[coend]]

$$
  lim^W\Delta A(U^\bullet)
  \simeq
  \int^{[n] \in \Delta} [\Delta^n, A(U_n)]
  \,.
$$


Unwrapping what this means one finds that an object/vertex of this is a choice of $n$-simplex in each $A(U^{n})$, subject to conditions which say that the boundary of this $n$-simplex must be obtained from pullback of $A$ along the maps $U^{[n]} \to U^{[n-1]}$ of the $(n-1)$-simplex in $A(U^{n-1})$

Namely an object in 

$
  lim^W\Delta A(U^\bullet)
  \simeq
  \int^{[n] \in \Delta} [\Delta^n, A(U_n)]
$

is a commuting diagram

$$
  \array{ 
    \uparrow &&&& \uparrow && \uparrow
    \\
    [2]
    &&&&
    \Delta^2 &\stackrel{f}{\to}& 
    A(U^2)
    \\
    \uparrow &&&& \uparrow && \uparrow
    \\
    [1]
    &&&&
    \Delta^1 &\stackrel{g}{\to}& 
    A(U^1)
    \\
    \uparrow &&&& \uparrow && \uparrow
    \\
    [0]
    &&&&
    \Delta^0 &\stackrel{a}{\to}& 
    A(U^0)
  }
$$

where the vertical arrows indicate all the simplicial maps of the cosimplicial objects $\Delta$ and $A(U_\bullet)$.

So this is

* on $U$ an object $a \in A(U)$;

* on double intersections $U \times_X U$ a gluing isomorphism $g : \pi_1^* a \to \pi_2^* a$ which identifies the two copies of $a$ obtained by pullback along the two projection maps $\pi_1, \pi_2 : U \times_X U \to U$.

* on triple intersections $U \times_X U \times_X U$ a gluing 2-isomorphism
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




## Gluing for ordinary stacks ##

The article 

* Sharon Hollander, _A Homotopy Theory for Stacks_ ([arXiv](http://arxiv.org/abs/math.AT/0110247))

spells out how the familiar formulation of the descent condition for ordinary [[stack]]s is equivalent to the corresponding descent condition for simplicial presheaves, duscussed above.

#Codescent#

Sometimes one wishes to compute the descent objects for presheaves of the form

$$
  [B(-), A] : S^{op} \to SSet
  \,,
$$

where $B : S \to [S^{op}, SSet]$ is a given presheaf-valued co-presheaf. For instance in the context of [[schreiber:Differential Nonabelian Cohomology|differential nonabelian cohomology]] one is interested in the co-presheaf that assigns [[fundamental infinity-groupoid]]s

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

## Examples ##

For $Str \omega Grpd$-valued presheaves on $S = Diff$, the codescent objects for  $B = P_1(-)$ -- the [[path groupoid]] -- and $B = P_2(-)$, the _path 2-groupoid_ are described and discussed [here](http://arxiv.org/abs/0705.0452) and [here](http://arxiv.org/abs/0808.1923).

It turns out that for $U_\bullet \to X$ a cover, the canonical morphism

$$
  Codesc(U_\bullet, P_1(-)) \to P_1(X)
$$

is an equivalence, as is

$$
  Codesc(U_\bullet, P_2(-)) \to P_2(X)
  \,.
$$

This should presumeably be read as saying that $P_n(-)$ _satisfies codescent_ and is hence an _$n$-costack_. 

This statement is closely related to the _homotopy van Kampen theorem_, which essentially asserts that $\Pi_n$ satisfies even a strict form of codescent.

For blog discussion about this see

* [Codescent and the van Kampen theorem](http://golem.ph.utexas.edu/category/2008/10/codescent_and_the_van_kempen_t.html)