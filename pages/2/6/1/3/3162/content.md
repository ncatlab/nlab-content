
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea 

From the [[nPOV]], a [[cohomology]] set $H(X,A)$ of cohomology classes on an [[object]] $X$ with coefficients in an [[object]] $A$ in an [[(∞,1)-topos]] is the [[decategorification]] of an [[derived hom space|hom ∞-groupoid]] $\mathbf{H}(X,A)$. The objects in this $\infty$-groupoid are called **cocycles** . The morphisms are called _coboundaries_ .

For suitable choices of $\mathbf{H}$ this applies notably to cocycles in

* general [[abelian sheaf cohomology]]

* general [[nonabelian cohomology]]

and in particular to

* [[chain homology and cohomology|chain cohomology]]

* [[group cohomology]]

* [[nonabelian group cohomology]].

It also encompasses variations such as cocycles in

* [[equivariant cohomology]]

* [[twisted cohomology]]

* [[differential cohomology]].

For a detailed discussion of this and how it relates to various familiar realizations of cocycles, see [[cohomology]] and the links provided there.

## Realizations of cocycles

The objects in the [[derived hom space|hom ∞-groupoid]] $\mathbf{H}(X,A)$ are often expressed in terms of various 1-categorical models for $\mathbf{H}$, such as a [[homotopical category]] $C$ equipped with 

* the extra structure of a [[calculus of fractions]],

* or with the structure of a [[category of fibrant objects]] 

* or even with the full structure of a [[model category]].

In all of these cases, cocycles $c$ on $X$ with coefficients in $A$ may be modeled by [[span]]s of the form

$$
  \array{
    X &\stackrel{\in FW}{\leftarrow}& \tilde X \to A
  }
$$

in the ordinary [[category]] $C$, where the morphism on the left is taken from a special class of morphisms (for instance from the class of acyclic fibrations in the case that $C$ is a [[category of fibrant objects]]). In each case the relevant [[hom-set]] in the [[homotopy category]] $H(X,A) = \pi_0 \mathbf{H}(X,A)$ is given by the collection of cocycles module an [[equivalence relation]] given by coboundaries. In formulas

$$
  H(X,A) = colim_{\tilde X \stackrel{\in FW}{\to} X} Hom_{\pi C}(X,A)
  \,.
$$

For details see the respective discussion at [[homotopy category]], [[calculus of fractions]] and [[category of fibrant objects]].

## Terminology

In the existing literature on [[localization]]s, the spans $ X \stackrel{\in FW}{\leftarrow} \tilde X \to X$ are often not called by a dedicated special term. On the other hand, in the existing literature that explicitly uses the term "cocycle", often more pedestrian definitions are used and it is not made explicit that morphisms in a [[homotopy category]] are being represented.

An notable exception to this is the article

* Jardine, _Cocycle categories_ ([web](http://www.math.uiuc.edu/K-theory/0782/))

that makes both the abstract concept and the terminology of cocycles explicit and manifest. The author is mainly motivated from the [[model structure on simplicial presheaves]] and its variants, which in particular models cocycles and cohomology of [[abelian sheaf cohomology]]. But more generally it models [[nonabelian cohomology]]. Notably when the underlying space is the point, it models ordinary [[chain homology and cohomology|chain cohomology]] as well as [[group cohomology]] and [[nonabelian group cohomology]].

Notice that this article chooses to work with the full structure of a [[model category]] but presents constructions for cocycles entirely analogous to and in fact inspired by those used in a [[category of fibrant objects]] or in one equipped with a [[calculus of fractions]]. The author emphasizes that he can give a definition where the left leg of the cocycle spans are not required to be acyclic fibrations, but can be any weak equivalences. But all this is just a technical question of how exactly to model a cocycle, not a question of principle of concept. For instance in this context every cocycle defined with respect to a weak equivalence over its domain is cohomologous to one defined with respect to an acyclic fibration over its domain.

In the special case that the category $C$ is [[Cat]] equipped with the [[folk model structure on Cat]], cocycles out of acyclic fibrations -- which are [[k-surjective functor]]s for all $k$ in this case -- have been considered in 

* Makkai, _[Avoiding the axiom of choice in general category theory](http://www.math.mcgill.ca/makkai/anafun/)_ .

There they are called **[[anafunctor]]s**.

One could take this as a suggestion to find a dedicated term for spans as above and call generally such a span an **anamorphism**. An anamorphism would be effectively the same as a cocycle, but the term _[[morphism]]_ in it would amplify the nature of cocycles as morphisms.

So 

* a _cocycle_ on $X$ with coefficients in $A$

would correspond to 

* an _anamorphism_ from $X$ to $Y$.


## Examples

### Cochain cocycles {#CochainCocycles}

The archetypical example of a notion of cocycles is that of [[chain homology and cohomology|chain cohomology]]:

a non-negatively graded [[chain complex]] $V_\bullet = (V_0 \stackrel{\partial_V}{\leftarrow} V_1 \stackrel{\partial_V}{\leftarrow} V_2 \stackrel{}{\leftarrow} \cdots)$ is given. An element $v \in V_n$ is a **chain**. A linear dual $\omega : V_n \to k$ on its elements is a **cochain**. The cochains arrange into the [[cochain complex]] $V^\bullet = (V^0 \stackrel{d_V}{\to} V^1 \to \stackrel{d_V}{\to} V^2 \to \cdots) := (V_0^* \stackrel{(\partial_V)^*}{\to} V_1^* \to \stackrel{(\partial_V)^*}{\to} V_2^* \to \cdots)$ 

A cochain $\omega \in V^n$ is a **cocycle** if it is closed with respect to the [[differential]] $d_V$ in that

$$
  d_V \omega = 0
  \,.
$$

One sees that such cocycles are in bijection to [[morphism]]s of [[chain complex]]es

$$
  \omega : V_\bullet \to (\mathbf{B}^n k)_\bullet
  \,,
$$

where on the right we have the [[Eilenberg-MacLane object]] of the ground field $k$, which is the chain complex trivial everywhere except in degree $n$, where it is $k$:

$$
  \mathbf{B}^n k = (0 \leftarrow \cdots \leftarrow 0 \leftarrow k \leftarrow 0 \leftarrow \cdots)
  \,.
$$

By definition such a morphism is a collection of morphisms $\omega_r : V_r \to (\mathbf{B}^n k)_r$, of which by definition only $\omega_n \in V_n^* = V^n$ can be nontrivial.

For the collection of these maps to be a morphism of chain complexes they have to make all squares in sight commute. The only nontrivial one in this case is the one

$$
  \array{
    V_{n+1} &\to& 0
    \\
    {}^{\mathllap{\partial_V}}\downarrow && \downarrow
    \\
    V_n &\stackrel{\omega}{\to}& k
  }
  \,.
$$

Its commutativity means in formulas that

$$
  \omega \circ \partial_V = d_V \omega = 0
  \,,
$$

which is the cocycle condition from above.

In most cases the morphism $\omega : V_\bullet \to \mathbf{B}^n k$ defined this way is already a morphism in the relevant [[(∞,1)-category]] $\mathbf{H}_{Ch_\bullet}$ of chain complexes: this is modeled for instance by the projective [[model structure on chain complexes]]. In this every object is fibrant, and the cofibrant objects are those consisting of projective $k$-[[module]]s. If we assume that all our modules are projective (for instance in the archetypical case that our modules are simply [[vector space]]s), then $\omega : V_\bullet \to \mathbf{B}^n k$ is a cocycle in $\mathbf{H}_{Ch_\bullet}$ from the above abstract nonsense point of view. For its cohomology class we may write

$$
  [\omega] \in H^n(V_\bullet,k) = \pi_0 \mathbf{H}_{Ch_\bullet}(V_\bullet, \mathbf{B}^n k)
  \,.
$$

## Objects classified by cocycles {#Classification}

One says for $\omega \in \mathbf{H}(X,A)$ a cocycle, that the object **classified by the cocycle** is its [[homotopy fiber]] $P \to X$ regarded as an object in the [[overcategory]] over $X$.

This homotopy fiber may be thought of as the internal [[principal ∞-bundle]] in $\mathbf{H}$ with classifying map $\omega$.


## Related concepts

[[!include chains and cochains - table]]


[[!redirects cocycles]]
