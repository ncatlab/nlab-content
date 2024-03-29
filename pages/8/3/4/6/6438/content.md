
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Phyiscs
+--{: .hide}
[[!include physicscontents]]
=--
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
=--
=--




> This is a sub-entry of [[sigma-model]]. See there for background and context.

***

#Contents#
* table of contents
{:toc}

## Exposition of quantum sigma-models

Above we have discussed some standard [classical sigma-models](#ExpositionClassical) and [higher gauge theories as sigma-models](#GaugeTheoryAsSigmaModel), also mostly classically. Here we talk about the [[quantization]] of these models (or some of them) to [[QFT]]s: _quantum $\sigma$-models_ .



### Particle on the line

for the moment see the discussion at

* [[path integral as a pull-push transform]]

### Topological string on a smooth manifold and string topology operations
 {#StringTopology}

Chas and Sullivan famously noticed, that the [[homology group]]s of the [[free loop space]] $L X$ of a [[compact space|compact]] [[orientation|oriented]] [[smooth manifold]] $X$ are equipped with an interesting paring operation

$$
  H_\bullet(L X) \otimes H_\bullet(L X) \to H_{\bullet - dim X}(L X)
$$

that generalizes the [[Goldman bracket]] on $H_0(L X) \simeq F \pi_1(X)$. Since this operation is induced from concatenating loops, they called it the _string product_ . Its study has come to be known as [[string topology]], now a branch of [[differential topology]].

It was soon realized that there indeed ought to be a relation to [[string]] physics: there ought to be a 2-dimensional [[quantum field theory]] associated with $X$, as follows:

for $\Sigma$ a 2-dimensional [[surface]] with incoming and outgoing [[boundary]] components $\partial_{in} \Sigma \stackrel{in}{\to} \Sigma \stackrel{out}{\leftarrow} \partial_{out} \Sigma$, the "space of [[state]]s" of the theory ought to be given by the [[homology group]]s $H_\bullet(X^{\partial_{in} \Sigma})$ and $H_\bullet(X^{\partial_{out} \Sigma})$, and the [[path integral as a pull-push transform]] along $\Sigma$ ought to be given by push-forward and dual [[fiber integration]]

$$
  (X^{out})_* \circ (X^{in})^! : H_\bullet(X^{\partial_{in} \Sigma})
   \to 
  H_{\bullet- dim X}(X^{\partial_{out} \Sigma})
$$

induced by the [[mapping space]] [[span]]

$$
  \array{
     && X^{\Sigma}
     \\
     & {}^{\mathllap{X^{in}}}\swarrow && \searrow^{\mathrlap{X^{out}}}
     \\
    X^{\partial_{in} \Sigma} &&&& X^{\partial_{out} \Sigma}
  }
  \,.
$$

For $\Sigma \simeq S^1 \vee S^1$ the 3-holed sphere with two incoming and one outgoing circle, this would describe an operation on string states induced by the merging of two closed strings to a single one

$$
  H_\bullet(X^{S^1 \coprod S^1})
 \simeq
  H_\bullet(L X) \times H_\bullet(L X)
  \to 
  H_\bullet(L X)
$$

and this ought to be Chas-Sullivan string product operation.

That this is indeed the case was finally demonstrated by [[Ralph Cohen]] and [[Veronique Godin]]. (See [[string topology]] for all references.) While the idea is rather simple, the concrete realization, especially when taking open strings into account, is fairly technical (see for instance [this MO discussion](http://mathoverflow.net/questions/66977/pull-push-in-godins-hcft-for-string-topology)).

But there should be more to it: one expects that these operations on [[homology group]]s are just a shadow of a refined construction on [[chain complex]]es (for instance [[singular homology|singular chains]]): while Godin's construction gives an _[[HQFT]]_ -- a [[quantum field theory]]  that depends only on the [[homology]] of the [[moduli space]]s of the relevant [[cobordism]]s -- one expect that this is the homology of a genuine [[extended TQFT]] (which in this dimension is widely but somewhat unfortunately known under the term "[[TCFT]]"). Remarks on how that might be obtained have been made in print by Costello and Lurie.

In the context of our discussion of $\sigma$-models, we would want to refine this even one further step and ask: is the string-topology TCFT of a manifold (given that it exists) formally a $\sigma$-model with [[target space]] that manifold, and using some suitable [[background gauge field]]?

Given that the string topology [[TCFT]] itself has not been fully identified yet, we cannot expect a complete answer to this at the moment, but we will discuss some crucial ingredients that are available. 

Notably we can first ignore the dynamics of the system, just consider the kinematics and ask the simple question: _which quantum $\sigma$-models on $X$ have [[(∞,n)-vector space]]s of [[states]] whose [[decategorification]] are graded [[homology group]]s $H_\bullet(X^{\partial \Sigma})$ of mapping spaces of $X$?_

The answer to this question is more more transparent after we formulate the question in more generality: as observed by Cohen and Godin in their _[[A Polarized View of String Topology]]_ , we may assume without restriction that the [[homology group]]s here are with respect to the [[generalized homology]] with coefficients in any [[E-∞ ring|commutative ∞-ring]] $K$ (as long as this is an "$\infty$-field" and as long as $X$ is $K$-[[orientation in generalized cohomology|oriented]]):

$$
  H_\bullet(X^{\partial_{in} \Sigma}) 
   := 
  H_\bullet(X^{\partial_{in}} \Sigma, K)
  \,.
$$ 

Most every statement about ordinary commutative rings has its analog for 
[[E-∞ ring|commutative ∞-rings]], and so we can just follow our nose:

An _[[(∞,1)-vector space]]_ over $K$ is an $K$-[[module spectrum]] and we have an [[(∞,1)-category]] $K$[[Mod]] of such $\infty$-vector spaces. Notice that these are a [[categorification]] of the ordinary notion of [[vector space]] only in the "$r$"-direction of the lattice of [[(n,r)-category|(r,n)-categories]]. A genuine [[(∞,n)-vector space]] over $K$ -- as appears in the description of general $n$-dimensional $\sigma$-models -- is instead an object of $(\cdots ((K Mod) Mod) \cdots ) Mod $. In particular the $(\infty,2)$-category of $(\infty,2)$-vector spaces over $K$ is 
something like $(K Mod) Mod$.

This means that an [[(∞,1)-vector bundle]] with flat [[connection on an ∞-bundle|∞-connection]] over some [[manifold]] $X$ is equivalently encoded by an [[(∞,1)-functor]]

$$
  \alpha : \Pi X \to K Mod
$$

out of the [[fundamental ∞-groupoid]] of $X$. This assigns to each point of $X$ a $K$-module -- the [[fiber]] of the [[(∞,1)-vector bundle]] thus encoded -- to each path in $X$ an [[equivalence in an (∞,1)-category|equivalence]] between the fibers over its endpoints, and so on: this is the [[higher parallel transport]] of a flat $\infty$-connection. We can also think of this as an [[∞-representation]] of $\Pi X$ on $K$-modules, also called a _[[representation up to homotopy]]_ . For instance if $X$ is the classifying space $X = B G$ of a [[discrete ∞-group]], then flat [[(∞,1)-vector bundle]]s on $X$ are precisely [[∞-representation]]s of $G$.

There is an evident [[full sub-(∞,1)-category]]

$$
  K Line \hookrightarrow K Mod
$$

of 1-dimensional $(\infty,1)$-vector spaces:  $K$-lines -- $K$-modules that are equivalent to $K$ itself regarded as a $K$-module. 

An $(\infty,1)$-vector bundle $\nabla : \Pi(X) \to K Mod$ that factors through this inclusion is a _$K$-line $\infty$-bundle_ .

One finds, as for the case of ordinary 1-vector spaces, that

$$
  K Line \simeq B GL_1(K) \simeq B Aut(K)
$$

is the [[delooping]] of the [[automorphism ∞-group]] of $K$. This means that $K$-line $\infty$-bundles are equivalently $GL_1(K)$-[[principal ∞-bundle]]s. We can think of the inclusion

$$
  \rho : B GL_1(K) \stackrel{\simeq}{\to} K Line \hookrightarrow K Mod
$$

as being the canonical linear [[∞-representation]] of $GL_1(K)$; and for $g : \Pi X \to B GL_1(K)$ a $GL_1(K)$-[[principal ∞-bundle]] of the $(\infty,1)$-vector bundle

$$
  \Pi X \stackrel{g}{\to} B GL_1(K) \stackrel{\rho}{\to} K Mod
$$

as the corresponding [[associated ∞-bundle]].

Therefore it makes sense to consider $\sigma$-models with [[target space]] $X$ and [[background gauge field]] given by an $K$-line $\infty$-bundle.

For instance for $K = K U$ the [[K-theory spectrum]], there is a canonical morphism $B^2 U(1) \to B GL_1(KU)$ and hence to every [[circle n-bundle|circle 2-bundle]] $\alpha : \Pi X \to B^2 U(1)$ is associated the corresponding $K U$-line $\infty$-bundle

$$
 \Pi X \stackrel{\alpha}{\to} B^2 U(1) \stackrel{}{\to}
   B GL_1(K U) \stackrel{\rho}{\to} K U Mod
  \,.
$$

Or for $K = tmf$ the [[tmf]] spectrum, there is a canonical morphism $B^3 U(1) \to B GL_1(tmf)$ and hence to every [[circle n-bundle|circle 3-bundle]] $\alpha : \Pi X \to B^3 U(1)$ is associated the corresponding $tmf$-line $\infty$-bundle

$$
 \Pi X \stackrel{\alpha}{\to} B^3 U(1) \stackrel{}{\to}
   B GL_1(tmf) \stackrel{\rho}{\to} tmf Mod
  \,.
$$

This was amplified by Ando, Blumberg, Gepner, Hopkins, and Rezk (see the reference at [[(∞,1)-vector bundle]]),  who notice much of the theory of [[generalized (Eilenberg-Steenrod) cohomology|K-(co)homology]] -- including notably its [[Thom spectrum]] theory and its [[twisted cohomology]] -- is neatly captured by simple statements about such $A$-line $(\infty,1)$-bundles. For instance the notion of [[orientation in generalized cohomology]] simply boils down to the notion of trivialization of such $K$-line $\infty$-bundles: 

a vector bundle $E \to X$ is _$K$-oriented_ precisely if the corresponding [[Thom space]]-bundle -- which is a [[sphere spectrum]]-line $\infty$-bundle $V: \Pi(X) \to S Line$ is such that the canonically associated $K$-line bundle is trivializable:

$$
  (V is K-orientable)
    \Leftrightarrow
  ( (\Pi(X) \stackrel{V}{\to} S Line \to K Line)
    \simeq
    const_K  )
  \,.
$$

For our discussion here this means that Cohen-Godin's finding that the string topology HQFT exists for $K$ such that $X$ is $K$-orientable meaks that the $K$-line $\infty$-bundle background field that we are to consider in this context are to be trivializable.

Recall that if we interpret an $(\infty,2)$-vector bundle as a [[background gauge field]] for a $\sigma$-model, then for $\Sigma$ any 2-dimensional [[cobordism]] the corresponding [[(∞,1)-vector space]] of states assigned to, say, the incoming boundary $\partial_{in} \Sigma$ is defined to be the $\infty$-vector space of sections of the [[transgression]] of this $(\infty,2)$-vector bundle to an [[(∞,1)-vector bundle]] the [[mapping space]] $X^{\partial_{in} \Sigma}$. The transgression of a trivial bundle is again the trivial bundle. And the $\infty$-vector space of (co)sections is, in the discrete case,  as we had discussed [above](ExpositionQuantization), the [[(∞,1)-colimit]]

$$
  \Gamma_{\partial_{in} \Sigma} 
    := 
  \lim_\to(\Pi X^{\partial_{in} \Sigma} \to S Line \to  K Mod )
  \,.
$$

This one can compute. By triviality of the bundle, Ando-Blumberg-Gepner-Hopkins-Rezk observe that this is the $K$-homology spectrum of $X^{\partial_{in} \Sigma}$

$$
  \cdots \simeq (\Sigma^\infty X^{\partial_{in} \Sigma}) \wedge K
  \in K Mod
 \,.
$$

(Here the main point is that for the bundle _not_ being trivial the result encodes the corresponding _[[twisted cohomology]]_ , but for our purposes at the moment we want the oriented/trivializable case.)

This is hence the $\infty$-vector space of states over $\partial_{in} \Sigma$ assigned by a $\sigma$-model with [[background gauge field]] a $K$-line $\infty$-bundle over a $K$-oriented [[target space]]. 

Notice that for $K = H \mathbb{Z}$ the [[Eilenberg-MacLane spectrum]] for the [[integer]]s, we have an equivalence

$$
  H \mathbb{Z} Mod \simeq Ch_\bullet
$$

and in fact

$$
  H \mathbb{Z} Alg \simeq dgAlg_{\mathbb{Z}}
$$

betwee the [[(∞,1)-category]] of $H \mathbb{Z}$-[[module spectra]]/$H \mathbb{Z}$-[[algebra spectra]] (see there for details on this equivalence) and the $(\infty,1)$-category [[presentable (infinity,1)-category|presented]] by the [[model structure on chain complexes]]/[[model structure on dg-algebras|on dg-algebras]]. Under this equivalence the above [[module spectrum]]-space of states over the circle ought to be identified with the ordinary integral homology chain complex

$$
  (\Sigma^\infty X^{S^1}) \wedge K
  \sim
  C_\bullet(X^{S^1})
  \,.
$$

The "[[decategorification]]" of this $\infty$-vector space of states is precisely the tower of homology groups of $X$:

$$
  \pi_\bullet(\Gamma_{\partial \Sigma}) = H_\bullet(X^{\partial_{in} \Sigma}, K)
  \,.
$$


### The topological $A$-model string and Gromov-Witten theory
 {#GWTheory}

The quantum [[string]]-[[sigma model]] whose [[target space]] is a [[symplectic manifold]] $(X, \omega)$ -- often called the [[A-model]] -- is given by the

* [[Gromov-Witten theory]] 

of $X$. For the moment see there for more details.

### Quantum abelian Chern-Simons
 {#QuantumAbelianCS}

For the moment see

* [[Topological Quantum Field Theories from Compact Lie Groups]].

