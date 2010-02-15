#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A **suspended category** is an [[additive category]] $C$ equipped with an additive functor $S:C\to C$ called __suspension__ and a class of $S$-sequences called __triangles__ satisfying axioms below. Here one calls an _$S$-sequence_ a sequence of morphisms of the form
$$
X\stackrel{f}\to Y\stackrel{g}\to Z\stackrel{h}\to S X,
$$
and morphisms are ladders of the type
$$\array{
X&\stackrel{f}\to &Y&\stackrel{g}\to &Z&\stackrel{h}\to& S X\\
a\downarrow&&b\downarrow&&c\downarrow&&\downarrow S a\\
 X'&\stackrel{f'}\to &Y'&\stackrel{g'}\to &Z'&\stackrel{h'}\to& S X',\\
}$$
where all the squares commute. Axioms:

(SP0) Each sequence [[isomorphism|isomorphic]] to a triangle is a triangle.

(SP1) Each sequence of the form $0\to X\stackrel{id}\to X\to S0$ is a triangle.

(SP2) If $X\stackrel{f}\to Y\stackrel{g}\to Z\stackrel{h}\to S X$ is a triangle, then $Y\stackrel{g}\to Z\stackrel{h}\to S X\stackrel{-S f}\to S Y$ is also a triangle.

(SP3) Every [[diagram]] of the form 

$$\array{
X&\stackrel{f}\to &Y&\stackrel{g}\to &Z&\stackrel{h}\to& S X\\
a\downarrow&&b\downarrow&&&&\downarrow S a\\
 X'&\stackrel{f'}\to &Y'&\stackrel{g'}\to &Z'&\stackrel{h'}\to& S X'\\
}$$

can be completed to a morphism of $S$-sequences.

(SP4) For any two morphisms $X\stackrel{f}\to Y$ and
$Y\stackrel{g}\to Z$ there is a commuting diagram
$$\array{
X&\stackrel{f}\to &Y&\stackrel{g}\to &Z'&\to& S X\\
=\downarrow&&f\downarrow&&\downarrow&&=\downarrow \\
 X&\to &Z&\to &Y'&\to& S X\\
&&\downarrow&&\downarrow&&\downarrow S f\\
 & &X'&\stackrel{id}\to &X'&\stackrel{j}\to& S Y\\
&&j\downarrow&&\downarrow&&\\
 &&S Y&\stackrel{S i}\to &S Z'&&\\
}$$
where the first two rows and the middle two columns are triangles. 

## Examples

* Every [[triangulated category]] is suspended. 

* Every suspended category in which $S$ is an equivalence is triangulated. 

* Under mild assumptions, the [[stable category]] of [[Quillen exact category]] $(A,E)$ is a suspended category. If $A$ is [[Frobenius category]] then $A$ is [[triangulated category]].

## References

Suspended categories were introduced in

* [[Bernhard Keller]], Dieter Vossieck,
Sous les cat&#233;gories d&#233;riv&#233;es. [Beneath the derived categories] C. R. Acad. Sci. Paris S&#233;r. I Math. 305 (1987), no. 6, 225--228. 

See also 

* B. Keller, Chain complexes and stable categories, Manus. Math. 67 (1990), 379-417.