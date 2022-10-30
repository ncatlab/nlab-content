
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _hypercover_ is the generalization of a [[Cech nerve]] of a [[cover]]: it is a simplicial [[resolution]] of an object obtained by iteratively applying covering families.

## Definition

Let 

$$
  (L \dashv i) : Sh(C) \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow}
  PSh(C)
$$

be the [[geometric embedding]] defining a [[sheaf topos]] $Sh(C)$ into a [[presheaf topos]] $PSh(C)$. 

+-- {: .num_defn #CoskeletonDefinition}
###### Definition

A morphism

$$
  (Y \stackrel{f}{\to} X) \in PSh(C)^{\Delta^{op}}
$$

in the [[category of simplicial objects]] in $PSh(C)$, hence the category of [[simplicial presheaves]], is called a **hypercover** if for all $n \in \mathbb{N}$ the canonical morphism

$$
  Y_{n} \to (\mathbf{cosk}_{n-1} Y)_n \times_{(\mathbf{cosk}_{n-1} X)_n} X_n
$$

in $PSh(C)$ are [[local epimorphisms]] (in other words, $f$ is a "[[Reedy model structure|Reedy]] local-epimorphism").  


Here this morphism into the [[fiber product]] is that 
induced from the [[naturality square]] 

$$
  \array{
    Y &\longrightarrow& X
    \\
    \downarrow && \downarrow
    \\
    \mathbf{cosk}_{n-1} Y &\longrightarrow& \mathbf{cosk}_{n-1} X
  }
$$

of the [[unit of a monad|unit]] of the [[coskeleton]] [[functor]] $\mathbf{cosk}_n : PSh(C)^{\Delta^{op}} \to PSh(C)^{\Delta^{op}}$.


A hypercover is called **bounded** by $n \in \mathbb{N}$ if for all $k \geq n$ the morphisms $Y_{k} \to (\mathbf{cosk}_{k-1} Y)_k \times_{(\mathbf{cosk}_{k-1} X)_k} X_k$ are [[isomorphism]]s.

The smallest $n$ for which this holds is called the **height** of the hypercover.

=--

+-- {: .num_defn #SplitHypercover}
###### Definition

A hypercover that also satisfies the [cofibrancy condition](model+structure+on+simplicial+presheaves#CofibrantObjects) in the projective [[local model structure on simplicial presheaves]] in that 

1. it is simplicial-degree wise a [[coproduct]] of [[representable functor|representables]];

1.  degenerate cells split off as a [[coproduct|direct summand]]) 

is called a **[[split hypercover]]**.

=--

([Dugger-Hollander-Isaksen 02, def. 4.13](#DuggerHollanderIsaksen02)) see also ([Low 14-05-26, 8.2.15](#Low))

+-- {: .num_remark}
###### Remark

Definition \ref{CoskeletonDefinition} is equivalent to saying that $f : Y \to X$ is a _local_ acyclic fibration: for all $U \in C$ and $n \in \mathbb{N}$ every lifting problem

$$
  \left(
  \array{
    \partial \Delta[n] \cdot U &\to& Y
    \\
    \downarrow && \downarrow^{\mathrlap{f}}
    \\
    \Delta[n]\cdot U &\to& X
  }
  \right)
  \;\;\simeq
  \;\;
  \left(
  \array{
    \partial \Delta[n] &\to& Y(U)
    \\
    \downarrow && \downarrow^{\mathrlap{f(U)}}
    \\
    \Delta[n] &\to& X(U)
  }
  \right)
$$

has a solution $(\sigma_i)$ after refining to some [[covering]] family $\{U_i \to U\}$ of $U$

$$
  \forall i :
  \left(
  \array{
    \partial \Delta[n] &\to& Y(U_i)
    \\
    \downarrow &{}^{\mathllap{\exists \sigma_i}}\nearrow& \downarrow^{\mathrlap{f(U_i)}}
    \\
    \Delta[n] &\to& X(U_i)
  }
  \right)
  \,,
$$

=--

([Dugger-Hollander-Isaksen 02, prop. 7.2](#DuggerHollanderIsaksen02)

+-- {: .num_remark}
###### Remark

If the [[topos]] $Sh(C)$ has [[point of a topos|enough points]] a morphism $f : Y \to X$ in $Sh(C)^{\Delta^{op}}$ is a hypercover if all its [[stalk]]s are acyclic [[Kan fibration]]s.

=--

In this form the notion of hypercover appears for instance in ([Brown 73](#Brown73)).

In some situations, we may be interested primarily in hypercovers that are built out of data entirely in the site $C$.  We obtain such hypercovers by restricting $X$ to be a discrete simplicial object which is representable, and each $Y_n$ to be a coproduct of representables.  This notion can equivalently be formulated in terms of diagrams $(\Delta/A) \to C$, where $A$ is some simplicial set and $(\Delta/A)$ is its [[category of simplices]].

## Examples

+-- {: .num_example}
###### Example

Consider the case that $X = const X_0$ is simplicially constant. Then the conditions on a morphism $Y \to X$ to be a hypercover is as follows.  

* in degree 0: $Y_0 \to X_0$ is a local epimorphism.

* in degree 1: The commuting diagram in question is

  $$
    \array{
      Y_1 &\to& X_0
      \\
      \downarrow && \downarrow^{\mathrlap{diag}}
      \\
      Y_0 \times Y_0 &\to& X_0 \times X_0
    }
    \,.
  $$

  Its [[pullback]] is $(Y_0 \times Y_0)_{X_0 \times X_0} X_0 \simeq Y_0 \times_{X_0} Y_0$, Hence the condition is that

  $Y_1 \to Y_0 \times_{X_0} Y_0$ is a local epimorphism.

* in degree 2: The commuting diagram in question is

  $$
    \array{
      Y_2 &\to& X_0
      \\
      \downarrow && \downarrow^{Id}
      \\
      (Y_1 \times_{Y_0} Y_1 \times_{Y_0}Y_1)_{\times_{Y_0 \times Y_0}}  Y_0
      &\to& X_0
    }
    \,.
  $$
 
  So the condition is that the vertical morphism is a local epi.

* Similarly, in any degree $n \geq 2$ the condition is that
  
  $$
    Y_n \to (\mathbf{cosk}_{n-1} Y)_n
  $$

  is a local epimorphism.

=--


## Properties


### Existence and refinements


#### Cech nerves

+-- {: .num_prop}
###### Proposition

For $U = \{U_i \to X\}$ a [[cover]], the [[Cech nerve]] projection $C(U) \to X$ is a hypercover of height 0.

=--

#### Over general sites
 {#OverGeneralSites}



+-- {: .num_prop #ExistenceOfSplitRefinements}
###### Proposition

Given any [[site]] $(\mathcal{C},J)$ and given a diagram of simplicial presheaves 

$$
  \array{
    && Y
    \\
    && \downarrow^{\mathrlap{hcov}}
    \\
    X' &\longrightarrow& X
  }
$$

where the vertical morphism is a hypercover, then there exists a completion to a [[commuting diagram]]

$$
  \array{
    Y' &\longrightarrow& Y
    \\
    \downarrow^{\mathrlap{hcov}} && \downarrow^{\mathrlap{hcov}}
    \\
    X' &\longrightarrow& X
  }
$$

where the left vertical morphism is a split hypercover, def. \ref{SplitHypercover}. 

Moreover, if $(\mathcal{D}, K)\to (\mathcal{C},J)$ is a [[dense subsite]] then $Y'$ as above exists such that it is simplicial-degree wise a [[coproduct]] of ([[representable functor|representables]] by) objects of $\mathcal{D}$.

=--

(e.g. [Low 14-05-26, lemma 8.2.20](#Low))

+-- {: .num_remark}
###### Remark

In particular taking $X'\to X$ in prop. \ref{ExistenceOfSplitRefinements} to be an identity, the proposition says that every hypercover may be refined by a split hypercover.

=--

(see also [Low 14-05-26, lemma 8.2.23](#Low))


#### Over Verdier sites
 {#OverVerdierSites}


+-- {: .num_defn}
###### Definition

A **[[Verdier site]]** is a [[small category]] with finite [[pullbacks]] equipped with a [[basis for a Grothendieck topology]] such that the generating [[covering]] maps $U_i \to X$ all have the property that their [[diagonal]]

$$
  U_i \to U_i \times_X U_i
$$

is also a generating covering. We say that $U_i \to X$ is **basal**.

=--

+-- {: .num_example}
###### Example

It is sufficient that all the $U_i \to X$ are [[monomorphism]]s. 

Examples include the standard [[open cover]]-topology on [[Top]]. 

=--

+-- {: .num_defn #BasalHypercover}
###### Definition

A **basal hypercover** over a [[Verdier site]] is a hypercover $U \to X$ such that for all $n \in \mathbb{N}$ the components of the maps into the matching object $U_n \to M U_n$ are basal maps, as above.

=--

+-- {: .num_theorem}
###### Theorem

Over a Verdier site, every hypercover may be refined by a split (def. \ref{SplitHypercover}) and basal hypercover (def. \ref{BasalHypercover}).

=--

This is ([Dugger-Hollander-Isaksen 02, theorem 8.6](#DuggerHollanderIsaksen02)).





### Hypercover homology {#HypercoverHomology}

Let $f : Y \to X$ be a hypercover. We may regard this as an object in the [[overcategory]] $Sh(C)/X$. By the discussion <a href="http://ncatlab.org/nlab/show/category+of+presheaves#RelWithOvercategories">here</a> this is equivalently $Sh(C/X)$. Write $Ab(Sh(C/X))$ for the category of abelian [[group object]]s in the [[sheaf topos]] $Sh(C/X)$. This is an [[abelian category]].

Forming in the sheaf topos the [[free functor|free]] abelian group on $f_n$ for each $n \in \mathbb{N}$, we obtain a simplicial abelian group object $\bar f \in Ab(Sh(C/X))^{\Delta}$. As such this has a [[Moore complex|normalized chain complex]] $N_\bullet(\bar f)$.

+-- {: .num_prop}
###### Proposition

For $f : Y \to X$ a hypercover, the [[chain homology]] of $N(\bar f)$ vanishes in positive degree and is the group of [[integer]]s in degree 0, as an object in $Ab(Sh(C)(X)$:

$$
  H_p(N(f)) \simeq 
  \left\{
    \array{
       0 & for \; p \geq 1
       \\
       \mathbb{Z} & for \; p = 0
    }
  \right.
  \,.
$$

=--

### Descent and cohomology
 {#DescentAndCohomology}

The following theorem characterizes the [[∞-stack]]/[[(∞,1)-sheaf]]-condition for the [[presentable (∞,1)-category|presentation]] of an [[(∞,1)-topos]] by a [[local model structure on simplicial presheaves]] in terms of descent along hypercovers.

+-- {: .num_theorem #DescentFromDescentAlongHypercovers}
###### Theorem

In the [[local model structure on simplicial presheaves]] $PSh(C)^{\Delta^{op}}$ an object is fibrant precisely if it is fibrant in the global [[model structure on simplicial presheaves]] and in addition satisfies [[descent]] along all hypercovers over representables that are degreewise [[coproduct]]s of representables.

=--

This is the central theorem in ([Dugger-Hollander-Isaksen 02](#DuggerHollanderIsaksen02)).

The following theorem is a corollary of this theorem, using the discussion at [[abelian sheaf cohomology]]. But historically it predates the above- theorem.

+-- {: .num_theorem}
###### Theorem
**(Verdier's hypercovering theorem)

For $X$ a [[topological space]] and $F$ a [[sheaf]] of [[abelian group]]s on $X$, we have that the [[abelian sheaf cohomology]] of $X$ with coefficients in $F$ is given

$$
  H^q(X, F) \simeq {\lim_{\to}}_{Y \to X} H^q(Hom_{Sh}(Y^\bullet,F))
$$

by computing for each hypercover $Y \to X$ the [[cochain cohomology]] of the [[Moore complex]] of the cosimplicial abelian group obtained by evaluating $F$ degreewise on the hypercover, and then taking  the [[colimit]] of the result over the [[poset]] of all hypercovers over $X$.

=--

A proof of this result in terms of the structure of a [[category of fibrant objects]] on the category of simplicial presheaves appears in ([Brown 73, section 3](#Brown73)).



## Reference

The concept of hypercovers was introduced for [[abelian sheaf cohomology]] in

*  [[Jean-Louis Verdier]], Expos&#233; V, sect. 7 of  [[SGA4]], 

An early standard reference founding [[étale homotopy theory]] is

* [[Michael Artin]], [[Barry Mazur]], _&#201;tale Homotopy_ , Lecture Notes in Mathematics 100, Springer- Verlag, Berline-Heidelberg-New York (1972).

The modern reformulation of their notion of hypercover in terms of simplicial presheaves is mentioned for instance at the end of section 2, on [p. 6](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf#page=6) of

* [[John Frederick Jardine]], _Fields Lectures: Simplicial presheaves_ ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))

A discussion of hypercovers of [[topological spaces]] and relation to [[étale homotopy type]] of [[smooth schemes]] and [[A1-homotopy theory]] is in 

* {#Isaksen01}[[Daniel Isaksen]], _&#201;tale realization of the $\mathbb{A}^1$-homotopy theory of schemes_, 2001 ([K-theory archive](http://www.math.uiuc.edu/K-theory/0495/))

* {#DuggerIsaksen05} [[Daniel Dugger]], [[Daniel Isaksen]], _Hypercovers in topology_, 2005 ([pdf](http://www.math.uiuc.edu/K-theory/0528/hypercover.pdf), [K-Theory archive](http://www.math.uiuc.edu/K-theory/0528/))


A discussion in a topos with enough points in in 

* {#Brown73} [[Kenneth Brown]], _[[BrownAHT|Abstract homotopy theory and generalized sheaf cohomology]]_, 1973


A thorough discussion of hypercovers over representables and their role in [[descent]] for simplicial presheaves is in

* {#DuggerHollanderIsaksen02} [[Daniel Dugger]], [[Sharon Hollander]], [[Daniel Isaksen]], _Hypercovers and simplicial presheaves_, Mathematical Proceedings of the Cambridge Philosophical Society. Vol. 136. No. 1., 2004. ([arXiv:0205027](http://arxiv.org/abs/math/0205027), [K-theory archive](http://www.math.uiuc.edu/K-theory/0563/))

On the Verdier hypercovering theorem see

* [[Kenneth Brown]], _[[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf Cohomology]]_

* [[John Frederick Jardine]], _The Verdier hypercovering theorem_ ([pdf](http://www.math.uwo.ca/~jardine/papers/preprints/Verdier4.pdf))

* [[Zhen Lin Low]], _Cocycles in categories of fibrant objects_, ([pdf](http://arxiv.org/abs/1502.03925v3))



Split hypercover refinement over general sites is discussed in 

* {#Low} [[Zhen Lin Low]], _[[Notes on homotopical algebra]]_

[[!redirects hypercovers]]

[[!redirects Verdier hypercover theorem]]
[[!redirects Verdier hypercovering theorem]]