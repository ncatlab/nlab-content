
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Definition

A [[Banach space]] $X$ is **reflexive** if the canonical map $X \to (X^*)^*$ from $X$ to its second dual is an [[isomorphism]] (it is always an [[isometry]] in the presence of [[axiom of choice|Choice]], by the [[Hahn–Banach theorem]]).


## Properties

(...)

Note that if two [[Banach space]]s are isomorphic as TVSes (but not necessarily isometrically isomorphic), then either both are reflexive or both are non-reflexive.

There is a nice proof that closed subspaces of reflexive [[Banach space]]s are reflexive (due to Linton? need to find citation) using naturality of the map $X\to X^{**}$.

It turns out that if $X$ is a [[Banach space]], then it is reflexive if and only if its (norm-)closed unit ball is compact in the $\sigma(X,X^*)$-topology. In particular, if $X$ is reflexive and $E\to X$, $X\to F$ are bounded linear operators, then the composition $E\to F$ is [[weakly compact]] as a linear operator.

A theorem of Davis-Figiel-Johnson-Pelczynski (1974) tells us that the converse is true:  every [[weakly compact]] linear operator between Banach spaces factors through some reflexive Banach space. The intermediate space is constructed by real interpolation and (at least as usually presented) does not seem to be canonical in any way.



## Examples and counterexamples

By the [[Riesz duality theorem]], every [[separable space|separable]] [[Hilbert space]] is reflexive.

The [[Lebesgue space]] $l^1$ is reflexive in [[dream mathematics]], but in [[classical mathematics]] it is not.

James (1950) constructed a separable non-reflexive Banach space which is isomorphic as a TVS to its second dual; nowadays this is known as the __James space__ $J$. More is true: the image of $J$ in $J^{**}$ under the canonical map turns out to have codimension $1$ in $J^{**}$.

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
