
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

An _$(\infty,1)$-cohesive site_ is a [[site]] such that the [[(∞,1)-category of (∞,1)-sheaves]] over it is a [[cohesive (∞,1)-topos]].




## Definition

+-- {: .un_def}
###### Definition

A [[site]] $C$ is **$\infty$-cohesive** over [[∞Grpd]] if it is

* a [[strongly ∞-connected site]]

* and an [[∞-local site]].


In detail this means that $C$ is

* a [[site]] -- a [[small category]] $C$ equipped with a [[coverage]];

* with the property that

  * it has a [[terminal object]] $*$;

  * it is a [[cosifted category]] (for instance in that it has all finite [[product]]s);
  
  * for every [[covering]] family $\{U_i \to U\}$ in $C$ 

    * the [[Cech nerve]] $C(U) \in [C^{op}, sSet]$ is degreewise 
      a [[coproduct]] of [[representable functor|representables]];

    * the [[simplicial set]] obtained by replacing each copy of a representable by a point is [[contractible]] (weakly equivalent to the 
      point in the standard [[model structure on simplicial sets]])

      $$
        \lim_\to C(U) \stackrel{\simeq}{\to} *
      $$

    * the simplicial set of points in $C(U)$ is weakly equivalent to the set of points of $U$:

      $$
        Hom_C(*, C(U)) \stackrel{\simeq}{\to} Hom_C(*,U)
        \,.
      $$
  
=--

+-- {: .un_remark}
###### Remark

These conditions are stronger than for a [[cohesive site]], which only guarantees cohesiveness of the 1-topos over it.

This definition is supposed to model the following ideas:

* every object $U$ has an underlying set of points $Hom_C(*,U)$. We may think of each $U$  as specifying one way in which there can be cohesion on this underlying set of points;

* in view of the [[nerve theorem]] the condition that $\lim_\to C(U)$ is contractible means that $U$ itself is contractible, as seen by the [[Grothendieck topology]] on $C$. This reflects the _local_ aspect of cohesion: we only specify cohesive structure on contractible lumps of points;

* in view of this the remaining condition that $Hom_C(*,C(U))$ is contractible is the $\infty$-analog of the condition on a [[concrete site]] that $Hom_C(*,\coprod_i U_i) \to Hom_C(*, U)$ is surjective.  This expresses that the notion of topology on $C$ and its concreteness over [[Set]] are consistent.

=--


## Examples

+-- {: .un_example}
###### Example

The site for a [[presheaf topos]], hence with trivial topology, is $\infty$-cohesive if it has finite [[product]]s.

=--

+-- {: .proof}
###### Proof

All covers $\{U_i \to U\}$ consist of only the [[identity]] morphism $\{U \stackrel{Id}{\to} U\}$. The Cech $C\{U\}$ is then the [[simplicial object]] constant on $U$ and hence satisfies its two conditions above trivially.

=--

+-- {: .un_example}
###### Examples/Proposition

The following [[site]]s are $\infty$-cohesive:

* the category [[CartSp]] with covering families given by open covers $\{U_i \hookrightarrow U\}$ by [[geodesically convex|convex]] subsets $U_i$;

  we can take the morphisms $\mathbb{R}^k \to \mathbb{R}^l$ in $CartSp$ to be 

  * [[continuous maps]] 

    -- in which case the sheaf topos over it models generalized [[topological space]]s, the [[2-sheaf]] [[2-topos]] contains for instance [[topological stack]]s; 

  * or [[smooth maps]]

    -- in which case the sheaf topos models generalized [[smooth space]]s such as [[diffeological space]]s, the [[(∞,1)-sheaf (∞,1)-topos]] is that of [[∞-Lie groupoid]]s;


* the site [[ThCartSp]] $ \subset \mathbb{L}$ of [[smooth loci]] consisting smoth loci of the form $R^n \times D^l_{(k)}$ with the second factor infinitesimal, where covering families those of the form $\{U_i \times D^l_{(k)} \to U \times D^l_{(k)}\}$ with $\{U_i \to U\}$ a covering family in $CartSp$ as above. 

  This is a site of definition for the [[Cahiers topos]].

More discussion of these two examples is at [[∞-Lie groupoid]] and [[∞-Lie algebroid]].

=--


+-- {: .proof}
###### Proof



Since every [[star-shaped]] region in $\mathbb{R}^n$ is [[diffeomorphic]] to an [[open ball]] (see there for details) we have that the covers $\{U_i \to U\}$ on [[CartSp]] by convex subsets are [[good open covers]] in the strong sens that all finite non-empty interseciton is [[diffeomorphic]] to an [[open ball]] and hence diffeomorphic to a [[Cartesian space]]. Therefore these are [[good open cover]]s in the strong sense of the word and their [[Cech nerve]]s $C(U)$ are degreewise coproducts of representables.

The fact that $\lim_\to C(U) \simeq *$ follows from the [[nerve theorem]], using that a [[Cartesian space]] regarded as a [[topological space]] is [[contractible]].


=--



## Properties {#Properties}

+-- {: .un_theorem}
###### Theorem

Let $C$ be an $\infty$-cohesive site. Then the [[(∞,1)-sheaf (∞,1)-topos]] $Sh_{(\infty,1)}(C)$ over $C$ is a [[cohesive (∞,1)-topos]] that satisfies the axiom "discrete objects are concrete" .

If moreover for all objects $U$ of $C$ we have that $C(*,U)$ is [[inhabited set|inhabited]], then the axiom "pieces have points" also holds.

=--

Since the [[(n,1)-topos]] over a site for any $n \in \mathbb{N}$ arises as the full [[sub-(∞,1)-category]] of the $(\infty,1)$-topos on the $n$-[[truncated]] objects and since the definition of cohesive $(n,1)$-topos is compatible with such truncation, it follows that

+-- {: .un_corollary}
###### Corollary

Let $C$ be an $\infty$-cohesive site. Then for all $n \in \mathbb{N}$ the [[(n,1)-topos]] $Sh_{(n,1)}(C)$ is cohesive. 

=--

To prove this, we need to show that

1. $Sh_{(\infty,1)}(C)$ is a [[locally ∞-connected (∞,1)-topos]] and a [[∞-connected (∞,1)-topos]].

  This follows with the discussion at [[∞-connected site]].

1. $Sh_{(\infty,1)}(C)$ is a [[local (∞,1)-topos]]. 

   This follows with the discussion at [[∞-local site]].

1. The [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] $\Pi : Sh_{(\infty,1)}(C) \to \infty Grpd$ preserves finite [[(∞,1)-products]]. 

1. If $\Gamma(U)$ is not empty for all $U \in C$, then _pieces have points_ in $Sh_{(\infty,1)}(C)$.

The last two conditions we demonstrate now.

+-- {: .un_prop}
###### Proposition

The functor $Pi : Sh_{(\infty,1)}(C) \to \infty Grpd$ whose existence is guaranteed by the above proposition preserves [[product]]s:

$$
  \Pi(A \times B) \simeq \Pi(A) \times \Pi(B)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the discussion at [[∞-connected site]] we have that $\Pi$ is given by the [[(∞,1)-colimit]] $\lim_\to : PSh_{(\infty,1)}(C) \to \infty Grpd$. By the assumption that $C$ is a [[cosifted (∞,1)-category]], it follows that this operation preserves finite products.

=--




Finally we prove that _pieces have points_ in $Sh_{(\infty,1)}(C)$ if all objects of $C$ have points.

+-- {: .proof}
###### Proof

By the above discussion both $\Gamma$ and $\Pi$ are presented by left Quillen functors on the projective model structure $[C^{op}, sSet]_{proj,loc}$. By Dugger's cofibrant replacement theorem (see [[model structure on simplicial presheaves]]) we have for $X$ any simplicial presheaf that a cofibrant replacement is given by an object that in the lowest two degrees is


$$
  \cdots
  \stackrel{\to}{\stackrel{\to}{\to}}
  \coprod_{U_0 \to U_1 \to X_1} U
   \stackrel{\to}{\to}
   \coprod_{U \to X_0} U
  \,,
$$

where the coproduct is over all morphisms out of representable presheaves $U_i$ as indicated. 

The model for $\Gamma$ sends this to

$$
  \cdots
  \stackrel{\to}{\stackrel{\to}{\to}}\coprod_{U_0 \to U_1 \to X_0} C(*,U_0)
   \stackrel{\to}{\to}
   \coprod_{U \to X_0} C(*,U)
  \,,
$$

whereas the model for $\Pi$ sends this to

$$
  \cdots
  \stackrel{\to}{\stackrel{\to}{\to}}\coprod_{U_0 \to U_1 \to X_0} *
   \stackrel{\to}{\to}
   \coprod_{U \to X_0} *
  \,.
$$

The morphism from the first to the latter is the evident one that componentwise sends $C(*,U)$ to the point. Since by assumption each $C(*,U)$ is nonempty, this is componentwise an epi. Hence the whole morphism is an epi on $\pi_0$.

=--






## Related concepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]

and

* [[locally connected site]] / [[locally ∞-connected site]]

  * [[connected site]] / [[∞-connected site]]

  * [[strongly connected site]] / [[strongly ∞-connected site]]

  * [[totally connected site]] / [[totally ∞-connected site]]

* [[local site]] / [[∞-local site]]

* [[cohesive site]], **∞-cohesive site**


[[!redirects ∞-cohesive site]]
[[!redirects ∞-cohesive sites]]

[[!redirects (infinity,1)-cohesive site]]


[[!redirects (∞,1)-cohesive site]]

[[!redirects (infinity,1)-cohesive sites]]
