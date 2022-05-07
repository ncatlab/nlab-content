
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A _monoidal functor_ is a [[functor]] between [[monoidal categories]] that preserves the monoidal structure: a [[homomorphism]] of monoidal categories.

## Definition ##


+-- {: .num_defn #LaxMonoidalFunctor}
###### Definition

Let $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ be two [[monoidal categories]]. A **lax monoidal functor** between them is

1. a [[functor]] 

   $$
     F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}
     \,,
   $$

1. a morphism

   $$
     \epsilon \;\colon\; 1_{\mathcal{D}} \longrightarrow F(1_{\mathcal{C}})
   $$  

1. a [[natural transformation]]

   $$
     \mu_{x,y} 
       \;\colon\; 
     F(x) \otimes_{\mathcal{D}} F(y) 
       \longrightarrow 
     F(x \otimes_{\mathcal{C}} y)
   $$

   for all $x,y \in \mathcal{C}$

satisfying the following conditions:

1. **([[associativity]])** For all objects $x,y,z \in \mathcal{C}$ the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       (F(x) \otimes_{\mathcal{D}} F(y)) \otimes_{\mathcal{D}} F(z)
         &\underoverset{\simeq}{a^{\mathcal{D}}_{F(x),F(y),F(z)}}{\longrightarrow}&
       F(x) \otimes_{\mathcal{D}}( F(y)\otimes_{\mathcal{D}} F(z) )
       \\
       {}^{\mathllap{\mu_{x,y} \otimes id}}\downarrow 
         && 
       \downarrow^{\mathrlap{id\otimes \mu_{y,z}}}
       \\
       F(x \otimes_{\mathcal{C}} y) \otimes_{\mathcal{D}} F(z)
        &&
       F(x) \otimes_{\mathcal{D}} F(y \otimes_{\mathcal{C}} z)
       \\
       {}^{\mathllap{\mu_{x \otimes_{\mathcal{C}} y , z} } }\downarrow 
         && 
       \downarrow^{\mathrlap{\mu_{ x, y \otimes_{\mathcal{C}} z  }}}
       \\
       F( ( x \otimes_{\mathcal{C}} y ) \otimes_{\mathcal{C}} z  )
         &\underset{F(a^{\mathcal{C}}_{x,y,z})}{\longrightarrow}&
       F( x \otimes_{\mathcal{C}} ( y \otimes_{\mathcal{C}} z ) )
     }
   $$

   where $a^{\mathcal{C}}$ and $a^{\mathcal{D}}$ denote the [[associators]] of the monoidal categories;


1. **([[unitality]])** For all $x \in \mathcal{C}$ the following [[commuting diagram|diagrams commute]]

   $$
     \array{
       1_{\mathcal{D}} \otimes_{\mathcal{D}} F(x)
         &\overset{\epsilon \otimes id}{\longrightarrow}&
       F(1_{\mathcal{C}}) \otimes_{\mathcal{D}} F(x)
       \\
       {}^{\mathllap{\ell^{\mathcal{D}}_{F(x)}}}\downarrow 
         && 
       \downarrow^{\mathrlap{\mu_{1_{\mathcal{C}}, x }}}
       \\
       F(x) 
         &\overset{F(\ell^{\mathcal{C}}_x )}{\longleftarrow}&
       F(1 \otimes_{\mathcal{C}} x  )
     }
   $$

   and  

   $$
     \array{
       F(x) \otimes_{\mathcal{D}}  1_{\mathcal{D}}
         &\overset{id \otimes \epsilon }{\longrightarrow}&
       F(x) \otimes_{\mathcal{D}}  F(1_{\mathcal{C}}) 
       \\
       {}^{\mathllap{r^{\mathcal{D}}_{F(x)}}}\downarrow 
         && 
       \downarrow^{\mathrlap{\mu_{x, 1_{\mathcal{C}} }}}
       \\
       F(x) 
         &\overset{F(r^{\mathcal{C}}_x )}{\longleftarrow}&
       F(x \otimes_{\mathcal{C}} 1  )
     }
   $$

   where $\ell^{\mathcal{C}}$, $\ell^{\mathcal{D}}$, $r^{\mathcal{C}}$, $r^{\mathcal{D}}$ denote the left and right [[unitors]] of the two monoidal categories, respectively.

If $\epsilon$ and all $\mu_{x,y}$ are [[isomorphisms]], then $F$ is called a **strong monoidal functor**. (Note that 'strong' is also sometimes applied to 'monoidal functor' to indicate possession of a [[tensorial strength]].) 

=--

+-- {: .num_remark}
###### Remark

In the literature often the term "monoidal functor" refers by default to what in def. \ref{LaxMonoidalFunctor} is called a strong monoidal functor.  With that convention then what def. \ref{LaxMonoidalFunctor} calls a lax monoidal functor is called a  **weak monoidal functor**.  

=--


+-- {: .num_remark}
###### Remark

Lax monoidal functors are the [[lax morphisms]] for an appropriate [[2-monad]].

=--



+-- {: .num_remark}
###### Definition

An __[[oplax monoidal functor]]__ (with various alternative names including **comonoidal**), is a monoidal functor from the [[opposite categories]] $C^{op}$ to $D^{op}$.

=--

+-- {: .num_remark}
###### Definition

A _[[monoidal transformation]]_ between monoidal functors is a [[natural transformation]] that respects the extra structure in an obvious way.

=--


## Properties


+-- {: .num_prop #MonoidsToMonoidsByLaxMonoidal}
###### Proposition
**(Lax monoidal functors send [[monoid]]s to monoids)**

If $F : (C,\otimes) \to (D,\otimes)$ is a lax monoidal functor and 

$$
  (A \in C,\;\; \mu_A : A \otimes A \to A, \; i_A : I \to A)
$$

is a [[monoid object]] in $C$, then the object $F(A)$ is naturally equipped with the structure of a monoid in $D$ by setting

$$
  i_{F(A)} : I_D \stackrel{}{\to} F(I_C) \stackrel{F(i_A)}{\to} F(A)
$$

and

$$
  \mu_{F(A)} : 
  F(A) \otimes F(A)
  \stackrel{\nabla_{F(A), F(A)}}{\to} 
  F(A \otimes A)
  \stackrel{F(\mu_A)}{\to}
  F(A)
  \,.
$$

This construction defines a functor

$$
  Mon(f) : Mon(C) \to Mon(D)
$$

between the [[categories of monoids]] in $C$ and $D$, respectively.

=--

Similarly: 

+-- {: .un_prop #OplaxSendsComonoidsToComonoids}
###### Proposition
**([[oplax monoidal functors]] sends [[comonoids]] to comonoids)**

For $(C,\otimes)$ a [[monoidal category]] write $\mathbf{B}C$ for the corresponding [[delooping]] [[2-category]].

Lax monoidal functor $f : C \to D$ correspond to [[lax 2-functor]] 

$$
  \mathbf{B}F : \mathbf{B}C \to \mathbf{B}D
  \,.
$$

If $F$ is strong monoidal then this is an ordinary [[2-functor]]. If it is strict monoidal, then this is a [[strict 2-functor]].

=--

## String diagrams

Just like monoidal categories, monoidal functors have a [[string diagram]] calculus; see [these slides](http://web.science.mq.edu.au/~mmccurdy/cms2010talk.pdf) for some examples.

## Related concepts

* **monoidal functor**, **strong monoidal functor**

* [[multifunctor]]

* [[module over a monoidal functor]]

* [[monoidal adjunction]]

* [[indexed monoidal category]]

* [[cartesian functor]]

* **lax monoidal functor**

  * [[functor with smash products]]

* [[oplax monoidal functor]]

* [[bilax monoidal functor]]

* [[Frobenius monoidal functor]]

* [[braided monoidal functor]]

* [[symmetric monoidal functor]]

* [[monoidal (∞,1)-functor]]

* [[monoidal (∞,n)-functor]]


## References

* Marcelo Aguiar and Swapneel Mahajan, _Monoidal functors, species and Hopf algebras_. ([pdf](http://pi.math.cornell.edu/~maguiar/a.pdf))

Exposition of basics of [[monoidal categories]] and [[categorical algebra]]:

* _[[geometry of physics -- categories and toposes]]_, Section 2: _[Basic notions of categorical algebra](geometry+of+physics+--+categories+and+toposes#BasicNotionsOfCategoricalAlgebra)_



[[!redirects lax monoidal functor]]
[[!redirects strict monoidal functor]]
[[!redirects strong monoidal functor]]
[[!redirects weak monoidal functor]]
[[!redirects monoidal functors]]
[[!redirects lax monoidal functors]]
[[!redirects strict monoidal functors]]
[[!redirects strong monoidal functors]]
[[!redirects weak monoidal functors]]
[[!redirects strength]]