
> under re-construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea


## Definitions

The notion of *local system* exists in several different forms, each trying to capture some basic intuition in an appropriate language  for the applications that are being considered. For the moment we will not enquire too deeply as to the exact relationships between them 


We start with a 'geometric' definition and then give the [[sheaf]]-theoretic one.

### Geometric definition ##

A **local system** on a topological space $X$ with coefficients in a category $A$ is a [[functor]]

$$
  tra : \Pi_1(X) \to A
$$

from the [[fundamental groupoid]] $\Pi_1(X)$ of $X$ to $A$. 
The category of local systems on $X$ with coefficients in $A$ is the [[functor category]]

$$
  [\Pi_1(X), A]
  \,.
$$


### Sheaf-theoretic definition


+-- {: .un_defn}
###### Definition

A **local system** is a [[locally constant sheaf]] on a [[topological space]] $X$ (or manifold, analytic manifold, or algebraic variety) whose stalk is a finite-dimensional vector space. 

=--

> well, in some areas it is assumed to take values in vector spaces, in other not 

+-- {: .un_lemma}
###### Lemma

On a connected topological space this is the same as a sheaf of sections of a finite-dimensional vector bundle equipped with flat connection; and it also corresponds to the [[representations]] of the [[fundamental group]] $\pi_1(X,x_0)$ in the typical stalk. On an analytic manifold or a variety, there is an equivalence between the category of non-singular coherent 
$D_X$-[[D-module|modules]] and local systems on $X$.
=--


##Examples

...

## Related entries

* [[simplicial local system]]: within Sullivan's (1977) theory of _Infinitesimal computations in topology_, he refers to 'local systems' several times. This seems to be simplicial in nature. [[simplicial local system|This]] entry explores some of the uses of that notion based on Halperin's lecture notes on minimal models

  * D. Sullivan, _Infinitesimal computations in topology_ ([pdf](http://archive.numdam.org/ARCHIVE/PMIHES/PMIHES_1977__47_/PMIHES_1977__47__269_0/PMIHES_1977__47__269_0.pdf))

* [[D-module]]

* [[abelian sheaf cohomology]]






## Expositions

A blog exposition of some aspects of local system is developed here:

* David Speyer: _Three ways of looking at a local system_

  * [Introduction and connection to cohomology theories](http://sbseminar.wordpress.com/2009/04/20/three-ways-of-looking-at-a-local-system-introduction-and-connection-to-cohomology-theories/)


  * [the path groupoid approach](http://sbseminar.wordpress.com/2009/04/21/local-systems-the-path-groupoid-approach/)

  * [the infinitesimal perspective](http://sbseminar.wordpress.com/2009/04/30/three-ways-of-looking-at-a-local-system-the-infinitesimal-perspective/)

  * [the infinitesimal site](http://sbseminar.wordpress.com/2009/05/06/the-infinitesimal-site/)

***


## A general picture {#nPOV}

+-- {: .query}

[[Urs Schreiber]]: I find the above entry so far a bit of a mess. It is lacking a good [[nPOV]] elegant global picture from which all the details then drop out automatically. Here is a proposal for what that could be.

=--

We try to give the general abstract [[nPOV]] on local systems.

In the context of a given [[(∞,1)-topos]] $\mathbf{H} = Sh_{(\infty,1)}(X)$ of [[∞-stack]]s on $C$, whose objects we think of as [[space]]s, for every [[object]] $X \in \mathbf{H}$ and [[pointed object]]$(* \to A) \in \mathbf{H}$,  a [[morphism]] $X \to A$ is a [[cocycle]] that [[homotopy fiber|classifies]] an $A$-[[principal ∞-bundle]] $P \to X$ over $X$.

A **local system** is the special case of this where, equivalently, 

* the [[principal ∞-bundle]] $P$ is like a [[covering space]] for $X$;

* the coefficient object $A$ is a [[constant ∞-stack]] on $C$ -- $A = LConst \mathcal{A}$ for some $\mathcal{A} \in \infty Grpd$;

* the [[homotopy fiber|classifying]] [[cocycle]] $X \to A$ exhibits an $\mathcal{A}$-valued [[locally constant ∞-stack]] on $X$.

Here a [[constant ∞-stack]] $A$ is an object in the image of

$$
  LConst : \infty Grpd \simeq PSh_{(\infty,1)}(*)
  \stackrel{const}{\to}
  PSh_{(\infty,1)}(C)
  \stackrel{L}{\to}
  Sh_{(\infty,1)}(X)
  \,,
$$

where $L$ is [[∞-stackification]]. If this has a [[left adjoint]] $\Pi \dashv LConst$ then $\Pi(X)$ is the bare geometric [[schreiber:path ∞-groupoid]] of $X$, and by the [[adjunction]] we have that $(A = LConst \mathcal{A})$-local systems are equivalent to [[(∞,1)-functor|∞-functors]] $\Pi(X) \to \mathcal{A}$:

$$
  Loc(X,A) = \mathbf{H}(X,A) \simeq \infty Grpd(\Pi(X), \mathcal{A})
  \,.
$$

With this the fourth characterization of an $\mathcal{A}$-valued local system on $X$ is:

* a [[representation]] of the [[schreiber:path ∞-groupoid]] $\Pi(X)$ on $\mathcal{A}$.

In the special case that $\mathcal{A} = Core{\infty FinGrpd}$ is the [[core]] of the [[(∞,1)-category]] of finite [[∞-groupoid]]s, $\mathcal{A}$-valued local systems on $X$ are precisely genuine [[locally constant ∞-stack]]s on $X$. Conversely,we may think of a local system as a generalization of a locally constant $\infty$-stack, which may take values in something richer than just finite $\infty$-groupoids.


## References

An early version of the definition of local system appears in

* [[Norman Steenrod]]: _Homology with local coefficients_, Annals 44 (1943) pp. 610 - 627,

This is before the formal notion of [[sheaf]] was published by [[Jean Leray]].  (Wikipedia's entry on [Sheaf theory](http://en.wikipedia.org/wiki/Sheaf_%28mathematics%29#History) is interesting for its historical perspective on this.)

A definition  appears as an exercise in 

* [[Edwin Spanier]], 1966, Algebraic Topology , McGraw Hill. (republished by Springer, 1982).

on page 58 : 

>_A local system on a space $X$ is a covariant functor from the fundamental groupoid of $X$ to some category._

A clear-sighted description of locally constant $(n-1)$-stacks / $n$-local systems as sections of constant $n$-stacks is in

* [[Pietro Polesello]], [[Ingo Waschkies]], Higher monodromy, Homology, Homotopy and Applications, Vol. 7(2005), No. 1, pp. 109-150;
[arXiv:0407507](http://arxiv.org/abs/math/0407507)

for [[locally constant stack]]s on [[topological space]]s. The above formulation is pretty much the evident generalization of this to general [[(∞,1)-topos]]es.

[[!redirects local systems]]
