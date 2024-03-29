+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(\infty,1)$-Topos Theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

An **$n$-connected object** is an object all whose [[homotopy group]]s _equal to or below_ degree $n$ are trivial.

More precisely, an object in an [[∞-stack]] [[(∞,1)-topos]] is $n$-connected if its [[homotopy groups in an (∞,1)-topos|categorical homotopy groups]] equal to or below degree $n$ are trivial.

The complementary notion is that of an [[n-truncated object of an (∞,1)-category]].

The [[Whitehead tower]] construction produces $n$-connected objects.


## Definition
 {#Definition}

+-- {: .num_defn #Connectedness}
###### Definition

An [[object]] $X$ in an [[(∞,1)-topos]] $\mathbf{H}$ is called **$n$-connected** for $ -1 \leq n \in \mathbb{Z}$ if

1. the [[terminal object|terminal]] morphism $X \to *$ is an [[effective epimorphism in an (infinity,1)-category|effective epimorphism]];

1. all [[homotopy groups in an (∞,1)-topos|categorical homotopy groups]]
   equal to or below degree $n$ are trivial.

   $$
     \pi_k(X) = * \;\;\; \text{for} \; k \leq n
     \,.
   $$
  
A [[morphism]] $f : X \to Y$ in an $(\infty,1)$-topos is called **$n$-connected** if 

1. it is an [[effective epimorphism in an (∞,1)-category]]

1. regarded as an object in the 
   [[over quasi-category|over-(∞,1)-category]] 
   $\mathbf{H}_{/Y}$ all [[homotopy groups in an (∞,1)-topos|categorical homotopy groups]]
   equal to or below degree $n$ are trivial.

=--

This appears as [[Higher Topos Theory|HTT, def. 6.5.1.10]], but under the name "[[n-connective object|$(n+1)$-connective]]".  Another possible term is "$n$-simply connected"; see [[n-connected space]] for discussion.

One adopts the following convenient terminology.

* Every object is $(-2)$-connected.

* A $(-1)$-connected object is also called an [[inhabited object]].

* A 0-connected object is simply called a **connected object**.

Notice that [[effective epimorphism in an (∞,1)-category|effective epimorphisms]] are precisely the $(-1)$-connected morphisms. For more on this see _[[n-connected/n-truncated factorization system]]_.



## Properties
 {#Properties}

### General
 {#PropertiesGeneral}

+-- {: .num_prop #ConnectednessViaTruncationComodalness}
###### Proposition

An object $X$ is $n$-connected, def. \ref{Connectedness}, precisely if its [[n-truncated object in an (∞,1)-category|n-truncation]] $\tau_{\leq n} X$ is [[generalized the|the]] [[terminal object]] of $\mathbf{H}$ (hence precisely if it is $\tau_{\leq n}$-[[comodal type|comodal]]).

=--

This is [[Higher Topos Theory|HTT, prop. 6.5.1.12]].

\begin{lemma}
Every [[equivalence in a quasi-category|equivalence]] is $\infty$-connected.
\end{lemma}

This is [[Higher Topos Theory|HTT, prop. 6.5.1.16, item 2]].

+-- {: .num_remark}
###### Remark

In a general $(\infty,1)$-topos the converse is not true: not every $\infty$-connected morphisms needs to be an equivalence. It is true in a [[hypercomplete (∞,1)-topos]].
=--


+-- {: .num_prop}
###### Proposition

The class of $n$-connected morphisms is stable under [[pullback]] and [[pushout]].

If the pullback of a morphism along an [[effective epimorphism]] is $n$-connected, then so is the original morphism.

=--

This is [[Higher Topos Theory|HTT, prop. 6.5.1.16, item 6]].

### Recursive characterization
 {#RecursiveCharacterization}

+-- {: .num_prop #CharacterizationByDiagonal}
###### Proposition

A morphism $f : X \to Y$ is $n$-connected precisely if it is 
an [[effective epimorphism in an (infinity,1)-category|effective epimorphism]] and the [[diagonal]] morphism into the [[(∞,1)-pullback]]

$$
  \Delta_f : X \to X \times_Y X
$$

is $(n-1)$-connected.

=--

This appears as [[Higher Topos Theory|HTT, prop. 6.5.1.18]].

### Factorization system

+-- {: .num_prop}
###### Proposition

Let $\mathbf{H}$ be an [[(∞,1)-topos]]. For all $(-2) \leq n \leq \infty$ the [[class]] of $n$-connected morphisms in $\mathbf{H}$ forms the left class in a [[orthogonal factorization system in an (∞,1)-category]]. The right class is that of [[n-truncated]] morphisms in $\mathbf{H}$.

=--

See also [[n-connected/n-truncated factorization system]].

This appears as a remark in [[Higher Topos Theory|HTT, Example 5.2.8.16]]. A construction of the factorization in terms of a [[model category]] [[presentable (∞,1)-category|presentation]] is in ([Rezk, prop. 8.5](#Rezk)).

### Blakers-Massey theorem

* [[Blakers-Massey theorem]]

### The truncated / connected clock
 {#Clock}


In a [[hypercomplete (∞,1)-topos]] the $\infty$-connected morphisms are precisely the [[equivalence in an (∞,1)-category|equivalences]].

Therefore in such a context we have the following "clock" of notions of [[truncated object in an (infinity,1)-category]] / connected :

* any morphism = $(-2)$-connected

* [[effective epimorphism in an (∞,1)-category|effective epimorphism]] = $(-1)$-connected

* 0-connected, 1-connected, 2-connected, $\cdots$;

* $\infty$-connected = [[equivalence in an (∞,1)-category|equivalence]] = $(-2)$-truncated

* [[monomorphism in an (∞,1)-category|monomorphism]] = $(-1)$-truncated

* 0-truncated, 1-truncated, 2-truncated, $\cdots$

* $\infty$-truncated = any morphism

## Examples


### In $Top$
 {#InTop}

In the the [[(∞,1)-category]] $L_{whe}$[[Top]] we have that an object is $n$-connected precisely if it is an [[n-connected topological space]]:

* a $(-1)$-connected object is an [[inhabited set|inhabited space]].

* a $0$-connected object is a [[path-connected space]].

* a $1$-connected object is a [[simply connected space]].

* a $\infty$-connected object is a [[contractible space]].

More generally, a continuous function represents an $n$-connected morphism in $L_{whe} Top$ precisely if it is an [[n-connected continuous function]] ("[[n-equivalence]]").

### In $Grpd$
 {#ExamplesInGrpd}

+-- {: .num_prop}
###### Proposition

Let $f : X \to Y$ be a [[functor]] between [[groupoids]].
Regarded as a morphism in [[∞Grpd]] $f$ is 0-connected precisely
if it is an [[essentially surjective and full functor]].

=--

+-- {: .proof}
###### Proof

As discussed there, an [[effective epimorphism in an (∞,1)-category|effective epimorphism]] in [[∞Grpd]] between 1-groupoids is precisely an
[[essentially surjective functor]].

So it remains to check that for an essentially surjective $f$, being
0-connected is equivalent to being full.

The [[homotopy pullback]] $X \times_Y X$ is given by the groupoid 
whose objects are triples $(x_1, x_2 \in X, \alpha : f(x_1) \to f(x_2))$
and whose morphisms are corresponding tuples of morphisms in $X$ making the
evident square in $Y$ commute.

By prop. \ref{CharacterizationByDiagonal} 
it is sufficient to check that the [[diagonal]] functor $X \to X \times_Y X$ is
(-1)-connected, hence, as before, essentially surjective, precisely if $f$ is full.
 
First assume that $f$ is full. 
Then for $(x_1,x_2, \alpha) \in X \times_Y X$
any object, by [[full functor|fullness]] of $f$ 
there is a morphism $\hat \alpha : x_1 \to x_2$ in $X$,
such that $f(\hat \alpha) = \alpha$.

Accordingly we have a morphism
$(\hat \alpha,id) : (x_1, x_2) \to (x_2, x_2)$ in $X \times_Y X$ 

$$
  \array{
     f(x_1) &\stackrel{f(\hat \alpha)}{\to}& f(x_2)
     \\
     \downarrow^{\mathrlap{\alpha}} && \downarrow^{\mathrlap{id}}
     \\
     f(x_2) &\stackrel{id}{\to}& f(x_2)
  }
$$

to an object in the diagonal.

Conversely, assume that the diagonal is essentially surjective. Then 
for every pair of objects $x_1, x_2 \in X$ such that there is a morphism
$\alpha : f(x_1) \to f(x_2)$ we are guaranteed morphisms
$h_1 : x_1 \to x_2$ and $h_2 : x_2 \to x_2$ such that 

$$
  \array{
    f(x_1) &\stackrel{f(h_1)}{\to}& f(x_2)
    \\
    \downarrow^{\mathrlap{\alpha}} && \downarrow^{\mathrlap{id}}
    \\
    f(x_2) &\stackrel{f(h_2)}{\to}& f(x_2)
  }
  \,.
$$

Therefore $h_2^{-1}\circ h_1$ is a preimage of $\alpha$ under $f$,
and hence $f$ is full.

=--

See also [[(eso+full, faithful) factorization system]].

## Related concepts

* [[n-truncated object in an (infinity,1)-category]]

* [[n-connective object]]

* [[Eilenberg subcomplex]]

* [[connective spectrum]], [[connective cover]]

* [[Freudenthal suspension theorem]]

* [[Blakers-Massey theorem]]

## References

Section 6.5.1 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

A discussion in terms of [[model category]] [[presentable (∞,1)-category|presentations]] is in section 8 of

* [[Charles Rezk]], _Toposes and homotopy toposes_ ([pdf](http://www.math.uiuc.edu/~rezk/homotopy-topos-sketch.pdf))


[[!redirects (-2)-connected]]
[[!redirects (-1)-connected]]
[[!redirects 0-connected]]
[[!redirects 1-connected]]

[[!redirects 2-connected]]
[[!redirects 3-connected]]
[[!redirects 4-connected]]
[[!redirects 5-connected]]
[[!redirects ∞-connected]]


[[!redirects n-connected]]




[[!redirects n-connected object]]


[[!redirects n-connected objects]]
[[!redirects n-simply connected object]]
[[!redirects n-simply connected objects]]

[[!redirects n-connected object in an (∞,1)-topos]]
[[!redirects n-connected object in an (infinity,1)-topos]]
[[!redirects n-connected object of an (∞,1)-topos]]
[[!redirects n-connected objects of an (∞,1)-topos]]
[[!redirects n-connected objects of (∞,1)-toposes]]
[[!redirects n-connected objects of (∞,1)-topoi]]
[[!redirects n-connected object of an (infinity,1)-topos]]
[[!redirects n-connected objects of an (infinity,1)-topos]]
[[!redirects n-connected objects of (infinity,1)-toposes]]
[[!redirects n-connected objects of (infinity,1)-topoi]]
[[!redirects n-simply connected object of an (∞,1)-topos]]
[[!redirects n-simply connected objects of an (∞,1)-topos]]
[[!redirects n-simply connected objects of (∞,1)-toposes]]
[[!redirects n-simply connected objects of (∞,1)-topoi]]
[[!redirects n-simply connected object of an (infinity,1)-topos]]
[[!redirects n-simply connected objects of an (infinity,1)-topos]]
[[!redirects n-simply connected objects of (infinity,1)-toposes]]
[[!redirects n-simply connected objects of (infinity,1)-topoi]]

[[!redirects n-connected object of an (∞,1)-category]]
[[!redirects n-connected objects of an (∞,1)-category]]
[[!redirects n-connected objects of (∞,1)-categories]]
[[!redirects n-connected object of an (infinity,1)-category]]
[[!redirects n-connected objects of an (infinity,1)-category]]
[[!redirects n-connected objects of (infinity,1)-categories]]

[[!redirects n-simply connected object of an (∞,1)-category]]
[[!redirects n-simply connected objects of an (∞,1)-category]]
[[!redirects n-simply connected objects of (∞,1)-categories]]
[[!redirects n-simply connected object of an (infinity,1)-category]]
[[!redirects n-simply connected objects of an (infinity,1)-category]]
[[!redirects n-simply connected objects of (infinity,1)-categories]]

[[!redirects n-connected morphism of an (∞,1)-category]]
[[!redirects n-connected morphisms of an (∞,1)-category]]
[[!redirects n-connected morphisms of (∞,1)-categories]]
[[!redirects n-connected morphism of an (infinity,1)-category]]
[[!redirects n-connected morphisms of an (infinity,1)-category]]
[[!redirects n-connected morphisms of (infinity,1)-categories]]

[[!redirects n-connected morphism of an ∞,1-category]]
[[!redirects n-connected morphisms of an ∞,1-category]]
[[!redirects n-connected morphisms of ∞,1-categories]]
[[!redirects n-connected morphism of an infinity,1-category]]
[[!redirects n-connected morphisms of an infinity,1-category]]
[[!redirects n-connected morphisms of infinity,1-categories]]


[[!redirects connected object in an infinity-topos]]
[[!redirects connected object of an infinity-topos]]
[[!redirects n-connected object of an infinity-topos]]
[[!redirects n-connected object of an infinity1-topos]]


[[!redirects connected object in an (infinity,1)-category]]
[[!redirects connected object in an (∞,1)-category]]
[[!redirects connected object in an (infinity,1)-topos]]
[[!redirects connected object in an (∞,1)-topos]]

[[!redirects 0-connected morphism]]
[[!redirects 0-connected morphisms]]


[[!redirects n-connected morphism]]
[[!redirects n-connected morphisms]]


[[!redirects connectivity]]

