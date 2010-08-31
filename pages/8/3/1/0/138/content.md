
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _hypercover_ is the generalization of a [[Cech nerve]] of a [[cover]].

## Definition

For $C$ a [[site]] and $[C^{op}, sSet]$ the category of [[simplicial presheaves]] on $C$, a morphism $(Y \to X) \in [C^{op}, sSet]$ with $X$ a [[representable functor|representable]] is called a **hypercover** if

1. $Y$ is degreewise a [[coproduct]] of [[representable functor|representables]],

   $Y = \int^{[n] \in \Delta} \Delta[n] \cdot \coprod_{i_n} U_{i_n} \;\,,
    \;\;\; with \{U_{i_n} \in C\}$ ;

1. with $Y \to X$ regarded as a presheaf of [[augmented simplicial set]]s, for all $n \in \mathbb{N}$ the morphism $Y_{n+1} \to (\mathbf{cosk}_n Y)_{n+1}$ into the $n+1$-cells of the $n$-[[coskeleton]] is a [[local epimorphism]] with respect to the given [[Grothendieck topology]] on $C$.

The local epimorphisms here are 

* in degree 0: $Y_0 \to X$;

* in degree 1: $Y_1 \to Y_0 \times_X Y_0$

* and so on.

A hypercover is called **bounded** by $n \in \mathbb{N}$ if for all $k \geq n$ the morphisms $Y_{k+1} \to (\mathbf{cosk}_{n})_{k+1}$ are [[isomorphism]]s.

The smallest $n$ for which this holds is called the **height** of the hypercover.

A hypercover that also satisfies a cofibrancy condition in the projective [[local model structure on simplicial presheaves]] is called a **[[split hypercover]] (see there for details).

## Examples

For $U = \{U_i \to X\}$ a [[cover]], the [[Cech nerve]] projection $C(U) \to X$ is a hypercover of height 0.


## Properties

### Hypercover homology {#HypercoverHomology}

Let $f : Y \to X$ be a hypercover. We may regard this as an object in the [[overcategory]] $Sh(C)/X$. By the discussion <a href="http://ncatlab.org/nlab/show/category+of+presheaves#RelWithOvercategories">here</a> this is equivalently $Sh(C/Y)$. Write $Ab(Sh(C/Y))$ for the category of abelian [[group object]]s in the [[sheaf topos]] $Sh(C/Y)$. This is an [[abelian category]].

Forming in the sheaf topos the [[free functor|free]] abelian group on $f_n$ for each $n \in \mathbb{N}$, we obtain a simplicial abelian group object $\bar f \in Ab(Sh(C/X))^{\Delta}$. As such this has a [[Moore complex|normalized chain complex]] $N_\bullet(\bar f)$.

+-- {: .un_prop}
###### Proposition

For $f : Y \to X$ a hypercover, the [[chain homology]] of $N(\bar f)$ vanishes in positive degree and is the group of [[integer]]s in degree 0, as an object in $Ab(Sh(C)(X)$:

$$
  H_p(N(f)) \simeq 
  \left\{
    \array{
       0 & for \; p \geq 1
       \\
       \mathbb{Z} & for \; p = 0
    }
  \right.
  \,.
$$

=--


## Reference


A thorough discussion is given in 

* [[Daniel Dugger]], [[Sharon Hollander]], [[Daniel Isaksen]], _Hypercovers and simplicial presheaves_ ([web](http://www.math.uiuc.edu/K-theory/0563/))

See also the remark at the end of section 2, on p. 6 of

* Jardine, _Fields Lectures: Simplicial presheaves_ ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))


[[!redirects hypercovers]]