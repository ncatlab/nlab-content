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

This is descibed at [[descent for simplicial presheaves]].

Notice from the discussion at [[abelian sheaf cohomology]] that this is known to reproduce in particular sheaf cohomology in terms of right [[derived functor]]s of global section functors as well as Cech hypercohomolohy for complexes of ableian sheaves.





# Relation to gluing conditions #

Often descent conditions are explicitly formulated as _gluing conditions_.

For instance for $A : S^{op} \to $ [[Grpd]] an ordinary [[stack]] (i.e. a 1-truncated $\infty$-stack), for $U \to X$ a [[cover]] and $Y = U^\bullet$ the corresponding simplicial object, the _objects of descent data_ are collections

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

That the category of such descent data for ordinary [[stack]]s indeed models $holim A(U^\bullet)$ was shown explicitly in

* Sharon Hollander, _A Homotopy Theory for Stacks_ ([arXiv](http://arxiv.org/abs/math.AT/0110247))

The point here is that the collection of descent data as above is naturally interpreted as the [[weighted limit]] in [[SSet]]-[[enriched category theory]]

$$
  lim^{\Delta} A(U^\bullet)
  \,,
$$

where 

$$
  A(U^\bullet) := \Delta \stackrel{(U^\bullet)^{op}}{\to} SPSh(S) \stackrel{A}{\to} SSet
$$

and where the weight is the canonical cosimplicial simplicial set given by the [[hom-functor]] $\Delta(-,-) : \Delta^{op} \times \Delta \to Set$.

Because the $\Delta$-[[weighted limit]] of an $SSet$-valued functor is just the [[hom-object]] in the [[enriched functor category]] $[\Delta, SSet]$:

$$ 
  lim^\Delta A(U^\bullet) \simeq [\Delta, SSet](\Delta, A(U^\bullet))
  \,.  
$$

An object/vertex in this simplicial set is a choice of $n$-simplex in each $A(U^{n})$, subject to conditions which say that the boundary of this $n$-simplex must be obtained from pullback of $A$ along the maps $U^{[n]} \to U^{[n-1]}$ of the $(n-1)$-simplex in $A(U^{n-1})$

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

In his work on descent, Ross Street took such a description in terms of gluing functions as the definition of descent. In

* Ross Street, _Categorical and combinatorial aspects of descent theory_ ([arXiv](http://arxiv.org/abs/math.CT/0303175))

he considers presheaves with values in [[strict omega-category|strict omega-categories]]

$$
  A : S^{op} \to Str \omega Cat
$$

and declares the descent $\omega$-category with respect to a simplicial object $U^\bullet : \Delta^{op} \to S$ to be the [[weighted limit]] in $Str\omega-Cat$-[[enriched category theory]]


$$
  lim^O A(U^\bullet) 
  \,,
$$

where $O : \Delta \to Str \omega Cat$ are the [[oriental]]s, i.e. the free $\omega$-categories on the simplicial [[simplex|simplices]]

$$
  O = F \circ \Delta
  \,,
$$

where $F : SSet \to Str\omega Cat$ is the [[right adjoint]] to the [[oriental|omega-nerve]] $N : Str \omega Cat \to SSet$.

For the case that $A$ happens to take values just in [[strict omega-groupoid]]s

$$
  A : S^{op} \to Str \omega Grpd
  \,,
$$

the two precscriptions

$$
 \array{
  lim^\Delta N A(U^\bullet) & in SSet
  \\
  \\
  lim^{F \Delta} A(U^\bullet) & in Str \omega Grpd
 }
$$

have a very similar appearance. Street took his weighted limit as the _definition_ of higher descent. In view of the above general nonsense introduction, it would be desireable to understand how and to which extent this definition actually describes parts of an [[(infinity,1)-category of (infinity,1)-sheaves]].

To that end, we first discuss under which conditions the homotopy limit $holim A(U^\bullet)$ over an [[SSet]]-valued functor can be re-expressed up to weak equivalence by the $\Delta$-weighted limit $lim^\Delta A(U^\bullet)$ that computes gluing data.

## From descent to gluing data ##

[[Reedy fibrant]], [[totalization]], [[Bousfield-Kan map]]




