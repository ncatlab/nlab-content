
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Frame and coframe bundles
* table of contents
{: toc}

## Definition

### Traditional

Given a $k$-[[vector bundle]] $p\colon E \to M$ of finite [[rank]] $n$, its __frame bundle__ (or bundle of [[frame of a vector space|frames]] in $E \to M$) is the bundle $F E \to M$ over the same base whose [[fiber]] over $x \in M$ is the set of all vector space [[basis|bases]] of $E_x = p^{-1}(x)$. The frame bundle has a natural action of $GL_n(k)$ given by an ordered change of basis which is free and transitive, i. e., the frame bundle is a [[principal bundle|principal]] $GL_n(k)$-bundle. 

The __frame bundle of a [[manifold]]__ $M$ is the [[principal bundle]] $F T M \to M$ (also denoted $F M \to M$) of frames in the [[tangent bundle]] $T M$. 

In the finite-dimensional case, the dual $GL_n$-principal bundle $(F T)^* M$ is the __coframe bundle__ of the manifold. This means that $F^* M = (F T)^* M$ is the associated bundle to $F T M \times_{GL_n(k)}GL_n(k)$ where the left action of $GL_n(k)$ on $GL_n(k)$ is given by right multiplication by inverses $g. h = h\cdot g^{-1}$. Also $F T M\cong (F T)^* M\times_{GL_n(k)} GL_n(k)$ using the same formula. Furthermore, the right action of $GL_n(k)$ on this associated bundle is given by left multiplication by inverses on $GL_n(k)$ factor. 

Coframe bundle $F^* M$ has the following independent description. One looks at the set $\mathcal{U}(M)$ of tuples of the form $(p,(U,h))$ where $p\in U$ and $(U,h)$ is chart of the smooth structure on $M$, $U\subset M$, $h : U\to \mathbf{R}^n$ (an atlas where $U$-s make a basis of topology suffices). $GL_n(k)$ acts on the right on $\mathcal{U}(M)$ by 

$$
(p, (U, h)) A := (p, (U, A^{-1} h)).
$$
Then $((p,(U,h))A)A' = (p,(U,h)) (AA')$ holds. 
The total space $F^* M$ of the coframe bundle by the definition, as a set, consists of classes of equivalence of tuples in $\mathcal{U}(M)$ where $(p,(U,h)) \sim (p',(U',h'))$ iff $p = p'$ and the [[Jacobian matrix]] of the transition between charts at $h'(p)$ is the unit matrix: $J_{h'(p)}(h\circ (h')^{-1}) = I$. The left action of $GL_n(k)$ is induced on the quotient. There is an obvious projection $\pi: [(p,(U,h)]\mapsto p$. To define the differential and principal bundle structure one charts $F^* M\to M$ with local trivializations from the neighborhoods of the form $U\times GL_n(k)$, transfers the structure and checks that the transition functions are of the appropriate smoothness class and right $GL_n(k)$-equivariant. The basic prescription is that to every chart $(U,h)$ one defines a map

$$
\phi_{h} = \pi^{-1}(U)\to U \times GL_n(k),\,\,\,\,\,\,z\mapsto (\pi(z), J_{h(\pi(z))}(h'\circ h^{-1})),
$$
where $z = [(\pi(z), (U',h'))]$ with $\pi(z)\in U'\cap U$. This does not depend on the choice of the chart $(U',h')$ around $\pi(z)$. There is an equivariance 
$$
J_{h(\pi(z A))}(h'\circ h^{-1})) = A^{-1} J_{h(\pi(z))}(h'\circ h^{-1}))
$$
and on intersection of $(U,h)$ and $(V,g)$
$$
J_{h(\pi(z))}(h'\circ h^{-1})) = J_{g(\pi(z))}(h'\circ g^{-1})J_{h(\pi(z))}(g\circ h^{-1})
$$
Then $\phi_h$ is onto and 

$$
(\phi_h \circ (\phi_g)^{-1})(p,A) = (p, A J_{h(p)}(g\circ h^{-1})
$$

what shows that the transition functions are smooth (where $GL_n(k)$ has the standard differential structure). 

### In differential cohesion
 {#InDifferentialCohesion}

In a context of [[differential cohesion]], then the frame bundle (or [[higher order frame bundle]]) of a $V$-[[manifold]] is the [[principal bundle]] ([[principal infinity-bundle]]) to which the [[infinitesimal disk bundle]] is the canonically [[associated bundle]] ([[associated infinity-bundle]])

See at _[differential cohesion -- Frame bundles](differential+cohesion#GLnTangentBundles)_.

## Properties

### The canonical differential 1-form
 {#TheCanonical1Form}

The frame bundle $Fr(X)$ carries a canonical [[differential 1-form]] with values in $\mathbb{R}^n$.

$$
  \alpha \in \Omega^1(Fr(X), \mathbb{R}^n)
$$

This is defined as follows. Let $p \in Fr(X)$ be a point in the frame bundle $\pi \colon Fr(X)\to X$ over some point $x \in X$, hence a linear isomorphism $p \colon T_x \simeq \mathbb{R}^n$. For $v \in T_p Fr(X)$ a [[tangent vector]] to the frame bundle, its projection $\pi_\ast v \in T_x X$ is a [[tangent vector]] to $X$. Then the value of $\alpha$ on $v$ is the image of this $\pi_\ast(v)$ under the isomorphism $p$

$$
  \alpha(v) \coloneqq p(\pi_\ast(v))
  \,.
$$

([Sternberg 64, section VII, (2.2)](#Sternberg64))

### Relation to $G$-structures

A choice sub-bundle of a frame bundle which is a $G$-[[principal bundle]] for $G\hookrightarrow GL(n)$ defines a _[[G-structure]]_. See there for more.

## Related concepts

* a [[section]] of a frame bundle is also called a _[[frame field]]_.

* [[higher order frame bundle]] ([[jet bundle]]-version)

## References

* Wikipedia (English) [frame bundle](http://en.wikipedia.org/wiki/Frame_bundle)

* {#Sternberg64} [[Shlomo Sternberg]], _Lectures on differential geometry_, Prentice Hall 1964; Russian transl. Mir 1970


[[!redirects coframe bundle]]
[[!redirects frame bundles]]