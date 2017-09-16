+-- {: .query}
[[Urs Schreiber|Urs]]:  The 0th space of the K-theory [[spectrum]] is $\mathbb{Z} \times B U$. I'd like to know a good way to encode the [[symmetric monoidal (infinity,1)-category|symmetric monoidal]] [[infinity-groupoid]] that this is the realization of.

Here is one thing that I talked about with [[Thomas Nikolaus]]. I'd like to know if anything along these lines has been considered before, and if so, if somebody has a reference, or can even provide some details here.

So start with the category $Vect$ of finite dimensional complex vector spaces. This has two standard monoidal structures, one coming from direct sum, the other from tensor product of vector spaces. The tensor product monoidal structure disctributes over the direct sum monoidal structure.

Let then $\mathbf{B}_\oplus Vect$ be the suspension of $Vect$ to a one-object [[bicategory]] using the direct sum monoidal structure. Let $N \mathbf{B}_\oplus Vect$ be its (Duskin) [[nerve]]. Let $Ex^\infty N \mathbf{B}_\oplus Vect$ be the [[Kanification]] of this [[nerve]]. Then consider the [[infinity-groupoid]] given by the loop [[Kan complex]] of that:

$$
  \Omega Ex^\infty N \mathbf{B}_\oplus Vect
  \,.
$$

This $\infty$-groupoid looks like it has good chances to be the one that gives the K-theory spectrum under realization $|-| : \infty Grpd \to Top$. 

* By the way $Ex^\infty$ works its objects are formal differences of vector spaces ([[groupoidification]] of the direct sum operation on vector spaces). 

* Morphisms are correspondingly formal direct sums/differences of linear maps, between vector spaces of arbitrary finite dimension. (Maybe one should start not with $Vect$ but with $Core(Vect)$, the maximal groupoid inside $Vect$ for the above?)

* Since the tensor product monoidal structure on $Vect$ distributes over $\oplus$, this Kanified $B Vect$ thing should still be symmetric monoidal.


=--
