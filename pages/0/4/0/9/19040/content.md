# Double category of algebras

* table of contents
{: toc}

## Idea

For a [[2-monad]] $T$, there are several naturally defined [[2-categories]] of $T$-[[algebra over a monad|algebras]], depending on whether we take the [[morphisms]] to be [[lax morphism|lax]], colax (oplax), strong/pseudo, or strict.  Of these, the lax and colax cases $T Alg_l$ and $T Alg_c$ are the most general, since a strict morphism is also strong, and a strong morphism can be regarded as either lax or colax (using the structure morphisms or their inverses).

There is no natural 2-category that contains *both* lax and colax morphisms, since a lax morphism cannot be composed with a colax morphism and obtain any sort of $T$-morphism.  However, lax and colax $T$-morphisms can be combined as the horizontal and vertical morphisms in a [[double category]].  This double category allows a characterization of strong morphisms as [[companion pairs]], of [[doctrinal adjunctions]] as [[conjoint pairs]], and its 2-cells are relevant for defining [[oplax/lax comma objects]].

## Definition

Let $T$ be a [[2-monad]] on a [[2-category]] $K$.  The objects of the double category $T \mathbf{Alg}$ are the $T$-algebras, the horizontal morphisms are the [[lax morphism|lax]] $T$-morphisms, and the vertical morphisms are the colax $T$-morphisms.  The 2-cells are 2-cells in $K$ between composites of underlying morphisms, such that a certain cube of structure 2-cells commutes: consider a square
\begin{tikzcd}
A \ar[r, "f"]\ar[d,"h"] & B\ar[d, "g"] \\
C \ar[r,"k"]& D
\end{tikzcd}
where horizontal arrows are lax $T$-morphism, and vertical ones are colax. A 2-cell $\alpha : g f \Rightarrow k h$ fills the square and it is such that the equality of pasting diagrams 
\begin{tikzcd}[row sep=5mm]
& TB \ar[shorten <=12mm,shorten >=12mm, Rightarrow, dddl]\arrow[rd] \arrow[dd] & & & & TB\ar[shorten <=4mm,shorten >=4mm, Rightarrow, dd, "T\alpha"] \arrow[rd] & \\
TA \arrow[ru] \arrow[dd] & & TD\arrow[dd] & & TA \arrow[rd] \arrow[ru] \arrow[dd] & & TD \ar[shorten <=12mm,shorten >=12mm, Rightarrow, dddl] \arrow[dd] \\
& B\ar[shorten <=4mm,shorten >=4mm, Rightarrow, ur] \ar[shorten <=4mm,shorten >=4mm, Rightarrow, dd, "\alpha"]\arrow[rd] & & = & & TC \arrow[ru] \arrow[dd] & \\
A \arrow[ru] \arrow[rd] & & D & & A \arrow[rd] \ar[shorten <=4mm,shorten >=4mm, Rightarrow, ur] && D \\
 & C \arrow[ru] & & & & C \arrow[ru] & 
\end{tikzcd}
holds. This means that a certain diagram of 2-cells, that can be obtained translating the above equality into a commutative hexagon, is commutative.
 
For a concrete example in the case of monoidal categories, take [[lax monoidal functors]] $F:A\to B$ and $G:C\to D$ and colax monoidal functors $H:B\to D$ and $K:A\to C$, this cube becomes a commutative hexagon:

$$\array{
H(F x \otimes F y) & \to & H F (x\otimes y) & \to & G K (x\otimes y) \\
\downarrow &&&& \downarrow \\
H F x \otimes H F x & \to & G K x \otimes G K x & \to & G (K x \otimes K y).
}$$

If $K$ is a [[strict 2-category]], then $T \mathbf{Alg}$ is a strict double category; otherwise it is "pseudo in both directions" in some sense (such double categories can be defined, but are tricky; see [[double category]]).  As the objects we can use either strict $T$-algebras (if $T$ is a strict 2-monad) or pseudo algebras (if $T$ is either a strict or a pseudo 2-monad).

## Properties

* The horizontal 2-category of $T \mathbf{Alg}$ is the 2-category $T Alg_l$ of lax $T$-morphisms, and its vertical 2-category is $T Alg_c$.

* There is a forgetful double functor from $T \mathbf{Alg}$ to the double category $\mathbf{Q}(K)$ of [[quintets]] in $K$.  In fact, $T \mathbf{Alg}$ can be enhanced to a [[triple category]] whose "transversal morphisms" are *strict* $T$-morphisms (or pseudo ones, if $T$ is only pseudo, in which case we have to deal with "triply pseudo triple categories"), and the induced forgetful functor from this triple category to the triple category of "quintets and commutative cubes" in $K$ is [[monadic functor|monadic]] in an appropriate sense.

* A [[companion pair]] in $T \mathbf{Alg}$ consists of two isomorphic morphisms in $K$ between a pair of $T$-algebras along with a pseudo $T$-morphism structure on one (hence both).  The category of companion pairs between two $T$-algebras is thus equivalent (though not isomorphic) to the category of pseudo $T$-morphisms.

* A [[conjoint pair]] in $T \mathbf{Alg}$ is precisely a "colax/lax" or [[doctrinal adjunction]], and the theorems about [[doctrinal adjunction]] can naturally be expressed as lifting properties of the forgetful functor from $T \mathbf{Alg}$ to $\mathbf{Q}(K)$.

* The universal 2-cell of an [[oplax/lax comma object]] has the structure of a square in $T \mathbf{Alg}$.  Its universal property ought to be related to $T \mathbf{Alg}$ as well, but this is still unclear.


[[!redirects double category of algebras]]
[[!redirects double category of T-algebras]]
[[!redirects double category of algebras over a 2-monad]]
[[!redirects double category of algebras for a 2-monad]]

[[!redirects double categories of algebras]]
[[!redirects double categories of T-algebras]]
[[!redirects double categories of algebras over a 2-monad]]
[[!redirects double categories of algebras for a 2-monad]]
