+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc} 

## Idea

The _Seiberg-Witten equations_ are [[partial differential equations]] for connections of principal U(1)-bundles and smooth sections of their spinor bundles. Their [[moduli space]] is used to define the [[Seiberg-Witten invariants]] capable to study smooth structures on [[4-manifolds]]. Since the [[gauge group]] of the Seiberg-Witten equations is abelian, many calculations could be simplified with new methods provided by them.

## Basics

Let $M$ be a [[compact]] [[orientable]] [[Riemannian manifold|Riemannian]] [[4-manifold]] with a [[Riemannian metric]] $g$ and [[spinᶜ structure]] $\mathfrak{s}$. Both always exist. In particular the latter is a lift of the [[classifying map]] $\tau\colon M\rightarrow BSO(4)$ of the [[tangent bundle]] $TM\cong\tau^*\gamma_\mathbb{R}^4$ to a map $\mathfrak{s}\colon M\rightarrow BSpin^\mathrm{c}(4)$. Because of the [[exceptional isomorphism]]:
$$
Spin^\mathrm{c}(4)
\cong U(2)\times_{U(1)}U(2)
=\{A^\pm\in U(2)|det(A^-)=det(A^+)\}
$$
the [[spinᶜ structure]] $\mathfrak{s}$ consists of two complex plane bundles $W^\pm\twoheadrightarrow M$, called _associated spinor bundles_, with same [[determinant line bundle]] $L=det(W^\pm)$. Since it preserves the first [[Chern class]] one has $c_1(L)=c_1(W^\pm)\in H^2(M,\mathbb{Z})$. Furthermore let $W=W^-\oplus W^+$ be the [[Whitney sum]] of the spinor bundles.

## Seiberg-Witten equations

[[covariant derivative|Covariant derivatives]] $\nabla\colon\Gamma^\infty(L)\rightarrow\Gamma^\infty(T^*M\otimes L)$ on the [[determinant line bundle]] $L$, which are [[linear map|linear]] and fulfill the [[Leibniz rule]], induce [[principal connections]] on the [[frame bundle]] $Fr_U(L)$, which is a principal U(1)-bundle, using the following [[isomorphisms]]:
$$
\Hom(\Gamma^\infty(L),\Gamma^\infty(T^*M\otimes L))
\cong\Gamma^\infty\underline{Hom}(L,T^*M\otimes L)
\cong\Gamma^\infty(T^*M\otimes L^*\otimes L)
\cong\Gamma^\infty(T^*M\otimes\underline{End}(L))
\cong\Omega^1(M,\underline{End}(L))
\cong\Omega^1(M,Ad Fr_U(L))
\cong\Omega_{Ad}^1(Fr_U(L),\mathfrak{u}(1))
$$
(In particular, since $L$ is a [[line bundle]], one has $\underline{End}(L)\cong\underline{\mathfrak{u}(1)}$, which can be seen with the fact that the [[identity]] provides a [[global section]].)

Since the first [[unitary group]] $U(1)$ is [[abelian group|abelian]], the Seiberg-Witten equations obtain a strong simplification compared to the [[Yang-Mills equations]], which are usually considered with non-abelian [[gauge groups]]. In particular this can be seen for the [[curvature form]] simplifying to $F_A=d A$. Its self-dual part is then given by:
$$
F_A^+
=\frac{1}{2}(F_A+\star F_A)
=\frac{1}{2}(d A+\star d A).
$$

Smooth sections of $W^-$, whose space is denoted $\Gamma^\infty(W^-)$ (or short $\Gamma(W^-)$), are called _antiselfdual spinor fields_ (or short _ASD spinor fields_). Smooth sections of $W^+$, whose space is denoted $\Gamma^\infty(W^+)$ (or short $\Gamma(W^+)$), are called _selfdual spinor fields_ (or short _SD spinor fields_). A connection like above induces a [[Dirac operator]] $D^A\colon\Gamma^\infty(W^+)\rightarrow\Gamma^\infty(W^-)$. Furthermore the Riemannian metric induces scalar products $\langle-,-\rangle\colon W^\pm\oplus W^\pm\rightarrow\underline{\mathbb{R}}$.

Now the Seiberg-Witten equations are [[partial differential equations]] for a connection $A\in\Omega^1(M,\mathfrak{u}(1))$ and a self-dual spinor field $\phi\in\Gamma^\infty(W^+)$, often given as _undisturbed Seiberg-Witten equations_ without and _disturbed Seiberg-Witten equations_ with a self-dual form $\eta\in\Omega_+^2(M,\mathfrak{u}(1))$ as:
$$
D^A\phi
=0;
$$
$$
F_A^+
+\tau(\phi)
+\eta
=0.
$$
Considering the undisturbed Seiberg-Witten equations with a vanishing spinor field $\phi=0$ yields the anti self-dual [[Yang-Mills equations]] (ASDYM equations) $F_A^+=0$.

## References

* {#Nicolaescu00} [[Liviu Nicolaescu]], *Notes on Seiberg-Witten theory*, American Mathematical Society (2000) &lbrack;[ISBN:978-0-8218-2145-9](https://bookstore.ams.org/GSM/28), [pdf](https://www3.nd.edu/~lnicolae/new1.pdf)&rbrack;

* Jürgen Einhorn, Thomas Friedrich, _Seiberg-Witten theory_ ([pdf](http://matwbn.icm.edu.pl/ksiazki/bcp/bcp39/bcp3925.pdf))

* [[Simon Donaldson]], _The Seiberg-Witten equations and 4-manifold topology_ ([pdf](http://www.ams.org/journals/bull/1996-33-01/S0273-0979-96-00625-8/S0273-0979-96-00625-8.pdf))

* [[Matilde Marcolli]], _Seiberg-Witten gauge theory_, [pdf](http://www.its.caltech.edu/~matilde/swcosi.pdf)

See also:

* Wikipedia, _[Seiberg-Witten equations](https://en.wikipedia.org/wiki/Seiberg%E2%80%93Witten_equations)_

[[!redirects Seiberg-Witten equation]]
[[!redirects Undisturbed Seiberg-Witten equation]]
[[!redirects Undisturbed Seiberg-Witten equations]]
[[!redirects undisturbed Seiberg-Witten equation]]
[[!redirects undisturbed Seiberg-Witten equations]]
[[!redirects Disturbed Seiberg-Witten equation]]
[[!redirects Disturbed Seiberg-Witten equations]]
[[!redirects disturbed Seiberg-Witten equation]]
[[!redirects disturbed Seiberg-Witten equations]]