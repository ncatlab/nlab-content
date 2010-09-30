
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--



#Contents#

* tic
{:toc}


##Idea

The _Kan extension_ of a [[functor]]
$F : C \to D$ with respect to a functor
$$
 \array{
  C
  \\
  \downarrow^p
  \\
  C'
 }
$$

is, if it exists, a "best approximation" to 
the problem of finding a functor $C' \to D$ such that 
$$
  \array{
     C &\stackrel{F}{\to}& D
     \\
     \downarrow^p & \nearrow
     \\
     C'
  }
  \,,
$$
i.e. to extending the domain of $F$ through $p$ from $C$ to $C'$.

More generally, this makes sense not only in [[Cat]] but in any [[2-category]].

Similarly, a [[Kan lift]] is the best approximation to lifting a morphism $F : C \to D$ through a morphism

$$
  \array{
    D'
    \\
    \downarrow
    \\
    D
  }
$$

to a morphism $\hat F$

$$
  \array{
    && D'
    \\
    & {}^{\hat F}\nearrow & \downarrow
    \\
    C &\stackrel{F}{\to}& D
  }
  \,.
$$


##Definitions

There are two definitions of Kan extensions, one of which is stronger than the other.

  When the stronger (or "pointwise") type of Kan extension exists, then it is also a Kan extension in the other (or "weak") sense, but a "weak" Kan extension can exist without being pointwise (see [below](#pointwiseVsWeak)).

* Ordinary, or "weak" Kan extensions, are given by adjoints to (or, more generally, universal transformations to/from) precomposition functors between functor categories.

* Strong, or "pointwise," Kan extensions, are computed at each input by a certain weighted (co)limit.

Kan extensions that are computed by limits and colimits are sometimes called **pointwise** Kan extensions, as in [[Categories Work]].  On the other hand, some authors (such as Kelly) assert that only pointwise Kan extensions deserve the name "Kan extension," and use a term such as "**weak** Kan extension" for a functor equipped with a universal natural transformation.  It is certainly true that most Kan extensions which arise in practice are pointwise.  This distinction is even more important in [[enriched category]] theory.


### Ordinary Kan extensions ##

Any functor $p : C \to C'$ induces, by precomposition, a functor between [[functor category|functor categories]]
$$
  p^*: G\mapsto G\circ p  : [C',D] \to [C,D]
  \,.
$$

(In some contexts, this functor might be called $p_*$; see "remark on terminology" below.)

+-- {: .un_defn}
###### Definition
If $p^*$ has a [[left adjoint]], then this left adjoint is called **left Kan extension** along $p$ and denoted 
$$
  Lan = Lan_p : [C,D] \to [C',D]
  \,,
$$
The image $Lan_p(f)$ of some functor $f\colon C\to D$ is called *the left Kan extension of $f$ along $p$*.  Similarly, if $p^*$ has a [[right adjoint]], this right adjoint is called **right Kan extension** along $p$ and denoted
$$
  Ran = Ran_p: [C,D] \to [C',D]
  \,.
$$
=--

We may call this the *global* definition of Kan extension.  It clearly makes sense as stated in other contexts, such as in [[enriched category theory]].  Note that if $C' = 1$ is the [[terminal category]], then saying that the left (resp. right) Kan extension functor exists along $p$ is the same as saying that $D$ admits all [[colimits]] (resp. [[limits]]) of shape $C$.

There is also a *local* definition of "the Kan extension of a given functor $f$ along $p$" which can exist even if the entire functor defined above does not.  This is a generalization of the fact that a *particular* diagram of shape $C$ can have a limit even if not every such diagram does.  It is also a special case of the fact discussed at [[adjoint functor]] that an adjoint functor can fail to exist completely, but may still be partially defined.  If the local Kan extension of every single functor exists for some given $p\colon C\to C'$ and $D$, then these local Kan extensions fit together to define a functor which is the global Kan extension.

Thus, by the general notion of "partial adjoints," *the left Kan extension of $F\in [C,D]$ along $p$* should be a functor $Lan_p\,F:C'\to D$ equipped with a natural isomorphism
$$
Hom_{[C,D]}(F,p^*(-))\cong Hom_{[C',D]}(Lan_p\,F,-),
$$
i.e. a (co)representation of the functor $Hom_{[C,D]}(F,p^*(-))$.  The local definition of right Kan extensions along $p$ is dual.

As for adjoints and limits, by the usual logic of representable functors this can be rephrased as a "universal arrow."  Namely, [[generalized the|the]] left Kan extension $Lan F = Lan_p F$ of $F : C \to D$ along $p:C\to C'$ is a functor $Lan F : C' \to D$ equipped with a [[natural transformation]] $\eta_F : F \Rightarrow p^* Lan F$. 

<center markdown="1">[[kan-0.png:pic]]</center>

with the property that every other natural transformation
$F \Rightarrow p^* G$ factors uniquely through $\eta_F$ as

<center markdown="1">[[kan-1.png:pic]]</center>

Similarly for the right Kan extension, with the direction of the natural transformations reversed:

<center markdown="1">[[kan-2.png:pic]]</center>

By the usual reasoning (see e.g. [[Categories Work]], chapter IV, theorem 2), if these representations exist for every $F$ then they can be organised into a left (right) adjoint $Lan_p$ ($Ran_p$) to $p^*$.

It is clear that the definition in this form makes sense in every [[2-category]]. In slightly different terminology, the left Kan extension 1-cell $F:C\to D$ along a 1-cell $p\in K(C,C')$ in a 2-category $K$ is a pair $(Lan_p F,\alpha)$ where $\alpha : F\to Lan_p F\circ p$ is a 2-cell which reflects the object $F\in K(C,D)$ along the functor $p^* = K(p,D):K(C',D)\to K(C,D)$.


### Pointwise Kan extensions {#Pointwise}

If $D$ admits certain [[limit|(co)limits]], then left and right Kan extensions can be computed in terms of these.  The requisite limits are most naturally expressed as [[weighted limits]], but in good cases they can be re-expressed in terms of [[end|(co)ends]] or conical colimits over [[comma categories]], which may be more familiar.  However, we first give a definition that doesn't rely on any computational framework:

+-- {: .un_defn}
###### Definition
A Kan extension is called _pointwise_ if and only if it is preserved by all [[representable functor]]s ([[Categories Work]], theorem X.5.3).
=--

#### in terms of weighted (co)limits {#byColimits}

Suppose given $F : C \to D$ and $p : C \to C'$ such that for every $c' \in C'$, the weighted limit
$$
  (Ran_p F)(c') \coloneqq lim^{C'(c',p(-))} F
  \,.
$$
exists.  Then these objects fit together into a functor $Ran_p F$ which is a right Kan extension of $F$ along $p$.  Dually, if the [[weighted limit|weighted colimit]]
$$
  (Lan_p F)(c') \coloneqq colim^{C'(p(-),c')} F
  \,.
$$
exists for all $c'$, then they fit together into a left Kan extension $Lan_p F$.  These definitions evidently make sense in the generality of $V$-[[enriched category theory]] for $V$ a [[closed monoidal category|closed]] [[symmetric monoidal category]].  (In fact, they can be modified slightly to make sense in the full generality of a [[2-category equipped with proarrows]].)

In particular, this means that if $C$ is [[small category|small] and $D$ is [[complete category|complete]] (resp. cocomplete), then all right (resp. left) Kan extensions of functors $F\colon C\to D$ exist along any functor $p\colon C\to C'$.


#### in terms of (co)ends {#byCoends}

If the $V$-[[enriched category]] $D$ is [[power]]ed over $V$, then the above weighted limit may be re-expressed in terms of an [[end]] as

$$
  (Ran_p F)(c') \simeq \int_{c \in C} C'(c',p(c))\pitchfork F(c')
  \,.
$$

So in particular when $D = V$ this is

$$
  (Ran_p F)(c') \simeq \int_{c \in C} [C'(c',p(c)),F(c')]
  \,.
$$


Similarly, if $D$ is [[copower|tensored]] over $V$, then the left Kan extension is given by a [[coend]].

$$
  (Lan_p F)(c') \simeq \int^{c \in C} C'(p(c),c')\otimes F(c')
  \,.
$$

#### in terms of conical colimits

In the special case that $V = Set$, and only then, there is an expression of a weighted (co)limit and hence a Kan extension as a (co)limit over a [[comma category]].  Namely, the right Kan extension of a functor of ordinary categories is given by the [[limit]]
$$
    (Ran_p F)(c')
      \simeq lim \left((const_{c'}/p) \to C \stackrel{F}{\to} D\right)
  \,,
$$
if it exists for all $c'$.  Likewise, the left Kan extension of a functor of ordinary categories is given by the [[colimit]]
$$
  \begin{aligned}
    (Lan_p F)(c')
      \simeq colim \left((p/const_{c'}) \to C \stackrel{F}{\to} D\right)
  \end{aligned}
$$
if it exists for all $c'$.  Here $(const_{c'}/p)$ and $(p/const_{c'})$ are [[comma category|comma categories]] in the notation described there.


### Comparing the definitions   {#pointwiseVsWeak}

Not all Kan extensions in the universal-transformation sense defined above are _pointwise_ Kan extensions, i.e. computed as weighted (co)limits.  Non-pointwise Kan extensions can exist even when $D$ does not admit very many limits.  For instance, the Kan extensions that arise in the study of [[derived functor]]s are not pointwise.

The upshot is that if a pointwise extension exists then it is the same as the corresponding non-pointwise extension, but the converse does not always hold.  


### in $(\infty,1)$-categories 

The global definition of Kan extensions for
$(\infty,1)$-functors in terms of left/right adjoints to pullbacks may be interpreted essentially verbatim in the context of [[(infinity,1)-category|(infinity,1)-categories]] using the corresponding notion of [[limit in quasi-categories]].

Details are in [section 4.3, p. 215](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=215)  of [[Higher Topos Theory|HTT]].


## Examples

* For $C' = $ the [[point]], the right Kan extension of $F$ is the [[limit]] of $F$, $Ran F \simeq \lim F$ and the left Kan extension is the [[colimit]] $Lan F \simeq colim F$.

* For $f : X \to Y$ a [[site|morphism of sites]] coming from a functor $f^t : S_Y \to S_X$ of the underlying categories, the left Kan extension of functors along $f^t$ is the [[inverse image]] operation $f^{-1} : PSh(Y) \to PSh(X)$.

* see also [[examples of Kan extensions]]

### Restriction and extension of sheaves 

For more on the following see also 

* [[restriction and extension of sheaves]]

The basic example for left Kan extensions using the above pointwise formula, is in the construction of the pullback of sheaves along a morphism of topological spaces. Let $f:X\to Y$ be a continuous map and $F$ a presheaf over $X$. Then the formula $(f_* F)(U) = F(f^{-1}(U))$ clearly defines a presheaf $f_* F$ on $Y$, which is in fact a sheaf if $F$ is.
On the other hand, given a presheaf $G$ over $Y$ we can not
define pullback presheaf $(f^{-1} G)(V)=G(f(V))$ because $f(V)$ might not be open in general (unless $f$ is an open map). For Grothendieck sites such $f(V)$ would not make even sense. But one can consider approximating from above by $G(W)$ for all $W\supset f(V)$ which are open and take a colimit of this diagram of inclusions (all $W$ are bigger, so getting down to the lower bound means going reverse to the direction of inclusions). But inclusion $f(V)\subset W$ implies $V\subset f^{-1}(f(V))\subset f^{-1}(W)$. The latter identity $V\subset f^{-1}(W)$ involves _only open sets_. Thus we take a colimit over the comma category $(V\downarrow f^{-1})$ of $G$. If $G$ is a sheaf, the colimit $G(V)$ understood as a rule $V\mapsto G(V)$ is still not a sheaf, we need to [[sheafification|sheafify]]. The result is sheaf-theoretic pullback 
$$
f^{-1}G = \mathrm{sheafify}(V\mapsto\mathrm{colim}_{V\hookrightarrow f^{-1}W} G(W)) = \mathrm{sheafify}(V\mapsto\mathrm{colim}_{(V\downarrow f^{-1})} G)
$$ 
which is a sheaf, and one can analyze this construction to show that $f^{-1}$ is a left adjoint to $f_*$. This usage of left Kan extension persists in the more general case of Grothendieck topologies. 



## Remark on terminology: pushforward vs. pullback

Generally, for $p : C \to C'$ a [[functor]], the induced "precomposition" functor on [[functor category|functor categories]]
$$
  [C', D] \stackrel{- \circ p}{\to}
  [C,D]
$$
is spoken of as _pulling back_ a functor on $C'$ to a functor on $C$, as this operation goes in the direction opposite to that of $p$ itself.  For this reason, we have above denoted this functor by $p^*$.  Likewise, one might call the (left or right) Kan extensions along $p$ a _push forward_ of functors from $C$ to functors on $C'$.

This notation also coincides with that for [[geometric morphisms]] in one case: any functor $p\colon C\to C'$ between small categories induces a geometric morphism $[C,Set] \to [C',Set]$ of [[presheaf topos|presheaf toposes]], whose [[inverse image]] is the above $p^*$ and whose [[direct image]] $p_*$ is the right Kan extension functor.  Note that $p^*$ preserves (finite) limits, as required of an inverse image functor, since it has a left adjoint, namely *left* Kan extension.

On the other hand, if $p$ is additionally a [[flat functor]], then the above precomposition functor is also the *direct* image of a geometric morphism, whose inverse image is given by *left* Kan extension (which preserves finite limits when $p$ is flat).  More generally, if $C^{op}$ and $(C')^{op}$ are [[sites]] and $p^{op}\colon C^{op}\to (C')^{op}$ is flat and preserves covering families (i.e. it is a [[morphism of sites]]), then precomposition is the direct image of a geometric morphism $Sh(C^{op})\to Sh((C')^{op})$ between sheaf toposes.

For example, $C^{op}$ and $(C')^{op}$ might be the [[posets]] $Open(X)$ and $Open(X')$ of open subsets of [[topological spaces]] (or [[locales]]) $X$ and $X'$ and inclusions, in which case
$$
  Open(X)^{op} \to Open(X')^{op}
$$ 
come from continuous maps of topological spaces going the other way
$$
  X \leftarrow X' : f
  \,,
$$
via the usual inverse image $f^{-1} : O(X)^{op} \to O(X')^{op}$ of open subsets.

Thus, in such cases, the functor $p^*$, which looks like a pullback of functors along $p = f^{-1}$, corresponds geometrically to a _push-forward_ of (pre)sheaves along $f$.  Therefore, in [[presheaf]] literature (such as [[Categories and Sheaves]]) the precomposition functor induced by $p$ is usually denoted $p_*$ and not $p^*$.

It is however noteworthy that also the opposite perspective does occur in geometrically motivated examples. For instance 

* if $C$ is the [[discrete category]] on smooth space and $D = U(1)$ is the discrete category on the smooth space $X$ underlying the Lie group $U(1)$, then smooth functors (i.e. functors [[internal category|internal to]] [[generalized smooth space|smooth spaces]]) $F : C \to D$ can be identified with smooth $U(1)$-valued functions on $X$, and the functor on these functor categories induced by a smooth functor $p : C \to C'$ does correspond to the familiar notion of _pullback_ of functions;

* and similar in higher degrees: if $C = P_1(X)$ is the smooth path groupoid of a smooth space and $D = \mathbf{B} U(1)$ the smooth [[group]] $U(1)$ regarded as a one-object [[Lie groupoid]], then smooth functors $C \to D$ correspond to smooth 1-forms $\in \Omega^1(X)$ on $X$, and precomposition with a smooth functor $p : P_1(X) \to P_1(X')$ corresponds to the familiar notion of _pullback_ of 1-forms.

This means that whether or not Kan extension corresponds geometrically to pushforward or to pullback depends on the way (covariant or contravariant) in which the domain categories $C$, $C'$ are identified with geometric entities.


## References

See for instance section 2.3 in 

* Kashiwara and Shapira, [[Categories and Sheaves]]

MacLane's book 

* MacLane, [[Categories Work|Categories for the working mathematician]] 

has a famous treatment of Kan extensions with a statement: "The notion of Kan extensions subsumes all the other fundamental concepts in category theory".  Of course, many other fundamental concepts of category theory can also be regarded as subsuming all the others.

For Kan extensions in the context of [[enriched category theory]] see

* Dubuc, Eduardo J. Kan extensions in enriched category theory. Lecture Notes in Mathematics, Vol. 145 Springer-Verlag, Berlin-New York 1970 xvi+173 pp.

* chapter 4 from G.M. Kelly, _Basic Concepts of Enriched Category Theory_, 
 Cambridge University Press, Lecture Notes in Mathematics 64, 1982,  Republished in:
Reprints in Theory and Applications of Categories, No. 10 (2005) pp. 1-136 ([pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))

The $(\infty,1)$-categorical discussion is in section 4.3 

* [[Jacob Lurie]], [[Higher Topos Theory]]

See also

* M&#233;lli&#232;s and Tabareau, _Free models of T-algebraic theories computed as Kan extensions_ ([web](http://hal.archives-ouvertes.fr/hal-00339331/fr/))


[[!redirects Kan extension]]
[[!redirects Kan extensions]]
[[!redirects kan extension]]
[[!redirects kan extensions]]
[[!redirects left Kan extension]]
[[!redirects left Kan extensions]]
[[!redirects left kan extension]]
[[!redirects left kan extensions]]
[[!redirects right Kan extension]]
[[!redirects right Kan extensions]]
[[!redirects right kan extension]]
[[!redirects right kan extensions]]
