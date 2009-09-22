<div class="rightHandSide toc">
[[!include category theory - contents]]
</div>

#Contents#

* tic
{:toc}


#Idea#

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

More generally, this makes sense in any [[2-category]] other than [[Cat]].

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



## Local vs global ##

As for the definition of [[limit]] (and [[homotopy limit]]) and induced from the _local_ definition of [[adjoint functor]]s, there is a _local_ definition of what Kan extension means, which applies to every single functor, and there is a _global_ definition, which applies to the category of all functors. If the local Kan extension of every single functor exists for some category, then both definitions coincide. 

In particular, the _global_ definition of Kan extension is a direct generalization of the _global_ definition of [[limit]].



##Definitions#

We give the following three definitions, which are equivalent in good situations

* local definitions

  * Kan extension in terms of a universal natural transformation;

  * Kan extension in terms of weighted (co)limits.

* global definition

  * Kan extension as the adjoint to pullback of functor categories;


### Global: adjoint to pullback of functor categories ##

The functor $p : C \to C'$ induces, by precomposition, a functor between [[functor category|functor categories]]
$$
  p^*: G\mapsto G\circ p  : [C',D] \to [C,D]
  \,.
$$

+--{.query}

[[Todd Trimble|Todd]]: I really think the notation ought to be $ p^* $, not $ p_* $. Normally the superscript form is used for pulling back in the direction opposite to $p$. For example, in the article [[preimage]], we have $ f^* = f^{-1}: P B \to P A $ where $f: A \to B$, where we could equally well write $ f^* = hom(f, 2): hom(B, 2) \to hom(A, 2) $. This is an instance of precomposition, so we should correspondingly write $ p^* = [p, D]: [C', D] \to [C, D] $.

_Toby_:  Yes, I would think so as well; and this fits into a much wider theory, like [[geometric morphism]]s of topoi.  It also gives us the notation $p_*$ for the left Kan extension and $p_!$ for the right Kan extension.  But see the **remark on terminology** below for the other side, I guess.

_Todd_: IMHO, the example of sheaves on a space seems a bit loaded, since there one homs an arrow $f$ into something twice (once into Sierpinski space, bringing one to maps between frames of the form $Open(X)$, and then once again into $Set$), which brings one back to covariance. The general situation just homs into something once. As it stands, the notation above really goes against the grain of established conventions, methinks.

_Toby_:  Yeah, well, *I* certainly won\'t mind if you change it!  (^_^)

[[Urs Schreiber|Urs]]: I had written the section _Remark on terminology: pushforward vs. pullback_ below after my original $p^*$ had been changed to $p_*$ by somebody, as far as I remember. I am in favor of having the $p^*$ back. So if we all agree on that, the next one reading this here should just implement the change. 

_Todd_: Thanks, Urs. I've made the changes accordingly. The section on _Remark on terminology_ hasn't been touched. 

_Eric_: It looks like Zoran changed it from $p^*$ to $p_*$ on March 26, 2009 in Revision 4.

_[[Eric]]_: I see that Goldblatt uses $F_\bullet$, which might help explain the change.
=--

The [[adjoint functor|left adjoint]] to $p^*$ is **left Kan extension** along $p$ of functors
$$
  Lan = Lan_p : [C,D] \to [C',D]
  \,,
$$
and the [[adjoint functor|right adjoint]] is **right Kan extension** along $p$ of functors
$$
  Ran = Ran_p: [C,D] \to [C',D]
  \,.
$$

This definition clearly makes sense as stated in particular also in [[enriched category theory]].

As discussed at [[adjoint functor]], it is possible that these adjoints do not exist, but may still be partially defined. Namely, for some functor $F\in [C,D]$ there exist a functor $Lan_p\,F:C'\to D$, *the left Kan extension of $F$ along $p$*,  and a natural isomorphism 
$$
Hom_{[C,D]}(F,p^*(-))\cong Hom_{[C',D]}(Lan_p\,F,-),
$$
i.e. a (co)representation of the functor $Hom_{[C,D]}(F,p^*(-))$. Similarly, right Kan extensions along $p$ may exist only for some $F$.


### Local: in terms of universal natural transformations ##

The above global definition _implies_ the following property:

[[generalized the|The]] left Kan extension $Lan F = Lan_p F$ of $F : C \to D$ along $p:C\to C'$ is a functor $Lan F : C' \to D$ equipped with a [[natural transformation]] $\eta_F : F \Rightarrow p^* Lan F$. 

<center markdown="1">[[kan-0.png:pic]]</center>

with the property that every other natural transformation
$F \Rightarrow p^* G$ factors uniquely through $\eta_F$ as

<center markdown="1">[[kan-1.png:pic]]</center>

Similarly for the right Kan extension, with the direction of the natural transformations reversed:

<center markdown="1">[[kan-2.png:pic]]</center>

It is clear that the definition in this form makes sense in every 2-category. In a bit different terminology, the left Kan extension 1-cell $F:C\to D$ along 1-cell $p\in K(C,C')$ in a 2-category $K$ is a pair $(Lan_p F,\alpha)$ where $\alpha : F\to Lan_p F\circ p$ is a 2-cell which reflects the object $F\in K(C,D)$ along the functor $p^* = K(p,D):K(C',D)\to K(C,D)$. 

This version of the definition clearly makes sense in any [[2-category]].

+-- {: .un_remark}
###### Warning

While this property is implied by the above global definition, it does not itself imply the global definition. For emphasis this definition here is sometimes called a **weak Kan extension** instead. See also the comment in the following section.
=--


### Local: pointwise in terms of weighted (co)limits ##

We give now a list of ways to express the Kan extension of a functor in terms of [[weighted limit|weighted]] [[limit|(co)limit]]s. These definitions apply in particular in the case that of $V$-[[enriched category theory]] for $V$ a [[closed monoidal category|closed]] [[symmetric monoidal category]].

The right Kan extension of a functor $F : C \to D$ along $p : C \to C'$ is at $c' \in C'$ the [[weighted limit]] over $F$ with weight $\hat p_{c'} : C^{op} \stackrel{C'(c',p(-))}{\to}  V$
$$
  (Ran_p F)(c') := lim^{C'(c',p(-))} F
  \,.
$$

Similarly the left Kan extension is given by the [[weighted limit|weighted colimit]]

$$
  (Lan_p F)(c') := colim^{C'(p(-),c')} F
  \,.
$$

### Local: pointwise in terms of (co)ends ###

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

### Local: in terms of (co)limits over comma-categories ###


In the special case that $V = Set$, and only then, there is an expression of the Kan extension as a (co)limit over a [[comma category]].

The right Kan extension of a functor of ordinary categories is given by the [[limit]]

$$
    (Ran_p F)(c')
      \simeq lim ((const_{c'}/p) \to C \stackrel{F}{\to} Set)
  \,,
$$

The left Kan extension of a functor of ordinary categories is given by the [[colimit]]

$$
  \begin{aligned}
    (Lan_p F)(c')
      \simeq colim ((p/const_{c'}) \to C \stackrel{F}{\to} Set)
  \end{aligned}
$$

Here $(const_{c'}/p)$ and $(p/const_{c'})$ are [[comma category|comma categories]] in the notation described there.


+-- {: .un_remark}
###### Warning

Note, however, that _not_ all _weak Kan extensions_ (in the universal-transformation sense defined above) are computed in this way, and weak Kan extensions can exist even when $D$ does not admit very many limits.  For instance, the weak Kan extensions that arise in the study of [[derived functor]]s are not computed in this way.
=--

Kan extensions that are computed by limits and colimits are sometimes called **pointwise** Kan extensions, as in [[Categories Work]].  On the other hand, some authors (such as Kelly) assert that only pointwise Kan extensions deserve the name "Kan extension," and use a term such as "weak Kan extension" for a functor equipped with a universal natural transformation.  It is certainly true that most Kan extensions which arise in practice are pointwise.  This distinction is even more important in [[enriched category]] theory.








### in $(\infty,1)$-categories #

The global definition of Kan extensions for
$(\infty,1)$-functors in terms of left/right adjoints to pullbacks may be interpreted essentially verbatim in the context of [[(infinity,1)-category|(infinity,1)-categories]] using the corresponding notion of [[limit in quasi-categories]].

Details are in [section 4.3, p. 215](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=215)  of [[Higher Topos Theory|HTT]].


##Examples#

* For $C' = $ the [[point]], the right Kan extension of $F$ is the [[limit]] of $F$, $Ran F \simeq \lim F$ and the left Kan extension is the [[colimit]] $Lan F \simeq colim F$.

* For $f : X \to Y$ a [[site|morphism of sites]] coming from a functor $f^t : S_Y \to S_X$ of the underlying categories, the left Kan extension of functors along $f^t$ is the [[inverse image]] operation $f^{-1} : PSh(Y) \to PSh(X)$.

* see also [[examples of Kan extensions]]

### restriction and extension of sheaves ###

For more on the following see also 

* [[restriction and extension of sheaves]]

The basic example for left Kan extensions using the above pointwise formula, is in the construction of the pullback of sheaves along a morphism of topological spaces. Let $f:X\to Y$ be a continuous map and $F$ a presheaf over $X$. Then the formula $(f_* F)(U) = F(f^{-1}(U))$ clearly defines a presheaf $f_* F$ on $Y$, which is in fact a sheaf if $F$ is.
On the other hand, given a presheaf $G$ over $Y$ we can not
define pullback presheaf $(f^{-1} G)(V)=G(f(V))$ because $f(V)$ might not be open in general (unless $f$ is an open map). For Grothendieck sites such $f(V)$ would not make even sense. But one can consider approximating from above by $G(W)$ for all $W\supset f(V)$ which are open and take a colimit of this diagram of inclusions (all $W$ are bigger, so getting down to the lower bound means going reverse to the direction of inclusions). But inclusion $f(V)\subset W$ implies $V\subset f^{-1}(f(V))\subset f^{-1}(W)$. The latter identity $V\subset f^{-1}(W)$ involves _only open sets_. Thus we take a colimit over the comma category $(V\downarrow f^{-1})$ of $G$. If $G$ is a sheaf, the colimit $G(V)$ understood as a rule $V\mapsto G(V)$ is still not a sheaf, we need to [[sheafification|sheafify]]. The result is sheaf-theoretic pullback 
$$
f^{-1}G = \mathrm{sheafify}(V\mapsto\mathrm{colim}_{V\hookrightarrow f^{-1}W} G(W)) = \mathrm{sheafify}(V\mapsto\mathrm{colim}_{(V\downarrow f^{-1})} G)
$$ 
which is a sheaf and one can analyze this construction to show that $f^{-1}$ is a right adjoint to $f_*$. This usage of left Kan extension persists in the more general case of Grothendieck topologies. 



##Remark on terminology: pushforward vs. pullback#

Generally, for $p : C \to C'$ a [[functor]], the induced functor on [[functor category|functor categories]]
$$
  [C', D] \stackrel{- \circ p}{\to}
  [C,D]
$$

_pulls back_ a functor on $C'$ to a functor on $C$, as this goes in the direction opposite to that of $p$ itself.

In that sense one would denote this functor by $p^*$ and call the (left or right) Kan exension along $p$, which goes the other way, the _push forward_ of functors from $C$ to functors on $C'$.

On the other hand, a crucial application of Kan extensions is to [[presheaf]] categories, i.e. to situations where $C = S^{op}$ and $S' = C'^{op}$ with $S$ and $S'$ both being [[site]]s.

In these cases the [[site]] may be thought of as representing a topological space. In particular $S$ may be the [[partial order|poset]] $Open(X)$ of open subsets of a topological space $X$ and inclusions and simlarly for $S'$. In that case, morphisms of sites

$$
  Open(X)^{op} \to Open(X')^{op}
$$ 
come from morphisms of topological spaces going the other way
$$
  X \leftarrow X' : f
  \,,
$$
because a continuous maps $f : X' \to X$ of topological spaces induces a pullback 
$$
  f^{-1} : O(X)^{op} \to O(X')^{op}
$$
$$
  U \mapsto f^{-1}(U)
$$
of open subsets. This means that when a functor $O(X)^{op} \to Set$ is thought of as a presheaf on a site, then what looks like a pullback of functors along $p = f^{-1}$ corresponds geometrically to a _push-forward_ of pre-sheaves. Therefore in [[presheaf]] literature (such as [[Categories and Sheaves]])  the functor induced by $p$ is usually denoted $p_*$ and not $p^*$.

It is however noteworthy that also the opposite perspective does occur in geometrically motivated examples. For instance 

* if $C$ is the [[discrete category]] on smooth space and $D = U(1)$ is the discrete category on the smooth space $X$ underlying the Lie group $U(1)$, then smooth functors (i.e. functors [[internal category|internal to]] [[generalized smooth space|smooth spaces]]) $F : C \to D$ can be identified with smooth $U(1)$-valued functions on $X$, and the functor on these functor categories induced by a smooth functor $p : C \to C'$ does correspond to the familiar notion of _pullback_ of functions;

* and similar in higher degrees: if $C = P_1(X)$ is the smooth path groupoid of a smooth space and $D = \mathbf{B} U(1)$ the smooth [[group]] $U(1)$ regarded as a one-object [[Lie groupoid]], then smooth functors $C \to D$ correspond to smooth 1-forms $\in \Omega^1(X)$ on $X$, and precomposition with a smooth functor $p : P_1(X) \to P_1(X')$ corresponds to the familiar notion of _pullback_ of 
1-forms.

This means that whether or not Kan extension corresponds geometrically to pushforward or to pullback depends on the way (covariant or contravariant) in which the domain categories $C$, $C'$ are identified with geometric entities.


##References#

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


[[!redirects Kan extensions]]