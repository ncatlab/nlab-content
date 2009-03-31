#Definition#

A **suspended category** is an [[additive category]] $C$ equipped with an additive functor $S:C\to C$ called __suspension__ and a class of $S$-sequence called __triangles__ satisfying axioms below. Here one calls an $S$-sequence a sequence of morphisms of the form
$$
X\stackrel{f}\to Y\stackrel{g}\to Z\stackrel{h}\to SX,
$$
and morphisms are ladders of the type
$$\array{
X&\stackrel{f}\to &Y&\stackrel{g}\to &Z&\stackrel{h}\to& SX\\
a\downarrow&&b\downarrow&&c\downarrow&&\downarrow Sa\\
 X'&\stackrel{f'}\to &Y'&\stackrel{g'}\to &Z'&\stackrel{h'}\to& SX',\\
}$$
where all the squares commute. Axioms:

(SP0) Each sequence [[isomorphism|isomorphic]] to a triangle is a triangle.

(SP1) Each sequence of the form $0\to X\stackrel{id}\to X\to S0$ is a triangle.

(SP2) If $X\stackrel{f}\to Y\stackrel{g}\to Z\stackrel{h}\to SX$ is a triangle, then $Y\stackrel{g}\to Z\stackrel{h}\to SX\stackrel{-Sf}\to SY$ is also a triangle.

(SP3) Every [[diagram]] of the form 

$$\array{
X&\stackrel{f}\to &Y&\stackrel{g}\to &Z&\stackrel{h}\to& SX\\
a\downarrow&&b\downarrow&&&&\downarrow Sa\\
 X'&\stackrel{f'}\to &Y'&\stackrel{g'}\to &Z'&\stackrel{h'}\to& SX'\\
}$$

can be completed to a morphism of $S$-sequences.

(SP4) For any two morphisms $X\stackrel{f}\to Y$ and
$Y\stackrel{g}\to Z$ there is a commuting diagram
$$\array{
X&\stackrel{f}\to &Y&\stackrel{g}\to &Z'&\to& SX\\
=\downarrow&&f\downarrow&&\downarrow&&=\downarrow \\
 X&\to &Z&\to &Y'&\to& SX\\
&&\downarrow&&\downarrow&&\downarrow Sf\\
 & &X'&\stackrel{id}\to &X'&\stackrel{j}\to& SY\\
&&j\downarrow&&\downarrow&&\\
 &&SY&\stackrel{Si}\to &SZ'&&\\
}$$
where the first two rows and the middle two columns are triangles. 

#Examples#

* Every [[triangulated category]] is suspended. 

* Every suspended category in which $S$ is an equivalence is triangulated. 

* Under mild assumptions, the [[stable category]] of [[Quillen exact category]] $(A,E)$ is a suspended category. If $A$ is [[Frobenius category]] then $A$ is [[triangulated category]].

#References#

Suspended categories were introduced in

* Bernhard Keller, Dieter Vossieck,
Sous les cat&#233;gories d&#233;riv&#233;es. [Beneath the derived categories] C. R. Acad. Sci. Paris S&#233;r. I Math. 305 (1987), no. 6, 225--228. 

See also 

* B. Keller, Chain complexes and stable categories, Manus. Math. 67 (1990), 379-417.