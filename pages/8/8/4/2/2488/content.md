[[!redirects n-truncated object of an (infinity,1)-topos]]

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

An **$n$-truncated [[∞-groupoid]]** is an [[n-groupoid]].

An **$n$-truncated [[topological space]]** is a [[homotopy n-type]]: all [[homotopy group]]s above degree $n$ are trivial.

An **$n$-truncated object** in a general [[(∞,1)-category]] is an object such that all hom-$\infty$-groupoids into it are $n$-truncated.

If an object in an [[∞-stack]] [[(∞,1)-topos]]_ is $k$-truncated for any (possibly large) $k$, then it is $n$-truncated precisely if all its [[homotopy groups in an (∞,1)-topos|categorical homotopy groups]] above degree $n$ are trivial. 

The complementary notion of $n$-truncated object  is that of an [[n-connected object of an (∞,1)-category]].

## Definition

### In terms of truncations

+-- {: .un_defn}
###### Definition
**($n$-truncated $\infty$-groupoid)**

An [[∞-groupoid]] $A \in \infty Grpd$ is **$n$-truncated** for $n \in \mathbb{N}$ if it is an [[n-groupoid]]:

Precisely: in the model of [[∞-groupoid]]s given by [[Kan complex]]es $A$ is **$n$-truncated** if, the [[simplicial homotopy group]]s $\pi_k(A,x)$ are trivial for all $x$ and all $k \gt n$.

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

* By the above convention on (-2)-truncated $\infty$-groupoid, it is the [[terminal object]]s of $C$ that are (-2)-truncated.


### In terms of categorical homotopy groups 

At least if the ambient [[(∞,1)-category]] is even an [[∞-stack]] [[(∞,1)-topos]] there is an alternative, more intrinsic, characterization of $n$-truncation in terms of [[homotopy group]]s:

+-- {: .un_prop}
###### Proposition

Suppose that an object $X$ in an [[∞-stack]] [[(∞,1)-topos]] is $k$-truncated for _some_ $k \in \mathbb{N}$ (possibly very large).

Then for any $n \in \mathbb{N}$ this $X$ is $n$-truncated precisely if all the [[homotopy groups in an (∞,1)-topos|categorical homotopy groups]] above degree $n$ are trivial.

=--

+-- {: .proof}
###### Proof


This is [[Higher Topos Theory|HTT, prop 6.5.1.7]].

=--

+-- {: .un_remark}
###### Remark

Notice that this expected statement does require the assumption that $X$ is $k$-truncated for some $k$. Without any _a priori_ truncation assumption on $X$, there is no comparable statement about the relaton to categorical homotopy groups. See [[Higher Topos Theory|HTT, remark 6.5.1.8]].

=--

## Truncation 

Under mild conditions there is for each $n$ a universal way to send an arbitrary object $A$ to its $n$-truncation $\tau_{\leq n} A$. This is a general version of [[decategorification]] where [[k-morphism|n-morphism]]s are identified if they are connected by an invertible $(n+1)$-morphism.

For $C$ an [[(∞,1)-category]] and $n \geq -2$ in $\mathbb{Z}$ write $\tau_{\leq n} C $ for the [[full subcategory]] of $C$ on its $n$-truncated objects. 

So for instance for $C = $ [[∞Grpd]] we have $\tau_{\leq n} \infty Grpd = n Grpd$.


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


### Postnikov tower

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
   \to \tau_{\leq 2}A \to \tau_{\leq 1} A \to \tau_{\leq 0} A
$$

is the [[Postnikov tower in an (∞,1)-category]] of $A$. See there for more details.

## Examples

### In $\infty Grpd$ and in $Top$

An object in [[∞Grpd]] is $n$-truncated precisely if it is an [[n-groupoid]].

Equivalently, an object in [[Top]] is $n$-truncated if it is (in the equivalence class of) a [[homotopy n-type]].

When [[∞-groupoid]]s are modeled as [[Kan complex]]es, then an object $X \in \infty Grpd$ is $n$-truncated precisely if it is [[coskeleton|n-coskeletal]]. The truncation $X \to \tau_{\leq n} X$ is the counit of the [[coskeleton]] $X \to \mathbf{cosk}_n X$.


## References

The discussion of truncated objects in an $(\infty,1)$-category is in section 5.5.6 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

The discussion of categorical [[homotopy groups in an (∞,1)-topos]] is in section 6.5.1.

A classical reference on $n$-truncation of $\infty$-groupoids is for instance

A classical article that amplifies the expression of Postnikov towers in terms of [[coskeleton]]s is

* [[William Dwyer]], [[Dan Kan]], _An obstruction theory for diagrams of simplicial sets_ ([pdf](http://www.nd.edu/~wgd/Dvi/ObstructionTheoryForDiagrams.pdf))


[[!redirects truncated]]

[[!redirects n-truncated object of an (∞,1)-topos]]
[[!redirects n-truncated object in an (∞,1)-category]]
[[!redirects n-truncated object in an (∞,1)-topos]]
[[!redirects n-truncated object in an (infinity,1)-topos]]
[[!redirects n-truncated object of an (infinity,1)-topos]]

[[!redirects n-truncated object of an (∞,1)-category]]
[[!redirects n-truncated object in an (∞,1)-category]]
[[!redirects n-truncated object in an (infinity,1)-topos]]

[[!redirects truncated object of an (∞,1)-topos]]
[[!redirects truncated object in an (∞,1)-category]]
[[!redirects truncated object in an (∞,1)-topos]]
[[!redirects truncated object in an (infinity,1)-topos]]
[[!redirects truncated object of an (infinity,1)-topos]]

[[!redirects truncated object of an (∞,1)-category]]
[[!redirects truncated object in an (∞,1)-category]]
[[!redirects truncated object in an (infinity,1)-topos]]
