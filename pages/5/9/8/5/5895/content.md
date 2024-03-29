
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
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

The notion of [[site]] may be [[internalization|internalized]] in any [[topos]] to yield a notion of _internal site_.

## Definition

+-- {: .num_defn}
###### Definition

For $\mathcal{E}$ a [[topos]], an **internal site** in $\mathcal{E}$ is an [[internal category]] $\mathbb{C} = C_1 \rightrightarrows C_0$ equipped with an internal [[coverage]].

=--


Spelled out in components, this means the following (as in ([Johnstone](#Johnstone)), we shall only define _sifted_ coverages). First, we define the [[subobject]] $Sv(\mathbb{C}) \hookrightarrow PC_1$ of _[[sieves]]_, where a subobject $S \hookrightarrow C_1$ is a sieve if the composite
$$
S\times_{C_0} C_1 \to C_1\times_{C_0} C_1 \to C_1
$$
factors through $S$. Also recall the usual membership relation $\in_{C_1} \stackrel{(n,e)}{\to} PC_1 \times C_1$.


+-- {: .num_defn}
###### Definition
An _internal sifted coverage_ is given by a span $C_0 \stackrel{b}{\leftarrow} T \stackrel{c}{\to} Sv(\mathbb{C})$ subject to:

* The square
$$
\array{
T \times_{PC_1} \in_{C_1} & \stackrel{e pr_2}{\to} & C_1 \\
{}^{pr_1}\downarrow   & {}                & \downarrow^{s} \\
T                  & \stackrel{b}{\to} & C_0
}
$$
commutes, where the pullback in the top left corner is of the map $\in_{C_1} \to PC_1$ along $T \to Sv(\mathbb{C}) \hookrightarrow PC_1$.

* If we define the subobject $Q\hookrightarrow T\times_{C_0} C_1 \times_{C_0} T$ as
$$
  Q := \{(t',a,t) | aa' \in t \forall a'\in t'\}
$$
(in the internal language), the composite $Q \hookrightarrow T\times_{C_0} C_1 \times_{C_0} T \stackrel{pr_{23}}{\to} C_1 \times_{C_0} T$ is required to be an epimorphism.

=--

We can additionally ask that more saturation conditions (as discussed at [[coverage]]) hold. 

(...)

## Properties

### Externalization

We discuss how to every internal site there is a corresponding external site such that the [[internal sheaf topos]] on the former agrees with the external sheaf topos on the latter.

+-- {: .num_defn #TheExternalizedSite}
###### Definition

Let $\mathcal{C}$ be a [[small category]] and let $\mathcal{E} := [\mathcal{C}^{op}, Set]$ be its [[presheaf topos]]. Let $\mathbb{D} \in \mathcal{E}$ be an internal site. Regarded, by the [[Yoneda lemma]], as a functor $\mathbb{D} : \mathcal{C}^{op} \to Cat$, this induces via the [[Grothendieck construction]] a [[fibered category]] which we denote

$$
  \mathcal{C} \rtimes \mathbb{D} \to \mathcal{C}
  \,.
$$

=--

This is reviewed for instance in ([Johnstone, p. 596](#Johnstone)).

The notation is motivated from the following example.

+-- {: .num_example}
###### Example

Let $G$ be a [[group]] (in [[Set]], hence a [[discrete group]]) and let $\mathcal{C} := \mathbf{B}G$ be its [[delooping]] [[groupoid]]. Then 

$$
  \mathcal{E} \simeq [\mathbf{B}G , Set]
$$

is the topos of [[permutation representation]]s of $G$. Let $H \in \mathcal{E}$ be a [[group object]]. This is equivalently a group in $Set$ equipped with a $G$-[[action]]. Its internal delooping gives the [[internal groupoid]] $\mathbb{D} := \mathcal{B}H$  in $\mathcal{E}$. 

In this case we have that 

$$
  \mathcal{C} \rtimes \mathbb{D} \simeq \mathbf{B}(G \rtimes H)
$$

is the delooping groupoid of the [[semidirect product]] group of the $G$-action on $H$.

=--

Generally we have

+-- {: .num_remark}
###### Remark

The category $\mathcal{C} \rtimes \mathbb{D}$ from def. \ref{TheExternalizedSite} is described as follows:

* [[object]]s are pairs $(U,V)$ with $U \in Ob \mathcal{C}$ and $V \in Ob \mathbb{D}(U)$;

* [[morphism]]s $(U',V') \to (U,V)$ are pairs $(a,b)$ where $a : U' \to U$ is in $\mathcal{C}$ and $b : V' \to \mathbb{D}(a)(V)$ in $\mathbb{D}(U')$.


=--

+-- {: .num_prop}
###### Proposition

We have an [[equivalence of categories]]

$$
  [\mathbb{D}^{op}, [\mathcal{C}^{op}, Set]]
   \simeq
  [(\mathcal{C} \rtimes \mathbb{D})^{op}, Set]
$$

between the [[category of internal presheaves]] in $\mathcal{E}$ over the internal category $\mathbb{D}$, and external presheaves over the semidirect product site $\mathcal{C} \rtimes \mathbb{D}$.

=--

This appears as ([Johnstone, lemma C2.5.3](#Johnstone)).

This result generalizes straightforwardly to an analogous statement for internal sheaves.

+-- {: .num_defn #CoverageOnTheExternalizedSite}
###### Definition

If $\mathcal{C}$ is equipped with a [[coverage]] $J$ and $\mathbb{D}$ is equipped with an internal coverage $K$ , define a coverage $J \rtimes K$ on $\mathcal{C} \rtimes \mathbb{D}$ by declaring that a [[sieve]] on an object $(U,V)$ is $(J \times K)$-covering if there exists an element $S \in K(U)$ with $b(S) = V$, ...

=--

+-- {: .num_prop}
###### Proposition

Let $\mathcal{E} = Sh_J(\mathcal{C})$ be a [[sheaf topos]] and $(\mathbb{D}, K)$ an internal site in $\mathcal{E}$. Then with def. \ref{CoverageOnTheExternalizedSite} we have an [[equivalence of categories]]

$$
  Sh_{K}(\mathbb{D})
  \simeq
  Sh_{J \rtimes K}(\mathcal{C} \rtimes \mathbb{D})
$$

between [[internal sheaves]] in $\mathcal{E}$ on $\mathbb{D}$ and [[sheaf|external sheaves]] on the semidirect product site $J \rtimes K$.

Moreover, the [[projection]] [[functor]] $P : \mathcal{C} \rtimes \mathbb{D}$ is [[cover-reflecting]] and induces a [[geometric morphism]]

$$
  \Gamma 
   \colon
  Sh_K(\mathbb{D})
  \stackrel{}{\to}
  \mathcal{E}
  \,.
$$

=--

This appears as ([Johnstone, prop. C2.5.4](#Johnstone)).

## Related concepts

* [[site]]

* [[internal locale]], [[internal sheaf]]

* [[internalization]], [[internal logic]]

## References

Section C2.4 and C2.5 of

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
 {#Johnstone}

The semidirect product externalization of internal sites is due to

* [[Ieke Moerdijk]], _Continuous fibrations and inverse limits of toposes_, Composition Math. 68 (1986) ([NUMDAM](http://www.numdam.org/item?id=CM_1986__58_1_45_0))
 {#Moerdijk}

[[!redirects internal sites]]