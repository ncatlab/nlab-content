
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Morphisms of sites

* table of contents
{: toc}

## Idea

A *morphism of sites* is, unsurprisingly, the appropriate sort of [[morphism]] between [[sites]].  It is defined exactly so as to induce a [[geometric morphism]] between [[toposes of sheaves]] (or, more generally, [[exact completions]]).

## Definition

Let $C$ and $D$ be [[sites]].

+-- {: .num_defn}
###### Definition
A [[functor]] $f:C\to D$ is a **morphism of sites** if

1. $f$ is [[flat functor#SiteValuedFunctors|covering-flat]], and

1. $f$ preserves covering families, i.e. for every [[covering]] $\{p_i : U_i \to U\}$ of an object $U \in C$, the family $\{f(p_i) : f(U_i) \to f(U)\}$ is a covering of $f(U) \in D$.
=--

+-- {: .num_remark}
###### Remark
If $C$ has [[finite limit]]s and all covering families in $D$ are [[strong epimorphism|strong epic]], then covering-flatness of $f$ is equivalent to $f$ preserving finite limits, i.e. being a [[left exact functor]], or equivalently to being a [[representably flat functor]].  Thus, frequently in the literature one finds a definition of a morphism of sites as being representably flat and preserving covering families.

For general $C$ and $D$, however, being representably flat *implies* being covering-flat, but not conversely.  Thus, the above definition of morphism of sites is more general than the common one.  There are few practical examples where the distinction matters, but our definition has better formal properties (see below).
=--

## Examples

+-- {: .num_example}
###### Example
If $A$ and $B$ are [[frame]]s regarded as sites via their canonical coverages, then a morphism of sites $A \to B$ is equivalently a frame [[homomorphism]], a function preserving finite [[meet]]s and arbitrary [[join]]s.
=--


+-- {: .num_example}
###### Example
**(slice sites)**

For $C$ a site and $U \in C$, the [[comma category]] $(C / U)$ inherits a topology from $C$, such that the [[forgetful functor]] $(C/U) \to C$ constitutes a morphism of sites.  This is also called the [[big site]] of $U$.  There are natural operations for [[restriction and extension of sheaves]] from a sub-site $U$ to $X$ and back.

For instance, if $X$ is a topological space and $U \in Op(X)$ is an open subset, then $U$ regarded as a topological space in its own right has corresponding to it the site $Op(U) = Op(X) \downarrow U$.
=--

+-- {: .num_example}
###### Example
For $C$ and $D$ [[regular category|regular categories]] equipped with their [[regular coverage]]s, a morphism of sites is the same as a [[regular functor]], i.e. a functor preserving finite limits and covers.

More generally, if $C$ and $D$ are [[∞-ary regular categories]] with their $\kappa$-canonical topologies, then a morphism of sites is the same as a $\kappa$-ary regular functor (preserving finite limits and $\kappa$-ary effective-epic families).
=--

+-- {: .num_example}
###### Example
For $C$ any site with finite limits, there is canonically a morphism of sites to its [[tangent category]]. See there for details.
=--


## Properties

### Relation to geometric morphisms
 {#RelationToGeometricMorphisms}

We discuss how morphisms of sites induce [[geometric morphism]]s of the corresponding [[sheaf topos]]es, and conversely.  The reader might want to first have a look at the discussion of _[geometric morphisms -- between presheaf toposes](geometric+morphism#BetweenPresheafToposes)_.


Let $f : (\mathcal{C},J) \to (\mathcal{D},K)$ be a morphism of sites, with $\mathcal{C}$ and $\mathcal{D}$ small.  Then precomposition with $f$ defines a [[functor]] between categories of presheaves $(-)\circ f : PSh(\mathcal{D}) \to PSh(\mathcal{C})$.

+-- {: .num_prop #MorphismsOfSitesInduceGeometricMorphisms}
###### Proposition
There is a [[geometric morphism]] between the [[categories of sheaves]]
$$
  (f^* \dashv f_*) : Sh(\mathcal{D},K) \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}
    Sh(\mathcal{C},J)
$$
where $f_*$ is the restriction of $(-)\circ f$ to sheaves.
=--

For the classical definition of morphisms of sites, using representably-flat functors, this appears for instance as ([Johnstone, lemma C2.3.3, cor. C2.3.4](#Johnstone)).  We give the proof in this special case; for the general case see ([Shulman](#Shulman)).

+-- {: .proof}
###### Proof

By the assumption that $f$ preserves covers we have that the restriction of $(-)\circ f$ to $Sh_K(\mathcal{D})$ indeed factors through $Sh(\mathcal{C}) \hookrightarrow PSh(\mathcal{C})$. 

Because for $\{U_i \to U\}$ a [[cover]] in $\mathcal{C}$ and $F$ a [[sheaf]] on $\mathcal{D}$, we have that (assuming here for simplicity that $\mathcal{C}$ has finite limits)

$$
  \begin{aligned}
    PSh_{\mathcal{C}}( \underset{\to}{\lim} ( \coprod_{i, j} U_i \times_{U} U_j)
    \stackrel{\to}{\to}
      \coprod_{i} U_i )
    \;,\;
    F(f(-))
    )
    & \simeq 
    \lim_{\leftarrow}
     \left(
      \prod_{i,j} PSh_{\mathcal{C}}( U_i \times_U U_j, F(f(-)))
       \stackrel{\leftarrow}{\leftarrow}
       \prod_i PSh_C(U_i , F(f(-)))
     \right)
    \\
    & \simeq
    \lim_{\leftarrow}
     \left(
      \prod_{i,j} F(f(U_i \times_U U_j)))
       \stackrel{\leftarrow}{\leftarrow}
       \prod_i F(f(U_i))
     \right)   
    \\
    & \simeq
    \lim_{\leftarrow}
     \left(
      \prod_{i,j} F(f(U_i) \times_{f(U)} f(U_j))))
       \stackrel{\leftarrow}{\leftarrow}
       \prod_i F(f(U_i))
     \right)       
    \\
    & \simeq
    PSh_{\mathcal{D}}( \underset{\to}{\lim} ( \coprod_{i, j} f(U_i) \times_{f(U)} f(U_j))
    \stackrel{\to}{\to}
      \coprod_{i} f(U_i) )
    \;,\;
    F
   )         
  \end{aligned}
  \,,
$$

where we used the [[Yoneda lemma]], the fact that the [[hom functor]] $PSh(-,-)$ sends [[colimit]]s in the first argument to [[limit]]s, and the assumption that $f$ preserves the [[pullback]]s involved.

Also $(-)\circ f$ preserves all [[limit]]s, because for presheaves these are computed objectwise. And since the inclusion $Sh_K(\mathcal{D}) \to PSh(\mathcal{D})$ is [[right adjoint]] (to [[sheafification]]) we have that 

$$
  f_* : Sh_K(\mathcal{D}) \hookrightarrow PSh(\mathcal{D}) \stackrel{(-)\circ f}{\to} Sh_J(\mathcal{C})
$$ 

preserves all limits. Therefore by the [[adjoint functor theorem]] it has a [[left adjoint]]. Explicitly, this is the composite of the left adjoint to $(-)\circ f$ and to sheaf inclusion. The first is left [[Kan extension]] $Lan_f$ along $f$ and the second is [[sheafification]] $L_J$ on $(\mathcal{C},J)$, so the left adjoint is the composite

$$
  f^*  :Sh_J(\mathcal{C}) \hookrightarrow PSh(\mathcal{C}) \stackrel{Lan_f}{\to}S
   PSh(\mathcal{D}) \stackrel{L_J}{\to} Sh_J(\mathcal{D})
  \,.
$$

Here the first morphism preserves all limits, the last one all finite limits. Hence the composite preserves all finite limits if the left [[Kan extension]] $Lan_f$ does. This is the case if $f$ is a [[flat functor]].

(Because the left [[Kan extension]] is given by the [[colimit]] 
$Lan_f X : d \mapsto {\underset{\to}{\lim}}((f^{op}/d) \to {\mathcal{C}}^{op} \stackrel{X}{\to} Set)$ over the [[comma category]] $f^{op}/d$ which is a [[filtered category]] if $f$ is flat, and [[filtered colimit]]s are precisely those that commute with [[finite limit]]s. For more details on this argument see the discussion at [Geometric morphisms between presheaf toposes](geometric+morphism#BetweenPresheafToposes).)

=--

+-- {: .num_remark}
###### Remark

This is a "contravariant" construction in that a morphism of sites going one way gives a geometric morphisms of toposes going the opposite way. Another condition, the _[[covering lifting property]]_ gives a covariant assignment.

=--


Conversely, any geometric morphism which restricts and corestricts to a functor between sites of definition is induced by a morphism between those sites:

+-- {: .num_prop #GeometricMorphismsComeFromMorphismsOfSites}
###### Proposition
Let $(\mathcal{C}, J)$ be a small site and let $(\mathcal{D}, K)$ be a [[small-generated site]].  Then a [[geometric morphism]]
$$
  f : Sh(\mathcal{D}, K) \to Sh(\mathcal{C}, J)
$$
is induced by a morphism of sites $(\mathcal{D}, K) \leftarrow (\mathcal{C}, J) : F$ precisely if the [[inverse image functor]] $f^*$ respects the [[Yoneda embedding]]s, i.e. there is a functor $F$ making the following diagram commute:
$$
  \array{
    \mathcal{D } &\stackrel{F}{\leftarrow}& \mathcal{C}
    \\
    {}^{\mathllap{j_{\mathcal{D}}}}\downarrow && \downarrow^{\mathrlap{j_{\mathcal{C}}}}
    \\
    Sh(\mathcal{D}, K) &\stackrel{f^*}{\leftarrow}&
    Sh(\mathcal{C}, J)    
  }
  \,.
$$
=--

In the special case when $\mathcal{C}$ and $\mathcal{D}$ have finite limits and $\mathcal{D}$ is subcanonical, so that morphisms of sites can be defined using representably flat functors, this appears as ([Johnstone, lemma C2.3.8](#Johnstone)).  We give the proof in this case; for the general case see ([Shulman, Prop. 11.14](#Shulman)).  Note that the general case would not be true for the classical definition of "morphism of sites".


+-- {: .proof}
###### Proof

It suffices to show that given $f$, the factorization $F$ is, if it exists, necessarily a morphism of sites: because since $f^*$ is [[left adjoint]] and thus preserves all [[colimit]]s and every object in $Sh(C)$ is a colimit of [[representable functor|representables]], $f^*$ is fixed by the factorization. By uniqueness of [[adjoint functor]]s this means then that together with its [[right adjoint]] it is the geometric morphism induced from the morphism of sites, by prop. \ref{MorphismsOfSitesInduceGeometricMorphisms}.

So we show that $F$ is necessarily a morphisms of sites: 

1. since the [[Yoneda embedding]] and [[sheafification]] as well as [[inverse image]]s preserve finite limits, so does $f^* j_{\mathcal{C}}$ and hence $F$ preserves finite limits, hence is a [[flat functor]];

1. $f^* h_{\mathcal{C}}$ preserves [[covering]]s (maps them to [[epimorphism]]s in $Sh(D, K)$) and since $K$ is assumed to be subcanonical it follows from [this prop.](site#CharacterizationOfSubcanonicalSites) that $j_{\mathcal{D}}$ also reflects covers. Therefore $F$ preserves covers.

=--

+-- {: .num_cor #LemmaForClassifyingToposes}
###### Corollary

Let $(\mathcal{C},J)$ be a [[small category|small]] site and let $\mathcal{E}$ be any [[sheaf topos]]. Then we have an [[equivalence of categories]]

$$
  Topos(\mathcal{E}, Sh(\mathcal{C}, J))
  \simeq
  Site((\mathcal{C}, J), \mathcal{E})
$$

between the [[geometric morphism]]s from $\mathcal{E}$ to $Sh(\mathcal{C}, J)$ and the morphisms of [[site]]s from $(\mathcal{C}, J)$ to the [[big site]] $(\mathcal{E}, C)$ for $C$ the [[canonical coverage]] on $\mathcal{E}$.

=--

This appears as ([Johnstone, cor. C2.3.9](#Johnstone)).

+-- {: .proof}
###### Proof

Since for the [[canonical coverage]] the [[Yoneda embedding]] is the [[identity]], this follows directly from prop. \ref{GeometricMorphismsComeFromMorphismsOfSites}.

=--

+-- {: .num_remark }
###### Remark

Corollary \ref{LemmaForClassifyingToposes} leads to the notion of
[[classifying toposes]]. See there for more details.

=--

### Between $\kappa$-ary sites

+-- {: .num_prop}
###### Proposition
If $C$ and $D$ are [[∞-ary sites]], then a functor $f:C\to D$ is a morphism of sites if and only if it preserves finite local $\kappa$-prelimits.
=--
+-- {: .proof}
###### Proof
See ([Shulman, Prop. 4.8](#Shulman))
=--


## References

* Kashiwara-Schapira, _[[Categories and Sheaves]]_, section 17.2 (in terms of [[local isomorphisms]]).

* [[Saunders MacLane]] [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_, section VII. 10 of (in terms of covering [[sieves]]).

* [[Peter Johnstone]], _[[Elephant|Sketches of an Elephant]]_, section C2.3.

* [[Michael Shulman]], "Exact completions and small sheaves".  *Theory and Applications of Categories*, Vol. 27, 2012, No. 7, pp 97-173.  [Free online](http://www.tac.mta.ca/tac/volumes/27/7/27-07abs.html)
{#Shulman}


[[!redirects morphism of sites]]
[[!redirects morphisms of sites]]