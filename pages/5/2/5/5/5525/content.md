
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

The term _discrete $\infty$-groupoid_ or _bare $\infty$-groupoid_ or _geometrically [[discrete object|discrete]] [[geometric homotopy type]]_ is essentially synonymous to just _[[∞-groupoid]]_ or just _[[homotopy type]]_. It is used for emphasis in contexts where one considers $\infty$-groupoids with extra [[geometric homotopy type|geometric structure]] (e.g. [[cohesive (∞,1)-topos|cohesive]] [[stuff, structure, property|structure]]) to indicate that this extra structure is being disregarded, or rather that the special case of [[discrete space|discrete]] such structure is considered.

## Definition

+-- {: .un_observation}
###### Observation

The [[terminal object in an (∞,1)-category|terminal]] [[(∞,1)-sheaf (∞,1)-topos]] [[∞Grpd]] is trivially a [[cohesive (∞,1)-topos]], where each of the defining four [[(∞,1)-functor]]s $(\Pi \dashv Disc \dashv \Gamma \dashv coDisc) : \infty Grpd \to \infty Grpd$ is an [[equivalence of (∞,1)-categories]]. 

=--


+-- {: .un_defn}
###### Definition

In the context of [[cohesive (∞,1)-topos]]es we say that [[∞Grpd]] defines **discrete cohesion** and refer to its objects as **discrete $\infty$-groupoids**.

More generally, given any other [[cohesive (∞,1)-topos]] 

$$
  (\Pi \dashv Disc \dashv \Gamma \dashv codisc) : \mathbf{H}  \stackrel{\overset{Disc}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
$$

the [[inverse image]] $Disc$ of the [[global section]] functor is a [[full and faithful (∞,1)-functor]] and hence embeds [[∞Grpd]] as a full [[sub-(∞,1)-category]] of $\mathbf{H}$. A general object in $\mathbf{H}$ is a _cohesive $\infty$-groupoid_ . We say $X \in \mathbf{H}$ is a **discrete $\infty$-groupoid** if it is in the [[image]] of $Disc$.

=--

+-- {: .un_remark}
###### Remark

This generalizes the traditional use of the terms [[discrete space]] and [[discrete group]]: 

* a [[discrete space]] is equivalently a 0-[[truncated]] discrete $\infty$-groupoid;

* a [[discrete group]] is equivalently a 0-[[truncated]] [[group object in an (∞,1)-category|group object]] in discrete $\infty$-groupoids.

=--

## Structures in $Disc\infty Grpd$

We discuss now some of the general abstract [[cohesive (∞,1)-topos -- structures|structures in a cohesive (∞,1)-topos]] realized in discrete $\infty$-groupoids.


### Geometric homotopy and Galois theory 
 {#TopAsCohesiveInfinTopos}

We discuss the general absatract notion of geometric homotopy in cohesive $(\infty,1)$-toposes (see <a href="http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+structures#Homotopy">here</a>) in the context of discrete cohesion.

By the [[homotopy hypothesis]]-theorem the [[(∞,1)-topos]]es [[Top]] and [[∞Grpd]] are [[equivalence of (∞,1)-categories|equivalent]], hence indistinguishable by general abstract constructions in [[(∞,1)-topos theory]]. However, in practice it can be useful to distinguish them as two different [[presentable (∞,1)-category|presentations]] for an equivalence class of $(\infty,1)$-toposes.

For that purposes consider the following

+-- {: .un_defn}
###### Definition

Define the [[quasi-categories]]

$$
  Top := N(Top_{Quillen})^\circ 
$$

and

$$
  \infty Grpd := N(sSet_{Quillen})^\circ 
  \,,
$$

where on the right we have the standard [[model structure on topological spaces]] $Top_{Quillen}$ and the standard [[model structure on simplicial sets]] $sSet_{Quillen}$  and $N((-)^\circ)$ denotes the [[homotopy coherent nerve]] of the [[simplicial category]] given by the full [[sSet]]-subcategory of these [[simplicial model categories]] on fibrant-cofibrant objects.

=--

For 

$$
  ({|-| \dashv Sing}) : Top_{Quillen} \stackrel{\overset{{|-|}}{\leftarrow}}{\underset{Sing}{\to}} sSet_{Quillen}
$$

the standard [[Quillen equivalence]] of the [[homotopy hypothesis]]-theorem given by the [[singular simplicial complex]]-functor and [[geometric realization]], write

$$
  (\mathbb{L} {|-|} \dashv \mathbb{R}Sing) : 
  Top 
    \stackrel{\overset{\mathbb{L}{|-|}}{\leftarrow}}{\underset{\mathbb{R}Sing}{\to}}
  \infty Grpd
$$

for the corresponding [[derived functor]]s (the image under the [[homotopy coherent nerve]] of the restriction of ${|-|}$ and $Sing$ to fibrant-cofibrant objects followed by functorial fibrant-cofibrant replacement) that constitute a pair of [[adjoint (∞,1)-functor]]s modeled as morphisms of [[quasi-categories]].

Since this is an [[equivalence of (∞,1)-categories]] either functor serves as the [[left adjoint]] and [[right adjoint]] and so we have

+-- {: .un_observation}
###### Observation

[[Top]] is exhibited a [[cohesive (∞,1)-topos]] over [[∞Grpd]] by setting

$$
  (\Pi \dashv Disc \dashv \Gamma \dashv coDisc)
  :
  Top
    \stackrel{\overset{\mathbb{R}Sing}{\to}}{\stackrel{\overset{\mathbb{L}{|-|}}{\leftarrow}}{\stackrel{\overset{\mathbb{R}Sing}{\to}}{\underset{\mathbb{L}{|-|}}{\leftarrow}}}}
  \infty Grpd
  \,.
  \,.
$$

In particular a presentation of the intrinsic [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] is given by the familiar [[singular simplicial complex]] construction

$$
  \Pi(X) \simeq \mathbb{R} Sing X
  \,.
$$


=--

+-- {: .un_remark}
###### Remark

While degenerate, it is sometimes useful to make this example of a [[cohesive (∞,1)-topos]] explicit. For instance it allows to think of simplicial models for topological fibrations in terms of topological [[higher parallel transport]]. Some remarks on this are in <a href="http://ncatlab.org/nlab/show/higher+parallel+transport#FlatInTop">Flat higher parallel transport in Top</a>.


=--

+-- {: .un_remark}
###### Remark

Notice that the [[topology]] that enters the explicit construction of the objects in [[Top]] here does _not_ show up as [[cohesive (∞,1)-topos|cohesive structure]]. A [[topological space]] here is a model for a _discrete_ $\infty$-groupoid, the [[topology]] only serves to allow the construction of $Sing X$.
For discussion of $\infty$-groupoids equipped with genuine _topological cohesion_ see [[Euclidean-topological ∞-groupoid]].

=--


### Cohomology and principal $\infty$-bundles

We discuss the general abstract notion of cohomology and principal $\infty$-bundles a 
in cohesive $\infty$-toposes (see <a href="http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+structures#Cohomology">here</a>) in the context of  discrete cohesion.

+-- {: .num_defn}
###### Definition

  Write $\mathrm{sGrp} = \mathrm{Grp}(\mathrm{sSet})$ 
 for the category of [[simplicial group]]s. 

=--

A classical reference is section 17 of [May](#May).

+-- {: .num_prop}
###### Proposition
 {#DiscreteLoopingDelooping}

The category $\mathrm{sGrpd}$ inherits a [[model category]] structure [[transferred model structure|transferred]] along the
forgetful functor $F : \mathrm{sGrp} \to \mathrm{sSet}$.
  
The category $\mathrm{sSet}_0 \hookrightarrow \mathrm{sSet}$ of reduced simplicial sets (simplicial sets with a single vertex) carries a model category structure whose weak equivalences and cofibrations are those of $\mathrm{sSet}_{\mathrm{Quillen}}$.
    
There is a [[Quillen equivalence]]
$$
  (G \dashv \bar W)
  :
  sGrp
   \stackrel{\overset{G}{\leftarrow}}{\underset{\bar W}{\to}}
  sSet_{0}
$$

which [[presentable (infinity,1)-category|presents]] the abstract [[looping and delooping]] equivalence of $\infty$-categories

 $$
   (\Omega \dashv \mathbf{B})
   :
   \infty Grpd
    \stackrel{\overset{\Omega}{\leftarrow}}{\underset{B}{\to}}
   \infty Grpd_{connected}
   \,,
$$

=--

The model structures and the Quillen equivalence are classical, discussed in  ([GoerssJardine, section V](#GoerssJardine))
 
This means on abstract grounds that for $G$ a [[simplicial group]], $\bar W G \in \mathrm{sSet}$ is a model of the
[[classifying space|classifying]] [[delooping]] object $\mathbf{B}G$ for discrte $G$-[[principal ∞-bundles]]. 
The following statements assert that these principal $\infty$-bundles themselves can  be modeled as ordinary [[simplicial principal bundle]]s

+-- {: .num_defn}
###### Definition

 For $G$ a [[simplicial group]] and $\bar W G$  the model for $\mathbf{B}G$ given by the above proposition, write
  
$$
  W G \to \bar W G
$$
 
for the simplicial [[decalage]] on $\bar W G$.

=--

This characterization of the object going by the classical name $W G$ is made fairly  explicit in ([Duskin, p. 85](#Duskin)).

+-- {: .num_prop}
###### Proposition

The morphism $W G \to \bar W G$ is a Kan fibration resolution of the point inclusion ${*} \to \bar W G$. 

=--

This follows directly from the characterization of $W G \to \bar W G$ by [[decalage]].
Pieces of this statement appear in ([May](#May)): lemma 18.2 there gives the fibration property, prop. 21.5 the contractibility of $W G$. 

+-- {: .num_cor}
###### Corollary
 For $G$ a [[simplicial group]], the sequence of simplicial sets

$$
  G \to W G \to \bar W G
$$

is a presentation of the [[fiber sequence]]
 
$$
  G \to * \to \mathbf{B}G
  \,.
$$

Hence $W G \to \bar W G$ is a model for the universal $G$-principal discrete $\infty$-bundle (see [[universal principal ∞-bundle]]):

every $G$-principal discrete $\infty$-bundle $P \to X$ in $\infty \mathrm{Grpd}$, which  by definition is a [[homotopy fiber]]

$$
  \array{
    P &\to& * 
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow
    \\
    X &\to& \mathbf{B}G
  }
$$

in [[∞Gpd]], is presented in the standard [[model structure on simplicial sets]] by the ordinary [[pullback]]

$$
  \array{
    P &\to& W G
    \\
    \downarrow && \downarrow
    \\
    X &\to& \bar W G
  }
  \,.
$$

=--

The explicit statement that the sequence $G \to W G \to \bar W G$ is a model for the looping fiber sequence appears on p. 239 of _[[Crossed Menagerie]]_ .
The universality of $W G \to \bar W G$ for $G$-principal simplicial bundles is the  topic of section 21 in ([May](#May)), where however it is not made explicit that the "[[twisted cartesian product]]s" considered there are precisely the models for the 
pullbacks as above. This is made explicit on page 148 of _[[Crossed Menagerie]]_.

In _[[Euclidean-topological ∞-groupoid]]_ we discuss how this model of discrete principal $\infty$-bundles
by simplicial principal bundles lifts to a model of topological principal $\infty$-bundles
by simplicial topological bundles principal over 
[[simplicial topological group]]s.


## Related concepts

* [[discrete space]]

* [[discrete group]]

* [[discrete groupoid]]

[[!include geometries of physics -- table]]

## References


[[simplicial group|Simplicial groups]] and [[simplicial principal bundles]] are discussed in

* [[Peter May]], _Simplicial Objects in Algebraic Topology_ ([djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu)).
 {#May}

and section V of

* [[Paul Goerss]] and [[Rick Jardine]], 1999, _Simplicial Homotopy Theory_, number 174 in Progress in Mathematics, Birkhauser. ([ps](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html))
 {#GoerssJardine}

The relation of $W G \to \bar W G$ to [[decalage]] is mentioned on p. 85 of

* [[John Duskin]], _Simplicial methods and the interpretation of "triple" cohomology_, number  163 in Mem. Amer. Math. Soc., 3, Amer. Math. Soc. (1975)
 {#Duskin}

Discrete cohesion is the topic of section 3.1 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ , 

where much of the above material is taken from.


[[!redirects geometrically discrete infinity-groupoids]]

[[!redirects geometrically discrete ∞-groupoid]]
[[!redirects geometrically discrete ∞-groupoids]]


[[!redirects discrete infinity-groupoid]]

[[!redirects discrete ∞-groupoid]]

[[!redirects discrete ∞-groupoids]]
[[!redirects discrete infinity-groupoids]]

[[!redirects Disc∞Grpd]]

[[!redirects discrete ∞-group]]
[[!redirects discrete ∞-groups]]


[[!redirects discrete infinity-group]]
[[!redirects discrete infinity-groups]]

[[!redirects geometrically discrete homotopy type]]
[[!redirects geometrically discrete homotopy types]]

[[!redirects Discrete∞Groupoid]]
[[!redirects Discrete∞Groupoids]]
[[!redirects Discrete∞Grpd]]
