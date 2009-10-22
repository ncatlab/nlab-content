[[!redirects semiotic congruence]]
[[!redirects semiotic congruences]]
[[!redirects semiotic equation]]
[[!redirects semiotic equations]]
[[!redirects semiotic equivalence]]
[[!redirects semiotic equivalence class]]
[[!redirects semiotic equivalence classes]]
[[!redirects semiotic equivalence relations]]
[[!redirects semiotic partition]]
[[!redirects semiotic partitions]]
[[!redirects SEC]][[!redirects SEP]]
[[!redirects SEQ]][[!redirects SER]]

* tic
{:toc}

A __semiotic equivalence relation__ (SER) is a special type of [[equivalence relation]] that arises in the analysis of [[sign relations]].  As a general rule, any equivalence relation is closely associated with a family of [[equivalence classes]] that [[partition]] the underlying set of elements, frequently called the _domain_ or _space_ of the relation.  In the case of a SER, the equivalence classes are called __semiotic equivalence classes__ (SECs) and the partition is called a __semiotic partition__ (SEP).

# Examples #

Tables&#160;1 and 2 list the triples of two finite relations, $L_\mathrm{A}$ and $L_\mathrm{B}$, that are introduced in the pages on [[sign relations]] and [[triadic relations]] as examples of those two concepts.

$$\array{
\array{\arrayopts{\frame{solid}\rowlines{solid solid none}}
\cellopts{\colspan{3}} \text{Table 1.  Sign Relation} \: L_\mathrm{A} \\
Object & Sign & Interpretant \\
\mathrm{A} & \backprime\backprime\mathrm{A}\prime\prime & \backprime\backprime\mathrm{A}\prime\prime \\
\mathrm{A} & \backprime\backprime\mathrm{A}\prime\prime & \backprime\backprime\mathrm{i}\prime\prime \\
\mathrm{A} & \backprime\backprime\mathrm{i}\prime\prime & \backprime\backprime\mathrm{A}\prime\prime \\
\mathrm{A} & \backprime\backprime\mathrm{i}\prime\prime & \backprime\backprime\mathrm{i}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{B}\prime\prime & \backprime\backprime\mathrm{B}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{B}\prime\prime & \backprime\backprime\mathrm{u}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{u}\prime\prime & \backprime\backprime\mathrm{B}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{u}\prime\prime & \backprime\backprime\mathrm{u}\prime\prime }
&
\array{\arrayopts{\frame{solid}\rowlines{solid solid none}}
\cellopts{\colspan{3}} \text{Table 2.  Sign Relation} \: L_\mathrm{B} \\
Object & Sign & Interpretant \\
\mathrm{A} & \backprime\backprime\mathrm{A}\prime\prime & \backprime\backprime\mathrm{A}\prime\prime \\
\mathrm{A} & \backprime\backprime\mathrm{A}\prime\prime & \backprime\backprime\mathrm{u}\prime\prime \\
\mathrm{A} & \backprime\backprime\mathrm{u}\prime\prime & \backprime\backprime\mathrm{A}\prime\prime \\
\mathrm{A} & \backprime\backprime\mathrm{u}\prime\prime & \backprime\backprime\mathrm{u}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{B}\prime\prime & \backprime\backprime\mathrm{B}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{B}\prime\prime & \backprime\backprime\mathrm{i}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{i}\prime\prime & \backprime\backprime\mathrm{B}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{i}\prime\prime & \backprime\backprime\mathrm{i}\prime\prime }
}$$

The sign relations $L_\mathrm{A}$ and $L_\mathrm{B}$ have many interesting properties that are not possessed by sign relations in general.  Some of these properties have to do with the relation between signs and their interpretant signs, as reflected in the projections of the sign relations $L_\mathrm{A}$ and $L_\mathrm{B}$ on the $S I$-plane, notated as $\mathop{proj}_{S I} L_\mathrm{A}$ and $\mathop{proj}_{S I} L_\mathrm{B}$, respectively.  The 2-adic relations on $S \:\times\: I$ that are induced by these projections are also referred to as the _connotative components_ of the corresponding sign relations, notated as $\mathop{Con} (L_\mathrm{A})$ and $\mathop{Con} (L_\mathrm{B})$, respectively.  The discussion of these properties is made a little easier by using the following abbreviations.

$$\array{
\mathop{Con} (L_\mathrm{A}) & \text{:=} & \mathop{proj}_{SI} L_\mathrm{A}
\\
\mathop{Con} (L_\mathrm{B}) & \text{:=} & \mathop{proj}_{SI} L_\mathrm{B}
}$$

Tables&#160;3 and 4 exhibit the connotative components of $L_\mathrm{A}$ and $L_\mathrm{B}$, respectively.

$$\array{
\array{\arrayopts{\frame{solid}\rowlines{solid solid none}}
\cellopts{\colspan{2}} \text{Table 3.} \: \mathop{Con} L_\mathrm{A} \\
S & I \\
\backprime\backprime\mathrm{A}\prime\prime & \backprime\backprime\mathrm{A}\prime\prime \\
\backprime\backprime\mathrm{A}\prime\prime & \backprime\backprime\mathrm{i}\prime\prime \\
\backprime\backprime\mathrm{i}\prime\prime & \backprime\backprime\mathrm{A}\prime\prime \\
\backprime\backprime\mathrm{i}\prime\prime & \backprime\backprime\mathrm{i}\prime\prime \\
\backprime\backprime\mathrm{B}\prime\prime & \backprime\backprime\mathrm{B}\prime\prime \\
\backprime\backprime\mathrm{B}\prime\prime & \backprime\backprime\mathrm{u}\prime\prime \\
\backprime\backprime\mathrm{u}\prime\prime & \backprime\backprime\mathrm{B}\prime\prime \\
\backprime\backprime\mathrm{u}\prime\prime & \backprime\backprime\mathrm{u}\prime\prime }
&
\array{\arrayopts{\frame{solid}\rowlines{solid solid none}}
\cellopts{\colspan{2}} \text{Table 4.} \: \mathop{Con} L_\mathrm{B} \\
S & I \\
\backprime\backprime\mathrm{A}\prime\prime & \backprime\backprime\mathrm{A}\prime\prime \\
\backprime\backprime\mathrm{A}\prime\prime & \backprime\backprime\mathrm{u}\prime\prime \\
\backprime\backprime\mathrm{u}\prime\prime & \backprime\backprime\mathrm{A}\prime\prime \\
\backprime\backprime\mathrm{u}\prime\prime & \backprime\backprime\mathrm{u}\prime\prime \\
\backprime\backprime\mathrm{B}\prime\prime & \backprime\backprime\mathrm{B}\prime\prime \\
\backprime\backprime\mathrm{B}\prime\prime & \backprime\backprime\mathrm{i}\prime\prime \\
\backprime\backprime\mathrm{i}\prime\prime & \backprime\backprime\mathrm{B}\prime\prime \\
\backprime\backprime\mathrm{i}\prime\prime & \backprime\backprime\mathrm{i}\prime\prime }
}$$

One nice property possessed by the sign relations $L_\mathrm{A}$ and $L_\mathrm{B}$ is that their connotative components $\mathop{Con} L_\mathrm{A}$ and $\mathop{Con} L_\mathrm{B}$ form a pair of equivalence relations on their common syntactic domain $S = I$.  It is convenient to refer to such a structure as a _semiotic equivalence relation_ (SER) since it equates signs that mean the same thing to some interpreter.  Each of the SERs, $\mathop{Con} L_\mathrm{A}, \mathop{Con} L_\mathrm{B} \subseteq S \:\times\: I \cong S \:\times\: S$ partitions the whole collection of signs into _semiotic equivalence classes_ (SECs).  This makes for a strong form of representation in that the structure of the participants' common object domain $\{ \mathrm{A}, \mathrm{B} \}$ is reflected or reconstructed, part for part, in the structure of each of their _semiotic partitions_ (SEPs) of the syntactic domain $\{ \backprime\backprime\mathrm{A}\prime\prime, \backprime\backprime\mathrm{B}\prime\prime, \backprime\backprime\mathrm{i}\prime\prime, \backprime\backprime\mathrm{u}\prime\prime \}$.  But it needs to be observed that the semiotic partitions for interpreters $\mathrm{A}$ and $\mathrm{B}$ are not the same, indeed, they are orthogonal to each other.  This makes it difficult to interpret either one of the partitions or equivalence relations on the syntactic domain as corresponding to any sort of objective structure or invariant reality, independent of the individual interpreter's point of view.

Information about the contrasting patterns of semiotic equivalence induced by the interpreters $\mathrm{A}$ and $\mathrm{B}$ is summarized in Tables&#160;5 and 6.  The form of these Tables should suffice to explain what is meant by saying that the SEPs for $\mathrm{A}$ and $\mathrm{B}$ are orthogonal to each other.

$$\array{
\text{Table 5.  SEP for A}
&
\text{Table 6.  SEP for B}
\\
\array{
\arrayopts{\frame{solid}\rowlines{solid}}
\backprime\backprime\mathrm{A}\prime\prime & \backprime\backprime\mathrm{i}\prime\prime \\
\backprime\backprime\mathrm{u}\prime\prime & \backprime\backprime\mathrm{B}\prime\prime }
&
\array{
\arrayopts{\frame{solid}\collines{solid}}
\backprime\backprime\mathrm{A}\prime\prime & \backprime\backprime\mathrm{i}\prime\prime \\
\backprime\backprime\mathrm{u}\prime\prime & \backprime\backprime\mathrm{B}\prime\prime }
}$$

# Notation #

A few items of notation are useful in discussing equivalence relations in general and semiotic equivalence relations in particular.

As a general consideration, if $E$ is an equivalence relation on a set $X$, then every element $x$ of $X$ belongs to a unique equivalence class under $E$ called "the equivalence class of $x$ under $E$".  Convention provides the _square bracket notation_ for denoting this equivalence class, either in the subscripted form $\left[ x \right]_E$ or in the simpler form $\left[ x \right]$ when the subscript $E$ is understood.  A statement that the elements $x$ and $y$ are equivalent under $E$ is called an _equation_ and can be expressed in numerous ways, for example, any of the following equivalent styles:

$$\array{
(x, y) & \in & E
\\
x & \in & \left[ y \right]_E
\\
y & \in & \left[ x \right]_E
\\
\left[ x \right]_E & = & \left[ y \right]_E
\\
x & =_E & y
}$$

Thus we have the following definitions:

$$\array{
[x]_E & \text{:=} & \{ y \in X : (x, y) \in E \}
\\
x =_E y & \iff & (x, y) \in E
}$$

In the application to sign relations it is useful to extend the square bracket notation in the following ways.  If $L$ is a sign relation whose connotative component or syntactic projection $L_{S I}$ is an equivalence relation on $S = I$, let $\left[ s \right]_L$ be the equivalence class of $s$ under $L_{S I}$.  That is to say, $\left[ s \right]_L \:\text{:=}\: \left[ s \right]_{L_{S I}}$.  A statement that the signs $x$ and $y$ are equivalent under a semiotic equivalence relation $L_{S I}$ is called a _semiotic equation_ (SEQ) and can be written in either of the following equivalent forms:

$$\array{
\left[ x \right]_L & = & \left[ y \right]_L
\\
x & =_L & y
}$$

In many situations there is one further adaptation of the square bracket notation that can be useful.  Namely, when there is known to exist a particular triple $(o, s, i) \in L$, it is permissible to let $\left[ o \right]_L \:\text{:=}\: \left[ s \right]_L$.  These modifications are designed to make the notation for semiotic equivalence classes harmonize as well as possible with the frequent use of similar devices for the denotations of signs and expressions.

The SER for interpreter $\mathrm{A}$ yields the following semiotic equations:

$$\array{
\left[ \backprime\backprime\mathrm{A}\prime\prime \right]_{L_\mathrm{A}}
& = &
\left[ \backprime\backprime\mathrm{i}\prime\prime \right]_{L_\mathrm{A}}
\\
\left[ \backprime\backprime\mathrm{B}\prime\prime \right]_{L_\mathrm{A}}
& = &
\left[ \backprime\backprime\mathrm{u}\prime\prime \right]_{L_\mathrm{A}}
}$$

or

$$\array{
\backprime\backprime\mathrm{A}\prime\prime
& =_{L_\mathrm{A}} &
\backprime\backprime\mathrm{i}\prime\prime
\\
\backprime\backprime\mathrm{B}\prime\prime
& =_{L_\mathrm{A}} &
\backprime\backprime\mathrm{u}\prime\prime
}$$

Thus it induces the semiotic partition:

$$\{ \{ \backprime\backprime\mathrm{A}\prime\prime, \backprime\backprime\mathrm{i}\prime\prime \}, \{ \backprime\backprime\mathrm{B}\prime\prime, \backprime\backprime\mathrm{u}\prime\prime \} \}$$

The SER for interpreter $\mathrm{B}$ yields the following semiotic equations:

$$\array{
\left[ \backprime\backprime\mathrm{A}\prime\prime \right]_{L_\mathrm{B}}
& = &
\left[ \backprime\backprime\mathrm{u}\prime\prime \right]_{L_\mathrm{B}}
\\
\left[ \backprime\backprime\mathrm{B}\prime\prime \right]_{L_\mathrm{B}}
& = &
\left[ \backprime\backprime\mathrm{i}\prime\prime \right]_{L_\mathrm{B}}
}$$

or

$$\array{
\backprime\backprime\mathrm{A}\prime\prime
& =_{L_\mathrm{B}} &
\backprime\backprime\mathrm{u}\prime\prime
\\
\backprime\backprime\mathrm{B}\prime\prime
& =_{L_\mathrm{B}} &
\backprime\backprime\mathrm{i}\prime\prime
}$$

Thus it induces the semiotic partition:

$$\{ \{ \backprime\backprime\mathrm{A}\prime\prime, \backprime\backprime\mathrm{u}\prime\prime \}, \{ \backprime\backprime\mathrm{B}\prime\prime, \backprime\backprime\mathrm{i}\prime\prime \} \}$$

# Links #

* [Semiotic Equivalence Relation @ PlanetMath](http://planetmath.org/encyclopedia/SemioticEquivalenceRelation.html)
