
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

Throughout, we work in the category $Bant$ whose objects are Banach spaces and where the morphisms are continuous linear maps. References below to the unit ball suggest that it _might_ be premature to cast everything in terms of a certain subcategory of TVS.

## Duality
Following the lead of Mac Lane (2nd ed.) Section IV.2, which does this for vector spaces) but with slight changes in notation: let $\overline{D}:Bant\to Bant$ be the contravariant functor which takes a Banach space to its [[dual vector space|dual space]], and sends a continuous linear map to its adjoint/dual map.

This gives rise, in a straightforward way, to two functors $D_L: Bant \to Bant^{op}$
 and $D_R: Bant^{op}\to Bant$. $D_L$ is the left adjoint of $D_R$, that is

$$ Bant^{op}(D_L X, Y) \cong Bant(X, D_R Y) $$

In general
$$ Bant^{op}(Y, D_L X) \not\cong Bant(D_R Y, X) $$
so that $D_L$ is not a right adjoint of $D_R$.
For example: take $Y$ to be the ground field $K$ and $X$ to be $c_0$ with the usual supremum norm.

**Not-a-proof-yet** of this claim: we have $D_R(K)\cong K$ and the $Bant$-morphisms from $K$ to $c_0$ are just vectors in $c_0$; but the $Bant$-morphisms from $D_L(c_0)\cong\ell^1$ to $K$ correspond to the vectors in $\ell^\infty$. (It would seem from this example that even in [[dream mathematics]] one doesn't get $D_L$ being a right adjoin of $D_R$.)

**Unit and counit.**
The unit of this adjunction is the canonical map $\kappa_X: X\to (X^*)^*$ from a Banach space $X$ to its second dual $X^{**}$. In the presence of
[[axiom of choice|Choice]], the [[Hahn–Banach theorem]] ensures that $\kappa_X$ is an isometry.

To get things to run smoothly, we seem to need more than $\kappa_X$ being monic in $Bant$; but I (YC) am not sure which of the usual variants -- extreme, regular, strong, strict -- is the key one.

The counit map $\veps_X: X^{***} \to X^*$ is sometimes known as the Dixmier projection from the third dual of a Banach space to (the canonical image of) its first dual; note that this map is weak-star-to-weak-star continuous. (It is a projection in the sense of vector spaces, by the triangle identity for the adjunction.)


## Definition

A [[Banach space]] $X$ is **reflexive** if $\kappa_X$ is an [[isomorphism]] in $Bant$. If we furthermore grant ourselves Hahn-Banach, then $\kappa_X$ will even be an [[isometric isomorphism]]: an isomorphism in the category of Banach spaces and [[short linear maps]].


## Properties

(...)

If two [[Banach space]]s are isomorphic as TVSes (but not necessarily isometrically isomorphic), then either both are reflexive or both are non-reflexive.

There is a nice proof that closed subspaces of reflexive [[Banach space]]s are reflexive (due to Linton? [^the details and citation are in the book of Cigler-Losert-Michor but the author of this sentence has no access to a copy at time of typing])
using naturality of $\kappa_X$.

It turns out that if $X$ is a [[Banach space]], then it is reflexive if and only if its (norm-)closed unit ball is compact in the $\sigma(X,X^*)$-topology. In particular, if $X$ is reflexive and $E\to X$, $X\to F$ are bounded linear operators, then the composition $E\to F$ is [[weakly compact]] as a linear operator.

A theorem of Davis-Figiel-Johnson-Pelczynski (1974) tells us that the converse is true:  every [[weakly compact]] linear operator between Banach spaces factors through some reflexive Banach space. The intermediate space is constructed by real interpolation and (at least as usually presented) does not seem to be canonical in any way.



## Examples and counterexamples

By the [[Riesz duality theorem]], every [[separable space|separable]] [[Hilbert space]] is reflexive.

The [[Lebesgue space]] $l^1$ is reflexive in [[dream mathematics]], but in [[classical mathematics]] it is not.

In [[dream mathematics]] $l^\infty$ is reflexive; but its closed subspace $c_0$ is not. On the other hand, if one works in a setting where $\kappa_X$ is a monomorphism, then closed subspaces of reflexive Banach spaces are reflexive (see above)


James (1950) constructed a separable non-reflexive Banach space which is isomorphic as a TVS to its second dual; nowadays this is known as the __James space__ $J$. More is true: $\kappa_J(J)J$ is a codimension-$1$ subspace of $J^{**}$.

One can renorm $J$ to obtain a non-reflexive Banach space which is isometrically isomorphic as a Banach space to its second dual (James, 1951).

## References

* [MR0039915](http://www.ams.org/mathscinet-getitem?mr=39915) (12,616b)
 James, Robert C. Bases and reflexivity of Banach spaces.
[Ann. of Math. (2) 52, (1950). 518&#8211;527.](http://dx.doi.org/10.2307/1969430)

* [MR0044024](http://www.ams.org/mathscinet-getitem?mr=44024) (13,356d)
James, Robert C. A non-reflexive Banach space isometric with its second conjugate space.
Proc. Nat. Acad. Sci. U. S. A. 37, (1951). 174&#8211;177. 


* [MR0355536](http://www.ams.org/mathscinet-getitem?mr=0355536) (50 #8010)
Davis, W. J.; Figiel, T.; Johnson, W. B.; Pe&#322;czy&#324;ski, A.
Factoring weakly compact operators.
J. Functional Analysis 17 (1974), 311&#8211;327. 
 
[[!redirects reflexive Banach space]]
[[!redirects reflexive Banach spaces]]
