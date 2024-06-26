
> See also _[[differentiable function]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--



# Contents
* table of contents
{: toc}

## Idea

_Differentiation_ is the process that assigns to a [[function]] $f : X \to Y$ its *derivative*, sometimes denoted $d f$. The derivative is a function that, roughly speaking, assigns to each point $x \in X$ the linear transformation $d f_x$ that maps [[infinitesimal space|infinitesimal]] [[differences]] $y - x$ (for points $y$ infinitesimally close to $x$) to infinitesimal differences $f(y) - f(x)$. 

## Definitions 

### Classical (analytic) definitions 

Classically, if $f: \mathbb{R}^n \to \mathbb{R}$ is a function, the derivative $d f_x$ at a point $x \in \mathbb{R}^n$ is defined by a [[convergence|limiting process]]: it is the unique (when it exists) [[linear transformation]] $L: \mathbb{R}^n \to \mathbb{R}$ such that 

$$\lim_{h \to 0} \frac{f(x + h) - f(x) - L h}{{|h|}} = 0$$ 

or in other words such that 

$$f(y) = f(x) + L(y - x) + g(y)$$ 

where $g(y)$ is $o({|y - x|})$ (see [[o-notation]]). We say in that case that $f$ is *differentiable* at $x$, with *derivative* $d f_x = L$. When $n = 1$, such a linear transformation $L: \mathbb{R} \to \mathbb{R}$ is multiplication by a [[scalar]] $\lambda \in \mathbb{R}$. This is often denoted $f'(x)$, so that the derivative may be regarded as another function $f': \mathbb{R} \to \mathbb{R}$. 

We say $f: \mathbb{R}^n \to \mathbb{R}$ is *differentiable* if it is differentiable at every point $x$ of its [[domain]]. In that case, we get a global derivative function $\mathbb{R}^n \times \mathbb{R}^n \to \mathbb{R}$ which takes a pair $(x, h)$ to $d f_x(h)$. We can then ask whether this function is itself differentiable, i.e., whether the differentiation process can be iterated. The *$n$-th derivative* is the result of differentiating $n$ times (the $0$-th derivative of $f$ is just $f$). We say that $f: \mathbb{R}^n \to \mathbb{R}$ is *infinitely differentiable* (or more briefly, that $f$ is *smooth*) if it has an $n$-th derivative for each [[natural number]] $n$. 

Notice that a differentiable function is necessarily [[continuous map|continuous]] (indeed, it is locally a [[Lipschitz function]]). One denotes the class of functions having a *continuous*[^1] $n^{th}$ derivative by $C^n(\mathbb{R}^n)$. Thus continuous functions $f: \mathbb{R}^n \to \mathbb{R}$ form a filtration 

$$\ldots \subset C^n(\mathbb{R}^k) \subset \ldots \subset C^1(\mathbb{R}^k) \subset C^0(\mathbb{R}^k)$$ 

and the intersection $C^\infty(\mathbb{R}^k) \coloneqq \bigcap_{n \geq 0} C^n(\mathbb{R}^k)$ coincides with the class of smooth functions. 

[^1]: Without the continuity assumption on derivatives, the class of (once-)differentiable functions exhibits non-trivial [[descriptive set theory|descriptive set-theoretic]] complexity, as may be surmised by [this paper](http://journals.cambridge.org/action/displayAbstract?fromPage=online&aid=6984080) by Kechris and Woodin. Thus the continuity assumption eliminates troublesome pathologies. 

Evidently differentiation gives a function $D: C^{n+1}(\mathbb{R}^k) \to C^n(\mathbb{R}^k \times \mathbb{R}^k)$. The convenient setting for developing the differential calculus is to go directly to the smooth case, where we have $D: C^\infty(\mathbb{R}^k) \to C^\infty(\mathbb{R}^k \times \mathbb{R}^k)$ without having to keep track of the degree of differentiability. 

This development carries over more generally to [[smooth manifolds]] $X$, which are locally (smoothly) isomorphic to [[Euclidean spaces]] $\mathbb{R}^k$. 

### Differentiation as a functor 
 {#AsAFunctor}

_Differentiation_ in more conceptual terms is a [[functor]] $d : Diff \to Diff$ on the [[category]] [[Diff]] of [[smooth manifold]]s that sends

* a manifold $X$ to its [[tangent bundle]] $T X$; recall that the points of $T X$ are [[ordered pairs]] $(x, v)$ where $x \in X$ and $v$ is a [[tangent vector]] at $x$, i.e., an (augmented) [[derivation]] $v: C^\infty(X) \to \mathbb{R}$ on the [[associative unital algebra|algebra]] of smooth functions, augmented by evaluation $ev_x: C^\infty(X) \to \mathbb{R}$ at $x$;

* a [[smooth function]] $f \colon X \to Y$ to its differential $d f : T X \to T Y$ (cf. *[[pushforward of vector fields]]*):

  if $\gamma : [-1,1] \to X$ is a path in $X$ that represents a vector $v \in T_x X$, then $(d f)(v) \in T_{f(x)} Y$ is the vector represented by the path
  $[-1,1] \stackrel{\gamma}{\to} X \stackrel{f}{\to} Y$. 

Equivalently, a smooth map $f: X \to Y$ induces an algebra map $f^\ast = - \circ f: C^\infty(Y) \to C^\infty(X)$, and hence by composition sends a derivation $v: C^\infty(X) \to \mathbb{R}$ to a derivation $v \circ f^\ast: C^\infty(Y) \to \mathbb{R}$ augmented by $ev_{f(x)}: C^\infty(Y) \to \mathbb{R}$). Concretely: $v \circ f^\ast(\phi) = v(\phi \circ f)$ for $\phi \in C^\infty(Y)$. Then the differential $d f: T X \to T Y$ is defined by $d f(x, v) = (f(x), v \circ f^\ast)$. 

According to either of these descriptions, differentiation is manifestly functorial. In the English literature, this fact is known as the [[chain rule]]. In more traditional form: 

$$d(f \circ g)_x = d f_{g(x)} \circ d g_x.$$

In a context $H$ of [[synthetic differential geometry]] (SDG) the functor $d$ is simply the [[internal hom]] out of the [[infinitesimal space|infinitesimal interval]] $D$

$$
  d = [D, -] : H \to H
  \,.
$$ 

where $D \hookrightarrow \mathbb{R}$ is the smooth locus defined by $x^2 = 0$. (Classically, i.e., in the [[topos]] $Set$, this locus consists of just a single point[^2], but in toposes that model SDG it should be regarded as an infinitesimal neighborhood about a point.) This description as internally [[representable functor]] underlies the following classical fact: 

+-- {: .num_theorem} 
###### Theorem 
Differentiation is a [[product-preserving functor]]. 
=-- 

For example, the product of two smooth functions $f, g: X \to \mathbb{R}$ is a composition 

$$X \stackrel{\Delta}{\to} X \times X \stackrel{f \times g}{\to} \mathbb{R} \times \mathbb{R} \stackrel{mult}{\to} \mathbb{R}$$ 

and the product rule for differentiation derives by applying the functor $d$ which results in the composite 

$$T X \stackrel{\Delta}{\to} T X \times T X \stackrel{d f \times d g}{\to} T \mathbb{R} \times T \mathbb{R} \stackrel{d mult}{\to} T \mathbb{R}$$ 

which reduces to computing $d mult$. 

[^2]: According to John Bell, the fact that classically this is merely a point bears comparison to Bishop Berkeley's objections to the differential calculus he put forth in *The Analyst*. 


## Exposition of differentiation via infinitesimals
 {#ExpositionDifferentiationViaInfinitesimal}


We attempt to give an exposition of differentiation not via taking limits in the sense of [[analysis]], but rather, by working with [[infinitesimal space]]s as in [[synthetic differential geometry]].

### Setup

For that purpose we regard objects such as the [[real line]] $\mathbb{R}$ and more generally any [[smooth manifold]] as being objects of a [[Models for Smooth Infinitesimal Analysis|well adapted]] [[smooth topos]] of [[smooth space]]s. But in fact much less is required for most of the discussion. For the basic theory, it is sufficient to work in the canonical [[site]] of such a topos, namely, the category $SmoothLoc$ of [[smooth loci]]. This site is defined via a categorial equivalence with the [[opposite category]] of the category of [[smooth algebra]]s:

$$
  C^\infty: SmoothLoc \stackrel{\sim}{\longrightarrow} SmoothAlg^{op}
$$


Apart from the real line $\mathbb{R}$, the other object involved in our discussion of the basics of differentiation is the first order [[infinitesimal space|infinitesimal line segment]] $D$ (an [[infinitesimally thickened point]]), a [[subobject]] of $\mathbb{R}$. This subobject collects those points of $\mathbb{R}$ that square to zero under the canonical multiplicative structure of $\mathbb{R}$

$$
  D = \{\epsilon \in \mathbb{R} | \epsilon^2 = 0\}
  \,.
$$

Although this is just $\{0\}$ when interpreted in the usual context of [[Set]], here we are to interpret this in the ambient [[smooth topos]], or equivalently just in our [[site]] $SmoothLoc$ for it. That is to say, $D$ satisfies a [[pullback]] square in $SmoothLoc$:

$$
  \array{
    D &\to& *
    \\
    \downarrow && \downarrow^{\mathrlap{0}}
    \\
    \mathbb{R} &\stackrel{(-)^2}{\to}& \mathbb{R}
  }
$$

Dually, the categorial equivalence $C^\infty$ from $SmoothLoc$ to the [[opposite category]] of [[smooth algebra]]s carries the above pullback square to a [[pushout]] square of [[smooth algebras]]:

$$
  \array{
     C^\infty(D) &\leftarrow& C^\infty(*) \simeq \mathbb{R}
     \\
     \uparrow && \uparrow^{\mathrlap{f \mapsto f(0)}}
     \\
     C^\infty(\mathbb{R}) 
      &\stackrel{x \mapsto x^2}{\leftarrow}& 
     C^\infty(\mathbb{R})
  }
$$

Here along the bottom and on the right are the ordinary smooth algebras of [[smooth function]]s on the [[smooth manifold]]s $\mathbb{R}^1 = \mathbb{R}$ and $\mathbb{R}^0 = *$, whereas $C^\infty(D)$ is new notation, suggestive and justified, for whatever the algebra of functions on the object $D$ is, where $D$ is _defined_ by the fact that it has this algebra of functions. The bottom morphism sends a smooth function $f : \mathbb{R} \to \mathbb{R}$ to the function $f((-)^2) : \mathbb{R} \to \mathbb{R}$. If we write $x = Id : \mathbb{R} \to \mathbb{R}$ for the canonical [[coordinate]] function, then this sends $x$ to the function $x^2$.  

Notice that the commutativity of this pushout square means that the image in $C^\infty(D)$ of the squared coordinate function $x^2 \in C^\infty(\mathbb{R})$  is zero. This is  because the former is the image under the bottom morphism of the coordinate function $x$ and that maps under the right vertical morphism to $0 \in C^\infty(*) \simeq \mathbb{R}$.

In fact one can show that the [[pushout]] $C^\infty(D)$ is _generated_ by the coordinate function $x \in C^\infty(\mathbb{R}))$ subject to the relation $x^2 = 0$: it is the [[ring of dual numbers]]

$$
  \begin{aligned}
    C^\infty(D) & \simeq C^\infty(\mathbb{R})/(x^2) 
    \\
    & \simeq \mathbb{R}[x]/(x^2)
  \end{aligned}
  \,.
$$

(Here in the second step we have used [[Hadamard's lemma]].)

This computation of the smooth algebra $C^\infty(D)$ of smooth functions on $D$ expresses the intuitive idea that $D$ is such a small neighbourhood of $0$ in $\mathbb{R}$ that while the canonical coordinate function of $\mathbb{R}$ restricted to $D$ is non-vanishing (it would vanish only when restricted entirely to the point 0) it is "so small that its square is always 0". Readers who like this intuitive statement should keep it in mind, as it is accurate and useful, whereas readers who do not like it could stick with the above precise definition, which unwinds this slogan in the [[internal logic]] of the ambient [[smooth topos]] that we keep alluding to.

In order to remind us about the infinitesimal nature of the generator $x$ in $C^\infty(D)$ we shall usually call this "$dx$" and write

$$
  C^\infty(D) = \mathbb{R}[dx]/((dx)^2) \simeq \mathbb{R} \oplus dx \mathbb{R}
  \,.
$$

### Functions and differential 1-forms
 {#FunctionsAndForms}

We discussion of [[differential 1-forms]] are functions on the space of infinitesimal paths. For more comprehensive such discussion see ([Stel 13](#Stel13)).

Define the [[smooth locus]] $\mathbb{R}^{(\Delta^1_{inf})}$ as the [[product]] $\mathbb{R} \times D$ of the [[real line]] with the first order [[infinitesimal space|infinitesimal line segment]].
We think of this as the space of **infinitesimal paths** in $\mathbb{R}$ (see [Spaces of infinitesimal k-simplicies](infinitesimal+object#SpacOfInfSimpl)). We do so by thinking of a [[generalized element]] of $\mathbb{R}^{(\Delta^1_{inf})}$ in the category $SmoothLoc$, namely a pair $(x, \epsilon) \in \mathbb{R} \times D$, as the linear path in $\mathbb{R}$ stretching from $x$ to $x + \epsilon$ (both regarded as [[generalized element]]s of $\mathbb{R}$).

We say a **smooth [[differential form|differential 1-form]]** on $\mathbb{R}$ is a function (meaning: a [[morphism]] in $SmoothLoc$)

$$
  \omega : 
  X^{(\Delta^1_{inf})} \to \mathbb{R}
$$

with the property that its restriction to $\mathbb{R}$ vanishes, hence so that the composite morphism

$$
 0 : \mathbb{R} \hookrightarrow X^{(\Delta^1_{inf})} \stackrel{\omega}{\to} \mathbb{R}
$$

vanishes, where the first morphism is the inclusion of $\mathbb{R}$ as the constant infinitesimal paths in $\mathbb{R}$, hence $(Id, 0) : \mathbb{R} \to \mathbb{R} \times D$.


We call the [[coproduct]] of [[smooth algebra]]s their [[tensor product]] (classically it is the _smoothly completed_ algebraic tensor product). For each smooth loci $X$ and $Y$, we have 

$$
  C^\infty(X \times Y) \simeq C^\infty(X) \otimes C^\infty(Y)
  \,.
$$

Using this property, we can dualize the above definition of a diferential 1-form. Namely, in the [[opposite category]] of [[smooth algebra]]s, a 1-form on the line is a morphism

$$
  C^\infty(\mathbb{R}) \otimes \mathbb{R}[dx]/((dx)^2)
   \leftarrow
  C^\infty(\mathbb{R})
  : 
  \omega^*
  \,,
$$

hence an assignment $ x \mapsto g(x) +  h(x) dx $ such that $g(x) = 0$. In other words, it is any element in $C^\infty(\mathrm{R}) \otimes \mathbb{R}[dx]/((dx)^2)$ that is proportional to the generator $dx$. We write $ \omega = h dx $ with $h \in C^\infty(\mathbb{R})$.

### Derivatives as infinitesimal differences

We can now "[[synthetic differential geometry|synthetically]]" describe differentiation as the process of taking infinitesimal differences of functions.

Consider the two morphisms of smooth loci

$$
  + : \mathbb{R}^{(\Delta^1_{inf})} = \mathbb{R} \times D \to \mathbb{R}
$$

and

$$
  p_1 : \mathbb{R}^{(\Delta^1_{inf})} = \mathbb{R} \times D \to \mathbb{R}
  \,,
$$

where the first is the restriction of the canonical addition operation $+ : \mathbb{R} \times \mathbb{R} \to \mathbb{R}$ of [[real number]]s, and where the second is the [[projection]] on the first factor out of the [[product]].

Given an element $f \in C^\infty(\mathbb{R})$, hence a [[smooth function]] $f : \mathbb{R} \to \mathbb{R}$, we can then form two functions on infinitesimal paths by precomposing with these two morphisms:

first we get

$$
 f : X^{(\Delta^1_{inf})} \stackrel{p_1}{\to} \mathbb{R}
   \stackrel{f}{\to} \mathbb{R}
  \,.
$$

This is the function on infinitesimal paths in the line that only depends on the starting point of a path, not on the length of the path, and which sends that starting point to the value of $f$ on that point. Therefore by slight abuse of notation we just keep writing "$f$" for this function.

The second combination is

$$
 \tilde f : X^{(\Delta^1_{inf})} \stackrel{+}{\to} \mathbb{R}
   \stackrel{f}{\to} \mathbb{R}
  \,.
$$

This is the function on infinitesimal paths that sends any path $(x) \to (x + \epsilon)$ to the value of the function on the _endpoint_ $(x + \epsilon)$ of the paths: in terms of these [[generalized element]]s $\tilde f$ is the assignment

$$
  \tilde f : (x , \epsilon) \mapsto f(x + \epsilon)
 \,.
$$

For instance consider the function $f : x \mapsto x^2$. Then 

$$
  \begin{aligned}
   \tilde f : (x, \epsilon) &\mapsto (x + \epsilon)^2
    \\ 
    & = x^2  + 2 x \epsilon + \epsilon^2 
    \\
    & = x^2 + 2 x \epsilon 
   \end{aligned}
   \,.
$$

This is evident, if maybe still somewhat mysterious, in the internal language of the ambient [[smooth topos]] that we keep alluding to, but to make it entirely explicit and concrete notice that the functions here are dually morphisms of smooth algebras

$$
  C^\infty(\mathbb{R}) \otimes (\mathbb{R} \oplus dx \mathbb{R})
  \leftarrow
  C^\infty(\mathbb{R})
  : 
  (\tilde f)^* 
$$

and the equation

$$
  (x + dx)^2 = x^2 + 2 x dx 
$$

holds in $C^\infty(\mathbb{R}) \otimes (\mathbb{R} \oplus dx \mathbb{R})$ by the [above discussion](FunctionsAndForms), where now $x \in C^\infty(\mathbb{R})$ and $dx \in C^\infty(D) = \mathbb{R} \oplus dx \mathbb{R}$ are the two canonical generators.

But notice that the expression $x^2 + 2 x dx $ is not a dfifferential 1-form by the above definition, equivalently the function $\tilde f$ does not vanish when restricted to constant infinitesimal paths.

To get such, we form the **[[derivative]]** or **infinitesimal difference**, the function

$$
  \tilde f - f : X^{(\Delta^1_{inf})} \to \mathbb{R}
$$

that acts on [[generalized element]]s of the space of infinitesimal paths in the line as

$$
  (\tilde f - f) : (x, \epsilon) \mapsto 
   f(x + \epsilon) - f(x)
  \,.
$$

By construction on the right this now is something linear in the infinitesimal length $\epsilon$ of the path. Write $f' \in C^\infty(\mathbb{R})$ for the coefficient:

$$
  f(x + \epsilon) - f(x) = \epsilon f'(x)
  \,.
$$

This function $f'$ is the **[[differential]]** of $f$. It is the function that gives the change of the function $f$ along a "unit infinitesimal path".

Dually, we have a morphism

$$
  C^\infty(\mathbb{R})\otimes (\mathbb{R} \oplus dx \mathbb{R})
  \leftarrow
  C^\infty(\mathbb{R})
  :
  (\tilde f - f)^*
$$

that sends

$$
  x \mapsto f(x + dx) - f(x) = f'(x) dx
  \,.
$$

The 1-form on the right is the [[de Rham differential]] of $f$, usually written

$$
  (d f)(x) = f'(x) dx \in C^\infty(\mathbb{R} \times D)
  \,.
$$ 

### As a map of tangent bundles
 {#InfinitesimalDifferentiationAsAMapOfTangentBundles}

Equivalently we may rephrase this differential $d f$ as a morphism of [[tangent bundles]] $d f \colon T \mathbb{R} \longrightarrow T \mathbb{R}$ as follows.

First, by the [[Kock-Lawvere axiom]] of SDG we have the standard fact that $T \mathbb{R} := \mathbb{R}^D \simeq \mathbb{R} \times \mathbb{R}$. Therefore given a function

$$
  \mathbb{R} \times D \longrightarrow \mathbb{R}
$$

this is by the [[internal hom]]-[[adjunction]] equivalently a function of the form

$$
  \mathbb{R} \longrightarrow \mathbb{R}^D = T \mathbb{R}
  \,.
$$

The condition on the original function makes this [[adjunct]] be a [[section]] of the [[tangent bundle]] of $\mathbb{R}$. This section is $x \mapsto f'(x)$, hence is the derivative of $f$ regarded as a [[tangent vector]] on $\mathbb{R}$. Moreover, since $\mathbb{R}$ is a [[microlinear space]], this induces by rescaling a function

$$
   T \mathbb{R} = \mathbb{R} \times \mathbb{R} \longrightarrow T \mathbb{R}
  \,.
$$

This is the differential of $f$ regarded as a map of tangent bundles.


## Related concepts

* [[product law]], [[chain rule]]

* [[Jacobian matrix]], [[Hessian matrix]], [[extremum]]

* [[partial differentiation]]

* [[Hadamard lemma]], [[Fermat theory]]

* [[derivative of distributions]]

* [[pullback of differential forms]]

* [[tangent space]], [[tangent bundle]]

* [[jet space]], [[jet bundle]], [[metric jet]]


[[!include infinitesimal and local - table]]


## References

### General

The [[Kock-Lawvere axiom]] for the [[axiom|axiomatization]] of differentiation in [[synthetic differential geometry]] was introduced in

* {#Kock77} [[Anders Kock]], _A simple axiomatics for differentiation_,  Mathematica Scandinavica Vol. 40, No. 2 (October 24, 1977), pp. 183-193 ([JSTOR](http://www.jstor.org/stable/24491223))

Another [[synthetic mathematics|synthetic]] formalization of the chain rule in [[differential cohesion|differential]] [[cohesive homotopy type theory]] is given in

* {#Wellen18} [[Felix Wellen]], section 3 of _[[schreiber:thesis Wellen|Cartan Geometry in Modal Homotopy Type Theory]]_ ([arXiv:1806.05966](https://arxiv.org/abs/1806.05966))

Discussion of differential forms as functions on infinitesimal simplices is in 

* {#Stel13} [[Herman Stel]], _Cosimplicial $C^\infty$ rings and the de Rham complex of Euclidean space_ ([arXiv:1310.7407](http://arxiv.org/abs/1310.7407))
 

### History

Discussion of the history of the concept of differentiation, with emphasis on its roots all the way back in [[Zeno's paradoxes of motion]] is in 

* {#Boyer49} Carl Benjamin Boyer, _The history of the Calculus and its conceptual development_, Dover 1949

