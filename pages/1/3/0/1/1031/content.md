+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The _kernel_ of a [[morphism]] is that part of its [[domain]] which is sent to [[zero]].


## Definition

There are various definitions of the notion of kernel, depending on the properties and structures available in the ambient category. We list a few definitions and discuss (in parts) when they are equivalent.

### As a pullback 


+-- {: .num_defn}
###### Definition

In a [[category]] with an [[initial object]] $0$ and [[pullbacks]], the __kernel__ $ker(f)$ of a [[morphism]] $f: A \to B$ is the [[pullback]] $ker(f) \to A$ along $f$ of the unique morphism $0 \to B$

$$
  \array{
    ker(f)
    &\to&
    0
    \\
    {}^{\mathllap{p}}\downarrow && \downarrow
    \\
    A &\stackrel{f}{\to}& B
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

More explicitly, this characterizes the object $ker(f)$ as [[generalized the|the]] object (unique up to unique [[isomorphism]]) that satisfies the following [[universal property]]:

for every object $C$ and every morphism $h : C \to A$ such that $f\circ h = 0$ is the [[zero morphism]], there is a unique morphism $\phi : C \to ker(f)$ such that $h = p\circ \phi$.

=--


### As an equalizer

+-- {: .num_defn}
###### Definition


In a [[category]] with [[zero morphism]]s (meaning: [[enriched category|enriched]] over the [[category of pointed sets]]), [[generalized the|the]] **kernel** $ker(f)$ of a [[morphism]] $f : c \to d$ is, if it exists, the [[equalizer]] of $f$ and the zero morphism $0_{c,d}$.  

=--

### As a weighted limit 

In any category enriched over pointed sets, the kernel of a morphism $f:c\to d$ is the universal morphism $k:a\to c$ such that $f \circ k$ is the basepoint.  It is a [[weighted limit]] in the sense of [[enriched category theory]].  This applies in particular in any (pre)-[[additive category]].

This is a special case of the construction of [[generalized kernels]] in enriched categories.

### As a representing object
 {#AsARepresentingObject}

Let [[Ab]] be the [[category]] of [[abelian groups]]. This has all kernels, in particular (it is the archetypical [[abelian category]]). 

In  every [[Ab]]-[[enriched category]] $A$, for every [[morphism]] $f \colon X\to Y$ in $A$ there is a [[subfunctor]] 

$$ker f \colon A^{op}\to Ab$$

of the [[representable functor]] $hom(-,X)$, defined on [[objects]] by

$$ (ker f)(Z) = ker\big(hom(Z,X)\to hom(Z,Y)\big), $$

where $ker$ on the right-hand side is the kernel in [[Ab]].

If the category is in fact [[preabelian category|preabelian]], $ker f$ is also representable with [[representing object]] $Ker f$. One has to be careful with the [[cokernel]] $Coker f$, which does not represent the functor naive  $coker f$ defined as $(coker f)(Z) = coker\big(hom(Z,X)\to hom(Z,Y)\big)$ in [[Ab]],
which is often not representable at all, even in the simple example of the category of [[abelian groups]].  Instead, as a [[colimit]] construction, one should [[corepresentable functor|co-represent]] another functor, namely, the [[covariant functor]] $Z\mapsto ker\big(hom(Y,Z) \to hom(X,Z)\big)$ (which is a [[quotient object|quotent]] of the corepresentable functor $hom(X,-)$). In short, $Coker f$ is defined by the "double dualization" (passing to [[opposite categories]]) of the kernel in [[Ab]]: $Coker f = (Ker f^{op})^{op}$.  This is a particular case of the dualization involved in defining any [[colimit]] from its corresponding [[limit]].


### In an $(\infty,1)$-category 

The kernel of a morphism in an [[(∞,1)-category]] with $\infty$-categorical [[zero object]] is the [[homotopy pullback]] as in the pullback definition above: the [[homotopy fiber]]. 

See also [[stable (∞,1)-category]].

### Other meanings 

In some fields, the term 'kernel' refers to an [[equivalence relation]] that category theorists would see as a [[kernel pair]].  This is especially important in fields such as [[monoid]] theory where both notions exist but are not equivalent (while in [[group]] theory they are equivalent).

In [[ring]] theory, even when one assumes that rings have units preserved by ring homomorphisms, the traditional notion of kernel (an [[ideal]]) exists in the category of non-unital rings (and is not itself a unital ring in general).  A purely category-theoretic theory of unital rings can be recovered either by using the kernel pair instead or (to fit better the usual language) moving to a category of [[modules]].

In [[universal algebra]], this may be handled in the framework of [[Malcev variety|Mal'cev varieties]].

Kashiwara-Schapira, following the terminology of EGA, uses kernel as a synonym of equalizer (and co-kernel of co-equalizer).

## Properties {#Properties}

+-- {: .num_prop}
###### Property

Let $C$ be a category with [[pullback]]s and [[zero object]].

In $C$, the kernel of a kernel is 0.

=--

+-- {: .proof}
###### Proof

By the <a href="http://nlab.mathforge.org/nlab/show/pullback#Pasting">pasting law for pullbacks</a> we have that the total square

$$
  \array{
     ker ker f &\to& ker f  &\to& 0
     \\
     \downarrow && \downarrow && \downarrow
     \\
     0 &\to& c &\stackrel{f}{\to}& d
  }
$$

is a pullback. Since $0 \to c$ is a [[monomorphism]] and the pullback of a monomorphism along itself is the domain of the monomorphis, we have $ker ker f \simeq 0$.


=--

+-- {: .num_remark}
###### Remark

This statement crucially fails to be true in [[higher category theory]]. There, the kernel of a kernel is the based [[loop space object]] of $d$. For this reason where one has [[short exact sequence]]s in 1-category theory, there are instead long [[fiber sequence]]s in higher category theory.

=--

+-- {: .num_prop}
###### Proposition

In a category $C$ with [[pullback]]s and [[pushout]]s and [[zero object]], kernel and [[cokernel]] form a pair of [[adjoint functor]]s on the [[arrow category|arrow categories]]

$$
  (coker \dashv ker) : Arr(C) \stackrel{\overset{coker}{\leftarrow}}{\underset{ker}{\to}} Arr(C)
  \,.
$$

=--

+-- {: .proof}
###### Proof


We check the hom-isomorphism of a pair of [[adjoint functor]]s. An element in the [[hom-set]] $Arr_C(g,ker f)$ is a [[diagram]]

$$
  \array{
     c &\to& ker(f) &\to& 0
     \\
     {}^{\mathllap{g}}\downarrow && \downarrow && \downarrow
     \\
     d &\to& a &\stackrel{f}{\to}& b
  }
  \,.
$$

By the universal property of the [[pullback]], this is the same as a diagram

$$
  \array{
     c  &\to& &\to& 0
     \\
     {}^{\mathllap{g}}\downarrow && && \downarrow
     \\
     d &\to& a &\stackrel{f}{\to}& b
  }
  \,.
$$

By the dual reasoning, an element in $Arr_C(coker g, f)$ is a diagram

$$
  \array{
    c &\stackrel{g}{\to}& d &\to& a
    \\
    \downarrow && \downarrow && \downarrow^{\mathrlap{f}}
    \\
    0 &\to& coker g &\to& b
  }
  \,.
$$

By the universal property of the [[pushout]] this is equivalently a diagram

$$
  \array{
    c &\stackrel{g}{\to}& d &\to& a
    \\
    \downarrow &&  && \downarrow^{\mathrlap{f}}
    \\
    0 &\to&  &\to& b
  }
  \,.
$$

=--

(This also follows from the general theory of [[generalized kernels]].)

## Examples

+-- {: .num_example}
###### Example

In the [[category]] [[Ab]] of abelian groups, the kernel of a [[group homomorphism]] $f : A \to B$ is the [[subgroup]] of $A$ on the set $f^{-1}(0)$ of elements of $A$ that are sent to the zero-element of $B$.

=--

+-- {: .num_example}
###### Example


More generally, for $R$ any [[ring]], this is true in $R$[[Mod]]: the kernel of a morphism of modules is the [[preimage]] of the zero-element at the level of the underlying sets, equipped with the unique sub-module structure on that set.

=--

## Related concepts

* **kernel**, [[fiber]], [[generalized kernel]]

* [[homotopy fiber]]

* [[cokernel]]


[[!redirects kernels]]