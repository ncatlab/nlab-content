
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Definition

### Discrete

A __$K$-linear map__ (also __$K$-linear function__, __$K$-[[linear operator]]__, or __$K$-linear transformation__) is a [[morphism]] in $K$-[[Vect]] (or $K$-[[Mod]]), that is a [[homomorphism]] of [[vector spaces]] (or [[modules]]).  Often one suppresses mention of the [[field]] (or [[commutative ring]] or [[rig]]) $K$.

In elementary terms, a __$K$-linear map__ between $K$-[[linear spaces]] $V$ and $W$ is a [[function]] $T\colon V \to W$ such that
$$ T(r x + y) = r T(x) + T(y) ,$$
for $x$ and $y$ elements of $V$ and $r$ an element of $K$.  (It is an easy exercise that this one identity is enough to ensure that $T$ preserves all [[linear combination | linear combinations]].)


### Topological

The [[morphisms]] between [[topological vector spaces]] are of course the [[continuous map|continuous]] linear maps.  Between [[Banach spaces]] (including of course [[Hilbert spaces]]), these are the same as the [[bounded map|bounded]] linear maps, so they\'re often called __[[bounded operators]]__ (with linearity tacitly assumed).

In this context, __[[linear operators]]__ are more general; they are (in general) only [[partial functions]].  However, we still require the [[domain]] of the partial function to be a linear [[subspace]], after which the definition above applies.  Because one typically restricts attention to [[complete spaces]], the [[densely-defined operator | densely-defined operators]] (where the domain is a [[dense subspace]]) are the most general needed.  To specify that the domain of a linear operator $T\colon V \to W$ is all of $V$, one may use a non-'operator' term, such as __linear mapping__.

Notice that we do *not* require partially-defined linear operators to be continuous; see [[unbounded operator]].  However, we have the theorem that any densely-defined, continuous, linear map $T\colon V \to W$, with $W$ [[complete space|complete]] and [[Hausdorff space|Hausdorff]], extends uniquely to all of $V$.  Thus one typically assumes that a continuous (or bounded) linear operator $T$ is defined on all of $V$ while an arbitrary linear operator $T$ is defined only on a dense subspace of $V$.


\begin{remark}
**(Terminology)**
In elementary mathematics (at least as taught in the United States, perhaps elsewhere?), the term 'linear function' is usually used more generally, for an [[affine map]] (but still between vector spaces); in this same context, the term 'linear transformation' is often used instead for specifically linear maps.  (Another difference at this level is that 'linear functions' are usually scalar-valued, while 'linear transformations' are usually vector-valued.)

In [[operator algebra|operator theory]], one sometimes distinguishes 'linear maps' (defined everywhere, but not necessarily continuous in general) from 'linear operators' (partially defined in general, but assumed to be defined everywhere if continuous between complete Hausdorff spaces).  There is also a tendency for 'operator' to be used only for (possibly partial) [[endomorphisms]], that is $T\colon V \to V$; then operators may be [[composition|composed]], giving rise to an [[operator algebra]].  If $V$ is a [[function space]], then an endomorphism of $V$ is an [[operator]] in the sense of [[higher-order logic]]; the more general meaning of 'linear operator' is abstracted from this.
\end{remark}

## Properties

* [[rank-nullity theorem]]


## Related concepts

* [[function]], [[quadratic function]], [[polynomial function]]

* [[operator product]]

* [[linear isomorphism]], [[linear isometry]]

* [[bounded linear operator]] / [[unbounded linear operator]]

* [[operator algebra]]

* [[eigenvector]], [[eigenvalue]]

* [[antilinear map]]

* [[self-adjoint operator]], [[positive operator]]

* [[linear subspace]]

* [[linear differential equation]]


## References

### General

Textbook accounts:

* [[Igor R. Shafarevich]], [[Alexey O. Remizov]]: §4 in: *Linear Algebra and Geometry* (2012) &lbrack;[doi:10.1007/978-3-642-30994-6](https://doi.org/10.1007/978-3-642-30994-6), [MAA-review](https://maa.org/press/maa-reviews/linear-algebra-and-geometry)&rbrack; 

### On Hilbert spaces

On linear operators on [[Hilbert spaces]] (see also at *[[operator algebra]]*):

Lecture notes:

* [[Bergfinnur Durhuus]], *Operators on Hilbert Space* &lbrack;[pdf](https://web.math.ku.dk/~durhuus/MatFys/MatFys4.pdf), [[Durhuus-OperatorsOnHilbertSpace.pdf:file]]&rbrack;



[[!redirects linear map]]
[[!redirects linear maps]]
[[!redirects linear mapping]]
[[!redirects linear mappings]]
[[!redirects linear function]]
[[!redirects linear functions]]

[[!redirects linear transformation]]
[[!redirects linear transformations]]

[[!redirects linear operator]]
[[!redirects linear operators]]
