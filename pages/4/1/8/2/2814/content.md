
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

Let $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ be two [[monoidal categories]]. A **lax monoidal functor** between them is a [[functor]]: 

   $$
     F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}
     \,,
   $$

together with coherence [[maps]]:

1. a [[morphism]]

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

{#StrictMonoidalFunctor} If $\epsilon$ and all $\mu_{x,y}$ are [[isomorphisms]], then $F$ is called a **strong monoidal functor**. 

> (Beware that it has also become common to say "strong monoidal functor" for monoidal functors with *[[tensorial strength]]*, which is different.)   

If they are even [[identity morphisms]], then $F$ is called a **strict monoidal functor**.

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

More generally, lax functors send [[enriched categories]] to enriched categories, an operation known as [[change of enriching category]]. See there for more details.

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


### Relation to multicategories

+-- {: .num_remark}
###### Remark

Lax monoidal functors between monoidal categories are in correspondence with [[morphism of multicategories|morphisms]] between their underlying ([[representable multicategories|representable]]) [[multicategories]].

=--

### Relation to PROs

+-- {: .num_remark}
###### Remark

Strong monoidal functors between monoidal categories are in correspondence with morphisms between their underlying (representable) colored [[PROs]].

=--

+-- {: .num_remark}
###### Remark

Strict monoidal functors between monoidal categories are in correspondence with morphisms between their underlying colored [[PROs]] that preserve the distinguished isomorphisms $() \xrightarrow{\sim} I$ and  $(A, B) \xrightarrow{\sim} (A \otimes B)$ for all $A, B$.

=--


### Relationships between categories of monoidal categories


+-- {: .num_prop}
###### Proposition

The 1-category of strict monoidal categories and strict monoidal functors is not equivalent to the 1-category of monoidal categories and strong monoidal functors.

=--

+-- {: .proof}
###### Proof

The former has an initial object, whereas the latter does not.

=--


+-- {: .num_prop}
###### Proposition

The inclusion from the 1-category of strict monoidal categories and strong monoidal functors into the 1-category of monoidal categories and strong monoidal functors is not an equivalence.

=--

+-- {: .proof}
###### Proof

As mentioned at [[monoidal category#the_2category_of_monoidal_categories|monoidal category]], not every skeletal monoidal category is monoidally equivalent to a strict skeletal monoidal category. Therefore the inclusion is not essentially surjective.

=--


+-- {: .num_prop}
###### Proposition

The inclusion from the 2-category of strict monoidal categories and strict monoidal functors into the 2-category of monoidal categories and strong monoidal functors is not an equivalence.

=--


+-- {: .proof}
###### Proof

Not every strong monoidal functor between strict monoidal categories is equivalent to a strict one. See for example [this MathOverflow question](https://mathoverflow.net/questions/172815/strictifying-strong-monoidal-functors).

=--


+-- {: .num_prop}
###### Proposition

The inclusion of the the 2-category of strict monoidal categories and strong monoidal functors into the 2-category of monoidal categories and strong monoidal functors is an equivalence.

=--


+-- {: .proof}
###### Proof

By the [[coherence theorem for monoidal categories]], every monoidal category is strong monoidally equivalent to a strict one.

=--


## String diagrams

Just like monoidal categories, monoidal functors have a [[string diagram]] calculus; see [these slides](https://web.archive.org/web/20191021024946/http://web.science.mq.edu.au/~mmccurdy/cms2010talk.pdf) for some examples.

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

* [[idempotent monoidal functor]]

* [[monoidal (∞,1)-functor]]

* [[monoidal (∞,n)-functor]]


## References

* {#EK65} [[Samuel Eilenberg]], [[G. Max Kelly]], p. 473 in: *Closed Categories*, in:  [[Samuel Eilenberg|S. Eilenberg]], [[D. K. Harrison]], [[S. MacLane]], [[H. Röhrl]] (eds.): *[[Proceedings of the Conference on Categorical Algebra - La Jolla 1965]]*, Springer (1966) 421-562 &lbrack;[doi:10.1007/978-3-642-99902-4](https://doi.org/10.1007/978-3-642-99902-4)&rbrack;

* [[Saunders MacLane]], §XI.2 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5** Springer (second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

* {#EGNO15} [[Pavel Etingof]], [[Shlomo Gelaki]], [[Dmitri Nikshych]], [[Victor Ostrik]], §2.4 in: *Tensor Categories*, AMS Mathematical Surveys and Monographs **205** (2015) &lbrack;[ISBN:978-1-4704-3441-0](https://bookstore.ams.org/surv-205), [pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf)&rbrack;

  > (discussed what we call *[[strong monoidal functors]]*)


* [[Marcelo Aguiar]] and Swapneel Mahajan, _Monoidal functors, species and Hopf algebras_. ([pdf](http://pi.math.cornell.edu/~maguiar/a.pdf))

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