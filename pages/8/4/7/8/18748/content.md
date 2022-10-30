
> This entry is about the concepts of direction of a vector and of a line in [[linear algebra]]/[[analytic geometry]]. For the concept in [[order theory]] see at _[[direction]]_.


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[vector space|vector]]/[[affine space|affine]] [[geometry]] the [[parallel]] [[vectors]] with the same [[orientation]] form an [[equivalence class]].  The same holds for oriented lines and even higher dimensional oriented subspaces.  The equivalence class of a vector (or other object) is called its *direction*.  (In the case of higher dimension we may say "$n$-direction"; see also [[bivector]].)  If the vector space is [[normed space|normed]], then each such equivalence class has a canonical [[unit vector]] representative, called a *direction vector*.

If we neglect the orientation we get a bigger equivalence class, called the *unoriented direction*.  Unoriented directions have a representing unit vector only up to sign.

## Definition

### Oriented direction


+-- {: .num_defn #DirectionOfAVector}
###### Definition


For $V$ a [[real vector space]], or more generally a vector space over an [[ordered field]], the _direction_ of a non-zero vector $v \in V$ is its [[equivalence class]] under the multiplication with [[positive number|positive]] scalars.  

If $V$ is a [[normed vector space]] (such as an [[inner product space]] with the induced [[norm]] $v\mapsto \sqrt{\langle v, v\rangle}$), the _direction_ of $v$ is canonically represented by the unit norm vector obtained by multiplying $v$ with the inverse of its [[norm]]

$$
  \tfrac{1}{\vert v\vert} v \;\in \; S(V) \subset V
  \,,
$$

which may be regarded as an element of the [[unit sphere]] $S(V)$ of $V$.

=--

(e.g. [MathWorld](#MathWorld))


Equivalently:

Recall that a nonzero vector $v$ is _parallel_ to a [[linear subspace]] $W$ of a vector space $V$ if $v$ has a representative of the form $\vec{A B}$ (i.e. $v = B - A$) with $A,B\in W$.  When $W$ is a [[line]], we say that $v$ furthermore has the same [[orientation]] as $W$ if $\vec{A B}$ points (in the sense of def. \ref{DirectionOfAVector}) in the positive direction along $W$.


+-- {: .num_defn #SheavesOnCartSp}
###### Definition

The _direction_ of a non-zero vector $v \in V$ is the [[equivalence class]] of oriented lines parallel to $v$ and having the same orientation.

=--

### Unoriented direction

Similarly, the _unoriented direction_ of a non-zero vector in any vector space is its [[equivalence class]] under multiplication by non-zero elements of the [[ground field]], hence the element it represents in the corresponding [[projective space]] $P V$.  Unlike oriented direction, this makes sense over an arbitrary field.

The unit direction vector can be attached not only to a (direction of) a vector but also to a direction of lines per se (see Wikipedia, _[Direction vector](https://en.wikipedia.org/wiki/Direction_vector)_).

J. Lelong-Ferrand defines the direction of an affine subspace of an affine space as its orbit under the action of the translation group. This agrees with the parallelness in Choquet where two affine subspaces of the same dimension are parallel if their translation group of vectors (as a subgroup of the group of vectors of translations of the entire space) is the same. 

## Examples
 {#Examples}

+-- {: .num_example #WaveFronts}
###### Example
**([[wave front set|wave fronts]])

In [[microlocal analysis]] the _[[wave front set]]_ of a [[distribution]] records the direction (def. \ref{DirectionOfAVector}) of all those [[wave vectors]] along which, locally, the [[Fourier transform of distributions|Fourier transform of the distribution]] is not a [[rapidly decaying function]].

=--

## Related concepts

* [[norm]], [[length]], [[absolute value]]

* [[wave vector]], [[orientation]], [[bivector]]

## References

* {#MathWorld} MathWorld, _[Unit vector](http://mathworld.wolfram.com/UnitVector.html)_

* Gustave Choquet, _Geometry in a modern setting_, Hermann 1969

* K. Horvati&#263;, _Linear algebra_ (in Croatian), 2004

* Jacquelline Lelong-Ferrand, _Les fondements de la g&#233;om&#233;trie_, Presses Universitaires de France 1985.

[[!redirects directions of vectors]]
[[!redirects direction vector]]
[[!redirects direction of a line]]