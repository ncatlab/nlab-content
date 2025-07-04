+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

Given a [[site]] $C$, the _sheafification_ [[functor]] universally turns [[presheaves]] on $C$ into [[sheaves]].

It is characterized as being the [[left adjoint|left]] [[adjoint functor]] $L : PSh(C) \to Sh(C)$ to the inclusion $Sh(C) \hookrightarrow PSh(C)$ of sheaves into all presheaves, exhibiting this as a [[reflective subcategory]].

Therefore sheafification is a special case of a very general phenomenon of [[localization|localizations]] of categories. See [[category of sheaves]] for more.

## Definition

Let $(C,J)$ be a [[site]] in the sense of: [[small category]] equipped with a [[coverage]]. Write $PSh(C)$ for the [[category of presheaves]] on $C$ and

$$
  j : C \to PSh(C)
$$

for the [[Yoneda embedding]]. Write 

$$
  i :  Sh_J(C) \hookrightarrow PSh(C)
$$ 

for the [[category of sheaves]]: the [[full subcategory]] on those presheaves that are $J$-[[sheaves]].

### Existence

+-- {: .num_prop #ExistenceOfLeftAdjoint}
###### Proposition

The inclusion of sheaves into presheaves admits a [[left adjoint|left]] [[adjoint functor]], which hence exhibits $Sh(C)$ as a [[reflective subcategory]] or reflective [[localization]] of $PSh(C)$:

$$
  (L \dashv i) : Sh_J(C) \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow}
   PSh(C)
  \,.
$$

=--

+-- {: .proof}
###### Proof

This follows by general properties discussed at [[reflective subcategory]]. We spell out the argument using the theory of [[localization]] at a set of morphisms satisfying a [[calculus of fractions]].

Recall from the discussion at [[sheaf]] that $Sh_J(C)$ is by definition the [[full subcategory]] of $PSh(C)$ on the [[local object|local objects]] with respect to the morphisms 

$$
  W = 
  \left\{
  S(\{U_i\}) := \lim_\to\left( 
    \coprod_{i,j} j(U_i) \times_{j(U)} j(U_j) \stackrel{\to}{\to} \coprod_i j(U_i) \right) \to j(U)
   |
   \;\;
  \{U_i \to U\}_{i \in I} \in J
  \right\}
$$

of [[sieve]] inclusions for all [[covering]] families of the [[coverage]] $J$. (Here the [[colimit]] $\lim_\to$ is the [[coequalizer]] of the two injection maps, as indicated. This is spelled out in more detail at [[sheaf]] and at [[sieve]].)

Now we invoke the following results:

1. The <a href="http://ncatlab.org/nlab/show/reflective+sub-(infinity%2C1)-category#LocalizationProposition">localization proposition</a> says that every [[full subcategory]] of a [[locally presentable category]] on the $W$-[[local object|local objects]] for a [[small set]] $W$ of morphisms is a [[reflective subcategory]], given by the [[localization]] at these morphisms;

1. By <a href="http://nlab.mathforge.org/nlab/show/reflective+subcategory#CharacterizationByLocalization">Gabriel-Zisman's theorem</a> every reflective subcategory is the [[localization]] at the collection of morphisms inverted by the left adjoint (which by the localization proposition is the saturation of the original set of morphisms).

1. If $W$ satisfies the axioms of a [[calculus of fractions]] then, by the discussion there, this localization is equivalently given by the category $PSh(C)[W^{-1}]$ whose objects are those of $PSh(C)$ and whose morphisms are given by $PSh(C)[W^{-1}](X,A) \simeq {\lim_{\to}}_{\hat X  \stackrel{w \in W}{\to} X} PSh_C(\hat X,A)$.


Notice that an object is a [[local object]] with respect to the above set of  morphisms $W$ precisely if it is local with respect to the set of all [[small set|small]] [[colimit|colimits]] (in the [[arrow category]] $Arr(PSh(C))$ ) of such morphims (since the [[hom-functor]] $PSh_C(-,A)$ sends colimits in the first argument to [[limit|limits]], and a limit of [[isomorphism|isomorphisms]] is an isomorphism).

Let hence $\bar W$ be the completion of $W$ under forming small colimits in $Arr(PSh(C))$.

We claim that the morphisms in $\bar W$ form a [[calculus of fractions]]. The first condition to check is that for all morphisms of presheaves $X \to j(U)$ and every covering family $\{U_i \to U\}$ there is a morphism $Y \to X$ in $\bar W$ and a [[commuting diagram]]

$$
  \array{
    Y &\to& S(\{U_i\})
    \\
    \downarrow && \downarrow^{\mathrlap{s}}
    \\
    X &\to& j(U)
  }
$$

in $PSh(C)$. (It is sufficient to demand this for $s \in W \subset \bar W$ to deduce the stability conditions for all morphisms in $\bar W$, since by [[universal colimits]] in the [[presheaf topos]] $PSh(C)$ the pullback of a colimit is a colimit of pullbacks.)

Similarly, to see that we can find $Y \to X$ we use the [[co-Yoneda lemma]] to decompose $X$ as a [[colimit]] of [[representable functor|representables]] $X \simeq {\lim_{\to}_j} K_j$ and then use [[universal colimits]] to deduce that we are looking at a diagram of the form

$$
  \array{
    {\lim_{\to}}_r s^* K_r &\to& S(\{U_i\})
    \\
    \downarrow && \downarrow^{\mathrlap{s}}
    \\
    {\lim_\to}_r j(K_r) &\to& j(U)
  }
  \,.
$$

Since $\bar W$ is closed under colimits, it is hence sufficient that we show the stability condition for $X$ any representable. So we need to fill diagrams of the form

$$
  \array{
    Y &\to& S(\{U_i\})
    \\
    \downarrow && \downarrow^{\mathrlap{s}}
    \\
    j(K) &\to& j(U)
  }
  \,.
$$

For this now use the single condition on a [[coverage]]: that for $\{U_i \to U\}$ a covering family in the [[site]] $(C,J)$ we can find a covering family $\{K_j \to K\}$ such that every $K_j \to K$ factors through one of the $U_i \to U$. But this means that also the [[sieve|sieves]] factor, and we have a commuting diagram

$$
  \array{
    S(\{K_j\}) &\to& S(\{U_i\})
    \\
    \downarrow && \downarrow
    \\
    j(K) &\to& j(U)
  }
  \,.
$$

This shows that $\bar W$ satisfies the first condition at [[factorization system]]. 

The second condition at [[calculus of fractions]] demands that if two composites of the form

$$
   X \stackrel{\to}{\to} S(\{U_i\}) \to j(U)
$$

are equal in $PSh(C)$, then there is a morphism $Y \to X$ in $PSh(C)$ such that the two composites

$$
  Y \to X \stackrel{\to}{\to} S(\{U_i\})
$$

are equal. But the [[sieve]] inclusions are [[monomorphism|monomorphisms]], hence this condition is trivially satisfied (choose $Y \to X$ to be the [[identity]] on $X$). Again by decomposing into colimits by the [[co-Yoneda lemma]] and using [[universal colimits]] and the pasting law for [[pullback|pullbacks]], the same follows for general morphisms in $\bar W$

$$
  \array{
    {\lim_\to}_k X_k &\stackrel{\simeq}{\to}& X
    \\
    \downarrow \downarrow && \downarrow \downarrow
    \\
    {\lim_\to}_k S(U_{k,i}) &\to& Y
    \\
    \downarrow && \downarrow 
    \\
    {\lim_\to}_k j(U_k) &\stackrel{\simeq}{\to}& j(U)
  }
  \,.
$$

by applying the above on each component $k$ of the colimit.

This gives us the [[localization]] $L : PSh(C) \to Sh_J(C)$ as described at [[calculus of fractions]]. By the discussion there 
we have that $Sh_J(C)$ is equivalently given by the category $PSh(C)[W^{-1}]$ with the same objects as $PSh(C)$ and [[hom-set|hom-sets]] given by

$$
  PSh(C)[W^{-1}](X,A) 
   \simeq
 {\lim_\to}_{\{\hat X \stackrel{w \in \hat W}{\to} X\}}
  PSh_C(\hat X,A)
  \,.
$$


So we have that for $X \in PSh(C)$ a presheaf and $A \in Sh_J(C)$ the [[hom-set]] $Sh_C(L(X),A)$ is given by

$$
  Sh_C(L(X), A) \simeq
  {\lim_{\to}}_{\hat X \stackrel{w \in \bar W}{\to} X} PSh_C(\hat X,A)
  \,.
$$

But if $A$ is a sheaf, it is a $\bar W$-[[local object]] and hence $PSh_C(\hat X \stackrel{w}{\to} X, A)$ is an [[isomorphism]] for all $w \in \bar W$. Hence the above colimit is over a diagram constant on its value at $w = Id : X \to X$ therefore we have a [[natural isomorphism]]

$$
  \cdots \simeq
  PSh_C(X,A)
  \,.
$$

This demonstrates the [[adjunction]] $(L \dashv i)$.

=--

### Construction

+-- {: .num_cor}
###### Corollary

For $X \in PSh(C)$ a [[presheaf]] on the [[site]] $(C,J)$, its **sheafification** $L(X)$ is the presheaf given on any $U \in C$ by

$$
  L(X) : U \mapsto {\lim_\to}_{\{\hat U \stackrel{w}{\to} j(U)\}} PSh_C(\hat U, X)
  \,,
$$

where the [[colimit]] on the right is over all $w \in \bar W$.

=--

+-- {: .proof}
###### Proof

By the [[Yoneda lemma]] we have

$$
  L(X)(U) \simeq PSh_C(j(U), L(X))
  \,.
$$

By the [above proposition](#ExistenceOfLeftAdjoint) this is 

$$
  \cdots \simeq Sh_C(L(j(U)), L(X))
  \,.
$$

By the proof of the above proposition, using the formulas discussed at [[calculus of fractions]], this hom-set is given by 

$$
  \cdots \simeq {\lim_\to}_{\{ \hat U \stackrel{w \in \bar W}{\to} j(U)\}} PSh_C(\hat U, X)
  \,.
$$

=--

\begin{remark}

By the definition of $\bar W$, the morphisms $\hat U \to j(U)$ in $\bar W$ are colimits of diagrams of [[covering]] [[sieve|sieves]]

$$
  \hat U \simeq 
    {\lim_\to}_{\{K \to U\}} S(\{K_i\}) \to {\lim_\to}_{\{K \to U\}} j(K)
  \,.
$$

This means (...) that the above colimit may be computed as two consecutive colimits of the form

$$
  {\lim_{\to}}_{\{S(\{U_i\}) \to j(U)\}} PSh_C(S(\{U_i\}), X)
  \,.
$$

One such application is called the [[plus construction]].

\end{remark}

\begin{proposition}

A morphism $S(\{U_i\}) \to X$ out of a [[sieve]] into any presheaf is in components precisely a [[matching family]] of the presheaf $X$ on the [[covering]] $\{U_i \to U\}$.

\end{proposition}

+-- {: .proof}
###### Proof

Use that the sieve is the [[coequalizer]]

$$
  S(\{U_i\}) \to \coprod_i j(U_i) \stackrel{\to}{\to}
   \coprod_{i,j} j(U_i) \times_{j(U)} j(U_j)
$$

and that the [[hom-functor]] $PSh_C(-,X)$ sends [[colimit|colimits]] to [[limit|limits]]. More details on this computation are at [[sheaf]].


=--


+-- {: .num_remark}
###### Remark

The [[unit of an adjunction|unit]] of the $(L \dashv i)$-[[adjunction]] has as components natural morphisms

$$
  X \to L X
$$

in $PSh(C)$, from any presheaf into its sheafification. By general properties of [[reflective subcategories]] these morphisms are mapped to [[isomorphism|isomorphisms]] by $L : PSh(C) \to Sh(C)$. Therefore these are [[local isomorphism|local isomorphisms]]. 

So every presheaf is related by a [[local isomorphism]] to its sheafification.

=--


## For sheaves with values in categories other than $Set$ 


For presheaves with values in categories other than
[[Set]], sheafification may be a difficult problem, unless one has some extra assumptions. 


### With values in models for finite-limit theories ###

Consider a type of structure $T$ defined in terms of an [[essentially algebraic theory]] finite limits (such as [[group|groups]], [[algebra|algebras]], [[module|modules]], etc.), then [[internal logic|internal]] $T$-[[algebra over an algebraic theory|models]] are preserved by both [[direct image|direct images]] and [[inverse image|inverse images]] of [[geometric morphism|geometric morphisms]].  Therefore, the [[adjunction]] $(L \dashv i) : Sh_J(C) \to PSh(C)$  directly induces an adjunction between $T$-models in sheaves and presheaves.  And since finite limits of sheaves and presheaves are computed pointwise, $T$-models in the category of (pre)sheaves are the same as (pre)sheaves of $T$-models-in-$Set$.

### Using the IPC-property

If a [[category]] $A$ satisfies the following assumptions, sheafification of presheaves in $[S^{op}, A]$ exists and is constructed analogously as for [[Set]]-valued sheaves.


* $A$ admits small [[limit|limits]];
* $A$ admits small [[colimit|colimits]];
* small [[filtered category|filtered colimits]] in $A$ are exact;
* $A$ satisfies the [[IPC-property]] .

This is true for instance for

* the category [[Set]] of sets;

* the category [[Grp]] of groups;

* the category $k Alg$ of $k$-algebras;

* the category $Mod(R)$ of [[module|modules]],

(but all of these are also $T$-models for finite-limit theories $T$).




## Related concepts

* **sheafification**, [[plus-construction on presheaves]]

* [[(∞,1)-sheafification]] / [[∞-stackification]]

## References

The description of sheafification in terms of [[local isomorphism|local isomorphisms]] is in section 16.3 (for [[Set]]-valued presheaves) and section 17.4 (for more general presheaves) of

* Kashiwara--Schapira, _[[Categories and Sheaves]]_

The description in terms of [[dense monomorphism|dense monomorphisms]] using [[Lawvere-Tierney topology]] is in section V.3 of

* [[Saunders Mac Lane]] and [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_

Extension of sheafification of presheaves with values in other categories has been advanced in

* [[Alex Heller]], K. A. Rowe, _On the category of sheaves_, Amer. J. Math. 84, 1962, 205-216

* Barr, Grillet, and Van Osdol, _Exact categories and categories of sheaves_, Lecture Notes in Math., Vol. 236, Springer, Berlin, 1971

* Friedrich Ulmer, _On the existence and exactness of the associated sheaf functor_, J. Pure Appl. Algebra 3, 1971, 295-306 

* [[Alexander Rosenberg]], _Almost quotient categories, sheaves and localizations_, 181 p. Seminar on supermanifolds 25, University of Stockholm, D. Leites editor, 1988 (in Russian; partial remake in English exists)

Discussion in [[homotopy type theory]] is in

* {#QuirinTabareau16} Kevin Quirin, Nicolas Tabareau, _Lawvere-Tierney sheafification in Homotopy Type Theory_, Journal of Formalized Reasoning, Vol 9, No 2, (2016) ([web](https://jfr.unibo.it/article/view/6232))


category: sheaf theory
[[!redirects sheafification functor]]
[[!redirects associated sheaf]]
[[!redirects associated sheaves]]
[[!redirects associated sheaf functor]]