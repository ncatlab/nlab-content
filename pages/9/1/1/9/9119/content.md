

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesion
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

In a context of [[synthetic differential geometry]]/[[differential cohesion]] a _reduced object_ is one "without purely infinitesimal extension". 

For instance in the context of [[formal schemes]]/[[formal smooth manifolds]] the reduced objects are the genuine [[schemes]] and the genuine [[smooth manifold]], those without formal extension.

Accordingly, an [[anti-reduced object]] is one consisting entirely of infinitesimal extension, hence is an [[infinitesimally thickened point]].

Beware that reduced objects in general do "contain infinitesimals in between their classical points", in that not every map from an [[anti-reduced object]] into them is necessarily [[constant map|constant]]. The objects "without any infinitesimals" in the sense that all such maps are constant are instead the [[coreduced objects]].

 

## Definition

A context of [[differential cohesion]] is determined by the existence of an [[adjoint triple]] of  [[modalities]]

$$
  \Re \dashv \Im \dashv \&
  \,,
$$

where $\Re$ and $\&$ are [[idempotent monad|idempotent]] [[comonads]] and $\Im$ is an [[idempotent monad]].

A **reduced object** or **reduced type** is one in the [[full subcategory]] defined by the leftmost modality $\Re$. 



## Examples
 {#Examples}

### In smooth differential geometry

Consider the [[Cahiers topos]] 

$$
  \mathbf{H} = Sh(\{\mathbb{R}^n \times Spec(W)\}_{n,W})
$$ 

as a [[categorical semantics|model]] of [[synthetic differential geometry]]/[[differential cohesion]] (where $W$ denotes [[infinitesimally thickened point|Weil algebras]]/[[Artin algebras]]). The sub-topos of reduced obects 

$$
  \mathbf{H}_{reduced} \hookrightarrow \mathbf{H}
$$

is the topos of [[smooth spaces]]

$$
  \mathbf{H}_{reduced} = Sh(\{\mathbb{R}^n\})
  \,.
$$

An object $D \in \mathbf{H}$ with is an [[anti-reduced object]], hence whose reduction coreflection is the [[terminal object]], $\Re(D) \simeq   \ast $ is an _[[infinitesimally thickened point]]_. 

For instance the [[Isbell duality|formal dual]] $D^1 = Spec(\mathbb{R}[\epsilon](\epsilon^2))$ of the [[ring of dual numbers]] is such that its reduction is the point $\Re(D) \simeq \ast$.

Under [[Yoneda embedding]] every [[smooth manifold]] is in $\mathbf{H}_{reduced}$ and is hence a reduced object in $\mathbf{H}$. More generally there are [[formal smooth manifolds]] in $\mathbf{H}$ and they are generally not reduced.

For example for $\Sigma \in SmoothMfd \hookrightarrow \mathbf{H}_{reduced}\hookrightarrow \mathbf{H}$ an ordinary smooth manifold (hence reduced) the object

$$
  \Sigma \times D^1 \in \mathbf{H}
$$

is a [[formal smooth manifold]] which is not reduced. It reduction is 

$$
  \Re(\Sigma\times D^1) \simeq \Sigma
  \,.
$$

In particular the [[real line]] which is the smooth line object of the [[smooth topos]] $\mathbf{H}$

$$
  \mathbb{R}^1 \in \mathbf{H}_{reduced}\hookrightarrow \mathbf{H}
$$

is reduced, $\Re(\mathbb{R}) \simeq \mathbb{R}$.

Observe from these examples that reduced objects do "contain infinitesimal points in between their classical points", which just means that there are non-[[constant map|constant]] morphisms of the form

$$
  D \longrightarrow \Sigma
  \,.
$$

###Contrast between reduced and coreduced objects

The objects $X \in \mathbf{H}$ for which all maps out of anti-reduced objects $D$ are [[constant maps]] are instead the [[coreduced objects]].

The [[coreduced objects]] are the ones with "no infinitesimal behavior", and the reduced objects are the ones "whose infinitesimal behavior is determined by their non-infinitesimal behavior".  A reduced object does contain infinitesimal points; what it lacks are "purely infinitesimal directions" while a coreduced object has no infinitesimal points.
  
### In algebraic geometry

A [[reduced scheme]] is one all whose local [[rings]] of functions have no non-zero nilpotent elements.

## Related concepts

* [[infinitesimal space]], [[infinitesimally thickened point]]

[[!include cohesion - table]]

* [[formally smooth morphism]], [[formally etale morphism]], [[formally unramified morphism]]


[[!redirects reduced objects]]

[[!redirects reduced type]]
[[!redirects reduced types]]

[[!redirects reduced space]]
[[!redirects reduced spaces]]
