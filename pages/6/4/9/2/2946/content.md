
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Most of the earliest instances of [[limits]] and [[colimits]] used in mathematics were for [[diagrams]] indexed by the [[partially ordered set]] of [[natural numbers]], which we now call _[[sequential limit|sequential]] (co)limits_.  Many of the nice features of these (co)limits apply more generally to _[[codirected limits]]_ and _[[directed colimits]]_, where the indexing category is a (co)-[[directed set]] (much as [[sequences]] in [[topology]] generalise fruitfully to [[nets]]).  A _filtered (co)limit_ is a further generalisation of this, essentially removing the requirement that the indexing category be a [[poset]] while preserving the directedness aspect in a [[categorification|categorified]] way.

Another very important class of early limits and colimits involved situations that generalised [[intersections]] and [[unions]].  If one is looking at a [[family of subsets]] of some [[set]], then one can close it up under finite intersections and/or unions (if they are not already included) and use it to index diagrams.  For instance, the family of [[continuous functions]] defined on [[open neighbourhoods]] of some point in a [[topological space]] will have this property.  It was noticed that these limits and colimits behaved very nicely and a closer look showed that it was the _(co)filtering_ nature of the indexing category that was the key.  This also leads us to filtered (co)limits.


So, a _filtered colimit_ is a [[colimit]] over a [[diagram]] from a [[filtered category]], and a _cofiltered limit_ (sometimes called a filtered limit) is a [[limit]] over a [[diagram]] from a [[cofiltered category]]. Taken in a suitable category such as [[Set]], **a colimit being filtered is equivalent to its commuting with [[finite limits]]**.

More generally, for $\kappa$ a [[regular cardinal]], a _$\kappa$-filtered colimit_ is one over a $\kappa$-filtered category (and dually), and when taken with values in [[Set]] these are precisely the colimits that commute with $\kappa$-[[small limit]]s. 


## Definition

+-- {: .num_defn}
###### Definition

A __filtered colimit__ or **finitely filtered colimit** is a [[colimit]] of a [[functor]] $F\colon D \to C$ where $D$ is a [[filtered category]].  

For $\kappa$ a [[regular cardinal]] a **$\kappa$-filtered colimit** is one over a $\kappa$-filtered category.


Similarly, a __cofiltered limit__ is a [[limit]] of a functor $F\colon D \to C$ where $D$ is a [[cofiltered category]], or equivalently of a [[contravariant functor]] $F\colon D \to C$ (that is a functor $F\colon D^{op} \to C$) where $D$ is a filtered category.  

=--

+-- {: .num_remark}
###### Remark

A cofiltered limit may also be called a __filtered limit__ (although this can be unclear); the respective terms __filtered [[direct limit]]__ and __filtered [[inverse limit]]__ are also popular.

=--

A [[functor]] that preserves all finitely filtered colimits is called a _[[finitary functor]]_ .



## Properties 
 {#Properties}

### $\kappa$-Filtered colimits commute with $\kappa$-small limits

The following is the crucial property of filtered colimits: that they [[commutativity of limits with colimits|commute]] with [[finite limits]].

\begin{remark}
For $C$ and $D$ two [[diagram]] categories and

$$
  F \,\colon\, C \times D \longrightarrow Set
$$

a [[diagram]], there is a canonical morphism

$$
  \lambda
  \,\colon\,
  \underset{\underset{C}{\longrightarrow}}{\lim} 
  \;
  \underset{\underset{D}{\longleftarrow}}{\lim} 
  \,
  F
  \longrightarrow 
  \underset{\underset{D}{\longleftarrow}}{\lim} 
  \;
  \underset{\underset{C}{\longrightarrow}}{\lim} 
  \,
  F
$$

from the [[colimit]] over $C$ of the [[limit]] over $D$ to the limit over $D$ of the colimit over $C$ of $F$:

$\lambda$ is given by a [[cone]], whose components

$$
  \lambda_d 
  \,\colon\, 
  \underset{\underset{C}{\longrightarrow}}{\lim} 
  \;
  \underset{\underset{D}{\longleftarrow}}{\lim} 
  \,
  F
    \longrightarrow
  \underset{\underset{C}{\longrightarrow}}{\lim} 
  \,
  F(-,d)
$$

are in turn given by a [[cocone]] with components

$$
  (\lambda_d)_c 
  \,\colon\, 
  \underset{\underset{D}{\longleftarrow}}{\lim} 
  \,
  F(c,-)
    \longrightarrow
  \underset{\underset{C}{\longrightarrow}}{\lim} 
  \,
  F(-,d)
  \,.
$$

This finally take to have as components

$$
  \underset{\underset{D}{\longleftarrow}}{\lim} 
  \,
  F(c,d)
    \longrightarrow
  F(c,d)
    \longrightarrow
  \underset{\underset{C}{\longrightarrow}}{\lim} 
  \,
  F(c,d)
  \,.
$$

One checks that this indeed implies that all the components are natural and gives the existence of  the original morphism.

Notice that in general $\lambda$ is _not_ an [[isomorphism]].
\end{remark}

\begin{definition}
We say the [[limit]] ${\lim_\leftarrow}_D F(-,-)$ **[[commutativity of limits with colimits|commutes]]** with the colimit ${\lim_\to}_C F(-,-)$ if the morphism $\lambda$ above is an [[isomorphism]]

$$
  {\lim_\to}_C {\lim_\leftarrow}_D F
   \stackrel{\simeq}{\longrightarrow}
  {\lim_\leftarrow}_D {\lim_\to}_C  F
  \,.
$$
\end{definition}


\begin{proposition}
\label{FilteredColimitsCommuterWithFiniteLimits}
In [[Set]], filtered colimits [[commutativity of limits with colimits|commute]] with [[finite limits]].

In fact, [[filtered categories]] $C$ are precisely those shapes of [[diagram]] categories such that colimits over them commute with all finite limits in Sets.

More generally, for $\kappa$ a [[regular cardinal]], then $\kappa$-filtered colimits commute with $\kappa$-small limits.
\end{proposition}

Proof of the first part is in [MacLane (1971), §IX.2 Thm. 1 (p. 211)](#MacLane71), [Borceux (1994), theorem I2.13.4](#Borceux). For more discussion see also [BJTS 14](#BJTS14),
and see also *[[limits and colimits by example]]*. 

\begin{remark} 
It is not true that filtered colimits and finite limits commute in *any* category $C$ which has them. A simple example is where $C$ is the [[poset]] of [[closed subspaces]] of the [[one-point compactification]] $\mathbb{N} \cup \{\infty\}$ of the [[discrete space]] of [[natural numbers]]. If $A = \{\infty\}$ and $B_i$ ranges over finite subsets of $\mathbb{N}$, then $A \times colim_i B_i = \{\infty\} \cap (\mathbb{N} \cup \{\infty\}) = \{\infty\}$, but $colim_i A \times B_i = colim_i \{\infty\} \cap B_i = colim_i \varnothing = \varnothing$. 
\end{remark}


According to 1.5 and 1.21 in [[LPAC]], a category has $\kappa$-[[directed colimits]] precisely if it has $\kappa$-filtered ones, and a functor preserves $\kappa$-directed colimits iff it preserves $\kappa$-filtered ones. A proof of this result, following Adamek & Rosicky, may be found [[directed colimits imply filtered colimits|here]]. 

The fact that directed colimits suffice to obtain all filtered ones may be regarded as a convenience similar to the fact that all [[colimits]] can be constructed from [[coproducts]] and [[coequalizers]].  Of course, a [[duality|dual]] result holds for [[codirected limits]].

### Flat functors and points of presheaf toposes 

Let $C$ be a small category. A functor $F: C \to Set$ is **[[flat functor|flat]]** if it is a filtered colimit of [[representable functor]]s. 

Equivalently, a [[module]] $F: C \to Set$ is flat if and only if the [[tensor product of functors|tensor product]] 

$$- \otimes_C F: Set^{C^{op}} \to Set$$ 

is [[left exact functor|left exact]]. One may prove as a corollary that if $C$ is [[finitely complete category|finitely complete]], $F$ is flat if and only if it is [[left exact functor|left exact]] (preserves finite limits). Since this tensor product is automatically a left adjoint, we have the following basic result: 

+-- {: .num_prop} 
######Proposition 

For $C$ a [[small category]], the category of [[point of a topos|topos points]] of the [[presheaf topos]] $Set^{C^{op}}$ (i.e., [[geometric morphism]]s $Set \to Set^{C^{op}}$ and natural transformations between them) is equivalent to the category of flat modules on $C$. 

=-- 

### Description in Set, Grp, Top and alike

Elements in filtered colimits in [[Set]] and [[Grp]] are given as classes of equivalences, so called [[germs]]. Filtered limits in [[Set]] and [[Top]] are given as families of compatible elements, so called [[threads]].


### More

(More was/is to be written here, including an application to [[geometric realization]], relation to [[Diaconescu's theorem]], and perhaps more.) 


## Related concepts

* [[filtered category]], [[compact object]]

* [[sifted colimit]], [[sifted (∞,1)-colimit]]

* [[filtered (∞,1)-colimit]], [[filtered homotopy colimit]]

* [[Kolmogorov product]]

Filtered colimits are also important in the theory of [[locally presentable category|locally presentable]] and [[accessible category|accessible]] categories.  See also [[pro-object]] and [[ind-object]].

## References

* {#MacLane71} [[Saunders MacLane]], §IX.2 in: *[[Categories for the Working Mathematician]]*, Graduate texts in mathematics, Springer (1971) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

* {#Borceux} [[Francis Borceux]], Section 2.13 in: _[[Handbook of Categorical Algebra]] vol 1_


Also

* {#BJTS14} [[Marie Bjerrum]], [[Peter Johnstone]], [[Tom Leinster]], [[William F. Sawin]], *Notes on commutation of limits and colimits*, Theory and Applications of Categories **30** (2015), 527-532 &lbrack;[arXiv:1409.7860](http://arxiv.org/abs/1409.7860), [tac:3015](http://www.tac.mta.ca/tac/volumes/30/15/30-15abs.html)&rbrack;


[[!redirects filtered limit]]
[[!redirects filtered limits]]
[[!redirects cofiltered limit]]
[[!redirects cofiltered limits]]
[[!redirects filtered colimit]]
[[!redirects filtered colimits]]
[[!redirects filtered inverse limit]]
[[!redirects filtered inverse limits]]
[[!redirects cofiltered inverse limit]]
[[!redirects cofiltered inverse limits]]
[[!redirects filtered direct limit]]
[[!redirects filtered direct limits]]