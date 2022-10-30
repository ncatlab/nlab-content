

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### $(\infty,1)$-Topos theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of **Postnikov tower in an $(\infty,1)$-category** is the  generalization of the notion of [[Postnikov tower]] from the archetypical [[(∞,1)-category]] [[Top]]$\simeq$ [[∞Grpd]] to more general $(\infty,1)$-categories.

## Definition

+-- {: .num_prop}
###### Proposition

For $C$ a [[presentable (∞,1)-category]] the subcategory $C_{\leq n}$ of [[n-truncated object in an (∞,1)-category|n-truncated objects]] is a [[reflective (∞,1)-subcategory]]

$$
  C_{\leq n} \stackrel{\overset{\tau_{\leq n}}{\leftarrow}}{\hookrightarrow}
  C
  \,.
$$

=--


This is ([Lurie, prop. 5.5.6.18](#Lurie)).


We write 

$$
  \mathbf{\tau}_{\leq n} : C \stackrel{\tau_{\leq n}}{\to} C_{\leq n} \hookrightarrow C
$$

for the corresponding localization. For $X \in C$, we say that $\mathbf{\tau}_{\leq n} X$ is the **$n$-truncation of $X$**. 

The reflector of the reflective embedding provides morphisms

$$
  X \to \mathbf{\tau}_{\leq n} X
$$

from each object to its $n$-truncation.




+-- {: .num_defn}
###### Definition

A **Postnikov tower** for $X \in C$ is a diagram

$$
  X \to \cdots \to X_2 \to X_1 \to X_0
$$

such that each $X \to X_n$ exhibits $X_n$ as [[generalized the|the]] $n$-truncation of $X$.

=--

This is [[Higher Topos Theory|HTT, def. 5.5.6.23]].

+-- {: .num_defn}
###### Definition

A **Postnikov pretower** is a pre-tower

$$
  \cdots \to X_2 \to X_1 \to X_0
$$

(no initial $X$ on the left!) which exhibits each $X_n$ as the $n$-truncation of $X_{n+1}$.

We say **Postnikov towers converge** in the ambient [[(∞,1)-category]] if the [[forgetful functor|forgetful]] [[(∞,1)-functor]] from Postnikov towers to Postnikov pretowers is an [[equivalence of (∞,1)-categories]].

=--

This is ([Lurie, def. 5.5.6.23](#Lurie)).

## Examples

### In $\infty Grpd$

When the archetypical [[(∞,1)-topos]] [[∞Grpd]] is [[locally presentable (∞,1)-category|presented]] by the [[model structure on simplicial sets]], truncation is given by the the [[coskeleton]] endofunctor 
$\mathbf{cosk}_{n+1}$ on [[sSet]].

The unit of the adjunction $(tr_n \dashv cosk_n)$

$$
  \mathbf{\tau}_n : \mathbf{}X \to \mathbf{cosk}_n(X)
$$

sends an $\infty$-groupoid modeled as a [[Kan complex]] [[simplicial set]] to its $n$-[[truncated|truncation]].

Discussion of this can be found for instance in

* [[William Dwyer]], [[Dan Kan]], _An obstruction theory for diagrams of simplicial sets_ ([pdf](http://www.nd.edu/~wgd/Dvi/ObstructionTheoryForDiagrams.pdf))

*  [[John Duskin]] _Simplicial matrices and the nerves of weak $n$-categories I: Nerves of bicategories_ , TAC **9** no. 2, (2002). ([web](http://www.emis.de/journals/TAC/volumes/9/n10/9-10abs.html))


### In $\infty$-Lie groupoids

...

### In $E_\infty$-rings

The Postnikov tower of a connective [[E-∞ ring]] is a sequence of [[square-zero extensions]]. See [Basterra 99](#Basterra99) and [Lurie "Higher Algebra", section 8.4](#LurieAlgebra) (the result is due to [Kriz](#Kriz93)).

### In simplicial commutative rings

(A special case of the above:) The Postnikov tower of a [[simplicial commutative ring]] is a sequence of [[square-zero extensions]]. See [Toen-Vezzosi](#TVHAGII).

## Properties

### Criteria for convergence

We discuss conditions that ensure that Postnikov towers converge.

+-- {: .num_prop}
###### Proposition

In an [[(∞,1)-topos]] which is _locally_ of finite [[homotopy dimension]], Postnikov towers converge.

=--

This is ([Lurie, prop. 7.2.1.10](#Lurie)).

## Relation to other concepts

* At least if the ambient $(\infty,1)$-category is a [[locally contractible (∞,1)-topos]] $\mathbf{H}$, so that there is a notion of structured [[schreiber:path ∞-groupoid]]-functor $\mathbf{\Pi} : \mathbf{H} \to \mathbf{H}$, the [[homotopy fiber]]s of the morphisms $X \to \mathbf{\Pi}_n(X)$ into the Postnikov tower of $\mathbf{\Pi}(X)$ form the

  * [[Whitehead tower in an (∞,1)-topos|Whitehead tower in the (∞,1)-topos]] $\mathbf{H}$ of the object $X$.

* In the context of [[nonabelian cohomology]] in [[(∞,1)-topos]]es the fact that we have Postnikov towers has been called the [[Whitehead principle of nonabelian cohomology]].


## References

Section 6.5...

* {#Lurie} [[Jacob Lurie]], _[[Higher Topos Theory]]_
 
For $E_\infty$-rings:  section 8.4 of

* {#LurieAlgebra} [[Jacob Lurie]], _[[Higher Algebra]]_

and in more classical language, section 8 of

* {#Basterra99} [[M. Basterra]], _Andre-Quillen cohomology of commutative S-algebras_, J. Pure Appl. Algebra 144 (1999), no. 2, 111&#8211;143.

* {#Kriz93} [[Igor Kriz]], _Towers of $E_\infty$-ring spectra with an application to BP_, preprint, 1993.

For [[simplicial commutative rings]],

* {#TVHAGII} [[Bertrand Toen]], [[Gabriele Vezzosi]], _Homotopical Algebraic Geometry II: geometric stacks and applications_, [arXiv:math/0404373](http://arxiv.org/abs/math/0404373).


[[!redirects Postnikov tower in an (∞,1)-category]]
[[!redirects Postnikov system in an (∞,1)-category]]
[[!redirects Postnikov system in an (infinity,1)-category]]
