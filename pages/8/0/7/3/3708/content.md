

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

+-- {: .un_defn}
###### Definition

For $C = $ [[CRing]] we have $T_C \simeq $ [[Mod]]. 

=--

+-- {: .proof}
###### Proof

At [[module]] it is described that for a fixed ring $R$ the functor

$$
  Mod_R \to Ab(CRing/R)
$$

that sends an $R$-module to its square-0-extension $R \oplus N \stackrel{p_1}{\to} R$, regarded as an abelian group object in $CRing/R$ is an [[equivalence of categories]]. 

So we need to check that this fiberwise equivalence extends to respect the morphisms in $T_C$ that have nontrivial projection to $C$.

If $(R_1,N_1)$ and $(R_2,N_2)$ are two objects in [[Mod]], then a morphism between them is a pair $(f : R_1 \to R_2, f_*:N_1 \to f^* N_2)$ consisting of a ring homorphism and a morphism of $R_1$ modules from $N_1$ to $R_1 \otimes_f N_2$.

For this to coincide with the definition of morphisms in $T_{CRing}$ above, we need to check that the diagram

$$
  \array{
    R_1 \oplus (R_1 \otimes_{R_2} N_2)  &\to& R_2 \oplus N_2
    \\
    \downarrow && \downarrow
    \\
    R_1 &\stackrel{f}{\to}& R_2
  }
$$

is a [[pullback]] diagram in [[CRing]].

We have that the elements of the pullback ring $R_1 \times_f (R_2 \oplus N_2)$ consists of the triples $(r_1, r_2, n)$ with $r_i \in R_i$ and $n \in N$ such that $f(r_1) = r_2$. So this is just as well encoded in terms of tuples $(r_1, n)$, with no condition and so we find that as an underlying ordinary group the pullback ring is $(R_1 \oplus N)$. 

But also the underlying group of the tensor product $(R_1 \otimes_{R_2} N)$ is just $(R_1 \oplus N)$, because the former consists of tuples $(r_1,n)$ that are each respectively identified with the tuple $(1, f(r_1) n)$, so that the underlying group may be taken to consist of the tuples $(1,n)$.

So it just remains to check that the multiplicative structure of the pullback ring is that of $(R_1 \oplus (R_1 \otimes_{f} N))$. The product structure on the former is

$$
  (r_1, (f(r_1), n)) \cdot (r'_1, (f(r'_1), n'))
  =
  (r_1 \cdot r'_2, (f(r_1 \cdot r_2), f(r_1) n' + f(r_2)n))
  \,,
$$

(where we used that $f$ is a ring homomorphism) and under the above identifications this indeed coincides with the ring structure on the square-0-extension $R_1 \oplus (R_1 \otimes_{f} N)$.

=--

_Second version_

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

