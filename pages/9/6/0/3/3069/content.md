
#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The **Beck--Chevalley condition**, also sometimes called just the *Beck condition* or the *Chevalley condition*, is a "commutation of [[adjoint functor|adjoint]]s" property that holds in many "[[base change|change of base]]" situations.


## Definition

Suppose given a [[commutative square]] (up to [[isomorphism]]) of [[functor]]s:
$$\array{ & \overset{f^*}{\to} & \\
  ^{g^*}\downarrow && \downarrow^{k^*}\\
  & \underset{h^*}{\to} & }$$
in which $f^*$ and $h^*$ have [[left adjoint]]s $f_!$ and $h_!$, respectively.  Then the [[natural isomorphism]] that makes the square commute has a [[mate]]
$$ h_! k^* \to g^* f_! $$
defined as the composite
$$ h_! k^* \overset{\eta}{\to} h_! k^* f^* f_! \overset{\cong}{\to} h_! h^* g^* f_! \overset{\epsilon}{\to} g^* f_! .$$

We say the original square satisfies the **Beck--Chevalley condition** if this mate is an [[isomorphism]].

### Left and right Beck--Chevalley condition

Of course, if $g^*$ and $k^*$ also have [[left adjoint]]s, there is also a Beck--Chevalley condition stating that the corresponding mate $k_! h^* \to f^* g_!$ is an isomorphism, and this is not equivalent in general.  Context is usually sufficient to disambiguate, although some people speak of the "left" and "right" Beck--Chevalley conditions.

### Dual Beck--Chevalley condition

If $f^*$ and $h^*$ have *right* adjoints $f_*$ and $h_*$, there is also a dual Beck--Chevalley condition saying that the mate $g^* f_* \to h_* k^*$ is an isomorphism.  By general nonsense, if $f^*$ and $h^*$ have right adjoints and $g^*$ and $k^*$ have left adjoints, then $g^* f_* \to h_* k^*$ is an isomorphism if and only if $k_! h^* \to f^* g_!$ is.

## Bifibrations

A common situation in which this occurs is when we have a [[bifibration]], with the functors $f^*$, $g^*$, etc. being the "pullback" functors coming from the cartesian liftings of a commutative square
$$\array{ & \overset{f}{\leftarrow} & \\
  ^g\uparrow && \uparrow^k\\
  & \underset{h}{\leftarrow} & }$$
in the base category.  In this case one also says that this commutative square "downstairs" has the Beck--Chevalley property.  Frequently this property holds for all [[pullback]] squares in the base category.  Note that since the transpose of a pullback square is a pullback square, in this case there is no left/right ambiguity.

According to the [[Benabou–Roubaud theorem]], the Beck--Chevalley condition  is crucial for establishing the connection between the descent in the sense of fibered categories and the [[monadic descent]].

### Examples

* The [[codomain fibration]] of any [[category]] with [[pullbacks]] is a bifibration, and satisfies the Beck--Chevalley condition at every pullback square.

* If $C$ is a [[regular category]] (such as a [[topos]]), the bifibration $Sub(C) \to C$ of [[subobjects]] satisfies the Beck--Chevalley condition at every pullback square.

* The [[family fibration]] $Fam(C)\to Set$ of any category $C$ satisfies the Beck--Chevalley condition at every pullback square in $Set$.


## References

* See Mac Lane and Moerdijk, section IV.9 (page 205).


[[!redirects Beck-Chevalley_Condition]]
[[!redirects Beck-Chevalley Condition]]
[[!redirects Beck–Chevalley condition]]
[[!redirects Beck--Chevalley condition]]
[[!redirects Beck condition]]
[[!redirects Chevalley condition]]
[[!redirects Beck-Chevalley property]]
[[!redirects Beck–Chevalley property]]
[[!redirects Beck--Chevalley property]]