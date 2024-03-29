
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

The concept of **dense subtopos** generalizes the concept of a [[dense subspace]] from topology to toposes. A _[[subtopos]]_ is _dense_ if it contains the [[initial object]] $\varnothing$ of the ambient [[topos]].

## Definition

Let $i:\mathcal{E}_j\hookrightarrow \mathcal{E}$ be a [[subtopos]] with corresponding [[Lawvere-Tierney topology]] $j$. $\mathcal{E}_j$ is called _dense_ if the following equivalent conditions hold:

* $j\circ\bot=\bot$ (with $\bot: 1\to\Omega$ the classifying map of $\emptyset\rightarrowtail 1$).

* $\emptyset\rightarrowtail 1$ is $j$-closed.

* $\emptyset$ is a $j$-sheaf.

* the [[direct image]] satisfies $i_\ast (\emptyset)\simeq\emptyset$.

* the [[inverse image]] satisfies: from $i^\ast (Z)\simeq\emptyset$ follows $Z\simeq\emptyset$.

A topology $j$ satisfying these conditions is also called _dense_.

### Remark

$j\circ\bot$ classifies the $j$-closure $\bar{\emptyset}$ of $\emptyset$ whence $j\circ\bot = \bot$ iff $\bar{\emptyset}=\emptyset$ i.e. $\emptyset\rightarrowtail 1$ is $j$-closed. Since $1$ is a $j$-sheaf for any topology $j$ and subobjects of $j$-sheaves in general are $j$-closed precisely when they are $j$-sheaves, this is equivalent to $\emptyset$ being a $j$-sheaf. Another way to say this is that $\emptyset$ is preserved by $i_\ast$.

The equivalence between the last two formulations follows from the adjunction $i^\ast\dashv i_\ast$ and the [[strict initial object|strictness]] of $\emptyset$ in a topos: $id_{i_\ast(\emptyset)}$ corresponds under the adjunction to a map $i^\ast( i_\ast (\emptyset))\to \emptyset$ showing that $i^\ast (i_\ast(\emptyset))\simeq\emptyset$ in general. Conversely, $id_{i^\ast (Z)}$ corresponds to a map $Z\to i_\ast(i^\ast(Z))$ showing that $Z\simeq\emptyset$ provided $i^\ast(Z)\simeq\emptyset$ and $i_\ast(\emptyset)\simeq\emptyset$.

In [[SGA4]] (p.430) another equivalent formulation is on offer, namely it suffices to check the last condition on [[subterminal object|subterminal objects]] $Z$ (because $i_\ast(\emptyset)$ is a subterminal in general since $i_\ast$ as a right adjoint preserves monos hence subterminals). An even more comprehensive list can be found in ([Caramello 2012](#Caramello12), p.9).


The last two conditions make sense not only for embeddings: general [[geometric morphisms]] fulfilling them are called [[dominant geometric morphism|dominant]]. So another way to express that $i:\mathcal{E}_j\hookrightarrow\mathcal{E}$ is a dense subtopos is to say that the inclusion $i$ is **dominant**.

Notice that there is also a certain [[Grothendieck topology]] on small categories $\mathcal{C}$ called the [[dense topology]] whose corresponding [[Lawvere-Tierney topology]] on $Set^{\mathcal{C}^{op}}$ is dense in the above sense, and coincides with the [[double negation|double-negation topology]] $\neg\neg$ on $Set^{\mathcal{C}^{op}}$.

## Properties

### Some basic observations

Of course, the composition $k\circ j$ of dense inclusions $j,k$ is again dense. Conversely, we have

+-- {: .num_prop #dense_factors}
###### Proposition
Given the following commutative diagram
$$
  \array{
    \mathcal{E}_i &\overset{j}{\to}& \mathcal{E}
    \\
     &{i}{\searrow}& \uparrow k
    \\
     & & \mathcal{E}_k 
  }
$$
where $i,j,k$ are subtopos inclusions. When $j$ is dense, then $i$ and $k$ are dense as well.
=--

**Proof**: Suppose $\emptyset =i^\ast (Z)$. Since $k$ is an inclusion we have that the counit $\epsilon:k^\ast k_\ast\to id_{\mathcal{E}_k}$ is a natural isomorphism whence $Z= k^\ast k_\ast (Z)$ and therefore 

$$\emptyset =i^\ast(Z)=i^\ast(k^\ast k_\ast (Z))=i^\ast k^\ast (k_\ast (Z))=j^\ast(k_\ast(Z))\quad .$$ 

From which $k_\ast(Z)=\emptyset$ since $j$ is dense by assumption.

Then $Z=k^\ast k_\ast (Z)=k^\ast (\emptyset)=\emptyset$ since $k^\ast$ preserves colimits, in other words, we have shown that $i$ is dense.

But from $k_\ast (Z)=\emptyset$ and $Z=\emptyset$ follows that $k$ is dense as well. $\qed$

Given two dense topologies $j_1$, $j_2$ on a topos $\mathcal{E}$, their join $j_1\vee j_2$ is again dense.

This follows from the general fact that $Sh_{j_1\vee j_2}(\mathcal{E})$ corresponds to the meet, i.e. the intersection of the corresponding subtoposes $Sh_{j_1}(\mathcal{E})\cap Sh_{j_2}(\mathcal{E})$ in the [[lattice of subtoposes]], and this obviously contains $\emptyset_\mathcal{E}$ for $j_1$, $j_2$ dense.

In other words, the intersection of two dense subtoposes is still dense!

Somewhat surprisingly, this still holds if one takes the intersection of _all_ dense subtoposes, as the next section details.

### Relation to double-negation topology {#double_negation}

For any topos $\mathcal{E}$, its [double negation topology](double+negation#DoubleNegationTopology) gives the _smallest_ dense subtopos. This agrees with the [situation for locales](double+negation#double_negation_locale) but contrasts with the [[dense subspace|situation for topological spaces]] where, in general, smallest dense subspaces do not exist.

+-- {: .num_prop #smallest_dense_subtopos}
###### Proposition
$Sh_{\not\not}(\mathcal{E}) \hookrightarrow \mathcal{E}$ is the smallest dense subtopos.
=--
([Johnstone, below Corollary 4.5.20](#Johnstone02))

In fact, dense topologies are characterized by their relation to $\neg\neg$:

+-- {: .num_prop #negdense}
###### Proposition
Let $\mathcal{E}$ be a topos. A topology $j$ satisfies $j\le\neg\neg$ , i.e. $j$ is dense, iff $(\mathcal{E}_j)_{\not\not}=\mathcal{E}_{\not\not}$.
=--

([Blass-Scedrov 1983](#BlassScedrov83), p.19, [Caramello 2012](#Caramello12), p.9, see also at [double negation](#boolean_subtopos)).

From this and the fact that $\mathcal{E}$ is trivially dense, follows:

+-- {: .num_prop #prop_boolean}
###### Proposition
A topos $\mathcal{E}$ is [[Boolean topos|Boolean]] iff $\mathcal{E}$ has exactly one dense subtopos, namely $\mathcal{E}_{\neg\neg}=\mathcal{E}$.
=--

Notice that, though these results prevent a topos from having more than one _dense_ Boolean subtopos, nothing prevents a topos from having more than one _Boolean_ subtopos e.g. the [[Sierpinski topos]] $Set^{\to}$ has two non trivial ones that complement each other in the [[lattice of subtoposes]]. This example, incidentally, also shows that in the [above proposition](#negdense) just $(\mathcal{E}_j)_{\neg\neg}\cong\mathcal{E}_{\neg\neg}$ wouldn't do.

### The (dense,closed)-factorization

A [[geometric embedding]] of [[elementary toposes]]

$$
  Sh_j(\mathcal{E}) \hookrightarrow \mathcal{E}
$$


factors as

$$
  Sh_j(\mathcal{E}) 
    \hookrightarrow
  Sh_{c(ext(j))}(\mathcal{E})
    \hookrightarrow
  \mathcal{E}
$$

where $ext(j)$ (the "exterior" of $j$) denotes the $j$-closure of $\emptyset \rightarrowtail 1$ and 

$$
  \bar j \coloneqq c(ext(j))
$$ 

the [[closed subtopos|closed topology]] corresponding to the [[subterminal object]] $ext(j)$.

Here the first inclusion exhibits a dense subtopos and the second a [[closed subtopos]].

This is the so called _[[(dense,closed)-factorization]]_ and implies e.g. that _proper_ dense subtoposes aren't closed.

Dense inclusions participate also in the description of [[skeletal geometric morphism|skeletal inclusions]] as the closure of [[open subtopos|open inclusions]] under composition with dense inclusions.

### Some parallels to topology{#parallels_topology}

The above terminology suggests to view a _dense subtopos_ as one with an _empty exterior_.

This analogy to topology is pursued further in ([SGA4](#SGA4), p.462) where a dense subtopos is characterized as a subtopos $Sh_j(\mathcal{E})$ whose 'exterior' $Ext(Sh_j(\mathcal{E}))$ (i.e. the [[open subtopos]] that corresponds to the [[subterminal object]] $ext(j)$) is trivial and whose 'closure' $Cl(Sh_j(\mathcal{E})):=Sh_{c(ext(j))}(\mathcal{E})$ (i.e. the [[closed subtopos]] corresponding to $ext(j)$) coincides with the 'whole space' $\mathcal{E}$.

Let's have a look at some of the details: 

Due to the construction of [[open subtopos|open subtoposes]] we know that the objects of $Ext(Sh_j(\mathcal{E}))$ have the form $X^{ext(j)}$ for some $X\in\mathcal{E}$. Hence the exterior is trivial, i.e. $X^{ext(j)}=1$ for all $X\in\mathcal{E}$, precisely when $\bar\emptyset =ext(j)\simeq \emptyset$ which means that $Sh_j(\mathcal{E})$ is dense. By construction $Cl(Sh_j(\mathcal{E}))$ is the [[complement]] of $Ext(Sh_j(\mathcal{E}))$ in the lattice of subtoposes hence $Cl(Sh_j(\mathcal{E}))=\mathcal{E}$ in case the latter is trivial. This follows also directly from the description of objects in $Cl(Sh_j(\mathcal{E}))$ as those objects $X\in\mathcal{E}$ with $X\times ext(j)\cong ext(j)$.

E.g. let $Sh_k(\mathcal{E})$ be a subtopos that has a trivial intersection with a non-trivial open subtopos $Sh_o(\mathcal{E})$. Then $Sh_k(\mathcal{E})$ is contained in the (closed) complement of $Sh_o(\mathcal{E})$ hence $Cl(Sh_k(\mathcal{E}))\neq \mathcal{E}$ and we see that $Sh_k(\mathcal{E})$ cannot be dense: we have recuperated the familiar fact from point-set topology that a [[dense subspace|dense subset]] intersects all non-trivial open sets non-trivially.

Another easy result in this vein is

+-- {: .num_prop}
###### Proposition
Let $i:Sh_j(\mathcal{E})\hookrightarrow\mathcal{E}$ be a dense subtopos that is [[connected object|connected]] in the sense that $1$ is indecomposable: if $W\coprod Z=1$ then $W=\emptyset$ or $Z=\emptyset$. Then $\mathcal{E}$ is connected as well.
=--

**Proof**: Let $X\coprod Y = 1$ be a decomposition of $1$ in $\mathcal{E}$. Since $i^\ast$ is a left exact left adjoint, it preserves coproducts and the terminal object and $i^\ast(X)\coprod i^\ast (Y)$ is therefore a decomposition of $1$ in $Sh_j(\mathcal{E})$ hence trivial by assumption. Let's say $i^\ast(X)\simeq\emptyset$ but $Sh_j(\mathcal{E})$ is dense and therefore we can conclude $X\simeq\emptyset$ hence $X\coprod Y = 1$ is trivial as well. $\qed$

###Example I: two-valued toposes

Presheaf toposes $Set^{M^{op}}$ of actions of a monoid $M$ are classical examples of toposes whose truth value objects $\Omega$ have exactly two global points $1\to\Omega$ without the toposes being necessarily Boolean. In fact they are Boolean precisely when $M$ is a group.

As the next proposition shows, they are also instances of toposes in which only the degenerate subtopos fails to be dense:

+-- {: .num_prop}
###### Proposition
The non-degenerate subtoposes $Sh_j(\mathcal{E})$ of a [[two-valued topos]] $\mathcal{E}$ are precisely the dense subtoposes of $\mathcal{E}$.
=--

**Proof**: Truth values $1\to\Omega$ correspond precisely to subobjects of $1$. Hence the $j$-closure $ext(j)$ of $\emptyset\rightarrowtail 1$ is either $\emptyset$ or $1$. In the first case, $Sh_j(\mathcal{E})$ is dense, in the second, from $X\times 1=1$ for $X\in Cl(Sh_j(\mathcal{E}))$ follows triviality. $\qed$

Combining this with the [above](#prop_boolean) shows that _two-valued and Boolean toposes are opposite extremes_ when it comes to dense subtoposes and the following observation (cf. [Caramello (2009)](#Caramello09); prop. 10.1) follows immediately:

+-- {: .num_prop}
###### Proposition
A topos $\mathcal{E}$ that is two-valued and Boolean has no non-trivial subtoposes. $\qed$
=--

In other words, two-valued Boolean toposes are atoms in the lattice of subtoposes. Notice that this applies e.g. to well-pointed toposes.

### Example II: persistent localizations

Recall that a [[persistent localization]] is given by a [[Lawvere-Tierney topology]] $j$ with the property that every $j$-separated object is a $j$-sheaf. But separated objects are closed under taking subobjects and therefore in the case of persistent $j$, subobjects of $j$-sheaves are themselves $j$-sheaves.

In particular, this applies to $\emptyset\rightarrowtail 1$, since $1$ is always a sheaf. Whence $\emptyset$ is a $j$-sheaf and we see that **persistent localizations are dense**. This includes e.g. 'quintessential localizations' aka [[quality type|quality types]].

This observation is due to [Johnstone (1996)](#Johnstone96).

By the [above proposition](#prop_boolean) it follows immediately that every persistent localization of a Boolean topos is trivial. 

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

In view of this, the subtopos being dense says that not only $\ast$, but this whole [[adjoint modality]] that it participates in sits inside the subtopos. [[Lawvere]] had proposed to call this situation **resolution** or (a special minimal version of it) _[[Aufhebung]]_ of the [[unity of opposites]] expressed by $\emptyset \dashv \ast$ ("[[becoming]]").

In other words, for an [[level| essential subtopos]] _being dense is equivalent to resolve_ $\emptyset \dashv \ast$ in the Hegelian calculus of [[level of a topos|levels]]!

#### Example: essential subtoposes of the topos of globular sets

[Kennett-Riehl-Roy-Zaks (2011)](#KRRZ11) show that in the [[gros topos]] $Set^{\mathcal{G}^{op}}$ of reflexive [[globular sets]] essential subtoposes correspond to [[n-truncation modality|dimensional truncations]] (plus the level ${Set^{\mathcal{G}^{op}}}$ 'at infinity'). Then [[level]] $n+1$ is the Aufhebung of $n$ starting from $\emptyset\dashv\ast$ at level $0$. In general, the Aufhebung $\bar{l}$ of a level $l$ resolves all the levels that $l$ resolves. Therefore in $Set^{\mathcal{G}^{op}}$ all essential subtoposes (above 0) resolve $\emptyset\dashv\ast$ and hence are _dense_!

## Related entries

* [[dense]]

* [[dense subspace]]

* [[(dense,closed)-factorization]]

* [[dominant geometric morphism]]

* [[skeletal geometric morphism]]

* [[dense topology]]

* [[double negation]]

* [[dense subcategory]]

## References

* {#SGA4}[[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas ([[SGA4]])_, LNM **269** Springer Heidelberg 1972. (pp.429-430, 462)

* {#BlassScedrov83}[[Andreas Blass]], Andrej Scedrov, _Boolean Classifying Topoi_ , JPAA **28** (1983) pp.15-30.

* {#Cara09} [[Olivia Caramello]], _Lattices of theories_ , arXiv:0905.0299 (2009). ([abstract](http://arxiv.org/abs/0905.0299))

* {#Caramello12}[[Olivia Caramello]], _Topologies for intermediate logics_ , arXiv:1205.2547 (2012). ([abstract](http://arxiv.org/abs/1205.2547))

* {#Johnstone96}[[Peter Johnstone]], _Remarks on Quintessential and Persistent Localizations_ , TAC **2** no.8 (1996) pp.90-99. ([pdf](http://www.tac.mta.ca/tac/volumes/1996/n8/n8.pdf))

* {#Johnstone02} [[Peter Johnstone]], _[[Sketches of an Elephant]] I_, Oxford UP 2002. (pp.211,219-220)

* {#KRRZ11} C. Kennett, [[Emily Riehl|E. Riehl]], M. Roy, M. Zaks, _Levels in the toposes of simplicial sets and cubical sets_ , JPAA **215** no.5 (2011) pp.949-961. (preprint as [arXiv:1003.5944](http://arxiv.org/abs/1003.5944))


[[!redirects dense subtoposes]]