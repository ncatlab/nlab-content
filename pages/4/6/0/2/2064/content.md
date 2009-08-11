## Idea

A __fibre bundle__ or __fiber bundle__ is a [[bundle]] in which every [[fibre]] is [[isomorphism|isomorphic]], in some coherent way, to a __standard fibre__.


## Definitions

In the most general sense, a __bundle__ over an object $B$ in a [[category]] $C$ is a [[morphism]] $p: E \to B$ in $C$.

In an appropriate contexts, a __fibre bundle__ over $B$ with standard fibre $F$ may be defined as a bundle over $B$ such that, given any [[global element]] $x: 1 \to B$, the [[pullback]] of $E$ along $x$ is isomorphic to $F$.  Certainly this definition is appropriate whenever $C$ has a [[terminal object]] $1$ which is a [[generator]], as in a [[well-pointed category]]; even then, however, one often wants the more restrictive notion below.

One often writes a typical fibre bundle in shorthand as $F \to E \to B$ or
$$ \array {
   F & \rightarrow & E \\
     &             & \downarrow \\
     &             & B
} $$
even though there is not a single morphism $F \to E$ but instead one for each global element $x$ (and none at all if $B$ has no global elements!).

If $C$ is a [[site]], then a __locally trivial fibre bundle__ over $B$ with standard fibre $F$ is a bundle over $B$ with a [[cover]] $(j_\alpha: U_\alpha \to B)_\alpha$ such that, for each index $\alpha$, the pullback $E_\alpha$ of $E$ along $j_\alpha$ is isomorphic in the [[slice category]] $C/{U_\alpha}$ to the [[trivial bundle]] $U_\alpha \times F$.

One can also drop $F$ and define a slightly more general notion of __locally trivial bundle__ over $B$ as a bundle over $B$ with a cover $(j_\alpha: U_\alpha \to B)_\alpha$ such that, for each index $\alpha$, there is a fibre $F_\alpha$ and an isomorphism in $C/{U_\alpha}$ between the pullback $E_\alpha$ and the trivial bundle $U_\alpha \times F_\alpha$.  Every locally trivial fibre bundle is obviously a locally trivial bundle; the converse holds if $B$ is [[connected object|connected]].

Now suppose that $E$ is a fibre bundle over $B$ with standard fibre $F$, locally trivialised using the cover $(U_\alpha)_\alpha$.  Given an index $\alpha$ and an index $\beta$, let $U_{\alpha,\beta}$ be the [[fibred product]] (pullback) of $U_\alpha$ and $U_\beta$.  Then we have an [[automorphism]] $g_{\alpha,\beta}$ of $U_{\alpha,\beta} \times F$ in $C/{U_{\alpha,\beta}}$ as follows:
(diagram to come)
The $g_{\alpha,\beta}$ are the __transition morphisms__ of the locally trivial fibre bundle $E$.

Often one considers special kinds of bundles, by requiring structure on the standard fibre $F$ and/or conditions on the transition morphisms $g_{\alpha,\beta}$.  For example:
*  If $G$ is a [[group object]] in $C$ that [[action|acts]] on $F$, then a __$G$-bundle__ over $B$ with standard fibre $F$ is a locally trivial fibre bundle over $B$ with standard fibre $F$ together with morphisms $U_{\alpha,\beta} \to G$ that, relative to the aciton of $G$ on $F$, give the transition maps $g_{\alpha,\beta}$.  (The morphism $U_{\alpha,\beta} \to G$ is also written $g_{\alpha,\beta}$, conflating action with application.)
*  More specifically, a (right or left) __[[principal bundle|principal]] $G$-bundle__ over $B$ is a $G$-bundle over $B$ with standard fibre $G$, associated with the action of $G$ on itself by (right or left) multiplication.
*  If $F$ is an object of a [[concrete category]] over $C$, then we can consider locally trivial fibre bundles with standard fibre $F$ such that the transition morphisms are structure-preserving morphisms.  If the [[automorphism group]] $Aut(F)$ can be internalised in $C$, then this the same as an $Aut(F)$-bundle, but the concept makes sense in any case.
*  As a fairly specific example, if $F$ is a [[topological vector space]] (and $C$ is a category with structure to support this, such as [[Top]] or [[Diff]]), then a __[[vector bundle]]__ over $B$ with standard fibre $F$ is a $GL(F)$-bundle over $B$ with standard fibre $F$, where $GL(F)$ is the [[general linear group]] with its defining action on $F$.


[[!redirects fibre bundle]]
[[!redirects standard fiber]]
[[!redirects standard fibre]]
[[!redirects locally trivial fiber bundle]]
[[!redirects locally trivial fibre bundle]]
[[!redirects locally trivial bundle]]
[[!redirects transition morphism]]
[[!redirects transition map]]
[[!redirects transition function]]
[[!redirects G-bundle]]
[[!redirects fiber bundles]]
[[!redirects fibre bundles]]
[[!redirects standard fibers]]
[[!redirects standard fibres]]
[[!redirects locally trivial fiber bundles]]
[[!redirects locally trivial fibre bundles]]
[[!redirects locally trivial bundles]]
[[!redirects transition morphisms]]
[[!redirects transition maps]]
[[!redirects transition functions]]
[[!redirects G-bundles]]