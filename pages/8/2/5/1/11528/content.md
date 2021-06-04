
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given a [[simplicial group]] $G_\bullet$, the _Borel model structure_ is a [[model category]] structure on the [[category]] of [[simplicial sets]] equipped with $G$-[[action]] which presents the [[(∞,1)-category]] of [[∞-actions]] of the [[∞-group]] (see there) presented by $G$.

In the context of [[equivariant homotopy theory]] this is also called the "coarse model structure" (e.g. [Guillou, section 5](#Guillou)), since it is not equivalent to the "fine" homotopy theory of [[G-spaces]] which enters [[Elmendorf's theorem]].


## Definition


\begin{defn}\label{BorelModelStructure}

For $G_\bullet$ a [[simplicial group]] write 

* $\mathbf{B}G_\bullet$ for the one-object [[sSet-enriched category]] (here: a [[simplicial groupoid]]) whose [[hom-object]] is $G_\bullet$. 

* $sSetCat\big(\mathbf{B}G_\bullet, sSet\big)$ for the [[sSet]]-[[enriched functor category]] to [[SimplicialSets]].

* $sSetCat\big(\mathbf{B}G_\bullet, sSet\big)_{proj}$ for the projective [[model structure on functors]] (projective [[model structure on simplicial presheaves]]). 

This is the $G_\bullet$ *Borel model structure*, naturally a [[simplicial model category]] ([DDK 80, Prop. 2.4](#DDK80)).

\end{defn}

## Properties

### Cofibrant replacement and homotopy quotients/fixed points
 {#CofibrantReplacementAndHomotopyQuotientsFixedPoints}

\begin{prop}
The cofibrations $i \colon X \to Y$ in $sSetCat\big(\mathbf{B}G_\bullet, sSet\big)_{proj}$ (Def. \ref{BorelModelStructure}) are precisely those morphisms such that

1. the underlying morphism of [[simplicial sets]] is a [[monomorphism]];

1. the $G_\bullet$-[[action]] is a relatively [[free action]], i.e. [[free action|free]] on all [[simplices]] not in the [[image]] of $i$.

\end{prop}

This is ([DDK 80, Prop. 2.2. (ii)](#DDK80), [Guillou, Prop. 5.3](#Guillou)).



\begin{remark}
In particular this means that an object is [[cofibrant object|cofibrant]] 
in $sSetCat\big(\mathbf{B}G_\bullet, sSet\big)_{proj}$ if the $G_\bullet$-[[action]] on it is [[free action|free]]. 

Hence [[cofibrant replacement]] is obtained by forming the [[Cartesian product|product]] with the model $W G_\bullet$ for the total space of the [[universal principal bundle]] over $G_\bullet$ (see at _[[simplicial group]]_ for notation and more details).
\end{remark}

\begin{remark}
It follows that for $X, A \in sSetCat\big(\mathbf{B}G_\bullet, sSet\big)_{proj}$ the [[derived hom space]]

$$
  R Hom_G(X,A)
$$

models the Borel $G$-[[equivariant cohomology]] of $X$ with [[coefficients]] in $A$. 

In particular,if $A$ is [[fibrant object|fibrant]] (the underlying simplicial set is a [[Kan complex]]) then 

1. if the $G_\bullet$-action on $A$ is trivial, then 

   $$
     R Hom_G(X,A) 
       \simeq 
     Hom_G(W G \times X , A) 
       \simeq 
     Hom(W G \times_G X, A)
   $$

   is equivalently maps of [[simplicial sets]] out of the [[Borel construction]] on $X$;

1. if $X = \ast $ is the [[point]] then 

   $$
     R Hom_G(X,A) 
       \simeq 
     Hom_G(W G, A) 
       \simeq 
     Hom(\overline{W} G , A)  
       \simeq 
     A^{h G}
   $$

   is the [[homotopy fixed points]] of $A$.

\end{remark}



### Relation to the slice over the simplicial classifying space

\begin{prop}
  For $G$ a [[simplicial group]], there is a pair of [[adjoint functors]]
  $$
    sSetCat\big(\mathbf{B}G_\bullet, sSet\big)_{proj}
      \underoverset
        {\underset{ \big((-) \times W G\big)/G }{\longrightarrow}}
        {\overset{ (-) \times_{\overline{W}G} W G  }{\longleftarrow}}
        {\bot}
    sSet_{/\overline{W}H}
  $$
  which constitute a [[Quillen equivalence]] between the Borel model structure (Def. \ref{BorelModelStructure}) and the [[slice model structure]] of the [[classical model structure on simplicial sets]] slices over the [[simplicial classifying space]] $\overline{W}G$.,
  
\end{prop}

([DDK 80, Prop. 2.3](#DDK80)) Here the [[right adjoint]] forms [[associated bundles]] and the [[left adjoint]] forms [[homotopy fibers]].

In fact, these are [[sSet]]-[[enriched functors]] which induced an [[equivalence of (infinity,1)-categories]] between the [[simplicial localizations]]  $L_W sSetCat\big(\mathbf{B}G_\bullet, sSet\big)_{proj} \simeq L_W sSet_{/\overline{W}H}$ ([DDK 80, Prop. 2.5](#DDK80)).


This kind of relation is discussed in more detail at _[[∞-action]]_.


### Relation to the fine model structure of equivariant homotopy theory

The [[identity functor]] goves a [[Quillen adjunction]] between the Borel model structure and [[equivariant homotopy theory]] ([Guillou, section 5](#Guillou)).

The left adjoint is

$$
  L = id 
    \;\colon\; 
  G_\bullet Act_{coarse} 
    \longrightarrow 
  G_\bullet Act_{fine}
$$

from the Borel model structure to the genuine [[equivariant homotopy theory]].

Because:

First of all, by ([Guillou, theorem 3.12, example 4.2](#Guillou)) $sSet^{\mathbf{B}G_\bullet}$ does carry a fine model structure. By ([Guillou, last line of page 3](#Guillou)) the fibrations and weak equivalences here are those maps which are ordinary fibrations and weak equivalences, respectively, on $H$-[[fixed point]] simplicial sets, for all subgroups $H$. This includes in particular the trivial subgroup and hence the identity functor

$$
  R = id \;\colon\; G_\bullet Act_{fine} \longrightarrow G_\bullet Act_{coarse}
$$

is right Quillen.

## References

The model structure, the characterization of its cofibrations, and its equivalence to the [[slice model structure]] of $sSet$ over $\bar W G$ is due to

* {#DDK80} [[Emmanuel Dror]], [[William Dwyer]], [[Daniel Kan]], _Equivariant maps which are self homotopy equivalences_, Proc. Amer. Math. Soc. 80 (1980), no. 4, 670&#8211;672 ([jstor:2043448](http://www.jstor.org/stable/2043448))

This is mentioned in 

* {#Dwyer2008} [[William Dwyer]], exercise 4.2 in: _Homotopy theory of classifying spaces_, Lecture notes Copenhagen (June, 2008) [pdf](http://www.math.ku.dk/~jg/homotopical2008/Dwyer.CopenhagenNotes.pdf)

Discussion in relation to the "fine" model structure of [[equivariant homotopy theory]] which appears in [[Elmendorf's theorem]] is in 

* {#Guillou} [[Bert Guillou]], _A short note on models for equivariant homotopy theory_ ([pdf](http://www.math.uiuc.edu/~bertg/EquivModels.pdf), [[GuillouModelsForEquivariantHomotopyTheory.pdf:file]])



Discussion with the model of [[∞-groups]] by [[simplicial groups]] replaced by groupal [[Segal spaces]] is in 

* [[Matan Prasma]], _Segal Group Actions_ ([arXiv:1311.4749](http://arxiv.org/abs/1311.4749))

Discussion of a [[global equivariant homotopy theory|globalized]] model structure for actions of all simplicial groups is in

* [[Yonatan Harpaz]], [[Matan Prasma]], section 6.2 of _The Grothendieck construction for model categories_ ([arXiv:1404.1852](http://arxiv.org/abs/1404.1852))


[[!redirects Borel model structures]]

