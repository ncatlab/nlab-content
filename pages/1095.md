
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
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

The notion of $(\infty,1)$-category of $(\infty,1)$-sheaves is the generalization of the notion of [[category of sheaves]] from [[category theory]] to the [[higher category theory]] of [[(∞,1)-categories]].

## Definition
 {#Definition}

+-- {: .num_defn #CategoryOfSheaves}
###### Definition

An **$(\infty,1)$-category of $(\infty,1)$-sheaves** is a [[reflective sub-(∞,1)-category]] 

$$
  Sh(C) \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow}
  PSh(C)
$$

of an [[(∞,1)-category of (∞,1)-presheaves]] such that the following equivalent conditions hold

* $L$ is a [[topological localization]];

* there is the structure of an [[(∞,1)-site]] on $C$ such that the objects of $Sh(C)$ are precisely those [[(∞,1)-presheaves]] $A$ that are [[local objects]] with respect to the _covering_ [[monomorphism in an (∞,1)-category|monomorphisms]] $p : U \to j(c)$ in $PSh(C)$ in that

  \[
   \label{DescentCondition}
    A(c) \simeq PSh(j(c),A) \stackrel{PSh(p,A)}{\to} PSh(U,A)
  \]

  is an [[(∞,1)-equivalence]] in [[∞Grpd]]. 

=--

This is [[Higher Topos Theory|HTT, def. 6.2.2.6]].

An $(\infty,1)$-category of $(\infty,1)$-sheaves is an **[[(∞,1)-topos]]**.

+-- {: .num_remark}
###### Remark

Equivalence (eq:DescentCondition) is the _[[descent]]_ condition and the presheaves satisfying it are the **[[(∞,1)-sheaves]]** .
  
Typically $U$ here is the [[Cech nerve]] 

$$
  C(\{U_i\}) = \lim_{\to_{[n]}} U_{i_0, \cdots U_{i_n}}
$$ 

of a [[covering]] family $\{U_i \to c\}$ 
(where the colimit is the [[limit in a quasi-category|(∞,1)-categorical colimit]] or [[homotopy colimit]]) so that the above [[descent]] condition becomes 

$$
  A(c) \simeq PSh(\lim_\to U_\cdots, A)
 \simeq
  \lim_{\leftarrow} A(U_\cdots)
 =
 \lim_{\leftarrow}
 \left(
    \cdots
    \stackrel{\to}{\stackrel{\to}{\to}}
    \prod_{i,j} A(U_i) \times_{A(c)} A(U_j) 
    \stackrel{\to}{\to}\prod_i A(U_i)
 \right)
 \,.
$$

=--


+-- {: .num_remark}
###### Remark

Sometimes [[(∞,1)-sheaves]] are called **[[∞-stacks]]**, though sometimes the latter term is reserved for [[hypercomplete]] $(\infty,1)$-sheaves and at other times again it refers to [[(∞,2)-sheaves]].

The [[(n,1)-category|(n,1)-categorical]] counting is:

* [[sheaf]] = 0-stack = 0-[[truncated]] $(\infty,1)$-sheaf


* $(2,1)$-sheaf = [[stack]] = 1-truncated $(\infty,1)$-sheaf

* $(3,1)$-sheaf = 2-stack = 2-truncated $(\infty,1)$-sheaf

* etc.

* $(\infty,1)$-sheaf = [[∞-stack]]  (or = [[hypercomplete]] $(\infty,1)$-sheaf).

=--


## Properties

### Localizations and Grothendieck topology {#LocAndTopology}

We reproduce the proof that the two characterization in def. \ref{CategoryOfSheaves} above are indeed equivalent.
 
+-- {: .num_prop}
###### Proposition

For $C$ an [[(∞,1)-site]], the full [[sub-(∞,1)-category]] of $PSh(C)$ on [[local objects]] with respect to the covering monomorphisms in $PSh(C)$ is indeed a [[topological localization]], and hence $Sh(C)$ is indeed an exact [[reflective sub-(∞,1)-category]] of $PSh(C)$ and hence an [[(∞,1)-topos]]. 

=--

This is [[Higher Topos Theory|HTT, Prop. 6.2.2.7]]

+-- {: .proof}
###### Proof

We must prove that the [[(∞,1)-sheafification]] functor $L \colon PSh(C)\to Sh(C)$ preserves [[finite (∞,1)-limits]]. To do so we give an explicit construction of $L$. Given a presheaf $F\in PSh(C)$, define a new presheaf $F^+$ by the formula

$$F^+(c)={\lim_{\rightarrow}}_U {\lim_{\leftarrow}}_{u\in U} F(u)$$

where the colimit is taken over all covering sieves $U$ of $c$; this is called the _[[plus construction]]_. It defines a functor $PSh(C)\to PSh(C)$ and there is an obvious morphism $F\to F^+$ natural in $F$.

It is clear that the construction $F\mapsto F^+$ preserves 
[[finite (∞,1)-limits]], since [[filtered (∞,1)-colimits]] do, and it is easy to see that the map $F\to F^+$ becomes an [[equivalence in an (∞,1)-category|equivalence]] in $Sh(C)$. Given an [[ordinal]] $\alpha$, let $F^{(\alpha)}$ be the $\alpha$-iteration of the [[plus construction]] applied to the presheaf $F$. Then the functor $F\mapsto F^{(\alpha)}$ preserves finite limits and the canonical map $F\to F^{(\alpha)}$ becomes an equivalence in $Sh(C)$. In particular, if $F^{(\alpha)}$ is a sheaf, then $F^{(\alpha)}\simeq L(F)$. Thus, it suffices to show that there exists an ordinal $\alpha$ such that, for every $F\in PSh(C)$, $F^{(\alpha)}$ is a sheaf.

Fix $c\in C$ and a covering sieve $U$ of $C$. Given a presheaf $G\in PSh(C/c)$, we define an auxiliary presheaf $Match(U,G)\in PSh(C/c)$ by the formula

$$Match(U,G)(f: d\to c)={\lim_{\leftarrow}}_{u\in f^\ast U}G(u).$$

Restriction maps induce a morphism $\theta_G: G\to Match(U,G)$. Since we clearly have $G(u)\stackrel{\sim}{\to} Match(U,G)(u)$ for $u\in U$, the functor $Match(U,-)$ is _idempotent_ in the sense that $Match(U,\theta_G)$ and $\theta_{Match(U,G)}$ are (equivalent) equivalences.

By definition, $F\in PSh(C)$ is a sheaf if and only if $F(c)\stackrel{\sim}{\to} Match(U,F|_{C/c})(c)$ for every $c\in C$ and every covering sieve $U$ of $c$. Our goal is therefore to find an ordinal $\alpha$ (depending only on the (∞,1)-site $C$) such that, for every $F\in PSh(C)$, the map

$$F^{(\alpha)}(c) \to \Match(U,F^{(\alpha)}|_{C/c})(c)$$

is an equivalence.

The morphism $G\to G^+$ in $PSh(C/c)$ factors as

$$G\to Match(U,G)\to G^+.$$

Applying $Match(U,-)$ to this factorization, we get a commutative diagram

$$
  \array{
     G &\to& Match(U,G) &\to& G^+
     \\
     \downarrow^{\mathrlap{\theta_G}} && \downarrow^{\mathrlap{\theta_{Match(U,G)}}} && \downarrow^{\mathrlap{\theta_{G^+}}}
     \\
     Match(U,G) &\to& Match(U,Match(U,G)) &\to& Match(U,G^+)
  }
$$

in which the map $\theta_{Match(U,G)}$ is an equivalence since $Match(U,-)$ is idempotent. By cofinality, the colimit of the maps $\theta_{G^{(n)}}$ as $n\to\infty$ is an equivalence. Applying this to $G=F|_{C/c}$, we get

$$ F^{(\omega)}(c)\stackrel{\sim}{\to} {\lim_{\rightarrow}}_{n\to\infty} Match(U,F^{(n)}|_{C/c})(c).$$

This _almost_ means that $F^{(\omega)}$ is a sheaf. The problem is that the filtered colimit on the right-hand side need not commute with the limit appearing in the definition of $Match(U,-)$, that is, the canonical map

$$ {\lim_{\rightarrow}}_{\alpha \lt \omega} Match(U,F^{(\alpha)}|_{C/c})(c) \to \Match(U,F^{(\omega)}|_{C/c})(c) $$

need not be an equivalence. To solve this problem, we choose a cardinal $\kappa$ such that for every $c\in C$ and every covering sieve $U$ of $c$, the functor $Match(U,(-)|_{C/c})(c):Psh(C)\to \infty Grpd$ preserves $\kappa$-filtered colimits. This is possible because $C$ is small and each of these functors, being the composition of the restriction functor $PSh(C)\to PSh(U)$ and the limit functor $PSh(U)\to\infty Grpd$, has a [[left adjoint|left]] [[adjoint (∞,1)-functor]] and is therefore accessible (see [[HTT|HTT Prop. 5.4.7.7]]). Then the above map with $\omega$ replaced by $\kappa$ is an equivalence. For every ordinal $\alpha\lt\kappa$, applying the above to $F^{(\alpha)}$ shows that

$$ F^{(\alpha+\omega)}(c)\stackrel{\sim}{\to} {\lim_{\rightarrow}}_{n\to\infty} Match(U,F^{(\alpha+n)}|_{C/c})(c),$$

Since $\kappa$ is a limit ordinal, we deduce that $F^{(\kappa)}$ is a sheaf by cofinality.

=--

And conversely:

+-- {: .num_prop}
###### Proposition
**(equivalence of site structures and categories of sheaves)**

For $C$ a [[small (∞,1)-category]], there is a bijective correspondence between structure of an [[(∞,1)-site]] on $C$ and equivalence classes of [[topological localization]]s of $PSh(C)$.

=--

This is [[Higher Topos Theory|HTT, prop. 6.2.2.9]].

+-- {: .num_lemma}
###### Lemma

For $C$ a small [[(∞,1)-site]] and $Sh(C) \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow} PSh(C)$ the corressponding reflective inclusion of [[(∞,1)-sheaves]] into [[(∞,1)-presheaves]] on $C$ we have that the image under $L$ of a sub-$(\infty,1)$-functor  $p : U \to j(c)$ of a [[representable functor|representable]] $j(c)$ is covering precisely if $L(p)$ is an equivalence.

=--

This is [[Higher Topos Theory|HTT, lemma 6.2.2.8]].

+-- {: .proof}
###### Proof of the Lemma

Since $Sh(C)$ is the reflectuive localization of $PSh(C)$ at covering monomorphisms, it is clear that if $p : U \to j(c)$ is covering, then $L(p)$ is an equivalence.

To see the converse, form the 0-truncation of $L i$ and conclude as for ordinary sheaves on the [[homotopy category of an (infinity,1)-category|homotopy catgegory]] of $C$.

... 

=--

+-- {: .proof}
###### Proof of the Proposition


We have seen in (...) that for every structure of an $(\infty,1)$-site on $C$ we obtain a topological localization of the presheaf category, and that this is an injective map from site structures to equivalence classes of sheaf categories. It remains to show that it is also a surjective map, i.e. that every [[topological localization]] of $PSh(C)$ comes from the structure of an [[(∞,1)-site]] on $C$.

So consider $S \subset Mor(PSh(C))$ a strongly saturated class of morphisms which s topological (closed under pullbacks). Write $S_0 \subset S$ for the subcalss of those that are [[monomorphism in an (infinity,1)-category|monomorphisms]] of the form $U \to j(c)$.

Observe that then $S$ is indeed generated by (is the smallest strongly saturated class containing) $S_0$: since by the [[co-Yoneda lemma]] every object $X \in PSh(C)$ is a colimit $x \simeq {\lim_\to}_k j(\Xi_k)$ over representables. It follows that every monomorphism $f : Y \to X$ is a colimit (in $Func(\Delta[1],PSh(C))$) of those of the form $U \to j(c)$: for consider the pullback diagram 

$$
  \array{
     f^* ({\lim_\to}_k \Xi_k) &\to& Y 
     \\
     \downarrow^{\mathrlap{\simeq f}} && \downarrow^{\mathrlap{f}}
     \\
     {\lim_\to}_k \Xi_k &\stackrel{\simeq}{\to}& X
  }
  \;\;\;\;\;
  \simeq
  \;\;\;\;\;
  \array{
     ({\lim_\to}_k f^* \Xi_k) &\to& Y 
     \\
     \downarrow^{\mathrlap{\simeq f}} && \downarrow^{\mathrlap{f}}
     \\
     {\lim_\to}_k \Xi_k &\stackrel{\simeq}{\to}& X
  }
$$

where the equivalence is due to the fact that we have [[universal colimits]] in $PSh(C)$. This realizes $f$ as a colimit over morphisms of the form $f^* j(\Xi_k) \to j(\Xi_k)$ that are each a pullback of a monomorphism. Since monomorphisms are stable under pullback (see [[monomorphism in an (∞,1)-category]] for details), all these component morphisms are themselves monomorphisms.


So every monomorphism in $S$ is generated from $S_0$, but by the assumption that $S$ is topological, it is itself entirely generated from monomorphisms, hence is generated from $S_0$.

So far this establishes that evry topological localization of $PSh(C)$ is a localization at a collection of sieves/ subfunctors $U \to j(c)$ of representables. It remains to show that this collection of subfunctors is indeed an Grothendieck topology and hence exhibits on $C$ the structure of an [[(∞,1)-site]]. We check the necessary three axioms:

1. _equivalences cover_ -- The equivalences $j(c) \stackrel{\simeq}{\to} j(c)$ belong to $S$ and are monomorphisms, hence belong to $S_0$.

1. _pullback of a cover is covering_ - Since monomorphisms are stable under pullback, we haave for every $p : U \to j(c)$ in $S$ and every $j(f) : j(d) \to j(c)$ that also the pullback $f^* p$

   $$
     \array{
        f^* U &\to& U
        \\
        \downarrow^{\mathrlap{f^* p}} && \downarrow^{\mathrlap{p}}
        \\
        j(d) &\stackrel{f}{\to}& j(c)
     }
   $$

   is a monomorphism and in $S$, hence in $S_0$.

1. _if restriction of a sieve to a cover is covering, then the sieve is covering_  -- Let $p : U \to j(c)$ be an arbitrary monomorphism and $f : X \to j(d)$ in $S_0$. Write $X \simeq {\lim_\to}_k \Xi_k$ and consider the pullback

   $$
     \array{
       {\lim_\to}_k p^* \Xi_k &\stackrel{p^* f}{\to}&  U
       \\
       \downarrow^{{\lim_\to}_k f_k^* p} && \downarrow^{\mathrlap{p}}
       \\
       {\lim_\to}_k \Xi_k &\stackrel{f}{\to}& j(c)
     }
     \,,
   $$

   where again we made use of the [[universal colimits]] in $PSh(C)$. Now notice that 

   1. $f$ is in $S$ by assumption;

   1. $p^* f$ is by pullback stability of $S$;

   1. each of the $f_k p$ is in $S$ by assumption, hence ${\lim_k f_k^* p}$
      is by the fact that $S$ is strongly saturated.

   1. so by commutativity $p \circ p^*f$ is in $S$.

   1. finally by 2-out-of-3 this means that $p$ is in $S$.
   

=--


### Over paracompact topological spaces {#OverParacompactSpaces}

We discuss how $(\infty,1)$-sheaves over a [[paracompact topological space]] are equivalent to topological spaces [[overcategory|over]] $X$. This is the analogue of the 1-categorical statement that [[sheaves]] on $X$ are equivalent to [[etale space]]s over $X$: an etale space over $X$ is one whose [[fiber]]s are [[discrete topological space]], hence 0-[[truncated]] spaces. The [[n-category]] analogy has [[homotopy n-type]]s as fibers. 

+-- {: .num_defn}
###### Definition

For $Y \to X$ a [[morphism]] in [[Top]], and $U \in Op(X)$ an [[open subset]] of $X$, write

$$
  Sing_X(Y,U) := Hom_X(U \times \Delta^\bullet, X)
$$

for the [[simplicial set]] (in fact a [[Kan complex]]) of [[continuous map]]s

$$
  \array{
    U \times \Delta^k && \to && Y
    \\
    & \searrow && \swarrow
    \\
    && X
  }
$$

from $U$ times the topological $k$-[[simplex]] $\Delta^k$ into $Y$, that are [[section]]s of $Y \to X$.

=--

This is a relative version of the [[singular simplicial complex]] functor.

+-- {: .num_prop #OverTopModelStructure}
###### Proposition

Let $(X, \mathcal{B})$ be a [[topological space]] equipped with a [[base for the topology]] $\mathcal{B}$.

There is a [[model category]] structure on the [[over category]] $Top/X$ with weak equivalences and fibration precisely those morphisms $Y \to Z$ over $X$ such that for each $U \in \mathcal{B}$ the induced morphism $Sing_X(Y,U) \to Sing_X(Z,U)$ is a weak equivalence or fibration, respectively, in the standard [[model structure on simplicial sets]].

=--

This is [[Higher Topos Theory|HTT, prop 7.1.2.1]].

Write $(Top/X)^\circ$ for the [[(∞,1)-category]] [[locally presentable (∞,1)-category|presented]] by this model structure.

+-- {: .num_prop}
###### Proposition

Let $X$ be a [[paracompact topological space]] and write as usual $Sh_{(\infty,1)}(X) := Sh_{(\infty,1)}(Op(X))$ for the $(\infty,1)$-category of $(\infty,1)$-sheaves on the [[category of open subsets]] of $X$; equipped with the canonical structure of a [[site]].

Let $\mathcal{B}$ be the set of **$F_\sigma$-open subsets** of $X$. This are those [[open subset]]s that are countable unions of [[closed subset]]s, equivalently the 0-sets of [[continuous function]]s $X \to [0,1]$.

Let $Top/X^\circ$ be the corresponding $(\infty,1)$-categoty according to the [above proposition](#OverTopModelStructure). Then $Sing_X(-,-)$ constitutes  an [[equivalence of (∞,1)-categories]]

$$
  Top/X^\circ \simeq Sh_{(\infty,1)}(X)
  \,.
$$


=--


This is [[Higher Topos Theory|HTT, corollary 7.1.4.4]].

### Difference to more general $(\infty,1)$-toposes {#DiffToOthers}

The [[(∞,1)-topos]]es that are $(\infty,1)$-categories of sheaves, i.e. that arise by [[topological localization]] from an [[(∞,1)-category of (∞,1)-presheaves]], enjoy  a number of special properties over other classes of $(\infty,1)$-toposes, such as notably [[hypercomplete (∞,1)-topos]]es.

The following lists these properties. ([[Higher Topos Theory|HTT, section 6.5.4]].)

#### Universal property

The construction of [[(∞,1)-sheaf]] [[(∞,1)-topos]]es on a given [[locale]] is singled out over the construction of other kinds of $(\infty,1)$-toposes (such as [[hypercomplete (∞,1)-topos]]es) by the following universal property:

forming $(\infty,1)$-sheaves is, roughly, [[right adjoint]] to the functor $\tau_{\leq -1}$ that sends each $(\infty,1)$-topos to its underlying [[locale]] of [[subobject]]s of the [[terminal object]].

See [[Higher Topos Theory|HTT, item 1) of section 6.5.4]].

For $X,Y$ two $(\infty,1)$-toposes, write $Geom(X,Y) \subset Func(X,Y)$ for the full [[sub-(∞,1)-category]] of the [[(∞,1)-category of (∞,1)-functors]] on those that are [[geometric morphism]]s.


+-- {: .num_lemma}
###### Lemma

For $C$ an [[essentially small (∞,1)-category|small]] [[(n,1)-category]] with [[finite (∞,1)-limits]] and equipped with the structure of an [[(∞,1)-site]] and for $Y$ an [[(∞,1)-topos]], the [[truncated|truncation functor]]

$$
  \tau_{\leq n-1} : 
  Geom(Y, Sh(C)) \to Geom(\tau_{\leq n-1} Y, \tau_{\leq n-1} Sh(C))
$$

is an [[equivalence in a quasi-category|equivalence]] (of [[(∞,1)-categories]]).


=--

This is [[Higher Topos Theory|HTT, lemma 6.4.5.6]].

See also [[n-localic (∞,1)-topos]].



#### Compact generation


+-- {: .num_prop}

###### Proposition

Let $X$ be a [[coherent topological space]] and let $Op(X)$ be its [[category of open subsets]] with the standard structure of an [[(∞,1)-site]].

Then $Sh_{(\infty,1)}(X) := Sh_{(\infty,1)}(Op(X))$ is _compactly generated_ in that it is generated by [[filtered colimit]]s of [[compact object]]s.

Moreover, the compact objects of $Sh_{(\infty,1)}(X)$ are those that are [[stalk]]wise compact objects in [[∞Grpd]] and [[locally constant ∞-stack|locally constant]] along a suitable [[stratification]] of $X$.

=--

This is [[Higher Topos Theory|HTT, prop. 6.5.4.4]].


This statement is false for the [[hypercompletion]] of $Sh_{(\infty,1)}(X)$, in general.


#### Nonabelian cohomology {#NonabelianCohomology}

For $X$ a [[topological space]], let

$$
  (LConst \dashv \Gamma) :  Sh_{(\infty,1)}(X)
  \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}
$$

be the [[global section]]s terminal [[geometric morphism]]. 

For $A \in \infty Grpd$, the ([[nonabelian cohomology|nonabelian]]) [[cohomology]] of $X$ with coefficients in $A$ is usually defined in [[∞Grpd]] as

$$
  H(X,A) := \pi_0 Func(Sing X, A)
  \,,
$$

where $Sing X$ is the [[fundamental ∞-groupoid]] of $X$. On the other hand, if we send $A$ into $Sh_{(\infty,1)}(X)$ via $LConst$, the there is the _intrinsic_ [[cohomology]] of the $(\infty,1)$-topos $Sh_{(\infty,1)}(X)$ 
  
$$
  H'(X,A) := \pi_0 Sh_{(\infty,1)}(X)(X, LConst A)
  \,.
$$

Noticing that $X$ is in fact the [[terminal object]] of $Sh_{(\infty,1)}(X)$ and that $Sh_{(\infty,1)}(X)(X,-)$ is in fact that [[global section]]s functor, this is equivalently

$$
  \cdots \simeq \pi_0 \Gamma LConst A
  \,.
$$

+-- {: .num_theorem }
###### Theorem

If $X$ is a [[paracompact space]], then these two definitions of [[nonabelian cohomology]] of $X$ with [[constant ∞-stack|constant coefficients]] $A \in \infty Grpd$ agree:

$$
  H(X,A) := \pi_0 \infty Grpd(Sing X,A)  \simeq Sh_{(\infty,1)}(X)(X,LConst A)
  \,.
$$

=--

This is [[Higher Topos Theory|HTT, theorem 7.1.0.1]].


## Models 


The topological localizations of an [[(∞,1)-category of (∞,1)-presheaves]] are [[presentable (∞,1)-category|presented]] by the [[Bousfield localization of model categories|left Bousfield localization]] of the global [[model structure on simplicial presheaves]] at the set of [[Cech cover]]s.

The [[hypercompletion|hypercomplete]] $(\infty,1)$-sheaf toposes are [[presentable (infinity,1)-category|presented]] by the local Joyal-Jardine [[model structure on simplicial presheaves]]. 

Detailed discussion of this [[model category]] presentation is at 

* [[models for infinity-stack (infinity,1)-toposes|models for (infinity,1)-category of (infinity,1)-sheaves]] .

## Related concepts

* [[geometric homotopy type theory]]

## References

The study of simplicial presheaves apparently goes back to 

* K. Brown, [[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf Cohomology]]

which considers locally [[Kan complex|Kan]] [[simplicial presheaf|simplicial presheaves]] as a [[category of fibrant objects]].

This was later conceived in terms of a [[model structure on simplicial presheaves]] and on simplicial sheaves by Joyal and Jardine. To&#235;n summarizes the situation and emphasizes the interpretation in terms of [[∞-stacks]] living in $(\infty,1)$-categories for instance in

B. To&#235;n, _Higher and derived stacks: a global overview_   ([arXiv](http://arxiv.org/abs/math/0604504)) .

This concerns mostly [[hypercomplete]] $(\infty,1)$-sheaves, though.

The full picture in terms of Grothendieck-[[(∞,1)-topos]]es of [[(∞,1)-sheaves]] is the topic of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

  * localization $(\infty,1)$-functors ($(\infty,1)$-sheafification for the present purpose) are discussed in section 5.2.7;

  * local objects ($(\infty,1)$-sheaves for the present purpose) and [[local isomorphism]]s are discussed in section 5.5.4;

  * the definition of $(\infty,1)$-topoi of $(\infty,1)$-sheaves is then definition 6.1.0.4 in section 6.1;

  * the characterization of $(\infty,1)$-sheaves in terms of [[descent]] is in section 6.1.3 

  * the relation between the [[model structure on simplicial presheaves|Brown?Joyal?Jardine model]] and the general story is discussed at length in section 6.5.4

An overview is in

* [[Denis-Charles Cisinski]], _Cat&#233;gories sup&#233;rieures et th&#233;orie des topos_, S&#233;minaire Bourbaki, 21.3.2015, [pdf](http://www.math.univ-toulouse.fr/~dcisinsk/1097.pdf).

[[!redirects (infinity,1)-category of (infinity,1)-sheaves]]
[[!redirects (∞,1)-category of (∞,1)-sheaves]]
[[!redirects (infinity,1)-categories of (infinity,1)-sheaves]]
[[!redirects (∞,1)-categories of (∞,1)-sheaves]]

[[!redirects (∞,1)-sheaf (∞,1)-topos]]
[[!redirects (∞,1)-sheaf (∞,1)-toposes]]
[[!redirects (∞,1)-sheaf (∞,1)-topoi]]

[[!redirects ∞-stack (∞,1)-topos]]
[[!redirects ∞-stack (∞,1)-toposes]]
[[!redirects ∞-stack (∞,1)-topoi]]

[[!redirects infinity-stack (infinity,1)-topos]]
[[!redirects infinity-stack (infinity,1)-toposes]]
[[!redirects infinity-stack (infinity,1)-topoi]]


[[!redirects (∞,1)-sheaf (∞,1)-category]]
[[!redirects (∞,1)-sheaf (∞,1)-categories]]

[[!redirects (infinity,1)-sheaf (infinity,1)-category]]
[[!redirects (infinity,1)-sheaf (infinity,1)-categories]]

[[!redirects (∞,1)-topos of (∞,1)-sheaves]]
[[!redirects (∞,1)-toposes of (∞,1)-sheaves]]
[[!redirects (infinity,1)-topos of (infinity,1)-sheaves]]
[[!redirects (infinity,1)-toposes of (infinity,1)-sheaves]]

[[!redirects (∞,1)-sheaf ∞-topos]]
[[!redirects (∞,1)-sheaf ∞-toposes]]


