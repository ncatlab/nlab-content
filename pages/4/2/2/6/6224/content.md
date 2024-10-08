
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


# Nilpotent groups
* table of contents
{: toc}

## Idea

A [[group]] is __nilpotent__ if it can be built up by [[central extensions]] from [[abelian groups]].  A __central series__ for a group is a witness to its nilpotency.

More generally, we may speak about $\mathcal{A}$-nilpotent $\pi$-groups, for any class $\mathcal{A}$ of abelian groups and any group $\pi$ acting on our groups.  A group $G$ is equivalently an [[Ab]]-nilpotent $G$-group for its [[adjoint action]].


## Definition

### Nilpotent groups and central series

+-- {: .num_defn}
###### Definition

The class of **nilpotent groups** is defined [[inductive definition|inductively]] by the following clauses:

1. The [[trivial group]] $1$ is nilpotent.

2. If $1\to G' \to G \to G''\to 1$ is a [[central extension]] (so that in particular, $G'$ is [[abelian group|abelian]]) and $G''$ is nilpotent, then $G$ is nilpotent.
=--

Phrased in this way, nilpotency is an inductive [[predicate]] on the class of groups.  If we regard the same clauses as defining an inductive [[family]] indexed over the class of groups, then we obtain the definition of a central series.

+-- {: .num_defn}
###### Definition

The set of **central series** for a group $G$ is defined [[inductive definition|inductively]] by the following clauses:

1. The trivial group $1$ has a specified central series, called the "trivial" one.

2. From any central extension $1\to G' \to G \to G''\to 1$ and any central series of $G''$, we obtain a central series of $G$, called an "extension" of the given one.
=--

Thus, central series are "witnesses" to nilpotency: a group is nilpotent if and only if it has some central series.

If we "expand out" the inductive definition of central series, and use the [[isomorphism theorems]], we see that it consists of a sequence of central extensions
$$ 1 \to G_1 \to G \to G/G_1 \to 1 $$
$$ 1 \to G_2/G_1 \to G/G_1 \to G/G_2 \to 1$$
$$ 1 \to G_3/G_2 \to G/G_2 \to G/G_3 \to 1$$
$$ \dots $$
$$ 1 \to G/G_{n-1} \to G/G_{n-1} \to 1 \to 1$$
and therefore a sequence of [[normal subgroups]]
$$ 1 = G_0 \trianglelefteq G_1 \trianglelefteq G_2 \trianglelefteq \dots \trianglelefteq G_{n-1} \trianglelefteq G_n = G $$
such that each $G_i/G_{i-1}$ is central in $G/G_{i-1}$.
This is the "usual" definition of central series.


### Nilpotency class

Every central series has a *length*, defined recursively by saying that the length of the trivial central series is $0$ and the length of an extension is one more than the length of the original.  The **nilpotency class** of a nilpotent group is the minimum length of all of its central series.

Proofs about nilpotent groups are often most naturally phrased using induction over the inductive definition of nilpotency.  However, probably due to widespread ignorance about inductive definitions, it is common to find them phrased instead using ordinary natural-number induction over the nilpotency class.


### Co-nilpotent groups and central streams

If we interpret the same defining clauses of nilpotent groups and central series [[coinductive definition|coinductively]] rather than inductively, we obtain notions that might be called *co-nilpotent groups* and *central streams* ("stream" being the standard name for the coinductive counterpart of a list).  Explicitly, a central stream is a descending countable sequence of normal subgroups, such that each successive quotient is central in the corresponding quotient of the whole group, that may or may not ever terminate with the trivial group.

In fact, *every* group admits some central stream and hence is co-nilpotent.  Two canonical central streams associated to any group are its [[lower central series]] and its [[upper central series]] (for now see [Wikipedia](http://en.wikipedia.org/wiki/Central_series#Upper_central_series)). Despite the names, these two central streams are actually central series (i.e. they terminate at the trivial group) if and only if the group is nilpotent.


### $\mathcal{A}$-nilpotent $\pi$-groups

The following generalization of nilpotent groups is sometimes useful.  Let $\mathcal{A}$ be any class of [[abelian groups]] containing $0$, and let $\pi$ be any group.  By a *$\pi$-group* we mean a group with an action of $\pi$ (through group automorphisms, of course).

+-- {: .num_defn}
###### Definition

The class of **$\mathcal{A}$-nilpotent** $\pi$-groups is defined [[inductive definition|inductively]] by the following clauses:

1. The trivial group $1$ is $\mathcal{A}$-nilpotent.

2. If $1\to G' \to G \to G''\to 1$ is a [[central extension]] of $\pi$-groups (i.e. a central extension whose maps are $\pi$-equivariant), and $G''$ is $\mathcal{A}$-nilpotent while $G'\in \mathcal{A}$ and $\pi$ acts trivially on $G'$, then $G$ is $\mathcal{A}$-nilpotent.
=--

A group $G$ is nilpotent in the original sense if and only if it is an $Ab$-nilpotent $G$-group with its [[adjoint action]].  If $\pi$ is nontrivial and/or $\mathcal{A}$ is strictly smaller than $Ab$, then the notion of $\mathcal{A}$-nilpotency can be nontrivial even for abelian groups (whereas every abelian group is obviously nilpotent in the ordinary sense).


## Properties

Every nilpotent group is an example of a [[solvable group]] (indeed, the groups in the [[lower central series]] of any group can be term-wise included into its [[derived series]]).

The [[Sylow p-subgroups]] of any nilpotent group are [[normal subgroup|normal]]. The direct product of these subgroups in such a group is its [[torsion subgroup]].

## Examples

Generally:

* Every [[abelian group]] is nilpotent.

* The [[direct product group]] of two nilpotent groups is again nilpotent.

* The [[central extension]] of any [[abelian group]] is nilpotent, a famous class of examples of such are the [[Heisenberg groups]].

Specifically:


* The multiplicative group of upper triangular unipotent $n \times n$ matrices with [[coefficients]] in any [[field]] is nilpotent.


## Related pages

* [[solvable group]]

* [[nilpotent module]]

* [[nilpotent element]]

* [[nilpotent Lie algebra]]

* [[nilpotent topological space]]

* [[localization of a space]]



## References

* [[Peter Hilton]], _Nilpotency in group theory and topology_, Publicacions de la Secció de Matemàtiques Vol. 26, No. 3 (1982), pp. 47-78 ([jstor:43741908](https://www.jstor.org/stable/43741908))

* [[Peter May]], [[Kate Ponto]], §3.1 in: _[[More concise algebraic topology]]_,   University of Chicago Press (2012) &lbrack;[ISBN:9780226511795](https://press.uchicago.edu/ucp/books/book/chicago/M/bo12322308.html), [pdf](https://www.math.uchicago.edu/~may/TEAK/KateBookFinal.pdf)&rbrack;


See also:

* eom [nilpotent group](http://eom.springer.de/n/n066720.htm)

* Wikipedia [nilpotent group](http://en.wikipedia.org/wiki/Nilpotent_group)

On nilpotent [[Lie groups]] (cf. at *[[nilpotent Lie algebra]]*):

* Arthur A. Sagle, Ralph E. Walde: *Nilpotent Lie Groups and Algebras*, Chapter 11 in: *Introduction to Lie Groups and Lie Algebras*, Pure and Applied Mathematics **51**, Elsevier (1973) 215-227 \[<a href="https://doi.org/10.1016/S0079-8169(08)61671-2">doi:10.1016/S0079-8169(08)61671-2</a>\]

* Laurence Corwin, Frederick P. Greenleaf: *Representations of Nilpotent Lie Groups and their Applications -- Volume 1  Part 1. Basic Theory and Examples*, Cambridge University Press (2004) &lbrack;[ISBN:9780521604956](https://www.cambridge.org/us/universitypress/subjects/mathematics/abstract-analysis/representations-nilpotent-lie-groups-and-their-applications-volume-1-part-1)&rbrack;

* Veronique Fischer, Michael Ruzhansky: *Quantization on Nilpotent Lie Groups*, Birkh&auml;user (2016) &lbrack;[doi:10.1007/978-3-319-29558-9](https://doi.org/10.1007/978-3-319-29558-9)&rbrack;

* [[Manuel Amann]], *On quasi-isometric nilpotent Lie groups* &lbrack;[arXiv:1710.04542](https://arxiv.org/abs/1710.04542)&rbrack;


[[!redirects nilpotent group]]
[[!redirects nilpotent groups]]

[[!redirects central series]]
