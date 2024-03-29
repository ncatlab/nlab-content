
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _cocommutative [[coalgebra]]_ is the formal [[duality|dual]] of [[commutative algebra]].

Cocommutative coalgebras form the [[category]] [[CocommCoalg]].

## Definition

For $(C,\otimes, I, \sigma)$ a [[symmetric monoidal category]], a [[comonoid object]] in $C$ is an [[object]] $A$ equipped with a [[morphism]]

$$
  \Delta : A \to A \otimes A
$$

("[[comultiplication]]") and a morphism 

$$
  \varepsilon: A \to I
$$

("[[counit]]") that satisfy the [[coassociativity]] and [[counitality]] equations: 

$$
  \array{
     A &\stackrel{\Delta}{\to}& A \otimes A
     \\
     ^\mathllap{\Delta} \downarrow && \downarrow^{\mathrlap{Id \otimes \Delta}}
     \\
     A \otimes A &\underset{\Delta \otimes Id}{\to}&
     A \otimes A \otimes A
  }
\qquad \qquad \qquad 
  \array{
     & & A & & 
     \\
     & ^\mathllap{Id} \swarrow & \downarrow^\mathrlap{\Delta} & \searrow^\mathrlap{Id} & 
     \\
     A & \underset{Id \otimes \varepsilon}{\leftarrow} & A \otimes A & \underset{\varepsilon \otimes Id}{\to} & A 
   }     
  \,.
$$

This is **co-commutative** if we have a [[commuting diagram]]

$$
  \array{
    && A \otimes A
    \\
    & {}^{\mathllap{\Delta}}\nearrow && \searrow^\mathrlap{\sigma_{A,A}}
    \\
    A  &&\underset{\Delta}{\to}&& A \otimes A
  }
  \,,
$$ 

where $\sigma_{A,A} : A \otimes A \to A \otimes A$ is the [[braiding]] [[isomorphism]] of $C$.

In the case of the symmetric monoidal category of [[module|modules]] over a [[commutative ring]] $R$, such an object is called a **cocommutative coalgebra** over $R$. In the case of the symmetric monoidal category of [[chain complex|chain complexes]] (or differential graded spaces), such an object is called a **DG coalgebra**. 

Sometimes "cocommutative coalgebra" in a symmetric monoidal category is used as a synonym for cocommutative comonoid object. We will follow that convention below. If $M$ is symmetric monoidal, then $CocommCoalg(M)$ denotes the category of cocommutative algebras and coalgebra maps in $M$. 

## Relation to cartesian monoidal categories 

Cocommutative coalgebras form a bridge between the [[doctrine|doctrines]] of symmetric monoidal categories and [[cartesian monoidal category|cartesian monoidal]] categories. Notice that every object in a cartesian monoidal category carries a unique cocommutative comonoid structure (the counit is the unique map to the terminal object, and the counicity equations then force the comultiplication map to be the diagonal), and every morphism in a cartesian monoidal category is thereby a coalgebra map. 

If $C$ and $D$ are two cocommutative coalgebras, then $C \otimes D$ becomes a cocommutative coalgebra with comultiplication 

$$C \otimes D \stackrel{\Delta_C \otimes \Delta_D}{\to} C \otimes C \otimes D \otimes D \stackrel{Id \otimes \sigma \otimes Id}{\to} C \otimes D \otimes C \otimes D$$ 

and counit 

$$C \otimes D \stackrel{\varepsilon_C \otimes \varepsilon_D}{\to} I \otimes I \cong I.$$ 

+-- {: .un_prop} 
###### Proposition 
$C \otimes D$ is the cartesian product of $C$ and $D$ in $CocommCoalg(M)$. 
=-- 

+-- {: .un_theorem}
###### Theorem 
The forgetful 2-functor 

$$U: CartMonCat \to SymMonCat,$$ 

from cartesian monoidal categories and product-preserving functors to symmetric monoidal categories and strong symmetric monoidal functors, is coreflective. That is to say, it has a right [[biadjunction|bi-adjoint]] which sends $M$ to $CocommCoalg(M)$, and the unit of the 2-adjunction is an equivalence. 
=-- 

+-- {: .un_cor}
###### Corollary 
The 2-category of cartesian monoidal categories is comonadic (in the bicategorical sense) over the 2-category of symmetric monoidal categories. 
=-- 

## Related concepts

* [[comonoid object]]

* [[monoid]], [[commutative monoid]], [[category of monoids]]

* [[gs-monoidal category]]



[[!redirects cocommutative]]
[[!redirects cocommutativity]]
[[!redirects co-commutative]]
[[!redirects co-commutativity]]


[[!redirects cocommutative coalgebras]]
[[!redirects co-commutative coalgebra]]
[[!redirects co-commutative coalgebras]]

[[!redirects cocommutative comonoid]]
[[!redirects cocommutative comonoids]]

