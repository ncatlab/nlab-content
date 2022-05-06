
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Geometry
+-- {: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


> To this day, the theorem of Pythagoras remains the most important single theorem in the whole of mathematics. -- Jacob Bronowski, _The Ascent of Man_, page 160. 

# Contents 
* table of contents 
{: toc} 

## Introduction and History 

In [[Euclidean geometry]], the _Pythagorean theorem_ expresses a necessary and sufficient condition on the [[lengths]] of the three sides of a [[triangle]] in order for it to be a right triangle. In the popular mind it is associated with the equation 

$$a^2 + b^2 = c^2,$$ 

where $c$ denotes the length of the hypotenuse of a right triangle, and $a, b$ are the lengths of the other two sides. 

It was apparently known (in some form or other) by a number of ancient civilizations (Mesopotamia, circa 1800 BCE[^1]; China, Zhou Dynasty, circa 1000 BCE[^2]), and appears in [[Euclid]]'s _[[Elements]]_ as a capstone result of Book 1 (as Proposition 47, and Proposition 48 for the converse). [Wikipedia](http://en.wikipedia.org/wiki/Pythagorean_theorem#Pythagorean_triples) mentions, but without a citation, that certain megalithic monuments in Northern Europe indicate that [[Pythagorean triples]] were known even before the invention of writing systems.[^2.5] 

[^1]: See [Maor](#Maor), chapter 1. 
[^2]: See [Wikipedia](http://en.wikipedia.org/wiki/Zhou_Bi_Suan_Jing), which exhibits an apparent proof based on the famous 'pinwheel' configuration. 
[^2.5]: On the other hand, the oft-repeated mention of the use of knotted ropes or the like in Ancient Egypt, to mark off 3-4-5 triangles and hence right angles, appears to have no scholarly backing whatsoever. 

While it was traditional among ancient historians to credit [[Pythagoras]] with the first recorded [[proof]] (at least the first from Hellenic civilization), there is cause to believe that this (semi-legendary) individual had little to do personally with such a proof or even with mathematics generally within his school -- without however there being doubt that this result and other mathematical ideas were vigorously discussed and developed by the Pythagoreans. 


## Proof 

There are apparently hundreds of proofs. It should be noted that the Pythagorean theorem is a [[theorem]] of [[Euclidean geometry]] and depends on Euclid's [[parallel postulate]], particularly the consequence that the sum of the interior angles of a triangle is invariably $180^\circ$. 

+-- {: .num_remark} 
###### Remark 
As perhaps goes without saying, very few of these proofs could be considered even remotely serious as "proofs" by the strict standards of modern axiomatic mathematics developed in the last one hundred years or so. That remark applies in particular to the pretend "proof" that follows, where there is for example some unanalyzed notion of adding angles and so on. Of course it can be made rigorous, but just how one goes about it is a matter of interest. One could for example situate it within a grand edifice (based on a [[set theory|theory of sets]]) that allows one to construct the [[real number]] system which in turn is used to model [[Euclidean spaces]]. Or one could proceed from a much more local axiomatic system, such as the axiomatics in Hilbert's *Grundlagen der Geometrie* or Tarski's Elementary Euclidean Geometry. In any case, in what follows we'll brush all such considerations under the rug, and beg the reader's indulgence to take the word "proof" here with whatever size grain of salt he or she requires. 
=-- 

One proof[^3] proceeds by constructing, given a right triangle with side lengths $a, b$ and hypotenuse length $c$, the unique line incident to the vertex at the right angle that meets the hypotenuse in a right angle. (N.B.: this construction is specific to Euclidean geometry.) This bisects the hypotenuse into two line segments, of length $c_1, c_2$ say with $c_1 + c_2 = c$. (A picture is given [here](http://en.wikipedia.org/wiki/Pythagorean_theorem#Proof_using_similar_triangles).) Moreover the given right triangle is thereby bisected into two right triangles, and due to the fact that the sum of the interior angles is always $180^\circ$, it may be seen that the two right triangles are similar (i.e., in proportion) to the given right triangle. Therefore, if one has side lengths $h, c_1$ and hypotenuse $a$ say, and the other has side lengths $h, c_2$ and hypotenuse $b$, we may derive proportionality equations 

$$c_1/a = a/c, \qquad c_2/b = b/c,$$ 

from which we may derive $a^2 + b^2 = c_1 c + c_2 c = (c_1 + c_2)c = c^2$. 

[^3]: The proof which appears in Book 1 of the _[[Elements]]_ looks somewhat more elaborate, but the proof based on similar triangles perhaps had to await the development of a theory of proportion, set out in Book 5. 


## Modern points of view 

One modern point of view on the Pythagorean theorem is the following:

Without loss of generality, we may consider the context of a 2-dimensional [[Euclidean space]] (the theorem being trivial in lower dimensions, and Euclidean structure on a higher-dimensional space just amounting to compatible Euclidean structure on each of its 2-dimensional subspaces). Over such a space, we consider the symmetric bilinear product taking two vectors to the oriented area of the parallelogram formed by the first and the quarter-turn of the second. (The quarter-turn operator is only canonical up to negation, but it doesn't matter for the canonicality of this product, interpreting its codomain suitably). Vectors are perpendicular just in case this product of them is zero; furthermore, the quadratic form corresponding to this product takes a vector to the area of the square formed upon it, which is to say, its squared length. Thus, we are in fact using the notions of perpendicularity and length which arise from an [[inner product space]], and the Pythagorean Theorem amounts to a special case of the simple algebraic identity $(a+b)^2=a^2+b^2+2 a b$ (which more generally is the [[Law of Cosines]]).

That the Pythagorean Theorem holds in an inner product space is trivial; all that matters is establishing that one is, in fact, working in an inner product space. What it takes to establish this depends on what one is starting from (e.g., one might just as well axiomatize Euclidean geometry as the study of inner product spaces of particular dimension&#8230;), but the above approach might fairly be construed as teasing out the inner product structure inherent in geometry as an interested amateur would already be inclined to think of it.


## References 

Named after [[Pythagoras]] (but see there for the issue of attribution).

* {#Maor} Eli Maor, _The Pythagorean Theorem: A 4000-year History_, Princeton University Press, 2007. 


[[!redirects Pythagorean theorem]]
[[!redirects Pythagorean Theorem]]
[[!redirects Pythagoras theorem]]
[[!redirects Pythagoras Theorem]]
