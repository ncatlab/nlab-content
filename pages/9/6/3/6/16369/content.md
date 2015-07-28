
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The concept of **dense subtopos** generalizes to toposes the concept of a [[dense subspace]] in topology. A _[[subtopos]]_ is _dense_ if it contains the [[initial object]] $\emptyset$ of the ambient [[topos]].

## Definition

Let $i:\mathcal{E}_j\hookrightarrow \mathcal{E}$ be a [[subtopos]] with corresponding [[Lawvere-Tierney topology]] $j$. $\mathcal{E}_j$ is called _dense_ if the following equivalent conditions hold:

* $j\circ\bot=\bot$ (with $\bot: 1\to\Omega$ the classifying map of $\emptyset\rightarrowtail 1$).

* $\emptyset\rightarrowtail 1$ is $j$-closed.

* $\emptyset$ is a $j$-sheaf.

* the corresponding [[localization]] $L$ satisfies $L(\emptyset) \simeq \emptyset$.

* (the [[direct image]] satisfies $i_\ast (\emptyset)\simeq\emptyset$.)

* the [[inverse image]] satisfies: from $i^\ast (Z)\simeq\emptyset$ follows $Z\simeq\emptyset$.

### Remark

$j\circ\bot$ classifies the $j$-closure $\bar{\emptyset}$ of $\emptyset$ whence $j\circ\bot = \bot$ iff $\bar{\emptyset}=\emptyset$ i.e. $\emptyset\rightarrowtail 1$ is $j$-closed. Since $1$ is a $j$-sheaf for any topology $j$ and subobjects of $j$-sheaves in general are $j$-closed precisely when they are $j$-sheaves, this is equivalent to $\emptyset$ being a $j$-sheaf. Another way to say this is that $\emptyset$ is preserved by $i_\ast$ (aka $L$). The equivalence between the last two formulations follows from the adjunction $i^\ast\dashv i_\ast$ and the [[strict initial object|strictness]] of $\emptyset$ in a topos. In [[SGA4]] (p.430) still another equivalent formulation is on offer, namely it suffices to check the last condition on [[subterminal object|subterminal objects]] $Z$.

Note that the last two conditions make sense not only for embeddings $i$: general [[geometric morphisms]] fullfilling them are called [[dominant geometric morphism|dominant]]. So another way to express that $i:\mathcal{E}_j\hookrightarrow\mathcal{E}$ is a dense subtopos is to say that the inclusion $i$ is **dominant**.

## Properties

### Relation to double-negation topology

For any topos $\mathcal{E}$, its [double negation topology](double+negation#DoubleNegationTopology) gives the _smallest_ dense subtopos. This agrees with the [situation for locales](double+negation#double_negation_locale) but contrasts with the [[dense subspace|situation for topological spaces]] where, in general, smallest dense subspaces do not exist.

+-- {: .num_prop #smallest_dense_subtopos}
###### Proposition
$Sh_{\not\not}(\mathcal{E}) \hookrightarrow \mathcal{E}$ is the smallest dense subtopos.
=--

([Johnstone, below Corollary 4.5.20](#Johnstone02))

### (Dense,Closed)-Factorization

A [[geometric embedding]] of [[elementary toposes]]

$$
  Sh_j(\mathcal{E}) \hookrightarrow \mathcal{E}
$$


factors as

$$
  Sh_j(\mathcal{E}) 
    \hookrightarrow
  Sh_{c(ext(j))} 
    \hookrightarrow
  \mathcal{E}
$$

where $ext(j)$ (the "exterior" of $j$) denotes the $j$-closure of $\emptyset \hookrightarrow \ast$ and 

$$
  \bar j \coloneqq c(ext(j))
$$ 

the [[closed subtopos|closed topology]] corresponding to the [[subterminal object]] $ext(j)$.

Here the first inclusion exhibits a dense subtopos and the second a [[closed subtopos]].

This is the _[[(dense,closed)-factorization]]_.

The above terminology suggests to view a _dense subtopos_ as one with an _empty exterior_.

### Relation to Aufhebung

Notice that, since the [[localization]] $L$ corresponding to a subtopos is a [[left exact functor]], all subtoposes necessarily contain the [[terminal object]] $\ast$ of the ambient topos. Moreover, the [[idempotent comonad]] and [[idempotent monad]] constant on the [[initial object]] and [[terminal object]], respectively, are [[adjoint functor|adjoint]] to each other (forming an [[adjoint modality]]). Denoting by "$\vee$" the inclusion of [[modal objects]], then the general situation for any subtopos localized on by $L$ is depicted by

$$
  \array{
     && L
     \\
     && \vee
     \\
     \emptyset &\dashv& \ast
  }
  \,.
$$ 

In view of this, the subtopos being dense says that not only $\ast$, but this whole [[adjoint modality]] that it partipates in sits inside the subtopos. [[Lawvere]] had proposed to call this situation **resolution** or (a special minimal version of it) _[[Aufhebung]]_ of the [[unity of opposites]] expressed by $\emptyset \dashv \ast$ ("[[becoming]]").

In other words, for an [[level| essential subtopos]] _being dense is equivalent to resolve_ $\emptyset \dashv \ast$ in the Hegelian calculus of [[level|levels]]!

#### Example

[Kennett-Riehl-Roy-Zaks (2011)](#KRRZ11) show that in the [[gros topos]] $Set^{\mathcal{G}^{op}}$ of reflexive [[globular sets]] all subtoposes are essential and correspond to [[n-truncation modality|dimensional truncations]]. Then [[level]] $n+1$ is the Aufhebung of $n$ starting from $\emptyset\dashv\ast$ at level $0$. In general, the Aufhebung $\bar{l}$ of a level $l$ resolves all the levels that $l$ resolves. Therefore in $Set^{\mathcal{G}^{op}}$ _all_ subtoposes (above 0) resolve $\emptyset\dashv\ast$ and hence are _dense_!

Compare this with the case of a **Boolean topos** which has only itself as a (trivial) dense subtopos[^proof]! 

[^proof]: This follows easily from the above [proposition](#smallest_dense_subtopos): cf. at [[Boolean topos]].

## Related pages

* [[dense subspace]]
* [[(dense,closed)-factorization]]
* [[dominant geometric morphism]]
* [[double negation]]

## References

* {#SGA4}[[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas ([[SGA4]])_, LNM **269** Springer Heidelberg 1972. (pp.429-430, 462)

* {#Johnstone02} [[Peter Johnstone]], _[[Sketches of an Elephant]] I_, Oxford UP 2002. (pp.211,219-220)

* {#KRRZ11} C. Kennett, [[Emily Riehl|E. Riehl]], M. Roy, M. Zaks, _Levels in the toposes of simplicial sets and cubical sets_ , JPAA **215** no.5 (2011) pp.949-961. ([preprint](http://arxiv.org/abs/1003.5944))


[[!redirects dense subtoposes]]