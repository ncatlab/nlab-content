
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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


+-- {: .un_defn}
###### Definition

Let 

$$
  (L \dashv i) : Sh(C) \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow}
  PSh(C)
$$

be the [[geometric embedding]] defining a [[sheaf topos]] $Sh(C)$ into a [[presheaf topos]] $PSh(C)$. A morphism

$$
  (Y \stackrel{f}{\to} X) \in PSh(C)^{\Delta^{op}}
$$

in the [[category of simplicial objects]] in $PSh(C)$, hence the category of [[simplicial presheaves]], is called a **hypercover** if for all $n \in \mathbb{N}$ the canonical morphism

$$
  Y_{n} \to (\mathbf{cosk}_{n-1} Y)_n \times_{(\mathbf{cosk}_{n-1} X)_n} X_n
$$

in $PSh(C)$ are [[local epimorphism]]s (in other words, $f$ is a "[[Reedy model structure|Reedy]] local-epimorphism").  Here $\mathbf{cosk}_n : PSh(C)^{\Delta^{op}} \to PSh(C)^{\Delta^{op}}$ is the [[coskeleton]] functor in degree $n$.

In low degree the local epimorphisms here are  

* in degree 0: $Y_0 \to X_0$;

* in degree 1: $Y_1 \to Y_0 \times_X Y_0$

* and so on.

A hypercover is called **bounded** by $n \in \mathbb{N}$ if for all $k \geq n$ the morphisms $Y_{k} \to (\mathbf{cosk}_{k-1} Y)_k \times_{(\mathbf{cosk}_{k-1} X)_k} X_k$ are [[isomorphism]]s.

The smallest $n$ for which this holds is called the **height** of the hypercover.

A hypercover that also satisfies a cofibrancy condition in the projective [[local model structure on simplicial presheaves]] (being locally a coproduct of represetables with degenerate cells splitting of as a direct summand) is called a **[[split hypercover]]

=--

+-- {: .un_remark}
###### Remark

This is equivalent to saying that $f : Y \to X$ is a _local_ acyclic fibration: for all $U \in C$ and $n \in \mathbb{N}$ every lifting problem

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

+-- {: .un_remark}
###### Remark

If the [[topos]] $Sh(C)$ has [[point of a topos|enough points]] a morphism $f : Y \to X$ in $Sh(C)^{\Delta^{op}}$ is a hypercover if all its [[stalk]]s are acyclic [[Kan fibration]]s.

=--

In this form the notion of hypercover appears for instance in ([Brown](#Brown)).

In some situations, we may be interested primarily in hypercovers that are built out of data entirely in the site $C$.  We obtain such hypercovers by restricting $X$ to be a discrete simplicial object which is representable, and each $Y_n$ to be a coproduct of representables.  This notion can equivalently be formulated in terms of diagrams $(\Delta/A) \to C$, where $A$ is some simplicial set and $(\Delta/A)$ is its [[category of simplices]].


## Properties


+-- {: .un_prop}
###### Proposition

For $U = \{U_i \to X\}$ a [[cover]], the [[Cech nerve]] projection $C(U) \to X$ is a hypercover of height 0.

=--

### Hypercover homology {#HypercoverHomology}

Let $f : Y \to X$ be a hypercover. We may regard this as an object in the [[overcategory]] $Sh(C)/X$. By the discussion <a href="http://ncatlab.org/nlab/show/category+of+presheaves#RelWithOvercategories">here</a> this is equivalently $Sh(C/X)$. Write $Ab(Sh(C/X))$ for the category of abelian [[group object]]s in the [[sheaf topos]] $Sh(C/X)$. This is an [[abelian category]].

Forming in the sheaf topos the [[free functor|free]] abelian group on $f_n$ for each $n \in \mathbb{N}$, we obtain a simplicial abelian group object $\bar f \in Ab(Sh(C/X))^{\Delta}$. As such this has a [[Moore complex|normalized chain complex]] $N_\bullet(\bar f)$.

+-- {: .un_prop}
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

The following theorem characterizes the [[∞-stack]]/[[(∞,1)-sheaf]]-condition for the [[presentable (∞,1)-category|presentation]] of an [[(∞,1)-topos]] by a [[local model structure on simplicial presheaves]] in terms of descent along hypercovers.

+-- {: .un_prop}
###### Theorem

In the [[local model structure on simplicial presheaves]] $PSh(C)^{\Delta^{op}}$ an object is fibrant precisely if it is fibrant in the global [[model structure on simplicial presheaves]] and in addition satisfies [[descent]] along all hypercovers over representables that are degreewise [[coproduct]]s of representables.

=--

This is the central theorem in ([DuggerHollanderIsaksen](#DuggerHollanderIsaksen)).

The following theorem is a corollary of this theorem, using the discussion at [[abelian sheaf cohomology]]. But historically it predates the above theorem.

+-- {: .un_prop}
###### Theorem
**(Verdier's hypercovering theorem)

For $X$ a [[topological space]] and $F$ a [[sheaf]] of [[abelian group]]s on $X$, we have that the [[abelian sheaf cohomology]] of $X$ with coefficients in $F$ is given

$$
  H^q(X, F) \simeq {\lim_{\to}}_{Y \to X} H^q(Hom_{Sh}(Y^\bullet,F))
$$

by computing for each hypercover $Y \to X$ the [[cochain cohomology]] of the [[Moore complex]] of the cosimplicial abelian group obtained by evaluating $F$ degreewise on the hypercover, and then taking  the [[colimit]] of the result over the [[poset]] of all hypercovers over $X$.

=--

A proof of this result in terms of the structure of a [[category of fibrant objects]] on the category of simplicial presheaves appears in ([Brown, section 3](#Brown)).

## Reference

An early standard reference is

* M. Artin and B. Mazur, _&Eacute;tale Homotopy_ , Lecture Notes in Mathematics 100, Springer- Verlag, Berline-Heidelberg-New York (1972).

The modern reformulation of their notion of hypercover in terms of simplicial presheaves is mentioned for instance at the end of section 2, on [p. 6](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf#page=6) of

* Jardine, _Fields Lectures: Simplicial presheaves_ ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))

A discussion in a topos with enough points in in 

* Kenneth Brown, _[[BrownAHT|Abstract homotopy theory and generalized sheaf cohomology]]_
{#Brown}

A thorough discussion of hypercovers over representables and their role in [[descent]] for simplicial presheaves is in

* [[Daniel Dugger]], [[Sharon Hollander]], [[Daniel Isaksen]], _Hypercovers and simplicial presheaves_ ([web](http://www.math.uiuc.edu/K-theory/0563/))
{#DuggerHollanderIsaksen}


[[!redirects hypercovers]]