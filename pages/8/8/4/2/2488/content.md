[[!redirects n-truncated object of an (infinity,1)-topos]]

#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

An _$n$-truncated object of an [[∞-stack]] [[(∞,1)-topos]]_ is the analog of an [[n-groupoid]] or [[homotopy n-type]] in the archetypical [[(∞,1)-topos]] [[∞-Grpd]]/[[Top]]: 

it is an object $X$ whose [[homotopy group (of an ∞-stack)|homotopy groups (of an ∞-stack)]] $\pi_k(X)$ are trivial for $k \gt n$.

#Definition#

## in terms of truncations ##

+-- {: .un_defn}
###### Definition
**($n$-truncated $\infty$-groupoid)**

An [[∞-groupoid]] $A \in \infty Grpd$ is **$n$-truncated** for $n \in \mathbb{N}$ if it is an [[n-groupoid]]:

Precisely: in the model of [[∞-groupoid]]-groupoids given by [[Kan complex]]es an [[∞-groupoid]] is **$n$-truncated** if, the [[simplicial homotopy group]]s $\pi_k(A,x)$ are trivial for all $x$ and all $k \gt n$.

=--

It makes sense for the following to adopt the convention that $A$ is called 

* _$(-1)$-truncated_ if it is empty or contractible

* $(-2)$-truncated if it is non-empty and contractible.

(following [[Higher Topos Theory|HTT, p. 6]]).

To generalize this, let now $C$ be an arbitrary [[(∞,1)-category]]. For $X,A$ objects in $C$ write $C(X,A) \in $ [[? Grpd]] for the [[(∞,1)-categorical hom-space]] (if $C$ is given as a [[simplicially enriched category]] then this is just the [[SSet]]-[[hom-object]] which is guaranteed to be a [[Kan complex]]).

Using this, it shall be useful to slightly reformulate the above as follows:

+-- {: .un_lemma}
###### Observation

An [[∞-groupoid]] $A$ is $n$-truncated precisely for all other [[∞-groupoid]]s $X$ the hom-$\infty$-groupoid $\infty Grpd(X,A)$ is $n$-truncated.

=--

In categorical terms this just says that [[(n,k)-transformation|(∞,k)-transformation]] between $X$ and $A$ whose components a [[k-morphism]]s in $A$ cannot be nontrivial for $k \gt n$ if there are no nontrivial [[k-morphism]]s with $k \gt n$ in $A$.

Using this fact we can transport the notion of $n$-truncation to any [[(∞,1)-category]] by testing it on hom-[[∞-groupoid]]s:

+-- {: .un_defn}
###### Definition
**($n$-truncated object in an $(\infty,1)$-category)**

An object $A \in C$ of an [[(∞,1)-category]] $C$ is **$n$-truncated**, for $n \in \mathbb{N}$, if for all $X \in C$ the hom-[[∞-groupoid]] $C(X,A)$ is $n$-truncated.

=--

This is [[Higher Topos Theory|HTT, def. 5.5.6.1]].


Some terminology:

* A 0-truncated object is also called **discrete** . Notice that this is _categorically discrete_ as in [[discrete category]], not discrete in the sense of [[topological space]]s. An object in an [[(∞,1)-topos]] is discrete in this sense if, regarded as an [[∞-groupoid]] with extra structure it has only trivial morphisms.

* By the above concention on (-2)-truncated $\infty$-groupoid, it is the [[terminal object]]s of $C$ that are (-2)-truncated.


## in terms of homotopy groups ##

At least if the ambient [[(∞,1)-category]] is even an [[∞-stack]] [[(∞,1)-topos]] there is an alternative, mor intrinsic, characterization of $n$-truncation in terms of [[homotopy group]]s:

an object $X$ in an [[∞-stack]] [[(∞,1)-topos]] is $n$-truncated precisely when its [[homotopy group (of an ∞-stack)|homotopy groups (of an ∞-stack)]] $\pi_k(X)$ are trivial for $k \gt n$. This is [[Higher Topos Theory|HTT prop 6.5.1.7]].


# Truncation #

Under mild conditions there is for each $n$ a universal way to send an arbitrary object $A$ to its $n$-truncation $\tau_{\leq n} A$. This is a general version of [[decategorification]] where [[k-morphism|n-morphism]]s are identified if they are connected by an invertible $(n+1)$-morphism.

For $C$ an [[(∞,1)-category]] and $n \geq -2$ in $\mathbb{Z}$ write $\tau_{\leq n} C $ for the [[full subcategory]] of $C$ on its $n$-truncated objects. 

So for instance for $C = \infty Grpd$ we have $\tau_{\leq n} \infty Grpd = n Grpd$.


+-- {: .un_prop}
###### Proposition

If $C$ is an [[(∞,1)-category]] that is [[presentable (∞,1)-category|presentable]] then the canonical inclusion [[(∞,1)-functor]]

$$
  \tau_{\leq n} C \hookrightarrow C
$$

has an [[accessible (infinity,1)-functor|accessible]] [[left adjoint]]

$$
  \tau_{\leq n} : C \to C_{\leq n}
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT 5.5.6.18]].

=--

Indeed, as the notation suggests, $C_{\leq n}$ is the [[essential image]] of $C$ under $\tau_{\leq n}$. The image  $\tau_{\leq n} A$ of an object $A$ under this operation is the **$n$-truncation** of $A$.


#application in Postnikov tower#

By the fact that the truncation functor $\tau_{\leq n}$ is a [[left adjoint]] one obtains canonical morphisms

$$
  \tau_{\leq n}A  \to A
$$

as the [[adjunct]] of the [[identity]] on $A$, and then by iteration also canonical morphisms

$$
  \tau_{\leq (n+1)} A \to \tau_{\leq n} A
  \,.
$$

For any $A \in C$ the sequence

$$
  \cdots
   \to \tau_{\leq 2} \to \tau_{\leq 1} A \to \tau_{\leq 0} A
$$

is called the [[Postnikov tower (in an (infinity,n)-category)]] of $A$. See there for more details.

#References#

The discussion of truncated objects is in section 5.5.6 of

* [[Jacob Lurie]], [[Higher Topos Theory]]

The discussion of [[homotopy group (of an ∞-stack)]] is in section 6.5.1.


[[!redirects n-truncated object of an (∞,1)-topos]]
[[!redirects n-truncated object in an (∞,1)-topos]]
[[!redirects n-truncated object in an (infinity,1)-topos]]
[[!redirects n-truncated object of an (infinity,1)-topos]]

[[!redirects n-truncated object of an (∞,1)-category]]
[[!redirects n-truncated object in an (∞,1)-category]]
[[!redirects n-truncated object in an (infinity,1)-topos]]
