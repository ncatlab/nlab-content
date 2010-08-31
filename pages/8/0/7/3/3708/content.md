
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of **tangent category** of a [[category]] $C$ is an approximation to the notion of [[tangent (∞,1)-category]] in ordinary [[category theory]]. 

For the moment see there for further motivation.

The tangent category $T_C$ of $C$ is effectively the _fiberwise abelianization_ of the [[codomain fibration]] $cod : [I,C] \to C$:

we may think of it as obtained from the codomain fibration by replacing each [[overcategory]] fiber $[I,C]_A = C/A$ by the corresponding category of abelian [[group object]]s and restricting the morphisms such as to respect the abelian group object structure.

## Definition

Let $C$ be a [[category]] with [[pullback]]s. Then the **tangent category** $T_C$ of $C$ is the category whose

* [[object]]s are pairs $(A,\mathcal{A})$ with $A \in Ob(C)$ and with $\mathcal{A}$ an abelian [[group object]] in the [[overcategory]] $C/B$;

  notice that for $\mathcal{B} \to B$ an object in the overcategory that is equipped with the structure of an abelian group object -- notably with a product $prod_{\mathcal{B}} : \mathcal{B} \times_B \mathcal{B} \to  \mathcal{B}$ -- and for $f : A \to B$ any morphism in $C$, the [[pullback]] $f^* \mathcal{B} := A \times_B \mathcal{B}$ in $C$ is naturally equipped with the structure of an abelian group object in $C/A$;
  

* [[morphism]]s $(f, \mathcal{f}) : (A,\mathcal{A}) \to (B, \mathcal{B})$ are commuting squares

  $$
    \array{
      \mathcal{A} &\stackrel{\mathcal{f}}{\to}& \mathcal{B}
      \\
      \downarrow && \downarrow 
      \\
      A &\stackrel{f}{\to}& B
    }
  $$

  such that the induced morphism $\mathcal{A} \to f^*\mathcal{B}$ is a morphism of abelian group objects in $C/A$; 

* composition of morphisms is given in the evident way by $(f_2, \mathcal{f}_2) \circ (f_1, \mathcal{f}_1) = (f_2 \circ f_1, \mathcal{f}_2 \circ \mathcal{f}_1) $.

## Properties

There is an evident [[functor]] $p : T_C \to C$, the underlying [[codomain fibration]]:

$$
  p 
  \;\;:
  \;\; 
  \left(
    \array{
      \mathcal{A} &\stackrel{\mathcal{f}}{\to}& \mathcal{B}
      \\
      \downarrow && \downarrow
      \\
      A &\stackrel{f}{\to}& B
    }
  \right)
  \;\;
  \mapsto
  \;\;
  (A \stackrel{f}{\to} B)
  \,.
$$

The fiber over $Id_A$ of this functor is the category of abelian group objects in the [[overcategory]] $C/A$:

$$ 
  (T_C)_A \simeq Ab(C/A)
  \,.
$$

There is also another functor $q : T_C \to C$, inherited from the [[domain cofibration]]

$$
  q 
  \;\;:
  \;\; 
  \left(
    \array{
      \mathcal{A} &\stackrel{\mathcal{f}}{\to}& \mathcal{B}
      \\
      \downarrow && \downarrow
      \\
      A &\stackrel{f}{\to}& B
    }
  \right)
  \;\;
  \mapsto
  \;\;
  (\mathcal{A} \stackrel{\mathcal{f}}{\to} \mathcal{B})
  \,,
$$

where we first forget the abelian group object structure and then project onto the domains.


> (we should be claiming that this functor has a left adjoint which is a section and computes the [[cotangent complex]]es of objects in $C$).


## Examples

### Modules as tangents to rings

+-- {: .un_prop}
###### Proposition

For $C = $ [[CRing]] we have $T_C \simeq $ [[Mod]]. 

=--

+-- {: .proof}
###### Proof

Consider the functor
$$
 F: Mod \to T_{CRing}
$$

that sends an $R$-module $N$ to the square-0-extension ring $R \oplus N \stackrel{p_1}{\to} R$, regarded as an abelian group object in $CRing/R$.

The action on morphisms is given as follows: if $(R_1,N_1)$ and $(R_2,N_2)$ are two objects in [[Mod]], then a morphism between them is a pair $(f : R_1 \to R_2, f_*:N_1 \to f^* N_2)$ consisting of a ring homorphism and a morphism of $R_1$ modules from $N_1$ to $R_1 \otimes_f N_2$; the corresponding morphism of rings $R_1\oplus N_1\to R_2\oplus N_2$ is $(r_1,n_1)\mapsto (f(r_1),f_*(n_2))$. The induced morphism of rings $R_1\oplus N_1\to R_1\times_{R_2}(R_2\oplus N_2)\cong R_1\oplus f^*N_2$ is explicitly given by $(r_1,n_1)\mapsto (r_1,f_*(n_1))$ and is easily checked to be a morphism of abelian group objects over $R_1$.

Moreover, by the natural isomorphism $R_1\times_{R_2}(R_2\oplus N_2)\cong R_1\oplus f^*N_2$ in $Ab(CRing/R)$, showing that $F:Mod\to T_{CRing}$ is an equivalence is reduced to showing that $F$ is a fibrewise equivalence, i.e., that that for any fixed ring $R$,

$$
F_R:  Mod_R \to Ab(CRing/R)
$$

is an [[equivalence of categories]]. This is shown at [[module]].

=--

### Modules over smooth algebras

Let $SmoothAlg$ (or $C^\infty Ring$) be the category of [[smooth algebra]]s. Notice that there is a canonical [[forgetful functor]]

$$
  U : SmoothAlg \to Ring
$$

to the underlying ordinary [[ring]]s.

+-- {: .un_prop}
###### Proposition

There is an [[equivalence of categories]]

$$
  T_{SmoothAlg} \stackrel{\simeq}{\to}
  SmoothAlg \times_{Ring} T_{Ring}
  \,,
$$

where on the right we have the strict [[pullback]] (i.e. taken in the 1-category [[Cat]]).

=--

We give the proof below. First some remarks and corollaries.

+-- {: .un_remark}
###### Remark

We may regard an object in $T_{SmoothAlg}$ as a module over a [[smooth algebra]]. The above says in particular that modules over smooth algebras are just modules over the underlying ordinary rings. However, the category structure on $T_{SmoothAlg}$ does reflect that modules over smooth algebras have a different nature than just bare modules, notably in that the left adjoint to the projection $T_{SmoothAlg} \to SmoothAlg$ produces the correct $C^\infty$-[[derivation]]s and $C^\infty$-[[Kähler differential]]s (see there) as opposed to the purely algebraic ones.
 
=--

+-- {: .un_cor}
###### Corollary

For any category $S$ we have that 

$$
  (T_{SmoothAlg})^S \simeq
  SmoothAlg^S \times_{Ring^S} (T_{Ring})^S
  \,.
$$

So in particular for $S = \Delta$ the [[simplex category]] we have that [[simplicial object|simplicial]] modules over simplicial smooth algebras are as objects just ordinary simplicial modules over the underlying [[simplicial ring]]s.

=--


+-- {: .proof}
###### Proof

The statement was suggested at some point by [[Thomas Nikolaus]] in discussion with [[Urs Schreiber]], who then asked [[Herman Stel]] to prove it. A writeup is in ([Stel](#Stel)).

(...)


=--


## In higher category theory

See [[tangent (infinity,1)-category]].

## References

The original observation that $T_{Ring} \simeq Mod$ is due to

* Quillen, ...

A discusson of $T_{SmoothAlg}$ is in 

* [[Herman Stel]], _[[schreiber:master thesis Stel|∞-Stacks and their Function Algebras]]_ 
{#Stel}