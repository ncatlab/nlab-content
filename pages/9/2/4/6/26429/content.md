[[!redirects strict free cocompletion]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Yoneda lemma
+--{: .hide}
[[!include Yoneda lemma - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[small presheaf]]-construction exhibits the [[free cocompletion]] of a [[locally small category]] (only) up to [[equivalence of categories]]. In other words, it exhibits a [[universal property]] that is [[bicategorical]] in nature. However, it is also possible to give a description of the free *strict* cocompletion, i.e. one satisfying a [[strict 2-category|strict 2-categorical]] universal property, in the sense of $Cat$-[[enriched category theory]], which characterises the free cocompletion up to an [[isomorphism of categories]].

Explicitly, the small presheaf construction exhibits a left [[pseudoadjoint]] to the forgetful 2-functor from the 2-category of [[locally small]] [[cocomplete categories]], whereas a strict free cocompletion exhibits a left [[2-adjoint|strict 2-adjoint]] (or left $Cat$-enriched adjoint).

Abstractly, this follows by the results of [Kelly and Lack (2000)](#KellyLack2000). However, there is also an explicit description, due to [Ehresmann (1981)](#Ehresmann1981), and expanded upon by [Beurier, Pastor & Guitart (2021)](#BPG2021). The idea is to give a much more "naïve" description of the free cocompletion of a category $\mathscr{C}$ whose objects are not presheaves, but simply [[diagrams]] into $\mathscr{C}$. While the objects are, in some sense, simpler than presheaves, the morphisms are considerably more complicated: their dual is called called **atlases** by [Ehresmann (1981)](#Ehresmann1981), and they are called **clusters** by [Ehresmann and Vanbremeersch (1987)](#EV1987). The free strict cocompletion is consequently called the **category of clusters** $Clu(\mathscr{C})$ by [Beurier, Pastor, and Guitart (2021)](#BPG2021).

The morphisms can be seen to satisfy the **limit--colimit formula** ([Beurier–Pastor–Guitart](#BPG2021), Proposition 3.11): given $P \colon \mathscr{P} \to \mathscr{C}$ and $Q \colon \mathscr{Q} \to \mathscr{C}$, we have $Clu(\mathscr{C})(P, Q) \,\cong\, lim_{p \in \mathscr{P}} colim_{q \in \mathscr{Q}} \mathscr{C}\big(P(p), Q(q)\big)$.

The category of clusters embeds [[fully faithfully]] into the [[small presheaf category]]. Its full image is called $LClu(\mathscr{C})$ by [Beurier, Pastor & Guitart (2021)](#BPG2021).

That the category of clusters forms the free strict cocompletion was stated in [Ehresmann (1981)](#Ehresmann1981) and [Ehresmann and Vanbremeersch (1987)](#EV1987), but without detailed proofs. A detailed treatment is given by [Beurier, Pastor &Guitart (2021)](#BPG2021).

[Ehresmann (1981)](#Ehresmann1981) also considers the restriction to the free strict cocompletion under a specified class $\mathscr{J}$ of [[diagram]] shapes: this is given by restricting the objects of the category of clusters.

## Universal property

See [Beurier–Pastor–Guitart](#BPG2021), Theorem 4.4.

Consider a [[locally small category]] $\mathscr{C}$,
its category of clusters $\mathscr{F}=Clu(\mathscr{C})$ (as desribed above),
and the canonical inclusion $I\colon\mathscr{C}\to Clu(\mathscr{C})$ that sends an object of $\mathscr{C}$ to a diagram indexed by the terminal category.
The triple $(\mathscr{C},\mathscr{F},I)$ has the following additional canonical structure: for every [[small diagram]] $P\colon\mathscr{P}\to\mathscr{C}$ we have a canonical colimit cocone $\lambda^P\colon I P\Rightarrow \lambda(I P)$ in $\mathscr{F}$.
Here $\lambda(I P)$ is an object of $\mathscr{F}$ given by the diagram $P$ itself, interpreted as an object of $\mathscr{F}$.

The free strict cocompletion $Clu(\mathscr{C})$ of a [[locally small category]] $\mathscr{C}$ satisfies the following universal property: given another such triple $(\mathscr{F}',I',\lambda')$, where $I'\colon \mathscr{C}\to\mathscr{F}'$ is a functor landing in a locally small cocomplete category $\mathscr{F}'$ and $\lambda'$ is a choice of a colimit cocone for every diagram of the form $I' P'$ ($P'\colon \mathscr{P}'\to \mathscr{C}$), there is a unique functor $J\colon\mathscr{F}\to\mathscr{F}'$ such that $J I = I'$ and $J$ sends cocones in $\lambda$ to the corresponding cocones in $\lambda'$.

In particular, $\mathscr{F}$ is unique up to an isomorphism.

## Properties

The assignment $\mathscr{C}\mapsto Clu(\mathscr{C})$ yields a __strict__ 2-functor from locally small categories to locally small categories that implements the free cocompletion construction.

This stands in contrast to the usual construction of [[small presheaves]], which only yields a pseudofunctor.

By restricting the types of diagrams in the construction of $Clu(\mathscr{C})$, we get strict cocompletion functors for certain types of colimits, e.g., [[ind-completions]].

## References

* {#Ehresmann1981} [[Andrée Ehresmann]], _Pro-objects and atlases_, Comments 199.1...3, p. 368. in [[Charles Ehresmann]], _Œuvres complètes et commentées. Vol. IV-1. Esquisses et complétions,
Amiens 1981, supplément no. 1 au volume XXII (1981) des [[Cahiers de topologie et géométrie différentielle]] ([pdf](https://mes-ehres.fr/ChEh/oeuvres/Ehresmann_C.-Oeuvres_IV_1.pdf#page=390))

* {#EV1987} [[Andrée Ehresmann]] and J-P. Vanbremeersch, _Hierarchical Evolutive Systems: A mathematical model for complex systems_, Bulletin of Mathematical Biology 49.1 (1987): 13-50.

* {#KellyLack2000} [[G. M. Kelly]], [[Stephen Lack]], _On the monadicity of categories with chosen colimits_, Theory and Applications of Categories **7** 7 (2000) 148-170 &lbrack;[TAC](http://www.tac.mta.ca/tac/volumes/7/n7/7-07abs.html)&rbrack;

* {#BPG2021} Erwan Beurier, Dominique Pastor, and René Guitart. _Presentations of clusters and strict free-cocompletions_. [[Theory and Applications of Categories]] 36.17 (2021): 492-513. ([link](http://www.tac.mta.ca/tac/volumes/36/17/36-17abs.html))

[[!redirects free strict cocompletions]]
[[!redirects strict free cocompletions]]
[[!redirects category of clusters]]