
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

An **associated $\infty$-bundle** $E \to X$ is a [[fiber bundle]] in an [[(∞,1)-topos]] $\mathbf{H}$ with typical fiber $F \in \mathbf{H}$ that is classified by a [[cocycle]] $X \to \mathbf{B}\underline{Aut}(F)$ with coefficients in the [[delooping]] of the [[internalization|internal]] [[automorphism ∞-group]] of $F$.  We say this is _associated to_ the corresponding  $\underline{Aut}(F)$-[[principal ∞-bundle]]. 

More generally there should be notions of associated $\infty$-bundles whose fibers are objects in an [[(∞,n)-topos]] over $\mathbf{H}$ for some $n \gt 1$.

## Definition

Let $\mathbf{H}$ be an [[(∞,1)-topos]]. 

+-- {: .num_def}
###### Definition

For $V,X \in \mathbf{H}$ two objects, say a _$V$-[[fiber ∞-bundle]] over $X$_ is a [[morphism]] $E \to X$ (an object in the [[slice (∞,1)-topos]] $\mathbf{H}_{/X}$) such that there exists an [[effective epimorphism in an (∞,1)-category|effective epimorphism]] $U \to X$ and an [[(∞,1)-pullback]] square

$$
  \array{
    U \times V &\to& E
    \\
    \downarrow && \downarrow
    \\
    U &\to& X
  }
  \,.
$$ 

=--

+-- {: .num_def}
###### Definition

Let $G \in Grp(\mathbf{H})$ be an [[∞-group]] equipped with an 
[[∞-action]] $\rho$ on $V$. Then for $P \to X$ a $G$-[[principal ∞-bundle]] over $X$, the _$\rho$-associated $\infty$-bundle_ is

$$
  P \times_G V \to X
  \,,
$$

where $P \times_G V := (P \times V)//G$ is the homotopy quotient of the diagonal $G$-action.

=--

+-- {: .num_remark}
###### Remark

Below in _[Properties](#Properties)_ we see that every $\rho$-associated $\infty$-bundle is a $V$-fiber $\infty$-bundle and that every $V$-fiber $\infty$-bundle arises as associated to an  $\mathbf{Aut}(V)$-[[principal ∞-bundle]]

=--

## Properties 
 {#Properties}


### General

+-- {: .num_prop #Classification}
###### Proposition

For $V \in \mathbf{H}$, write $\mathbf{Aut}(V) \in Grp(\mathbf{H})$ for the internal [[automorphism ∞-group]] of $V$. This comes with a canonical action on $V$. Then the operation of sending an $\mathbf{Aut}$-[[principal ∞-bundle]] $P \to X$ to the associated $P \times_G V \to X$ establishes an equivalence

$$
  H^1(X, \mathbf{Aut}(V)) \simeq \{V-fiber\;\infty-bundles\}
  \,.
$$


=--

More specifically, if $\rho$ is an [[∞-action]] of $G$ on some $V \in \mathbf{H}$, then under the [[equivalence of (∞,1)-categories]]

$$
  G Act \simeq \mathbf{H}_{/\mathbf{B}G}
$$

it corresponds to a [[fiber sequence]]

$$
  \array{
    V &\to& V//G
    \\
    && \downarrow^{\mathrlap{\overline{\rho}}}
    \\
    && \mathbf{B}G
  }
$$

in $\mathbf{H}$. This is the **universal $\rho$-associated $V$-bundle** in that for $P \to X$ any $G$-[[principal ∞-bundle]] modulated by $g \colon X \to \mathbf{B}G$ we have a natural equivalence

$$
  P \times_G V \simeq g^* \overline{\rho}
  \,.
$$

This is discussed in ([NSS, section I 4.1](#NSS)). 


### Presentation in simplicial presheaves



In ([Wendt](#Wendt)), section 5.5, a [[presentable (infinity,1)-category|presentation]] of the general situation for [[n-localic (infinity,1)-topos|1-localic]] [[(∞,1)-toposes]] is given in terms of the [[model structure on simplicial presheaves]] (as discussed at [[models for ∞-stack (∞,1)-toposes]]) .

Under this presentation we have:

+-- {: .num_prop}
###### Proposition

The universal $F$-$\infty$-bundle $\mathbf{E} F \to \mathbf{B}Aut(F)$ is presented by the [[bar construction]]

$$
  F \to B(*, Aut(F), F) \to B(*, Aut(F), *)
  \,.
$$


=--

Compare [[universal principal ∞-bundle]].

## Examples

### Fibrations of topological spaces / simplicial sets

For the special case that $\mathbf{H} = $ [[∞Grpd]] and using the [[presentable (∞,1)-category|presentation]] by the [[model structure on topological spaces]]/[[model structure on simplicial sets]] the classification theorem \ref{Classification} reduces to the classical statement of ([Stasheff](#Stasheff), [May](#May)).

### $\infty$-Gerbes

In the case that the fiber $F$ is the [[delooping]] $F = \mathbf{B}G$ of an [[∞-group]] object $G$, the $\underline{Aut}(\mathbf{B}G)$-associated $\infty$-bundles are called **$G$-[[∞-gerbes]]**. See there for more details.

## Related concepts

* [[action]], [[∞-action]]

* [[representation]], [[∞-representation]]

* [[principal bundle]] / [[torsor]] / [[associated bundle]]

* [[principal 2-bundle]] / [[gerbe]] / [[bundle gerbe]]

* [[principal 3-bundle]] / [[2-gerbe]] / [[bundle 2-gerbe]]

* [[principal ∞-bundle]] / [[∞-gerbe]] / **associated $\infty$-bundle**

* [[vector bundle]]

* [[(∞,1)-vector bundle]]

## References
 {#References}

Early work on associated $\infty$-bundles takes place in the $(\infty,1)$-topos [[∞Grpd]] $\simeq$ [[Top]]. In

* [[Jim Stasheff]], _A classification theorem for fiber spaces_ , Topology 2 (1963) 239-246
 {#Stasheff}

* [[Jim Stasheff]], _H-spaces and classifying spaces: foundations and recent developments_. Algebraic topology (Proc. Sympos. Pure Math., Vol. XXII, Univ. Wisconsin, Madison, Wis., 1970), pp. 247&#8211;272. MR0321079 (47 #9612) 

a classification of [[fibrations]] of [[CW-complexes]] with given CW-complex fiber in terms of maps into a classifying CW-complex is given.

In 

* [[Daniel Gottlieb]], _The total space of universal fibrations._  Pacific J. Math. Volume 46, Number 2 (1973), 415-417. 

the total space of the universal $F$-[[fiber ∞-bundle]] in the pointed context is identified with $\mathbf{B}Aut_*(F)$ (the pointed [[automorphism ∞-group]]).

A generalization or more systematic account of the classification theory is then given in

* [[Peter May]], _Classifying Spaces and Fibrations_ Mem. Amer. Math. Soc. 155 (1975) ([pdf](http://www.math.uchicago.edu/~may/BOOKS/Classifying.pdf))
{#May}

This has been reproven in various guises, such as the statement of [[univalence]] in the [[model]] [[sSet]] for [[homotopy type theory]]. See the references at _[[univalence]]_ for more on this.

Generalizations with extra structure on the fibers are discussed in 

* Claudio Pacati, Petar Pavesic, Renzo Piccinini, _On the classification of $\mathcal{F}$-fibrations_, Topology and its applications 87 (1998) ([pdf](http://www.fmf.uni-lj.si/~pavesic/RESEARCH/On%20the%20classification%20of%20F-fibrations.pdf))

Consideration of associated $\infty$-bundles / [[fiber sequences]] in general [[n-localic (infinity,1)-topos|1-localic]] [[(∞,1)-toposes]] [[presentable (infinity,1)-category|presented]] by a [[model structure on simplicial presheaves]] (which subsumes the above case for the trivial site) is discussed in

* [[Matthias Wendt]], _Classifying spaces and fibrations of simplicial sheaves_ , Journal of  Homotopy and Related Structures 6(1), 2011, pp. 1--38.  ([arXiv](http://arxiv.org/abs/1009.2930)) ([published version](http://tcms.org.ge/Journals/JHRS/volumes/2011/volume6-1.htm))
{#Wendt}

Related discussion on the behaviour of [[fiber sequences]] under left [[Bousfield localization of model categories]] is in

* [[Matthias Wendt]], _Fibre sequences and localization of simplicial sheaves_ ([pdf](http://home.mathematik.uni-freiburg.de/arithmetische-geometrie/preprints/wendt-flocal.pdf))

Similar considerations and results are in 

* Martin Blomgren, [[Wojciech Chacholski]], _On the classification of fibrations_ ([arXiv:1206.4443](http://arxiv.org/abs/1206.4443))
 {#BlomgrenChacholski}

With the advent of [[(∞,1)-topos theory]] all these statements and their generalizations follow from the existence of [[object classifiers]] in an [[(∞,1)-topos]]. For the classical case in [[∞Grpd]] $\simeq$ [[Top]]${}^\circ$ [[sSet]]${}^\circ$ this is discussed in 

* _[object classifier in ∞Grpd](http://ncatlab.org/nlab/show/%28sub%29object+classifier+in+an+%28infinity%2C1%29-topos#ObjectClassifierInInfinityGroupoid)_,

which reproduces the classical results ([Stasheff](#Stasheff), [May](#May)).

For general [[(∞,1)-toposes]] the classification of associated $\infty$-bundles is discussed in section I 4.1 of 

* [[schreiber:Principal ∞-bundles -- theory, presentations and applications]] 

Models in [[rational homotopy theory]] of classifying spaces for homotopy types $Aut(F)$ go back to [[Sullivan]]'s remarks on the [[automorphism L-infinity algebra]]. Further developments are reviewed and developed in 

* [[Andrey Lazarev]], _Models for classifying spaces and derived deformation theory_ ([arXiv:1209.3866](http://arxiv.org/abs/1209.3866))



[[!redirects associated infinity-bundle]]
[[!redirects associated infinity-bundles]]
[[!redirects associated ∞-bundle]]
[[!redirects associated ∞-bundles]]

[[!redirects universal associated infinity-bundle]]
[[!redirects universal associated infinity-bundles]]
[[!redirects universal associated ∞-bundle]]
[[!redirects universal associated ∞-bundles]]

