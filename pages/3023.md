
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

A Riemann surface is a $1$-dimensional [[algebraic geometry|algebro-geometric]] object with good properties.  The name 'surface' comes from the classical case, which is $1$-dimensional over the [[complex numbers]] and therefore $2$-dimensional over the [[real numbers]].

There are several distinct meaning of what is a Riemann surface, and it can be considered in several generalities.


## Definition

Classically, a **Riemann surface** is a [[connected space|connected]] complex-$1$-dimensional [[complex manifold]], in the strictest sense of 'manifold'.  In other words, it's a [[Hausdorff space|Hausdorff]] [[second countable space]] $M$ which is locally [[homeomorphism|homeomorphic]] to the [[complex plane]] $\mathbb{C}$ via charts (i.e., [[homeomorphisms]]) $\phi_i:U_i \to V_i$ for $U_i \subset M, V_i \subset \mathbb{C}$ open and such that $\phi_j \circ \phi_i^{-1}: V_i \cap V_j \to V_i \cap V_j$ is [[holomorphic function|holomorphic]].

There are generalizations e.g. over [[local field]]s in [[rigid analytic geometry]]. 


## Examples

Evidently an [[open subspace]] of a Riemann surface is a Riemann surface.  In particular, an open subset of $\mathbb{C}$ is a Riemann surface in a natural manner.

The [[Riemann sphere]] $P^1(\mathbb{C}) := \mathbb{C} \cup \{ \infty \}$ or $S^2$ is a Riemann surface with the open sets $U_1 = \mathbb{C}, U_2 = \mathbb{C} - \{0\} \cup \{\infty\}$ and the charts
\[ \phi_1 =z, \;\phi_2 = \frac{1}{z}.\]
The transition map is $\frac{1}{z}$ and thus holomorphic on $U_1 \cap U_2 = \mathbb{C}^*$.

An important example comes from [[analytic continuation]], which we will briefly sketch below.   A **function element** is a pair $(f,V)$ where $f: V \to \mathbb{C}$ is holomorphic and $V \subset \mathbb{C}$ is an open disk.
Two function elements $(f,V), (g,W)$ are said to be **direct analytic continuations** of each other if $V \cap W \neq \emptyset$ and $f \equiv g $ on $V \cap W$.  By piecing together direct analytic continuations on a curve, we can talk about the analytic continuation of a function element along a curve (which may or may not exist, but if it does, it is unique).

Starting with a given function element $\gamma = (f,V)$, we can consider the totality $X$ of all equivalence classes of function elements that can be obtained by continuing $\gamma$ along curves in $\mathbb{C}$.  Then $X$ is actually a Riemann surface.

Indeed, we must first put a topology on $X$.  If $(g,W) \in X$ with $W=D_r(w_0)$ centered at $w_0$, then let a neighborhood of $g$ be given by all function elements $(g_w, W')$ for $w \in W, W' \subset W$; these form a basis for a suitable topology on $X$.  Then the coordinate projections $(g,W) \to w_0$ form appropriate local coordinates.  In fact, there is a globally defined map $X \to \mathbb{C}$, whose image in general will be a proper subset of $\mathbb{C}$.

## Properties

### Basic facts

Since we have local coordinates, we can define a map $f: X \to Y$ of Riemann surfaces to be **holomorphic** or **regular** if it is so in local coordinates.  In particular, we can define a holomorphic complex function as a holomorphic map $f: X \to \mathbb{C}$; for [[meromorphic function|meromorphicity]], this becomes $f: X \to S^2$.

Many of the usual theorems of elementary [[complex analysis]] (that is to say, the local ones) transfer immediately to the case of Riemann surfaces.  For instance, we can locally get a [[Laurent series|Laurent expansion]], etc.

+-- {: .num_theorem}
###### Theorem

Let $f: X \to Y$ be a regular map.  If $X$ is compact and $f$ is nonconstant, then $f$ is surjective and $Y$ compact.

=--


To see this, note that $f(X)$ is [[compact space|compact]], and an open subset by the [[open mapping theorem]], so the result follows by connectedness of $Y$.


### Complexified differentials

Since a Riemann surface $X$ is a $2$-dimensional [[smooth manifold]] in the usual (real) sense, it is possible to do the usual [[differential form|exterior calculus]].  We could consider a 1-form to be a section of the (usual) [[cotangent bundle]] $T^*(X)$, but it is more natural to take the **complexified cotangent bundle** $\mathbb{C} \otimes_{\mathbb{R}} T^*(X)$, which we will in the future just abbreviate $T^*(X)$; this should not be confusing since we will only do this when we talk about complex manifolds.  Sections of this bundle will be called (complex-valued) 1-forms.  Similarly, we do the same for 2-forms.  

If $z = x + i y$ is  a local coordinate on $X$, defined say on $U \subset X$, define the (complex) differentials
\[d z = d x + i d y , \;d\bar{z} = d x - i d y.\]
These form a basis for the complexified cotangent space at each point of $U$.  There is also a dual basis
\[ \frac{\partial}{\partial z }  := \frac{1}{2}\left( \frac{\partial}{\partial x} - i \frac{\partial}{\partial y}\right), \;
\frac{\partial}{\partial \bar{z} }  := \frac{1}{2}\left( \frac{\partial}{\partial x} + i \frac{\partial}{\partial y}\right)\]
for the complexified tangent space.

We now claim that we can split the tangent space $T(X) = T^{1,0}(X) + T^{0,1}(X)$, where the former consists of multiples of $\frac{\partial}{\partial z}$ and the latter of multiples of  $\frac{\partial}{\partial \bar{z}}$; clearly a similar thing is possible for the cotangent space.
This is always possible locally, and a holomorphic map preserves the decomposition.
One way to  see the last claim quickly is that given $g: U \to \mathbb{C}$ for $U \subset \mathbb{C}$ open and $0 \in U$ (just for convenience), we can write
\[ g(z) = g(0) + Az + A' \bar{z} + o(|z|) \]
where $A =   \frac{\partial g }{\partial  z }(0), A' = \frac{\partial g }{\partial \bar{z} }(0)$, which we will often abbreviate as $g_z(0), g_{\bar{z}}(0)$.  If $\psi: U' \to U$ is holomorphic and conformal sending $z_0 \in U' \to 0 \in U$, we have
\[ g(\phi(\zeta)) = g(\phi(0)) + A \phi'(z_0)(\zeta-z_0) + A' \overline{ \phi'(z_0)(\zeta-z_0)} + o(|z|); \]
in particular, $\phi$ preserves the decomposition of $T_0(\mathbb{C})$.

Given $f: X \to \mathbb{C}$ smooth, we can consider the projections of the 1-form $df$ onto $T^{1,0}(X)$ and $T^{0,1}(X)$, respectively; these will be called $\partial f, \overline{\partial} f$.  Similarly, we define the corresponding operators on 1-forms: to define $\partial \omega$, first project onto $T^{0,1}(M)$ (the reversal is intentional!) and then apply $d$, and vice versa for $\overline{\partial} \omega$.

In particular, if we write in local coordinates $\omega = u d z + v d\bar{z}$, then
\[ \partial \omega = d( v d \bar{z}) = v_z d z \wedge d\bar{z},\]
and
\[ \overline{\partial} \omega  = d( u d z) = u_{\bar{z}} d\bar{z} \wedge d z.\]
To see this, we have tacitly observed that $d v = v_z d z + v_{\bar{z}} d\bar{z}$.

### Picard group of holomorphic line bundles
 {#PicardGroupOfHolomorphicLineBundles}

The [[Picard group]] of a Riemann surface is the group of [[holomorphic line bundles]] in it. Introductions include ([Bobenko, section 8](#Bobenko)).

See also at _[[Narasimhan–Seshadri theorem]]_ and at _[moduli space of connections -- Flat connections over a torus](moduli+space+of+connections#FlatConnectionsOverATorus)_.

### Central theorems

In the theory of Riemann surfaces, there are several important theorems.  Here are two:

* The [[Riemann-Roch theorem]], which analyzes the vector space of meromorphic functions satisfying certain conditions on zeros and poles;

* The [[uniformization theorem]], which partially classifies Riemann surfaces.

### Homotopy type

A [[compact topological space|compact]] Riemann surface of [[genus]] $g \geq 2$ is a [[homotopy 1-type]]. The [[fundamental groupoid]] is a [[Fuchsian group]].


([MO discussion](http://mathoverflow.net/a/93340/381))

### Branched covers

By the [[Riemann existence theorem]], every connected compact [[Riemann surface]] admits the [[structure]] of a [[branched cover of the Riemann sphere]]. ([MO discussion](http://mathoverflow.net/a/53286/381))

### Function field analogy

[[!include function field analogy -- table]]

## Related concepts

* [[annulus]], [[2-sphere]], [[trinion]]

* [[Teichmüller space]]

* [[moduli space of Riemann surfaces]]

* [[super Riemann surface]]

* [[stable vector bundle]]

* [[elliptic curve]]

* [[worldsheet]]

* [[beta-gamma system]]

* [[quadratic differential]]

## References

Historical references:

* [[Hermann Weyl]], _Die Idee der Riemannschen Fl&#228;che_, 1913 (*The concept of a Riemann surface*) (on the book, by Peter Schreiber, 2013: [web](http://mathineurope.eu/en/home/47-information/math-calendar/971-1913-publication-of-the-concept-of-a-riemann-surface-by-hermann-weyl))

* {#Rado25} [[Tibor Radó]], *Über den Begriff der Riemannschen Fläche*, Acta Litt. Sci. Szeged, 2 (101-121), 10 ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/rado.pdf), [pdf](http://acta.bibl.u-szeged.hu/13312/1/math_002_101-121.pdf))

  > (proving the [[triangulation theorem]])

Lecture notes:

* {#Bobenko} [[Alexander Bobenko]], _Compact Riemann Surfaces_ lecture notes ([pdf](http://page.math.tu-berlin.de/~bobenko/Lehre/Skripte/RS.pdf))

*  [[Eberhard Freitag]], _Riemann surfaces -- Sheaf theory, Riemann Surfaces, Automorphic forms_, 2013 ([pdf](http://www.rzuser.uni-heidelberg.de/~t91/skripten/riemfl.pdf))

* {#Wehler20} [[Joachim Wehler]], *Riemann surfaces* 2020 ([pdf](https://www.mathematik.uni-muenchen.de/~wehler/20190530_RiemannSurfacesScript.pdf))


[[!redirects Riemann surfaces]]