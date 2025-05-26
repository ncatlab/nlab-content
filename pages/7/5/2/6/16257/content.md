
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

One usually defines [[cohomology]] with respect to some [[coefficient]] objects:

* For [[group cohomology]] of a [[group]] $G$, the coefficients come from a (left) $G$-[[module]].
* For [[Lie algebra cohomology]] of a [[Lie algebra]] $\mathfrak{g}$, the coefficients come from a (left) $\mathfrak{g}$-module.
* For [[Hochschild cohomology]] of an [[associative algebra]] $A$, the coefficients come from an $A$-[[bimodule]].

**Beck modules** are a simultaneous generalisation of all three types of module.

## Definition

Let $\mathcal{C}$ be a [[category]] with [[pullback]]s and let $A$ be an object in $\mathcal{C}$. A **Beck module** over $A$ is an [[abelian group object]] in the slice category $\mathcal{C}_{/ A}$. In particular, if $A$ is the terminal object, this reduces to the notion of an abelian group object in $\mathcal{C}$. We write $\mathbf{Ab}(\mathcal{C}_{/ A})$ for the category of Beck modules over $A$.

([Beck 67, def. 5](#Beck67))

## Properties

+-- {: .num_prop}
###### Proposition

Let $\mathcal{C}$ be an [[effective regular category]] (resp. [[locally presentable category]]) and let $A$ be an object in $\mathcal{C}$. Then $\mathbf{Ab}(\mathcal{C}_{/ A})$ is an [[abelian category]] (resp. locally presentable category).

=--

+-- {: .proof}
###### Proof

If $\mathcal{C}$ is a effective regular category (resp. locally presentable category), then so is $\mathcal{C}_{/ A}$. Thus, the claim reduces to the fact that the category of abelian group objects in an effective regular category (resp. locally presentable category) is an abelian category (resp. locally presentable category).

=--

+-- {: .num_prop}
###### Proposition

Let $\mathcal{C}$ be an effective regular category with [[filtered colimits]] and let $A$ be an object in $\mathcal{C}$. If filtered colimits in $\mathcal{C}$ preserve finite [[limits]], then $\mathbf{Ab}(\mathcal{C}_{/ A})$ (is an abelian category and) satisfies axiom AB5.

=--

+-- {: .proof}
###### Proof

The forgetful functor $\mathcal{C}_{/ A} \to \mathcal{C}$ [[created limit|creates]] pullbacks and filtered colimits, so filtered colimits in $\mathcal{C}_{/ A}$ also preserve finite limits. The forgetful functor $\mathbf{Ab}(\mathcal{C}_{/ A}) \to \mathcal{C}_{/ A}$ creates limits and filtered colimits, so filtered colimits in $\mathbf{Ab}(\mathcal{C}_{/ A})$ preserve kernels. In view of the earlier proposition, it follows that $\mathbf{Ab}(\mathcal{C}_{/ A})$ satisfies axiom AB5.

=--

+-- {: .num_cor}
###### Corollary

Let $\mathcal{C}$ be a locally finitely presentable effective regular category and let $A$ be an object in $\mathcal{C}$. Then $\mathbf{Ab}(\mathcal{C}_{/ A})$ is a [[Grothendieck category]].

=--

+-- {: .proof}
###### Proof

Combine the two propositions above.

=--

## Derivations

Let $\mathcal{C}$ be a category with pullbacks, let $A$ be an object in $\mathcal{C}$, and let $U : \mathbf{Ab}(\mathcal{C}_{/ A}) \to \mathcal{C}_{/ A}$ be the forgetful functor. Given a Beck module $M$ over $A$, an $M$-valued **derivation** of $A$ is a morphism $1_A \to U M$ in $\mathcal{C}_{/ A}$, where $1_A$ is the terminal object in $\mathcal{C}_{/ A}$, and we write
$$Der (A, M) = \mathcal{C}_{/ A} (1_A, U M)$$
for the set of $M$-valued derivations of $A$. The **Beck module of differentials** over $A$ is an object $\Omega_A$ in $\mathbf{Ab}(\mathcal{C}_{/ A})$ [[representable functor|representing]] the functor $Der (A, -) : \mathbf{Ab}(\mathcal{C}_{/ A}) \to \mathbf{Set}$.

The Beck module $\Omega_A$ is not guaranteed to exist in general. When the functor $U : \mathbf{Ab}(\mathcal{C}_{/ A}) \to \mathcal{C}_{/ A}$ has a left adjoint, $\Omega_A$ is simply the value of the left adjoint at $1_A$.

+-- {: .num_prop}
###### Proposition

Let $\mathcal{C}$ be a locally presentable category and let $A$ be an object in $\mathcal{C}$. Then the forgetful functor $U : \mathbf{Ab}(\mathcal{C}_{/ A}) \to \mathcal{C}_{/ A}$ has a left adjoint.

=--

+-- {: .proof}
###### Proof

The forgetful functor $\mathbf{Ab}(\mathcal{C}_{/ A}) \to \mathcal{C}_{/ A}$ creates limits and $\kappa$-filtered colimits (for some $\kappa$ large enough), so we may apply the accessible [[adjoint functor theorem]].

=--

## Examples

### Beck modules over associative algebras
 {#OverAssociativeAlgebras}

+-- {: .num_prop}
###### Proposition

Let $\mathcal{C}$ be the category of (not necessarily [[commutative ring|commutative]]) [[rings]] and let $A$ be a ring. Then $\mathbf{Ab}(\mathcal{C}_{/ A})$ is equivalent to the [[category]] [[Bimod]] of $A$-[[bimodules]].

=--

+-- {: .proof}
###### Proof

Let $\epsilon : B \to A$ be ring homomorphism. To give it the structure of a Beck module over $A$, we must give ring homomorphisms $\eta : A \to B$ and $\mu : B \times_A B \to B$ such that $\epsilon \circ \eta = id_A$, $\epsilon (\mu (b_0, b_1)) = \epsilon (b_0) = \epsilon (b_1)$, as well as various other equations. Given elements $b_0, b_1, b_2, b_3$ of $B$ such that $\epsilon (b_0) = \epsilon (b_2)$ and $\epsilon (b_1) = \epsilon (b_3)$, we have the following interchange law:
$$\mu (b_0 + b_1, b_2 + b_3) = \mu (b_0, b_2) + \mu (b_1, b_3)$$
Hence, if $a = \epsilon (b_1) = \epsilon (b_2)$,
$$\mu (b_1, b_2) = \mu (\eta (a) + b_1 - \eta (a), \eta (a) + b_2 - \eta (a)) = \mu (\eta (a), \eta (a)) + \mu (b_1 - \eta(a), b_2 - \eta (a)) = \eta (a) + \mu (b_1 - \eta(a), b_2 - \eta (a))$$
but $\epsilon (b_1 - \eta (a)) = \epsilon (b_2 - \eta (a)) = 0$, so
$$\mu (b_1 - \eta(a), b_2 - \eta(a)) = \mu (0, b_2 - \eta (a)) + \mu (b_1 - \eta (a), 0) = b_2 - \eta (a) + b_1 - \eta (a)$$
and we conclude that
$$\mu (b_1, b_2) = b_1 - \eta (\epsilon (b_1)) + b_2 = b_1 + b_2 - \eta (\epsilon (b_2))$$
and in particular, $\mu$ is entirely determined by $\eta$ and $\epsilon$. We also have the following interchange law,
$$\mu (b_0 b_1, b_2 b_3) = \mu (b_0, b_2) \mu (b_1, b_3)$$
and in particular,
$$\mu (\eta (\epsilon (b_2)) b_1, b_2 \eta (\epsilon (b_1))) = \mu (\eta (\epsilon (b_2)), b_2) \mu (b_1, \eta (\epsilon (b_1))) = b_2 b_1$$
hence,
$$b_2 b_1 = \eta (\epsilon (b_2)) b_1 - \eta (\epsilon (b_2 b_1)) + b_2 \eta (\epsilon (b_1))$$
so if $\epsilon (b_1) = \epsilon (b_2) = 0$, then $b_2 b_1 = 0$.

Let $M = \ker \epsilon$. The above shows that the internal abelian group structure on $B$ restricts to the pre-existing abelian group structure on $\ker \epsilon$. In addition, the homomorphism $\eta : A \to B$ gives $M$ the structure of an $A$-bimodule, and we see that $B$ is naturally isomorphic to the [[square-0 extension]] ring $A \oplus M$, with componentwise addition and the multiplication given below,
$$(a_0, m_0) \cdot (a_1, m_1) = (a_0 a_1, a_0 m_1 + m_0 a_1)$$
regarded as a Beck module over $A$ by defining $\epsilon : A \oplus M \to A$, $\eta : A \to A \oplus M$, and $\mu : (A \oplus M) \times_A (A \oplus M) \to A \oplus M$ as follows:
$$\epsilon (a, m) = a$$
$$\eta (a) = (a, 0)$$
$$\mu ((a, m_0), (a, m_1)) = (a, m_0 + m_1)$$
Thus, we have an equivalence between $\mathbf{Ab}(\mathcal{C}_{/ A})$ and the category of $A$-bimodules, as claimed.

=--

+-- {: .num_prop}
###### Proposition

Let $A$ be a ring. Then the Beck module $\Omega_A$ is isomorphic to the $A$-bimodule of [[Kähler differentials]] (relative to $\mathbb{Z}$).

=--

+-- {: .proof}
###### Proof

Let $M$ be an $A$-bimodule, regard $A \oplus M$ as a ring as above, and let $\epsilon : A \oplus M \to A$ be the obvious projection. A ring homomorphism $\phi : A \to A \oplus M$ satisfying $\epsilon \circ \phi = id_A$ is the same thing as an additive homomorphism $\delta : A \to M$ satisfying the following equations,
$$\delta (a_0 a_1) = \delta (a_0) a_1 + a_0 \delta (a_1)$$
i.e. a derivation $A \to M$ (over $\mathbb{Z}$). Thus, the Beck module $\Omega_A$ has the same universal property as the $A$-bimodule of K&#228;hler differentials.

=--


### Beck modules over C^∞-rings

The above proof also shows that Beck modules over [[C^∞-rings]] coincide with ordinary modules, once we recall that [[ideals]] of [[C^∞-rings]] coincide with ordinary ideals and the square zero extension constructed above is a [[C^∞-ring]] via [[Taylor expansion]].

Beck derivations of [[C^∞-rings]] then coincide with [[C^∞-derivations]], which is also shown using the above proof, but replacing the main displayed formula with
$$\delta (f(a_1, \ldots, a_n)) = \sum_i {\partial f\over \partial x_i}(a_1,\ldots,a_n)\delta (a_i).$$

### Beck modules over groups

+-- {: .num_prop}
###### Proposition

Let $\mathcal{C}$ be the category of (not necessarily abelian) [[groups]] and let $G$ be a group. Then $\mathbf{Ab}(\mathcal{C}_{/ G})$ is equivalent to the category of left $G$-modules.

=--

+-- {: .proof}
###### Proof

Let $\epsilon : H \to G$ be group homomorphism. To give it the structure of a Beck module over $G$, we must give group homomorphisms $\eta : G \to H$ and $\mu : H \times_G H \to H$ such that $\epsilon \circ \eta = id_G$, $\epsilon (\mu (h_0, h_1)) = \epsilon (h_0) = \epsilon (h_1)$, as well as various other equations. Given elements $h_0, h_1, h_2, h_3$ of $H$ such that $\epsilon (h_0) = \epsilon (h_2)$ and $\epsilon (h_1) = \epsilon (h_3)$, we have the following interchange law:
$$\mu (h_0 h_1, h_2 h_3) = \mu (h_0, h_2) \mu (h_1, h_3)$$
and in particular,
$$\mu (\eta (\epsilon (h_2)) h_1, h_2 \eta (\epsilon (h_1))) = \mu (\eta (\epsilon (h_2)), h_2) \mu (h_1, \eta (\epsilon (h_1))) = h_2 h_1$$
but on the other hand, if $g = \epsilon (h_1) = \epsilon (h_2)$, then
$$\mu (h_1, h_2) = \mu (\eta (g) \eta (g)^{-1} h_1, \eta (g) \eta (g)^{-1} h_2) = \mu (\eta (g), \eta (g)) \mu (\eta (g)^{-1} h_1, \eta (g)^{-1} h_2) = \eta (g) \mu (\eta (g)^{-1} h_1, \eta (g)^{-1} h_2)$$
and writing $e$ for the unit of $G$ and $H$, we have $\epsilon (\eta (g)^{-1} h_1) = \epsilon (\eta (g)^{-1} h_2) = e$, hence
$$\mu (\eta (g)^{-1} h_1, \eta (g)^{-1} h_2) = \mu (e, \eta (g)^{-1} h_2) \mu (\eta (g)^{-1} h_1, e) = \eta (g)^{-1} h_2 \eta (g)^{-1} h_1$$
so we conclude that
$$\mu (h_1, h_2) = h_2 \eta (g)^{-1} h_1$$
and in particular, $\mu$ is entirely determined by $\eta$.

Let $M = \ker \epsilon$. The above shows that the internal abelian group structure on $B$ restricts to the pre-existing group structure on $\ker \epsilon$. (In particular, $M$ is an abelian group!) We make $M$ into a left $G$-module as follows:
$$g \cdot m = \eta (g) m \eta (g)^{-1}$$
We can then construct the [[semi-direct product]] $M \rtimes G$, which has the following multplication:
$$(m_0, g_0) \cdot (m_1, g_1) = (m_0 \eta (g_0) m_1 \eta (g_0)^{-1}, g_0 g_1)$$
There is a group homomorphism $M \rtimes G \to H$ defined by $(m, g) \mapsto m \eta (g)$, and it is bijective: surjectivity is clear, and injectivity is a consequence of the fact that $M \cap \operatorname{im} \eta = \{ e \}$. We may regard $M \rtimes G$ as a Beck module over $G$ by defining $\epsilon : M \rtimes G \to G$, $\eta : G \to M \rtimes G$, and $\mu : (M \rtimes G) \times_G (M \rtimes G) \to M \rtimes G$ as follows:
$$\epsilon (m, g) = g$$
$$\eta (g) = (0, g)$$
$$\mu ((m_0, g), (m_1, g)) = (m_1 m_0, g)$$
Thus, we have an equivalence between $\mathbf{Ab}(\mathcal{C}_{/ G})$ and the category of left $G$-modules, as claimed.

=--

+-- {: .num_prop}
###### Proposition

Let $G$ be a group and let $M$ be a left $G$-module. Under the above identification of Beck modules over $G$ with left $G$-modules, $M$-valued derivations of $G$ are precisely crossed homomorphisms $G \to M$, i.e. maps $\delta : G \to M$ satisfying the following equation:
$$\delta (g_0 g_1) = \delta (g_0) + g_0 \cdot \delta (g_1)$$

=--

+-- {: .proof}
###### Proof

Let $\epsilon : M \rtimes G \to G$ be the evident projection. A group homomorphism $\phi : G \to M \rtimes G$ such that $\epsilon \circ \phi = id_G$ is the same thing as a map $\delta : G \to M$ satisfying the equation below,
$$(\delta (g_0), g_0) \cdot (\delta (g_1), g_1) = (\delta (g_0 g_1), g_0 g_1)$$
which is equivalent to the defining equation for crossed homomorphisms.

=--

## The tangent category

One may assemble the individual categories of Beck modules over the objects of $\mathcal{C}$ into a category fibred over $\mathcal{C}$, called the [[tangent category]].

## References

The concept is due to

* {#Beck67} [[Jon Beck]], _Triples, algebras and cohomology_, Ph.D. thesis, Columbia University, 1967, Reprints in Theory and Applications of Categories, No. 2 (2003) pp 1-59 ([TAC](http://www.tac.mta.ca/tac/reprints/articles/2/tr2abs.html))

and was popularized in

* {#Quillen70} [[Daniel G. Quillen]], _On the (co-)homology of commutative rings_, in Proc. Symp. on Categorical Algebra, 65 &#8211; 87, American Math. Soc.,  1970.

See also

* [[Michael Barr]], _Acyclic models_, Chapter 6, &#167;1.

An application to [[knot theory]] is given in

* [[Markus Szymik]], _Alexander-Beck modules detect the unknot_, Fund. Math. 246 (2019) 89-108.

[[!redirects Beck modules]]