

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


\tableofcontents


## Idea
 {#Idea}

The notion of [[group presentations]] may be realized [[homotopy theory|homotopy-theoretically]] by attaching [[2-cells]] to a [[wedge sum]] of [[circles]] along [[loops]] representing the defining [[relations]].

This is a [[homotopy pushout]]-construction that has notably a neat formulation in [[homotopy type theory]]. Its [[1-truncation]] gives a model for the [[classifying space]] $B G$  and more generally of the *[[moduli stack]]* or *[[delooping groupoid]]* $\mathbf{B}G$ of the presented group.

This construction relates the algebraic description of a group by [[generators and relations]] to its description as the [[fundamental group]] of a [[connected homotopy type|connected space]].



## Construction

A [[group presentation]] can be realized geometrically by representing generators as loops and relations as homotopies contracting specified compositions of these loops. The resulting space is constructed by attaching 2-cells to a [[wedge sum]] of circles, or equivalently by forming a [[homotopy pushout]].

Let $X$ be a set of generators and $R$ a set of relators, equipped with a function $r:R\to F(X)$, where $F(X)$ is the [[free group]] on $X$. The presented group is

$$
  G_P 
    \coloneqq 
  F(X)/\langle\!\langle r(R)\rangle\!\rangle,
$$

where $\langle\!\langle r(R)\rangle\!\rangle$ denotes the [[normal closure]] of the relators. The construction below realizes this quotient at the level of fundamental groups.

### The generator space

Consider the pointed space

$$
  W_X \coloneqq \bigvee_{x\in X} S^1,
$$

the [[wedge sum]] of circles indexed by $X$, with all circles identified at a common basepoint. Each generator $x\in X$ determines a distinguished based loop $\gamma_x:S^1\to W_X$.

By the [[Seifert-van Kampen theorem]], the fundamental group of this space is the free group on $X$:

$$
\pi_1(W_X)\cong F(X).
$$

Under this isomorphism, the homotopy class $[\gamma_x]$ corresponds to the free generator $x$. Group multiplication is represented by concatenation of loops, while inversion corresponds to reversing their orientation. For instance, the word $x_1x_2^{-1}x_3$ is represented by the composite loop $\gamma_{x_1}\cdot\gamma_{x_2}^{-1}\cdot\gamma_{x_3}$.

Thus, $W_X$ realizes the generators without imposing any relations.

### Attaching the relations

Each relator $a\in R$ determines an element $r(a)\in F(X)\cong\pi_1(W_X)$, represented by a based loop $\rho_a:S^1\to W_X$.

To impose the relation $r(a)=1$, one attaches a disk $D^2$ along $\rho_a$. The disk provides a null-homotopy of the corresponding loop, making its homotopy class trivial in the resulting space.

Collecting these loops gives an attaching map $\rho:R\times S^1\to W_X$, defined by $\rho(a,z)=\rho_a(z)$. The presentation space is the [[homotopy pushout]]

$$
  C_P 
  \coloneqq
  \operatorname{hocolim}
  \big(
    W_X \xleftarrow{\rho} R\times S^1
      \xrightarrow{\mathrm{pr}_1} 
    R
  \big).
$$

Here $\mathrm{pr}_1:R\times S^1\to R$ sends each circle to its indexing relator. Equivalently, the construction attaches one 2-cell for every relator:

$$
C_P\simeq
W_X\cup_{\coprod_{a\in R}S^1}
\coprod_{a\in R}D^2.
$$

This is the classical presentation [[CW-complex]]. The homotopy pushout retains the homotopy data of the attachments, whereas an ordinary pushout that simply collapses each relator loop may fail to preserve the intended homotopy type.

In [[homotopy type theory]], the same construction can be expressed using a [[pushout type]], whose path constructors encode the homotopies associated with the attachments.

### Example: a cyclic group

Consider the presentation $G = \langle x \mid x^n = 1 \rangle \cong \mathbb{Z}/n\mathbb{Z}$, for $n\geq 1$.

Since there is one generator, $W_X=S^1$. The relator $x^n$ is represented by the degree-$n$ map $\rho_n:S^1\to S^1$, and the presentation space is

$$
C_P=S^1\cup_{\rho_n}D^2.
$$

The attached disk makes the loop traversing the circle $n$ times null-homotopic. By the [[Seifert-van Kampen theorem]],

$$
\pi_1(C_P) \cong \langle x \mid x^n = 1 \rangle \cong \mathbb{Z}/n\mathbb{Z}
$$

This illustrates the general correspondence: generators determine loops, relators determine 2-cell attachments, and the resulting fundamental group is the group specified by the presentation.



## Fundamental group

The fundamental group of the presentation space $C_P$ is precisely the group specified by the original presentation. This follows from the [[Seifert-van Kampen theorem]], which describes how attaching 2-cells affects the fundamental group of a space.

Recall that the generator space $W_X=\bigvee_{x\in X}S^1$ satisfies $\pi_1(W_X)\cong F(X)$. Each relator $a\in R$ determines a loop $\rho_a:S^1\to W_X$, whose homotopy class corresponds to $r(a)\in F(X)$.

Attaching a 2-cell along $\rho_a$ makes this loop null-homotopic. At the level of fundamental groups, this imposes the relation $r(a)=1$. Moreover, every conjugate $wr(a)w^{-1}$ also becomes trivial, since the induced map on fundamental groups is a group homomorphism.

Consequently, the kernel of the homomorphism induced by the inclusion $W_X\to C_P$ is exactly the [[normal closure]] of the relators:

$$
\ker\bigl(\pi_1(W_X)\to\pi_1(C_P)\bigr)
=
\langle\!\langle r(R)\rangle\!\rangle.
$$

By the [[Seifert-van Kampen theorem]], the induced homomorphism is surjective, and therefore

$$
\pi_1(C_P)
\cong
F(X)/\langle\!\langle r(R)\rangle\!\rangle
\cong G_P.
$$

Thus, the homotopy pushout realizes the algebraic quotient defining the presented group. The generators become homotopy classes of loops, while the relations become null-homotopies of the corresponding composite loops.

This construction is valid for arbitrary sets of generators and relators, without requiring the presentation to be finite.

## Classifying space

Although $C_P$ has fundamental group $G_P$, it is not necessarily a [[classifying space]] for $G_P$. A classifying space $BG_P$, regarded as an [[Eilenberg-Mac Lane space]] $K(G_P,1)$, has fundamental group $G_P$ and trivial higher homotopy groups.

The presentation space $C_P$ is a connected [[CW-complex]] of dimension at most two, but it may have nontrivial higher homotopy groups. In particular, the relations imposed on its fundamental group do not necessarily eliminate higher-dimensional homotopy information.

To obtain the classifying space, consider the [[1-truncation]] of $C_P$, denoted by $\|C_P\|_1$. The canonical truncation map $C_P\to\|C_P\|_1$ preserves the fundamental group while eliminating homotopy information above dimension one.

Hence,

$$
\pi_1(\|C_P\|_1)
\cong
\pi_1(C_P)
\cong G_P,
$$

while $\pi_n(\|C_P\|_1)=0$ for every $n\geq 2$.

Since $C_P$ is connected, its 1-truncation is a connected pointed [[1-type]]. By the classification of connected pointed 1-types in [[homotopy type theory]], it is pointed-equivalent to the classifying space of its fundamental group:

$$
\|C_P\|_1 \simeq_* BG_P.
$$

Equivalently, the classifying space of a group presented by generators and relations may be obtained by first forming the corresponding homotopy pushout and then applying 1-truncation.

The distinction between $C_P$ and $\|C_P\|_1$ is essential. The former retains the higher homotopy information of the presentation complex, whereas the latter retains precisely the connected 1-type determined by the presented group.


## Formulation in homotopy type theory

In [[homotopy type theory]], the preceding construction can be expressed internally using [[suspension]]s, [[path type]]s, [[pushout type]]s and homotopy [[truncation]]. The generators and relations are encoded by paths and higher-dimensional identifications, rather than by attaching cells to an externally defined topological space.

Throughout this section, $X$ and $R$ are regarded as sets (0-types), and $P=(X,R,r)$ denotes the group presentation introduced above.

### Suspension as the generator space

Instead of starting with a wedge of circles, consider the [[suspension]] of the coproduct of the unit type and the generator set:

$$
  S_X \coloneqq \operatorname{Susp}(\mathbf{1}+X)
  \mathrlap{\,.}
$$

The suspension has two distinguished points, $\mathsf{north}$ and $\mathsf{south}$, together with a meridian

$$
\mathsf{merid}(a):\mathsf{north}=\mathsf{south}
$$

for each $a:\mathbf{1}+X$.

The unit summand provides a distinguished reference meridian $m_* \coloneqq \mathsf{merid}\big(\mathsf{inl}(*)\big)$. Every generator $x:X$ provides another meridian $m_x \coloneqq \mathsf{merid}(\mathsf{inr}(x))$.

Taking $\mathsf{north}$ as the basepoint, define the generator loop

$$
  \gamma_x \coloneqq m_x\cdot m_*^{-1}
   : \mathsf{north} = \mathsf{north}
  \mathrlap{\,.}
$$

The reference meridian is not an additional group generator. Rather, it allows each generator meridian to be converted into a loop based at $\mathsf{north}$.

For a set $X$, the resulting pointed type is equivalent to the wedge of circles indexed by $X$:

$$
  (S_X,\mathsf{north})
  \simeq_*
  \bigvee_{x\in X}S^1
  \mathrlap{\,.}
$$

Consequently, its fundamental group is the free group on $X$.

### Generator loops and words

The [[loop space]] $\Omega(S_X,\mathsf{north})$ consists of paths from $\mathsf{north}$ to itself. Its operations are path concatenation, path inversion and the constant path.

These operations allow words in the generators to be interpreted as loops. In particular, define a map from signed words to based loops by sending a positive generator $x$ to $\gamma_x$ and a negative generator to $\gamma_x^{-1}$.

For a word $w=x_1^{\varepsilon_1}\cdots x_k^{\varepsilon_k}$, where each $\varepsilon_i\in\{+1,-1\}$, its associated loop is

$$
  \gamma_w \coloneqq
  \gamma_{x_1}^{\varepsilon_1}\cdot
  \ldots\cdot
  \gamma_{x_k}^{\varepsilon_k}
  \mathrlap{\,.}
$$

The empty word is interpreted as the constant path. Concatenation of words corresponds to concatenation of loops, and freely reduced words determine the same element of the fundamental group.

More precisely, passing to homotopy classes of loops gives the canonical identification

$$
  F(X) \cong \pi_1(S_X,\mathsf{north}).
  \mathrlap{\,.}
$$

Thus, the free group is recovered from the fundamental group of the suspension-based generator type.

### Relations as higher paths

Each relator $a:R$ specifies an element $r(a):F(X)$, and hence a homotopy class of based loops in $S_X$. Choose a representative loop $\gamma_{r(a)}:\mathsf{north}=\mathsf{north}$.

The relation $r(a)=1$ is imposed by requiring this loop to be homotopic to the constant loop. In type-theoretic notation, the corresponding witness has type

$$
\gamma_{r(a)}=\mathsf{refl}_{\mathsf{north}}.
$$

Since $\gamma_{r(a)}$ is itself a path, such a witness is a path between paths, or a 2-dimensional path.

The construction does not assume that these witnesses already exist in $S_X$. Instead, they are introduced by the higher inductive construction that attaches the relations.

For each $a:R$, the chosen loop determines a pointed map $\rho_a:S^1\to S_X$. Together, these define an attaching map $\rho:R\times S^1\to S_X$.

### The pushout type and 1-truncation

The presentation type is defined by the [[pushout type]] of the span

$$
S_X
\xleftarrow{\rho}
R\times S^1
\xrightarrow{\mathrm{pr}_1}
R.
$$

Explicitly,

$$
  C_P^{\mathrm{HoTT}} \coloneqq
  \operatorname{Pushout}
  \big(
    S_X 
      \xleftarrow{\rho} 
    R\times S^1
      \xrightarrow{\mathrm{pr}_1} 
    R
  \big)
  \mathrlap{\,.}
$$

As a [[higher inductive type]], the pushout has point constructors for the two sides of the span and path constructors identifying their images for each element of $R\times S^1$.

These identifications provide null-homotopies of the relator loops in the resulting type. The pushout therefore implements the relations homotopically, without collapsing the generator space by strict equality.

The resulting type is connected, and its fundamental group is the group specified by the presentation:

$$
 \pi_1(C_P^{\mathrm{HoTT}}) \cong G_P
 \mathrlap{\,.}
$$

However, the pushout may retain nontrivial higher homotopy information. Applying [[1-truncation]] produces a connected 1-type whose fundamental group is $G_P$.

Hence, there is a pointed equivalence

$$
  \left\|C_P^{\mathrm{HoTT}}\right\|_1
    \simeq_* 
  BG_P.
$$

This expresses the [[classifying space]] of a presented group entirely in terms of higher inductive types, path operations and truncation. It is the internal homotopy-type-theoretic counterpart of the classical presentation complex.


## Motivation from topological quantum gates

One motivation for studying such constructions in homotopy type theory arises from [[topological quantum computation]].

Groups associated with topological configurations, including [[braid group]]s, admit descriptions by generators and relations. Their classifying spaces provide homotopy-theoretic models for the corresponding group structures.

In the work of Myers, Sati, and Schreiber on topological quantum gates, homotopy-theoretic methods are used to describe topological structures relevant to quantum gates.

The presentation pushout supplies a general construction of the classifying space of a presented group. The specification of quantum gates additionally requires suitable geometric or representation-theoretic data.




## Formalization in Cubical Agda

The construction described above has been partially formalized in [[Cubical Agda]], using higher inductive types for suspensions, circles, pushouts, and truncations.

The formal development constructs a suspension-based generator space, interprets relations as loops, and forms the corresponding homotopy pushout and its 1-truncation. It also defines the algebraic group associated with the presentation and a canonical homomorphism

$$
c_P : G_P \longrightarrow \pi_1(\|C_P\|_1).
$$

The principal formally verified result is the surjectivity of this homomorphism. Injectivity, the resulting group isomorphism, and the classifying-space equivalence remain open in the formal development.

All modules in the development have been type-checked in Cubical Agda. The accompanying Shadow Paper provides a mathematical exposition with explicit references to the corresponding formal definitions and proofs.

The Shadow Paper, Cubical Agda source code, and complete project repository are available in [[nLab materials#GroupPresentationPushout]].

## Related concepts

* [[group presentation]]

* [[free group]]

* [[homotopy pushout]]

* [[pushout type]]

* [[higher inductive type]]

* [[classifying space]]

* [[fundamental group]]

* [[Seifert-van Kampen theorem]]

* [[topological quantum computation]]


## References
 {#References}

Classical discussion in terms of [[fundamental groups]] of [[CW-complexes]]:

* [[Joseph J. Rotman]]; Thm. 7.34 in: *An Introduction to the Theory of Groups*, Springer (1995) &lbrack;[doi:10.1007/978-1-4612-4176-8](https://doi.org/10.1007/978-1-4612-4176-8), [pdf](https://eclass.uoa.gr/modules/document/file.php/MATH676/Rotman%20An%20introduction%20to%20the%20theory%20of%20groups.pdf)&rbrack;

* {#Hatcher02} [[Allen Hatcher]]; §1.2 of: *Algebraic Topology*, Cambridge University Press (2002) &lbrack;[ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)&rbrack;

* Behrooz Mashayekhy, Hanieh Mirebrahimi: *Some Properties of Finitely Presented Groups with Topological Viewpoints*, International Journal of Mathematics, Game Theory and Algebra **18** 6 (2010) 511--515 &lbrack;[arXiv:1012.1744](https://arxiv.org/abs/1012.1744)&rbrack;

Discussion in [[homotopy type theory]]:

* [[Univalent Foundations Project]]; Ex. 8.7.17 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]*, Institute for Advanced Study (2013)

* [[David Jaz Myers]], [[Hisham Sati]] [[Urs Schreiber]]; p. 64 of: *Topological Quantum Gates in Homotopy Type Theory*, Comm. Math. Phys. **405** 172 (2024) &lbrack;[doi:10.1007/s00220-024-05020-8](https://doi.org/10.1007/s00220-024-05020-8), [arXiv:2303.02382](https://arxiv.org/abs/2303.02382)&rbrack;


See also:

* {#Brown06} [[Ronald Brown]]: *Topology and Groupoids*, Booksurge (2006) &lbrack;[webpage](https://groupoids.org.uk/topgpds.html), [pdf](https://groupoids.org.uk/pdffiles/topgrpds-e.pdf), [pdf](https://www.sas.rochester.edu/mth/sites/doug-ravenel/otherpapers/rbrown-topgrpds-e.pdf)&rbrack;



category: group theory

[[!redirects group presentations as homotopy pushouts]]
