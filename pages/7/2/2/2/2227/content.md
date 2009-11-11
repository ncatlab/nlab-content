[[!redirects 3-ary relation]]
[[!redirects 3-ary relations]]
[[!redirects 3-adic relation]]
[[!redirects 3-adic relations]]
[[!redirects 3-place relation]]
[[!redirects 3-place relations]]
[[!redirects ternary relation]]
[[!redirects ternary relations]]
[[!redirects triadic relations]]
[[!redirects triadic relation"]]

* tic
{:toc}

A __triadic relation__ (or a __ternary relation__) is an important special case of a [[relation theory|polyadic or finitary relation]], one in which the number of places in the relation is three.  One may also see the adjectives _3-adic_, _3-ary_, _3-dimensional_, or _3-place_ being used to describe these relations.

Mathematics is positively rife with examples of 3-adic relations, and the concept of a [[sign relation]], a special case of a 3-adic relation, is fundamental to the field of semiotics, or the theory of signs.  Therefore it will be useful to consider a few concrete examples from each of these two realms.

# Examples from mathematics #

Let $\mathbb{B} = \{ 0, 1 \}$ and let "+" be taken in the sense of GF(2).

For the sake of topics to be taken up later it is useful to examine a pair of 3-adic relations in tandem that are defined as follows:

$$L_0 = \{ (x, y, z) \in \mathbb{B}^3 : x + y + z = 0 \}.$$

$$L_1 = \{ (x, y, z) \in \mathbb{B}^3 : x + y + z = 1 \}.$$

The triples that make up the relations $L_0$ and $L_1$ are conveniently arranged in the form of relational data tables, as follows:

$$
\array{
\array{
\arrayopts{\frame{solid}\rowlines{solid solid none}}
\cellopts{\colspan{3}} L_0 = \{ (x, y, z) \in \mathbb{B}^3 : x + y + z = 0 \} \\
x & y & z \\
0 & 0 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
1 & 1 & 0  }
&
\array{
\arrayopts{\frame{solid}\rowlines{solid solid none}}
\cellopts{\colspan{3}} L_1 = \{ (x, y, z) \in \mathbb{B}^3 : x + y + z = 1 \} \\
x & y & z \\
0 & 0 & 1 \\
0 & 1 & 0 \\
1 & 0 & 0 \\
1 & 1 & 1  }
}
$$

# Examples from semiotics #

The study of signs, the full array of significant forms of expression, in relation to the things that signs are significant _of_, as well as in relation to the interpretive agents that signs are significant _to_, is known as _semiotics_ or the _theory of signs_.  As just described, semiotics treats of 3-place relations among signs, their objects, and their interpreters.

The term _semiosis_ refers to any activity or process that involves signs.  Studies of semiosis that deal with its more abstract form are not concerned with every concrete detail of the entities that act as signs, objects, or agents of semiosis, but only with the most salient patterns of relationship among these three roles.  In particular, the formal theory of signs does not consider every property of the interpretive agent but only the more striking features of the impressions that signs make on a representative interpreter.  In its formal aspects that impact or influence may be treated as just another sign, called the _interpretant sign_, or the _interpretant_ for short.  Hence the definition of a [[sign relation]] as a 3-adic relation among objects, signs, and interpretants.

For example, consider the aspects of sign use that concern two people, say, $\mathrm{Ann}$ and $\mathrm{Bob}$, in using their own proper names, "$\mathrm{Ann}$" and "$\mathrm{Bob}$", and in using the pronouns, "$\mathrm{I}$" and "$\mathrm{you}$".  For simplicity, these four signs may be abbreviated to form the set $\{ \backprime\backprime\mathrm{A}\prime\prime, \backprime\backprime\mathrm{B}\prime\prime, \backprime\backprime\mathrm{i}\prime\prime, \backprime\backprime\mathrm{u}\prime\prime \}$.  The abstract consideration of how $\mathrm{A}$ and $\mathrm{B}$ use this set of signs to refer to themselves and to each other leads to the contemplation of a pair of 3-adic relations, the sign relations $L_{\mathrm{A}}$ and $L_{\mathrm{B}}$, that reflect the differential use of these signs by $\mathrm{A}$ and $\mathrm{B}$, respectively.

Each of the sign relations, $L_{\mathrm{A}}$ and $L_{\mathrm{B}}$, consists of eight triples of the form $(x, y, z)$, where the object $x$ belongs to the object domain $O = \{ \mathrm{A}, \mathrm{B} \}$, where the sign $y$ belongs to the sign domain $S$, where the interpretant sign $z$ belongs to the interpretant domain $I$, and where it happens in this case that $S = I = \{ \backprime\backprime\mathrm{A}\prime\prime, \backprime\backprime\mathrm{B}\prime\prime, \backprime\backprime\mathrm{i}\prime\prime, \backprime\backprime\mathrm{u}\prime\prime \}$.  In general, it is convenient to refer to the union $S \:\cup\: I$ as the _syntactic domain_, but in this case $S = I = S \:\cup\: I$.

The set-up so far can be summarized as follows:

$$\array{
L_{\mathrm{A}}, L_{\mathrm{B}} & \subseteq & O \quad\times\quad S \quad\times\quad I
\\
O & = & \{ \mathrm{A}, \mathrm{B} \}
\\
S & = & \{ \backprime\backprime\mathrm{A}\prime\prime, \backprime\backprime\mathrm{B}\prime\prime, \backprime\backprime\mathrm{i}\prime\prime, \backprime\backprime\mathrm{u}\prime\prime \}
\\
I & = & \{ \backprime\backprime\mathrm{A}\prime\prime, \backprime\backprime\mathrm{B}\prime\prime, \backprime\backprime\mathrm{i}\prime\prime, \backprime\backprime\mathrm{u}\prime\prime \}
}$$

The triples that make up the relations $L_{\mathrm{A}}$ and $L_{\mathrm{B}}$ are conveniently arranged in the form of relational data tables, as follows:

$$\array{
\array{\arrayopts{\frame{solid}\rowlines{solid solid none}}
\cellopts{\colspan{3}} L_{\mathrm{A}} = \text{Sign Relation of Interpreter A} \\
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
\cellopts{\colspan{3}} L_{\mathrm{B}} = \text{Sign Relation of Interpreter B} \\
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

* The triples in $L_{\mathrm{A}}$ represent the way that interpreter $\mathrm{A}$ uses signs.  For example, the listing of the triple $(\mathrm{B}, \backprime\backprime \mathrm{u} \prime\prime, \backprime\backprime \mathrm{B} \prime\prime)$ in $L_{\mathrm{A}}$ represents the fact that $\mathrm{A}$ uses $\backprime\backprime \mathrm{B} \prime\prime$ to mean the same thing that $\mathrm{A}$ uses $\backprime\backprime \mathrm{u} \prime\prime$ to mean, namely, $\mathrm{B}$.

* The triples in $L_{\mathrm{B}}$ represent the way that interpreter $\mathrm{B}$ uses signs. For example, the listing of the triple $(\mathrm{B}, \backprime\backprime \mathrm{i} \prime\prime, \backprime\backprime \mathrm{B} \prime\prime)$ in $L_{\mathrm{B}}$ represents the fact that $\mathrm{B}$ uses $\backprime\backprime \mathrm{B} \prime\prime$ to mean the same thing that $\mathrm{B}$ uses $\backprime\backprime \mathrm{i} \prime\prime$ to mean, namely, $\mathrm{B}$.

# Related topics #

* [[sign relation]]
* [[referent equivalence relation]]
* [[semiotic equivalence relation]]

# Links #

* [Triadic Relation @ MyWikiBiz](http://mywikibiz.com/Triadic_relation)

* [Triadic Relation @ PlanetMath](http://planetmath.org/encyclopedia/TriadicRelation.html)

# Discussion #

[[Toby Bartels]]: Is this from [[Charles Sanders Peirce|Peirce]]\'s theory of signs?  Have later researchers (mathematicians, logicians, semioticists, ...) continued to work on this?  ---Toby

[[Jon Awbrey]]: Yes, I'll always be hewing to Peirce's line in this --- sometimes people use the form _[semeiotic](http://knol.google.com/k/jon-awbrey/semeiotic/3fkwvf69kridz/4)_ to distinguish his angle from others, but that often leads to long and pointless discussions about the words instead of the things.  I'll be giving some current links and references in due course.

[[Jon Awbrey]]: Actually, I think that's pretty much all I'll have to say about sign relations under this heading --- leaving these examples here simply by way of having illustrations of 3-adic relations with non-identical domains --- and developing the subject of sign relations further under their own heading.  It's probably hard to tell from these impoverished examples, but there are applications to logic and computation --- eventually, ultimately --- which is kinda how I came to explore them in the first place.
