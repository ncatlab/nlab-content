# Contents # 
* table of contents 
{:toc}

This page describes some nice properties of the [[category]] $R Cocomm Coalg$ of [[cocommutative coalgebra|cocommutative]] [[coalgebras]] over a [[ground ring]] $R$, in particular details of the proof that it is a [[complete category|complete]], [[cocomplete category|cocomplete]], [[lextensive category|lextensive]], [[cartesian closed category]] with a [[generating set]]. 

In the sequel, we will simply say "coalgebra", although we really mean *cocommutative* (coassociative, counital) coalgebra. 

## Colimits 

Colimits in $R Cocomm Coalg$ are created (reflected) by the forgetful functor $U: R Cocomm Coalg \to R Mod$. As the codomain is cocomplete, so is the domain. Thus for example, the coproduct of coalgebras $C, D$ is the direct sum module $C \oplus D$ equipped with the evident comultiplication $C \oplus D \to (C \otimes C) \oplus (D \otimes D) \hookrightarrow (C \oplus D) \otimes (C \oplus D)$. 

It is perhaps well to point out explicitly that if $f: C \to D$ is a coalgebra map, then the [[image]] $f(C)$ in $R Mod$ inherits a coalgebra structure from $D$ and provides the image in $R Cocomm Coalg$. This is an easy consequence of the fact that $f(C \otimes C) = f(C) \otimes f(C)$ as submodules of $D \otimes D$. 

## Local presentability 

Most of the nice properties can be derived as consequences of the [[locally presentable category|local presentability]] of $R Cocomm Coalg$. For this we refer to the paper by [Porst](#Porst). 

In the case where $R$ is a [[field]] $k$, the category $k Cocomm Coalg$ is locally finitely presentable. The finitely presentable objects of $k Cocomm Coalg$ are those coalgebras that are [[finite-dimensional vector space|finite-dimensional]] as [[vector spaces]]. The first step towards establishing locally finite presentability is the fundamental theorem of coalgebras, which guarantees that every coalgebra is a filtered colimit of finite-dimensional coalgebras: 

+-- {: .num_theorem} 
###### Theorem 
Every coalgebra $C$ is the union of its finite-dimensional subcoalgebras, i.e., is the [[directed colimit]] of the system of finite-dimensional subcoalgebras of $C$ and inclusion maps between them. 
=-- 

(For the nonce, we define "subcoalgebra" of $C$ to mean vector subspace $i: V \hookrightarrow C$ such that the restricted comultiplication $\delta_C \circ i$ is contained in the subspace $V \otimes V$ of $C \otimes C$. Later we will see that subcoalgebras are actually the same thing as [[subobjects]] in $k Cocomm Coalg$ in the sense of equivalence classes of [[monomorphisms]].) 

+-- {: .num_prop} 
###### Proposition 
Every finite-dimensional coalgebra $C$ is finitely presentable, i.e., $\hom(C, -): k Cocomm Coalg \to Set$ preserves filtered colimits. 
=-- 

+-- {: .proof} 
###### Proof 
If $D = colim_j D_j$ is a directed colimit, then the image of a coalgebra map $f: C \to D$ is a finite-dimensional subcoalgebra inclusion $f(C) \to D$ which, as a finitely presentable vector space, is included in one of the components $D_j \to D$ of the colimit cone; this inclusion is a subcoalgebra inclusion. 
=-- 

It follows easily from these results and cocompleteness of $k Cocomm Coalg$ that $k Cocomm Coalg$ is locally finitely presentable. As a result we have a [[Gabriel-Ulmer duality|Gabriel-Ulmer]] equivalence 

$$k Cocomm Coalg \simeq Lex(k Cocomm Coalg_{fd}^{op}, Set)$$ 

where the category of finite-dimensional coalgebras is dual to the category of finite-dimensional algebras, so that also 

$$k Cocomm Coalg \simeq Lex(Comm Alg_{fd}, Set).$$ 

Naturally, choosing a representative of each isomorphism class of finite-dimensional coalgebras, we obtain a generating set of $k Cocomm Coalg$. 

## Totality and completeness 

As is the case for any locally presentable category, $R Cocomm Coalg$ is not only cocomplete but is a [[total category|totally cocomplete category]] and is (therefore) [[complete category|complete]] as well. 

The construction of [[limits]] can be described explicitly. The [[equalizer]] of two coalgebra maps $f, g: C \stackrel{\to}{\to} D$ is the largest subcoalgebra contained in the $R Mod$ equalizer (the latter coincides with the equalizer as computed in [[Set]]). This can be described even more explicitly in [[Sweedler notation]]: the equalizer of $f, g$ is the set 

$$E = \{c \in C: c_{(1)} \otimes f(c_{(2)}) \otimes c_{(3)} = c_{(1)} \otimes g(c_{(2)}) \otimes c_{(3)}\}$$ 

with the unique structure of coalgebra that makes it a subcoalgebra of $C$. 

Assuming the construction of [[cofree coalgebra|cofree cocommutative coalgebra]]s, viz. the right adjoint $K: R Mod \to R Cocomm Coalg$ to the forgetful functor $U: R Cocomm Coalg \to R Mod$ (which we also touch on below), the [[product]] of a family of coalgebras $C_i$ can be described as follows. Consider the product $\prod_i C_i$ taken in $R Mod$, and let $p: U K(\prod_i C_i) \to \prod_i C_i$ be the component of the counit of the adjunction $U \dashv K$ at that product. Then the product $C$ of the $C_i$ taken in $R Cocomm Coalg$ is the largest subcoalgebra $j: C \hookrightarrow K(\prod_i C_i)$ such that each composite $\pi_i p j: C \to C_i$ is a coalgebra map. For a proof, see the [article](#Agore) by Agore. 

## Cartesian closure 

The [[cartesian product]] of two coalgebras $C, D$ is given by $C \otimes D$ with the evident coalgebra structure. The functor $C \otimes -: R Cocomm Coalg \to R Cocomm Coalg$ is a [[cocontinuous functor]], since colimits are reflected from $R Mod$ and $C \otimes -: R Mod \to R Mod$ is cocontinuous there. 

For locally presentable or more generally total categories $\mathbf{C}$, cocontinuity of a functor $F: \mathbf{C} \to \mathbf{C}$ is enough to guarantee that $F$ has a right adjoint. It follows that $R Cocomm Coalg$ is cartesian closed. 

## Comonadicity over $R Mod$ 

Again, since $U: R Cocomm Coalg \to R Mod$ is cocontinuous and $R Cocomm Coalg$ is locally presentable, $U$ has a right adjoint $K$. This is described more explicitly at [[cofree coalgebra|cofree cocommutative coalgebra]]. 

The comonadicity of $U$ is proven in the [article](#Barr) by Barr, section 4. 

## Extensivity 

We will show that $k Cocomm Coalg$ is a [[lextensive category]]. 

+-- {: .num_prop} 
###### Proposition 
Coproducts of coalgebras are disjoint. 
=-- 

+-- {: .proof} 
###### Proof 
The coproduct of coalgebras $C, D$ is $C \oplus D$, and the pullback of the two coalgebra inclusions $i_C: C \to C \oplus D, i_D: D \to C \oplus D$ is the coalgebra equalizer of the two maps  

$$\array{
 & & C & &  \\ 
 & _\mathllap{\pi_C} \nearrow & & \searrow _\mathrlap{i_C} \\ 
C \otimes D & & & & C \oplus D \\
 & _\mathllap{\pi_D} \searrow & & \nearrow _\mathrlap{i_D} \\ 
 & & D & &
}$$ 

This coalgebra equalizer is constructed as the largest subcoalgebra of $C \otimes D$ contained in the $k Vect$ equalizer. But the $k Vect$ equalizer is easily seen to be $0$ (cf. the fact that $k Vect$ coproducts are themselves disjoint), and so the coalgebra equalizer must be $0$ as well, concluding the proof. 
=-- 

+-- {: .num_prop} 
###### Proposition 
Coproducts of coalgebras are stable under pullback. 
=-- 

+-- {: .proof} 
###### Proof 
Consider the following diagram: 

$$\array{
& & F & & \\ 
& & \downarrow j & & \\
& & X & & \\ 
& & \downarrow f & & \\ 
C & \underset{i_C}{\to} & C \oplus D & \underset{i_D}{\leftarrow} & D
}$$ 

where $f$ is an arbitrary coalgebra map and $j: F \hookrightarrow X$ is a finite-dimensional subcoalgebra inclusion. We will show that the pullback of the coproduct diagram along $f \circ j$ is a coproduct decomposition of $F$. 
=--

## References 

* {#Barr} [[Michael Barr]], *Coalgebras over a commutative ring*, Journal of Algebra **32** 3 (1974) 600-610 &lbrack;<a href="https://doi.org/10.1016/0021-8693(74)90161-6">doi:10.1016/0021-8693(74)90161-6</a>, [pdf](https://www.math.mcgill.ca/barr/ftp/pdffiles/coalgebra.pdf), [[Barr-Coalgebras.pdf:file]]&rbrack;


* {#Porst} [[Hans-Eberhard Porst]], *On corings and comodules*, Archivum Mathematicum **42** 4 (2006) 419-425 &lbrack;[dmlcz:108017](https://dml.cz/handle/10338.dmlcz/108017), [pdf](http://dml.cz/bitstream/handle/10338.dmlcz/108017/ArchMathRetro_042-2006-4_7.pdf)&rbrack; 
  

* Ana L. Agore, _Limits of Coalgebras, Bialgebras and Hopf Algebras_, arxiv.org/pdf/1003.0318, 2010. ([pdf](http://arxiv.org/pdf/1003.0318.pdf)) 
 {#Agore} 

[[!redirects Cocomm Coalg]]
[[!redirects CommCoalg]]
[[!redirects Comm Coalg]]
[[!redirects category of cocommutative coalgebras]]
[[!redirects category of commutative coalgebras]]

category: category